---
title: "當中國 AI 的 Token 吞噬量首次超越美國：一場靜悄悄的權力轉移"
date: 2026-02-27
description: "2026 年 2 月，中國 AI 模型在全球最大 API 聚合平台 OpenRouter 的 Token 調用量首次超越美國，四款中國模型霸佔全球前五。這不只是數字遊戲——背後是開源策略、架構創新與極致成本控制的集體爆發，正在重寫全球 AI 的權力地圖。"
tags: [deep-dive, llm, ai-industry, ai-research]
---

## 引言

想像你是一個矽谷的 AI 新創公司創辦人。2026 年 2 月的某個早上，你打開 OpenRouter 的儀表板，準備檢查你的 AI Agent 昨晚跑了多少 Token——然後你愣住了。

全球調用量排名前五的模型裡，有四個名字你一年前幾乎沒聽過：MiniMax M2.5、Kimi K2.5、GLM-5、DeepSeek V3.2。全部來自中國。而你正在用的 Claude Opus 4.6，每百萬 Token 的輸出價格是 MiniMax 的 22.7 倍。

你開始算帳。你的 AI Agent 每天燒掉的 Token 量，用中國模型跑的話，月費從五萬美元直接砍到三千。你的投資人會怎麼想？你的競爭對手是不是已經換了？

這不是假設情境。這是 2026 年 2 月正在發生的事。

全球最大的 AI 模型 API 聚合平台 OpenRouter 的數據顯示，2 月 9 日至 15 日那一週，中國模型以 4.12 萬億 Token 的調用量，**首次超越**同期美國模型的 2.94 萬億 Token。一週後，這個數字飆升至 5.16 萬億，三週內暴漲 127%。截至 2 月 24 日，中國模型已佔據平台總 Token 消耗量的 **61%**。

這篇報導的起點是[《每日經濟新聞》的一篇深度分析](https://www.36kr.com/p/3700980530851712)，但故事遠不止於此。一個數據平台的排名翻轉，背後是一整個產業生態的結構性變化——從 MoE 架構的技術突破、到春節期間數百億人民幣的補貼大戰、到矽谷新創公司悄悄換掉底層模型的現實。這場靜悄悄的權力轉移，值得我們花點時間看清楚。

---

## 事件全貌

### 數字說了什麼

先把時間線拉開來看。2025 年 3 月，OpenRouter 平台前十大模型的週調用量還只有 1.24 萬億 Token。到 2026 年 2 月中旬，這個數字已飆升至 13.95 萬億——不到一年，**成長超過 10 倍**。而在這爆炸性成長中，劇本的主角悄悄換了人。

2025 年全年，美國模型是市場增長的主力，Token 週調用量一度佔據平台前十大模型總量的近七成，中國模型佔比不到兩成。但進入 2026 年，畫風急轉。

2 月第一週，中國模型的週調用量躍升至 2.27 萬億 Token，發出追擊信號。僅僅一週後，就完成了歷史性超越。到 2 月 24 日那一週，前五名的排行是這樣的：

| 排名 | 模型 | 公司 | 週 Token 量 | 週環比 |
|------|------|------|-------------|--------|
| 1 | MiniMax M2.5 | 上海 MiniMax | 2.45 萬億 | +197% |
| 2 | Kimi K2.5 | 月之暗面（Moonshot AI） | 1.21 萬億 | -20% |
| 3 | GLM-5 | 智譜 AI | 7,800 億 | +158% |
| 4 | Claude Sonnet 4.6 | Anthropic | — | — |
| 5 | DeepSeek V3.2 | DeepSeek | — | — |

這裡有一個特別值得注意的事實：OpenRouter 的用戶主體是**海外開發者**，[美國用戶佔比高達 47.17%](https://wealthari.com/chinese-ai-models-capture-majority-of-openrouter-token-volume-as-minimax-m2-5-surges-to-the-top/)，中國開發者僅佔 6.01%。換句話說，這不是中國人在自己家裡刷量——是全球開發者真金白銀地「用腳投票」。

### 四個新面孔

讓我們認識一下這四位新霸主。

**MiniMax M2.5** 是這波浪潮中最耀眼的黑馬。這家上海公司在 2 月 12 日發布了這款模型，上線不到一週就衝上全球第一。它採用 MoE 架構，總參數 2,300 億，但每次推理只啟用 100 億——相當於用 4.3% 的參數量跑出全參數的效果。在 [SWE-Bench Verified](https://www.minimax.io/news/minimax-m25)（軟體工程任務基準）上拿到 80.2 分，BrowseComp（網頁瀏覽代理任務）拿到 76.3 分，都是頂尖水準。

**Kimi K2.5** 來自月之暗面，1 月 27 日發布。它的殺手鐧是 [Agent Swarm](https://www.infoq.com/news/2026/02/kimi-k25-swarm/)——能同時協調最多 100 個子代理並行執行任務，工作流程跨越多達 1,500 個協調步驟。吳恩達評價這個模型代表了「從循序推理到協作任務執行的轉變」。在 BrowseComp 上超越了 GPT-5.2 Pro。

**GLM-5** 來自智譜 AI，2 月 11 日發布。它有一個特別的身份標籤：完全基於**華為昇騰晶片**訓練，不依賴任何 NVIDIA GPU。7,440 億總參數，每次推理啟用 440 億，200K 上下文窗口，以 MIT 開源許可發布。智譜 AI 在香港上市後股價飆升 34%。

**DeepSeek V3.2** 不用多介紹了——這是去年就把全球 AI 產業攪了個天翻地覆的那家公司的最新作品。在 OpenRouter 的累計數據中，[DeepSeek 全系列模型的總 Token 調用量以 14.37 萬億位居全球第一](https://a16z.com/state-of-ai/)。

### 價格戰的震撼

但真正讓開發者「叛變」的不只是性能——是價格。

MiniMax M2.5 的輸入價格是 0.15 美元/百萬 Token，輸出價格是 1.20 美元/百萬 Token。Claude Opus 4.6 呢？輸入 5 美元，輸出 25 美元。簡單算一下：用 MiniMax 跑同樣的任務，[成本只有 Claude 的 1/20](https://venturebeat.com/technology/minimaxs-new-open-m2-5-and-m2-5-lightning-near-state-of-the-art-while)。

連續運行一小時的成本？MiniMax M2.5 是 0.30 美元，M2.5-Lightning 是 1.00 美元，而 Claude Opus 4.6 大約要 20 美元以上。

對一個每天要跑數百萬 Token 的 AI Agent 來說，這個價差不是「省一點」的問題，而是「能不能活下去」的問題。

---

## 脈絡

### DeepSeek 的蝴蝶效應

要理解 2026 年 2 月的這場翻轉，得把時間倒回 2025 年初。

DeepSeek 在 2025 年 1 月的橫空出世，是一切的起點。一家中國公司聲稱只花了 557 萬美元的訓練成本，就訓練出了能與 OpenAI o1 對標的模型——而 o1 的單次訓練成本估計在 6,000 萬美元左右。儘管業界對這個數字有爭議（[實際研發成本估計約 1 億美元](https://www.thirdbridge.com/en-us/about-us/media/perspectives/five-key-questions-the-impact-of-deepseek-s-rise-on-the-ai-industry)），但核心事實無可否認：中國團隊用遠低於美國的成本，達到了接近甚至對標的性能。

這個「DeepSeek 時刻」觸發了一連串連鎖反應。NVIDIA 單日市值蒸發超過 5,000 億美元，創史上最大單日跌幅。OpenAI 加速降價。Google 大幅調降 Gemini Flash 的 API 價格。一場全球性的 AI 價格戰就此拉開。

但更深遠的影響是心理層面的：它打破了「只有砸最多錢、用最好的 GPU 才能做出最強模型」的迷思。中國開發者社區受到極大鼓舞，一大批公司開始加速衝刺。

### MoE：窮人的核武器

中國模型能在成本上碾壓美國對手，核心技術秘密是**混合專家架構（Mixture-of-Experts, MoE）**。

概念其實不複雜：把一個巨大的模型拆成多個小型「專家網路」和一個「門控網路」。模型的總參數量可以非常龐大（維持知識廣度），但每次處理任務時，門控網路只會激活一小部分最相關的專家——「按需開燈，不是全屋照明」。

數字說明一切：

| 模型 | 總參數 | 每次推理啟用 | 啟用比例 |
|------|--------|-------------|---------|
| DeepSeek R1 | 6,710 億 | 370 億 | 5.5% |
| MiniMax M2.5 | 2,300 億 | 100 億 | 4.3% |
| Kimi K2.5 | 1 萬億 | 320 億 | 3.2% |
| GLM-5 | 7,440 億 | 440 億 | 5.9% |
| Qwen 3.5 Plus | 3,970 億 | 170 億 | 4.3% |

這意味著什麼？MoE 架構可以讓推理時的顯存佔用降低 60%，推理吞吐量提升高達 19 倍。當你只需要動用 4% 的參數就能完成任務，單位 Token 的成本自然暴跌。

美國公司不是不知道 MoE——Google 的 [Switch Transformer 早在 2021 年就提出了這個概念](https://arxiv.org/abs/2101.03961)。但中國團隊把它推向了極致，並且在工程層面做了大量優化。字節跳動的火山引擎甚至開發了「潮汐調度」系統，把計算負載分散到離峰時段，[聲稱能在數據中心成本的 10%-20% 交付雲端推理](https://hellochinatech.com/p/china-compute-efficiency-vs-scale)。

### 春節大戰：數百億補貼的背後

2026 年的農曆新年，中國 AI 產業上演了一場補貼大戰，規模之大令人咋舌。

阿里巴巴投入 30 億人民幣（約 4.31 億美元）補貼其 Qwen 系列模型。騰訊砸了 10 億人民幣推「元寶」，拿下超過 5,000 萬日活、1.14 億月活。百度投入 5 億人民幣，月活用戶突破 2 億。字節跳動拿下央視春晚 AI 雲服務獨家合作。[各平台合計補貼規模超過 450 億人民幣（約 63 億美元）](https://www.asiatechlens.com/p/the-chinese-new-year-ai-gateway-war-tencent-bytedance-baidu-alibaba-cny)。

這場「紅包大戰」的目的很明確：搶用戶入口。中國數位化專家 Ashley Dudarenok 指出，這是一場「不可持續的補貼戰」，但短期內確實將數億用戶拉進了 AI 生態。而這些用戶產生的 Token 調用量，直接反映在了 OpenRouter 的全球排行榜上。

阿里還在除夕夜發布了 Qwen 3.5 Plus——3,970 億總參數、僅啟用 170 億，多項指標比肩 GPT-5.2 和 Gemini 3 Pro。根據 [a16z 與 OpenRouter 的聯合報告](https://a16z.com/state-of-ai/)，Qwen 全系列模型的總 Token 調用量以 5.59 萬億位居全球第二，僅次於 DeepSeek。在 Hugging Face 上，Qwen 系列已衍生出超過 18 萬個衍生模型，累計下載量超越了 Meta 的 Llama 系列。

---

## 多方觀點

### 樂觀派：「這是開源的勝利」

a16z 合夥人 Martin Casado 觀察到一個驚人的現象：[「我估計有 80% 的機率，向我們基金投資的新創公司正在使用中國開源模型。」](https://eu.36kr.com/en/p/3440755786126725)

這個數字如果屬實，意味著矽谷最前沿的 AI 新創生態，已經在底層悄悄完成了一次「去美國化」。不是因為政治立場，純粹是因為開源 + 便宜 + 夠用。

OpenRouter COO Chris Clark 提供了一個關鍵洞察：[「中國開源模型在美國企業的代理流程（agentic flows）中佔比不成比例地偏高。」](https://wealthari.com/chinese-ai-models-capture-majority-of-openrouter-token-volume-as-minimax-m2-5-surges-to-the-top/) 也就是說，中國模型特別受歡迎的場景不是日常聊天，而是 AI Agent 自動執行任務——這恰恰是 Token 消耗量最大、成本最敏感的領域。

上海財經大學特聘教授胡延平提出了「AI 中國團」的說法，認為中國有多家頭部企業形成寬廣的技術群落，而不是少數寡頭壟斷，「對於競爭創新和人才生態建設是好事，也有利於在中美 AI 競爭中形成集群優勢」。

### 質疑派：「數字會騙人」

但也有不少冷靜的聲音。

首先，**OpenRouter 不等於全球 AI 市場**。它服務的是 500 多萬開發者，以 API 調用為主。相比之下，OpenAI 的 API 在 2025 年 10 月每日平均處理約 86 億 Token——是 OpenRouter 同期日均量的約 8.6 倍。而且 Claude 在 OpenRouter 的編程工作負載中仍佔超過 60% 的份額，說明在高端、高複雜度的任務上，美國模型仍有優勢。

其次，**新模型上線的蜜月效應**不容忽視。MiniMax M2.5 的 197% 週增長部分受到免費促銷活動驅動，Kilo Code、Cline 等工具提供了免費試用額度。同期 Kimi K2.5 的調用量已經下滑 20%。[Founders Space 的 Steven Hoffman 指出](https://dataconomy.com/2026/02/25/chinese-ai-models-hit-61-market-share-on-openrouter/)：「人們不會看到價值……並在促銷結束後回歸」——長期留存才是真正的考驗。

再來是安全和合規的隱憂。DeepSeek 自動收集 IP 位址、按鍵模式、cookie 並儲存於中國伺服器。中國的《國家情報法》要求中國企業和個人配合國安機構工作。[台灣已對 DeepSeek 等中國 AI 的偏見與數據洩露風險發出警告](https://thehill.com/policy/technology/5126075-chinese-ai-model-raises-national-security-concerns/)。對於處理敏感數據的企業客戶來說，這不是能用「便宜」兩個字帶過的問題。

### 蒸餾風暴：偷來的捷徑？

2 月 23 日，Anthropic 投下了一顆震撼彈。

他們指控三家中國 AI 公司——DeepSeek、月之暗面、MiniMax——通過「蒸餾攻擊」非法複製 Claude 的能力。[根據 Anthropic 的說法](https://techcrunch.com/2026/02/23/anthropic-accuses-chinese-ai-labs-of-mining-claude-as-us-debates-ai-chip-exports/)，這三家公司使用約 24,000 個虛假帳戶，向 Claude 發送了超過 1,600 萬次 API 查詢——其中 MiniMax 佔了 1,300 萬次，目標是提取編程和工具使用能力。

Anthropic 強調，「提示的量、結構和焦點與正常使用模式明顯不同，反映的是蓄意的能力提取，而非合法使用。」OpenAI 同時聲稱發現了類似的「工業規模蒸餾活動」。

這個指控的時機耐人尋味——恰好在中國模型霸榜 OpenRouter 的同一週。它暗示了一個尖銳的問題：這些中國模型的優異表現，有多少是獨立研發的成果，有多少是「站在巨人肩膀上」——而且可能沒經過巨人同意？

知識蒸餾本身是 AI 訓練的常見技術，但用假帳戶進行大規模系統性提取，那就是另一回事了。不過也有分析人士指出，即使蒸餾確實發生，它也無法解釋 MoE 架構創新、推理優化、以及整個工程系統的效率提升——這些是蒸餾學不來的。

### 以我的觀察

站在一個每天都在用這些模型的人的角度，我的看法是：中國模型在 OpenRouter 的爆發是真實的，但需要加上好幾個星號。

首先，61% 的市佔率聽起來嚇人，但很大一部分是由 Agent 自動化工作流驅動的——這類場景對成本極度敏感，自然會往最便宜的模型跑。在需要最高品質推理的場景（複雜程式碼架構、細膩的創意寫作、高風險決策），Claude 和 GPT 仍然是首選。

其次，蒸餾指控是一個值得嚴肅對待的問題。如果中國模型的部分能力確實來自對 Claude 的系統性提取，那麼它們的「成本優勢」就需要被重新定義——你不能把研發費用省下來卻靠偷別人的成果。但另一方面，MoE 架構的創新、開源生態的構建、以及工程優化的深度，這些都是實打實的。

這場競爭的本質不是「誰的模型更強」，而是「AI 算力經濟學的重心在哪裡」。中國團隊用效率換規模，用開源換生態，用價格換市場——這個策略正在奏效。

---

## 產業衝擊

### 第一層：開發者的算帳時刻

對全球 AI 開發者來說，這場變化最直接的衝擊是：**你的 AI 成本結構可能需要重新設計**。

以一個中等規模的 AI Agent 應用為例，如果每天處理 1 億個 Token（這在 agentic 工作流中很常見），用 Claude Opus 4.6 的話月費大約是 15 萬美元。換成 MiniMax M2.5，同樣的工作量只需要不到 8,000 美元。[對於印度等新興市場的 AI 新創公司，月度 API 成本可以從約 5 萬美元直接降到 3,000-5,000 美元](https://siliconcanals.com/sc-n-chinas-deepseek-triggers-global-ai-price-war-as-tech-giants-slash-api-costs/)——這是「能不能創業」和「創不了業」的區別。

根據 a16z 與 OpenRouter 的報告，編程場景已成為最大的 Token 消耗類別。2025 年初，[編程佔 OpenRouter Token 總量約 11%](https://openrouter.ai/state-of-ai)；到 2025 年底至 2026 年初，這個比例已超過 50%。AI Agent 的崛起讓 Token 從「打字費」變成了「燃料費」——你的 Agent 越自動化、越能幹，它燒掉的 Token 就越多。

在這個邏輯下，成本就是生死線。這也是為什麼中國模型在 Agent 場景中的佔比「不成比例地偏高」——不是因為它們更聰明，而是因為在大量消耗 Token 的場景中，10 倍的價差是無法忽視的。

### 第二層：SaaS 與商業模式的地震

中國模型的價格攻勢正在加速 AI 對傳統 SaaS 的衝擊。

[Salesforce 在 2026 財年 Q4 的財報](https://www.36kr.com/p/3700798936460930)給出了一個複雜的信號：營收增速看似提升，但剔除收購並表後原有業務增長乏力。GAAP 經營利潤顯著跑輸預期。在「AI 殺死 SaaS」的敘事下，CRM 這個 SaaS 龍頭正面臨前所未有的估值壓力。

問題的核心在於定價模型的顛覆。傳統 SaaS 按「席位」收費——每個用戶每月多少錢。但當 AI Agent 可以替代人工完成大量工作時，「席位」的概念就變得模糊了。你需要為一個 AI Agent 付席位費嗎？

國聯民生證券提出的「Token 通膨」概念精準地描述了這個轉變：單位時間內、單位用戶的 Token 消耗在結構性上升。這不是因為 Token 變貴了，而是因為 AI 在做的事情越來越重——從簡單問答到重構程式碼、生成文檔、跑測試、執行多步驟推理。

[Deloitte 的研究指出](https://www.deloitte.com/us/en/insights/topics/emerging-technologies/ai-tokens-how-to-navigate-spend-dynamics.html)，某些企業的 AI 消費已達 IT 支出的 50%，但只有 28% 的全球財務主管表示從 AI 投資中看到清晰可衡量的價值。AI 的商業模式正在從「按量計費」向「燃料 + 成果」的混合模式演進——而中國模型的低價策略，正在加速這個轉型的到來。

### 第三層：晶片產業的矛盾

這裡出現了一個有趣的悖論：中國 AI 模型越成功，它們對高端 GPU 的需求就越大——而這些 GPU 正是美國試圖禁運的。

根據外交關係委員會（CFR）的分析，在完全禁運場景下，美國相對中國的 AI 算力優勢約為 [21-49 倍](https://www.cfr.org/article/chinas-ai-chip-deficit-why-huawei-cant-catch-nvidia-and-us-export-controls-should-remain)。華為的昇騰晶片目前的實際推理性能約為 NVIDIA H100 的 60%，而且受制於中芯國際的 7nm 製程，無法在短期內追平。CFR 的評估很直接：「華為不是正在崛起的競爭者。相反，它正在進一步落後。」

但與此同時，中國團隊正在用軟體層面的效率優化來彌補硬體差距。MoE 架構本質上就是「用更少的算力做更多的事」。這也解釋了一個看似矛盾的現象：中國在 AI 算力投資上遠落後於美國（2025 年約 570 億美元 vs 美國約 4,000 億美元，[比例 1:3.5](https://hellochinatech.com/p/china-compute-efficiency-vs-scale)），但模型的實際表現卻在快速追平。

NVIDIA CEO 黃仁勋在 2 月 26 日的業績電話會上反覆強調「計算即收入」「推理即收入」，認為每一個 Token 的生成都需要算力支撐。但中國的回答是：同樣的 Token，我用更少的算力就能生成。

Meta 最近也做了一個耐人尋味的動作——[放棄了代號 Iris 和 Olympus 的兩款自研訓練晶片](https://www.36kr.com/p/3700868248284809)，轉而擁抱 Google TPU。連全球第二大 AI 公司都覺得自研晶片的風險太大，這從側面說明了 NVIDIA 的護城河——但也說明了晶片之外的效率創新空間有多大。

### 第四層：二階效應

中國模型霸榜帶來的連鎖反應正在多個層面展開。

**價格螺旋加速**。當中國模型把 Token 價格打到地板，美國公司不得不跟進降價，這反過來壓縮了所有人的利潤空間。OpenAI 已經在加速推出低價方案，Google 大幅調降 Gemini Flash 的價格。整個 AI API 市場正在經歷一場殘酷的價格戰，最終受益的是開發者和終端用戶。

**地緣政治升溫**。美國國會議員 Moolenaar 和 Krishnamoorthi 已經呼籲禁止聯邦政府採購基於中國模型的 AI 系統。同時出現了 AI Overwatch Act，要求對 AI 出口進行類似軍售的國會審查。中國 AI 的商業成功正在轉化為政治壓力——這可能反過來加速「技術脫鉤」。

**開源生態的重心轉移**。在 Hugging Face 的開源模型排行榜上，[全球排名前 16 的開源模型全部來自中國](https://eu.36kr.com/en/p/3440755786126725)。排名最高的非中國模型排在第 17 位。阿里的 Qwen 系列在 Hugging Face 的累計下載量已超越 Meta 的 Llama 系列。開源 AI 的重心正在從美國滑向中國，這對全球 AI 生態的長期影響深遠。

**全球南方的翻身機會**。對於印度、東南亞、非洲等新興市場的開發者來說，中國模型的低價 API 意味著前所未有的創業機會。過去只有矽谷團隊才負擔得起的 AI 能力，現在任何人都能用。[DeepSeek 在非洲的興趣水平是其他地區的 2-4 倍](https://capacityglobal.com/news/deepseek-one-year-later-china-global-ai-race/)——全球 AI 的民主化正在以出乎意料的方式推進。

---

## 未來展望

### 短期（3-6 個月）：幾乎確定會發生的事

**價格戰繼續白熱化**。摩根大通預測，從 2025 年到 2030 年，[中國 Token 消耗量的年復合增長率將達到 330%](https://www.36kr.com/p/3700980530851712)，五年間實現 370 倍的增長。在這個增長曲線上，價格只會持續下降。Claude、GPT 等美國模型的 API 價格會繼續下調，利潤空間被進一步壓縮。

**蒸餾爭議持續發酵**。Anthropic 和 OpenAI 的指控不會止步於聲明，預計會有法律行動。美國政界可能以此為由推動對中國 AI 模型的限制措施。但技術層面上，防止模型蒸餾極其困難——這是一場貓鼠遊戲。

**更多中國模型進入全球開發者視野**。目前 OpenRouter 上的四大中國模型只是冰山一角。阿里的 Qwen、字節跳動的豆包、百度的文心一言都有海外擴張的野心。預計 3-6 個月內，中國模型在全球 API 市場的佔比會從目前的 61% 繼續攀升。

### 中期（6-18 個月）：三種可能的發展路徑

**情境一：效率為王**。中國模型繼續在成本效率上領跑，全球開發者大規模遷移到中國模型的 API。美國公司被迫走向更深的垂直化——專注於高端、高品質、差異化的應用場景，放棄通用 API 市場的價格競爭。AI 行業出現類似智慧手機市場的分層：「蘋果」（高端少量）vs「安卓」（低價大量）。

**情境二：鐵幕落下**。地緣政治壓力導致美國對中國 AI 模型實施使用限制，類似 TikTok 禁令的邏輯。企業被迫在「便宜但有合規風險」和「貴但安全」之間做選擇。AI 生態進一步分裂為兩個平行世界——但這會顯著推高全球 AI 應用的成本。

**情境三：融合競爭**。美國公司加速自己的開源和降價策略（Meta 的 Llama 持續進化，Google 開放更多模型），同時中國公司在資料安全和合規上做出讓步。全球開發者在多模型之間靈活切換，形成一個更多元、更競爭、整體成本更低的生態。以我的判斷，這是最可能的結局——但過程會很混亂。

### 長期推演：3-5 年後的世界

如果這個趨勢持續下去，3-5 年後的 AI 產業格局會是什麼樣子？

Token 的價格會趨近於電力的邊際成本。當 MoE 架構和推理優化被推到極致，Token 的生成成本主要取決於兩件事：晶片的計算效率和數據中心的電力成本。就像雲端運算的價格在過去十年持續下降一樣，Token 的價格也會走同樣的路。

AI 的競爭焦點會從「模型能力」轉向「應用生態」和「數據飛輪」。當基礎模型變成廉價的商品化基礎設施，真正的護城河在於：你能用這些模型做什麼？你有什麼獨特的數據？你的用戶黏性在哪裡？

中美在 AI 領域的競爭會從「誰的模型更強」變成「誰的生態更深」。美國可能在基礎研究和前沿能力上保持領先（DeepMind CEO Demis Hassabis 估計[差距「僅有數月」](https://vertu.com/lifestyle/the-global-ai-race-why-china-is-just-months-behind-the-us-according-to-deepminds-ceo/)），但中國在應用落地、用戶規模和成本效率上的優勢會持續擴大。

### 給讀者的建議

**如果你是開發者**：現在就開始測試中國的開源模型。不是為了政治正確，而是為了經濟理性。在你的多模型路由策略中加入 MiniMax M2.5、Kimi K2.5 或 Qwen 3.5 Plus，對於非敏感、高 Token 消耗的 Agent 場景，成本節約是實打實的。但對於涉及客戶敏感數據的場景，仍然需要仔細評估安全和合規風險。

**如果你是創業者**：重新算你的 AI 成本假設。如果你的商業模式建立在「AI API 很貴所以只有少數人用得起」的前提上，這個前提正在被打破。反過來說，如果你能利用低成本 API 構建以前不可能的產品——現在是最好的時機。

**如果你是一般科技從業者**：理解「Token 經濟學」比理解任何單一模型都重要。AI 正在從一個「能力問題」變成一個「經濟學問題」——不是「AI 能不能做」，而是「AI 做這件事劃不划算」。當 Token 的價格持續下降，越來越多的人類工作會被 AI 取代——不是因為 AI 變聰明了，而是因為 AI 變便宜了。

2026 年 2 月的這場 Token 戰爭，表面上是幾家中國公司在一個 API 平台上的排名超車。但往深處看，它折射出的是 AI 產業從「軍備競賽」走向「效率革命」的結構性轉折。在這場轉折中，有人會發財，有人會失業，有人會找到前所未有的機會。

唯一確定的是：Token 的價格只會更便宜，AI 的滲透只會更深。準備好了嗎？

---

## 延伸閱讀

- [Chinese AI Models Capture Majority of OpenRouter Token Volume — Wealthari](https://wealthari.com/chinese-ai-models-capture-majority-of-openrouter-token-volume-as-minimax-m2-5-surges-to-the-top/)：最完整的 OpenRouter 數據分析，包含用戶結構和調用趨勢細節
- [State of AI: An Empirical 100 Trillion Token Study — a16z × OpenRouter](https://a16z.com/state-of-ai/)：a16z 和 OpenRouter 聯合發布的年度 AI 使用報告，開源模型佔比和中國模型崛起的數據基礎
- [MiniMax M2.5: Built for Real-World Productivity — MiniMax 官方](https://www.minimax.io/news/minimax-m25)：理解 MiniMax M2.5 的技術架構和 Forge 強化學習框架
- [Moonshot AI Releases Open-Weight Kimi K2.5 — InfoQ](https://www.infoq.com/news/2026/02/kimi-k25-swarm/)：深入解析 Kimi K2.5 的 Agent Swarm 技術和多代理並行架構
- [China's AI Chip Deficit: Why Huawei Can't Catch NVIDIA — CFR](https://www.cfr.org/article/chinas-ai-chip-deficit-why-huawei-cant-catch-nvidia-and-us-export-controls-should-remain)：美國外交關係委員會對中國 AI 晶片差距的硬核分析
- [Anthropic Accuses Chinese AI Labs of Mining Claude — TechCrunch](https://techcrunch.com/2026/02/23/anthropic-accuses-chinese-ai-labs-of-mining-claude-as-us-debates-ai-chip-exports/)：蒸餾爭議的第一手報導
- [China's Compute Bet: Can Efficiency Replace Scale? — HelloChinaTech](https://hellochinatech.com/p/china-compute-efficiency-vs-scale)：深入分析中國 AI 團隊如何用效率換規模的策略
- [AI Tokens: How to Navigate AI's New Spend Dynamics — Deloitte](https://www.deloitte.com/us/en/insights/topics/emerging-technologies/ai-tokens-how-to-navigate-spend-dynamics.html)：Deloitte 對 Token 經濟和企業 AI 支出動態的研究報告
