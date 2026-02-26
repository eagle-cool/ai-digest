---
title: "NVIDIA 年賺 1200 億美元之後：算力即營收的新世界，與它的隱憂"
date: 2026-02-26
description: "NVIDIA 財年淨利潤三年暴增 30 倍，黃仁勳宣告 Agentic AI 拐點到來，卻面臨股價停滯、ASIC 競爭與中國市場萎縮。當「算力即營收」成為新信條，AI 產業的下一章究竟會怎麼寫？"
tags: [deep-dive, ai-industry, ai-agents, llm]
---

## 引言

三年前，NVIDIA 的年淨利潤是 44 億美元。2026 財年，這個數字是 1200 億美元。

三十倍。三十六個月。在現代科技史上，沒有任何一家公司在這麼短的時間內完成過這種量級的跳躍。即便是蘋果從 iPhone 的輝煌十年，利潤成長的速度也遠不及此。NVIDIA 從一家遊戲顯卡公司變成全美國最賺錢的公司之一，市值逼近 5 萬億美元——它不是在攀爬，而是在垂直起飛。

但弔詭的是，當 NVIDIA 在 2 月 25 日公佈這份「史詩級」財報之後，股價盤後僅上漲了 1%，隨後迅速回吐漲幅。過去幾個月，NVIDIA 的股價基本處於區間震盪的狀態。一家利潤翻了 30 倍的公司，股價卻彷彿原地踏步——這件事本身就值得深思。

在這場財報電話會上，黃仁勳丟出了一個他顯然準備已久的論述框架：**「算力即營收（Compute equals revenues）」**。他說，在這個 AI 的新世界裡，沒有算力就無法生成 Token，沒有 Token 就無法實現營收增長。他還宣告：**Agentic AI 的拐點已經到來**。

這不只是一份財報，這是一場關於 AI 產業下一章的宣言。但宣言歸宣言，現實是——就在同一週，AMD 拿下了 Meta 價值 600 億美元的 6GW GPU 訂單，Google 的 TPU 市佔率正在悄悄逼近 35%，而 NVIDIA 在中國的 H20 晶片全年營收，只有可憐的 6000 萬美元。

這篇報導的起點是[芯東西對 NVIDIA 2026 財年第四季度財報的詳細拆解](https://www.36kr.com/p/3699584520498825)以及[字母 AI 對黃仁勳財報電話會的深度分析](https://www.36kr.com/p/3699542976688648)，但故事遠不止於此。

---

## 事件全貌

先看數字。NVIDIA 2026 財年第四季度（截至 2026 年 1 月 25 日）營收達 681.3 億美元，年增 73%，季增 20%，輕鬆超越華爾街預期的 662 億美元。淨利潤 430 億美元，年增 94%。全年營收 2159.4 億美元，年增 65%；淨利潤 1200.8 億美元，年增 65%。

數據中心業務是絕對的核心，單季貢獻 623.1 億美元，佔總營收超過 91%。其中計算業務 513.3 億美元，年增 58%；但更值得注意的是**網路業務——單季 109.8 億美元，年增 263%**。網路營收暴增意味著客戶不只是在買 GPU，而是在買整套機架級的計算系統。這是規模化部署 AI 基礎設施的明確信號。

[Blackwell 架構](https://nvidianews.nvidia.com/news/nvidia-announces-financial-results-for-fourth-quarter-and-fiscal-2026)已成為主力產品，佔當季數據中心營收的三分之二。CFO Colette Kress 表示，Vera Rubin 樣品已在本週出貨給客戶，計劃在今年下半年開始量產。Rubin 將提供比 Blackwell 更高的性能，NVIDIA 預計每家雲端模型建構商都將部署 Rubin 系統。

展望下一季度，NVIDIA 給出了 780 億美元的營收指引，遠高於華爾街預期的 720-730 億美元。這等於在說：別擔心，需求還在加速。指引中特別標註了一個細節：**不包含來自中國的數據中心計算收入**。這句話的潛台詞是——即使完全拋開中國市場，NVIDIA 的增長引擎依然強勁。

值得一提的是銷售集中度的問題。財報顯示，少數幾個關鍵客戶的銷售額佔比達到 36%，高於上一財年的 34%。超大規模數據中心運營商佔數據中心收入的略高於 50%。這意味著 NVIDIA 的營收增長高度依賴頭部科技公司，結構性風險並未消失。如果這幾家大客戶中的任何一家突然減少了採購——不管是因為自研晶片成功，還是因為 AI ROI 不達預期——都會對 NVIDIA 造成不成比例的衝擊。

但真正讓這場財報會與眾不同的，不是這些數字，而是黃仁勳在電話會上的一段論述。他提出了 AI 產業經歷的**三次平台轉移**：從傳統 CPU 到 GPU 加速計算，從傳統機器學習到生成式 AI，再從生成式 AI 到 Agentic AI。每一次轉移都獨立地需要大規模投資。他說前兩次轉移已經通過成本節約和營收增長「自我資助」，而 Agentic AI 是疊加在上面的全新層級。

他還透露了幾個關鍵訊息：與 OpenAI 的合作協議「接近敲定」，計劃投資超過 1300 億美元用於 AI 基礎設施建設；Groq 的技術將作為加速器來擴展 NVIDIA 的架構，更多細節將在 GTC 大會上揭曉。NVIDIA 去年底以 200 億美元收購 Groq 核心團隊和技術授權，這是 NVIDIA 史上最大的收購案——[年報顯示 Groq 相關投資活動現金流為 -130 億美元](https://www.36kr.com/p/3699584520498825)。

---

## 脈絡

要理解 NVIDIA 今天的處境，必須回溯 AI 算力需求的演化史。

2022 年 11 月，ChatGPT 橫空出世。在那之前，NVIDIA 的數據中心業務雖然已經在穩步成長，但規模遠不及今天。CFO Kress 在這次財報會上提到一個驚人的數字：**自 ChatGPT 誕生以來，NVIDIA 的數據中心營收已經增長至原來的近 13 倍**。

第一階段是訓練軍備競賽。2023 年到 2024 年，全球每一家有野心的科技公司都在瘋狂購買 NVIDIA 的 H100 和 A100 GPU 來訓練自己的大型語言模型。OpenAI、Google、Meta、Anthropic、Mistral——每一家都需要成千上萬甚至數萬張 GPU 來訓練越來越大的模型。這個階段，NVIDIA 幾乎是唯一的選擇，因為它的 CUDA 軟體生態系統已經構建了數十年的護城河。

第二階段是推理的崛起。到了 2025 年，隨著模型訓練的邊際收益開始遞減（所謂的 Scaling Law 撞牆論爭），產業的焦點開始轉向推理——也就是讓已經訓練好的模型實際為用戶提供服務。[Deloitte 的研究報告指出](https://www.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions/2026/compute-power-ai.html)，歷史上大約 80% 的 AI 支出用於訓練，20% 用於推理，但這個比例正在急劇反轉——預測到 2026 年底，80% 的支出將用於推理。

第三階段——也就是黃仁勳這次宣告的——是 Agentic AI。如果說推理是讓 AI 回答一個問題，那麼 Agentic AI 就是讓 AI 自主地完成一連串任務：規劃、執行、驗證、修正，循環往復。每一個 Agent 在執行任務時會生成大量的 Token，這些 Token 的計算需求遠超傳統的聊天式問答。

[根據 Market.us 的研究](https://market.us/report/agentic-ai-market/)，Agentic AI 市場在 2025 年估值約 70 億美元，預計以超過 43% 的年複合增長率擴張。[IBM 和 Salesforce 估計](https://masterofcode.com/blog/ai-agent-statistics)，到 2026 年底，全球將有超過 10 億個 AI Agent 在運行。[Gartner 預測](https://onereach.ai/blog/agentic-ai-adoption-rates-roi-market-trends/)，到 2026 年底，40% 的企業應用將包含特定任務的 AI Agent。

這就是黃仁勳「算力即營收」論述的基礎邏輯：Agent 越多，生成的 Token 越多，需要的算力越大，NVIDIA 的營收就越高。一個完美的飛輪效應——至少在理論上是這樣。

但歷史脈絡中還有一個容易被忽略的暗線：**NVIDIA 的成功很大程度上是「生態系統鎖定」的結果**。Hugging Face 上超過 150 萬個 AI 模型都運行在 NVIDIA 的 CUDA 平台上。這種生態系統的黏性比任何單一晶片的性能優勢都更持久。黃仁勳在電話會上也明確強調了這一點：「我們的平台能夠運行全球大部分開源模型並且支持廣泛的軟體生態。」但問題是，生態系統的護城河並非不可逾越。PyTorch 對多後端的支持越來越好，Google 的 JAX 框架正在快速成長，ONNX Runtime 讓模型跨平台變得更容易。推理時代的到來，恰恰加速了這種生態系統的多元化——因為推理的軟體棧比訓練簡單得多，切換成本也更低。

---

## 多方觀點

### 樂觀派：AI 的黃金時代才剛開始

黃仁勳自己的立場非常明確：**「AI 不會倒退，AI 只會變得更好。」** 他在電話會上反覆強調，全球所需的 Token 生成能力遠超 7000 億美元（指五大美國科技公司 2026 年合計資本支出），世界需要的計算量將是目前的一千倍。他對 2030 年全球數據中心資本支出達到 3 至 4 萬億美元的預期保持樂觀。

支持這個觀點的陣營有相當的數據支撐。[四大雲端巨頭（Google、Meta、Microsoft、Amazon）在 2026 年的資本支出預計超過 6600 億美元](https://futurumgroup.com/insights/ai-capex-2026-the-690b-infrastructure-sprint/)，同比增長 62%。Meta 的 Mark Zuckerberg 剛剛宣佈了 2000 億美元的 AI 基礎設施投資計劃。Kress 在電話會上提到，運行在 NVIDIA 晶片上的 AI 系統為 Facebook 帶來了 3.5% 的廣告點擊率提升——這是實實在在的 ROI。

黃仁勳還特別提到了 Claude Code、OpenClaw 等 AI 應用帶來的計算需求飆升，並稱所有企業級軟體開發商現在都在開發 Agent 系統。[61% 的 CEO 正在將 Agent 整合到核心業務運營中](https://onereach.ai/blog/agentic-ai-adoption-rates-roi-market-trends/)，這個數字超過了早期 RPA（機器人流程自動化）浪潮的採用率。

### 質疑派：算力能自動等於營收嗎？

但「算力即營收」這個論述並非無懈可擊。[Gizmodo 的深度分析指出](https://gizmodo.com/compute-equals-revenues-nvidia-needs-jensen-huangs-new-catchphrase-to-be-true-2000726841)幾個關鍵的反面數據：儘管 70% 的企業已經在使用 AI，超過 80% 的企業報告 AI 對就業或生產力**沒有顯著影響**。OpenAI 的 COO 甚至承認，企業 AI「還沒有真正滲透到企業的業務流程中」。

更致命的一擊來自 Goldman Sachs 的一位分析師，他發現 AI 在 2025 年對美國 GDP 的貢獻「基本上為零」，儘管當年的 AI 支出創下歷史紀錄。這直接挑戰了「計算投資會自動產生對等營收」的假設。

[有分析師警告](https://coastaljournal.substack.com/p/ai-capex-vs-roi-big-techs-spending)，大型科技公司的自由現金流在 2026 年可能下降高達 90%，因為資本支出的增速遠超 AI 相關營收的增速。如果這些公司無法在未來幾個季度展示出清晰的 AI ROI，資本支出的持續性將面臨嚴峻挑戰——而這會直接影響 NVIDIA 的訂單簿。

[「泡沫預言家」Michael Burry](https://cressetcapital.com/articles/market-update/market-update-12-17-25-2026-outlook-is-ai-a-bubble/)——就是那個預測了 2008 年次貸危機的人——已經公開表示，當前的 AI 熱潮具有泡沫特徵，指向不可持續的資本支出。

### 第一線的聲音：推理成本是真正的戰場

在實務層面，企業用戶最關心的不是訓練有多強大，而是推理成本有多低。[SDxCentral 的報導指出](https://www.sdxcentral.com/analysis/ai-inferencing-will-define-2026-and-the-markets-wide-open/)，2026 年將成為 AI 推理的爆發年。企業每月的 AI 帳單動輒數千萬美元，其中最大的成本來源已經不是模型訓練，而是維持 Agent 系統持續運行所需的推理計算。

這正是 NVIDIA 面臨競爭壓力的核心戰場。在訓練階段，NVIDIA GPU 的優勢是壓倒性的；但在推理階段，對性能的要求相對較低，而對成本效率的要求極高。這給了 Google TPU、Broadcom 定制 ASIC 和 AMD 切入的機會。

[全球 AI 推理市場預計從 2025 年的 1061 億美元增長到 2030 年的 2550 億美元](https://www.marketsandmarkets.com/Market-Reports/ai-inference-market-189921964.html)，年複合增長率 19.2%。推理專用晶片市場在 2026 年預計將突破 500 億美元。這個市場正在從「NVIDIA 一家獨大」走向「多元化競爭」——而且競爭的維度不只是晶片性能，更包括整體 TCO（Total Cost of Ownership）、能源效率、以及與特定工作負載的適配程度。一些企業甚至開始將高頻推理任務從雲端拉回自建機房，因為當推理需求是 24/7 不間斷的，自建的經濟效益反而比按需付費更好。

### 我的觀點

以我的經驗來看，黃仁勳的「算力即營收」論述有一半是對的，一半是精心包裝的行銷敘事。

對的部分：AI Agent 確實會大幅增加推理計算的需求，而且這個需求是持續性的、與營收直接掛鉤的。當你的 AI Agent 每秒都在生成 Token 來完成客戶的任務，每個 Token 都對應著收入——這個邏輯是成立的。

但包裝的部分在於：黃仁勳暗示「所有的算力投資都會自動轉化為營收」，這顯然過度簡化了。現實是，很多企業買了 GPU 卻還不知道怎麼用它來賺錢。而且更關鍵的是，他忽略了一個事實——算力不一定要來自 NVIDIA。推理時代的到來，恰恰是 NVIDIA 壟斷地位可能開始鬆動的時刻。

---

## 產業衝擊

### 第一層：誰受益？誰受損？

最直接的受益者當然是 NVIDIA 自己——至少在短期內。年營收 2159 億美元、淨利潤 1200 億美元、現金及等價物 626 億美元。這是一台印鈔機在全速運轉。

但 NVIDIA 的高利潤率（75% 的毛利率）意味著**產業鏈上的大部分利潤被它一個人拿走了**。這對下游客戶來說不是什麼好消息。當你的供應商拿走了 75% 的毛利，你自己的經濟效益就很難看。[海豚投研的分析精闢地指出](https://www.36kr.com/p/3699542976688648)：「上游 NVIDIA 晶片的高毛利率，帶走了產業鏈中的大量利潤，這直接影響到了下游的經濟性。」

這正是為什麼每一家大型科技公司都在積極尋求替代方案。

### 第二層：ASIC 競爭正式進入深水區

本週最具象徵意義的事件之一，是 [AMD 與 Meta 簽署了價值 600 億美元的 6GW AI GPU 合約](https://www.amd.com/en/newsroom/press-releases/2026-2-24-amd-and-meta-announce-expanded-strategic-partnersh.html)。這是生成式 AI 時代以來，NVIDIA 首次面臨來自 AMD 的真正價格競爭。合約包括一個績效掛鉤的認股權證——Meta 可以收購 1.6 億股 AMD 股票（約佔 AMD 10% 的股份）——這種利益綁定的深度，在 AI 晶片市場前所未有。

[根據分析師估計](https://www.benzinga.com/analyst-stock-ratings/reiteration/26/02/50874778/amd-strikes-100-billion-blow-to-nvidia-massive-meta-deal-could-crown-new-ai-king-analyst)，Meta 計劃的 6GW 部署從 2027 年到 2030 年每年可為 AMD 帶來 230-250 億美元的營收，四年累計可達 900-1000 億美元。這不是一張小訂單，這是一次產業格局的重新洗牌。

在 ASIC 端，Google TPU 的威脅更加深遠。[Goldman Sachs 的估計顯示](https://www.zerohedge.com/news/2026-01-27/gpus-vs-asics-and-inference-cost-curve)，TPU 在推理工作負載中的市佔率到 2026 年第四季度可能達到 35%。定制 ASIC 的出貨量預計在 2026 年增長 44.6%，而 GPU 出貨量增速僅為 16.1%。Google 的 TPU v7 在每百萬 Token 成本上已經與 NVIDIA 的 GB200 NVL72 持平甚至更低。

黃仁勳對此的回應是典型的黃式策略——他不否認 ASIC 的存在，但強調 NVIDIA 只有在「別無選擇」的情況下才會使用小晶片（chiplet）架構，因為每次跨越小晶片邊界都會增加延遲和功耗。換句話說，他在暗示 NVIDIA 的單片大晶片在性能上仍有結構性優勢。

但市場顯然不完全買帳。這也是為什麼 NVIDIA 的股價在這麼漂亮的財報面前依然不為所動——**投資者已經在為 2027 財年之後的不確定性定價**。

### 第三層：Groq 收購的深層含義

NVIDIA 以 200 億美元收購 Groq 的核心團隊和技術授權，這筆交易的意義遠超表面。[有分析師直言](https://www.uncoveralpha.com/p/the-20-billion-admission-why-nvidia)，這是 NVIDIA「對 ASIC 革命的一次 200 億美元的承認」。Groq 的 LPU（Language Processing Unit）以超低延遲的推理性能著稱——正好是 NVIDIA GPU 相對較弱的領域。

黃仁勳在電話會上說要「像用 Mellanox 擴展自身架構一樣」來整合 Groq。但 [CNBC 的報導引用分析師的話指出](https://www.cnbc.com/2025/12/26/nvidia-groq-deal-is-structured-to-keep-fiction-of-competition-alive.html)，這筆交易被結構化為「非獨家授權協議」，目的之一可能是「維持競爭的假象」以規避監管審查。

無論如何，這筆收購傳達了一個清晰的信號：**NVIDIA 知道推理時代需要不同的硬體架構**，而它選擇通過收購而非純粹的內部研發來補足這個短板。

### 第四層：中國市場的萎縮

NVIDIA 財報中最令人矚目的數字之一：在獲得美國政府許可後，H20 晶片在中國的全年營收僅約 6000 萬美元。H200 的許可則更加模糊——NVIDIA 表示「截至目前還沒有在 H200 許可項目下產生任何收入」。

這與 NVIDIA 在中國曾經數十億美元的營收形成了鮮明對比。[儘管 Trump 政府在 2025 年 12 月宣佈允許 NVIDIA 向中國出售 H200 晶片](https://thediplomat.com/2026/02/nvidias-h200-chips-re-enter-china-but-beijing-isnt-giving-up-on-huawei/)（附帶 25% 的稅），中國海關卻被指示阻擋 H200 的進口。NVIDIA 甚至要求中國客戶全額預付款，以應對監管不確定性。

更值得關注的是 Kress 在電話會上的一句話：**NVIDIA 在中國的競爭對手，在近期 IPO 的推動下正在取得進展，並有可能在長期內顛覆全球 AI 行業的格局。** 她沒有點名，但明眼人都知道她指的是華為的昇騰系列和其他中國 AI 晶片廠商。

中國市場的萎縮對 NVIDIA 短期財務影響有限（中國營收佔比已經大幅下降），但長期的戰略影響不容忽視——一個 14 億人的市場正在被迫建立自己的 AI 晶片生態系統，而一旦這個生態系統成熟，它可能不會回頭。

這裡有一個更大的地緣政治故事正在展開。美國的晶片禁令客觀上加速了中國 AI 晶片產業的自主化進程。華為的昇騰 910B 系列已經在中國市場佔據了相當份額，百度、阿里巴巴、字節跳動等大廠都在積極適配華為的晶片方案。DeepSeek 更是用相對有限的硬體資源展示了驚人的模型能力，動搖了「沒有最頂級 GPU 就做不了最頂級 AI」的假設。NVIDIA 可能正在失去的不只是一個市場，而是一整代中國 AI 開發者對 CUDA 生態系統的依賴。

---

## 未來展望

### 短期（3-6 個月）：確定性依然很高

幾件幾乎確定會發生的事：

NVIDIA 的 2027 財年第一季度營收將達到 780 億美元左右，繼續超越預期。Blackwell+Rubin 到 2026 年底的累計出貨量將達到 2000 萬顆，大致對應 5000 億美元的收入。GTC 大會上將揭曉 Groq 整合的更多細節，以及可能的 Rubin 架構深度展示。

與 OpenAI 的合作協議大概率在未來一兩個月內正式敲定，投資規模可能超過 1300 億美元。這將是 AI 時代最重要的算力綁定之一。

Agentic AI 的企業採用將加速。Claude Code、OpenClaw 的企業版、Microsoft Copilot Studio——每一個都在驅動更多的推理計算需求。

### 中期（6-18 個月）：分歧開始顯現

**情境一：正向循環確立。** 如果 AI Agent 在企業中真正實現了可量化的 ROI——比如客服成本降低 50%、軟體開發效率翻倍、銷售轉化率顯著提升——那麼「算力即營收」的邏輯就會被驗證。我們已經看到一些初步的信號：Meta 報告 AI 帶來了 3.5% 的廣告點擊率提升，Salesforce 的 Agentforce 平台號稱為客戶節省了數百萬美元的人力成本。如果這些案例在 2026 年下半年大規模複製，企業將加大投入，雲端巨頭的資本支出將繼續攀升，NVIDIA 的業績增長可以延續到 2028 年及以後。這是黃仁勳押注的情境。

**情境二：ROI 焦慮蔓延。** 如果大量企業發現 AI 投資的回報週期比預期更長，或者 AI Agent 在實際部署中的表現不如演示時那麼亮眼，那麼 2027 年下半年可能出現資本支出的增速放緩。不需要絕對金額下降——僅僅是增速從 62% 降到 20%，就足以讓 NVIDIA 的成長敘事受到衝擊。

**情境三：ASIC 加速追趕。** AMD-Meta 的 600 億美元訂單只是開始。如果 Google TPU v7 在推理成本上持續壓倒 NVIDIA，如果 Broadcom 的定制 ASIC 業務在 2027 年大幅擴張，NVIDIA 在推理市場的份額可能從目前的 70-80% 下降到 50-60%。這不會殺死 NVIDIA——訓練市場的霸主地位仍然穩固——但會顯著壓縮其毛利率。市場對此最為擔憂。

### 長期推演：3-5 年後的世界

如果黃仁勳的願景成真，2030 年的全球數據中心資本支出將達到 3-4 萬億美元。AI 將不再是「一項技術」，而是像電力一樣成為所有經濟活動的基礎設施。每一家公司都將是 AI 公司，每一個業務流程都將有 Agent 在運行，每一個 Agent 都在 24/7 不間斷地生成 Token。

在這個世界裡，NVIDIA 的角色更像是「AI 時代的台積電」——不可或缺，但也會面臨利潤率被逐漸壓縮的壓力，因為沒有任何客戶願意永遠讓供應商拿走 75% 的毛利。

但也存在一個更溫和的情境：AI Agent 的滲透率不如預期，推理計算的需求增長在某個點開始飽和，行業經歷一次類似 2001 年互聯網泡沫後的「理性回歸」。回顧歷史，2000 年的互聯網泡沫破裂並沒有殺死網際網路——它殺死的是過度投資和不切實際的估值。十年後，Google、Amazon、Facebook 都成了巨頭。AI 可能會走類似的路徑：長期趨勢確定，但短期的資本配置效率可能遠低於市場的樂觀假設。在這個情境中，NVIDIA 的營收不會崩盤——需求仍在——但增速將回到個位數或低雙位數，估值也將大幅修正。而那些在泡沫期過度舉債建設數據中心的公司，可能會面臨現金流的嚴峻挑戰。

### 給讀者的行動建議

**如果你是開發者：** 現在是學習 Agent 開發框架的最佳時機。不管底層硬體格局怎麼變，推理和 Agent 的應用層需求是確定的。同時，不要把自己鎖定在只能在 NVIDIA GPU 上運行的技術棧裡——跨平台推理能力（支持 NVIDIA、AMD、TPU、甚至 CPU 推理）將成為越來越重要的工程能力。

**如果你是創業者或產品經理：** 關注推理成本的下降曲線。每一代晶片的推出都在降低每 Token 的成本——NVIDIA 自己說 Blackwell 的每 Token 成本遠低於上一代，Rubin 還會更低。這意味著今天因為成本而不可行的 AI 應用場景，在 12 個月後可能就變得可行了。但不要只看成本，也要看延遲——Agentic AI 對延遲的敏感度遠高於傳統的聊天應用。

**如果你是投資者或一般科技從業者：** NVIDIA 的短期業績確定性很高，但長期估值面臨 ASIC 競爭和毛利率壓縮的結構性風險。更重要的是，與其只盯著 NVIDIA 一家公司，不如關注整個 AI 基礎設施供應鏈的重新洗牌——Broadcom、AMD、台積電、甚至電力基礎設施公司，都可能是這場變革中的重要玩家。

---

黃仁勳在電話會上說了一句話，我覺得值得所有人認真思考：**「過去的時代，軟體運行在計算機上。現如今，AI 需要的計算量是傳統軟體的一千倍。」**

如果這句話是對的——而目前的數據確實在支持這個方向——那麼我們正站在一次計算經濟學的根本性重構的起點。不是「要不要投資 AI」的問題，而是「算力的供給結構會是什麼樣子」的問題。

NVIDIA 今天是這個新世界的絕對霸主。但歷史告訴我們，沒有哪個霸主能永遠獨占鰲頭——尤其是當你的毛利率高到讓每一個客戶都有動力去尋找替代方案的時候。

三十倍的利潤增長，是一個時代的奇蹟，也可能是一個頂點的預兆。真正的問題不是 NVIDIA 能不能繼續賺錢——它當然能。問題是，**在這個「算力即營收」的新世界裡，算力是否只能來自 NVIDIA？**

答案，正在以每季度一次的速度，逐漸明朗。

---

## 延伸閱讀

- [NVIDIA 2026 財年 Q4 財報官方新聞稿 — NVIDIA Newsroom](https://nvidianews.nvidia.com/news/nvidia-announces-financial-results-for-fourth-quarter-and-fiscal-2026)：最權威的第一手財務數據
- [In Nvidia We Trust: 'The Agentic AI Inflection Point Has Arrived' — Fortune](https://fortune.com/2026/02/25/nvidia-nvda-earnings-q4-results-jensen-huang/)：Fortune 對黃仁勳三大平台轉移論述的深度解讀
- ['Compute Equals Revenues': Nvidia Needs Jensen Huang's New Catchphrase to Be True — Gizmodo](https://gizmodo.com/compute-equals-revenues-nvidia-needs-jensen-huangs-new-catchphrase-to-be-true-2000726841)：對「算力即營收」論述最犀利的質疑
- [AMD Secures Historic 6-Gigawatt AI Infrastructure Deal with Meta — AMD Newsroom](https://www.amd.com/en/newsroom/press-releases/2026-2-24-amd-and-meta-announce-expanded-strategic-partnersh.html)：AMD-Meta 600 億美元訂單的官方公告，NVIDIA 壟斷格局開始鬆動的標誌性事件
- [Big Tech's 'Breathtaking' $660bn Spending Spree Reignites AI Bubble Fears — Irish Times](https://www.irishtimes.com/technology/big-tech/2026/02/06/big-techs-breathtaking-660bn-spending-spree-reignites-ai-bubble-fears/)：6600 億美元 AI 資本支出的泡沫隱憂分析
- [AI Inferencing Will Define 2026, and the Market's Wide Open — SDxCentral](https://www.sdxcentral.com/analysis/ai-inferencing-will-define-2026-and-the-markets-wide-open/)：推理市場如何重塑 AI 硬體競爭格局
- [The $20 Billion Admission: Why NVIDIA Just Bought Into the ASIC Revolution with Groq — Uncover Alpha](https://www.uncoveralpha.com/p/the-20-billion-admission-why-nvidia)：Groq 收購案的深層戰略分析
- [NVIDIA's H200 Chips Re-enter China — But Beijing Isn't Giving Up on Huawei — The Diplomat](https://thediplomat.com/2026/02/nvidias-h200-chips-re-enter-china-but-beijing-isnt-giving-up-on-huawei/)：NVIDIA 中國市場地緣政治困局的最新報導
