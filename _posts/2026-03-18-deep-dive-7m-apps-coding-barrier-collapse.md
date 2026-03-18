---
title: "八個月七百萬個 App：寫程式的門檻消失之後"
date: 2026-03-18
description: "一家 YC 新創在八個月內讓用戶創建超過七百萬個應用程式，其中七成來自零程式經驗的人。當軟體開發的門檻正在消失，真正的問題不是誰能寫程式，而是誰能寫出值得存活的程式。"
tags: [deep-dive, ai-tools, ai-coding, ai-industry]
---

## 引言

想像一下這個場景：一位做設備安裝的小企業主，白天在工地跑來跑去，晚上回家對著螢幕說了幾句話，三天後他有了一個客製化的報價系統。一位律師，從來沒碰過任何程式語言，花了一個週末做出了完全貼合自己工作流程的客戶管理工具。一位把心理諮詢和運動訓練結合起來的創業者，找遍外包公司都開價太高，最後自己在 AI 平台上做出了一個跨學科應用——幾週後已經有數百位用戶在用。

這些不是科幻小說的情節。2026 年 3 月 16 日，YC 的 Lightcone 播客裡，一家叫 Emergent 的新創公司兩位創辦人丟出了一組讓人必須反覆確認的數字：**八個月，超過七百萬個應用程式**，其中 70% 到 80% 來自完全沒有程式經驗的人。

七百萬。不是七百萬行程式碼，是七百萬個 App。

這個數字之所以值得花二十分鐘細讀，不是因為它大到離譜，而是因為它指向一個正在發生的結構性轉變：**軟體開發的門檻，正在以肉眼可見的速度消失。** 但門檻消失之後，迎接我們的究竟是全民創造的黃金時代，還是一場品質災難？

這篇深度分析的起點是 [36氪的一篇報導](https://www.36kr.com/p/3727875874323334)，它整理了 YC Lightcone 播客的核心內容。但故事遠不止於此——我們需要看得更遠、更深。

---

## 事件全貌

Emergent 是一家由雙胞胎兄弟 Mukund Jha 和 Madhav Jha 創立的公司，2024 年成立，背後站著一票頂級投資人：Khosla Ventures、SoftBank、Google、Lightspeed India、Prosus Ventures，加上 Y Combinator——總融資額達到 [1 億美元](https://www.ycombinator.com/companies/emergent)。

他們做的事情，說穿了就一句話：**讓你用自然語言描述需求，AI 自動生成、測試、部署完整的生產級應用程式。** 不是做個原型給你看看，而是直接可以上線、接訂單、處理數據的完整產品。

有趣的是，Emergent 最初不是做 App 建構工具的。他們一開始盯的是軟體測試——因為在真實開發中，最慢的從來不是寫第一版程式碼，而是改、再改、繼續改。每一次修改都要確認能不能用、會不會出錯。當他們把這一步自動化之後，整個開發迴圈就被壓縮了：想法輸入 → 自動生成 → 自動檢查 → 自動調整。

結果？公開上線七個月就達到 [5000 萬美元年經常性收入（ARR）](https://www.ycombinator.com/companies/emergent)，成為全球成長最快的新創公司之一。超過 190 個國家、500 萬用戶在平台上建構了超過 600 萬個應用程式。訪談中甚至提到，有一家公司靠在 Emergent 上開發的產品拿到了 400 萬美元融資。

但 Emergent 不是孤例。它只是一個更大浪潮的縮影。

**Lovable**，這家斯德哥爾摩的 AI App 建構平台，在八個月內就衝破了 [1 億美元 ARR](https://techcrunch.com/2025/12/18/vibe-coding-startup-lovable-raises-330m-at-a-6-6b-valuation/)，四個月後翻倍到 2 億美元。2025 年 12 月完成 3.3 億美元 B 輪融資，估值從半年前的 18 億飆到 66 億美元——三倍增長。每天有超過 10 萬個新專案在平台上誕生。它的客戶名單裡有 Klarna、Uber、Zendesk。CEO 直接放話：Lovable 要成為「企業最後需要購買的一套軟體」。

**Bolt.new**，另一匹黑馬，在短短 4.5 個月內就達到 [4000 萬美元 ARR](https://vibecoding.app/blog/best-ai-app-builders)。

整個「vibe coding」市場在 2026 年的估值已經[突破 500 億美元](https://vibecoding.app/blog/best-ai-app-builders)。從 Replit（估值 90 億美元）到 v0、Mocha、Base44——十幾家平台在搶同一塊蛋糕。這不是某一家公司的故事，這是一整個產業的誕生。

---

## 脈絡

要理解這波浪潮的真正意義，我們得先回頭看：軟體開發的「民主化」，從來不是新概念。

2003 年，WordPress 誕生。它讓不會寫 HTML、CSS、JavaScript 的人也能架網站。二十多年後的今天，WordPress [驅動了全球 42.6% 的網站](https://www.wpzoom.com/blog/wordpress-statistics/)，超過 5.18 億個網站。接著是 Wix、Squarespace、Webflow——每一波都在降低門檻，每一波都讓更多人能夠「發布」。

但這些工具降低的，始終是「網站」的門檻，不是「軟體」的門檻。做一個部落格和做一個能處理訂單、管理庫存、跑數據分析的應用程式，是完全不同層級的事情。後者需要的不只是介面，還有後端邏輯、數據庫、API 串接、安全性、效能優化——這些東西，直到 2024 年之前，都還是專業工程師的領域。

轉折點出現在 2023 年。當時還在 Tesla 帶 AI 團隊的 Andrej Karpathy 說了一句後來被引用到爛的話：**「最火的新程式語言是英語。」** 那時候大家當他在開玩笑。

2025 年 2 月，Karpathy 正式[提出「vibe coding」這個概念](https://x.com/karpathy/status/1886192184808149383)——他描述自己用 Cursor 搭配 Claude 模型、靠語音輸入（SuperWhisper）來開發軟體，完全不逐行審查 AI 生成的程式碼。「把自己交給 vibe，擁抱指數成長，忘記程式碼的存在。」

一年後的 2026 年，Karpathy 自己又把這個詞升級了。他說 vibe coding 已經「過時」，取而代之的是[「agentic engineering」](https://thenewstack.io/vibe-coding-is-passe/)——你 99% 的時間不是在寫程式碼，而是在指揮 AI agent 寫程式碼，你的角色是監督和品質把關。從「跟著 vibe 走」到「工程化的 agent 協作」，這個語義升級本身就說明了很多事情。

為什麼是現在？幾個條件同時成熟了。LLM 的程式碼生成能力在 2025 年有了質的飛躍——不只是能寫出語法正確的程式碼，而是能理解上下文、處理複雜邏輯、生成完整的前後端架構。自動化測試框架的成熟，讓 AI 生成的程式碼能被即時驗證。雲端部署的門檻降到接近零。當這些條件同時到位，「想法直接變成產品」就從願景變成了事實。

---

## 多方觀點

### 樂觀派：這是創造力的解放

Emergent 創辦人 Mukund Jha 在 YC 播客中的核心論點很清楚：過去阻礙軟體創新的，從來不是技術能力，而是**表達的摩擦**。「比錢更難的，是表達的問題。我明明知道自己想做什麼，但講給別人聽的時候，很多細節就丟了。」

這個觀點有道理。每個做過軟體專案的人都知道，需求文件裡永遠裝不下腦中的完整畫面。你在白板上畫的流程圖，到了工程師手中會變成另一個東西。而現在，那個把想法翻譯成程式碼的中間人——不管是產品經理、設計師還是外包團隊——正在被 AI 取代。

9to5Mac 的一位作者提供了一個[生動的案例](https://9to5mac.com/2026/02/23/ai-coding-tools-may-be-the-end-of-freemium-utility-apps/)：他用 OpenAI 的 Codex 在不到 15 分鐘內，從一個空資料夾開始，做出了一個完全符合需求的 Mac 應用程式。而且比 App Store 上那些塞滿廣告的免費版和功能半殘的付費版都好用。他的結論是：**「廣告滿天飛的爛 App 日子不多了。」**

### 悲觀派：品質危機正在醞釀

The Register 直接用標題開砲：[「Vibe coding: What is it good for? Absolutely nothing.」](https://www.theregister.com/2025/11/24/opinion_column_vibe_coding/)

他們的擔憂不是沒有根據。Lawfare 的一篇[深度分析](https://www.lawfaremedia.org/article/when-the-vibe-are-off--the-security-risks-of-ai-generated-code)指出，AI 生成的程式碼中，只有約 55% 是安全的——也就是說，**將近一半的 AI 生成程式碼帶有已知的安全漏洞**。更令人擔憂的是一個叫「slopsquatting」的攻擊手法：AI 會生成看起來很合理但實際不存在的套件名稱，攻擊者搶先註冊這些名稱，植入惡意程式碼。用了 AI 生成程式碼的開發者，等於在不知不覺中引入了後門。

2025 年中，Lovable 平台上 [1,645 個網頁應用中有 170 個被發現存在會洩露個人資料的安全漏洞](https://en.wikipedia.org/wiki/Vibe_coding)——超過 10% 的安全事故率，對一個估值 66 億美元的平台來說，這不是小事。

GitClear 的一項[追蹤 2.11 億行程式碼變更的縱向研究](https://dev.to/shayy/why-your-vibe-coded-app-will-fail-and-how-to-fix-it-369p)揭示了更深層的問題：從 2021 到 2024 年，程式碼重構的比例從 25% 暴跌到不足 10%，程式碼重複量增加了約四倍，程式碼翻修率（churn）幾乎翻倍。AI 不是在寫更好的程式碼——它是在寫更多的程式碼，而且是更難維護的程式碼。

一位資深工程師的評論最為一針見血：大規模 debug AI 生成的程式碼，「幾乎是不可能的事」。

### 最精彩的反轉：Karpathy 自己也不用 vibe coding

這或許是整個故事中最耐人尋味的細節。Futurism [報導](https://futurism.com/artificial-intelligence/inventor-vibe-coding-doesnt-work)，「vibe coding」這個詞的發明者 Karpathy，在做他自己的新專案時，承認他選擇了手寫程式碼。為什麼？因為 vibe coding 在面對真正複雜的工程問題時，還是不夠可靠。

這不是打臉，這是一個非常誠實的訊號：**vibe coding 適合快速原型和簡單應用，但不是萬能的。** 知道它的邊界在哪裡，比盲目吹捧重要得多。

### 第一線開發者的真實反饋

Stack Overflow 部落格上一篇[關於 AI 對 Gen Z 開發者影響的深度分析](https://stackoverflow.blog/2025/12/26/ai-vs-gen-z/)提供了來自前線的聲音。84% 的開發者現在使用 AI 工具輔助開發，比前一年增加 14%。但同時，70% 的招聘經理認為 AI 可以執行實習生的工作，37% 的雇主甚至表示「比起應屆畢業生，他們更願意『雇用』AI」。

這些數據不是抽象的趨勢報告——它們代表真實的人、真實的職涯焦慮。

### 我的看法

以我的經驗來看，這波浪潮的核心張力在於：**它同時是真實的革命和潛在的災難，取決於你站在哪個角度看。** 對於那些被技術門檻擋在門外的創業者和業務人員來說，這是千載難逢的機會。對於把「會寫程式」當作職業護城河的初級開發者來說，地板正在塌陷。

但我不認為這是一個零和遊戲。WordPress 讓人人都能架網站，但專業的 Web 開發者並沒有消失——他們的角色從「幫你架網站」變成了「幫你架好的網站」。同樣的邏輯可能適用於 AI App 建構工具：當人人都能做 App，差異化就不再是「有沒有 App」，而是「App 好不好用、安不安全、能不能維護」。

問題是，這一次的速度比 WordPress 時代快了不知道多少倍。市場可能沒有足夠的時間消化這個轉變。

---

## 產業衝擊

### 第一層：初級開發者首當其衝

數據已經很殘酷了。根據多項調查，**22 至 25 歲軟體開發者的就業率，從 2022 年底的高峰下滑了近 20%**。入門級科技招聘同比下降 25%，科技實習職位發布量自 2023 年以來減少 30%。Gen Z（22-27 歲）的失業率達到 7.4%，幾乎是[全國平均 4.2% 的兩倍](https://stackoverflow.blog/2025/12/26/ai-vs-gen-z/)。

更令人不安的是一個結構性矛盾：電腦科學畢業生的失業率達到 6.1%，**甚至高於文科畢業生的約 5%**。電腦工程畢業生更慘，7.5%。這在五年前是不可想像的。

Forrester 預測，電腦科學入學人數將[下降 20%](https://www.finalroundai.com/blog/software-engineering-job-market-2026)，填補開發者職位所需的時間將翻倍。如果初級開發者的培養管道被卡住，幾年後資深開發者的供給也會出問題。正如 Stack Overflow 上那句被廣泛引用的話：**「如果你現在不培養初級開發者，未來就永遠不會有資深開發者。」**

### 第二層：免費增值模式的 App 正在被淘汰

9to5Mac 的[分析](https://9to5mac.com/2026/02/23/ai-coding-tools-may-be-the-end-of-freemium-utility-apps/)指向一個有趣的推論：當任何有一點想法的人都能在 15 分鐘內做出一個客製化的工具，誰還需要下載那些塞滿廣告、功能陽春的免費 App？誰還願意為一個只做一件事的工具付月費？

那些靠「單一功能 + 訂閱制」活著的獨立開發者和小型 SaaS 公司，可能會發現自己的商業模式正在被侵蝕。不是被大公司打敗，而是被自己的用戶取代——用戶自己做了一個更貼合需求的版本。

### 第三層：AI App 的留存率危機

TechCrunch 報導的 [RevenueCat 報告](https://techcrunch.com/2026/03/10/ai-powered-apps-struggle-with-long-term-retention-new-report-shows/)揭示了一個尷尬的事實：**AI 驅動的 App 用戶取消年度訂閱的速度，比非 AI App 快 30%。** 退款率上限也更高（15.6% vs 12.5%）。報告的結論很直白：「AI 能驅動更強的早期變現，但維持價值仍是挑戰。」

翻譯成白話：AI 做的 App 很容易讓人心動，但很難讓人留下。這可能是因為 AI 生成的產品缺乏深度打磨——它們解決了「有沒有」的問題，但沒解決「好不好用」的問題。

### 第四層：安全債和技術債的定時炸彈

Barrack AI 的一項調查發現，[2025 年 1 月到 2026 年 2 月間，每一次對 AI 應用的獨立安全審計都發現了相同的結構性問題](https://blog.barrack.ai/every-ai-app-data-breach-2025-2026/)：Firebase 和 Supabase 配置錯誤、硬編碼在客戶端程式碼中的密鑰、缺乏身份驗證機制。這些不是個別案例，而是系統性的流行病。

歐盟的《網路韌性法案》（Cyber Resilience Act）要求軟體產品必須符合「安全設計」原則、進行風險評估、提供多年的漏洞修補。Lawfare 的分析直言：vibe coding 的「接受 bug 存在」哲學，與這些法規要求**從根本上不相容**。

更諷刺的是，技術文件和風險評估報告本身也可能是 AI 生成的，創造出一種「合規假象」——看起來什麼都有，實際什麼都沒做。

### 第五層：二階效應——商業模式的根本重構

如果軟體開發的邊際成本趨近於零，整個軟體產業的價值分配就會被重新洗牌。

過去的邏輯是：你付錢買軟體（或訂閱制付月費），因為做軟體很貴。但當做軟體的成本從幾百萬降到幾萬，甚至免費，**人們為什麼還要付錢給 SaaS 公司？** OpenAI COO 最近也在公開場合被問到這個問題——他承認 AI 無法完全取代傳統 SaaS，但語氣明顯比一年前謹慎了很多。

真正的贏家可能是提供 AI 開發平台的公司本身。Lovable、Emergent、Bolt.new——它們的商業模式不是賣軟體，而是賣「做軟體的能力」。這是一個更上游的位置，也是一個更有防禦力的位置。但它們面臨一個根本挑戰：當你的平台讓所有人都能做軟體，你怎麼確保這些軟體的品質不會反過來摧毀你的聲譽？

---

## 未來展望

### 短期（3-6 個月）：井噴與洗牌同時發生

幾乎可以確定會發生的事：更多 AI App 建構平台會湧入市場，平台間的差異化會越來越難。App Store 和 Google Play 會面臨更大的 AI 生成 App 審核壓力。企業客戶會開始嘗試用這些工具取代部分內部系統開發。

同時，第一批「vibe coding 災難」會開始浮出水面——安全事件、數據洩露、因為無法維護而被迫放棄的專案。這些案例會成為反對派最有力的論據。

### 中期（6-18 個月）：分化出兩條路線

**路線 A：消費級「用完即丟」型 App。** 大量個人化、場景化的小工具，不追求長期維護，用幾個月就換下一個。這會是 AI App 建構工具最自然的落腳點——就像現在的 Google Sheets 公式一樣，不是正式產品，但確實解決問題。

**路線 B：企業級「agentic engineering」。** 就像 Karpathy 說的，從 vibe coding 進化到 agentic engineering——AI 寫程式碼，但有系統化的人類監督、程式碼審查、安全掃描。這條路線需要專業開發者，只是他們的角色從寫程式碼變成審程式碼。

我認為路線 A 的市場規模會更大，但路線 B 才是真正有商業價值的地方。

### 長期推演：3-5 年後的軟體世界

如果這個趨勢持續——而且我看不到任何逆轉的跡象——3 到 5 年後，「軟體開發者」這個職業的定義會被徹底改寫。會寫程式碼不再是核心競爭力，就像會用 Word 不是文書工作者的核心競爭力一樣。核心競爭力會轉移到：**系統架構思維、安全工程、品質把關、以及最關鍵的——理解業務需求的能力。**

Morgan Stanley 的[分析](https://www.morganstanley.com/insights/articles/ai-software-development-industry-growth)預測，AI 不會減少開發者的總需求，反而會因為軟體的應用場景爆炸性增長而創造更多需求。但這些需求的「形狀」會完全不同——不是更多寫 CRUD 的人，而是更多能把 AI 生成的東西變得可靠、可維護、可信賴的人。

### 給不同角色的行動建議

**如果你是開發者：** 停止把「會寫程式碼」當作護城河。你需要的護城河是：理解系統架構、寫得出好的測試、看得懂安全漏洞、能在 AI 的輸出中判斷什麼是好的設計。學會「審程式碼」比「寫程式碼」更重要。

**如果你是創業者或產品經理：** 這是好消息——你的想法到產品的距離從來沒有這麼短過。但不要被速度沖昏頭。用 AI 快速驗證想法，但在準備規模化之前，找專業的人來處理安全和維護。那個 15 分鐘做出來的 MVP，和一個能撐住一萬個用戶的產品之間，仍然有巨大的差距。

**如果你是一般科技從業者：** 學會使用這些工具。不是要你變成開發者，而是要你知道什麼是可能的。就像你不需要會攝影才能用手機拍照，但你需要知道手機能拍照。AI App 建構工具正在變成每個知識工作者的基本技能之一。

---

我們正站在一個奇妙的交叉口。七百萬個 App 誕生了，但其中有多少能活過第一年？門檻消失了，但品質的門檻可能比以前更高。人人都能造船了，但大海依然是大海——知道怎麼造船和知道怎麼航行，從來就不是同一件事。

真正的問題或許不是「AI 會不會取代開發者」，而是：**當造軟體變得跟寫文件一樣簡單，我們對軟體的期待，會不會也跟著降低？**

如果答案是「會」，那才是最值得擔心的事。

---

## 延伸閱讀

- [Emergent — Y Combinator 公司頁面](https://www.ycombinator.com/companies/emergent)：Emergent 的完整背景、融資資訊和產品定位
- [Vibe-coding startup Lovable raises $330M at a $6.6B valuation — TechCrunch](https://techcrunch.com/2025/12/18/vibe-coding-startup-lovable-raises-330m-at-a-6-6b-valuation/)：Lovable 的驚人成長數據和估值飆升的完整報導
- [AI vs Gen Z: How AI has changed the career pathway for junior developers — Stack Overflow Blog](https://stackoverflow.blog/2025/12/26/ai-vs-gen-z/)：大量第一手數據揭示 AI 對初級開發者就業市場的衝擊
- [When the Vibes Are Off: The Security Risks of AI-Generated Code — Lawfare](https://www.lawfaremedia.org/article/when-the-vibe-are-off--the-security-risks-of-ai-generated-code)：從法律和安全角度深度剖析 vibe coding 的風險
- [Vibe coding is passé. Karpathy has a new name for the future of software — The New Stack](https://thenewstack.io/vibe-coding-is-passe/)：Karpathy 從 vibe coding 到 agentic engineering 的思路演變
- [AI coding tools may be the end of freemium utility apps — 9to5Mac](https://9to5mac.com/2026/02/23/ai-coding-tools-may-be-the-end-of-freemium-utility-apps/)：AI 建構工具如何威脅免費增值模式 App 的生存空間
- [AI-powered apps struggle with long-term retention — TechCrunch](https://techcrunch.com/2026/03/10/ai-powered-apps-struggle-with-long-term-retention-new-report-shows/)：RevenueCat 報告揭示 AI App 的留存率困境
- [AI, Hiring, and the Future of Coding — Morgan Stanley](https://www.morganstanley.com/insights/articles/ai-software-development-industry-growth)：Morgan Stanley 對 AI 時代軟體開發人力市場的分析
