---
name: deep-dive
description: Selects one high-impact article from RSS feeds and produces a long-form feature report with independent research. Focuses on industry transformation, AI replacing humans, business model disruption, and developer ecosystem shifts.
argument-hint: "[optional: topic keyword or article URL]"
disable-model-invocation: false
user-invocable: true
allowed-tools: Task, WebFetch, WebSearch, Read, Write, Bash(date*), Bash(ls*), Bash(node *), Bash(test *), Bash(docker *), Bash(git *), Bash(rm *)
---

# Deep Dive — RSS 選題 + 獨立研究 → 深度專題報導

> **Source**: Miniflux RSS (選題) + WebSearch + WebFetch (獨立研究)
> **Strategy**: RSS 選出一篇最值得深挖的文章，再用網路搜尋補充多方資料，寫成深度專題
> **Publish**: GitHub Pages (Jekyll) + Discord notification
> **Language**: Traditional Chinese (繁體中文)
> **Length**: 6000-8000 字（雜誌專題等級）

## Core Architecture

```
┌──────────────────────────────────────────────────────────────────┐
│                     Deep Dive Agent (Orchestrator)                │
├──────────────────────────────────────────────────────────────────┤
│                                                                   │
│   ┌──────────┐    ┌──────────┐    ┌──────────┐    ┌──────────┐  │
│   │ Phase 1  │ →  │ Phase 2  │ →  │ Phase 3  │ →  │ Phase 4  │  │
│   │ Source   │    │ Deep     │    │ Research │    │ Write    │  │
│   │ Select   │    │ Read     │    │ & Verify │    │ Report   │  │
│   └──────────┘    └──────────┘    └──────────┘    └──────────┘  │
│       │                │                │                │       │
│       ▼                ▼                ▼                ▼       │
│   RSS entries →    Full article    WebSearch for      6000-8000  │
│   pick THE ONE     content         related sources    字專題報導  │
│                                                                   │
│   ┌──────────┐    ┌──────────┐    ┌──────────┐                  │
│   │ Phase 5  │ →  │ Phase 6  │ →  │ Phase 7  │                  │
│   │ Mark     │    │ Publish  │    │ Discord  │                  │
│   │ Read     │    │ Pages    │    │ Notify   │                  │
│   └──────────┘    └──────────┘    └──────────┘                  │
│       │                │                │                        │
│       ▼                ▼                ▼                        │
│   Miniflux API    git push →      Send summary                  │
│   mark as read    GitHub Pages    to Discord                     │
│                                                                   │
└──────────────────────────────────────────────────────────────────┘
```

## Phase 0: Load SOUL

Before starting any phase, **read `SOUL.md`** from the project root to load the author persona.

```yaml
Steps:
  1. Read SOUL.md from the project root (ai-digest/SOUL.md)
  2. Internalize the persona: identity, writing style, tone, attitude, dos & don'ts
  3. ALL written content must reflect the SOUL.md persona throughout
  4. The persona nickname must NEVER appear in published content
  5. Deep Dive 的語氣比日報更沉穩，但依然保持矽谷浪人的個性
     — 可以更慢、更深、更有分量，但不能變成學術論文
```

## Execution Process

### Phase 1: Source Selection — 找到那篇最值得深挖的文章

Two modes depending on user input:

**Mode A — 自動選題 (no argument or keyword argument):**

```yaml
Steps:
  0. Pre-flight: ensure Miniflux is running
     docker ps --filter name=miniflux --format '{{.Names}}' | grep -q miniflux
     - If NOT running: inform user to start Miniflux first
  1. Determine lookback window:
     - Default: 7 days (deep-dive looks at a wider window than daily digest)
     - Calculate "after" timestamp: date -v-7d +%s (macOS)
  2. Fetch unread entries — two queries:
     Query 1 — Main pool (AI category, category_id=3):
       node ~/.claude/skills/miniflux/client.mjs entries --status unread --limit 200 --category 3 --after <unix_timestamp> --direction desc
     Query 2 — Blog pool (AI-Blogs category, category_id=7):
       node ~/.claude/skills/miniflux/client.mjs entries --status unread --limit 50 --category 7 --after <unix_timestamp> --direction desc
     → Merge both pools. Blog entries are often excellent deep-dive candidates (long-form analysis).
  3. If user provided a keyword argument (e.g., /deep-dive agents):
     - Filter entries whose title or content_preview match the keyword
  3a. Dedup check — avoid repeating recent topics:
     - Run: ls _posts/ | grep deep-dive | tail -14
     - Read the titles of deep-dive posts from the last 14 days
     - If a candidate topic overlaps significantly with a recent deep-dive, deprioritize it
     - "Overlap" = same company + same event, or same core thesis
  4. Score each entry for DEEP-DIVE WORTHINESS (not same as daily digest scoring):

Deep-Dive Selection Criteria (score 1-10):
  Priority topics (score boost +3):
    - 產業大轉變: Signs of fundamental industry shifts, paradigm changes
      Examples: "AWS AI agent took down production" (AI reliability crisis), "SaaS tsunami" (AI disrupting entire software category), "llama.cpp acquired by Meta" (open-source AI consolidation)
    - 人類被取代: AI replacing human jobs, automation of cognitive work
      MUST have concrete evidence (layoff data, productivity metrics, case studies) — not speculation or opinion pieces
    - 商業模式衝擊: Business model disruption — focus on "how money is made differently now"
      Examples: AI-first pricing models, per-token economics killing seat-based SaaS, open-source models commoditizing proprietary APIs
    - 開發者生態: Developer workflow revolution, fundamental changes in how developers work
      Examples: AI coding agents replacing junior dev tasks, new IDE paradigms, shift from writing code to reviewing AI-generated code
  High score indicators:
    - The article reveals a trend, not just a product launch
    - It has implications beyond the immediate news
    - There are multiple angles to explore (technical, business, societal)
    - It connects to a bigger narrative about where AI is heading
    - It would benefit from cross-referencing with other sources
  Low score indicators:
    - Pure product announcement with no deeper implications
    - Already well-covered topic with nothing new to add
    - Too niche or technical to sustain a 6000+ word analysis
    - Topic already covered in a recent deep-dive (see dedup check in step 3a)

  5. Select THE ONE article with the highest score
     - Present the top 3 candidates to yourself with reasoning
     - Pick the one with the richest potential for deep analysis
     - Record: title, url, entry_id, feed_name, selection_reasoning
```

**Mode B — 指定文章 (user provides a URL):**

```yaml
Steps:
  1. User provides a specific article URL
  2. Skip RSS scoring, use the provided URL directly
  3. Proceed to Phase 2
```

### Phase 2: Deep Read — 完整閱讀選中的文章

```yaml
Steps:
  1. Read the full article content:
     Method 1 — Miniflux fetch-content (if from RSS):
       node ~/.claude/skills/miniflux/client.mjs fetch-content <entry_id>
     Method 2 — WebFetch (if URL provided or Miniflux returns empty):
       Use WebFetch to read the article URL directly

  2. Extract and internalize:
     - Core thesis / main argument of the article
     - Key facts, data points, quotes
     - Companies, people, technologies mentioned
     - The "so what" — why does this matter beyond the headline
     - Gaps in the article — what questions does it NOT answer?
     - What would a reader want to know more about?

  3. Formulate research questions (5-8 questions):
     These guide Phase 3 research. Must cover multiple dimensions:
     Technical dimension:
     - "What is the technical mechanism behind this? How does it actually work?"
     - "What are the technical limitations or caveats not mentioned?"
     Industry dimension:
     - "What do other analysts say about this trend?"
     - "How does this affect the competitive landscape?"
     - "What business models does this enable or destroy?"
     Human/societal dimension:
     - "What jobs or roles are directly impacted?"
     - "Are there contradicting data points or viewpoints?"
     - "What historical precedents exist for this kind of shift?"
     Forward-looking:
     - "What are the second and third-order effects?"
     - "What would need to happen for this to succeed/fail?"
```

### Phase 3: Research & Verify — 獨立研究，不靠通用知識

This is the critical differentiator from a regular summary. The Agent MUST do independent research.

```yaml
Steps:
  1. For each research question from Phase 2, conduct WebSearch:
     - Use specific, targeted search queries
     - Search in both English and Chinese where relevant
     - Look for: expert analyses, data reports, opposing viewpoints, historical context

  2. For the most promising search results (5-8 articles), do WebFetch:
     - Read the full content of each source
     - Extract relevant quotes, data points, statistics, and perspectives
     - Note the source credibility, author expertise, and publication date
     - Look specifically for: concrete numbers, expert quotes, case studies, counter-arguments

  3. Conduct a SECOND round of research if needed:
     - Based on what you learned in the first round, formulate follow-up queries
     - Dig deeper into the most interesting threads
     - Seek out primary sources (original papers, official announcements, earnings reports)
     - Look for regional perspectives (US, China, EU, Taiwan/Asia) if relevant

  4. Cross-reference and synthesize:
     - Identify agreements and disagreements between sources
     - Find data points that support or challenge the original article
     - Discover angles the original article missed
     - Map out cause-and-effect chains
     - Identify who wins, who loses, and why
     - Build a multi-dimensional understanding of the topic

  5. Compile research notes:
     - List all sources with URLs (for citations)
     - Key findings from each source
     - Your own analysis connecting the dots
     - Identify the strongest narrative thread for the report

Research Quality Standards:
  - Minimum 5 additional sources beyond the original article
  - At least 2 sources should present different or opposing perspectives
  - At least 1 source with concrete data (numbers, statistics, market data)
  - Prefer recent sources (within 3 months)
  - Prefer authoritative sources (established publications, expert blogs, research papers)
  - NEVER fabricate sources or quotes
  - If a search yields no useful results, note the gap honestly
```

### Phase 4: Write Report — 撰寫深度專題報導

```yaml
SEO Title Generation (繁體中文):
  - Capture the article's core tension or revelation
  - Must be specific and thought-provoking
  - 25-50 characters
  - Examples:
    - "當 AI 學會寫程式：軟體工程師的生存指南"
    - "OpenAI 的 Agent 野心背後：誰會是最大輸家？"
    - "Scaling Law 撞牆之後：AI 產業的下一個十年"

Slug Generation:
  - Based on the core topic
  - Format: lowercase English, hyphen-separated, max 6 words
  - Prefix: deep-dive-
  - Examples:
    - "deep-dive-ai-replacing-developers"
    - "deep-dive-openai-agent-ecosystem"
    - "deep-dive-scaling-law-plateau"

Tags:
  - MUST include: deep-dive
  - Also include relevant ones from: llm, agents, ai-tools, ai-research, ai-industry, ai-safety, mlops, ai-coding

Jekyll Front Matter:
  ---
  title: "<SEO Title>"
  date: YYYY-MM-DD
  description: "<80-120 字繁中摘要，點出核心問題和關鍵洞見>"
  tags: [deep-dive, ...]
  ---

Content Structure (專題報導風, 6000-8000 字):

  NO H1 title — Jekyll front matter `title` already renders as the page heading.
  IMPORTANT: 6000-8000 字是硬性要求，不是建議。每個章節都要充分展開。

  ## 引言 — Hook（約 500-800 字）
  - 3-4 段，從原始文章的核心發現切入
  - 用一個具體的場景、數據或引述抓住注意力
  - 可以用一個小故事或假想情境開場（例如：「想像你是一個 2024 年的初級工程師...」）
  - 點出核心問題：這件事為什麼重要？為什麼現在？
  - 預告文章會帶讀者看到什麼——給讀者一個繼續讀下去的理由
  - 在引言段落末尾標注觸發本文的原始文章連結

  ## 事件全貌 — What Happened（約 800-1200 字）
  - 4-5 段，完整還原事件本身
  - 不只是「某公司發布了某產品」，而是交代完整的事件脈絡
  - 關鍵數據、技術細節、官方說法
  - 與前代產品或競品的具體比較（附數據）
  - 引用原始報導和官方來源（附內文連結）

  ## 脈絡 — Context & History（約 800-1200 字）
  - 4-5 段，把事件放進更大的歷史脈絡中
  - 這個趨勢/事件是怎麼走到今天的？回溯關鍵里程碑
  - 引用研究資料中的數據和事實（附內文連結）
  - 類似的歷史事件或類比（科技史上有沒有類似的轉折？）
  - 讓讀者理解「為什麼是現在」——什麼條件成熟了？

  ## 多方觀點 — Perspectives（約 1000-1500 字）
  - 5-6 段，呈現不同陣營的聲音
  - 樂觀派怎麼看？具體引用誰說了什麼（附來源連結）
  - 悲觀派 / 質疑派怎麼看？他們的擔憂有沒有道理？
  - 實務工作者怎麼看？（第一線使用者、開發者的真實反饋）
  - 不同地區的觀點差異（美國 vs 中國 vs 歐盟 vs 台灣/亞洲，如果相關的話）
  - 你自己的觀點（用矽谷浪人的語氣，有立場但不偏激）
  - 不要只是列出觀點，要分析這些觀點之間的張力和矛盾

  ## 產業衝擊 — Impact Analysis（約 1000-1500 字）
  - 5-6 段，層層剖析實際影響
  - **第一層：直接受影響者** — 誰會受益？誰會受損？具體的職位、公司、產業
  - **第二層：商業模式衝擊** — 現有的商業模式會怎麼變？新的商業模式是什麼？
  - **第三層：開發者生態** — 對開發者的工具鏈、工作流程、技能需求有什麼影響？
  - **第四層：二階效應** — 連鎖反應是什麼？這件事會觸發什麼後續發展？
  - 用具體案例、數據或類比來支撐分析（附連結）
  - 可以用「如果...那麼...」的推演框架

  ## 未來展望 — What's Next（約 800-1200 字）
  - 4-5 段，有層次地往前看
  - **短期（3-6 個月）**：幾乎確定會發生的事
  - **中期（6-18 個月）**：可能的發展路徑，列出 2-3 種情境
  - **長期推演**：如果這個趨勢持續下去，3-5 年後世界會長什麼樣？
  - **給讀者的行動建議** — 實用、具體、不說教：
    - 如果你是開發者，現在應該學什麼 / 做什麼
    - 如果你是創業者 / 產品經理，應該關注什麼
    - 如果你是一般科技從業者，怎麼為這個變化做準備
  - 結尾收在一個有力的觀點或發人深省的問題上

  ---

  ## 延伸閱讀

  列出本文引用和參考的所有來源，分類整理：
  - [標題 — 來源名稱](URL)：一句話說明這篇的價值
  - [標題 — 來源名稱](URL)：一句話說明
  - ...（至少 6 個來源）

Writing Style Notes:
  - 比日報更沉穩、更有分量，但不失矽谷浪人的個性
  - 段落可以更長，論述可以更完整展開
  - 每個段落都要有新的資訊或觀點，嚴禁水字數
  - 善用小標題（###）、粗體、列表來增加長文的可讀性
  - 資料引用要自然融入文中，不像學術論文
  - 適度使用具體數字和案例讓抽象觀點落地
  - 可以穿插短小的「側寫」或「案例框」來增加可讀性
  - 最後的延伸閱讀不只是列連結，要告訴讀者每篇的價值
  - 整篇文章要有一條清晰的敘事主線，從頭到尾都在回答一個核心問題

Output:
  - Write directly to: _posts/YYYY-MM-DD-<slug>.md
```

### Phase 5: Mark Read

```yaml
Steps:
  1. If article was from RSS (Mode A), mark it as read in Miniflux:
     node ~/.claude/skills/miniflux/client.mjs mark-read <entry_id>
  2. If article was user-provided URL (Mode B), skip this step
```

### Phase 6: Publish to GitHub Pages

```yaml
GitHub Pages URL base: https://eagle-cool.github.io/ai-digest

Steps:
  1. Pull, commit, and push:
     git add -A && git commit -m "YYYY-MM-DD: <slug>" && git pull --rebase && git push
  2. Construct page URL:
     https://eagle-cool.github.io/ai-digest/posts/<slug>/
  3. Wait 30 seconds for GitHub Pages to build, then verify once with WebFetch:
     - If live: proceed to Phase 7
     - If not live: proceed to Phase 7 anyway
```

### Phase 7: Discord Notification

```yaml
Steps:
  1. Check .env exists (if not: skip, inform user)
  2. Compose message (繁體中文, max 1800 chars):
     Format below
  3. Send text message:
     node ~/.claude/skills/discord-send/send.mjs ai-digest --text "<message>"
  4. Best-effort: failure does not affect report
```

**Discord message template:**

```
🔬 深度專題：<Title>

<2-3 句核心觀點摘要，點出為什麼值得花 20 分鐘讀>

📖 <URL>
```

## Output Template

```markdown
---
title: "<SEO Title>"
date: YYYY-MM-DD
description: "<80-120 字摘要>"
tags: [deep-dive, llm, agents]
---

## 引言

[3-4 段 Hook — 用一個具體的場景、數據或小故事開場]

[點出核心問題，為什麼這件事值得花 20 分鐘深讀]

[預告文章會帶讀者看到什麼]

[原始文章引用：這篇報導的起點是 [文章標題](URL)，但故事遠不止於此。]

---

## 事件全貌

[4-5 段完整還原事件]

[關鍵數據、技術細節、官方說法]

[與前代產品或競品的具體比較]

[引用原始報導和官方來源]

---

## 脈絡

[4-5 段歷史背景]

[回溯關鍵里程碑和轉折點]

[引用研究資料（[來源](URL)）]

[類似的歷史類比，為什麼是現在]

---

## 多方觀點

[樂觀派觀點 + 具體引用來源]

[悲觀派 / 質疑觀點 + 具體引用來源]

[實務工作者的第一線反饋]

[不同地區的觀點差異（如相關）]

[矽谷浪人自己的看法 — 有立場、有根據、分析觀點之間的張力]

---

## 產業衝擊

[直接受影響者：誰受益？誰受損？具體職位和產業]

[商業模式衝擊：現有模式怎麼變？新模式是什麼？]

[開發者生態：工具鏈、工作流程、技能需求的變化]

[二階效應：連鎖反應和後續發展推演]

[具體案例或數據支撐]

---

## 未來展望

[短期（3-6 個月）：幾乎確定會發生的事]

[中期（6-18 個月）：2-3 種可能的發展情境]

[長期推演：3-5 年後的世界]

[給讀者的行動建議 — 依角色分別建議（開發者/創業者/一般從業者）]

[收在一個有力的觀點或發人深省的問題上]

---

## 延伸閱讀

- [標題 — 來源](URL)：這篇的價值一句話
- [標題 — 來源](URL)：這篇的價值一句話
- [標題 — 來源](URL)：這篇的價值一句話
- [標題 — 來源](URL)：這篇的價值一句話
- [標題 — 來源](URL)：這篇的價值一句話
- [標題 — 來源](URL)：這篇的價值一句話
```

## Constraints & Principles

1. **One Article, One Deep Dive**: 每次只選一篇文章深挖，不是做摘要集錦。
2. **Research-Backed**: 必須做獨立研究（WebSearch + WebFetch），不能只靠通用知識或原文內容。至少引用 5 個額外來源，做至少 2 輪搜尋。
3. **Opinion with Evidence**: 可以有強烈觀點，但每個觀點都要有事實或數據支撐。
4. **No Filler, But Go Deep**: 6000-8000 字的每一段都要有新資訊或新觀點，嚴禁水字數。深度不是廢話多，而是每個面向都挖得夠深。
4a. **Length is Non-Negotiable**: 6000 字是下限，不是目標。如果寫完不到 6000 字，回頭檢查是不是有面向沒展開、有觀點沒支撐、有案例沒舉。
5. **Honest Gaps**: 如果研究中發現資訊不足或不確定的地方，誠實說明，不要硬掰。
6. **SOUL.md First**: 所有內容必須符合 SOUL.md 的人格設定和語氣。
7. **No Implementation Leaks**: 不提 RSS、Miniflux、feeds、aggregation 等內部工具。
8. **Source Attribution**: 所有引用的外部資料都要附上連結，文末整理延伸閱讀。
9. **Deep-Dive Tag**: 所有深度專題文章必須包含 `deep-dive` tag，以便與日報區分。
10. **Selection Transparency**: 在寫作前，先在心中確認為什麼選這篇、能從什麼角度深挖、有什麼核心問題值得追。

## Error Handling

| Error | Handling |
|-------|---------|
| Miniflux unreachable | Run healthcheck, report error, stop |
| 0 unread entries | Report "no articles found for deep dive", stop |
| No article scores high enough | Report "no article worthy of deep dive this week", stop |
| WebSearch returns no useful results | Note the gap, rely more on original article + general analysis |
| WebFetch fails for a research source | Skip that source, note it, continue with others |
| git push fails | Report error, report still saved locally in _posts/ |
| Discord send fails | Log error, do not affect report |
