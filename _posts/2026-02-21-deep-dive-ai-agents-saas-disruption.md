---
title: "當 AI Agent 開始吃掉 SaaS：一場 2 兆美元的產業海嘯"
date: 2026-02-21
description: "2026 年 2 月，AI Agent 引爆 SaaS 產業史上最大拋售潮，2 兆美元市值蒸發。從 Klarna 的激進實驗到 Salesforce 的定價革命，per-seat 授權模式正在崩解——但 SaaS 真的要死了嗎？深入剖析這場產業海嘯的真相、贏家與輸家。"
tags: [deep-dive, ai-industry, agents, ai-tools]
---

## 引言

2026 年 2 月 3 日，一個看似平常的星期一，Nasdaq Cloud Index 在兩天內蒸發了將近 3,000 億美元的市值。Salesforce 股價暴跌超過 25%，Adobe 的本益比從一年前的 26 倍壓縮到 16 倍。華爾街的交易員們給這場屠殺取了一個戲劇性的名字——**SaaSpocalypse**，SaaS 末日。

觸發這場崩盤的，不是什麼金融危機或經濟衰退。是兩個產品發布：Anthropic 的 Claude Cowork 和 OpenAI 的 Project Operator。前者讓 AI Agent 能自主管理複雜的商業流程，後者則讓 AI 直接操作任何軟體介面——不需要人類登入、不需要人類點擊、不需要人類「坐在座位上」。

當 AI Agent 不需要座位，per-seat 授權模式就失去了存在的意義。

這場恐慌的導火線，其實在更早之前就已經埋下。2025 年，瑞典金融科技公司 Klarna 的 CEO Sebastian Siemiatkowski 高調宣布，公司已經從 7,000 人縮減到不到 3,000 人，而且還打算在 2030 年前進一步縮減到 2,000 人。他的 AI 客服機器人據說能做 [800 個全職客服的工作](https://fortune.com/2026/02/17/klarnas-ceo-dario-amodei-ai-white-collar-workforce-shrink-2030/)，把平均問題解決時間從 11 分鐘壓到 2 分鐘以內。更勁爆的是，Klarna 宣稱要「關閉 SaaS 供應商」，用 AI 取代整個企業軟體堆疊。

但故事沒有那麼簡單。事實上，Klarna 的 CEO 後來承認「我們走得太遠了」，開始重新聘僱人類員工。而且他們實際上並沒有用 AI 取代 Salesforce——他們只是換了一套 SaaS 工具。

這篇報導的起點是 [Roundly.io 的一篇分析](https://roundly.io/blog/klarna-ai-agents-replacing-saas)，標題直接叫「SaaS 滅絕事件」。但真正的故事，遠比「SaaS 要死了」複雜得多。這是一場關於定價模式、資料壟斷、企業軟體架構，以及 AI 到底能取代什麼、不能取代什麼的深度拆解。

---

## 事件全貌

### SaaSpocalypse 的引爆時刻

讓我們把時間拉回 2026 年 2 月初。

2 月 3 日，Anthropic 正式推出 [Claude Cowork](https://www.anthropic.com/claude)——一套能夠自主管理複雜商業流程的 AI Agent 系統。同一天，OpenAI 發布了 Project Operator，讓 AI 能直接透過瀏覽器介面操作任何軟體，跳過傳統的 API 整合。這兩個產品的共同訊息很明確：**AI Agent 不再需要人類作為中介去使用軟體**。

市場的反應是即時且劇烈的。根據 [Financial Content 的報導](https://markets.financialcontent.com/stocks/article/marketminute-2026-2-18-the-death-of-the-seat-how-ai-agents-triggered-the-2026-saaspocalypse-for-salesforce-and-adobe)，在 2 月 3 日到 4 日兩天內，Nasdaq Cloud Index 就蒸發了近 3,000 億美元。到了 2 月中旬，整個軟體產業累計市值損失高達約 **2 兆美元**。

這不是一般的股市回調。軟體公司的 forward earnings multiple 從 39 倍暴跌到 21 倍，回到 2010 年代中期的水準。分析師們爭先恐後地創造新詞彙——SaaSpocalypse、SaaSmageddon、SaaS 末日——來描述這場前所未有的產業震盪。

### 「Seat Compression」：一個新概念的誕生

這場恐慌的核心，是一個叫做 **seat compression**（座位壓縮）的概念。邏輯很直觀：如果一個 AI Agent 能做 10 個業務員的工作，你就不需要 10 個 Salesforce 的授權席位。座位數量壓縮 90%，營收就壓縮 90%。

過去二十年，SaaS 公司的商業模式建立在一個簡單的公式上：**客戶公司的員工越多 = 需要的座位越多 = SaaS 公司的營收越高**。這個模式在人類勞動力持續擴張的時代運作得完美。但當 AI Agent 開始取代人類執行任務時，這個公式就徹底崩解了。

Salesforce 的應對策略是推出 [Agentic Enterprise License Agreement（AELA）](https://markets.financialcontent.com/stocks/article/marketminute-2026-2-18-the-death-of-the-seat-how-ai-agents-triggered-the-2026-saaspocalypse-for-salesforce-and-adobe)，透過所謂的「Flex Credits」按每個自主操作收費 0.10 美元。Adobe 則轉向「Generative Credit」系統，使用者（或他們的 AI Agent）按產出付費，而不是按軟體存取權付費。

這些都是在恐慌中緊急推出的止血措施。市場的疑問是：這些每筆 0.10 美元的微交易，真的能彌補失去的高毛利訂閱收入嗎？

### Klarna：從海報案例到反面教材

Klarna 一直是「AI 取代一切」敘事的海報案例。CEO Siemiatkowski 的數字確實驚人：員工從 7,000 人砍到不到 3,000 人，一個 AI 聊天機器人做了 800 個客服的工作，整個營運效率大幅提升。

但 [CX Today 的調查報導](https://www.cxtoday.com/crm/klarna-didnt-replace-salesforce-it-replaced-them-with-alternative-saas-apps/) 揭露了一個尷尬的事實：**Klarna 並沒有用 AI 取代 Salesforce，他們只是換成了其他 SaaS 工具**。他們用 Deel 取代了 Workday 做人力資源管理，CRM 功能則是透過「多個第三方和內部解決方案」的組合來替代。Klarna 甚至還繼續使用 Salesforce 旗下的 Slack。

更尷尬的是，Siemiatkowski 後來公開承認 [AI 替代策略走得太遠了](https://www.entrepreneur.com/business-news/klarna-ceo-reverses-course-by-hiring-more-humans-not-ai/491396)。內部審查和客戶反饋顯示，AI 系統缺乏同理心，無法處理客服中需要細膩判斷的複雜情境。Klarna 正在重新聘僱人類客服，採用一種類似 Uber 的彈性工作模式。

一句話總結：AI 取代 SaaS 的旗手，自己證明了 AI 取代有其極限。

---

## 脈絡

### SaaS 帝國是怎麼建起來的

要理解為什麼 AI Agent 對 SaaS 構成威脅，得先理解 SaaS 的護城河到底是什麼。

過去二十年，企業軟體公司建立帝國的方式驚人地一致：先讓企業把資料倒進你的系統，然後靠資料遷移的巨大摩擦成本鎖住客戶。你可能對 CRM 系統不滿意，但要把幾百萬筆客戶紀錄從 Salesforce 搬到另一個平台？那是幾個月的顧問費和整合工作。所以你留下來了，每年乖乖續約，還接受漲價。

這就是所謂的 **data lock-in**（資料鎖定）。它不是技術上的護城河，而是行政上的護城河。

在 ZIRP（零利率政策）時代，這個模式把 SaaS 公司的估值推到了瘋狂的高度。根據 [Aventis Advisors 的數據](https://aventis-advisors.com/saas-valuation-multiples/)，企業 SaaS 公司的營收倍數在高峰期達到 20-30 倍。投資人的邏輯是：高毛利、近乎零的客戶流失率、每年自動成長的訂閱收入——這是印鈔機，值得高估值。

### 企業軟體堆疊的膨脹病

但 SaaS 的成功也帶來了一個結構性問題：**企業軟體堆疊的極度膨脹**。

原始文章中有一個精彩的例子：一個企業客戶——比如 Sephora——在 Salesforce 裡是一筆 CRM 紀錄、在 Slack 裡是一個專屬頻道、在 Google Drive 裡是一堆簡報檔、在 Stripe 裡是一筆帳務紀錄、在 Zendesk 裡是一段客服歷史。**同樣的基本資訊，在十幾個不同的供應商系統裡被重複儲存、重複處理、重複付費**。

Siemiatkowski 拿 Wikipedia 做對比：Wikipedia 是全世界最成功的知識圖譜，因為它嚴格執行單一事實來源原則——關於 Sephora 的資訊只有一篇文章，不是十五篇。

### 歷史的回音：這不是第一次

如果你在科技圈待得夠久，會發現類似的恐慌並不新鮮。

2000 年代中期，開源軟體的崛起曾讓人預言商業軟體的末日。Linux 要殺死 Windows Server，MySQL 要幹掉 Oracle，Red Hat 要顛覆微軟。結果呢？商業軟體沒有消亡，而是被迫提供更好的整合、更可靠的支援和更完善的企業功能。開源確實壓低了軟體的價格地板，但也同時擴大了整個市場的規模。

2010 年代初期，「雲端將殺死企業 IT」的說法同樣甚囂塵上。AWS 和 Azure 確實顛覆了 on-premise 的部署模式，但這個過程花了十五年，而且許多企業至今仍在混合雲的過渡期中。

這次的 AI Agent 顛覆，和之前的開源革命、雲端遷移有一個本質上的不同：**它同時攻擊 SaaS 的技術護城河（資料鎖定）和商業護城河（per-seat 定價）**。前者是因為 AI 能大幅降低資料遷移成本，後者是因為 AI 直接減少了「需要座位」的人數。這種雙重夾擊，是 SaaS 之前從未面對過的。

### 為什麼是「現在」

AI Agent 的能力在 2025-2026 年達到了一個關鍵轉折點。早期的 AI 助手只能回答問題或生成文字；現在的 AI Agent 能夠**推理、規劃、跨系統執行多步驟任務**。OpenAI 的 o3 推理模型在兩個月內成本下降了 80%，讓大規模部署 Agent 變得經濟可行。

[Deloitte 的數據](https://www.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions/2026/saas-ai-agents.html) 顯示了一組關鍵指標：企業員工接觸 AI 的比例在 2025 年上升了 50%，73% 的受訪企業領袖在過去 12 個月內為 AI 或 GenAI 能力撥款，39% 明確投資了 Agentic AI。目前有 23% 的公司正在適度使用 Agentic AI，但兩年內這個數字預計會飆升到 74%。

[Bain & Company 的報告](https://www.bain.com/insights/will-agentic-ai-disrupt-saas-technology-report-2025/) 用一句話概括了這個轉折：「三年內，任何例行性、規則型的數位任務，都可以從『人類 + 應用程式』轉變為『AI Agent + API』。」

當 AI Agent 能夠無縫地從一個系統提取資料、重新映射、部署到另一個系統時，data lock-in 的護城河就不攻自破了。企業不再需要忍受糟糕的軟體，因為遷移成本從「幾個月的顧問費」變成了「一個 prompt」。

這就是為什麼市場反應如此劇烈。這不只是「又一個 AI 功能」的故事——這是整個商業模式的地基在動搖。

---

## 多方觀點

### 末日派：SaaS 已死

最激進的聲音來自投資圈和新創社群。[Remio.ai 的分析](https://www.remio.ai/post/saas-pocalypse-2026-why-ai-agents-are-wiping-out-300b-in-software-value) 直接把這場危機比喻為「3,000 億美元的軟體價值被 AI Agent 抹去」。他們的核心論點是：

- **Per-seat 模式已死**：當一個 AI Agent 能取代幾十個人的工作，按人頭收費的模式就不再成立
- **資料護城河正在瓦解**：AI 的資料遷移能力讓 switching cost 趨近於零
- **Vibe coding 讓 SaaS 複製變得廉價**：非技術人員也能用 AI 快速搭建出類似功能的應用

原始文章的作者更是直言：「軟體印鈔機壞了。我們正醒來面對一個現實——產品真的得做事才行。」

值得注意的是，連 Klarna 的 CEO 自己也站在這個陣營。Siemiatkowski 明確表態[他比較認同 Anthropic CEO Dario Amodei 的觀點](https://fortune.com/2026/02/17/klarnas-ceo-dario-amodei-ai-white-collar-workforce-shrink-2030/)，後者警告 AI 可能消滅 50% 的入門級職位，推動失業率升至 10-20%。Siemiatkowski 說：「我想誠實面對這個事實——我確實認為將會有非常大的轉變。」他把員工的薪資提高了近 50%，用更高的個人產出來彌補人數的減少——這個模式如果被其他企業效仿，對 per-seat SaaS 的衝擊會更加劇烈。

### 審慎樂觀派：SaaS 在轉型，不是消亡

但另一邊的數據同樣有說服力。

[Forrester 的分析](https://www.forrester.com/blogs/saas-as-we-know-it-is-dead-how-to-survive-the-saas-pocalypse/) 指出，儘管市場恐慌，全球 SaaS 支出預計仍將從 2025 年的 **3,180 億美元**成長到 2029 年的 **5,760 億美元**。垂直領域軟體（針對醫療、製造、製藥等特定產業的解決方案）甚至預計從 1,335 億美元成長到 1,940 億美元。

JPMorgan 的策略師則認為這次拋售是潛在的買入機會，認為市場對 AI 顛覆的悲觀預期已經超過了實際影響。

Gartner 給了一個更精確的預測框架：到 2030 年，**35% 的單點 SaaS 工具會被 AI Agent 取代**，但這也意味著 65% 不會。到 2030 年，至少 40% 的企業 SaaS 支出將轉向使用量、Agent 或成果導向的定價模式——這是轉型，不是消亡。

### 實務工作者：Klarna 的教訓

最有說服力的觀點來自真正嘗試過的人。

Klarna 的故事是一面兩面鏡子。一方面，他們確實用 AI 大幅提升了效率——AI 聊天機器人處理了三分之二的客服互動，解決時間從 11 分鐘降到 2 分鐘。另一方面，CEO Siemiatkowski [公開承認](https://www.entrepreneur.com/business-news/klarna-ceo-reverses-course-by-hiring-more-humans-not-ai/491396)「對效率和成本的過度關注，最終降低了公司產品的品質，侵蝕了客戶的信任。」

更值得玩味的是，Klarna 在 SaaS 替代上的實際做法也與宣傳不符。他們不是用 AI 取代了 Salesforce——他們是用另一套 SaaS 工具取代了 Salesforce。這是一個「精簡和優化」的故事，而不是一個「AI 消滅一切」的故事。

[Fortune 的報導](https://fortune.com/2025/05/09/klarna-ai-humans-return-on-investment/) 還引用了一項調查，顯示大多數 AI 專案未能達到預期回報。Klarna 的經驗不是孤例——它可能代表了整個產業在 AI 採用上即將面臨的清算。

### 我的看法

以我在科技圈混了這麼多年的經驗，看到這種「XX 已死」的敘事已經見過太多次了。雲端運算「殺死」了本地部署？沒有，它花了十五年慢慢侵蝕。手機「殺死」了桌面？也沒有，只是改變了使用情境。

**SaaS 不是在死亡，它是在被迫進化。** 真正在死的，是那個特定的商業模式——per-seat 授權、資料鎖定、每年漲 5% 的懶人訂閱。但企業仍然需要軟體來管理營運，仍然需要可靠的系統來處理合規和資料安全。

Klarna 的案例完美地說明了這個區別。他們試圖用 AI 取代一切，結果發現 AI 擅長的是標準化的重複任務，不擅長的是需要人類判斷力的複雜情境。他們試圖拋棄所有 SaaS，結果只是換了一套 SaaS。

這場 2 兆美元的市值蒸發，與其說是「SaaS 末日」，不如說是一場遲來已久的**重新定價**。市場終於開始區分「真正有護城河的軟體」和「靠資料鎖定苟延殘喘的租金收割者」。這對整個產業來說，其實是健康的。

---

## 產業衝擊

### 第一層：誰受益，誰受損

**最直接的輸家**是那些依賴高客單價 per-seat 授權的水平型 SaaS 公司。想想那些功能單一、切換成本低、沒有獨特資料護城河的工具——專案管理、文件簽署、基礎 CRM、簡單的客服系統。當 AI Agent 能在幾分鐘內複製這些功能時，每月 150 美元/人的訂閱費就顯得荒謬了。

根據 [Bain 的分析框架](https://www.bain.com/insights/will-agentic-ai-disrupt-saas-technology-report-2025/)，最脆弱的 SaaS 工作流程具備以下特徵：高度結構化和重複性的任務、低度的專有資料依賴、高度的產業標準化、以及成熟的 Agent 協議支持。

**最直接的贏家**是 AI 基礎設施提供者——OpenAI、Anthropic、Google——以及那些能在 AI 時代重新定位的垂直領域軟體公司。垂直軟體之所以更安全，是因為它們掌握著特定產業的專有資料和合規邏輯，這些是通用 AI Agent 短期內難以複製的。[Forrester 預測](https://www.forrester.com/blogs/saas-as-we-know-it-is-dead-how-to-survive-the-saas-pocalypse/)垂直軟體市場將在 2029 年達到 1,940 億美元。

### 第二層：定價模式的革命

這場危機正在強迫整個產業重新思考「軟體應該怎麼收費」。

傳統的 per-seat 模式正在向三個方向分裂：

1. **使用量計費**（consumption-based）：按 API 呼叫次數、處理的資料量或消耗的運算資源計費。AWS 模式的推廣版。
2. **成果計費**（outcome-based）：按實際完成的任務計費——解決了幾張客服單、生成了幾份報告、處理了幾筆交易。Salesforce 的 AELA 模式（每次自主操作 0.10 美元）就是這個方向的試探。
3. **Generative Credit 系統**：Adobe 率先採用的模式，使用者按產出（一張圖、一段影片、一份設計稿）付費，而不是按軟體存取權付費。

[Deloitte 的數據](https://www.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions/2026/saas-ai-agents.html) 顯示，83% 的 AI 原生 SaaS 公司已經採用使用量計費模式。但 Gartner 預測，要到 2030 年，才會有 40% 的企業 SaaS 支出轉向新的定價模式。這中間的過渡期——大約三到五年——會是一段非常混亂的時期。

對企業來說，好消息是議價權正在從供應商轉移到買家手中。Forrester 建議企業現在就應該開始重新談判合約，為定價模式的轉型做準備。

### 第三層：開發者生態的重塑

對開發者來說，這場變革帶來的影響是雙面的。

一方面，「SaaS 被 AI 取代」的敘事創造了一個全新的市場機會。**Agent-first 的新創公司**正在大量湧現，它們不是在做另一個 SaaS 工具，而是在做 AI Agent 的協調層、安全層、監控層。這是一個全新的技術棧，需要全新的開發能力。

另一方面，Bain 的報告指出了一個關鍵的基礎設施缺口：AI Agent 的 **語義層**（semantic layer）。目前不同供應商的 Agent 之間缺乏統一的概念定義——什麼是「發票」？什麼是「客戶」？什麼是「訂單」？Anthropic 的 Model Context Protocol 和 Google 的 Agent2Agent 正在嘗試建立通訊協議，但定義跨供應商概念的語義標準仍然是空白。Bain 認為，誰能率先建立這個語義層，誰就能掌握「下一波巨大價值」。

對於傳統 SaaS 公司的開發團隊，挑戰則更為複雜。他們需要把按座位設計的產品架構重新改造成按使用量或按成果計費的架構——這不只是改定價頁面，而是要重新設計整個計量、計費和授權系統。同時，他們還得在產品中深度整合 AI 能力，否則就會被原生 AI 產品超越。

### 第四層：大玩家的反擊

傳統 SaaS 巨頭並不是坐以待斃。

Salesforce 雖然股價暴跌，但它的 [Agentforce 平台](https://markets.financialcontent.com/stocks/article/marketminute-2026-2-18-the-death-of-the-seat-how-ai-agents-triggered-the-2026-saaspocalypse-for-salesforce-and-adobe) 已經實現了 84% 的客戶互動自主化。問題是，當你的 AI 替客戶做了 84% 的工作，客戶為什麼還要付那麼多錢？Salesforce 試圖用 AELA 模式（每次自主操作收 0.10 美元）來回答這個問題，但市場對這個微交易模式能否撐起原本的高毛利營收仍持懷疑態度。

OpenAI 和 Anthropic 則從另一端切入。OpenAI 推出了 OpenAI Frontier 平台，讓企業建構、部署和管理 AI Agent，旗艦客戶包括 HP、Intuit、Oracle 和 Uber。Anthropic 的 Claude Cowork 則直接讓小型企業主開始質疑他們的 SaaS 訂閱費用。這兩家公司正在從「模型供應商」轉型為「企業作業系統」——這個定位直接威脅到 Salesforce、ServiceNow、Workday 的核心地盤。

根據 [Mayer Brown 的法律分析](https://www.mayerbrown.com/en/insights/publications/2026/02/contracting-for-agentic-ai-solutions-shifting-the-model-from-saas-to-services)，合約結構也在跟著變。傳統的 SaaS 合約正在被「Agentic AI 服務合約」取代，定價從軟體存取權轉向服務成果。這不只是商業模式的變化——整個企業軟體的法律和採購框架都在重建。

### 第五層：二階效應

這場產業重整會觸發幾個值得關注的連鎖反應：

**併購潮**。手上有現金的大型 SaaS 公司會開始大量收購 agent-first 新創公司，用買的方式補齊 AI 能力。反過來，估值崩跌的中小型 SaaS 公司會成為被收購的目標。預期 2026 下半年到 2027 年會看到一波軟體產業的整合潮。

**企業 IT 部門的權力重組**。當 AI Agent 能直接完成任務，繞過傳統軟體介面時，CIO 的角色從「管理軟體供應商關係」轉變為「管理 AI Agent 的治理和安全」。[Deloitte 的數據](https://www.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions/2026/saas-ai-agents.html) 顯示，高達 75% 的公司可能在 2026 年投資 Agentic AI，但只有 23% 已經在適度使用。這中間的落差代表著巨大的執行風險。

**新的關鍵指標**。投資人評估軟體公司的關鍵指標正在從 ARR（年度經常性收入）轉向 **Credit Consumption Velocity**（信用消耗速度）。這個轉變會重塑整個軟體產業的估值邏輯。

---

## 未來展望

### 短期（3-6 個月）：動盪繼續

幾件幾乎確定會發生的事：

- **更多 SaaS 公司宣布定價模式改革**。Salesforce 和 Adobe 已經開了第一槍，接下來 ServiceNow、Workday、HubSpot 等都會跟進，推出某種形式的使用量計費或成果計費選項。
- **財報季的逐筆審查**。投資人會逐字檢查每家 SaaS 公司的 AI 策略和座位數變化。任何顯示 seat compression 跡象的公司都會被無情拋售。
- **Klarna 效應擴散**。更多公司會嘗試用 AI 減少軟體訂閱支出，但也會有更多公司發現 AI 替代的限制——預計會看到更多「走得太遠然後回調」的案例。

### 中期（6-18 個月）：三條可能的路徑

**情境一：漸進轉型（最可能）**。SaaS 公司逐步在現有產品中整合 AI Agent 能力，定價模式混合 per-seat 和 usage-based，市場慢慢消化估值壓縮。垂直 SaaS 表現優異，水平 SaaS 持續承壓。這基本上就是 Forrester 和 Deloitte 預測的路徑。

**情境二：加速替代**。如果 AI Agent 的能力在接下來一年內出現又一次跳躍式進步（比如 Agent 能可靠地處理合規和安全敏感的任務），替代速度可能比預期快得多。這個情境下，更多的傳統 SaaS 公司會面臨生存危機。

**情境三：AI 幻滅期**。如果企業在大規模部署 AI Agent 後發現可靠性、安全性和成本都達不到預期（就像 Klarna 的經驗那樣），市場可能會出現反向修正。SaaS 股票反彈，「AI 取代一切」的敘事降溫。

### 長期推演：3-5 年後的世界

如果當前趨勢持續，到 2028-2030 年，企業軟體的格局會長這樣：

**「Service as Software」取代「Software as a Service」**。企業購買的不再是軟體工具，而是服務成果。你不買一個 CRM 系統——你訂閱一個「客戶關係管理服務」，底層可能是 AI Agent 加上開源資料庫，也可能是某個重新包裝的 SaaS 平台。使用者不在乎也不需要知道。

**三層架構的新秩序**。Bain 的報告描繪了一個清晰的三層架構：底層是 Systems of Record（資料紀錄系統），中間是 Agent Operating Systems（Agent 協調層），上層是 Outcome Interfaces（成果介面）。競爭會在每一層發生，但最大的價值創造可能在中間的協調層——這也是為什麼 OpenAI 和 Anthropic 都在積極佈局企業市場。

**SaaS 公司的兩極分化**。一部分 SaaS 公司會成功轉型為「AI 原生」平台，用 AI 強化而非取代其核心功能。另一部分會萎縮為 commodity utility，以極低的利潤運營。中間的灰色地帶會消失。

### 給讀者的行動建議

**如果你是開發者**：現在最值得投資的技能不是「學 AI」這麼籠統，而是要具體學會**建構和協調 AI Agent 系統**。理解 Anthropic 的 Model Context Protocol、學會設計 Agent 的工具使用邏輯、掌握 AI 原生應用的計量和計費架構。這些是接下來三年最有價值的技能。

**如果你是創業者或產品經理**：不要再用 SaaS 的舊劇本——建一個漂亮的介面、鎖住使用者資料、收月費。新的劇本是：**掌握某個垂直領域的獨特資料、建構能產出可衡量成果的 AI Agent、按成果收費**。如果你的產品只是一個 AI 的薄薄包裝，你很快就會被更好的模型或免費的開源方案取代。

**如果你是一般科技從業者**：關注你公司的軟體支出變化。如果你的老闆開始談論「用 AI 取代 XX 工具」，那是你的機會——成為推動這個轉型的人，而不是被轉型淘汰的人。同時，記住 Klarna 的教訓：AI 能做的事和 AI 應該做的事之間有很大的差距。能辨別這個差距的人，在接下來幾年會非常搶手。

最後，站遠一點看，這場 SaaSpocalypse 其實是科技產業自我淨化的過程。過去十年 ZIRP 時代養出來的軟體泡沫——靠資料鎖定收租、靠功能堆疊漲價、靠慣性留住不滿意的客戶——本來就不該有那麼高的估值。AI Agent 只是加速了這個清算。

真正好的軟體——解決真實問題、掌握獨特資料、持續為使用者創造價值的軟體——不但不會消亡，反而會在這場洗牌中變得更強。而那些「產品真的得做事才行」的時代，對所有人來說，其實是好事。

---

## 延伸閱讀

- [The SaaS Extinction Event — Roundly.io](https://roundly.io/blog/klarna-ai-agents-replacing-saas)：本文的出發點，分析 Klarna 的 AI Agent 策略如何威脅傳統 SaaS 估值模型
- [Will Agentic AI Disrupt SaaS? — Bain & Company](https://www.bain.com/insights/will-agentic-ai-disrupt-saas-technology-report-2025/)：最完整的 SaaS 顛覆框架，包含五種戰略情境分析和兩維度評估工具
- [SaaS As We Know It Is Dead — Forrester](https://www.forrester.com/blogs/saas-as-we-know-it-is-dead-how-to-survive-the-saas-pocalypse/)：Forrester 對 SaaSpocalypse 的冷靜分析，包含企業買家的四步應對策略
- [SaaS meets AI agents — Deloitte](https://www.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions/2026/saas-ai-agents.html)：Deloitte 2026 年預測，包含企業 AI 投資數據和定價模式轉型分析
- [Klarna Didn't Replace Salesforce with AI — CX Today](https://www.cxtoday.com/crm/klarna-didnt-replace-salesforce-it-replaced-them-with-alternative-saas-apps/)：揭露 Klarna「AI 取代 SaaS」敘事背後的真實情況
- [Klarna CEO Reverses Course on AI — Entrepreneur](https://www.entrepreneur.com/business-news/klarna-ceo-reverses-course-by-hiring-more-humans-not-ai/491396)：Klarna CEO 承認 AI 替代走得太遠，開始重新聘僱人類員工
- [The Death of the 'Seat' — Financial Content](https://markets.financialcontent.com/stocks/article/marketminute-2026-2-18-the-death-of-the-seat-how-ai-agents-triggered-the-2026-saaspocalypse-for-salesforce-and-adobe)：詳細記錄 SaaSpocalypse 的市場衝擊數據，包括 Salesforce 和 Adobe 的應對策略
- [Klarna CEO on AI Workforce — Fortune](https://fortune.com/2026/02/17/klarnas-ceo-dario-amodei-ai-white-collar-workforce-shrink-2030/)：Klarna CEO 預測 2030 年公司員工進一步縮減至 2,000 人
