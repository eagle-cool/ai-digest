---
title: "免費的暴力：當 Vibe Design 撕開 SaaS 末日的序幕"
date: 2026-03-22
description: "Google 一個免費的 AI 設計工具 Stitch，讓合作夥伴 Figma 兩天蒸發 12% 市值。從 Vibe Coding 到 Vibe Design，AI 正在系統性摧毀整個 SaaS 產業的定價邏輯，而這場屠殺才剛開始。"
tags: [deep-dive, ai-tools, ai-industry]
---

## 引言

3 月 18 日，Google 在自家部落格上低調發了一篇文章，介紹旗下 AI 設計工具 Stitch 的最新更新。沒有發布會，沒有倒數計時，就是一篇技術部落格。

隔天早上，Figma 股價暴跌 8%。再隔一天，又跌了 4%。兩個交易日，市值蒸發超過 12%。

這不是什麼黑天鵝事件。Google 做的事情很簡單——它讓 Stitch 支援了「Vibe Design」：用自然語言甚至語音告訴 AI 你想要什麼樣的介面，它就直接幫你生成出來。不需要 Figma，不需要拖拽元件，不需要調間距。你只要開口說話就好。

最諷刺的是什麼？就在五個月前，2025 年 10 月 9 日，Google Cloud 和 Figma 才剛高調宣布「擴大合作」，要把 Gemini 2.5 Flash 和 Imagen 4 整合進 Figma 平台。當時 Google Cloud CEO Thomas Kurian 還說：「數百萬用戶將受益於 Google AI 模型和 Figma 工具的結合。」

五個月後，Google 親手成了那個拿槍指著 Figma 的人。

但這篇文章要講的，不只是一家公司的股價波動。Figma 的危機只是冰山一角——2026 年初，整個軟體產業已經蒸發了約 2 兆美元市值，「SaaSpocalypse」（SaaS 末日）成了華爾街的新流行語。當 AI 能免費做到專業工具 80% 的功能，以每人每月 12 到 90 美元計價的 SaaS 模式，還有明天嗎？

這篇報導的起點是[量子位的這篇分析](https://www.36kr.com/p/3733553048256518)，但故事遠不止於此。

---

## 事件全貌

### Google Stitch：一個「實驗性工具」的核武級升級

Stitch 並不是新產品。它最早在 2025 年 Google I/O 上作為 Google Labs 的實驗項目亮相，當時能做的事情很有限——輸入一段文字描述，生成一個 UI 畫面。一次只能生成一個畫面，沒有什麼了不起的。

但 3 月 18 日的更新，是一次質變。Google 一口氣推出了五個重大功能：

**第一，AI 原生畫布。** Stitch 採用了基於節點的無限畫布設計，可以同時容納圖片、程式碼、產品需求文件（PRD），讓你在一個空間裡並行探索多個設計方向。這不是在現有工具上加 AI——這是從零打造一個以 AI 為核心的設計環境。

**第二，設計 Agent。** 這個 Agent 能理解你整個專案的演進歷史，不再是每次對話都從零開始。它處理版面決策、元件選擇、迭代優化，基於你餵給它的提示詞、截圖、程式碼片段和競品 UI 參考來做判斷。一次可以生成最多五個畫面。

**第三，語音互動。** 你可以直接對著畫布說話。AI 會聽你講，問你釐清問題，給你即時設計點評，然後直接動手改。完全免手動操作。

**第四，即時原型。** 靜態畫面點一下「播放」就變成可互動的原型，Stitch 會自動判斷畫面之間的邏輯關係、加上轉場效果，還能分享連結給別人看。

**第五，DESIGN.md。** 這是一種用自然語言寫的設計規範檔案，可以跨專案匯入匯出，確保設計一致性。更狠的是，它直接提供 MCP（Model Context Protocol）整合，能無縫對接 Claude Code、Cursor、Gemini CLI——設計完直接丟給 AI 寫程式。

而且，全部免費。350 次月生成額度，只要有 Gmail 帳號就能用。Google 甚至沒有承諾服務可用性——言下之意是：這只是個實驗，但我們不收你錢。

### Figma 的股價，和那個尷尬的合作

Figma 不是小公司。2025 年 7 月在紐交所 IPO，代碼 FIG，當天股價最高飆漲 275%，市值一度逼近 680 億美元，後來穩定在約 570 億。CEO Dylan Field 從大學輟學生變成了億萬富翁。2025 年全年營收 10.6 億美元，年增 41%。Q4 單季營收 3.038 億。淨收入留存率 136%——意味著老客戶不但沒跑，還花更多錢。

但 2026 年開年後，一切都變了。Figma 股價年初至今已經下跌約 35%，和整個軟體產業一起崩。Google Stitch 的更新只是壓倒駱駝的那根稻草——但這根稻草的殺傷力特別大，因為它直接打中了 Figma 的核心功能：UI/UX 設計。

[CNBC 的報導](https://www.cnbc.com/2026/03/19/figma-stock-drops-11percent-after-google-releases-vibe-design-product-stitch.html)指出，Figma 在產品設計軟體領域的市場份額高達 80-90%。但 Google 手上有三張 Figma 沒有的牌：**免費**（零元 vs. 每人每月 12-90 美元）、**分發**（數億 Workspace 企業用戶已經在 Google 生態裡）、**捆綁**（買企業套餐順手就用了）。

Google 不需要在技術上碾壓 Figma，只需要「夠用」，然後用生態吃掉市場份額。

---

## 脈絡

### 從 Vibe Coding 到 Vibe Design：AI 吞噬的路徑

要理解 Vibe Design 為什麼重要，得先回溯一年前的 Vibe Coding。

2025 年 2 月 2 日，前 OpenAI 共同創辦人、前 Tesla AI 負責人 Andrej Karpathy 在 X 上發了一則推文，獲得超過 450 萬次觀看。他寫道：「有一種新的寫程式方式，我叫它 vibe coding——你完全投入氛圍，擁抱指數級成長，然後忘掉程式碼的存在。」

這個詞在一年內從一則推文變成了 Merriam-Webster 收錄的俚語、Collins 英語辭典 2025 年度詞彙，以及一整個產業運動的代名詞。Cursor、Bolt、Replit、Lovable——一大批工具讓不會寫程式的人也能用自然語言「說」出一個 App。

而到了 2026 年，Karpathy 自己都說 vibe coding [已經過時了](https://thenewstack.io/vibe-coding-is-passe/)，他現在偏好的說法是「agentic engineering」——因為 LLM 已經聰明到你 99% 的時間都不需要自己寫程式，你只是在指揮 Agent 幹活。

有趣的是，Karpathy 在提出 vibe coding 的時候就預示了它的擴散。他原文提到自己是用 SuperWhisper（語音轉文字工具）加上 Cursor Composer 搭配 Sonnet 來「vibing」——語音、AI、自然語言，這三個元素的組合不只能用在寫程式，它本質上可以用在任何創作活動。

Vibe Design 是這條路徑的自然延伸。如果 AI 能幫你寫程式，為什麼不能幫你做設計？如果你可以用嘴巴告訴 Cursor 你想要什麼功能，為什麼不能用嘴巴告訴 Stitch 你想要什麼介面？從 vibe coding 到 vibe design，本質上是同一種範式——用意圖驅動取代手動執行——在不同領域的複製。

### Adobe 那個 200 億美元的教訓

說到 Figma，就不得不提 2022 年那筆轟動業界的收購案。Adobe 宣布以 200 億美元收購 Figma——當時 Figma 的年營收不到 5 億，這個價格是 50 倍營收。華爾街震驚了。

但歐盟和英國的反壟斷監管機構不買帳。Figma 在產品設計軟體市場佔了超過 80% 的營收份額，而 Adobe 自家的 XD 只有 5-10%。監管機構認為這筆交易會扼殺競爭。2023 年 12 月，[Adobe 和 Figma 共同宣布終止合併](https://news.adobe.com/news/news-details/2023/adobe-and-figma-mutually-agree-to-terminate-merger-agreement)，Adobe 支付了 10 億美元的分手費。

事後來看，Adobe 虧大了。Figma 2025 年 IPO 後市值最高接近 680 億，比 Adobe 當年出價高了超過 370 億。但現在回頭看，也許 Adobe 該慶幸——如果它 2022 年真的花 200 億買了 Figma，2026 年它要面對的就不只是股價下跌，而是一筆 200 億美元的資產被 AI 系統性吞噬。

### SaaSpocalypse：2 兆美元的恐慌

Figma 的困境不是孤例。2026 年 1 月到 2 月間，[整個軟體產業蒸發了約 2 兆美元市值](https://www.bain.com/insights/why-saas-stocks-have-dropped-and-what-it-signals-for-softwares-next-chapter/)。Atlassian 下跌 35%，Salesforce 下跌 28%。Bloomberg 發明了一個詞叫「SaaSpocalypse」——SaaS 末日。

觸發這場恐慌的導火線，是 Anthropic 在 2 月初發表了 Claude Cowork，展示 AI Agent 能自動完成大量原本需要人類使用 SaaS 工具才能做的工作。市場突然意識到一個問題：如果 AI Agent 能直接幫你做事，你還需要買那麼多軟體座位嗎？

當 per-seat 定價遇上 AI——原本需要 500 個座位的客戶，現在也許只需要 450 個。聽起來只是 10% 的差異，但對靠座位數計算營收的 SaaS 公司來說，這是個存在性威脅。

---

## 多方觀點

### 樂觀派：「這是世界上最不合邏輯的事」

NVIDIA 的黃仁勳在 2 月一場思科 AI 活動上被問到「AI 是否會殺死軟體公司」，他的回答很直接：「你能看出來，有一大批軟體公司股價承受巨大壓力。這是世界上最不合邏輯的事情，時間會證明自己。」

老黃的邏輯不難理解——AI 需要更多軟體來運行，不是更少。AI Agent 不會在虛空中運作，它需要呼叫 API、操作介面、處理資料，這些全都要軟體。如果 AI 真的讓所有人都能做設計、寫程式，那軟體的使用量應該是暴增的，怎麼軟體公司反而要倒？

Figma CEO Dylan Field 也保持著創業者的樂觀。他在 2 月受訪時說：「我認為波動從長遠來看可能對公司是好事。」他還提出了一個有意思的框架——AI 可以「降低地板，但拉高天花板」（lower the floor, but raise the ceiling），意思是 AI 讓更多人能做設計（降低門檻），但專業設計的深度和價值反而會提升。

Morgan Stanley 的軟體研究主管 Elizabeth Porter 對 Figma 給出了相對正面的評估，她認為 Figma 是產品設計軟體的「行業標準」，即時協作平台是其競爭優勢。JP Morgan 策略師也認為市場目前定價的是「不太可能在短期內實現的最壞 AI 衝擊情境」。Morgan Stanley 另一位主管 Katy Huberty 則直接稱這波賣壓是「情緒驅動的錯位」，不反映公司的真實業務狀況。

這些樂觀派有一個共同的底層邏輯：AI 擴大了整塊餅，即使切法改變，每個人分到的都不會少。問題是，歷史上「餅變大了所以每個人都受益」的許諾，很少會完整兌現。

### 悲觀派：免費是最狠的武器

但另一邊的聲音同樣有理有據。[Bain & Company 的分析](https://www.bain.com/insights/why-saas-stocks-have-dropped-and-what-it-signals-for-softwares-next-chapter/)指出，「AI 日益增長的能力能複製核心功能，並隨著時間侵蝕用戶基礎」——這不是恐慌，是正在發生的事。

以 Figma 為例，Google Stitch 和 Figma 的核心功能高度重疊——都是做 UI/UX 設計。但一個免費，一個每人每月最高 90 美元。一個背靠數億 Workspace 用戶的分發能力，一個要靠口碑和社群慢慢長。這不是技術之戰，是經濟結構之戰。

自由設計師的報價也在崩潰。以前一個 Landing Page 設計收費 2,000 到 5,000 美元是常態。現在用 Stitch 二十分鐘就能生成一個 6 分品質的初稿——對很多小團隊和新創公司來說，6 分就夠用了。

### 設計師的第一線：接受、反抗、然後適應

[99designs 的調查](https://sleek.design/blog/vibe-design-ai-revolution-impact)顯示，52% 的自由設計師在 2024 年就已經在使用生成式 AI 工具，比 2023 年的 39% 大幅增長。Adobe 2026 年的創意趨勢報告進一步指出，58% 的專業設計師每週至少使用一次 AI 生成工具。2025 年的 State of AI in Design Report 則顯示 89% 的設計師認為 AI 在某種程度上改善了他們的工作流程。

但接受工具和接受被取代是兩回事。一個有趣的現象是：設計師在擁抱 AI 的同時，也在刻意追求「不完美」的美學——故意打破 AI 無法輕易複製的規則，用手工感和瑕疵感來彰顯「這是人做的」。Canva 的 2026 設計趨勢報告甚至把「Imperfect by Design」列為年度趨勢之一。這是一種創意上的反抗，也是一種身份焦慮的投射。

有設計師在社群裡半開玩笑說：「以前我的工作是把客戶的破想法變成好設計，現在我的工作是把 AI 的好設計變成客戶要的破設計。」笑話歸笑話，但它精準地捕捉到了設計師正在經歷的身份危機——當 AI 在技術執行層面已經「夠好」的時候，設計師的價值到底在哪裡？

2026 年的設計師正在從「製作者」轉型為「策展人」——不再是自己一筆一畫地畫，而是指導 AI 生成、然後挑選和精修。這聽起來很美好，但殘酷的現實是：市場需要的「策展人」數量，遠少於「製作者」。就像攝影從底片時代進入數位時代，暗房技術員消失了，但攝影師沒有消失——只是市場需要的攝影師數量，再也回不到從前。

### 我的看法：真正的威脅不是技術，是分發

以我的經驗來看，Google Stitch 在技術上並沒有碾壓 Figma。它生成的設計大概是 6 分水準，專業設計師一眼就能看出粗糙的地方——缺乏視覺層次感、使用者旅程設計、情感共鳴這些 AI 目前做不好的深層能力。

但問題是：對大量使用場景來說，6 分就夠了。

一個正在做 MVP 的創業者、一個需要快速出原型的產品經理、一個想改改內部工具介面的開發者——他們不需要 9 分的設計，他們需要「今天下午就能用」的設計。Stitch 滿足的是這個需求。

而 Google 真正可怕的地方不在於 Stitch 有多好，而在於它能把 Stitch 放在哪裡。Gmail、Google Docs、Google Drive——數億企業用戶已經在 Google 的生態系統裡。Stitch 只要一鍵整合進 Workspace，就能觸達 Figma 夢寐以求但永遠拿不到的用戶群。

這個劇本我們看過太多次了。Google Docs 沒有 Microsoft Word 強大，但它免費、在瀏覽器裡就能用、和 Gmail 無縫整合——然後它就吃掉了一大塊市場。Google Maps 沒有一開始就比 MapQuest 好多少，但它免費、內建在 Android 裡——然後 MapQuest 就消失了。

免費，加上分發，就是核武。

---

## 產業衝擊

### 第一層：誰直接受傷？

最直接的受害者是自由設計師和初級 UI/UX 設計師。根據 [NxCode 的分析](https://www.nxcode.io/resources/news/google-stitch-vs-figma-ai-design-comparison-2026)，Stitch 特別適合幾類人：獨立設計師和自由工作者、正在做 MVP 的創業者、需要快速 Mockup 的開發者、預算有限的小團隊。這些人是 Figma 免費方案和低價方案的核心用戶——也是設計師接案的主要客群。

當這些客戶發現他們可以免費自己做「夠用」的設計，他們為什麼還要花 2,000 美元請設計師？AI 做完了設計的前 80%，設計師只被需要來做剩下的 20%——但客戶只願意為 20% 的工作付 20% 的價格嗎？通常不會，他們會想：「這 20% 我自己調一調也行。」

受益者則是有整合能力的平台公司。Google 不只有 Stitch——它有 Gemini、有 Cloud、有 Workspace、有 Android。Stitch 是棋盤上的一顆棋子，不是全部。真正的遊戲是讓企業客戶留在 Google 的生態系統裡，從設計到程式碼到部署全部在 Google 的管道上完成。

### 第二層：SaaS 定價模型的崩潰

Figma 的定價是典型的 per-seat 模式——每個用戶每月付費。這個模式建立在一個假設上：設計是需要「人」來做的事，所以你有多少設計師，就買多少座位。

但當 AI Agent 能做設計的時候，這個假設就崩了。一個十人的設計團隊，如果其中五個人的日常工作可以被 AI 處理，公司就只需要買五個座位。Figma 也意識到了這個問題——它從 2026 年 3 月 11 日開始推出 AI credits 的使用量計價模式，試圖從 per-seat 轉向 per-usage。

但這個轉型本身就充滿矛盾。如果 AI 讓設計效率提升了 5 倍，客戶用量降低了，使用量計價的收入也會下降。而且你還得和 Google 的「免費」競爭。

Figma 2026 年的營收指引是 13.66-13.74 億美元，看起來很穩健。但市場擔心的不是今年，是三年後。當 AI 設計工具的品質從 6 分進步到 8 分、9 分，Figma 的護城河——即時協作、設計系統管理、2000+ 外掛生態——還夠深嗎？

更令人擔憂的是整個 SaaS 產業的骨牌效應。Atlassian 年初至今下跌 35%，Salesforce 下跌 28%——它們的核心工作流（任務追蹤、數據輸入、客戶記錄）恰恰是 AI Agent 最擅長自動化的。[Forrester 的分析](https://www.forrester.com/blogs/saas-as-we-know-it-is-dead-how-to-survive-the-saas-pocalypse/)甚至直接宣告「SaaS as we know it is dead」。這不是某一家公司的問題，這是整個商業模式的問題。

Figma 並非坐以待斃。它在 2 月和 Anthropic 合作推出了 [「Code to Canvas」](https://www.figma.com/blog/introducing-claude-code-to-figma/)功能，讓用 Claude Code 生成的程式碼可以直接匯入 Figma 變成可編輯的設計稿。這是一步聰明的棋——把自己定位在 AI 工作流的「精修端」而非「生成端」。用 AI 生成初稿，用 Figma 來修。但這是一條越走越窄的路。

### 第三層：設計與程式碼的界線正在消融

Stitch 的 MCP 整合和 DESIGN.md 格式指向一個更深層的變化：設計和程式碼之間的邊界正在消失。

以前的流程是：設計師在 Figma 畫好設計 → 交給開發者 → 開發者照著設計寫程式碼 → 來回修改直到一致。這個流程可能要花三到五天。

現在的流程可以是：用 Stitch 語音描述想要什麼 → AI 生成設計和程式碼 → 匯出 React 程式碼 → 直接部署。二十分鐘搞定。

DESIGN.md 是一個特別值得注意的發明。它用自然語言定義設計規範——色彩、字體、間距、元件風格——然後可以被任何 AI 工具讀取和遵循。這意味著設計規範不再鎖在 Figma 的設計系統裡，而是變成了一個可攜式的文字檔案，能跨工具、跨平台使用。

對開發者來說，這是好事——AI 可以直接讀 DESIGN.md 來生成符合規範的程式碼，不需要再去 Figma 裡面查。但對 Figma 來說，這是把設計資產從自己的平台裡抽離出來。

### 第四層：連鎖反應

如果 Vibe Design 的邏輯成立——用自然語言就能做設計——那下一個被吃掉的會是什麼？

Vibe Coding 吃掉了低階程式設計。Vibe Design 正在吃 UI/UX 設計。按照這個路徑，Vibe Marketing（用語音描述想要什麼行銷素材）、Vibe Presentation（用語音做簡報）、Vibe Video（用語音做影片）全都在射程內。每一個「用嘴巴說就能做」的領域，都對應著一個現有的 SaaS 工具和一群專業工作者。

Canva 在做 Vibe Marketing。Gamma 在做 Vibe Presentation。Runway 和 Pika 在做 Vibe Video。這不是未來，這是正在發生的事。

整個 SaaS 產業正在面臨一個根本性的問題：當 AI 能把「做事」的成本壓到接近零，按座位收費的商業模式就失去了根基。未來能存活的可能只有兩種 SaaS：一是擁有不可替代的資料和網路效應的平台（比如 Slack 的對話歷史、Notion 的知識庫），二是成功轉型為 AI 基礎設施的工具（比如提供 Agent 呼叫的 API 而非人類操作的介面）。

---

## 未來展望

### 短期（3-6 個月）：Figma 的反擊戰

幾乎可以確定，Figma 會加速 AI 功能的投入。它已經有了 Figma Make（AI 設計生成，週活躍用戶季增 70%）和 Code to Canvas（與 Anthropic 合作）。接下來 Figma 很可能會推出自己的語音設計功能、更強的 AI Agent、以及更積極的 AI credits 定價策略。

同時，Google Stitch 會持續迭代。目前它還在 Google Labs 的實驗階段，沒有 SLA 也沒有企業級支援。但一旦 Google 決定把 Stitch 正式整合進 Workspace——那才是 Figma 真正的噩夢。

### 中期（6-18 個月）：設計工具的兩極化

我認為最可能的發展路徑是設計工具市場的兩極化：

**情境一：專業端和消費端徹底分裂。** Stitch 類的工具吃掉「從 0 到 1」的市場——MVP、原型、快速迭代。Figma 退守「從 1 到 100」的市場——生產級設計、大型設計系統、企業級協作。兩者共存，但 Figma 的可觸及市場（TAM）大幅縮水。

**情境二：混合工作流成為常態。** 設計師的日常變成：用 Stitch 快速探索十個方向 → 挑出最好的兩三個 → 匯入 Figma 精修 → 用 Dev Mode 交給開發者。Figma 不再是設計的起點，而是終點站。

**情境三：Google 認真起來。** 如果 Google 決定把 Stitch 從實驗項目升級為正式產品，加入即時協作、設計系統管理、企業級權限——那 Figma 就不是面對一個玩具，而是面對一個有無限資源的巨頭在自己的核心領域發起全面進攻。歷史上，這種局面很少有好結局。

### 長期（3-5 年）：設計師的身份重塑

如果把時間軸拉長，Vibe Design 最深遠的影響不在工具市場，而在職業定義本身。

設計師的角色正在從「製作者」轉型為「創意總監」。不是自己畫，而是指導 AI 畫。不是調像素，而是定方向。不是執行，而是判斷。

這聽起來是升級，但它意味著市場需要的設計師數量會大幅減少。一個資深設計師指揮五個 AI Agent，就能做到以前十個設計師的產出。審美、品味、判斷力——這些「軟」能力會變得更值錢，但它們恰恰是最難教、最難量化、也最依賴人生經歷累積的東西。

### 給不同角色的建議

**如果你是設計師：** 現在就開始學習 AI 設計工具，但不是為了和 AI 比速度——你永遠比不過。把精力放在 AI 做不好的事情上：使用者研究、資訊架構、品牌策略、系統性設計思維。你要成為那個決定「AI 該做什麼」的人，而不是「AI 做的事情」。同時學一點程式基礎不會吃虧——設計和程式碼的邊界消失對雙棲人才是利多。

**如果你是創業者或產品經理：** 用 Vibe Design 工具來加速早期產品探索。二十分鐘出一個 6 分的原型，然後拿去做用戶測試，比花三天做一個 9 分的原型更有效率。但不要因此省掉設計師——AI 生成的介面能通過「看起來不錯」的測試，但往往通不過「用起來順手」的測試。在找到 Product-Market Fit 之前用 AI，找到之後請專業設計師。

**如果你在 SaaS 公司工作：** 認真思考你的產品在 AI 時代的護城河是什麼。如果答案只是「好用的介面」和「功能齊全」，那你很危險——AI 正在把這些東西商品化。真正的護城河是資料（用戶累積的內容和歷史）、網路效應（協作帶來的鎖定效應）、和工作流整合（成為企業流程中不可拆除的一環）。

---

回到最初的問題：當設計只需要一張嘴，設計工具的 570 億美元市值還能撐多久？

答案可能不在技術，而在一個更根本的經濟學問題——當 AI 把「做事」的邊際成本壓到接近零，價值不會消失，但會劇烈重新分配。從工具廠商流向平台巨頭，從執行者流向決策者，從座位數流向使用量。

Figma 不一定會死，但它必須接受一個新現實：它統治的那個世界——每個設計師都需要打開一個設計工具、手動拖拽每一個像素的世界——正在快速消失。能適應這個變化的公司會活下來，但它們會長得和今天很不一樣。

而對我們這些在科技業裡浮沉的人來說，Vibe Design 的故事其實只是一個更大故事的最新章節：AI 不是來取代你的工具的，它是來取代你「使用工具」這個動作的。當這個動作本身不再有價值，你的價值在哪裡？

這個問題，值得每個人認真想想。

---

## 延伸閱讀

- [Figma stock drops 12% after Google releases vibe design product Stitch — CNBC](https://www.cnbc.com/2026/03/19/figma-stock-drops-11percent-after-google-releases-vibe-design-product-stitch.html)：事件核心報導，包含股價數據和分析師觀點
- [Google Stitch vs Figma 2026: Will AI Design Replace Figma? — NxCode](https://www.nxcode.io/resources/news/google-stitch-vs-figma-ai-design-comparison-2026)：最詳細的功能對比分析，附帶使用場景建議
- [Why SaaS Stocks Have Dropped — Bain & Company](https://www.bain.com/insights/why-saas-stocks-have-dropped-and-what-it-signals-for-softwares-next-chapter/)：管理顧問視角的 SaaS 產業衝擊分析
- [Vibe Design: AI Revolution in Design 2026 — Sleek](https://sleek.design/blog/vibe-design-ai-revolution-impact)：設計師視角的 Vibe Design 趨勢深度報告，含調查數據
- [Vibe coding is passé. Karpathy has a new name for the future of software. — The New Stack](https://thenewstack.io/vibe-coding-is-passe/)：從 Vibe Coding 到 Agentic Engineering 的演進脈絡
- [Figma partners with Anthropic to turn AI-generated code into editable designs — CNBC](https://www.cnbc.com/2026/02/17/figma-anthropic-ai-code-designs.html)：Figma 的 AI 反擊策略：Code to Canvas
- [Adobe's Failed Acquisition of Figma Has Cost the Company Over $38 Billion — Yahoo Finance](https://finance.yahoo.com/news/adobe-failed-acquisition-figma-cost-151035766.html)：Adobe 錯失 Figma 的歷史脈絡和財務影響
- [Google Stitch: The Free AI Design Tool Killing Figma — The AI Corner](https://www.the-ai-corner.com/p/google-stitch-ai-design-tool-guide-2026)：Google Stitch 的完整功能指南和工作流建議
- [AI fears pummel software stocks: SaaS apocalypse? — CNBC](https://www.cnbc.com/2026/02/06/ai-anthropic-tools-saas-software-stocks-selloff.html)：SaaSpocalypse 的全景報導，含黃仁勳和各方觀點
