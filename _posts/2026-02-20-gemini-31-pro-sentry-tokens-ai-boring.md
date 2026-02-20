---
title: "Gemini 3.1 Pro 半價對打 Opus、Sentry 90 天燒十萬鎂 Token"
date: 2026-02-20
description: "Google 發布 Gemini 3.1 Pro，價格不到 Claude Opus 4.6 一半但 benchmark 相近；Sentry 公開 AI 使用數據震驚業界；一篇爆紅文章點出 AI 正在讓人變得無聊。"
tags: [llm, ai-tools, ai-coding, ai-industry]
---

今天的浪很有意思——Google 丟了個 Gemini 3.1 Pro 出來，價格直接砍到 Opus 4.6 的一半不到，benchmark 還差不多。然後 Sentry 的人跑來 HN 曬帳單，90 天燒了十萬美金的 token，整間公司 81% 的人都在用 AI coding tool。但最讓我停下來想的，反而是一篇 238 個 upvote 的文章——AI 正在讓我們變得無聊。

---

## 🌊 今日浪頭

### [Gemini 3.1 Pro](https://simonwillison.net/2026/Feb/19/gemini-31-pro/#atom-everything)

Google 發布了 Gemini 3.1 系列的第一個模型，定價跟 Gemini 3 Pro 一樣：200K token 以下是 $2/M input、$12/M output。換算下來，這價格不到 Claude Opus 4.6 的一半，但 benchmark 分數居然很接近。Simon Willison 第一時間拿去跑他的招牌測試——畫一隻鵜鶘騎腳踏車的 SVG，模型想了 323 秒後交出了一張相當不錯的成品，腳踏車籃子裡還放了一條魚。

**為什麼這道浪值得追：**
- 價格是 Opus 4.6 的一半以下，benchmark 卻相近——這對開發者的錢包是個好消息
- SVG 生成能力大幅提升，Jeff Dean 親自發推展示各種動物騎車的動畫
- 目前速度還很慢（簡單的 "hi" 要 104 秒），但這應該只是上線首日的問題

### [AI makes you boring](https://www.marginalia.nu/log/a_132_ai_bores/)

這篇在 HN 上炸了 238 個 upvote、153 則討論，作者的核心論點很簡單但很痛：AI 不是讓你更有創意，它是在讓你變得無聊。原因是——原創想法來自於長時間沉浸在問題中，而當你把思考外包給 LLM，你跳過的恰好就是產生原創想法的那個過程。作者拿 Show HN 當例子，以前看到的是一個人花了很長時間思考某個問題後做出來的東西，現在看到的是一堆 vibe code 出來的淺碟作品。

**為什麼這道浪值得追：**
- 「你不會用挖土機舉重來練肌肉，你也不會用 GPU 思考來產生有趣的想法」——這句話值得每個用 AI 的人想想
- 不是反 AI，而是提醒我們 AI 省掉的「過程」可能才是最有價值的部分
- 對所有用 AI 寫 code、寫文章、做產品的人都是一記警鐘

### [Sharing internal AI adoption/spend stats from Sentry](https://news.ycombinator.com/item?id=47075795)

Sentry 的人直接在 HN 上公開了他們的 AI 使用數據，這可能是目前最透明的企業 AI 採用案例。90 天內花了超過 $100K、用掉 1000 億個 token。最常用的模型是 Opus 4.5，佔 40% 以上。最猛的單一使用者一個人用了 42 億 token。372 個全職員工中有 302 個（81%）嘗試過 agentic coding tool，整體 commit 數量上升了 79%。

**為什麼這道浪值得追：**
- 這是真實企業數據，不是 survey、不是估算——直接攤開來給你看
- 81% 採用率不只是工程師，包含全公司所有人，這個數字很驚人
- commit 數量上升 79% 但「生產力」到底有沒有等比例上升？這跟下面快報裡那則 "93% use AI but productivity still 10%" 形成有趣對照

---

## ⚡ 衝浪快報

- **[CTO Says 93% of Developers Use AI, but Productivity Is Still 10%](https://shiftmag.dev/this-cto-says-93-of-developers-use-ai-but-productivity-is-still-10-8013/)** — 52 個 upvote 的熱門討論。幾乎所有人都在用 AI，但整體生產力提升才 10%？這數字讓人反思 AI 到底是真的在幫忙還是在製造更多工作
- **[AI found 12 of 12 OpenSSL zero-days](https://www.lesswrong.com/posts/7aJwgbMEiKq5egQbd/ai-found-12-of-12-openssl-zero-days-while-curl-cancelled-its)** — AI 找到了 OpenSSL 全部 12 個 zero-day 漏洞。同時 curl 專案卻取消了他們的 AI 安全審計。這對比太諷刺了
- **[AI pioneer Fei-Fei Li's World Labs raises $1B in funding](https://www.reuters.com/technology/artificial-intelligence/ai-pioneer-fei-fei-lis-world-labs-raises-1-billion-funding-2026-02-18/)** — 李飛飛的 World Labs 拿到 10 億美金融資，空間智慧 AI 這條賽道正式進入大資本時代
- **[Atlassian Founders Lose $7.2B as Software Stocks Slump on AI Fears](https://www.bloomberg.com/news/articles/2026-02-19/software-rout-wipes-7-2-billion-off-atlassian-founders-wealth)** — AI 恐慌直接蒸發了 Atlassian 創辦人 72 億美金的身價。傳統 SaaS 的日子不好過
- **[Accenture links staff promotions to use of AI tools](https://www.theguardian.com/accenture/2026/feb/19/accenture-links-staff-promotions-to-use-of-ai-tools)** — 不用 AI 就別想升遷？Accenture 把 AI 工具使用率跟晉升直接掛鉤，這操作夠激進
- **[AI Helped Uncover a 50-80x Improvement for Linux's IO_uring](https://www.phoronix.com/news/AI-50-80x-IO-uring)** — AI 幫忙在 Linux 核心的 io_uring 找到了 50-80 倍的效能提升。這不是 demo，是真的進了 kernel patch
- **[Google Banning AI Ultra subscribers for using OpenCode](https://old.reddit.com/r/google_antigravity/comments/1r2hnn8/ultra_user_get_banned/)** — Google 把用 OpenCode 的 AI Ultra 訂閱者直接 ban 掉，但還繼續收費。這公關災難等級的操作
- **[Perplexity AI drops ads implementation plan to keep user trust](https://www.msn.com/en-us/money/other/perplexity-ai-drops-ads-implementation-plan-to-keep-user-trust/ar-AA1WBvyY)** — Perplexity 決定不放廣告了，選擇用戶信任。在 AI 搜尋這場戰爭裡，這是個聰明的差異化策略
- **[AI made coding more enjoyable](https://weberdominik.com/blog/ai-coding-enjoyable/)** — 41 個 upvote。跟上面那篇「AI 讓你無聊」形成有趣對照——有人覺得 AI 讓寫 code 變好玩了
- **[Measuring AI agent autonomy in practice](https://www.anthropic.com/research/measuring-agent-autonomy)** — Anthropic 發了一篇研究，試圖量化 AI agent 的自主程度。當 agent 越來越自主，怎麼衡量和管控變成關鍵問題
- **[Ambani Joins Adani, Tata with Plans to Invest $110B in AI](https://www.bloomberg.com/news/articles/2026-02-19/ambani-s-reliance-to-invest-110-billion-in-ai-infrastructure)** — 印度三大財閥全部押注 AI 基礎建設，Reliance 的 Ambani 喊出 1100 億美金投資計畫

---

## 🏄 深水區

- **[AI is not a coworker, it's an exoskeleton](https://www.kasava.dev/blog/ai-as-exoskeleton)** — 18 個 upvote、18 則討論。把 AI 比喻成外骨骼而不是同事——你穿上它變強，但脫掉它你還是你。這個框架比「AI 同事」的比喻精準得多，值得花十分鐘讀
- **[I traced 3,177 API calls to see what 4 AI coding tools put in the context window](https://theredbeard.io/blog/i-intercepted-3177-api-calls-across-4-ai-coding-tools/)** — 有人攔截了 Cursor、Copilot 等四個 AI coding tool 的 3177 個 API call，看它們到底往 context window 塞了什麼。如果你對這些工具的底層運作好奇，這篇是必讀
- **[The bug fix paradox: why AI agents keep breaking working code](https://kiro.dev/blog/bug-fix-paradox/)** — 為什麼 AI agent 修一個 bug 會同時搞壞其他東西？這篇深入分析了 AI coding agent 的系統性盲點
- **[Boundary Point Jail: A new way to break the strongest AI defences](https://www.aisi.gov.uk/blog/boundary-point-jailbreaking-a-new-way-to-break-the-strongest-ai-defences)** — 英國 AI 安全研究所（AISI）發表的新型 jailbreak 技術。連最強的 AI 防禦都擋不住，這對 AI safety 來說是重要的研究方向
