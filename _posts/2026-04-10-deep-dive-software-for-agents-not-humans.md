---
title: "當軟體的使用者不再是人類：萬億智能體時代的生存法則"
date: 2026-04-10
description: "Neon 資料庫 80% 由 AI Agent 自動建立、SaaS 市值一個月蒸發 2 兆美元——當軟體的主要使用者從人類變成智能體，整個軟體產業的設計邏輯、定價模型和基礎設施都在被重寫。"
tags: [deep-dive, agents, ai-tools, ai-industry, ai-coding]
---

## 引言

想像一下這個畫面：你登入公司的資料庫管理後台，發現上個月新建的幾百個資料庫裡，只有不到兩成是你的同事建的——其餘八成，全是 AI Agent 自己建的。

這不是科幻小說的場景。根據 Neon（被 Databricks 以約 10 億美元收購的 Serverless Postgres 平台）的內部遙測數據，[他們平台上超過 80% 的資料庫是由 AI Agent 自動建立的](https://www.databricks.com/company/newsroom/press-releases/databricks-agrees-acquire-neon-help-developers-deliver-ai-systems)，而不是人類開發者。這個數字在一年前還只有 30%。

讓這個數據沉澱一下。

我們花了幾十年在爭論什麼框架最好、什麼 ORM 最順手、什麼資料庫介面最人性化——結果現在最大的使用者根本不在乎你的 UI 長什麼樣。它們不需要精美的儀表板，不需要拖拉式的視覺化介面，甚至不需要登入頁面。它們只需要一個乾淨的 API、一個穩定的端點、和一份寫得清楚的文件。

Box 的 CEO Aaron Levie 在三月初把這件事說得最直白——他在 X 上發了一篇長文，核心論點只有一句話：**「智能體將成為未來所有軟體的主要使用者。」** 他把 Paul Graham 那句經典的 YC 口號「做出大家想要的東西」（Make Something People Want）改寫成了這個時代的版本：**Make Something Agents Want**——做出智能體想要的東西。

這篇報導的起點是[36氪編譯的一篇分析文](https://www.36kr.com/p/3759555759370757)，但故事遠不止於此。當整個軟體產業的「客戶」從人類變成機器，衝擊的不只是產品設計，而是定價模型、基礎設施、開發者的技能樹、甚至軟體公司的存亡。

---

## 事件全貌

### 一個 CEO 的預言，還是一個產業的現實？

Levie 的論述並不是空穴來風。他經營的 Box 是一家企業級雲端儲存和內容管理平台，而他們正在第一線感受到這個轉變：越來越多存取 Box 檔案的「使用者」不是人類員工，而是代替員工工作的 AI Agent。

他的核心觀點可以拆成三層：

**第一層：API 優先，否則你不存在。** 如果你的軟體功能沒有提供 API，那對智能體來說，這個功能就等於不存在。不能透過命令列介面（CLI）或 Model Context Protocol（MCP）伺服器暴露出來的能力，就是你的競爭劣勢。更致命的是——如果你的 API 設計混亂，給智能體提供了互相矛盾的執行路徑，你就是在主動把客戶推向競爭對手。

Y Combinator 的 Jared Friedman 補了一刀：「即使是最好的開發者工具，大多數仍然不支援透過 API 註冊帳號。在 Claude Code 時代，這是一個重大失誤——因為 Claude 沒辦法自己註冊。」

想想看。你的產品連讓 AI 自己開帳號都做不到，那在智能體的世界裡，你基本上出局了。

**第二層：定價模型即將崩盤。** 一個智能體可以在幾秒鐘內完成人類幾小時的工作，然後只把最終結果呈現給終端使用者。如果你的商業模式是按人頭收費（per-seat），那當一個 AI Agent 取代了 10 個人的工作量時，你的營收就直接砍掉 90%。

**第三層：智能體需要自己的基礎設施。** 就像人類使用者需要電腦、瀏覽器、作業系統，智能體也需要自己的沙盒環境、身份系統、通訊協議、甚至支付錢包。這不是什麼遙遠的未來——這些東西已經在被建造了。

NVIDIA 的 Jensen Huang 從另一個角度佐證了同樣的觀點：AI Agent 已經足夠聰明，可以代替人類使用軟體工具來提升生產力。他認為軟體的使用量不會因此減少，反而會*增加*——因為每個組織都會部署大量智能體。

### 數據說話

讓我們看看這個轉變有多真實：

- **Neon 資料庫**：80% 由 AI Agent 建立（一年前僅 30%）
- **GitHub 提交**：目前約 4% 由 Claude Code 撰寫，預計年底達 20% 以上
- **非人類身份**：企業中每位人類員工對應 144 個非人類身份（2024 年初為 92:1）
- **AI 原生平台**：每天有超過 10 萬個產品在 Cursor、Replit、Lovable、Bolt.new 等平台上被建立
- **自主工作時間**：Agent 的自主工作持續時間從 2024 年初的 4 分鐘，延長到 2026 年 2 月的 14.5 小時

這不是趨勢預測，這是已經在發生的事。

---

## 脈絡

### 軟體典範轉移簡史

回顧軟體產業的每一次典範轉移，核心問題都是同一個：**「誰在用這個軟體？」**

1960-70 年代，答案是「穿白袍的電腦科學家」——軟體為大型主機而寫，使用者是少數菁英。1980 年代 PC 革命後，答案變成「坐在桌前的辦公室員工」——GUI 誕生了，因為普通人需要看得懂的介面。2000 年代網路時代，答案變成「任何有瀏覽器的人」——軟體變成服務（SaaS），用戶數從萬級跳到億級。2010 年代行動時代，答案是「口袋裡有手機的每個人」——觸控介面、推播通知、App Store 生態隨之而來。

2026 年，答案正在變成：**「不是人。」**

每一次轉移都重新定義了軟體該長什麼樣、怎麼賣、怎麼分發。而這一次的轉移可能是最劇烈的——因為機器不需要漂亮的 UI，不需要新手引導流程，不會被行銷文案打動，也不會因為品牌忠誠度而留下來。它們只選最好用的 API。

### 協議戰爭：MCP、A2A 與新秩序

要理解智能體如何「使用」軟體，得先理解它們的溝通方式。2026 年的 AI Agent 協議生態正在快速成形：

**MCP（Model Context Protocol）** 是 Anthropic 在 2024 年 11 月推出的開放標準，定義了 AI 系統如何連接外部工具和資料。它的採用曲線堪稱瘋狂：從推出時的每月 200 萬次 SDK 下載，到 OpenAI 在 2025 年 4 月加入（2,200 萬），Microsoft 在 7 月跟進（4,500 萬），AWS 在 11 月加入（6,800 萬），到 [2026 年 3 月已突破 9,700 萬次月下載](https://www.cdata.com/blog/2026-year-enterprise-ready-mcp-adoption)，活躍的公開 MCP 伺服器超過 10,000 個。

**A2A（Agent-to-Agent Protocol）** 則解決另一個問題：智能體之間怎麼對話。Google 在 2025 年 4 月推出這個協議，隨後 IBM 的 ACP（Agent Communication Protocol）在 2025 年 8 月[正式合併進 A2A](https://www.ibm.com/think/topics/agent2agent-protocol)，統一在 Linux 基金會旗下。技術指導委員會的成員包括 Google、Microsoft、AWS、Cisco、Salesforce、ServiceNow 和 SAP——基本上就是企業軟體的半壁江山。

一句話總結這個格局：**MCP 是智能體使用工具的方式，A2A 是智能體互相協作的方式。** 前者解決「Agent 怎麼用你的軟體」，後者解決「Agent 怎麼跟別的 Agent 配合」。兩者加在一起，構成了智能體時代的 TCP/IP。

### 推論成本暴跌的推力

另一個讓這一切成為可能的關鍵因素：AI 推論成本在三年內[暴跌了 92%](https://meditations.metavert.io/p/the-state-of-ai-agents-in-2026)——從 2023 年初的每百萬 token 30 美元，降到 2026 年 2 月的 0.10-2.50 美元。當一個智能體完成一個任務的成本從幾美元降到幾分錢，大規模部署就從「算得過帳」變成了「不用不是傻子」。

這就是為什麼「萬億智能體」的說法並不誇張。IDC 預測 G2000 企業的 [Agent 使用量將在 2027 年增長 10 倍](https://joget.com/ai-agent-adoption-in-2026-what-the-analysts-data-shows/)，相關的 API 呼叫負載將增長 1,000 倍。

---

## 多方觀點

### 樂觀派：這是軟體的黃金時代

Jensen Huang 代表的是最樂觀的那一派。他的邏輯很簡單：AI Agent 不會消滅軟體需求，反而會把它推到前所未有的高度。每個組織裡的每個員工都會有多個替自己工作的 Agent，一家公司的 Agent 數量可能是員工人數的 100 到 1,000 倍。軟體的使用量會暴增，只是使用者的身份從人類換成了機器。

E2B 的數據支持這個觀點。這家提供 AI Agent 雲端沙盒的公司表示，[88% 的 Fortune 100 企業已經註冊使用他們的 Agentic 工作流程平台](https://e2b.dev/blog/series-a)。他們最近完成了 2,100 萬美元的 A 輪融資，核心賣點就是一句話：「在未來，伺服器農場不再為我們的應用服務，而是為我們的智能體服務。」

McKinsey 的估算更驚人：AI Agent [可能每年為全球商業創造 2.6 兆到 4.4 兆美元的價值](https://joget.com/ai-agent-adoption-in-2026-what-the-analysts-data-shows/)。

### 質疑派：野心勃勃，過度炒作，仍在訓練中

但另一邊的聲音同樣尖銳。多家美國媒體在年初刊出了一篇廣泛轉載的評論文章，標題就叫[《認識 2026 年的 AI Agent——野心勃勃、過度炒作、仍在訓練中》](https://lasvegassun.com/news/2026/jan/03/meet-the-ai-agents-of-2026-ambitious-overhyped-and/)。文中指出：

> 「這些系統仍然不可靠、脆弱，並且高度依賴人類監督。它們更像是動作很快、自信滿滿但經常出錯的初級員工，需要持續的檢查和善後。」

文章認為，「把 Agent 當作自主工人而非工具，是一個分類錯誤（category error），2026 年將使這一點越來越明顯。」

數據也有支撐。一個 95% 可靠的單步驟操作，在連續 20 個步驟後成功率會衰減到 36%——這就是所謂的「可靠性複利問題」。Gartner 更直接預警：[超過 40% 的 Agentic AI 專案將在 2027 年底前被取消](https://joget.com/ai-agent-adoption-in-2026-what-the-analysts-data-shows/)，原因是治理失敗、投資回報不清、成本失控。

最刺眼的一個數字：儘管全球 AI 總支出已達 1.5 兆美元，2025 年的創投投入達 2,110 億美元，但**只有 6% 的組織報告 AI 帶來了超過 5% 的 EBIT 影響**。

### 實務工作者的前線觀察

Gartner 的一項預測特別值得注意：2026 年底前，[40% 的企業應用將搭載任務型 AI Agent](https://joget.com/ai-agent-adoption-in-2026-what-the-analysts-data-shows/)，而 2025 年這個數字還不到 5%。這意味著在未來八個月內，大量軟體產品將被「Agent 化」——不管它們準備好了沒有。

治理是最大的痛點。企業中每位員工對應 144 個非人類身份，但能夠有效治理這些 Agent 的企業不到 10%。換句話說，大多數公司已經放了一大堆 Agent 出去工作，但根本不知道它們在做什麼、存取了什麼資料、會不會犯下代價高昂的錯誤。

### 我的看法

說真的，兩邊都有道理，但我更傾向於一個中間偏樂觀的判斷：**轉變是真的，但速度會比樂觀派預期的慢，影響卻比質疑派承認的深。**

質疑派說得沒錯，現在的 Agent 還不夠可靠，20 步驟後只剩 36% 成功率確實嚇人。但他們忽略了一件事——14.5 小時的自主工作時間，是在模型每幾個月就大幅進步的背景下達成的。這條曲線還在陡峭上升。

真正的問題不是「Agent 能不能取代人類使用軟體」，而是**「軟體產業是否有足夠的時間完成轉型」**。答案是：很多公司沒有。

---

## 產業衝擊

### 第一層：SaaS 定價模型的生死存亡

這是最直接、最痛的衝擊。

2026 年 1 月，全球 SaaS 市值在一個月內[蒸發了 2 兆美元](https://meditations.metavert.io/p/the-state-of-ai-agents-in-2026)。催化劑之一是 Anthropic 推出 Claude Cowork，讓投資人開始認真質疑 per-seat 定價模式的可持續性——當一個 Agent 能做十個人的事，誰還要買十個 seat？

[按 PinkLime 的分析](https://pinklime.io/blog/future-saas-pricing-ai-era)，seat-based 模型有三個致命弱點：

1. **量體崩潰**：客戶用 AI 變高效後需要更少的 seat，50 人做 100 人的事但只買 50 個 seat
2. **價值錯配**：一個用 AI 增強的 power user 創造 10 倍價值，但付一樣的錢
3. **指標倒錯**：用 AI 最成功的公司反而縮減人數，導致 SaaS 營收下降——完全反向

替代方案正在快速成形。目前 [43% 的 SaaS 公司已採用混合定價](https://editorialge.com/saas-trends-q1/)（基礎費用 + 用量或成效計費），預計年底將達 61%。Intercom 的 $0.99/已解決工單就是一個典型的 outcome-based 模式，據報告客戶留存率提高了 31%。

但消費型定價也帶來新問題：[78% 的 IT 主管](https://zylo.com/blog/ai-cost/) 反映 SaaS 出現了意外的消費型帳單——當你的 Agent 半夜自己跑了 10 萬次 API 呼叫，月底帳單可以很驚人。

### 第二層：新基礎設施的贏家

智能體需要自己的「電腦」，而一波新創公司正在搶佔這個市場：

- **沙盒環境**：E2B（Firecracker microVM，150ms 冷啟動）、Daytona（Docker 容器，90ms 啟動，[2026 年 2 月完成 2,400 萬美元 A 輪](https://northflank.com/blog/daytona-vs-e2b-ai-code-execution-sandboxes)）、Modal（GPU 工作負載，秒級擴展到 50,000+ 實例）
- **Agent 通訊**：Agentmail 為 Agent 提供持久化電子信箱；Parallel、Exa 重新建構了為 Agent 優化的網頁搜尋
- **Agent 支付**：2026 年 3 月 18 日，[Stripe 和 Tempo 推出了 MPP（Machine Payments Protocol）](https://www.tenzro.com/blog/payments-for-ai-agents)；Coinbase 推出 x402 協議讓 Agent 用穩定幣即時支付；Skyfire 建立了 KYA（Know Your Agent）身份驗證框架

為什麼加密貨幣在 Agent 支付中佔了一席之地？原因很現實：AI Agent 沒辦法開銀行帳戶（銀行需要身份驗證），但加密錢包只需要一把私鑰——不用 KYC、不用合規審查、不用等待。目前 Agentic 商務的年交易量已達 [91.4 億美元](https://blog.payai.network/agentic-payments/)。

### 第三層：開發者的技能重組

如果你是開發者，這個轉變對你意味著什麼？

過去十年，前端開發是軟體業最炙手可熱的領域之一——因為使用者是人類，人類需要漂亮的介面。但當主要使用者是 Agent，**API 設計的重要性將超越 UI 設計**。你的 REST endpoint 有沒有一致的命名慣例、錯誤回應有沒有標準化、文件是不是機器可讀——這些以前是「nice to have」，現在變成了「你的產品能不能被 Agent 發現和使用」的生死門檻。

MCP 伺服器的開發正在成為新的熱門技能。Forrester 預測 [30% 的企業應用供應商將在 2026 年推出自己的 MCP 伺服器](https://truto.one/blog/what-is-mcp-model-context-protocol-the-2026-guide-for-saas-pms/)。如果你能幫公司的產品寫一個好用的 MCP 伺服器，你的市場價值會很不一樣。

### 第四層：二階效應——Agent 經濟的連鎖反應

當 Agent 成為軟體的主要使用者，幾個連鎖反應正在展開：

**搜尋引擎優化（SEO）可能要被 AEO（Agent Engine Optimization）取代。** 以前你優化網站是為了讓 Google 爬蟲找到你。未來你優化 API 是為了讓 AI Agent 選中你。Parallel、Exa 等公司正在為 Agent 重建網路搜尋——如果你的服務不被它們索引，你就失去了未來最大的流量來源。

**微支付終於有了真實的應用場景。** Agent 不會買年度訂閱，它們需要按次付費——用一個 API 呼叫花 0.001 美元，取一次資料花 0.01 美元。這正是加密貨幣微支付多年來一直在尋找的「殺手級應用」。

**企業安全和合規必須徹底重構。** 當你有 144 個非人類身份在公司網路裡跑，但只有不到 10% 的企業能有效管理——這是一場等待發生的安全災難。MCP 的 2026 路線圖包括 Q2 推出的 [OAuth 2.1 企業身份整合](https://blog.modelcontextprotocol.io/posts/2026-mcp-roadmap/)（支援 Okta、Azure AD），Q3 推出的 Agent-to-Agent 協調能力。這些不是可有可無的功能，而是 Agent 大規模部署的必要條件。

---

## 未來展望

### 短期（3-6 個月）：基礎設施就位

幾件幾乎確定會發生的事：

- MCP 的 OAuth 2.1 企業整合將在 Q2 上線，讓 Agent 能安全地以企業員工身份存取公司的 SaaS 工具
- 更多 SaaS 公司會急忙推出混合定價方案——不改的公司會看到營收加速流失
- Agent 沙盒市場會繼續整合，E2B 和 Daytona 可能進一步融資或被收購

### 中期（6-18 個月）：Agent 經濟成形

三種可能的發展情境：

**情境一：平穩過渡。** 大型 SaaS 公司成功轉型為混合定價和 API-first 架構，Agent 的使用量增長填補了 seat 減少的營收缺口。產業洗牌但沒有大規模崩盤。

**情境二：兩極分化。** 少數快速轉型的公司（如 Box、Intercom）吃掉大量市場份額，而轉型緩慢的公司則面臨客戶流失和估值暴跌。SaaS 產業出現類似 2000 年的達康泡沫式洗牌。

**情境三：Agent 可靠性瓶頸。** 如果可靠性複利問題（20 步驟 36% 成功率）遲遲沒有突破，Agent 的採用速度可能大幅放緩，軟體的「Agent 化」退化為行銷噱頭而非真實產品能力。

我個人押注情境二的可能性最高——兩極分化已經在發生了。

### 長期推演：3-5 年後的軟體世界

如果這個趨勢持續下去，到 2030 年左右，我們可能會看到這樣的世界：

軟體產品分成兩大類——**「人機介面」和「機機介面」**。前者是給人看的（Dashboard、報告、視覺化），後者是給 Agent 用的（API、MCP 伺服器、資料管線）。許多產品的「機機介面」會比「人機介面」承載更大的流量和營收。

「全棧開發者」的定義也會改變。以前是「前端+後端」，未來是「人類介面 + Agent 介面 + Agent 工作流程編排」。

### 給讀者的行動建議

**如果你是開發者：** 現在就開始學 MCP 伺服器開發，理解 A2A 協議的設計理念。不要只寫人看得懂的文件，也要寫機器讀得懂的文件。API 設計能力的投資報酬率，在接下來兩年會比前端框架高得多。

**如果你是創業者或產品經理：** 立刻審視你的產品有沒有完整的 API 覆蓋，你的 onboarding 流程能不能被 Agent 自動完成，你的定價模型是不是 per-seat。如果三個答案分別是「沒有」「不能」「是」，你需要把這件事升級為最高優先。

**如果你是一般科技從業者：** 不需要恐慌，但要理解一件事——未來你的很多工作會是「指揮 Agent 去完成任務」而不是「自己打開軟體完成任務」。學會描述清楚你要什麼、驗證 Agent 的產出、設定正確的護欄（guardrails），這些軟技能的重要性會超過你對特定工具的熟練度。

---

軟體產業每一次典範轉移，都有人因為太早進場而受傷，也有人因為太晚反應而出局。這一次的轉移特別有趣的地方在於：它不是改變了「使用者想要什麼」，而是改變了「使用者是誰」。

當你的客戶不是人類，你對「好產品」的所有直覺——漂亮的設計、流暢的體驗、有溫度的品牌——可能都要重新校準。取而代之的是另一套標準：穩定的 API、可預測的行為、標準化的協議、和透明的定價。

聽起來很無趣？也許。但無趣的基礎設施，往往是最大的生意。

---

## 延伸閱讀

- [The State of AI Agents in 2026 — Jon Radoff](https://meditations.metavert.io/p/the-state-of-ai-agents-in-2026)：最全面的 2026 年 AI Agent 現狀分析，涵蓋技術、經濟、基礎設施全面向，數據量驚人
- [The Death of Per-Seat Pricing — PinkLime](https://pinklime.io/blog/future-saas-pricing-ai-era)：深入解析 AI 如何摧毀 SaaS 的 per-seat 模式，並梳理替代方案的優劣
- [AI Agent Adoption 2026: What the Data Shows — Joget/Gartner/IDC](https://joget.com/ai-agent-adoption-in-2026-what-the-analysts-data-shows/)：彙整 Gartner、IDC、Forrester 的最新預測數據，企業採用現況一次看完
- [2026: The Year for Enterprise-Ready MCP Adoption — CData](https://www.cdata.com/blog/2026-year-enterprise-ready-mcp-adoption)：MCP 從實驗到企業級採用的完整路線圖，包括 OAuth 整合和安全功能
- [Meet the AI Agents of 2026 — Ambitious, Overhyped and Still in Training](https://lasvegassun.com/news/2026/jan/03/meet-the-ai-agents-of-2026-ambitious-overhyped-and/)：質疑派的最佳代表作，冷靜分析為什麼 Agent 還沒準備好承擔自主工作
- [AI Agent Protocol Ecosystem Map 2026 — Digital Applied](https://www.digitalapplied.com/blog/ai-agent-protocol-ecosystem-map-2026-mcp-a2a-acp-ucp)：MCP、A2A、ACP 等協議的全景比較，理解智能體通訊的技術格局
- [Agentic Payments: How AI Agents Pay and Transact — PayAI](https://blog.payai.network/agentic-payments/)：智能體支付基礎設施的完整解析，從 x402 到 MPP 到 KYA
- [Box CEO: AI Agents Will Be the Biggest Users of Software — CNBC](https://www.cnbc.com/video/2026/03/04/techcheck-box-ceo-ai-agents-will-be-the-biggest-users-of-software-in-the-future.html)：Aaron Levie 本人的 CNBC 訪談，闡述「為 Agent 做產品」的完整邏輯
