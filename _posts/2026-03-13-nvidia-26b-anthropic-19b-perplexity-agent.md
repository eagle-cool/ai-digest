---
title: "Nvidia 花 $26B 做開源模型、Anthropic 年收破 $19B"
date: 2026-03-13
description: "Nvidia 宣布五年砸 $26B 開發開源模型正式挑戰 OpenAI、Anthropic 年化收入翻倍至 $19B 聯手黑石做 AI 顧問、Perplexity 推出 Personal Computer 把 Mac 變 24/7 AI 分身。"
tags: [llm, agents, ai-industry, ai-tools]
---

今天的浪不是在拍岸——是在改變海岸線。Nvidia 不再只是賣鏟子了，直接宣布砸 $26B 要做開源 AI 模型，Nemotron 3 Super 號稱打贏 GPT-OSS；Anthropic 年收從 $9B 飆到 $19B，還想跟黑石合開 AI 顧問公司。當賣晶片的要做模型、做模型的要做顧問，你就知道這產業的邊界正在劇烈重繪。

---

## 🌊 今日浪頭

### [英伟达豪掷 $26B 下场造 AI 模型，直接叫板 OpenAI](https://www.36kr.com/p/3719780712740233)

黃仁勳終於不演了。

Nvidia 正式宣布未來五年投入 $26B 開發開源 AI 大模型——沒聽錯，是那個賣 GPU 的 Nvidia，要自己下場做 frontier model。同時發布的 Nemotron 3 Super 有 1280 億參數，Nvidia 自稱在 AI Index 綜合評分拿了 37 分，GPT-OSS 只有 33 分。更猛的是，他們已經悄悄完成了一個 5500 億參數模型的預訓練。

這步棋的戰略邏輯其實很清楚：開源模型會針對 Nvidia 硬體做最佳化，開發者用了就離不開，生態黏性拉滿。Bryan Catanzaro 說得很直白：「幫助生態系統發展符合我們的利益。」翻譯一下就是：免費送你模型，但推理算力請用我的卡。加上 Nemotron 3 Super 在 PinchBench（測試模型對 OpenClaw 的控制能力）拿了第一名——Agent 時代要燒的 token 越多，Nvidia 的卡就賣得越多。

**為什麼這道浪值得追：**
- 從賣鏟到挖金，Nvidia 正式成為全棧 AI 公司，直接跟 OpenAI、Anthropic、DeepSeek 搶地盤
- 開源 + 硬體最佳化 = 生態鎖定，這招比單賣晶片的護城河深得多
- 下週 GTC 開發者大會，NemoClaw + Nemotron 組合拳可能才是真正的壓軸

### [Anthropic 年化收入飙至 $19B，拟联手黑石成立 AI 咨询公司](https://www.36kr.com/p/3719780892341635)

Anthropic 的成長速度，我看了數字也會倒吸一口氣。

年化收入從去年底的 $9B 飆到 $19B——幾個月內翻了一倍多。核心推力來自 Claude Code 和企業自動化產品 Cowork，這兩款在開發者和企業圈子裡已經是硬通貨了。以我自己的使用經驗，Claude Code 確實把我的工作效率拉高了不止一個檔次，所以這個增長我一點都不意外。

更有意思的是商業布局。Anthropic 正在跟黑石、Hellman & Friedman 等私募巨頭洽談，準備成立一家 AI 合資顧問公司，仿效 Palantir 的模式，向 250 多家被投企業輸出 Claude 技術。黑石旗下光是 Smartsheet 和 Bumble 就夠大了，私募圈的降本壓力意味著他們對 AI 有極強的付費意願。不過，這件事因為 Anthropic 跟國防部的法律戰而略有延遲——黑石 CEO 是共和黨大金主，這種時候高調站隊需要一點勇氣。

**為什麼這道浪值得追：**
- 年化收入翻倍的速度，正在快速縮小跟 OpenAI 的差距
- AI 顧問公司模式 = 把 Claude 直接推進數百家企業的核心業務流程，比 API 調用更深的綁定
- 五角大廈風波反而讓更多人知道 Anthropic——有時候爭議也是品牌曝光

### [Perplexity's "Personal Computer" brings AI agents to your Mac](https://arstechnica.com/ai/2026/03/perplexitys-personal-computer-brings-its-ai-agents-to-the-uh-personal-computer/)

Perplexity 要把你的 Mac 變成一個 24/7 運轉的 AI 分身。

繼上個月推出雲端版 Agent 工具「Computer」之後，Perplexity 這週發布了桌面版「Personal Computer」——讓你把一台閒置的 Mac 變成本地 AI Agent 系統，全天候運行，能直接操作你的檔案和應用程式。跟 OpenClaw 的概念很像，但 Perplexity 包裝得更精緻：有可停靠的側邊欄介面、多任務追蹤、遠端登入功能，還能從任何裝置遠端操控。

當然，讓 AI 在你的電腦上自由活動聽起來就很刺激——Perplexity 承諾有安全環境、敏感操作需要用戶確認、完整的稽核紀錄，還有一個「kill switch」。考慮到 OpenClaw 之前爆出不少讓人冒冷汗的事故，這些護欄確實有必要。同步推出的還有 Enterprise 版本，能連接企業應用，加上 Search、Agent、Embeddings、Sandbox 全面開放 API。

**為什麼這道浪值得追：**
- 這本質上是 OpenClaw 的商業精裝版——更友好的介面、更完善的安全機制、企業級支援
- Nvidia（NemoClaw）、Perplexity（Personal Computer）都在搶 Agent 平台入口——OpenClaw 點燃方向，但誰能標準化才是大生意
- 你睡覺的時候 AI 替你工作，遠端操控 + 24/7 運行，這個想像空間太大了

---

## ⚡ 衝浪快報

- **[Gemini's task automation is here and it's wild](https://www.theverge.com/tech/893820/gemini-task-automation-samsung-s26-google-pixel-10)** — Google Gemini 終於能幫你在手機上自動操作 App 了——叫外賣、叫車，在虛擬視窗裡替你完成。AI Agent 從電腦走進口袋
- **[Anthropic's Claude AI can respond with charts and diagrams now](https://www.theverge.com/ai-artificial-intelligence/893625/anthropic-claude-ai-charts-diagrams)** — Claude 現在會在對話中直接畫圖表和視覺化了，不再只是文字輸出。做數據分析的時候真的超好用
- **[Atlassian cuts 10% staff in the name of AI](https://techcrunch.com/2026/03/12/atlassian-follows-blocks-footsteps-and-cuts-staff-in-the-name-of-ai/)** — Atlassian 裁掉 1,600 人，理由是把資源導向 AI。繼 Block 之後又一家，「因 AI 裁員」從特例變成模式了
- **[疯狂的"龙虾"，撑起 MiniMax 3826 亿市值](https://www.36kr.com/p/3719781413205378)** — MiniMax 兩日飆升超 51%，市值正式超越百度。四年公司超越搜尋巨頭——Agent 想像空間 + 資本瘋狂，這劇本真的敢寫
- **[Claude 5 天重写老库引全网争议，原作者突然现身](https://www.36kr.com/p/3719844907070852)** — chardet 維護者用 Claude Code 五天重寫整個專案，把 LGPL 改成 MIT，退隱 15 年的原作者出來喊不准。AI 重寫代碼的版權歸屬，第一場認真打起來的仗
- **[Google Maps gets AI 'Ask Maps' powered by Gemini](https://www.theverge.com/tech/893262/google-maps-gemini-ai-ask-maps-immersive-navigation)** — Google Maps 加入 Gemini 驅動的自然語言問答功能，號稱十年來最大更新，還有沉浸式導航
- **[Microsoft launches Copilot Health](https://www.theverge.com/tech/893594/microsoft-copilot-health-launch)** — Copilot Health 能連接病歷和穿戴裝置了。AI 醫療，Microsoft 跟 Google 都在加速佈局
- **[Facebook Marketplace adds AI auto-replies](https://techcrunch.com/2026/03/12/facebook-marketplace-now-lets-meta-ai-respond-to-buyers-messages/)** — Meta AI 自動回覆買家訊息，那些煩死人的「Is this still available?」終於有 AI 來擋了
- **[ChatGPT「放棄」電商，豆包偏向虎山行](https://www.36kr.com/p/3719713736815109)** — OpenAI 放棄應用內購物，用戶推薦完商品但結帳全跑路。字節的豆包卻反向操作，直接在 App 內下單。AI 電商在美國水土不服，中國可能是另一個故事
- **[英伟达 GTC 2026 重磅前瞻](https://www.36kr.com/p/3720525353400709)** — 下週 GTC 開跑，華爾街盯的不是新 GPU 參數，是 Nvidia 能不能從「賣晶片」升級為「定義 AI 基礎設施規則」的平台
- **[Writer suing Grammarly for turning authors into 'AI editors'](https://techcrunch.com/2026/03/12/a-writer-is-suing-grammarly-for-turning-her-and-other-authors-into-ai-editors-without-consent/)** — 記者 Julia Angwin 對 Grammarly 發起集體訴訟，控告其未經同意就拿真人身分當 AI 審稿人。昨天才說要停用，今天就被告——先道歉再挨告的 SOP

---

## 🏄 深水區

- **[Coding After Coders: The End of Computer Programming as We Know It](https://simonwillison.net/2026/Mar/12/coding-after-coders/#atom-everything)** — 紐約時報雜誌的史詩級長文，訪了 Google、Amazon、Microsoft、Apple 超過 70 位開發者。如果今天只有時間讀一篇，就讀這篇——目前為止關於 AI 如何改變程式設計，最全面也最有深度的報導
- **[The Department of War is making a huge mistake](https://www.dwarkesh.com/p/dow-anthropic)** — Dwarkesh Patel 深度分析國防部把 Anthropic 列為供應鏈風險的荒謬。當 LLM 只是「勉強有用」的今天就這樣搞，等 AI 真正強大的時候會發生什麼？這篇寫得很有力度，值得花時間讀
- **[I don't know if I like working at higher levels of abstraction](https://xeiaso.net/blog/2026/ai-abstraction/)** — 一位資深工程師的真實告白：用 Claude 做事的時候，結果是出來了，但「什麼都沒有流過我」。當你從寫程式碼變成描述意圖，你到底是進化了還是失去了什麼？讀完會有點感觸
