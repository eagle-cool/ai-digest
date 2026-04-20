---
title: "SaaS 巨頭的自我獻祭：Salesforce 與釘釘決定親手殺掉 GUI"
date: 2026-04-20
description: "一年蒸發 2 兆美元市值、SaaS ETF 重挫 28%，Salesforce 和釘釘相隔一個月宣布同一件事：把自家平台打碎重寫，變成 API、MCP 和 CLI 讓 AI Agent 直接呼叫。當操作軟體的不再是人類，數人頭收費的商業模式就到頭了——這不是升級，是二十年 SaaS 商業邏輯的葬禮。"
tags: [deep-dive, ai-industry, agents, ai-tools, llm]
---

## 引言

想像這個畫面：你是某家公司的 IT 主管，公司有 500 個員工，每個月你付 Salesforce 每人 150 美元——一張帳單 7.5 萬，一年 90 萬。這個數字你付了七年，從沒想過會變。

然後 2026 年過完年，你發現公司裡 300 個人已經很少自己打開 Salesforce 網頁了。他們在 Claude Desktop 裡問一句「幫我把這季所有過期 lead 重新分派到對的業務」，AI 就把事情做完了——不是用滑鼠點按鈕，是直接呼叫後端 API。每個動作花掉公司一兩毛錢的 token，一個月帳單可能只剩幾千美元。

你抬頭看財務總監：那我們為什麼還在付 90 萬一年的座位費？

這個問題，過去一年讓全球企業軟體市場少了超過 2 兆美元市值。追蹤 SaaS 類股的 iShares Expanded Tech-Software ETF（IGV）從年初至四月累計下跌 27%，Salesforce 跌 30%，Workday 跌超過 40%，Atlassian 從高點腰斬一半，Adobe 跌 30%。軟體股的遠期本益比從 2020–2022 年高峰的 84.1 倍崩到 22.7 倍，有生以來第一次跌到比 S&P 500 整體還便宜。([humai.blog](https://www.humai.blog/saaspocalypse-why-enterprise-software-has-lost-more-than-2-trillion-in-2026/))

市場用腳投票的理由很直白——大型語言模型正在讓一個最基本的商業前提失效：**企業為什麼要為一個需要人類去點擊、拖拽、填表的圖形介面付錢？**

面對這個 existential 級別的質問，過去一個月，太平洋兩岸的兩家 SaaS 巨頭給出了一個令人不寒而慄的相似答案：**打碎自己**。2026 年 3 月 17 日，阿里巴巴旗下的釘釘在杭州宣布把服務 8 億用戶的底層架構整個砍掉重寫，推出名為「悟空」的企業 AI 原生平台，並把自己重新定義為 Agent OS。一個月後的 4 月 16 日，27 歲的 Salesforce 在舊金山 TrailblazerDX 大會上揭幕「Headless 360」，把平台的每一項能力剝成 API、MCP 工具或 CLI 指令，讓 AI Agent 不用打開瀏覽器就能操作全系統。

兩家公司、一東一西，不約而同選了同一條路：把按鈕變成代碼，讓 AI 接管操作。這篇文章要帶你看清楚的，不是一次普通的產品升級——是整個 B 端軟體產業二十年商業邏輯的葬禮，以及即將在這場葬禮之後重新分配的幾兆美元蛋糕。這個故事的起點，是一篇題為〈[前有釘釘後有 Salesforce，中美 SaaS 巨頭做出了相同的歷史抉擇](https://www.36kr.com/p/3774602459263752)〉的行業分析，但故事遠不止於此。

---

## 事件全貌

先說 Salesforce 這邊的動作有多劇烈。在 TDX 2026 大會上，執行副總裁 Jayesh Govindarjan 揭幕 Headless 360 時沒有客套——他說這個決定 **兩年半前就下了**，現在只是把它端上桌。平台的口號非常工程師：「Build any way, deploy any surface, trust at scale.」

第一個支柱「任意方式構建」背後的數字是：**60 多個新的 MCP（Model Context Protocol）工具**，**30 多個預配置的編碼技能**，支援 Claude Code、Cursor、Codex、Windsurf 等外部 AI 編碼代理**完全實時存取**整個 Salesforce 環境。這意味著一個 Claude Code 使用者可以直接叫出 Salesforce 的資料、工作流、業務邏輯，而不必打開瀏覽器登入 Salesforce。連 Salesforce 自家的開發工具 Agentforce Vibes IDE 都是基於 VS Code 的瀏覽器版本，預設的編碼模型是 Claude Sonnet 4.5。([salesforceben.com](https://www.salesforceben.com/salesforce-headless-360-and-agentforce-vibes-2-0-revealed-at-tdx-2026/))

第二個支柱「任意表面部署」才是商業模式上的關鍵。Salesforce 推出了 Agentforce Experience Layer——一個把 Agent 行為和呈現方式拆開的服務。同一個 Agent，可以原生渲染到 Slack、Mobile、Microsoft Teams、ChatGPT、Claude、Gemini——六個入口，一次開發。換句話說，**使用者以後不需要來 Salesforce 的網站，Agent 會把 Salesforce 帶到使用者所在的任何地方**。

第三個支柱是最容易被略過但最要命的：可信的規模化。Salesforce 推出了 **Agent Script**——一種專門用來確定性定義 Agent 行為的領域語言，已經開源，Claude Code 可以原生生成它。Salesforce 的 AI 總裁 Joe Inzerillo 在現場說了一句讓台下設計師倒抽一口冷氣的話：「The builder is talking to these tools... most of the code is going to be written by the agents.」——代碼以後主要由 Agent 寫，人類只負責跟 Agent 說話。([theregister.com](https://www.theregister.com/2026/04/15/salesforce_headless_360/))

一個月前釘釘那邊的手術更狠。CEO 陳航（化名吳釗）在 3 月 17 日發布會上說的第一句話是：「今天，我們把釘釘拆掉，用 AI 重建了它，鍛造出了『悟空』。」整整一年時間，釘釘把服務 8 億用戶的整個底層改寫，把過去十年累積的圖形介面能力「全面 CLI 化」——每一個原本由人類點擊的功能，現在都變成可以被 AI Agent 直接呼叫的命令列指令。

規模上，悟空建立了**中國最大的企業級 MCP 能力廣場**，首批覆蓋企業常用的 6000 多個 MCP 能力，並把自家的 CLI 工具開源。3 月底那一天，釘釘和字節跳動旗下的飛書在 24 小時內前後腳把 CLI 工具推上 GitHub——中國兩大協作平台默契地向世界宣告：我們這邊也不走 GUI 了。

悟空的企業級定位比 Salesforce 更鮮明。從 Day 1 開始，AI Agent 自動繼承企業權限、所有操作在沙箱中執行、token 消耗即時透明——陳航在現場算了一筆帳：「光是檔案讀寫這件事，AI 一秒鐘可以做上千次操作。」過去企業管員工上下班打卡，未來要管 AI 幾點幾分燒了多少 token。([kr-asia.com](https://kr-asia.com/alibabas-wukong-recasts-dingtalk-as-part-of-ai-native-work-platform))

而在母集團層面，阿里巴巴 3 月 16 日同步宣布成立「阿里 Token Hub（ATH）」事業群，CEO 吳泳銘親自統帥，旗下包含通義實驗室、MaaS 業務線、千問事業部、AI 創新事業部，以及一個從未在公開場合出現過的新名字：**悟空事業部**。釘釘被整個改名裝進去——陳航說得毫不遮掩：「新時代來了，這玩意叫釘釘還是悟空，已經不重要了。」

兩場發布會放在一起看，最震撼的不是技術架構雷同，而是**商業模式的同步轉向**。Salesforce 從最初的 $2 美元一場對話，兩年內演化出 Flex Credits（$0.10 一個動作，10 萬 credits 售價 500 美元）、Flex Agreement（未用完的席位可換成 credits）、Agentforce 1 Editions（每人每月 550 美元）——一套三選一、預算彈性極高的組合拳。釘釘則直接喊出「商業可交付、按結果付費」的新口號，CEO 陳航的原話是：「讓所有開發者都可以基於釘釘 AI 能力，在 ToB 市場真正能賺到錢。」([getmonetizely.com](https://www.getmonetizely.com/blogs/the-doomed-evolution-of-salesforces-agentforce-pricing))

按對話收美元，還是按結果收人民幣，這些都只是外殼。核心只有一件事：**既然幹活的是 AI 不是人，那數人頭收費這條路就走不通了**。

---

## 脈絡

要理解為什麼兩家巨頭今天在擂台上拼命拆自己的牆，得把時間線拉回去幾個月。這場 SaaS 大屠殺有一條很清楚的引爆時間表。

2026 年 1 月 29 日，OpenAI 發布 Project Operator——一個可以自己開瀏覽器、自己填表、自己下單的通用型 AI Agent。當天，微軟單日市值蒸發 **3570 億美元**。市場不傻：如果 Agent 可以自己操作任何網頁，那些靠「使用者要登入我家網站才能做事」賺錢的生意，前途堪慮。

2 月 24 日，Anthropic 發布 Claude Cowork——把 Agent 能力直接整合進企業工作流的產品。那場 demo 展示了 AI Agent 端到端處理法律文件審查、財務分析、專案管理，**48 小時內 SaaS 板塊蒸發 2850 億美元市值**。Thomson Reuters 單日跌 15.83%，LegalZoom 跌 19.68%——凡是業務本質是「讓人填表」的公司，股價全都被壓著打。([taskade.com](https://www.taskade.com/blog/saaspocalypse-explained))

然後是企業側的真實反應。Klarna 公開承認 2024 年靠 AI 砍掉 700 個人，並終止和 Salesforce、Workday 的合約。Workday 自己 Q1 2026 裁了 8.5% 的員工——一家賣「人力資本管理」軟體的公司，因為 AI 自己把自己裁了，這畫面堪稱 2026 年科技業最黑色幽默的一幕。Monday.com 的 CEO 公開宣布用 AI Agent 取代了 100 個業務開發代表。Atlassian 在 3 月的財報裡出現了**有史以來第一次的企業座位數下降**——SaaS 產業二十年來從沒發生過這種事。一份今年一月流出的 Fortune 50 大廠內部備忘錄寫著：「年底前砍掉 60% 的 Salesforce 和 ServiceNow 支出。」

這些數字要放在一個更大的背景裡才能看懂：根據市場分析，**全球企業 IT 預算有大約 40% 正在從傳統 SaaS 訂閱轉移到 Agent 平台和 LLM tokens**。這不是市場份額在玩家之間換手，這是整個支出類別在重新歸類——曾經被劃為「軟體訂閱」的錢，現在被劃為「AI 算力」。對軟體公司來說，這是比任何競爭對手都可怕的事：他們不是在失去客戶，他們是在失去整個支出口袋。

歷史上類似的轉折其實發生過。2013 年 Adobe 從盒裝軟體（Creative Suite）轉向訂閱制（Creative Cloud），當時 Adobe 股價短期震盪，但五年後創造歷史新高——因為他們搶在同業之前跳進新世界。2014 年 Microsoft 用 Satya Nadella 押注雲端，犧牲 Windows 作業系統的霸權換取 Azure 的成長——結果證明那是矽谷史上最成功的轉身之一。

但這一次的震盪更大，因為 Adobe 和 Microsoft 那時候改的是**發貨方式**（從光碟變下載、從本地變雲端），產品邏輯沒有變。而這次改的是**使用者是誰**——從人類變成 AI。當使用者都不是同一個物種了，整個產品定義都得重新來過。這不是換渠道，是換客群。

所以兩家 SaaS 巨頭今天在擂台上拆自己，不是戰術抉擇，是生存動作。他們看得很清楚：如果 Claude Desktop 和 ChatGPT 變成企業員工的新「工作桌面」，那 Salesforce 網頁、釘釘 App 就會變成地下停車場——沒人會特意去，但東西要在那裡才能被 Agent 取用。

---

## 多方觀點

最有意思的是，連 Salesforce 自己都不確定這條路走得通。Jayesh Govindarjan 在被問到 MCP 會不會成為業界標準時，回答出乎意料地坦率：「**說實話，我完全不確定。**」他說：「很多工程師覺得 MCP 只是一個好用的 CLI 外面套了層殼……有人覺得 CLI 本身就夠用了。」

這句話從一個剛剛在自家平台上鋪了 60 個 MCP 工具的副總裁嘴裡說出來，意味很深。Salesforce 的策略本質上是實用主義——**API、CLI、MCP 三種訪問方式同時提供**，誰贏都不會死。這跟釘釘那邊「全面 CLI 化」的押注微妙不同：釘釘選邊站到 CLI，因為 CLI 是被開發者驗證了幾十年的確定性介面；Salesforce 腳踏三船，看哪個協議最後能贏市場。([dataconomy.com](https://dataconomy.com/2026/04/17/salesforce-shifts-to-api-first-future-with-headless-360/))

Govindarjan 的懷疑不是沒道理的。2026 年 MCP 面臨嚴重的安全挑戰：研究人員揭露一個設計缺陷**讓多達 20 萬台 MCP server 暴露在接管風險之下**，Anthropic 的回應是「這是設計，不是 bug」——意思是鍋要開發者自己背。學界的 arxiv 論文已經在批評 MCP 工具描述「不夠乾淨」導致 Agent 效率低下，雙跳延遲和上下文視窗膨脹也是擺在眼前的問題。對於需要穩定性和治理的企業來說，MCP 還不是一個可以無腦壓下去的地基。([computing.co.uk](https://www.computing.co.uk/news/2026/security/flaw-in-anthropic-s-mcp-putting-200k-servers-at-risk))

然後是實務工作者的聲音。Agentforce 推出頭一年，**Salesforce 15 萬客戶裡只有 8000 家實際導入**。一個買家的吐槽很傳神：「那張帳單讓我想起 1991 年的手機流量方案，每個月收到帳單都是進入未知領域的一場冒險。」Agentforce 從 $2/對話改到 Flex Credits 再加回人頭訂閱，三改兩改，就是被企業財務部門按著頭逼出來的。([getmonetizely.com](https://www.getmonetizely.com/blogs/the-doomed-evolution-of-salesforces-agentforce-pricing))

這揭露了一個容易被 agent-first 敘事蓋住的真實問題：企業採購的節奏比技術進化慢太多。CFO 要可預測的月帳單，不是按 token 燒的俄羅斯輪盤。而且企業 IT 採購的大頭——金融、醫療、政府——對治理、審計、回滾的要求高到窒息，「Agent 跑一趟就完成了」這種浪漫敘事在合規框架下活不過一個 SOC 2 審計會議。

悲觀派的陣營裡最大的聲音來自軟體研究者。Bain 的 Agentic AI 平台報告提醒：**Agent-first 不等於 UI-less**，Experience Layer 存在的理由正是人類監督、逐步審核、異常介入。如果一個 Agent 做錯事，你需要一個能讓人類 override 的地方——那個地方通常還是 GUI。Anthropic 自己在〈[Building Effective Agents](https://www.anthropic.com/research/building-effective-agents)〉的文章裡也寫得很清楚：最有效的 agentic 系統是「workflow + agent」的混合體，而不是純粹的 autonomous agent。

地區觀點的差異也很戲劇。美國 Salesforce 的策略是**押注 Builder 生態**——開源 Agent Script，拿 5000 萬美元設立 Builder 基金，跟 Claude Code/Cursor 這些通用型 AI IDE 深度整合。他們賭的是「未來的應用開發，大部分代碼是 Agent 寫的」這個敘事。中國釘釘的策略是**押注企業場景的深度整合**——把阿里整個 B 端生態（淘寶、天貓、1688、支付寶、阿里雲）逐步當成 Skills 接進悟空。美國在做橫向標準，中國在做縱向整合，邏輯迥異但動機一致。

我自己的看法是：**這不是「GUI 死不死」的問題，是「誰付錢」的問題。** GUI 短期內死不了——至少金融業、醫療業、律師業不會讓一個概率性系統完全自己跑。但即使 GUI 不死，**如果大部分操作是 Agent 發起的，那企業會不會用「席位」為單位付錢，就極度可疑**。一個座位可能一年真正打開介面 10 次，你要怎麼收 150 美元一個月？Salesforce 和釘釘看懂了這件事，所以先自己動手。等 CFO 動手，那就是壞消息。

這兩家的選擇其實給出了一個殘忍的判斷：**他們默認 GUI 已經是上一個時代的遺物了**，即使遺物還會用一陣子。

從台灣的視角看這件事還有一個特別的角度。台灣的 SaaS 產業大部分是 local player——鼎新、SAP Taiwan、Oracle 的本地部署、日系 ERP——大部分企業客戶還停在 on-prem 或私有雲的階段。這場 agent-first 革命對台灣的衝擊會是**延遲但猛烈的**：當國際原廠把 headless 當成標準，台灣本地 ISV 和整合商要麼跟上，要麼在兩三年內被邊緣化。中小企業的財務長現在應該做的功課是：**盤點今年的 SaaS 訂閱，哪幾張是靠人頭計費、哪幾張沒有 API 或 MCP 入口**——前者是未來談判桌上的籌碼，後者是準備被替換的對象。

---

## 產業衝擊

這場轉向的衝擊可以分成四層來看，每一層都有很具體的輸家和贏家。

**第一層——直接受影響者。** 最明顯的輸家是**傳統 SaaS 的 per-seat 授權模式**本身。按人頭計費的生意一年可以養活一家上市公司，但一個 Agent 可以抵 5–9 個人的產能，這筆帳怎麼算？Klarna 已經示範了：2024 年砍 700 個人，等同於這 700 個人對應的所有 SaaS 軟體訂閱被一次性清光。Workday 砍 8.5% 員工，對 LinkedIn Premium、Zoom、Asana 這些靠人頭數的工具來說都是直接失血。Atlassian 史上第一次的企業座位數下降是一個警鐘：市場不再成長，開始萎縮。([humai.blog](https://www.humai.blog/saaspocalypse-why-enterprise-software-has-lost-more-than-2-trillion-in-2026/))

受益者是**通用型 AI 助手和 Agent 平台**。Claude Cowork、Project Operator、Microsoft Copilot 變成企業員工的新前端。OpenAI、Anthropic、Google 成為真正的作業系統級別玩家。然後是**MCP 工具生態創業公司**——Salesforce AgentExchange 一上線就有一千多個 Agent 和工具進駐，5000 萬美元的 Builder 基金在後面頂著，這是一個全新的 app 經濟分紅點。

**第二層——商業模式衝擊。** 最深的重寫發生在計價維度。過去 20 年 SaaS 的收入公式簡單粗暴：**MRR = 座位數 × 每座單價 × 淨續費率**。AI 把這個公式的第一項變成了偽變數。當一個 Agent 可以自己完成原本 3 個員工的工作，你花錢買的到底是什麼？Salesforce 給出了四個計費模型，釘釘給出了按結果付費——沒有人知道哪個最後會贏，但有一點很確定：**按人頭計費這條路大家都開始主動棄用**。

這裡有個更深的問題：**當計費變成按 token、按 action、按 outcome，軟體公司的毛利結構會被徹底重寫**。傳統 SaaS 的毛利是 80%，因為軟體本身邊際成本趨近零。但 AI Agent 每跑一次都燒算力，每個 token 都有成本。軟體業有史以來第一次，毛利變得像製造業——有實體的可變成本。這也解釋了為什麼軟體股的 EV/Sales 倍數從 5.6 倍崩到 4.2 倍——市場正在用製造業邏輯重估軟體股。

**第三層——開發者生態。** 這一層的變化對從業者最切身。Claude Code、Cursor、Codex、Windsurf 現在可以**實時操作 Salesforce 的完整環境**——過去你要寫個 Salesforce 整合至少要熟 Apex 語法、Flow Builder、Lightning Component 至少一樣，現在你寫句「幫我從 Salesforce 拉出所有上季過期 lead，寄信分派」就可以。

這對 Salesforce 生態系那些高薪 Consultant（時薪 150–300 美元，全球有 400 萬持證開發者）是直接的價值稀釋。Salesforce AI 總裁 Madhav Thattai 那句「我們要擴大帳篷，讓歷史上不屬於 Salesforce 生態的人進來」翻譯成白話就是：**過去你要考 Admin、Developer、Architect 三張證才能吃這碗飯，現在懂寫 prompt 就夠了**。

前端工程師和 UX 設計師面臨的是類似問題。根據 2025 AI Jobs Report，**AI 已經自動化了 40% 的入門級 UI 任務**。設計師不會消失，但「畫 Figma 做 wireframe」這種 entry-level 的工作會被重寫——設計師的工作會變成「設計 Agent 的行為邊界」「設計 Agent 卡住時的 fallback 流程」「設計 Agent 可信任感的視覺語言」。template 設計師已死，系統設計師的角色會變得更高階。([medium.com](https://medium.com/design-bootcamp/entry-level-ui-ux-jobs-in-2026-are-disappearing-364d3b5e04ee))

**第四層——二階效應。** 最值得玩味的連鎖反應有幾個。

**第一個是瀏覽器的命運。** 如果大部分企業操作不再經過瀏覽器，Chrome、Edge、Safari 的戰略地位會怎麼變？Google 的搜尋廣告引擎還撐得住嗎？Perplexity、Arc、Dia 這些 agent-native 瀏覽器的賭注突然看起來很合理了。

**第二個是「應用程式」這個概念的瓦解。** 如果 Salesforce 把自己拆成 API 和 MCP 工具、釘釘把自己拆成 CLI 指令集，那「應用程式」就從一個**有 UI、有品牌、有使用者忠誠度的產品**，退化成一個**可被 Agent 隨意呼叫的函數庫**。使用者不再記得「我用了 Salesforce」，只會記得「我讓 Claude 做了一件事」。品牌資產在這個新世界裡會被怎麼重新定價？這是每一家 SaaS 上市公司投資人關係部正在偷偷失眠的問題。

**第三個是 Agent 作業系統戰爭**。如果 Claude Desktop、ChatGPT、Gemini 都想當新的企業工作桌面，那就是一場規模堪比當年 PC 作業系統大戰的新戰爭。Salesforce 的 Agentforce Experience Layer 一次渲染六個入口的架構，其實是在**對沖**——他們不想把身家押在其中一家的 OS 上，就像當年軟體商不想被綁死在 Windows 一樣。

---

## 未來展望

**短期（3–6 個月）：**

Oracle、SAP、Workday 會跟著拆自己。他們別無選擇——當 Salesforce 和釘釘這兩個市場主心骨都選了 Headless，其他人不跟就是自動讓出 Agent 生態的制高點。我大膽預測：我們會在 2026 年第三季看到 Oracle 版的「Headless Fusion」或 Workday 版的「Agent Workday」。ServiceNow 壓力最大，因為他們的 Now Platform 過去十年賣的就是「漂亮的介面」，現在要把漂亮介面當成可丟棄物拆了，品牌敘事要怎麼講？

MCP 安全戰也會升級。當 Salesforce 背書 MCP、釘釘直接跳過它，Linux Foundation 今年會被迫快速推動新版本規範。如果安全問題沒解，Govindarjan 的「CLI 才是王道」預言可能會成真——這會把 Anthropic 從 MCP 標準制定者的位置拉下來，是 OpenAI 意料之外的機會。

Agentforce 的導入率會被市場盯得很緊。Salesforce 在 2026 Q3 財報如果不能拿出「至少 15% 客戶完成 Headless 360 升級」的數字，股價會被狠砍一波。反過來如果能端出導入率數字，會帶起一波 SaaS 股票的技術性反彈——市場最怕的不是壞消息，是「大家一起不知道怎麼辦」的那種真空狀態。

Microsoft 和 Google 也不會袖手旁觀。Microsoft 的 Copilot Studio 和 Google 的 Agent Builder 會借這個風向加速擁抱外部 MCP 工具——他們有 Azure 和 GCP 的基礎設施優勢，只要出手夠快，可以一口氣把 Salesforce 和釘釘拉下來的市場份額接走。OpenAI 的 AgentKit 會繼續往企業整合方向演化，特別是 Project Operator 的 B 端版本，這會是 2026 下半年最值得盯的產品線。

**中期（6–18 個月）：三種可能情境**

**情境一：Agent-native 完全勝利。** 企業軟體變成純後端，GUI 縮到接近零，所有操作經由 Claude Desktop/ChatGPT 這類 super-assistant 發起。Salesforce、釘釘、Workday 都變成「infrastructure provider」，用量化計價，毛利下降但總量擴大。這個情境的訊號是：Claude 或 ChatGPT 的企業 ARR 在 2027 年初突破 100 億美元。

**情境二：Hybrid 均衡。** GUI 為核心工作台不死，Agent 變成「超級快捷鍵」。企業員工一天有 30% 的時間直接對 Agent 講話、70% 時間還是在各家 SaaS 的介面裡。計費模式變成「基礎訂閱 + 用量加購」的組合拳。這個情境對既有 SaaS 最友善，也最符合 CFO 口味。訊號是：SaaS ETF 在 2026 下半年止跌回升，forward P/E 回到 30 倍以上。

**情境三：新一波垂直 agent-first 新創洗牌市場。** 既有玩家反應太慢，一批從頭設計的 agent-native 新創在 CRM、ERP、HR、ITSM 每個垂直領域崛起。Salesforce、Workday 被漸進蠶食，不會快死但會慢慢萎縮，像今天的 IBM。這個情境的訊號是：2026 下半年出現第一個 ARR 破億、完全 agent-native 的 CRM 新創。

我自己押注**情境二為主、情境三為輔**。大企業換系統的轉換成本極高，但 SMB 市場和新興行業會被 agent-native 新創吃掉。既有 SaaS 巨頭不會死，但會從高毛利的「軟體商」變成低毛利的「API 提供商」——這是它們現在拚命自我改造的原因。

**長期推演（3–5 年）：**

SaaS 這個詞可能會消失。2030 年的企業軟體目錄上，寫的不再是「某某軟體年費」，而是「Agent Cloud 使用額度」「工作結果承包合約」。軟體公司的財報會出現新的指標：AAU（Active Agent Users）、TPU（Tokens Per Unit of Work）、OCR（Outcome Completion Rate）。

軟體這個行業會從靜態資產變成動態服務。過去一家公司買 Salesforce 是「買一個系統」，未來是「訂閱一個持續學習、持續進化的業務流程」。軟體的本體從「代碼」變成「代碼 + 模型 + 資料管線 + 人類審核點」的複合體——這是一個毛利更低、但總市場更大的新形態。

**給不同讀者的行動建議：**

如果你是**開發者**——現在就開始學 MCP、CLI 工具設計、Agent Script 這類確定性定義語言。你的未來不是寫 UI，是幫企業**把業務流程轉譯成 Agent 可以確定性執行的形式**。這個技能市場還沒成熟，早入場的人會拿到類似 2008 年 iOS 開發者的先機。同時，別再只靠「某 SaaS 平台認證」賺錢——那個護城河正在縮水。

如果你是**創業者或產品經理**——現在是重寫 B2B 產品的窗口期。你的競爭對手不是別家 SaaS，是「同一個需求被 Claude 用 API 組合出來的方案」。問自己：我的產品有沒有辦法被 Agent 完全呼叫？我的計價模式能不能從 per-seat 改成 per-outcome？如果答案是否定的，那你可能在錯誤的賽道上跑。

如果你是**一般科技從業者**——重點不是學 AI，是重新設計你的**工作流**。觀察你一天點了多少次滑鼠，那些動作哪些是 Agent 可以代勞的，哪些是你真正在「思考」。把前者交給 Agent，把自己的時間留給後者。你的工作價值不會消失，但會重新定位到那些**只有人類能做判斷**的節點上。

最後留個問題：**如果 Salesforce 和釘釘今天已經願意把自己拆掉，那些還沒動手的公司，還有多少時間？**

這場葬禮的請帖，其實已經寄到每一家企業軟體公司的 CEO 桌上了。

---

## 延伸閱讀

- [Salesforce launches Headless 360 to turn its entire platform into infrastructure for AI agents — VentureBeat](https://venturebeat.com/ai/salesforce-launches-headless-360-to-turn-its-entire-platform-into-infrastructure-for-ai-agents)：TDX 2026 的第一手深度報導，包含 Govindarjan 關於 MCP 標準化不確定性的完整訪談。
- [Alibaba's Wukong recasts DingTalk as part of AI-native work platform — KrAsia](https://kr-asia.com/alibabas-wukong-recasts-dingtalk-as-part-of-ai-native-work-platform)：釘釘悟空發布會的英文深度報導，釐清阿里 ATH 事業群的戰略意圖。
- [SaaSpocalypse: Why Enterprise Software Has Lost More Than $2 Trillion in 2026 — humai.blog](https://www.humai.blog/saaspocalypse-why-enterprise-software-has-lost-more-than-2-trillion-in-2026/)：把整個 SaaS 崩盤用具體數字串起來的分析文，IGV、P/E、單日跌幅全在這一篇。
- [The Doomed Evolution of Salesforce's Agentforce Pricing — Monetizely](https://www.getmonetizely.com/blogs/the-doomed-evolution-of-salesforces-agentforce-pricing)：把 Salesforce 從 $2/對話到 Flex Credits 的定價演化拆得最清楚的一篇，包含 15 萬客戶只 8000 導入的關鍵數字。
- [Salesforce debuts Headless 360 agentic platform — The Register](https://www.theregister.com/2026/04/15/salesforce_headless_360/)：對 Agent Script 和確定性/概率性張力解釋最技術性的報導。
- [Flaw in Anthropic's MCP putting 200k servers at risk — Computing](https://www.computing.co.uk/news/2026/security/flaw-in-anthropic-s-mcp-putting-200k-servers-at-risk)：MCP 安全爭議的第一手報導，理解為什麼 Govindarjan 說「完全不確定」MCP 會贏。
- [Entry Level UI UX Jobs in 2026 Are Disappearing — Medium](https://medium.com/design-bootcamp/entry-level-ui-ux-jobs-in-2026-are-disappearing-364d3b5e04ee)：看清 agent-first 對設計師 entry-level 就業市場的直接衝擊。
- [Building Effective AI Agents — Anthropic](https://www.anthropic.com/research/building-effective-agents)：Anthropic 自己對「workflow vs agent」的清醒論述，讀完你會明白為什麼 GUI 短期還死不了。
