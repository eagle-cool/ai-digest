---
title: "當 14 億人的通訊錄出現第一個 AI：微信開門養蝦背後的平台戰爭"
date: 2026-03-23
description: "微信正式推出 ClawBot 插件，14 億用戶的通訊錄首次出現非人類聯繫人。這不只是一個功能更新，而是全球通訊平台 AI 入口爭奪戰的關鍵一步——誰控制了對話框，誰就掌握了下一代 AI 的分發權。"
tags: [deep-dive, agents, ai-tools, ai-industry]
---

## 引言

想像一下這個場景：你打開微信通訊錄，在「文件傳輸助手」旁邊，多了一個叫「ClawBot」的聯繫人。它不是你的同事，不是你的朋友，甚至不是一個人——它是一隻龍蝦，一個 AI Agent 的遙控器。

這件事在 2026 年 3 月 22 日真的發生了。

微信公開課發文宣布正式推出 ClawBot 插件，用戶可以在微信聊天界面直接連接自己的 OpenClaw，調用 AI 能力執行任務。對於一個連改版都會上熱搜的產品來說，在通訊錄裡塞進一個「非人類存在」——這動作的意義，遠超過功能本身。

微信誕生十五年來，通訊錄裡的每一個條目都對應一個真實的人。ClawBot 打破了這個前提。從「連接人與人」到「連接人與 AI」，這不是一句行銷口號，而是一次底層敘事的靜默改寫。

但如果你以為微信這次大開城門、擁抱 AI 時代，那你又想多了。ClawBot 不能進群、不能讀你的朋友圈、不能叫外賣、不能碰微信生態裡的任何數據——它就是一條從微信到你電腦上那隻蝦的消息通道，僅此而已。

門是開了，但只開了一條縫。

這篇報導的起點是 36 氪的兩篇分析文章：[〈微信正式向"龍蝦"開門，但只開了一條縫〉](https://www.36kr.com/p/3734838062772736)和[〈關於微信接入 OpenClaw 的 10 條冷思考〉](https://www.36kr.com/p/3733780366999554)，但故事遠不止於此。

---

## 事件全貌

### 腾讯的全線出擊

3 月 22 日 ClawBot 上線之前，騰訊已經在 Agent 戰場上打了大半個月的密集戰。

3 月 6 日，騰訊在深圳總部門口擺攤，免費幫人安裝 OpenClaw，隊伍從北廣場排到馬路對面——[超過一千人排隊](https://www.cnbc.com/2026/03/12/china-openclaw-ai-agent-adoption-tech-companies-government-support-lobster-shrimp.html)，場面堪比 iPhone 首賣日。3 月 11 日凌晨，馬化騰在朋友圈亮出家底：「自研龍蝦、本地蝦、雲端蝦、企業蝦、雲桌面蝦……還有一批產品陸續趕來。」

接下來的兩週，騰訊各事業部的龍蝦產品密集亮相：面向個人用戶的 QClaw、面向開發者的 Lighthouse（騰訊雲「養蝦車間」）、面向企業的 WorkBuddy，加上 SkillHub 技能社區，一張完整的 Agent 產品矩陣在短短十天內搭建完成。

但所有人都知道，真正的王牌還沒出。

元寶、QQ、企業微信雖然都接了 OpenClaw，但它們的體量和微信不在同一個量級。騰訊安全管家推出的 QClaw 雖然透過服務號和小程序實現了「微信直連」，但那終究不是官方正規通道。大家在等的，是張小龍什麼時候點頭。

### ClawBot：戰略卡位而非功能爆發

3 月 22 日，靴子落地。微信以插件形式推出 ClawBot，iOS 8.0.70 及以上版本的用戶可以直接在插件中心找到入口。安裝完成後，ClawBot 作為一個聯繫人出現在通訊錄裡，與「文件傳輸助手」並列——這個產品決策本身就是一個信號。

根據[多方報導](https://www.ithome.com/0/931/382.htm)，ClawBot 目前的能力邊界非常清晰：

- **支持**：連接本地或雲端的 OpenClaw、文字和文件傳輸、斜線快捷命令
- **不支持**：進入群聊、微信生態數據存取、流式輸出、多隻蝦同時連接、轉發他人對話、Mac 端（暫時）

這些限制共同指向一個結論：ClawBot 是戰略佔位，不是功能競爭。它的核心任務是——讓「微信裡有 AI」這件事，從新聞變成日常。

ClawBot 上線當天，QClaw 的「微信直連」亮點瞬間被覆蓋。距離 QClaw 全量公測才過了兩天——這是騰訊「賽馬機制」的典型結局：外圍產品先試水溫，驗證完需求和安全邊界後，微信收割。

---

## 脈絡

### 從二維碼到 AI：微信的三次平台躍遷

要理解 ClawBot 的意義，得先理解微信作為平台的進化史。

**第一次躍遷（2013）：微信支付。** 從純粹的通訊工具變成生活基礎設施。

**第二次躍遷（2017）：小程序。** 張小龍構想的「即用即走」輕應用生態，[最終長成了一個擁有超過 600 萬個小程序、9.45 億月活用戶的巨型平台](https://www.demandsage.com/wechat-statistics/)。到 2021 年，小程序年交易額突破 4000 億美元。微信從此不只是 App，它成了 App Store 的替代品——一個 App 裡的 App 生態系。

**第三次躍遷（2026）：AI Agent 入口。** ClawBot 的出現，標誌著微信開始從「連接人與服務」走向「連接人與 AI」。

這三次躍遷有一個共同的模式：微信從不做第一個吃螃蟹的，但每次入局，都是在基礎設施層面改變遊戲規則。

二維碼不是微信發明的，但 2012 年微信加入「掃一掃」之後，二維碼從極客玩具變成了全民基礎設施。小程序也不是微信首創的概念，但微信把它做成了全球最大的小程序生態。現在，AI Agent 同樣不是微信的發明——但當 14 億月活的超級 App 正式接入，「養蝦」這件事的意義就完全不同了。

### OpenClaw 在中國的瘋狂擴散

要理解微信為什麼「不得不做」，得看 OpenClaw 在中國的擴散速度。

根據[美國網路安全公司 SecurityScorecard 的數據](https://intellectia.ai/news/etf/chinas-openclaw-craze-surpasses-us-adoption)，中國的 OpenClaw 使用量已經超過美國。截至 2026 年 3 月，OpenClaw 在 GitHub 上累積了超過 24.7 萬顆星星，成為歷史上成長最快的開源 AI Agent。

更關鍵的是，中國的各級政府都在推波助瀾。深圳和合肥的地方政府為採用 OpenClaw 的企業提供最高一千萬人民幣的股權融資支持。百度把 OpenClaw 整合進了 7 億用戶的搜索 App，阿里巴巴推出了企業級 Agent 平台「悟空」，字節跳動的飛書更是把「一鍵養蝦」做成了核心賣點。

在這種全民養蝦的氛圍下，微信如果不做，反而會被視為反常。業界甚至已經有人把微信和蘋果放在一起比較——蘋果的 AI 進展遲遲拿不出能用的東西，讓人著急。微信至少踏出了這一步。

但也有人把「速度」這個問題看得更透。衛夕計算過：去年 DeepSeek 大火時，微信搜索在 20 天內就接入了 DeepSeek。這次從 OpenClaw 春節爆紅算起，微信花了超過一個月才出手。當然，動搜索和動通訊錄，是完全不同量級的決策。搜索出錯，最多是搜到些奇怪的東西；通訊錄出錯，那是社交關係鏈的信任崩塌。

正如那篇冷思考文章所說：「你不做，對其他做了的 IM 是加成作用；你做了，對自己有多大提升，打個問號。你已經是基礎設施了。」

---

## 多方觀點

### 「微信終結比賽」派

ClawBot 上線當天，朋友圈再次出現了「微信終結比賽」的虎狼之詞。支持者的邏輯很簡單：微信有 14.11 億月活用戶，這個量級碾壓一切。飛書管工作，但微信管生活——你的家人、朋友、日常消費、生活服務全都沉澱在微信裡。一旦 AI Agent 從工具升級成入口，微信的社交護城河就是最深的護城河。

[騰訊總裁劉熾平在財報電話會上的表態印證了這個方向](https://www.scmp.com/tech/big-tech/article/3347023/chinas-tencent-meets-expectations-fourth-quarter-results-ai-wave-lifts-all-boats)：「我們的下一步是基於微信多元的生態——小程序、內容、電商、社交和支付——來打造 Agent。」

更重要的是，誰佔了入口，誰就能拿到最真實的用戶交互數據。哪怕不談訓練模型，那些真實的對話和行為反饋本身就是頂級數據資產。

### 「別太興奮」派

另一個陣營的聲音更冷靜。科技博主衛夕在他的十條冷思考中，直接給這股熱潮潑了一盆冷水：

> 微信降低的是跟蝦聊天的門檻，並不是養蝦的門檻本身。

他指出，元寶其實早就原生支持了微信，但大部分人還是習慣去打開元寶的 App 或是用豆包。技術圈的人覺得天都變了，普通用戶覺得啥也沒發生——二八法則永遠生效。

目前真正在養蝦的人，在微信 14 億用戶裡佔比微乎其微。養好一隻蝦需要的不只是一個聊天入口，還需要選對模型、設定好 soul.md 和 user.md、理解 Agent 的能力邊界——這些都是「道」層面的東西，不是微信插件能解決的。

### 飛書陣營：深度整合才是真正的護城河

如果說微信是廣度之王，飛書就是深度之王。

根據 OpenClaw-China 社區 3 月 11 日的週報數據，飛書在中國所有 IM 工具裡的 Agent 接入率達到 65.2%，遙遙領先。3 月 19 日推出的 [aily](https://www.qbitai.com/2026/03/389311.html)，是深度融合於飛書底座的原生 Agent 平台，可以直接調用飛書全量工作上下文——文檔、日程、群聊消息、業務優先級——這種深度原生能力，是外部接入的 OpenClaw 無法複製的。

飛書的邏輯是：你在哪個平台留下了最多的工作痕跡，那個平台的 Agent 就最懂你，也就最好用。字節隨即系統性放大這個先發優勢——API 調用額度提高到每月 100 萬次，官方插件全面對接火山引擎、Kimi、MiniMax、智谱等主流模型。

但飛書的天花板也很明確：它的用戶基盤受限於職場圈層。工作可以切換 App，生活更難遷移。而且飛書在中國的市場份額遠不如釘釘和企業微信——它的 Agent 接入率高，部分原因是它的用戶本身就是對新技術接受度最高的那群人。這是一個典型的「在自己的舒適區裡領先」的情況。

另外，阿里巴巴也沒閒著。3 月 17 日推出的企業級 Agent 平台[「悟空」](https://techstartups.com/2026/03/17/alibaba-launches-wukong-ai-agent-platform-to-unify-enterprise-workflows-across-slack-teams-and-wechat/)，定位是跨平台的 Agent 協調層——可以橫跨 Slack、Microsoft Teams 和微信，在單一介面內處理文檔編輯、會議轉錄等複雜企業任務。阿里的算盤是：不管你用什麼通訊平台，我的 Agent 都能服務你。這和微信、飛書的「平台鎖定」邏輯截然不同。

### 全球視角：Meta 選了相反的路

有意思的是，在全球範圍內，另一個超級通訊平台選了完全相反的策略。

2025 年 10 月，Meta 修改 WhatsApp Business API 政策，[禁止 OpenAI、Perplexity 等第三方 AI 聊天機器人使用 WhatsApp 的商業工具](https://techcrunch.com/2025/12/04/eu-investigating-meta-over-policy-change-that-bans-rival-ai-chatbots-from-whatsapp/)。2026 年 1 月政策生效後，只有 Meta AI 被允許在平台上運行。

歐盟隨即[展開反壟斷調查](https://ec.europa.eu/commission/presscorner/detail/en/ip_25_2896)，認為這一政策「可能對市場造成嚴重且不可逆的傷害」。義大利和巴西也下達了暫停令。如果罪名成立，Meta 可能面臨年營收 10% 的罰款。

在多方壓力下，Meta 在 2026 年 3 月 5 日[讓步](https://almcorp.com/blog/meta-whatsapp-rival-ai-chatbots-eu/)，同意在歐盟開放 WhatsApp 給競爭對手的 AI 機器人——但引入了按消息收費的定價模型，競爭對手直斥這是「用另一種方式複製禁令效果」。

這形成了一個鮮明的對比：

| | 微信 (ClawBot) | WhatsApp (Meta AI) |
|---|---|---|
| 策略 | 開放接入所有兼容 OpenClaw 的蝦 | 僅允許 Meta AI，封殺第三方 |
| 商業模式 | 平台思維，不做蝦做連接 | 圍牆花園，AI 是私有資產 |
| 監管壓力 | 無（中國政府鼓勵 Agent 普及） | 歐盟反壟斷、多國暫停令 |
| 生態效果 | 做大整個蛋糕 | 壟斷自己的蛋糕 |

### 我的看法

我覺得兩邊的極端派都錯了。

「終結比賽」派低估了養蝦的認知門檻——你不能指望 14 億人突然都開始配置 soul.md。「沒啥影響」派則低估了佔位的長期價值——2012 年微信加入掃一掃的時候，也沒人覺得二維碼能改變什麼。

ClawBot 真正的價值不在於它「現在能做什麼」，而在於它讓一件事變得正常：你的通訊錄裡可以有一個不是人的存在。一旦這個認知被建立，後續的每一步開放——進群、讀消息、調用小程序——都不再是驚天動地的越界，而是順理成章的延伸。

張小龍的套路一向如此：先讓你覺得正常，再讓你覺得好用。

---

## 產業衝擊

### 第一層：通訊平台的 AI 入口之爭

[Agentic AI 市場預計到 2034 年將達到 1,960 億美元](https://beam.ai/agentic-insights/tencent-launches-qclaw-what-the-ai-agent-mainstream-moment-means-for-enterprise)——而通訊平台正是這個市場的核心戰場。ClawBot 上線標誌著全球通訊平台 AI 入口爭奪戰進入白熱化。

目前的格局已經相當清晰。[根據一份產業分析](https://www.casys.ai/blog/ai-moves-to-messaging)，全球主要通訊平台在 AI Agent 接入上分為三個陣營：

- **開放派**：Telegram（5 億日活，對 AI bot 零限制）、KakaoTalk（[已發布 PlayMCP，首個在 production 環境中運行 MCP 原生 AI 工具的通訊平台](https://www.casys.ai/blog/ai-moves-to-messaging)）
- **有限開放派**：微信（ClawBot 插件，但功能受限）、LINE（訂閱制 AI 功能）
- **封閉派**：WhatsApp（封殺第三方，僅允許 Meta AI）

[Manus 在 2 月就已經在 Telegram 上推出了個人 AI Agent](https://siliconangle.com/2026/02/16/manus-launches-personal-ai-agents-telegram-messaging-apps-come/)，並宣布更多平台即將跟進。這意味著 Agent 的分發渠道正在從專用 App 轉移到用戶已經在的地方。

WhatsApp 有 23 億日活用戶，是 ChatGPT 的 27 倍。當 AI 必須「去人在的地方」而不是要求人來找 AI，通訊平台就變成了 AI 的分發層。誰控制了對話框，誰就掌握了下一代 AI 的分發權。

### 第二層：商業模式的重新定義

這場爭奪戰正在重塑通訊平台的商業模式邏輯。

微信選擇了「遙控器」模式——它不做蝦，只做連接。你在微信裡發指令，蝦在電腦或雲端執行，結果回傳微信，微信本身的數據邊界紋絲不動。這是典型的平台思維：不與生態夥伴競爭，而是讓所有人都依賴你。

但微信的克制背後，有一個更大的佈局。[根據 The Information 的報導](https://technode.com/2026/03/11/tencent-is-said-to-be-developing-a-top-secret-ai-agent-project-for-wechat/)，騰訊從 2025 年就開始秘密研發微信原生 AI Agent，計劃與微信內數百萬個小程序深度連接，覆蓋打車、訂餐、購物等全生活場景，2026 年年中開始灰度測試。

有趣的是，[微信團隊甚至還沒決定要用騰訊自研的混元模型，還是外部模型](https://www.scmp.com/tech/big-tech/article/3347023/chinas-tencent-meets-expectations-fourth-quarter-results-ai-wave-lifts-all-boats)——他們已經測試了智谱、阿里、DeepSeek 等多家廠商的模型。這種「模型不可知論」的態度，恰恰說明微信認為自己的核心資產不在模型，而在生態。

微信的 600 萬個小程序、9.45 億小程序月活用戶、橫跨出行、餐飲、電商、支付的完整服務鏈——這才是護城河。一旦原生 AI Agent 上線，能夠直接調度這些小程序能力，那才是「滿血版」的微信 AI，是任何第三方蝦都無法複製的體驗。

ClawBot 和未來的原生 Agent 在邏輯上幾乎沒有重疊：ClawBot 解決的是當下已經養蝦的用戶的即時需求，同時完成認知預熱；原生 Agent 才是微信 AI 能力的系統性釋放。前者是過渡形態，後者是終局佈局。

### 第三層：開發者生態的分化

對開發者而言，這場平台戰爭意味著一個關鍵選擇：押注哪個生態？

目前的狀況是碎片化嚴重。Claude Code、OpenAI、LangChain、CrewAI、AutoGen——每個框架定義 Agent 的方式都不同，同樣的 Agent 邏輯要針對不同框架反覆重寫。微信的 ClawBot 至少做了一件好事：它支持所有兼容 OpenClaw 協議的蝦，而不是只支持騰訊自家的。

但這個「中立」能維持多久？當微信自己的原生 Agent 上線，它的入口位置、推廣資源、在微信介面裡的優先級，大概率會比 OpenClaw 的蝦高得多。畢竟是「親兒子」。

開發者面臨的不只是技術選型問題，而是生態站隊問題。在飛書做深度整合？在微信做輕量接入？還是走 Telegram 的完全開放路線？每個選擇背後都是不同的商業邏輯和用戶觸達方式。

### 第四層：二階效應——AI 安全與社交信任

ClawBot 不開放群聊功能，不是技術做不到——「從技術角度，加上群聊是分分鐘的事。」真正的原因是安全。

一旦 AI Agent 進入群聊，各種 prompt injection 攻擊、社會工程手段就會層出不窮。有人會想辦法 hack 你的蝦，讓它洩露敏感資訊或執行惡意操作。對微信來說，14 億人的社交關係鏈是核心資產，也是阿喀琉斯之踵。

[Bloomberg 的報導也指出](https://www.bloomberg.com/news/articles/2026-03-12/openclaw-frenzy-drives-china-s-agentic-ai-adoption-raises-security-concerns)，中國當局已經加強了對 OpenClaw 安全和數據風險的警告，並指示銀行等敏感行業的政府機構和企業限制使用。這是一個微妙的矛盾：政府一方面補貼推廣 OpenClaw，另一方面又在收緊安全管控。

這個矛盾在微信身上體現得最為集中。微信可能是世界上最不能出安全事故的 App——任何涉及用戶隱私或社交關係鏈的事故，都可能是系統性風險。所以微信寧可被罵「閹割」，也不會冒險讓 AI Agent 觸碰核心數據。

---

## 未來展望

### 短期（3-6 個月）：灰度測試與模型卡位

幾乎確定會發生的事：

- **微信原生 AI Agent 灰度測試**：根據多方報導，2026 年年中啟動測試。這將是真正的分水嶺——一個能調度 600 萬個小程序的 AI 助手，對用戶體驗的衝擊將遠超 ClawBot。
- **騰訊混元 3.0 (HY 3.0) 發布**：[計劃 4 月發布](https://www.caixinglobal.com/2026-03-18/tencent-to-launch-hunyuan-30-in-april-build-wechat-ai-agent-102424421.html)，由前 OpenAI 研究員姚順雨主導。但微信是否採用，仍是未知數。
- **ClawBot 功能逐步開放**：Android 支持、Mac 端支持、多蝦連接等功能大概率會陸續上線。但群聊功能短期內不太可能開放。
- **騰訊 AI 投入翻倍**：[2026 年至少投入 360 億人民幣](https://phemex.com/news/article/tencent-to-double-ai-investment-to-over-36-billion-yuan-in-2026-67270)，是 2025 年 180 億的兩倍。但摩根士丹利仍認為騰訊的投資規模不及阿里巴巴 3800 億以上的計劃。

### 中期（6-18 個月）：三種可能的格局

**情境一：微信一統天下。** 原生 AI Agent 成功上線，深度打通小程序生態，讓用戶在微信裡用一句話完成打車、點外賣、買機票。飛書和其他 IM 的 Agent 接入率開始下滑，因為生活場景的黏性遠大於工作場景。微信成為中國 AI Agent 事實上的分發平台。

**情境二：各據山頭。** 微信在生活場景稱王，飛書在職場場景守擂，Telegram 在技術社群保持影響力。不同平台的 Agent 無法互通，用戶被迫在多個平台間切換。Agent 生態碎片化加劇，開發者苦不堪言。

**情境三：協議標準化。** OpenClaw 的成功催生了 Agent 通訊協議的標準化。就像 HTTP 統一了 Web、SMTP 統一了 Email，一個統一的 Agent 協議讓用戶不管在哪個平台都能調用同樣的 Agent 能力。平台之間的競爭從「誰能跑通」轉向「誰的體驗最好」。

以我的判斷，短期內最可能出現的是情境二，中期會向情境一或情境三演進——取決於微信的原生 Agent 做得有多好，以及開放生態的壓力有多大。

### 長期推演：3-5 年後的世界

如果這個趨勢持續下去，我們正在見證的是一場「入口大遷移」。

過去十年，移動互聯網的入口是 App Store。你要觸達用戶，就得做一個 App，上架審核，爭搶排名。下一個十年，入口可能就是對話框。你不再需要讓用戶下載你的 App，只需要讓 AI Agent 在用戶的對話框裡幫你完成服務。

這意味著：

- **App 的定義會改變。** 小程序可能進一步縮水成「技能」（Skill），被 Agent 在後台自動調用，用戶甚至不需要知道它的存在。
- **搜尋引擎的價值會被稀釋。** 如果你可以直接告訴 Agent「幫我訂明天下午三點從台北到東京的機票」，你為什麼還要打開 Google？
- **平台的護城河會從「用戶量」變成「上下文密度」。** 誰擁有最豐富的用戶上下文（對話紀錄、消費習慣、社交關係、地理位置），誰的 Agent 就最好用。

### 給讀者的行動建議

**如果你是開發者**：現在最重要的不是選邊站，而是確保你的 Agent 邏輯是「協議不可知」的。用 OpenClaw 協議作為基礎，讓你的 Agent 可以在任何平台上運行。別把命運綁死在某一個平台上——2017 年把命綁在微信小程序上的開發者，當年不少被規則變動搞得很慘。

**如果你是創業者或產品經理**：如果你的產品還在做獨立 App，認真想想是不是該做成一個「可被 Agent 調用的服務」。下一波 PMF 可能不是「用戶願意下載你的 App」，而是「Agent 願意調用你的 API」。

**如果你是一般科技從業者**：現在開始認真養一隻蝦吧。不是為了趕流行，而是為了理解 AI Agent 的能力邊界。你不需要會寫程式，但你需要學會如何有效地把工作分配給 AI——這是未來兩三年內最重要的職場技能之一。微信接入 ClawBot 降低了你跟蝦溝通的門檻，但真正的價值在於你願意把多少事情交給它去做。

最後，回到微信通訊錄裡那個新出現的聯繫人。它現在還很笨，功能閹割得厲害，大部分人用了一下就放在那裡積灰。但十年後回看，這個看似無關痛癢的時刻，可能就是微信從「人與人的連接」走向「人與 AI 的連接」的起點。

就像 2012 年的掃一掃。

龍哥向來不急，但每一步都挺準。

---

## 延伸閱讀

- [Tencent Secretly Develops WeChat AI Agent — TechNode](https://technode.com/2026/03/11/tencent-is-said-to-be-developing-a-top-secret-ai-agent-project-for-wechat/)：The Information 獨家報導的微信內部 AI Agent 計畫，揭露了原生 Agent 的野心和時間表
- [Tencent Pledges Higher AI Investment — South China Morning Post](https://www.scmp.com/tech/big-tech/article/3347023/chinas-tencent-meets-expectations-fourth-quarter-results-ai-wave-lifts-all-boats)：騰訊財報電話會上劉熾平談 AI 戰略，包含微信 Agent 和混元模型的最新方向
- [AI Is Moving to Your Messaging App — Casys.ai](https://www.casys.ai/blog/ai-moves-to-messaging)：全球通訊平台 AI 整合的全景分析，對比了 WhatsApp、Telegram、KakaoTalk、LINE 和微信的策略差異
- [EU Opens Antitrust Investigation into Meta — European Commission](https://ec.europa.eu/commission/presscorner/detail/en/ip_25_2896)：歐盟對 Meta 封殺 WhatsApp 第三方 AI 的反壟斷調查，是理解「封閉 vs 開放」策略的重要參考
- [China's OpenClaw Craze Surpasses US Adoption — Bloomberg](https://www.bloomberg.com/news/articles/2026-03-12/openclaw-frenzy-drives-china-s-agentic-ai-adoption-raises-security-concerns)：中國 OpenClaw 採用率超越美國的報導，同時揭露了安全隱憂和監管動態
- [Four Key Product Principles from WeChat's Creator — a16z](https://a16z.com/four-key-product-principles-from-wechats-creator/)：a16z 整理的張小龍產品哲學，理解「先讓你覺得正常，再讓你覺得好用」的微信方法論
- [Tencent to Launch Hunyuan 3.0 in April — Caixin Global](https://www.caixinglobal.com/2026-03-18/tencent-to-launch-hunyuan-30-in-april-build-wechat-ai-agent-102424421.html)：騰訊混元 3.0 的發布計畫，以及微信 Agent 團隊在模型選擇上的「不可知論」態度
