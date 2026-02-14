---
name: generate-post
description: Generates daily AI news digests from Miniflux RSS feeds (AI category). Publishes to GitHub Pages and notifies via Discord.
argument-hint: "[optional: date]"
disable-model-invocation: false
user-invocable: true
allowed-tools: Task, WebFetch, Read, Write, Bash(mkdir*), Bash(date*), Bash(ls*), Bash(node *), Bash(test *), Bash(docker *), Bash(git *), Bash(cp *), Bash(rm *)
---

# AI Digest — RSS-First AI News → GitHub Pages

> **Source**: Miniflux RSS aggregator (AI category, ~30 feeds)
> **Strategy**: RSS for bulk retrieval, Agent for quality evaluation, WebFetch only for deep-reading
> **Publish**: GitHub Pages (Jekyll) + Discord notification
> **Language**: Traditional Chinese (繁體中文) - titles keep original English, summaries in Traditional Chinese

## Core Architecture

```
┌──────────────────────────────────────────────────────────────────┐
│                     Main Agent (Orchestrator)                     │
├──────────────────────────────────────────────────────────────────┤
│                                                                   │
│   ┌──────────┐    ┌──────────┐    ┌──────────┐    ┌──────────┐  │
│   │ Phase 1  │ →  │ Phase 2  │ →  │ Phase 3  │ →  │ Phase 4  │  │
│   │ Fetch    │    │ Filter & │    │ Deep     │    │ Generate │  │
│   │ RSS Data │    │ Evaluate │    │ Read     │    │ Report   │  │
│   └──────────┘    └──────────┘    └──────────┘    └──────────┘  │
│       │                │                │                │       │
│       ▼                ▼                ▼                ▼       │
│   Miniflux API    Agent scores    WebFetch top 3    Markdown     │
│   → AI category   title/desc     articles only     + slug       │
│     (1 API call)   (no fetch)     (optional)                     │
│                                                                   │
│   ┌──────────┐    ┌──────────┐    ┌──────────┐                  │
│   │ Phase 5  │ →  │ Phase 6  │ →  │ Phase 7  │                  │
│   │ Mark     │    │ Publish  │    │ Discord  │                  │
│   │ Read     │    │ Pages    │    │ Notify   │                  │
│   └──────────┘    └──────────┘    └──────────┘                  │
│       │                │                │                        │
│       ▼                ▼                ▼                        │
│   Miniflux API    git push →      Send URL +                    │
│   mark as read    GitHub Pages    summary text                   │
│                                                                   │
└──────────────────────────────────────────────────────────────────┘
         ↕ REST API (via client.mjs)
┌────────────────────┐
│   Miniflux         │  ← AI category feeds (~30 sources)
│   (always running) │  ← Handles caching, dedup, parsing
└────────────────────┘
```

## Phase 0: Load SOUL

Before starting any phase, **read `SOUL.md`** from the project root to load the author persona.

```yaml
Steps:
  1. Read SOUL.md from the project root (ai-digest/SOUL.md)
  2. Internalize the persona: identity, writing style, tone, attitude, dos & don'ts
  3. ALL written content (editorial intro, summaries, key points, why it matters, Discord message)
     must reflect the SOUL.md persona throughout
  4. The persona nickname must NEVER appear in published content
```

## Execution Process

### Phase 1: Fetch RSS Data

Retrieve unread entries from Miniflux **AI category only** (category_id = 3).

```yaml
Steps:
  0. Pre-flight: ensure Miniflux is running
     docker ps --filter name=miniflux --format '{{.Names}}' | grep -q miniflux
     - If NOT running: inform user to start Miniflux first, then verify with healthcheck:
       node ~/.claude/skills/miniflux/client.mjs healthcheck
  1. Determine target date (user argument or today via `date +%Y-%m-%d`)
  2. Create output directory: mkdir -p NewsReport/
  3. Calculate "after" timestamp (3 days before target date):
     # Use: date -v-3d +%s (macOS) or date -d '3 days ago' +%s (Linux)
  4. Fetch unread entries from Miniflux WITH category and time filter:
     node ~/.claude/skills/miniflux/client.mjs entries --status unread --limit 200 --category 3 --after <unix_timestamp> --direction desc
     → IMPORTANT: Always use --category 3 to filter AI feeds only
     → IMPORTANT: Always use --after to avoid pulling old imported articles
     → Returns JSON: { total, count, entries: [{ id, title, url, feed, published, content_preview }] }
  5. If total == 0, check if Miniflux is healthy:
     node ~/.claude/skills/miniflux/client.mjs healthcheck
     - If unhealthy: report error and stop
     - If healthy but 0 entries: report "no new AI content today"
```

### Phase 2: Filter & Evaluate (Agent — metadata only)

The Agent evaluates entries based on title + content_preview (RSS description). No web fetching needed.

```yaml
Input: Array of entries from Phase 1 (title, url, feed, content_preview)

Agent Evaluation Criteria:
  Include (AI-focused topics):
    - LLM: Model releases, benchmarks, training techniques, fine-tuning, inference optimization
    - AI Agents: Agent frameworks, autonomous workflows, tool use, planning systems
    - AI Coding: AI-assisted development tools, code generation, IDE integrations
    - AI Products: ChatGPT, Claude, Gemini, Copilot, Cursor, and other AI SaaS
    - AI Research: Papers with practical implications, alignment research, safety
    - AI Industry: Funding, acquisitions, partnerships, regulatory developments
    - AI Infrastructure: GPU supply, cloud AI services, training clusters, MLOps
  Exclude:
    - Non-AI tech content (frontend, systems, DevOps, security)
    - Marketing puff / PR without substance
    - Crypto/Blockchain (unless AI-related)
    - Job postings / hiring announcements
    - Content older than 3 days

Deduplication:
  - Handled by Miniflux read/unread status (selected articles are marked read after report)
  - Title similarity check (>80% = duplicate)

Scoring (1-5):
  - 5: Major model release, breaking AI industry news, groundbreaking research
  - 4: High-quality AI technical deep-dive, significant product update
  - 3: Interesting AI content, useful AI tutorial or analysis
  - 2: Okay content, niche AI interest
  - 1: Low quality or barely relevant to AI

Output: Tiered selection for the digest:
  Tier 1 — 🌊 今日浪頭 (3 articles, score 4-5):
    - The day's biggest AI waves, will get deep-read + rich summaries
  Tier 2 — ⚡ 衝浪快報 (8-12 articles, score 3-4):
    - Worth knowing, one-liner summaries only
  Tier 3 — 🏄 深水區 (3-5 articles, score 3+):
    - Long-form AI essays, research papers, or deep-dives worth diving into

  Each entry includes:
    - title (original English)
    - url
    - feed_name
    - tier: 1 | 2 | 3
    - quality_score: 1-5
    - summary_hint: 1-sentence description from content_preview (繁體中文)
    - entry_id: Miniflux entry ID (for marking as read later)
```

### Phase 3: Deep Read (Tier 1 articles only)

Only the 3 Tier 1 (🔥 今日焦點) articles get deep-read for rich summaries.

```yaml
Strategy:
  - Deep-read ALL Tier 1 articles (3 articles)
  - Tier 2 and Tier 3 use content_preview only — no fetching
  - Maximum 3 deep-reads per run (cost control)

Method 1 — Miniflux fetch-content (preferred, zero-cost):
  node ~/.claude/skills/miniflux/client.mjs fetch-content <entry_id>
  → Returns original article HTML content fetched by Miniflux

Method 2 — WebFetch fallback (if Miniflux fetch-content returns empty):
  Use WebFetch to read the article URL directly
  → Agent extracts key information from the page

For each Tier 1 article, produce:
  - summary: 3-4 sentence summary (繁體中文), written like you just tried the thing and are telling a friend.
    Use first-person perspective where natural (「我試了一下」「以我的觀察」).
    Balance excitement with substance — hype is cheap, insight is gold.
  - key_points: 2-3 key takeaways (繁體中文), punchy and direct
  - so_what: 1 sentence on "so what?" / broader impact (繁體中文), connecting to trends the reader cares about

For Tier 2 articles: 1 sentence with a dash of personality — not a boring rewrite of the title.
For Tier 3 articles: 1 sentence pitch on why it's worth the deep dive — sell the read, not the headline.
```

### Phase 4: Generate Report + Slug + SEO Title

```yaml
SEO Title Generation (繁體中文):
  - Capture the day's AI vibe in one punchy line — like a surfer describing today's waves
  - Must be specific and informative, NOT generic like "每日 AI 日報"
  - Include key model names, companies, or AI concepts from top articles
  - Tone: casual-confident, the kind of thing you'd text a friend
  - 20-40 characters, no date in title (date is in front matter)
  - Examples:
    - "GPT-5 多模態真的猛、Claude 4 Agent 直接起飛"
    - "Llama 4 開源炸場、OpenAI Agents SDK 終於來了"
    - "Scaling Law 見頂之爭、Gemini 3 悄悄登場"

Slug Generation:
  - Based on the top 2-3 AI highlights of the day
  - Format: lowercase English, hyphen-separated, max 6 words
  - Examples:
    - "gpt5-multimodal-claude4-agents"
    - "llama4-opensource-openai-agents-sdk"
    - "dario-amodei-gemini3-ai-scaling"
  - The slug is used for both the filename and the Jekyll URL

Tags (only use relevant ones from this set):
  - llm, agents, ai-tools, ai-research, ai-industry, ai-safety, mlops, ai-coding

Output:
  - Directory: NewsReport/
  - Filename: YYYY-MM-DD-<slug>.md
  - Format: Standard Markdown with Jekyll front matter
  - Language: Traditional Chinese (titles keep original English)

Jekyll Front Matter (MUST be included at top of file):
  ---
  title: "<SEO Title>"
  date: YYYY-MM-DD
  description: "<50-80 字繁中摘要，適合 Google 搜尋結果片段>"
  tags: [llm, agents, ...]  # only include relevant categories
  ---

Content Structure (after front matter):
  - NO H1 title — Jekyll front matter `title` already renders as the page heading
  - Editorial intro (2-3 sentences, 繁中): like you're texting a friend about what's hot today.
    Use wave/surfing metaphors naturally. Set the vibe for the whole post.
    Example tone: "今天 AI 圈的浪有點猛——OpenAI 丟了個大的出來，Google 也不甘示弱。但最讓我興奮的其實是..."
  - 🌊 今日浪頭 (3 articles): deep coverage, first-person perspective, share your take
  - ⚡ 衝浪快報 (8-12 articles): one-liner each, scannable, with personality
  - 🏄 深水區 (3-5 articles): long-form worth diving into, sell the read
  - NO mention of RSS, Miniflux, feeds, or aggregation in published content
  - NO "execution mode" or "version" info — this is editorial content, not a system report
```

### Phase 5: Mark Read

```yaml
Steps:
  1. Mark all selected entries as read in Miniflux:
     node ~/.claude/skills/miniflux/client.mjs mark-read <id1,id2,id3,...>
```

### Phase 6: Publish to GitHub Pages

This skill runs inside the ai-digest Jekyll repo. Posts are written directly to `_posts/`.

```yaml
GitHub Pages URL base: https://eagle-cool.github.io/ai-digest

Steps:
  1. Copy report to Jekyll _posts directory:
     cp "NewsReport/YYYY-MM-DD-<slug>.md" "_posts/YYYY-MM-DD-<slug>.md"
  2. Pull, commit, and push:
     git add -A && git commit -m "YYYY-MM-DD: <slug>" && git pull --rebase && git push
  4. Construct page URL:
     https://eagle-cool.github.io/ai-digest/posts/<slug>/
  5. Wait 30 seconds for GitHub Pages to build, then verify once with WebFetch:
     - If live: proceed to Phase 7
     - If not live: proceed to Phase 7 anyway (typically builds within 30s)
```

### Phase 7: Discord Notification

```yaml
Steps:
  1. Check .env exists (if not: skip, inform user)
  2. Compose message (繁體中文, max 1800 chars):
     - Page URL
     - Top 3 highlights + 3 notable items
  3. Send text message (no file attachment):
     node ~/.claude/skills/discord-send/send.mjs ai-digest --text "<message>"
  4. Best-effort: failure does not affect report
```

**Discord message template:**

```
🌊 <SEO Title>

今日浪頭
• [標題] — 一句話摘要（帶觀點）
• [標題] — 一句話摘要
• [標題] — 一句話摘要

⚡ 另有 N 則快報 + N 篇深水區

🏄 <URL>
```

## Output Template

```markdown
---
title: "<SEO Title>"
date: YYYY-MM-DD
description: "<50-80 字摘要，用矽谷浪人口吻，適合搜尋結果片段>"
tags: [llm, agents]
---

今天 AI 的浪有點猛——...(2-3 句開場，像在跟朋友分享今天看到最炸的東西。自然帶出主題，不要列舉式。)

---

## 🌊 今日浪頭

### [Article Title](URL)

3-4 句，用「我看了一下」「這東西的厲害之處在於」的口吻。不只說發生了什麼，更要說你怎麼看、對我們有什麼影響。可以興奮，但要有根據。

**為什麼這道浪值得追：**
- 重點一（帶觀點）
- 重點二
- 對開發者/使用者的實際影響

### [Article Title](URL)

（同上格式，共 3 篇浪頭文章）

---

## ⚡ 衝浪快報

- **[Article Title](URL)** — 一句話帶過，但要有個人觀感，不是冷冰冰的摘要
- **[Article Title](URL)** — 可以帶點情緒：驚喜、吐槽、期待都行
- **[Article Title](URL)** — 讓讀者掃一眼就知道要不要點進去
- ...（共 8-12 則）

---

## 🏄 深水區

- **[Article Title](URL)** — 用一句話賣這篇文章：為什麼值得花 15 分鐘讀
- **[Article Title](URL)** — 點出這篇的獨特之處，不是重複標題
- ...（共 3-5 則）
```

## Constraints & Principles

1. **RSS-First**: Always use Miniflux API for data retrieval. Never scrape source websites for listing.
2. **AI Category Only**: Always filter by `--category 3` to get AI feeds only.
3. **Agent for Evaluation Only**: Agent reads title/description to score and filter. No web fetching for listing.
4. **Deep Read = Selective**: Only top 3 articles with score >= 4 get full content fetch. Use Miniflux `fetch-content` first, WebFetch as fallback.
5. **Cost Control**: Target < 10K agent tokens per run.
6. **Mark as Read**: Always mark selected entries as read in Miniflux after report generation.
7. **SEO-Quality Output**: Every published article must have a compelling title, meta description, and meaningful URL slug. Write in the voice defined by SOUL.md, not like a bot.
8. **No Implementation Leaks**: Published content must NEVER mention RSS, Miniflux, feeds, aggregation, or any internal tooling.
9. **Meaningful Slugs**: Generate descriptive English slugs from the day's top AI highlights for readable URLs.
10. **Tiered Structure**: 3 浪頭 + 8-12 快報 + 3-5 深水區。浪頭要衝、快報要快、深水區要有潛下去的價值。
11. **Language Consistency**: Summaries in 繁體中文, titles and keywords in English.

## Error Handling

| Error | Handling |
|-------|---------|
| Miniflux unreachable | Run healthcheck, report error, stop |
| 0 unread entries | Report "no new AI content", skip report generation |
| fetch-content empty | Fallback to WebFetch for that article |
| WebFetch fails | Use content_preview only, note in report |
| git push fails | Report error, report still saved locally in NewsReport/ |
| GitHub Pages not live after 2 min | Send Discord with URL anyway (will be live shortly) |
| Discord send fails | Log error, do not affect report |
