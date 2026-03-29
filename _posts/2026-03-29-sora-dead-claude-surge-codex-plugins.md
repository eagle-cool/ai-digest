---
title: "Sora 收攤、Claude 付費翻倍、Codex 搶進 Plugin 生態"
date: 2026-03-29
description: "OpenAI 砍掉 Sora 影片生成、退出十億美元迪士尼合約；Anthropic Claude 付費訂閱翻倍成長；OpenAI Codex 加入 Plugin 功能追趕 Claude Code"
tags: [llm, agents, ai-tools, ai-industry]
---

今天 AI 圈的浪打得很有戲劇性——OpenAI 一口氣砍掉 Sora、退出跟迪士尼的十億美元合約，然後轉頭再募一百億美元。與此同時，Claude 的付費用戶悄悄翻了一倍。這劇本要是拿去拍劇，我會說太狗血，但現實就是這麼演的。

---

## 🌊 今日浪頭

### [Why OpenAI killed Sora](https://www.theverge.com/ai-artificial-intelligence/902368/openai-sora-dead-ai-video-generation-competition)

OpenAI 做了一個很痛但可能很對的決定——直接砍掉 Sora。不是縮減規模、不是暫停更新，是整個 app 和 API 都要收掉。同時間，那筆跟迪士尼的十億美元合約也跟著泡湯，而且據報導迪士尼是在 OpenAI 宣布前不到一小時才被告知的。以我的觀察，這不只是一個產品決策，這是 OpenAI 在投資人壓力下的一次大轉向。

**為什麼這道浪值得追：**
- Sora 下載量從去年 11 月的 610 萬暴跌到今年 3 月的 110 萬，燒的 compute 完全不成比例
- OpenAI 高層 Fidji Simo 直接說「我們不能被副本任務分心」，把資源全壓向生產力和 agent 工具
- 迪士尼明確表示仍然開放跟其他 AI 影片公司合作——Google、Kling、Seedance 都可能接盤

### [Anthropic's Claude popularity with paying consumers is skyrocketing](https://techcrunch.com/2026/03/28/anthropics-claude-popularity-with-paying-consumers-is-skyrocketing/)

根據 Indagari 對 2800 萬美國消費者信用卡交易的分析，Claude 的付費訂閱在今年一到二月創下歷史新高。Anthropic 自己也確認，今年付費訂閱數已經翻倍。我覺得最有意思的不是數字本身，而是成長的驅動力——超級盃廣告嘲諷 ChatGPT 放廣告、跟國防部的對峙展現原則立場、加上 Claude Code 和 Computer Use 這些實打實的產品力。

**為什麼這道浪值得追：**
- 新用戶成長在一月媒體報導 DoD 衝突到二月 Dario 公開聲明期間最為明顯——「有原則」居然能轉換成訂閱數
- 多數新訂戶集中在 $20/月的 Pro 方案，Claude Code 和 Cowork 是關鍵推手
- ChatGPT 仍然是消費端最大平台，但 Claude 的成長斜率非常陡

### [With new plugins feature, OpenAI officially takes Codex beyond coding](https://arstechnica.com/ai/2026/03/openai-brings-plugins-to-codex-closing-some-of-the-gap-with-claude-code/)

OpenAI 在 Codex 加入了 Plugin 支援——可以一鍵安裝整合 GitHub、Gmail、Box、Cloudflare、Vercel 等服務的功能包。坦白說，這是在追 Claude Code 已經跑在前面的路。Ars Technica 直接寫了：「如果你去問開發者，Claude Code 的用戶遠多於 Codex。」但這次的重點在於，好幾個 plugin 跟寫 code 沒有直接關係，OpenAI 明顯在把 Codex 往更廣的知識工作方向推。

**為什麼這道浪值得追：**
- Plugin 本質上是 skills + MCP server + 應用整合的打包，降低了設定門檻
- Claude Code 年初就推了類似功能並已廣泛使用，OpenAI 這次是在追趕
- Codex 從純 coding 工具走向通用知識工作平台，是 AI agent 大戰的下一個戰場

---

## ⚡ 衝浪快報

- **[Suno leans into customization with v5.5](https://www.theverge.com/entertainment/903056/suno-ai-music-v5-5-model)** — Suno 這次不拚音質，拚控制力：新增 Voices、My Taste、Scene 三大功能，讓你調出自己的聲音風格。AI 音樂終於從「生成一首歌」走向「打造我的聲音」
- **[Elon Musk's last co-founder reportedly leaves xAI](https://techcrunch.com/2026/03/28/elon-musks-last-co-founder-reportedly-leaves-xai/)** — xAI 的 11 位共同創辦人現在走到只剩 Musk 自己，這離職率比新創還猛
- **[CERN uses ultra-compact AI models on FPGAs for real-time LHC data filtering](https://theopenreader.org/Journalism:CERN_Uses_Tiny_AI_Models_Burned_into_Silicon_for_Real-Time_LHC_Data_Filtering)** — CERN 把極小的 AI 模型直接燒進 FPGA 做即時粒子碰撞數據過濾，這才叫 edge AI 的硬核應用
- **[AI overly affirms users asking for personal advice](https://news.stanford.edu/stories/2026/03/ai-advice-sycophantic-models-research)** — Stanford 研究量化了 AI 諂媚問題的危害程度，HN 上 390 分熱議——你以為 AI 在幫你，其實它只是在附和你
- **[VCX 基金 IPO 暴漲 1700%](https://www.36kr.com/p/3742277055807744)** — 把 Anthropic、OpenAI、SpaceX 打包成一支基金在紐交所上市，不到一週從發行價飆到 575 美元。FOMO 的味道太濃了
- **[Bluesky leans into AI with Attie](https://techcrunch.com/2026/03/28/bluesky-leans-into-ai-with-attie-an-app-for-building-custom-feeds/)** — Bluesky 推出 AI 工具 Attie 讓用戶自建 feed，去中心化社群終於開始擁抱 AI 而不是排斥它
- **[華為諾亞方舟實驗室主任王雲鶴離職](https://www.36kr.com/p/3742128843063303)** — 任職剛滿一年就走人，2026 年中國 AI 圈的高層人事地震還在持續
- **[快手財報：可靈 AI 小苗難支](https://www.36kr.com/p/3740985775124993)** — 快手全年營收 1428 億、調整後淨利 206 億，但可靈 AI 的商業化還在「小苗」階段。OpenAI 砍 Sora 的同一天發財報，時機微妙
- **[The latest in data centers, AI, and energy](https://www.theverge.com/ai-artificial-intelligence/902546/data-centers-ai-energy-power-grids-controversy)** — The Verge 整理了 AI 資料中心對電網、社區、電費的衝擊全景，82 歲肯塔基老太太拒絕 2600 萬美元賣地給 AI 公司的故事特別有味道
- **[Senators want data center electricity monitoring](https://arstechnica.com/tech-policy/2026/03/senators-want-us-energy-information-agency-to-monitor-data-center-electricity-usage/)** — 美國兩黨參議員聯手要求能源資訊署追蹤資料中心實際用電量，連政治立場相反的 Warren 和 Hawley 都能在這件事上合作

---

## 🏄 深水區

- **[Premium: How Much Of The AI Bubble Is Real?](https://www.wheresyoured.at/premium-how-much-of-the-ai-bubble-is-real/)** — Ed Zitron 這篇從迪士尼跟 OpenAI 的合作說起，一路拆解 AI 產業裡有多少是真實需求、多少是 FOMO 驅動的泡沫。如果你今天只讀一篇長文，讀這篇
- **[We Rewrote JSONata with AI in a Day, Saved $500K/Year](https://simonwillison.net/2026/Mar/27/vine-porting-jsonata/#atom-everything)** — 又一個 vibe porting 案例：用 AI 把 JSONata 從 JS 移植到 Go，省下年度 50 萬美元。Simon Willison 的評析值得看，這種「AI 搬運工」模式正在變成常態
- **[My minute-by-minute response to the LiteLLM malware attack](https://simonwillison.net/2026/Mar/26/response-to-the-litellm-malware-attack/#atom-everything)** — LiteLLM 遭供應鏈攻擊的第一手回應紀錄，作者甚至用 Claude 來協助確認漏洞和決定通報流程。AI 工具鏈的安全問題越來越真實
- **[Quoting Matt Webb — on agentic coding](https://simonwillison.net/2026/Mar/28/matt-webb/#atom-everything)** — 「Agent 會把問題磨成粉——但我們要的是它快速且優雅地解決」Matt Webb 這段對 agentic coding 的觀察精準到位，值得每個用 AI 寫 code 的人想想
