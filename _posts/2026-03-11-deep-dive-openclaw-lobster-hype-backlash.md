---
title: "從一蝦難求到付費卸載：OpenClaw 龍蝦狂潮的荒誕啟示錄"
date: 2026-03-11
description: "OpenClaw 從萬人排隊安裝到用戶付費卸載，只花了不到一個月。這場 AI Agent 史上最荒誕的 hype cycle，揭露了 token 經濟的真實成本、軟體產業的結構性崩塌，以及「養蝦人」與「賣鏟人」之間殘酷的財富轉移。"
tags: [deep-dive, agents, ai-tools, ai-industry, llm]
---

## 引言

想像一下這個場景：深圳騰訊總部門口，近一千人排著長隊，等著讓工程師在自己的筆電上安裝一隻「龍蝦」。隊伍裡有程序員、退休工程師、家庭主婦、學生——甚至有人從外地坐高鐵專程趕來。黃牛代裝費一度炒到上千元人民幣，安裝教程在小紅書上的點擊量以億計，馬化騰在朋友圈感嘆「沒想到這麼火」，雷軍連發三條微博推「小米龍蝦」。

這隻「龍蝦」，就是 OpenClaw——一個開源 AI 智能體框架，因為圖標酷似紅色波士頓龍蝦而得了這個暱稱。它用了三個月就拿下 GitHub 史上最高 star 數（超過 24.7 萬），打破了 React 花了 13 年才建立的紀錄。

但故事的反轉來得比任何人預期都快。

不到一個月後，社群平台上開始湧現一種新服務：**付費卸載龍蝦**。「週五求安裝，週一求卸載」——一位兼職做「龍蝦清理」的技術人員在網上曬出了新業務。有人一覺醒來發現帳單暴增數百美元，有人的 AI 失控刪光了郵件，有人的 API 密鑰被惡意技能竊取。那隻曾被視為「數位員工」的龍蝦，搖身一變成了吞噬 token 費用、製造系統混亂的「電子河豚」。

從一蝦難求到蝦手不及，這場被全球媒體稱為「養龍蝦」的 AI 狂潮，在極短時間內完成了從神話到笑話的荒誕輪回。但如果你只看到笑話，那你錯過了這個故事真正重要的部分。

這不只是一場 hype cycle 的教科書案例。OpenClaw 現象的背後，是 AI Agent 正在對整個軟體產業發動的結構性顛覆、是 token 經濟對傳統商業模式的根本挑戰、是「養蝦人」與「賣鏟人」之間一場殘酷而精準的財富轉移。

這篇報導的起點是[「付費卸載龍蝦：一場 AI 狂熱的荒誕反轉」](https://www.36kr.com/p/3717175279809031)，但故事遠不止於此。

---

## 事件全貌

### 一隻龍蝦的誕生

OpenClaw 的創造者是奧地利開發者 Peter Steinberger。這位花了 13 年做 PDF 格式化工具的工程師，在 2025 年 4 月感受到了 AI 的「範式轉移」——他試著做一個 Twitter 分析工具，發現 AI 已經可以處理所有重複性的程式碼搭建工作。於是他用一個週末寫了個 WhatsApp 中繼工具，讓 AI 能透過即時通訊軟體來執行任務。

這個「週末專案」在 2025 年 11 月以「Clawd」之名面世（取自 Claude + Claw 的雙關語），但很快被 Anthropic 的法務團隊要求改名。經過社群在凌晨五點的 Discord 頭腦風暴，先是改叫 Moltbot（取自龍蝦蛻殼的 molt），最後定名 [OpenClaw](https://openclaw.ai/)。

技術上，OpenClaw 是一個持續運行的 Node.js 程序，它像一個永不下線的管家，連接你的聊天工具（Signal、Telegram、WhatsApp、Discord）、AI 模型（Claude、GPT、DeepSeek、Kimi）和本地系統。和 ChatGPT 最大的不同是：**它有「手」**。它可以執行終端命令、自動化瀏覽器操作、管理本地檔案、透過排程器（Heartbeat）自主執行任務——即使你不在電腦前。

截至 2026 年 3 月，OpenClaw 有超過 50 種整合、100 種以上預設 AgentSkills、[ClawHub 上超過 5,700 個社群技能](https://github.com/openclaw/openclaw)，npm 週下載量達到 150 萬次。

### 中國的龍蝦熱

真正讓 OpenClaw 從極客玩具變成全民運動的，是中國市場的瘋狂擁抱。

2026 年初，「養龍蝦」一詞開始在中國社群媒體上瘋傳。短短幾週內，中國五大雲端服務商——騰訊雲、阿里雲、火山引擎、京東雲、百度智能雲——全部推出了「一鍵部署 OpenClaw」服務。每家大廠都發布了自己的 OpenClaw 相容分支：[KimiClaw](https://medium.com/@julian.goldie_83205/kimi-claw-a-4-8-billion-chinese-ai-company-just-put-openclaw-in-your-browser-7dfcf48609d2)、MaxClaw、CoPaw、ArkClaw、WorkBuddy、AutoClaw⋯⋯名單還在不斷增長。

騰訊是動作最大的一家。3 月 9 日，騰訊一天之內連發三款產品：[WorkBuddy](https://technode.com/2026/03/09/tencent-launches-openclaw-like-workplace-ai-agent-workbuddy/)（桌面端 AI 智能體，相容 OpenClaw 技能，整合企業微信、QQ、飛書、釘釘），[QClaw](https://technode.com/2026/03/09/tencent-reportedly-tests-qclaw-ai-agent-with-one-click-openclaw-deployment/)（一鍵安裝器，把 OpenClaw 塞進微信和 QQ），以及企業微信的官方接入教程。消息公布後，[騰訊股價單日暴漲 7.27%](https://www.bloomberg.com/news/articles/2026-03-10/tencent-zhipu-shares-jump-on-launches-of-ai-agents-tapping-into-openclaw)，創下近半年來最大單日漲幅，市值重回 5 萬億港元。

更令人驚訝的是政策面的響應速度。「AI 智能體」首次被寫進中國政府工作報告，國務院總理在報告中明確提出要「推動新一代智能終端和 AI 智能體的加速應用」。[深圳龍崗區推出「龍蝦十條」](https://www.yahoo.com/news/articles/chinas-shenzhen-backs-openclaw-ai-122205994.html)，對 OpenClaw 相關專案最高補貼 200 萬元人民幣；[無錫高新區推出「養 AI 龍蝦 12 條」](https://www.globaltimes.cn/page/202603/1356657.shtml)，單項支持最高達 500 萬元，鼓勵將龍蝦與工業質檢、設備預測性維護等垂直領域結合。

NVIDIA 也沒缺席，推出了[企業級開源 AI Agent 平台 NemoClaw](https://www.cnbc.com/2026/03/10/nvidia-open-source-ai-agent-platform-nemoclaw-wired-agentic-tools-openclaw-clawdbot-moltbot.html)。

### 然後，潮水開始退了

但在全民狂歡的喧囂之下，問題正在迅速累積。

深圳華強北的一位檔口老闆花 800 元請人裝了龍蝦，期望它能自動管理拼多多和淘寶店鋪。結果 AI 連「滿 199 減 20」和「第二件半價」都分不清。「折騰了三天，最後發現還不如我自己用手機回覆來得快。」

一位退休大媽在菜市場聽人說龍蝦「能幫人炒股賺錢」，讓孫子幫忙裝了一個。結果電腦開始變卡，也沒見它賺到錢。

更嚴重的案例接連出現：有人一覺醒來發現 API 帳單暴增數百美元，有人的 AI 智能體失控刪除了整個郵箱，有人發現自己的 API 密鑰被從 ClawHub 下載的「技能」偷走了。

「付費卸載」服務應運而生。從淘寶上幾百元的「一鍵安裝」，到小紅書上標價 998 元的「七天精通龍蝦課」，再到「付費卸載 + 系統清理」——信息差的生意，被做到了極致的兩個方向。

---

## 脈絡

### 從 ChatGPT 到 OpenClaw：Agent 的進化之路

要理解 OpenClaw 為什麼能引爆這場狂潮，得先回看 AI Agent 走過的路。

2022 年底 ChatGPT 上線，AI 進入「對話」時代——你問它答，一來一回。2023 年出現了 AutoGPT、BabyAGI 等早期 Agent 嘗試，但因為模型能力不足，大多停留在 demo 階段。2024 年，隨著 GPT-4、Claude 3 等模型的推理能力大幅提升，Devin（AI 軟體工程師）、Manus（AI 通用助手）等產品開始展示 Agent 的可能性。2025 年，Anthropic 推出 Claude Computer Use，讓 AI 能直接操作電腦介面——Agent 終於有了「手」。

OpenClaw 正是在這個時間點切入的。它不是發明了新技術，而是用開源的方式把所有碎片拼在了一起：模型接口 + 聊天整合 + 本地執行 + 技能市場 + 排程器。它讓任何人都能在自己的電腦上跑一個 AI Agent——不需要寫程式，不需要懂 API，只需要一台電腦和一個聊天帳號。

這就是為什麼它會爆炸式增長。不是因為技術多先進，而是因為**它把 Agent 的使用門檻降到了幾乎為零**。

### 中國為什麼反應最激烈

中國市場的狂熱有其特殊背景。首先，DeepSeek 在 2025 年底的爆紅已經在中國製造了一波 AI 民族自信心——中國模型可以跟美國最好的模型掰手腕。其次，中國的社群生態（微信、小紅書、抖音）天然適合病毒式傳播，「養龍蝦」這個接地氣的比喻更是讓技術概念瞬間出圈。第三，地方政府在 DeepSeek 那波錯過了先機，這次不願再觀望——深圳和無錫的政策反應速度快得驚人。

更深層的原因是：中國的 AI 大模型公司（Kimi、MiniMax、智譜、DeepSeek）需要一個爆款應用場景來消耗它們的算力產能。OpenClaw 恰好成了這個「殺手級應用」——每個活躍用戶每天可以燒掉數千萬個 token。[OpenRouter 的數據顯示](https://www.panewslab.com/en/articles/019cc79a-90b0-7177-92d6-bb10771ea27e)，中國模型在 2 月 24 日佔據全球 token 消耗量的 61%，前五名中有四個是中國模型。Kimi K2.5 在上線不到 20 天，累計收入就超過了 2025 年全年。

這不是巧合。這是一條精心設計的價值鏈：用戶養龍蝦 → 龍蝦燒 token → token 變成模型公司的收入。

---

## 多方觀點

### 技術樂觀派：「這是生產力革命的開始」

看好 OpenClaw 的人有充分理由樂觀。創業者傅盛讓自己的 AI Agent 在四分鐘內向 600 多個聯繫人發送問候，生成的帖子獲得了超過 100 萬次瀏覽。設計師 Mark Yang 說使用 OpenClaw 感覺像有了「虛擬員工」，工作量明顯減輕。那些真正懂技術的極客——了解程式碼、搞得定環境配置的人——確實從中獲得了實實在在的效率提升。

騰訊的 WorkBuddy 已經在 2,000 名非技術員工（HR、行政、營運）中完成測試，據報可以在一分鐘內完成設定，完全省去了 OpenClaw 原版的複雜配置流程。這說明大廠有能力把 Agent 的體驗打磨到「好用」的程度。

Peter Steinberger 加入 OpenAI 後，Sam Altman 在 X 上稱他為「天才」，並表示 OpenClaw 將成為 OpenAI 「非常聰明的 Agent 互相協作為人類做有用的事情」願景的核心。這暗示了一個更大的未來：Agent 不只是個人助手，而是一個由多個 Agent 組成的自主工作網絡。

### 安全研究者：「這是一場安全噩夢」

[Cisco 的安全團隊](https://blogs.cisco.com/ai/personal-ai-agents-like-openclaw-are-a-security-nightmare)毫不留情。他們對一個名為「What Would Elon Do?」的第三方技能進行分析，發現了 **9 個安全問題——其中 2 個嚴重、5 個高危**。具體包括：靜默數據外洩（技能在用戶不知情的情況下用 curl 命令將數據發送到外部伺服器）、prompt injection（惡意指令繞過安全準則）、command injection（通過技能流程執行 bash 命令）、tool poisoning（在技能文件中嵌入惡意載荷）。

Cisco 直言：「OpenClaw 的安全是可選的，但不是內建的。」

數字更觸目驚心。Bitdefender 發現 ClawHub 上大約 4,500 個技能中，[有約 900 個（20%）是惡意的](https://www.authmind.com/blogs/openclaw-malicious-skills-agentic-ai-supply-chain)——從憑證竊取器到後門程式應有盡有。SecurityScorecard 發現[全球有 42,900 個 OpenClaw 實例暴露在公網上](https://www.truenorthradionetwork.com/online_features/press_releases/the-openclaw-security-crisis-42-000-exposed-deployments-at-risk/article_4635e6b0-e6ba-58ca-865f-886e5a3a9762.html)，其中 15,200 個存在遠端程式碼執行漏洞。2026 年 1 月底披露的 CVE-2026-25253（CVSS 8.8）讓任何網站都能透過 WebSocket 劫持你本地的 OpenClaw——只需訪問一個惡意網頁，就足以竊取你的所有驗證 token。

中國工信部網路安全威脅和漏洞資訊共享平台為此[連續發布了兩次高危風險預警](https://www.scmp.com/tech/tech-trends/article/3346138/china-issues-second-warning-openclaw-risks-amid-adoption-frenzy)。

### 產業悲觀派：「軟體業已經被打殘了」

如果安全問題是 OpenClaw 的「內傷」，那麼它對傳統軟體產業的衝擊就是一場「外科手術」——而且手術刀握在別人手裡。

一篇在中國企業服務圈引起巨大迴響的文章[「軟件業被打殘了，吃布洛芬有用嗎？」](https://www.36kr.com/p/3717813006792068)直指核心：不管是前年的大模型一體機，還是今天的龍蝦，都指向同一個趨勢——**客戶要直接對接 AI 廠商，傳統軟體公司的中間商角色正在消失**。用友 BIP 號稱投入百億、金蝶蒼穹投入幾十億打造的低代碼平台，被 AI 降維打擊——現在畢業的大學生全部擁抱 Vibe Coding，沒人學各家自成體系的低代碼了。

### Andrej Karpathy 的冷水

但也有人在狂熱中保持清醒。前 OpenAI 和 Tesla 研究者 [Andrej Karpathy 在接受 Dwarkesh Patel 採訪時](https://www.podcastdigests.com/why-ai-agents-will-take-a-decade-to-deliver-andrej-karpathy-on-hype-reality-and-whats-missing/)潑了一盆冷水：他稱目前 Agent 的產出為「slop」（劣質品），認為真正可靠的 AI Agent **還需要十年**才能兌現當前的承諾。原因包括：智能水平不足、多模態能力有限、缺乏持續學習能力。

不過 Karpathy 也承認變化已經在發生：「你不再直接寫程式碼了，99% 的時間你在指揮 Agent 寫——你的角色是監督者。」他把這個轉變稱為從「Vibe Coding」到「Agentic Engineering」的進化。

### 以我的觀察

我認為 Karpathy 的「十年」判斷可能偏保守——考慮到模型能力的進步速度，三到五年更合理——但他對當前 Agent 能力的評估是準確的。OpenClaw 的核心問題不在於 Agent 概念有沒有用，而是**現階段的 Agent 還不具備獨立工作的可靠性**。它可以在技術人員的監督下成為強大的效率倍增器，但讓它無人值守地替你「自動管店鋪」或「自動炒股」？以目前的水準，結果多半是災難。

狂熱與幻滅之間的差距，正是技術成熟度與使用者期望之間的鴻溝。

---

## 產業衝擊

### 第一層：誰受益，誰受損

**贏家很明確——而且他們從來不在蝦池裡。**

最大贏家是大模型廠商。OpenClaw 本身是開源免費的，但驅動它運轉的「燃料」——token——是實打實的硬成本。每一次任務拆解、程式碼除錯、文件讀取，背後都是真金白銀的 API 調用。一個重度用戶每月的 token 消耗可達[數百甚至上千美元](https://www.sentisight.ai/how-much-openclaw-cost-per-month/)，全天候運行 Claude API 的成本在 800 到 1,500 美元之間。更極端的案例中，用戶報告因為自動任務配置錯誤，[每天燃燒超過 200 美元](https://eu.36kr.com/en/p/3709890881975048)。

次級贏家是雲端服務商。騰訊雲 Lighthouse 的開發者數量短時間內突破 10 萬，阿里雲的 9.9 元搶購活動日日秒空。表面上只是賣基礎設施，實際上一旦用戶的記憶文件、技能配置、API 密鑰全部沉澱在雲端，遷移成本就高到令人卻步——這才是真正的「放長線釣大魚」。

**輸家是傳統軟體公司和盲目跟風的普通用戶。**

### 第二層：SaaSpocalypse——每個座位都在消失

這場衝擊不只發生在中國。2026 年 2 月 3 日，Anthropic 發布 Claude Cowork 法律自動化工具，觸發了交易員所稱的[「SaaSpocalypse」](https://www.outlookindia.com/xhub/blockchain-insights/the-saaspocalypse-of-2026-how-agentic-ai-killed-per-seat-saas)——**一天之內，全球軟體公司蒸發了約 2,850 億美元市值**。2026 年以來，軟體產業市值[累計蒸發超過一兆美元](https://markets.financialcontent.com/stocks/article/marketminute-2026-2-24-the-1-trillion-software-carnage-how-ai-agents-broke-the-saas-model)。

[Salesforce](https://www.cnbc.com/2026/02/04/software-stocks-plunge-us-ai-disruption.html)、ServiceNow、HubSpot 股價暴跌，Infosys、Wipro、TCS 等印度 IT 外包巨頭也未能倖免。在中國，金蝶國際一度暴跌 16%。

核心邏輯很殘酷：如果 10 個 AI Agent 能做 100 個業務員的工作，你就不需要 100 個 Salesforce 座位了——你只需要 10 個。**座位數減少 90%，收入減少 90%，但產出不變。** 這不是軟體不好用了，是「用軟體的人」變少了。

不過也有反面觀點。[JP Morgan 的分析師認為](https://www.cnbc.com/2026/02/06/ai-anthropic-tools-saas-software-stocks-selloff.html)恐慌過頭了，投資者正在為不太可能實現的最壞情境定價。SaaStr 創辦人也認為這更像是估值修正而非產業末日。但即便是最樂觀的聲音，也沒有否認一個事實：per-seat 定價模型的時代，結束了。

### 第三層：開發者生態的重塑

OpenClaw 生態中已經有 [126 個創業項目](https://eu.36kr.com/en/p/3709890881975048)，其中前 30 名的盈利項目裡，超過 17 個聚焦在「一鍵雲端部署」——解決的是最後一哩路的部署門檻問題。

更深遠的變化在於開發者角色的轉變。以前你是寫程式的人，現在你是**指揮 AI 寫程式的人**。以前的護城河是「我懂某個框架」，現在的護城河是「我懂怎麼把問題拆解成 Agent 能執行的任務」。傳統低代碼平台投入的幾十億研發費用，正面臨 Vibe Coding 的降維打擊，研發成本可能全部沉沒。

DeepMind 的 Jeff Dean 觀察到，token 的消耗邏輯發生了「根本性的結構轉變」——從人機對話轉向 Agent 自主循環。一個活躍的 OpenClaw 實例執行跨郵件、日曆和瀏覽器的任務，每天可以燒掉數千萬個 token。2025 年 AI 使用報告顯示，Agent 驅動的輸出 token 已經超過平台總消耗量的 50%。

### 第四層：二階效應

如果 Agent 真的成為主流使用方式，連鎖反應是驚人的。軟體的「App 層」——那些為人類設計的介面——[將逐漸退化為「Agent 的數據和操作介面」](https://eu.36kr.com/en/p/3709890881975048)。用戶不再直接跟產品互動，他們的 Agent 自主呼叫這些服務。這意味著 UI/UX 設計的重要性可能大幅下降，取而代之的是 API 設計和 Agent 友善的數據結構。

對地方政府而言，補貼養龍蝦看似搶佔先機，但如果忽視安全底線，一旦發生大規模數據洩漏，不僅是經濟損失，更可能重創當地的數位治理生態。工信部的連續預警已經是很強的信號了。

---

## 未來展望

### 短期（3-6 個月）：洗牌已經開始

幾乎可以確定的事：大廠的「馴化版」Agent 會快速取代原版 OpenClaw 在普通用戶中的地位。騰訊的 WorkBuddy、QClaw，以及即將推出的微信自有 AI 模型，會把「養龍蝦」的門檻從「需要懂技術」降到「掃碼即用」。NVIDIA 的 NemoClaw 會收割企業市場。

同時，OpenClaw 的安全問題會催生一個全新的市場：Agent 安全審計、技能合規檢測、token 消耗監控。Cisco 已經開源了 Skill Scanner 工具，更多安全公司會跟進。

那些盲目入場的「養蝦投機者」會大量退場，市場會從 FOMO 驅動轉向價值驅動。「付費卸載」服務的高峰可能就在這幾個月。

### 中期（6-18 個月）：三種情境

**情境一：Agent 成為新的操作系統層。** 如果模型能力持續提升（考慮到目前的速度，這很可能），Agent 會成為介於人和所有數位服務之間的中間層。每個人都有一個或多個 Agent 代理日常工作，軟體公司被迫轉型為「Agent 的 API 供應商」。

**情境二：安全事件導致監管收緊。** 如果發生大規模的 Agent 安全事件（例如企業機密因 Agent 洩漏、Agent 執行了未授權的金融交易），各國政府可能對 Agent 的權限和部署施加嚴格監管，放緩普及速度。

**情境三：token 成本阻礙大規模普及。** 如果模型推理成本沒有持續下降，Agent 可能會停留在高淨值用戶和企業的工具，而非人人可用的「數位員工」。不過考慮到中國模型（DeepSeek、Kimi）正在用價格戰瘋狂壓低 token 成本，這個情境的可能性相對較低。

### 長期推演：3-5 年後

如果我們把視線拉遠到 2029-2031 年，Agent 可能真的會實現 OpenClaw 今天承諾但還做不到的那些事情。Karpathy 說的「十年」可能太悲觀了，但方向是對的——Agent 會越來越可靠，越來越自主，越來越普及。

在那個世界裡，「用軟體」這件事本身可能會變得跟今天「打字」一樣無感——你不再想著「我要用 Salesforce」，而是告訴你的 Agent「幫我跟進那 20 個客戶」，Agent 自己決定用什麼工具、怎麼做。

### 給讀者的行動建議

**如果你是開發者：** 現在就開始學習 Agent 開發——不是 OpenClaw 的特定 API，而是 Agent 架構設計的通用思維：任務拆解、工具呼叫、記憶管理、安全邊界。Karpathy 說得對，「Agentic Engineering」是下一個需要掌握的專業能力。別再投資時間學任何一家的低代碼平台了。

**如果你是創業者/產品經理：** 認真評估你的產品在 Agent 時代的定位。你的產品是「給人用的介面」還是「給 Agent 用的 API」？如果是前者，你需要加速轉型。如果你在做 B2B SaaS，開始思考 per-outcome 定價模型——因為 per-seat 的日子真的不多了。

**如果你是一般科技從業者：** 不要因為 FOMO 而盲目「養龍蝦」。如果你不懂技術，等大廠的馴化版本（WorkBuddy、QClaw 之類的）。如果你真的要嘗試原版 OpenClaw，至少遵守五條守則：不在主力機上安裝、不給過高權限、設定 token 消耗上限、只從官方渠道下載技能、隨時準備斷網止損。

這場龍蝦熱潮最深刻的教訓或許是：**在每一場淘金熱中，真正的贏家從來不是淘金者，而是賣鏟子的人。** 而在 AI Agent 的淘金熱中，鏟子就是 token。那些坐收 token 費用的模型公司、收取「場地費」的雲端廠商、靠信息差兩頭收錢的「卸載服務商」——他們才是這場遊戲裡最清醒的玩家。

在大廚就位、菜譜完善之前，普通人最好的策略，是站在廚房門口多看一會兒。

---

## 延伸閱讀

- [OpenClaw fever: why is China rushing to 'raise a lobster'? — South China Morning Post](https://www.scmp.com/tech/tech-trends/article/3345865/openclaw-fever-why-china-rushing-raise-lobster)：最完整的中國龍蝦熱英文報導，涵蓋用戶故事和政策分析
- [Personal AI Agents like OpenClaw Are a Security Nightmare — Cisco Blog](https://blogs.cisco.com/ai/personal-ai-agents-like-openclaw-are-a-security-nightmare)：Cisco 安全團隊的第一手分析，展示 Agent 技能供應鏈的真實威脅
- [SaaSpocalypse 2026: How Agentic AI Killed Per-Seat SaaS — Outlook India](https://www.outlookindia.com/xhub/blockchain-insights/the-saaspocalypse-of-2026-how-agentic-ai-killed-per-seat-saas)：深度分析 AI Agent 如何從根本上顛覆 SaaS 訂閱模式
- [After OpenClaw Reached the Top, Agent Quietly Killed the "Application" — 36Kr](https://eu.36kr.com/en/p/3709890881975048)：從 token 經濟學角度分析 Agent 如何重塑軟體產業價值鏈
- [Why AI Agents Will Take a Decade to Deliver — Andrej Karpathy](https://www.podcastdigests.com/why-ai-agents-will-take-a-decade-to-deliver-andrej-karpathy-on-hype-reality-and-whats-missing/)：Karpathy 對 Agent 現狀和未來的冷靜評估
- [OpenClaw creator Peter Steinberger joins OpenAI — TechCrunch](https://techcrunch.com/2026/02/15/openclaw-creator-peter-steinberger-joins-openai/)：OpenClaw 創造者的去向和 OpenAI 的 Agent 戰略
- [China issues second warning on OpenClaw risks — South China Morning Post](https://www.scmp.com/tech/tech-trends/article/3346138/china-issues-second-warning-openclaw-risks-amid-adoption-frenzy)：中國官方對 OpenClaw 安全風險的態度和監管走向
- [The $1 Trillion Software Carnage — FinancialContent](https://markets.financialcontent.com/stocks/article/marketminute-2026-2-24-the-1-trillion-software-carnage-how-ai-agents-broke-the-saas-model)：一兆美元軟體市值蒸發的完整數據分析
