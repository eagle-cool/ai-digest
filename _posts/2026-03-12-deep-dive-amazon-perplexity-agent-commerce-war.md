---
title: "當 AI 幫你買東西：Amazon 訴 Perplexity 背後的電商存亡之戰"
date: 2026-03-12
description: "一場看似簡單的帳號授權糾紛，揭開了 AI Agent 時代電商平台最深層的恐懼：當消費者不再需要打開你的 App，你的廣告帝國還能撐多久？Amazon 對 Perplexity 的禁令，是平台主權的最後防線，還是螳臂當車？"
tags: [deep-dive, agents, ai-industry, ai-tools]
---

## 引言

想像一個場景：你躺在沙發上，跟 AI 說「幫我買一條跟上次差不多的 USB-C 充電線，要最便宜的那種」。AI 自動登入你的 Amazon 帳號，搜尋商品、比較價格、確認配送時間，然後下單。整個過程你連 Amazon 的頁面都沒看過一眼。

聽起來很方便，對吧？但對 Amazon 來說，這是一場噩夢。因為在這個場景裡，你沒有看到那條充電線旁邊的「Sponsored」推薦，沒有看到結帳前的「你可能也喜歡」，沒有被任何一個精心設計的行銷漏斗捕捉到。你的整個消費決策過程——Amazon 過去二十年花了數十億美元打造的護城河——在 AI Agent 面前，變得毫無意義。

2026 年 3 月 10 日，美國加州北區聯邦法院法官 Maxine Chesney 發出了一紙初步禁令，禁止 Perplexity AI 的 Comet 瀏覽器透過 AI Agent 存取 Amazon 的帳戶系統、執行購物操作。這是全球第一起法院正式裁決「AI 代理購物」是否合法的案件。表面上看，這是一場關於帳號授權的技術糾紛。但往深了看，這是一場關於**誰有權控制消費決策路徑**的存亡之戰。

這篇報導的起點是[知產力的法律分析](https://www.36kr.com/p/3719289614037512)，但故事遠不止於此。當 AI Agent 開始幫人類購物，整個電商產業——從流量入口到廣告模式到平台經濟——都面臨二十年來最根本的結構性衝擊。

---

## 事件全貌

### 一隻「偽裝成人類」的 AI

事件的主角是 Perplexity AI 的 [Comet 瀏覽器](https://www.perplexity.ai/comet)。這不是一個普通的瀏覽器——它內建了 AI Agent 功能，能在使用者授權後，自動完成多步驟的網路任務：搜尋商品、比較價格、加入購物車、完成下單。Pro 用戶的 Comet Agent 預設使用 Claude Sonnet 4.6，Max 用戶則用 Opus 4.6。

技術上，Comet 的做法頗具爭議。使用者把 Amazon 帳號密碼交給 Comet，AI Agent 在背後模擬普通瀏覽器的行為——它不會標識自己是自動化程式，而是偽裝成 Chrome 瀏覽器進行操作。在 Amazon 的伺服器看來，這跟一個真人在瀏覽網頁沒有區別。

Amazon 認為這是刻意欺騙。[根據法院文件](https://www.theregister.com/2026/03/11/perplexity_comet_amazon_ban/)，Comet 不僅存取了用戶的密碼保護帳戶，還把「用戶的私人 Amazon 帳戶資訊傳送到 Perplexity 的伺服器」。這不只是幫人購物——這是在沒有平台許可的情況下，把用戶的消費數據吸走。

更讓 Amazon 坐不住的是安全風險。Amazon 在訴訟中指控，Comet 要求用戶將登入憑證暴露給一個「有已知漏洞的瀏覽器」，這對消費者的帳戶安全構成直接威脅。當你把 Amazon 帳密交給第三方——而這個第三方還會把你的帳戶資料傳回自家伺服器——你的購物歷史、信用卡資訊、配送地址，全都暴露在另一條資料管線中。

### 從警告到訴訟：18 個月的拉鋸

這場衝突的時間線比多數人想像的要長得多：

- **2024 年 11 月**：Perplexity 為美國付費用戶推出 AI 購物 Agent。Amazon 隨即發出第一封停止函。前後至少發了五次警告
- **2025 年 8 月**：Amazon 實施技術封鎖，阻擋 Comet 的存取。結果 Perplexity 在 **24 小時內**釋出軟體更新，繞過了封鎖
- **2025 年 11 月**：Amazon 正式提起訴訟
- **2026 年 3 月 10 日**：法院發出初步禁令，Perplexity 隨即提出上訴

24 小時內繞過技術封鎖這個細節，在法官眼中顯然不是加分項。法官 Chesney [在裁定中寫道](https://winbuzzer.com/2026/03/11/federal-judge-halts-perplexity-comet-ai-shopping-agent-amazon-xcxwbn/)，Amazon 提供了「強有力的證據」（strong evidence），證明 Perplexity 的行為可能構成違反聯邦《電腦詐欺與濫用法》（CFAA）。

### 法律核心：用戶授權 ≠ 平台授權

這個案子最精妙的地方在於法官畫出的那條線。

法官承認，Comet 確實取得了用戶的授權——使用者是自願把帳密交給 AI 的。但法官做了一個關鍵區分：**用戶授權第三方使用自己的帳號，不等於平台授權該第三方存取自己的系統**。

用白話說：你可以把家裡鑰匙給朋友，但大樓管委會有權拒絕你朋友進入大樓。

這個區分在法律上意義重大。過去的 [hiQ v. LinkedIn 案](https://en.wikipedia.org/wiki/HiQ_Labs_v._LinkedIn)（2022 年第九巡迴法院判決）確立了一個原則：爬取公開數據不違反 CFAA。在那個案子裡，法院認為公開的 LinkedIn 個人資料不需要授權就能存取，所以 hiQ 的爬蟲並沒有「未經授權」。但 Amazon 的案子完全不一樣——Comet 存取的是**密碼保護的帳戶**，而且是在平台明確拒絕之後繼續存取。這兩個條件加在一起，幾乎完美地命中了 CFAA「未經授權存取電腦系統」的核心構成要件。

值得注意的是，法院沒有完全否定「用戶有權委託 AI 操作帳號」的概念。法官認定的是：在平台已經明確拒絕的情況下，Perplexity 繼續存取構成違法。這留下了一個微妙的空間——如果未來有一個平台沒有明確拒絕 AI Agent 存取，或者甚至在服務條款中允許了，那法律判斷可能完全不同。

---

## 脈絡

### 電商平台二十年的「流量霸權」

要理解這場戰爭的深度，得先理解電商平台過去二十年建立的商業邏輯。

從 Amazon 到淘寶，電商平台的核心護城河從來不只是「有東西賣」。它們的真正武器是**消費決策路徑的控制權**。你打開 App → 搜尋 → 看到推薦 → 看到廣告 → 比價 → 下單。這整條路徑上的每一個節點，都是平台的變現機會。

Amazon 2025 年的廣告營收達到 [563 億美元](https://www.emarketer.com/content/amazon-fights-back-ai-shopping-agents-threaten-ad-revenues)，光第三季就有 177 億美元，年增 24%。這筆錢主要來自搜尋結果中的 Sponsored Products、推薦欄位中的 Sponsored Brands、以及各種展示型廣告。換句話說，Amazon 靠的不只是賣東西的抽成——它靠的是**你在平台上逛的每一秒鐘**。

而 AI Agent 做的事情，恰恰是把這條路徑從中間砍斷。

### 從搜尋引擎到 AI Agent：流量入口的第三次遷移

回顧科技史，電商流量入口經歷過兩次重大遷移：

**第一次**是從線下到線上。實體店的客流量被電商平台吸走，商場變成試衣間。

**第二次**是搜尋引擎和社群媒體。Google Shopping、Instagram Shopping、TikTok 電商——這些平台把部分流量從 Amazon 搶了過來，但最終交易還是在電商平台上完成。Amazon 的護城河受到侵蝕，但沒有被攻破。

**第三次**就是現在——AI Agent。不同於搜尋引擎只是幫你找到商品，AI Agent 是**直接幫你完成整個交易**。從需求理解、商品篩選、價格判斷到下單付款，一條龍服務。平台從「消費決策的中心」變成了「交易執行的基礎設施」。

這個轉變有多大？用 Gartner 副總裁 Andrew Frank 的話說，這影響的是[「任何想要和客戶建立關係的人」](https://www.marketingbrew.com/stories/2026/01/12/perplexity-amazon-lawsuit-agentic-AI-retail-media)。

### 歷史類比：出版業的前車之鑑

這不是第一次「中間人」被技術淘汰。最明顯的類比是新聞出版業。

Google 搜尋和後來的 AI 生成摘要，系統性地抽空了新聞網站的流量。讀者在 Google 上就能得到答案，不再需要點進原始網站。出版商的廣告收入因此崩塌。

Andrew Frank [警告](https://www.marketingbrew.com/stories/2026/01/12/perplexity-amazon-lawsuit-agentic-AI-retail-media)，電商平台面臨的是「出版業和零售業的持續邊緣化」。而且電商的處境可能更糟——至少新聞出版商後來還能透過授權協議向 Google 收費，但當 AI Agent 直接繞過平台完成交易，平台連收費的立足點都沒有。

還有一個更早期的歷史參照：早期電子商務本身的信任建立。[HBR 文章](https://hbr.org/2026/02/how-brands-can-adapt-when-ai-agents-do-the-shopping)指出了一個有啟發性的類比——消費者當初也不信任在網路上輸入信用卡號碼。最終是 SSL 加密、PCI 標準和詐欺保護機制這些「信任基礎設施」解決了問題。Agent 購物同樣需要等價的信任基礎設施——HBR 稱之為「信任層」（trust layer）——才能真正實現大規模普及。

### 不只是美國的問題

這場戰爭目前以美國法院為主戰場，但影響是全球性的。在中國，阿里巴巴和京東面臨類似的挑戰——OpenClaw 的爆紅已經讓各大平台開始思考 AI Agent 的入口問題。騰訊在一週內推出了全套「龍虾」產品矩陣，本質上就是在搶佔 Agent 生態的入口。

在歐洲，《數位市場法》（DMA）要求大型平台開放互操作性，這在理論上可能迫使平台允許第三方 AI Agent 存取。如果歐盟監管機構認定 Amazon 封鎖 AI Agent 構成反競爭行為，法律計算可能完全反轉——平台不是有權封鎖，而是有義務開放。

這也是為什麼 Google 選擇了「協定路線」而非「破門路線」。Google 在 2026 年 1 月 NRF 大會上推出 UCP 時，拉了一整排零售巨頭站台——[Shopify、Etsy、Wayfair、Target、Walmart](https://techcrunch.com/2026/01/11/google-announces-a-new-protocol-to-facilitate-commerce-using-ai-agents/)。Google 的策略很明確：與其像 Perplexity 那樣硬闖，不如建立一個平台願意加入的開放標準。這是一條更慢但更穩的路。

---

## 多方觀點

### Amazon：「我們在保護消費者」

Amazon 的官方立場是消費者保護。CEO Andy Jassy [表示](https://www.emarketer.com/content/amazon-fights-back-ai-shopping-agents-threaten-ad-revenues)：「（AI Agent 購物）沒有個人化推薦、沒有購物歷史、配送時間常常是錯的、價格也經常不對。」

Amazon 還把自己類比為餐廳和外送平台的關係——[就像餐廳有權選擇跟哪個外送平台合作](https://www.pymnts.com/amazon/2026/amazon-secures-court-order-against-perplexity-ai-shopping-agent/)，電商平台也應該有權決定哪些 AI Agent 能存取自己的系統。

但這個說法有個破綻：Amazon 自己也在開發 AI Agent。它的「Buy For Me」功能和 Rufus 助手都是 AI 購物工具——只是它們是 Amazon 自己的。換句話說，Amazon 不是反對 AI Agent 購物，**它反對的是不受自己控制的 AI Agent 購物**。

### Perplexity：「這是使用者的權利」

Perplexity 的回應同樣充滿火藥味。公司發言人[對 The Register 表示](https://www.theregister.com/2026/03/11/perplexity_comet_amazon_ban/)：「Perplexity 會繼續為網路使用者選擇任何 AI 的權利而戰。」

更早之前，Perplexity 直接把 Amazon 的法律行動稱為[「霸凌策略」](https://www.emarketer.com/content/amazon-fights-back-ai-shopping-agents-threaten-ad-revenues)（bully tactic），並辯稱 Agent 購物實際上會為 Amazon 帶來**更多**交易量。

Perplexity 的論點核心是「用戶主權」：如果我是 Amazon 帳號的持有人，我授權 AI 幫我操作我自己的帳號，這跟我請朋友幫我下單有什麼不同？平台有什麼資格告訴我，只能用它核准的方式使用我自己的帳號？

這個論點直覺上很有力，但法院顯然不買帳。原因可能是技術層面的——Comet 偽裝成 Chrome、繞過技術封鎖、把帳戶資料傳回自己的伺服器——這些做法超出了「用戶委託」的合理範圍。

### 產業分析師：「存亡威脅」

VML 的 Tyler Murray [把 AI Agent 購物稱為](https://www.marketingbrew.com/stories/2026/01/12/perplexity-amazon-lawsuit-agentic-AI-retail-media)零售媒體的「存亡威脅」（existential threat）。這不是誇張——如果消費者不再看到廣告，零售媒體的整個商業模式就瓦解了。

McKinsey [預測](https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-agentic-commerce-opportunity-how-ai-agents-are-ushering-in-a-new-era-for-consumers-and-merchants)，agentic commerce 到 2030 年可能在美國創造 1 兆美元的零售營收。Morgan Stanley 分析師預期，屆時將有近 50% 的美國消費者使用 AI Agent 購物，潛在增加 1150 億美元的電商支出。

但 Forrester 的 Sucharita Kodali [提出一個冷水觀點](https://www.modernretail.co/technology/why-the-ai-shopping-agent-wars-will-heat-up-in-2026/)：商品目錄還沒準備好。大多數零售商的產品資料是為搜尋引擎優化的，不是為 AI Agent 設計的。AI Agent 需要結構化的、機器可讀的產品數據（材質、尺寸規格、溫度範圍），而不是給人看的行銷文案。基礎建設還沒到位，大規模取代為時尚早。

### 消費者的態度：想要但不信任

PwC 的 [2025 年消費者購物未來調查](https://hbr.org/2026/02/how-brands-can-adapt-when-ai-agents-do-the-shopping)顯示，**64% 的消費者至少需要一項安全保障**（如退款保證）才願意讓 AI Agent 代為購買。即使是數位原生的 Gen Z 和 Gen Alpha 也不例外。另一項調查顯示，只有三分之一的受訪者願意透過 AI Agent 完成付款。

消費者想要便利，但不信任代理。這是一個經典的「先有雞還是先有蛋」問題——信任需要好的體驗來建立，但好的體驗需要平台開放存取才能實現。

而且信任問題不只是消費者端的。品牌方同樣焦慮。當 AI Agent 代替消費者做決策，品牌怎麼確保自己的產品不被 Agent 忽略？如果 Agent 推薦了錯誤的尺寸、虛構了產品功能、或者展示了過時的價格，[HBR 將這些列為五大風險](https://hbr.org/2026/02/how-brands-can-adapt-when-ai-agents-do-the-shopping)——產品誤解、未授權操作、數據曝露、品牌錯誤呈現、以及自動化失敗後的客訴處理困難。每一個都足以永久損害品牌與消費者的關係。

### 我的看法

以我的觀察，Amazon 這次打官司，與其說是在保護消費者，不如說是在保護自己的**廣告帝國**。Perplexity 的代言人[說得很直白](https://www.marketingbrew.com/stories/2026/01/12/perplexity-amazon-lawsuit-agentic-AI-retail-media)：「AI Agent 沒有眼球可以看到 Amazon 鋪天蓋地的廣告。」這句話一針見血。

但 Perplexity 的做法確實也有問題。偽裝成 Chrome、24 小時內繞過技術封鎖、把用戶帳密傳回自己的伺服器——不管你的理念多正確，這些做法在法律和安全層面都說不過去。你可以為了打破壟斷而戰，但你不能用偷雞摸狗的方式打這場仗。

真正有趣的是，兩邊的論點都有道理，這才是這場戰爭複雜的地方。平台有沒有權控制自己的系統？有。用戶有沒有權選擇用什麼工具操作自己的帳號？也有。當這兩個權利碰撞的時候，答案不是非黑即白的。

---

## 產業衝擊

### 第一層：廣告產業的地震

AI Agent 購物對電商平台最直接的威脅，不是交易量的流失，而是**廣告曝光的消失**。

想想看整個流程：當人類在 Amazon 上購物，他們搜尋、瀏覽、點擊——每一個動作都是廣告曝光的機會。Sponsored Products 出現在搜尋結果中，Sponsored Brands 展示在分類頁面，Display Ads 散布在各處。這些廣告位不只是 Amazon 的收入來源，也是品牌方觸達消費者的唯一管道。

當 AI Agent 接管購物流程，它直接跳到「最符合用戶需求的商品」，完全略過搜尋結果和推薦欄位。[如 Marketing Brew 所分析的](https://www.marketingbrew.com/stories/2026/01/12/perplexity-amazon-lawsuit-agentic-AI-retail-media)，AI Agent 把多步驟的購物過程（發現、比較、購買）壓縮成一個動作，跳過了驅動 Amazon 利潤的贊助結果和推薦系統。

Amazon 563 億美元的廣告營收中，有多少會因此蒸發？沒有人知道確切數字，但從 Amazon 反應的激烈程度來看，這個數字讓他們晚上睡不著。

### 第二層：商業模式的重新定義

如果 AI Agent 購物成為主流，電商平台的商業模式需要從根本上重新設計。

**現有模式**：平台靠「流量 × 轉化率 × 客單價」賺錢。流量來自搜尋引擎導流和 App 開啟，轉化率靠推薦算法和廣告位優化，客單價靠交叉銷售和促銷。

**Agent 模式下**：使用者不再「逛」平台，AI Agent 直接去拿最佳匹配。平台變成了一個倉庫和物流系統——有貨、能送，但使用者看不到你的品牌，你也沒機會推銷別的東西給他。

這已經在發生了。Amazon 自己的「Buy For Me」功能本質上就是在做一樣的事——只是它是 Amazon 自己的 Agent，能確保流量和數據留在自己的生態系中。

那平台未來靠什麼賺錢？原始文章提出了幾個方向：API 存取費、Agent 交易佣金、數據服務收費。Google 和 OpenAI 已經在用另一種方式嘗試——建立開放的 Agent 商務協定，讓平台在可控的框架下與 AI Agent 合作。

有一個數據值得特別關注：目前大約 [2% 的 ChatGPT 查詢是購物相關的](https://www.modernretail.co/technology/why-the-ai-shopping-agent-wars-will-heat-up-in-2026/)，以 ChatGPT 8 億週活躍用戶計算，這已經是每天約 5000 萬次購物查詢。這個比例只會往上走。而且別忘了，OpenAI 在 2026 年 2 月才剛上線「Buy it in ChatGPT」功能——[Etsy 商家已經接入，超過 100 萬 Shopify 商家即將跟進](https://openai.com/index/buy-it-in-chatgpt/)，PayPal 預計今年將帶來數千萬小型商家。當 Agent 購物從「能用」變成「好用」，那 2% 會變成 20%，整個電商的流量地圖就要重畫了。

有趣的是，OpenAI 最近又[傳出縮減了 ChatGPT 的 instant checkout 功能](https://cxotoday.com/ai/agentic-commerce-in-doldrums-openai-scales-back-shopping-plans-for-chatgpt/)。消息一出，旅遊和外送公司的股價立刻反彈——這側面證明了市場有多認真看待 Agent 購物對現有商業模式的威脅。連 OpenAI 自己都在試探這條路的邊界在哪裡。

### 第三層：開發者生態的劇變

對開發者來說，這場戰爭催生了一個全新的技術棧。

**Google 的 Universal Commerce Protocol（UCP）**在 2026 年 1 月的 NRF 大會上正式發布，由 Google CEO Sundar Pichai 親自宣布。[這是一個開源標準](https://developers.googleblog.com/under-the-hood-universal-commerce-protocol-ucp/)，讓 AI Agent 能透過標準化介面與電商系統互動——從商品搜尋、價格查詢到完成交易。Shopify、Etsy、Wayfair、Target、Walmart 都是共同開發者，超過 20 家合作夥伴已加入。

**OpenAI 的 Agentic Commerce Protocol（ACP）**則是與 Stripe 共同開發的開放框架，[支撐了「Buy it in ChatGPT」功能](https://openai.com/index/buy-it-in-chatgpt/)。2026 年 2 月上線時，已有 Etsy 商家和超過 100 萬 Shopify 商家接入，PayPal 預計今年將帶來數千萬小型商家上線。

這意味著開發者現在需要學習一整套新的技術——UCP、ACP、Agent2Agent（A2A）協定、Model Context Protocol（MCP）——來讓自己的電商系統對 AI Agent 「可見」和「可交互」。[Harvard Business Review 的分析指出](https://hbr.org/2026/02/how-brands-can-adapt-when-ai-agents-do-the-shopping)，品牌的產品資料必須從「為人類設計」轉向「為 Agent 設計」——機器可讀的結構化數據取代感性的行銷文案。

### 第四層：二階效應——品牌忠誠度的崩解

Deloitte 的 [2026 年全球零售展望](https://www.growthhq.io/our-thinking/agentic-commerce-how-ai-shopping-agents-are-set-to-disrupt-global-retail-in-2026-and-beyond)調查顯示，**81% 的零售高管認為生成式 AI 將在 2027 年前削弱品牌忠誠度**。

邏輯很簡單：如果 AI Agent 純粹按「性價比」幫你選商品，品牌故事、包裝設計、情感連結——這些傳統上建立忠誠度的手段——全部失效。你說 Nike 比白牌好？AI Agent 不看你的廣告，它看的是用戶評分、退貨率和價格。

這會引發一連串連鎖反應：品牌行銷預算需要從「對人廣告」轉向「對 AI 優化」。想想 SEO（搜尋引擎優化）的歷史——當 Google 主導了流量入口，整個行銷產業圍繞 Google 的算法重新組織。現在，同樣的事情要在 AI Agent 層面再發生一次。[HBR 稱之為「Agent 可觀測性」](https://hbr.org/2026/02/how-brands-can-adapt-when-ai-agents-do-the-shopping)（agentic observability）——品牌需要即時監控 AI Agent 如何描述自己的產品、引用哪些來源、如何框架推薦邏輯。

---

## 未來展望

### 短期（3-6 個月）：法律戰升級，協定競賽加速

Perplexity 已經在 3 月 10 日提出上訴。這個案子幾乎確定會進入上訴法院，甚至可能最終打到最高法院——因為它涉及的問題太根本了：CFAA 在 AI Agent 時代的適用範圍、平台主權與用戶主權的邊界、自動化存取的法律地位。

同時，eBay 已經在 2026 年 1 月更新政策禁止購物機器人，更多平台可能跟進。但另一邊，Google（UCP）和 OpenAI（ACP）的開放協定也在快速擴張。未來幾個月的關鍵問題是：**Amazon 會加入某個開放協定，還是繼續閉鎖自己的生態？**

有跡象顯示 Amazon 不會永遠閉鎖。[CNBC 報導](https://www.cnbc.com/2025/12/24/amazon-faces-a-dilemma-fight-ai-shopping-agents-or-join-them.html)，Amazon 預期將與部分第三方 Agent 合作，並已與一些提供商進行了對話。畢竟，如果消費者真的開始大規模使用 AI Agent 購物，完全拒絕 Agent 存取等於把客戶推向其他平台。

### 中期（6-18 個月）：三種可能的發展情境

**情境一：平台主導型 Agent 生態（圍牆花園 2.0）**。Amazon、Google、阿里巴巴等巨頭各自建立自己的 Agent 生態系——消費者只能用平台核准的 AI 工具。Amazon 的 Buy For Me 和 Rufus 就是這條路的先行者。這最符合平台的利益，能保護廣告收入和數據護城河。但缺點是消費者體驗受限，不同平台的 Agent 之間無法互通，用戶得分別跟 Amazon 的 Agent 和 Walmart 的 Agent 打交道。就像現在手機的 App 生態——每家一個圍牆花園，消費者在不同花園間疲於奔命。

**情境二：協定驅動的開放生態（HTTP 時刻）**。UCP 和 ACP 成為通用標準，任何 AI Agent 都能透過標準化介面與任何平台互動。零售商只需接入協定，就能對所有 AI Agent 開放。這最符合消費者利益，也最可能催生創新——就像 HTTP 協定催生了整個 Web 生態。但這條路的最大阻力是：誰來說服 Amazon 放棄它的流量控制權？除非歐盟的 DMA 或類似法規強制要求開放，否則最大的平台有充分的動機抵制。

**情境三：差異化共存（最可能的現實路徑）**。高價值、高信任的交易（電子產品、處方藥、金融商品）仍需透過平台核准的 Agent 或直接人工操作，因為退貨、保固、法規遵循的風險太高。低風險的日常消費品（衛生紙、充電線、零食）則開放給第三方 Agent——反正這些品類的利潤薄、品牌忠誠度低，平台也沒太大動力死守。平台透過 API 存取層收費，建立新的變現模式——本質上從「廣告商」轉型為「Agent 基礎設施提供商」。

以我的判斷，情境三是最可能的落地結果。但到達那個終態的過程中，會有大量的法律戰、政策辯論和商業談判。新創公司如 [Daydream（時尚 AI 購物，剛拿了 5000 萬美元種子輪）](https://www.modernretail.co/technology/why-the-ai-shopping-agent-wars-will-heat-up-in-2026/)和 [Composio（Agent 專屬互聯網介面，融資 2900 萬美元）](https://www.36kr.com/p/3719289614037512)都在押注這個過渡期的機會。如同 Modern Retail 引用的一位高管所說：「每個人都在造太空船，但沒有人真正發射過。」

### 長期推演：3-5 年後的消費世界

如果 AI Agent 購物真的普及（Morgan Stanley 預測 2030 年 50% 消費者使用），我們面對的是一個根本不同的商業世界：

**商品變成「API 可呼叫的服務」**。品牌不再把商品放在貨架上等人來挑，而是讓商品數據以結構化格式存在於各種 AI Agent 的知識庫中。誰的數據結構化做得好、API 回應速度快、價格動態調整精準，誰就能在 Agent 的推薦中獲得優先。

**廣告從「對人展示」轉向「對 Agent 優化」**。Brand marketing 的概念不會消失，但會分裂成兩條路線：一條繼續面向人類（社群媒體、短影音），建立情感連結；另一條面向 AI Agent（結構化數據、Agent 可讀的品牌描述、API 回應品質），確保在 Agent 的推薦邏輯中佔有一席之地。

**平台從「商場」變成「倉庫 + 物流」**。這跟實體零售的演化路徑驚人地相似——當年 Walmart 靠超級商場把社區雜貨店打趴，現在 AI Agent 可能把 Walmart 變成一個消費者永遠看不到的後端倉庫。

### 給讀者的行動建議

**如果你是開發者**：現在就開始學習 UCP 和 ACP 協定。[Google Developers](https://developers.google.com/merchant/ucp) 和 [OpenAI Developers](https://developers.openai.com/commerce/) 都有完整的文件。掌握 Agent 可讀的結構化產品數據格式，這會是未來幾年最有價值的技能之一。

**如果你是創業者或產品經理**：思考你的產品在 Agent 生態中的定位。你是要做 Agent（像 Perplexity），還是做 Agent 的基礎設施（像 Shopify）？前者正面對激烈的法律和商業風險，後者可能是更穩健的切入點。

**如果你是一般科技從業者**：開始關注「Agent 可觀測性」的概念。當 AI Agent 成為消費者和品牌之間的中間層，理解 Agent 如何做出推薦決策、如何呈現品牌資訊，會成為行銷和產品策略的核心能力。

最後一個問題留給大家想想：**當 AI Agent 成為消費決策的新中間人，我們是解放了消費者的選擇權，還是只是把守門人從 Amazon 換成了 OpenAI？**

這場戰爭才剛開始。GTC 2026 下週就要登場，Jensen Huang 肯定會談 AI Agent 的未來。而 Perplexity 的上訴結果，可能定義接下來十年數位商業的遊戲規則。

不管結果如何，有一件事是確定的：那個你打開 App、滑啊滑、比價半小時、最後加了一堆本來沒打算買的東西——這種購物體驗的日子，可能已經開始倒數了。

---

## 延伸閱讀

- [Amazon wins court order to block Perplexity's AI shopping agent — CNBC](https://www.cnbc.com/2026/03/10/amazon-wins-court-order-to-block-perplexitys-ai-shopping-agent.html)：最完整的案件報導，包含法官裁定原文引述
- [Perplexity Comet hurtling toward Amazon ban — The Register](https://www.theregister.com/2026/03/11/perplexity_comet_amazon_ban/)：技術面最深入的分析，包含 Comet 偽裝 Chrome 的細節和 Perplexity 的完整回應
- [What the Perplexity-Amazon lawsuit could mean for digital advertising — Marketing Brew](https://www.marketingbrew.com/stories/2026/01/12/perplexity-amazon-lawsuit-agentic-AI-retail-media)：從廣告產業角度分析此案影響，包含 Gartner 和 VML 分析師觀點
- [How Brands Can Adapt When AI Agents Do the Shopping — Harvard Business Review](https://hbr.org/2026/02/how-brands-can-adapt-when-ai-agents-do-the-shopping)：品牌端最有策略深度的分析，提出「信任層」框架和五大行動方向
- [Why the AI shopping agent wars will heat up in 2026 — Modern Retail](https://www.modernretail.co/technology/why-the-ai-shopping-agent-wars-will-heat-up-in-2026/)：全景式的市場競爭格局，涵蓋所有主要玩家的動態和數據
- [Amazon fights back as AI shopping agents threaten ad revenues — eMarketer](https://www.emarketer.com/content/amazon-fights-back-ai-shopping-agents-threaten-ad-revenues)：廣告營收數據最詳實的分析，包含 Andy Jassy 的直接引述
- [Google announces Universal Commerce Protocol — TechCrunch](https://techcrunch.com/2026/01/11/google-announces-a-new-protocol-to-facilitate-commerce-using-ai-agents/)：Google UCP 的首次報導，理解「協定路線」vs.「破門路線」的關鍵資料
- [Buy it in ChatGPT — OpenAI](https://openai.com/index/buy-it-in-chatgpt/)：OpenAI ACP 的官方介紹，了解另一條開放商務協定的路徑
