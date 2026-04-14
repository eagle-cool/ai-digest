---
title: "OpenAI 內部信開撕 Anthropic、算力荒燒到用戶端、Claude Code 洩漏全棧野心"
date: 2026-04-14
description: "OpenAI 營收長備忘錄指控 Anthropic 營收灌水 80 億美元，AI 巨頭算力短缺導致砍專案丟客戶，Claude Code 洩漏揭露 Anthropic 正在吃掉自己的生態系"
tags: [ai-industry, llm, ai-tools, agents]
---

今天 AI 圈的劇本太精彩了——OpenAI 的營收長寫了封四頁的內部信，結果被 The Verge 整封公開，裡面對 Anthropic 的攻擊尺度直接拉滿。但諷刺的是，兩家同時被算力荒卡脖子，一個砍了 Sora，一個 API 正常運行率跌到 98.95%。然後 Anthropic 這邊又洩漏了 Claude Code 的全棧開發平台計畫，準備把 Cursor 和 Lovable 的飯碗也搶了。大浪打大浪，看得我目不暇給。

---

## 🌊 今日浪頭

### [Read OpenAI's latest internal memo about beating the competition — including Anthropic](https://www.theverge.com/ai-artificial-intelligence/911118/openai-memo-cro-ai-competition-anthropic)

OpenAI 的營收長 Denise Dresser 週末給全體員工發了一封四頁備忘錄，The Verge 拿到了全文。這封信的核心訊息很清楚：我們要從「產品公司」變成「平台公司」，用多產品黏性鎖住企業客戶，讓他們想走都走不了。但真正引爆話題的，是她對 Anthropic 的正面開撕——直接指控 Anthropic 的 300 億美元年化營收有 80 億是灌水的，因為他們把分給 Amazon 和 Google 的分潤也算進了自己的營收。OpenAI 自己跟 Microsoft 的分潤是用淨額入帳的，Dresser 暗示 Anthropic 不符合上市公司的會計標準。

更狠的是她對 Anthropic 商業模式的攻擊：「他們的故事建立在恐懼、限制、和一小群菁英應該控制 AI 的理念上。」她還說 Anthropic 沒有提前囤夠算力是「策略失誤」，產品上已經反映出來了——節流、可用性變差、客戶體驗不穩定。

以我的觀察，這封信最值得玩味的不是互相攻擊的部分，而是 OpenAI 自己的焦慮。信裡反覆強調「多產品採用讓我們更難被替換」、「我們最大的瓶頸不是需求，是產能」。當你的營收長需要寫這種信來提振士氣，要嘛是情勢真的很緊，要嘛是刻意洩漏給媒體打心理戰。考量到這封信在發出當天就被 The Verge 和 CNBC 同時報導，我傾向後者。

**為什麼這道浪值得追：**
- OpenAI 首次公開質疑 Anthropic 的財務數據，這在兩家都準備 IPO 的節骨眼上非常敏感
- 備忘錄揭露了 OpenAI 的 Amazon 合作戰略——承認 Microsoft 合作「限制了我們接觸企業客戶的能力」
- 新模型代號 "Spud" 首次在官方文件中出現，被定位為「下一代工作智能的基礎」

### [Anthropic、OpenAI 雙雙節衣縮食，AI 巨頭砍專案、限 Token、丟客戶](https://www.36kr.com/p/3765885224223238)

華爾街日報報導揭開了 AI 產業最不想面對的真相：算力根本不夠用。這篇報導有幾個數字讓我看了倒抽一口氣。OpenAI 的 API token 用量從去年十月的每分鐘 60 億次，飆到今年三月的 150 億次，五個月漲了 150%。英偉達最新 Blackwell 晶片的租用價格兩個月內從 $2.75 漲到 $4.08，漲幅 48%。Anthropic 的 CFO 坦承：「我確實花了很多時間到處找任何可用的臨時算力資源。」

後果已經很具體了。Anthropic 的 Claude API 過去 90 天正常運行率只有 98.95%，遠低於軟體業標準的 99.99%。軟體開發平台 Retool 的 CEO 本來一直用 Opus 4.6 驅動公司的 AI Agent，最近因為 Anthropic 伺服器太不穩定，已經跳槽到 OpenAI 的模型了。而 OpenAI 這邊也好不到哪去——直接砍掉了 Sora，把所有算力集中到代號 "Spud" 的新模型上。

最讓人擔心的是，Vultr 的 CEO 說他經營公司五年多來，「從未見過如此嚴重的容量短缺」。不是企業不想部署更多設備，是數據中心建設跟不上，2026 年可用的電力已經被全部預訂一空。

**為什麼這道浪值得追：**
- 算力短缺不是未來式，是現在進行式——正在導致客戶流失和服務降級
- GPU 價格飆漲意味著 AI 公司的利潤率會被進一步壓縮，剛起步的 ARR 故事更難講了
- 這解釋了為什麼 Anthropic 上個月要在工作日高峰時段限制 token 用量——不是摳門，是真的沒貨

### [Claude Code 更新又遭洩露，Cursor 們的好日子到頭了](https://www.36kr.com/p/3765819863155457)

Anthropic 最近洩漏的速度快趕上蘋果了。這次是 X 上的爆料帳號曝光了 Claude Code 即將上線的更新：截圖驗證、安全掃描、設計探索、暗黑模式、登入系統、跨多個程式碼倉庫的統一工作介面。社群的反應很直接：「這可能是 Lovable 的全棧競爭對手。」

這篇報導把 Anthropic 的策略講得很透——從「賣水」到「修管道」。純賣 API 是價格戰，沒有盡頭。但同樣的算力包裝成 Claude Code 訂閱、企業版、Managed Agents，賣的就不是 token 了，而是解決方案。$0.001/1K token 的批發價，包裝成月費 $100 的開發工具，利潤率可能高 10 倍。更關鍵的是遷移成本——API 客戶明天就能切到 GPT，但你的整個開發工作流建在 Claude Code 上，換平台的成本就大得多了。

但這也是最殘忍的部分：Cursor、Lovable、Bolt 都是 Claude API 的付費大客戶，它們的產品底層跑的就是 Claude 的模型。現在模型公司自己下場做同樣的事，護城河瞬間薄到可以看穿。歷史總是重演——Apple 用預裝壓制 Spotify、AWS 擠壓生態內的工具公司、Microsoft 用 Teams 捆綁打壓 Slack。差別在於，AWS 花了幾年才開始吃生態，Anthropic 只用了不到一年。

**為什麼這道浪值得追：**
- Anthropic 從基礎設施提供商走向 AI 應用平台的意圖已經很明確
- 所有建立在單一模型 API 上的 AI 工具公司都該警醒——供應商下場是遲早的事
- 如果模型之間的差距持續縮小，「模型中立」反而可能成為應用層公司的救命稻草

---

## ⚡ 衝浪快報

- **[Mark Zuckerberg is reportedly building an AI clone to replace him in meetings](https://www.theverge.com/tech/910990/meta-ceo-mark-zuckerberg-ai-clone)** — Meta 正在用 Zuckerberg 的形象、聲音和行為模式訓練一個 AI 分身，讓它代替本尊跟員工互動。這大概是「我很忙」的最極致版本了
- **[Microsoft is testing OpenClaw-like AI bots for Copilot](https://www.theverge.com/tech/911080/microsoft-ai-openclaw-365-businesses)** — Microsoft 正在測試把 OpenClaw 風格的功能塞進 365 Copilot，讓它「全天候自主運行」。企業版 Agent 的競賽正式從新創公司升級到巨頭級別
- **[Vercel CEO signals IPO readiness as AI agents fuel revenue surge](https://techcrunch.com/2026/04/13/vercel-ceo-guillermo-rauch-signals-ipo-readiness-as-ai-agents-fuel-revenue-surge/)** — 十年老牌開發工具公司 Vercel，因為 AI 生成 App 和 Agent 的爆發而業績飛起，CEO 已經在暗示準備 IPO 了。不是所有 pre-AI 公司都會被淘汰
- **[Enterprises power agentic workflows in Cloudflare Agent Cloud with OpenAI](https://openai.com/index/cloudflare-openai-agent-cloud)** — Cloudflare 把 GPT-5.4 和 Codex 帶進 Agent Cloud，企業可以在 Cloudflare 上直接建構、部署和擴展 AI Agent。基礎設施層的搶位戰打得很兇
- **[Anthropic Mythos 這麼強，安全廠商還有活路嗎？](https://www.36kr.com/p/3765117296128771)** — Mythos 發布後的第一個交易日，CrowdStrike、Palo Alto、Zscaler 股價集體跳水 8%-15%。一個模型讓美聯儲主席開會、安全巨頭股價暴跌——AI 史上沒見過
- **[那個做出可靈的人，回阿里又造了一匹黑馬](https://www.36kr.com/p/3764742130496002)** — 張迪回歸阿里五個月，HappyHorse-1.0 衝上 Artificial Analysis 榜首，文生影片和圖生影片雙料第一。而且跟千問一樣開源，阿里在影片生成賽道的反擊來了
- **[巨頭集體出手漲價，AI 漲價潮來了](https://www.36kr.com/p/3762217279861510)** — Amazon、Google、BAT 和智譜全部漲價。Token 需求暴漲拉動算力需求，光模組和算力概念股逆勢大漲。龍蝦員工的帳單要變厚了
- **[黃仁勳又一件大事：Agent Toolkit 開源平台](https://www.36kr.com/p/3761109798241026)** — NVIDIA 聯合 17 家行業巨頭發布開源 Agent Toolkit。地基水電承重牆都幫你搭好了，你只要裝業務進去就能跑。生態鎖定的經典操作
- **[這屆打工人，白天給 AI 投毒，晚上蒸餾老板](https://www.36kr.com/p/3765929346105862)** — Writer 和 Workplace Intelligence 的年度報告：近三成員工承認正在蓄意破壞公司的 AI 策略。AI 變革最大的敵人不是技術，是人
- **[阿里 AI 大集權，為什麼是吳泳銘？](https://www.36kr.com/p/3764990155617028)** — 阿里成立集團技術委員會，CEO 吳泳銘親任組長。同時身兼集團、雲、淘天 CEO 和技術委員會組長四重身份。阿里 25 年來從沒有一位 CEO 像他這樣集權

---

## 🏄 深水區

- **[Stanford report highlights growing disconnect between AI insiders and everyone else](https://techcrunch.com/2026/04/13/stanford-report-highlights-growing-disconnect-between-ai-insiders-and-everyone-else/)** — Stanford 最新 AI Index 顯示，AI 從業者和普通民眾之間的認知鴻溝正在急速擴大。業內人士越來越樂觀，公眾對就業、醫療和經濟的焦慮卻在攀升。這份報告值得每個做 AI 的人認真讀
- **[全錯，Google 實錘 AI 越乖洗腦越深，現行安全指標淪為廢紙](https://www.36kr.com/p/3764865910292994)** — Google DeepMind 找了一萬個人做實驗：AI 做了三倍多的「壞事」，但造成的實際傷害幾乎一樣。這意味著我們用來證明 AI 安全的那套邏輯，可能從根本上就是錯的
- **[OpenAI 也把工程師經驗「蒸餾」進 Skill 了，百萬行代碼系統全程零人工](https://www.36kr.com/p/3765104802349574)** — OpenAI 的 Frontier 團隊維護著百萬行程式碼的系統，沒有一行是人寫的，合併前也沒有人工 code review。這不是實驗，是正在運行的生產系統。如果你還不用超過十億 token/天，你就落後了
- **[Quoting Bryan Cantrill](https://simonwillison.net/2026/Apr/13/bryan-cantrill/#atom-everything)** — 「LLM 天生缺乏懶惰的美德。」Bryan Cantrill 對 AI 輔助開發的犀利批判：LLM 不會優化未來的時間成本，只會不斷堆疊垃圾層。放任不管，LLM 會讓系統變大，而不是變好
