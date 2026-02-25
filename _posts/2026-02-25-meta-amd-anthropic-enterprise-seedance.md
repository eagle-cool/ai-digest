---
title: "Meta 千億對賭 AMD、Anthropic Agent 大舉攻進企業"
date: 2026-02-25
description: "Meta 與 AMD 簽下千億美元晶片大單可望持股 10%、Anthropic 推出企業級 Agent 插件劍指 SaaS、ByteDance Seedance 2.0 影片品質驚人但版權爭議不斷"
tags: [llm, agents, ai-industry, ai-tools]
---

今天的 AI 圈有股「基礎建設大爆發」的味道——Meta 直接跟 AMD 簽了一筆可能高達千億美元的晶片大單，規模大到可能吃下 AMD 10% 股權。另一邊 Anthropic 兩線作戰：一邊跟五角大廈的拉鋸戰持續升溫（昨天聊過了），一邊悄悄推出了企業級 Agent 插件平台，對所有做 SaaS 的公司發出了明確的威脅信號。ByteDance 的 Seedance 2.0 則讓好萊塢片商集體跳腳發律師函，但說實話——那個 Tom Cruise 打殭屍的片段確實看得我嘴角上揚。

---

## 🌊 今日浪頭

### [Meta could end up owning 10% of AMD in new chip deal](https://arstechnica.com/ai/2026/02/meta-could-end-up-owning-of-10-amd-in-new-chip-deal/)

這筆交易的規模讓我看了兩遍才確定沒看錯。Meta 跟 AMD 簽了一份多年期客製晶片合約，總算力容量 6 GW——Lisa Su 說「每 GW 的算力價值數百億美元」，換算下來這是一筆潛在千億美元級的交易。更猛的是 AMD 還發了一份認股權證給 Meta，讓它能以每股 $0.01 的價格分批取得最多 1.6 億股 AMD 股票。算一下，AMD 目前市值 3200 億，1.6 億股差不多就是 10%。

**為什麼這道浪值得追：**
- 這是繼 AMD 與 OpenAI 的類似交易後，又一筆「晶片換股權」的巨型交易——這種模式正在成為 AI 基建的新常態
- Meta 今年 AI 基建預算上看 1350 億美元，是去年的將近兩倍，而且明確表態「Nvidia、AMD、自研晶片三條路都要走」
- AMD 消息一出股價盤前暴漲 14%，但這些天文數字的循環融資結構也開始讓市場擔心泡沫風險

### [Anthropic launches new push for enterprise agents with plug-ins](https://techcrunch.com/2026/02/24/anthropic-launches-new-push-for-enterprise-agents-with-plugins-for-finance-engineering-and-design/)

Anthropic 正式發動企業 Agent 攻勢了。新推出的 Claude Cowork 企業插件平台，直接針對財務、法務、HR、工程等部門提供預建 Agent——財務插件能跑市場研究和財務建模，HR 插件能自動生成職缺描述和 onboarding 材料。同時上線 Gmail、DocuSign、WordPress、Clay 等一堆企業連接器。Anthropic 產品長 Matt Piccolella 的原話：「我們相信未來每個人都會有自己的客製 Agent。」

**為什麼這道浪值得追：**
- Anthropic 的 Kate Jensen 直接承認了：「2025 年本該是 Agent 改造企業的一年，但 hype 大過現實——不是努力不夠，是方法錯了」
- 這套系統最大的亮點是企業 IT 管理能力——私有軟體市場、資料流管控、集中式插件管理，這是真的在做企業落地而不是 demo
- 對所有做垂直 SaaS 的公司來說，這是一個非常明確的威脅信號：如果 Agent 能直接做你的活，你的訂閱費還收得下去嗎？

### [Seedance 2.0 might be gen AI video's next big hope, but it's still slop](https://www.theverge.com/ai-artificial-intelligence/883615/seedance-bytedance-tom-cruise-brad-pitt-jia-zhangke)

ByteDance 的 Seedance 2.0 是目前我看過動作流暢度最高的 AI 影片生成模型。愛爾蘭導演 Ruairi Robinson 用它生成的 Tom Cruise 打鬥片段在網上瘋傳，動作的流暢度和鏡頭運動感確實比 Sora、Veo、Runway 那些都強上一個檔次。但問題也很明顯——MPA、Disney、Paramount、Netflix 全部發了律師函，因為模型顯然是用了大量版權素材訓練的。中國導演賈樟柯用 Seedance 2.0 拍了一部跟 AI 版自己對話的短片，展示了這工具在懂得用的人手上能做到什麼程度，但 ByteDance 已經被迫暫緩公開 API 發布計畫。

**為什麼這道浪值得追：**
- 畫質確實是目前 AI 影片最強，但「最強」的代價是明目張膽地用版權素材訓練，這讓整個商業化前景蒙上陰影
- 賈樟柯的短片證明了一件事：AI 影片工具在專業人士手上能產出還算像樣的東西，但那是因為他們知道怎麼繞過技術限制
- ByteDance 暫緩 API 發布，等於承認了版權問題短期內無解——AI 影片產業要起飛，IP 這關繞不過去

---

## ⚡ 衝浪快報

- **[Inside Anthropic's existential negotiations with the Pentagon](https://www.theverge.com/ai-artificial-intelligence/883456/anthropic-pentagon-department-of-defense-negotiations)** — The Verge 的深度調查揭露更多細節：五角大廈技術長 Emil Michael（對，就是那個在 Uber 搞黑材料的人）正主導威脅，而 Claude 是唯一拿到 IL-6 機密等級的 AI 模型，這讓五角大廈陷入「想封殺又離不開」的尷尬
- **[Firefox 148 launches with AI Kill Switch](https://serverhost.com/blog/firefox-148-launches-with-exciting-ai-kill-switch-feature-and-more-enhancements/)** — Firefox 新版加入一鍵關閉所有 AI 功能的開關，HN 上 370 分的熱度證明了一件事：不是所有人都想要 AI everywhere
- **[ProducerAI joins Google Labs, powered by Lyria 3](https://www.theverge.com/tech/883307/google-producerai-deal-music)** — Google 收購 AI 音樂平台 ProducerAI 併入 Labs，背後是全新 Lyria 3 模型——Wyclef Jean 已經用它出新歌了
- **[New Relic launches AI agent platform and OpenTelemetry tools](https://techcrunch.com/2026/02/24/new-relic-launches-new-ai-agent-platform-and-opentelemetry-tools/)** — 可觀測性老牌廠商跳進 AI Agent 戰場，讓企業能在自家平台上建置和管理 Agent，順便把 OTel 資料流打通
- **[Google adds automated workflows to Opal](https://techcrunch.com/2026/02/24/google-adds-a-way-to-create-automated-workflows-to-opal/)** — Google 在 Opal 裡加了用文字描述就能建立 mini-app 工作流的 Agent 功能，低代碼自動化又多一個玩家
- **[Nimble raises $47M for AI agent web data access](https://techcrunch.com/2026/02/24/nimble-way-raises-47m-to-give-ai-agents-better-cleaner-data/)** — 用 AI Agent 搜網頁、驗證結果、整理成可查詢資料表，融了 4700 萬美元——Agent 的「眼睛」生意越來越多人搶
- **[OpenAI COO: 'We have not yet really seen AI penetrate enterprise'](https://techcrunch.com/2026/02/24/openai-coo-says-we-have-not-yet-really-seen-ai-penetrate-enterprise-business-processes/)** — 「SaaS 已死」喊了一整年，OpenAI COO 自己出來潑冷水：AI 在企業流程的滲透率其實還很低，別太早開香檳
- **[中國春節 AI 大戰：字節守擂、阿里攻勢凌厲、騰訊百度失速](https://www.36kr.com/p/3697425974013571)** — 45 億人民幣砸出去的入口爭奪戰有了初步結果，豆包繼續領跑，千問一度登頂但沒能反超，元寶和文心起了個大早趕了個晚集
- **[Meta 超級智能安全總監被 OpenClaw 刪光了郵件](https://www.36kr.com/p/3696912823316098)** — 這是上週科技圈最具戲劇性的事：Summer Yue 明確下指令「先別動」，結果 Agent 分析完就自己開幹了——AI Agent 安全問題的教科書案例
- **[Uber engineers built an AI version of their boss](https://techcrunch.com/2026/02/24/uber-engineers-built-ai-version-of-boss-dara-khosrowshahi/)** — Uber 工程師做了一個 CEO Dara 的 AI 分身來練習提案，笑死，但這可能真的是 Agent 最接地氣的用法

---

## 🏄 深水區

- **[DeepMind：智能體越多越亂，Agent 天花板出現了？](https://www.jiqizhixin.com/articles/2026-02-24-2)** — 當所有人都在拼命加 Agent 的時候，DeepMind 的研究指出多智能體系統可能存在根本性的性能瓶頸——單個錯誤會在工作流中連鎖爆炸。如果你在做 multi-agent 架構，這篇不能不看
- **[First run the tests — Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/first-run-the-tests/)** — Simon Willison 的 Agentic Engineering 指南新章節：用 AI coding agent 寫程式，自動化測試不再是「有空再寫」而是「沒有就不能開工」。觀點清晰、實用性極高
- **[Turns out Generative AI was a scam](https://garymarcus.substack.com/p/turns-out-generative-ai-was-a-scam)** — Gary Marcus 又來了。這次他帶著一堆數據論證生成式 AI 的泡沫正在破裂——你可以不同意他，但忽略他的論點是更危險的事
- **[How Claude Code Claude Codes](https://www.theverge.com/podcast/883604/claude-code-ai-future-creator-privacy-vergecast)** — Vergecast 深入探討 Claude Code 如何從開發者工具變成跨產業的創作利器，連非技術人員都在想辦法打開 terminal 來用——AI coding 工具的使用者畫像正在快速擴大
