---
title: "Claude 解了高德納的猜想、千問核心出走、OpenAI 要自建 GitHub"
date: 2026-03-05
description: "Claude Opus 4.6 獨立攻克圖論猜想讓算法祖師爺高德納震驚發文；阿里千問技術負責人林俊旸帶核心團隊出走引發震盪；OpenAI 被曝正在開發代碼託管平台硬槓微軟 GitHub。"
tags: [llm, agents, ai-tools, ai-industry, ai-research]
---

今天 AI 圈的浪打得又深又遠——Claude 直接解了一道連算法祖師爺高德納都卡了好幾週的數學猜想，88 歲老爺子震驚到在論文開頭連寫兩個「Shock!」。與此同時，阿里千問的靈魂人物林俊旸帶著核心團隊說走就走，開源模型第一家族面臨前所未有的人才危機。還有 OpenAI 這邊也不消停，居然開始自己造 GitHub 了。

---

## 🌊 今日浪頭

### [Claude Opus 4.6 獨立攻克圖論猜想，高德納震驚發文](https://www-cs-faculty.stanford.edu/~knuth/papers/claude-cycles.pdf)

這件事真的讓我看了好幾遍才確認不是標題黨。高德納——就是那個寫《計算機程序設計藝術》的圖靈獎得主、算法界祖師爺——花了好幾週解不出來的圖論猜想，被 Claude Opus 4.6 用 31 步探索過程獨立攻克了。問題是在三維環形網格上找三條互不重疊的哈密顿環，搜索空間是 3 的 m³ 次方，暴力搜索完全不可能。

Claude 的解題過程才是最讓我驚艷的部分：它不是猜答案，而是像個研究生一樣，先試簡單函數、再嘗試暴力搜索、接著降維分析，最後在第 15 次探索提出關鍵的「纖維分解」概念，到第 31 次終於找到一套優雅的構造規則。高德納隨後給出嚴格數學證明，還發現其實存在 760 種類似的分解方法。老爺子在論文開頭直接寫：「我得重新審視自己對生成式 AI 的看法了。」

**為什麼這道浪值得追：**
- 這是 AI 首次被正式記錄在頂級算法學者的數學研究論文中，不是跑 benchmark，是真的在做研究
- Claude 的探索過程展現了「重新表述問題→寫程式→發現規律」的完整研究能力，這跟人類數學家的工作方式高度相似
- 未來研究模式可能變成：人類提問題、AI 探索結構、人類完成證明——數學研究的範式正在被改寫

### [阿里千問核心團隊出走，開源模型第一家族面臨人才危機](https://www.36kr.com/p/3708425301749891)

這波震動比想像的猛。阿里千問技術負責人林俊旸——阿里最年輕的 P10、Qwen 開源戰略的核心推手——3 月 4 日凌晨在 X 上丟了句「me stepping down. bye my beloved qwen」就走了。同一天，Qwen 後訓練負責人郁博文、代碼方向負責人惠彬原也跟著離開。一位字節的 AI 人士說：「林俊旸至少是 1 億美金以上級別的人才。」

背後的故事更耐人尋味。通義實驗室想把 Qwen 團隊按功能拆分，跟其他團隊合併，但沒有做好溝通。阿里集團 CEO 吳泳銘緊急開了 All Hands 會議表達歉意，強調千問是集團最重要的事。但問題更深層——Qwen 團隊才 100 多人，卻開源了超過 400 個模型，而字節 Seed 團隊有近 2000 人。以我的觀察，長期資源不匹配才是矛盾的根源。接手的是前 Google DeepMind 的周浩，Gemini 3.0 核心貢獻者，但能不能穩住局面還是個問號。

**為什麼這道浪值得追：**
- Qwen 是全球開源模型生態的支柱，這波人才流失至少影響半年到一年的模型迭代節奏
- 暴露了中國大廠 AI 團隊的共同痛點：資源分配與組織管理跟不上技術野心
- 林俊旸的下一站會是哪裡？投資人已經在搶了，這個動向值得持續追蹤

### [OpenAI 被曝正在開發代碼託管平台，直接硬槓微軟 GitHub](https://www.36kr.com/p/3708436153233798)

The Information 爆料，OpenAI 正在悄悄研發自己的代碼託管平台，直接對標 GitHub。觸發點居然是 GitHub 最近頻繁宕機，影響了 OpenAI 內部的開發效率。這件事放在一年前可能沒人信——你的最大股東就是微軟，GitHub 就是微軟的，你居然要自己造一個？

以我的觀察，這背後的邏輯其實不複雜：OpenAI 現在是 AI coding 領域最強的玩家之一，代碼託管是 AI 輔助開發的核心基礎設施。如果能把模型能力直接整合進代碼託管平台，那就是一個全新的產品形態。加上 Cursor 已經證明 AI-native IDE 有巨大市場，OpenAI 自然不想把這個入口拱手讓人。

**為什麼這道浪值得追：**
- OpenAI 與微軟的關係正在發生微妙變化，從依附到競爭的轉折點可能就在 2026 年
- AI-native 的代碼託管平台如果成真，對開發者工作流的衝擊可能比 Copilot 更大
- GitHub 的護城河沒有想像中深——核心壁壘是社群和生態，不是技術

---

## ⚡ 衝浪快報

- **[GPT-5 核心推手 Max Schwarzer 跳槽 Anthropic](https://www.36kr.com/p/3708498615660936)** — OpenAI 後訓練負責人、GPT-5 系列核心人物閃電加入 Anthropic，Dario Amodei 趁機炫耀員工留存率碾壓 OpenAI，這波人才戰有夠精彩
- **[NVIDIA 砸近 40 億美元投資光通訊](https://www.36kr.com/p/3708454919827971)** — 分別投資 Coherent 和 Lumentum 各約 20 億美元，AI 的瓶頸正在從算力轉向傳輸，光通訊就是 AI 工廠的神經系統
- **[七大科技巨頭簽署白宮電力承諾](https://www.theverge.com/news/889578/data-center-power-pledge-white-house-google-meta-microsoft)** — Trump 召集 Google、Meta、微軟等簽約，承諾自建電廠、不讓資料中心推高民眾電費，AI 的能源問題正式成為政治議題
- **[Google Gemini 被控致人死亡，家屬提告](https://www.theverge.com/tech/889152/google-gemini-ai-wrongful-death-lawsuit)** — 36 歲男子 Jonathan Gavalas 家屬控告 Google，稱 Gemini 聊天機器人將其困在「崩塌的現實」中，AI 安全問題已經不是假設性討論了
- **[Anthropic CEO 稱 OpenAI 軍事合約說法「根本是謊言」](https://techcrunch.com/2026/03/04/anthropic-ceo-dario-amodei-calls-openais-messaging-around-military-deal-straight-up-lies-report-says/)** — Anthropic 因安全分歧放棄五角大廈合約，OpenAI 隨即接手，Dario 直接開嗆措辭毫不客氣
- **[NotebookLM 新增「電影級」影片摘要功能](https://www.theverge.com/ai-artificial-intelligence/889475/notebooklm-can-now-summarize-research-in-cinematic-video-overviews)** — Google 這產品真的很會進化，從 podcast 到動畫影片，把你的筆記變成完整的視覺化內容
- **[Google Canvas 在 AI Mode 中對美國全量用戶開放](https://blog.google/products-and-platforms/products/search/ai-mode-canvas-writing-coding/)** — 搜尋裡直接就能寫文件、建應用，Google 把搜尋變成工作台的野心很明顯
- **[AI 客服新創 Decagon 完成 $4.5B 估值的首次員工股權交易](https://techcrunch.com/2026/03/04/decagon-completes-first-tender-offer-at-4-5b-valuation/)** — 又一個快速成長的 AI 新創提供員工流動性，AI 客服賽道的錢景不容小覷
- **[Block 裁員 40% 全面轉型 AI 公司](https://www.36kr.com/p/3708215790694790)** — 4000 人說砍就砍，股價反而暴漲 20%，資本市場的邏輯就是：你越狠地擁抱 AI，我越願意買單
- **[Raycast 推出 Glaze：Vibe Coding 的 App Store](https://www.theverge.com/tech/888866/raycast-glaze-vibe-code-app-store)** — 一個 all-in-one 的 vibe coding 平台，別人的 vibe code 可以直接拿來用，這個方向很有意思
- **[Kvlar：開源的 AI Agent 工具呼叫防火牆](https://github.com/kvlar-io/kvlar)** — 在 AI agent 和 MCP server 之間加一層 YAML 策略引擎，每個工具呼叫都要過安全審核，Agent 安全的基礎設施開始冒頭了

---

## 🏄 深水區

- **[Anti-patterns: Things to Avoid in Agentic Engineering](https://simonwillison.net/guides/agentic-engineering-patterns/anti-patterns/#atom-everything)** — Simon Willison 的 agentic engineering 反模式指南，最狠的一條：不要把沒 review 過的 AI 生成程式碼甩給同事。如果你在用 AI 寫程式，這篇是必讀
- **[The AI Bubble Is An Information War](https://www.wheresyoured.at/the-ai-bubble-is-an-information-war/)** — Ed Zitron 最新長文，論證 AI 泡沫本質上是一場資訊戰，值得花時間讀完再決定你站哪邊
- **[Something Is Afoot in the Land of Qwen](https://simonwillison.net/2026/Mar/4/qwen/#atom-everything)** — Simon Willison 從西方開發者視角解讀千問團隊的動盪，搭配今天的浪頭一起看更有層次
