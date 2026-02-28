---
title: "OpenAI 狂收 1100 億美元、Trump 封殺 Anthropic、中國模型 Token 量全球反超"
date: 2026-02-28
description: "OpenAI 拿下史上最大私募融資 1100 億美元，Amazon、NVIDIA、軟銀聯手押注；Trump 下令全面封殺 Anthropic 聯邦合約；中國開源模型在 OpenRouter 調用量首超美國，四款中國模型佔據全球前五。"
tags: [llm, ai-industry, agents]
---

今天 AI 圈不是浪，是海嘯——OpenAI 一口氣吞下 1100 億美元，直接改寫私募融資史；Trump 親自下場對 Anthropic 開炮，命令聯邦機構全面停用 Claude；而在太平洋另一邊，中國開源模型在全球 API 平台的 Token 消耗量悄悄超過了美國。三件事串在一起看，AI 產業的權力格局正在以月為單位重新洗牌。

---

## 🌊 今日浪頭

### [OpenAI 融資 1100 億美元，Amazon 投 500 億、NVIDIA 軟銀各 300 億](https://techcrunch.com/2026/02/27/openai-raises-110b-in-one-of-the-largest-private-funding-rounds-in-history/)

這個數字已經不是「融資」，是「造國」。OpenAI 一次拿下 1100 億美元，估值 7300 億，Amazon 單筆就砸了 500 億（首期 150 億，剩下 350 億要看 OpenAI 能不能達到 AGI 里程碑或 IPO）。NVIDIA 和軟銀各投 300 億。而且這輪還沒結束，OpenAI 說「歡迎更多投資者加入」。上一輪 400 億已經是史上最大私募了，這次直接把紀錄翻了將近三倍。

更值得注意的是交易背後的基建綁定：Amazon 的投資換來 OpenAI 在 AWS Bedrock 上建「stateful runtime environment」，承諾消耗至少 2GW 的 AWS Trainium 算力，還要幫 Amazon 消費產品做客製化模型。NVIDIA 那邊是 3GW 推論容量加 2GW Vera Rubin 訓練。這些不只是投資，是把 OpenAI 的命運跟這些基建巨頭焊死在一起。

**為什麼這道浪值得追：**
- ChatGPT 週活 9 億、付費用戶超 5000 萬——這些數字解釋了為什麼投資人敢砸這種天文數字，使用者規模已經到了「不投就被別人投走」的地步
- Amazon 的 350 億有條件款跟 AGI 里程碑綁定，這可能是第一次有大型投資合約把 AGI 當成可量化的商業指標
- 1100 億聽起來瘋狂，但如果 OpenAI 的基建承諾都是「以服務抵投資」，實際現金可能比帳面數字低不少——只是精確比例沒公開

### [Trump 下令全面封殺 Anthropic，指控其「挾持五角大廈」](https://www.theverge.com/policy/886489/pentagon-anthropic-trump-dod)

昨天的最後通牒，今天有了答案——而且比所有人預想的都更激烈。Trump 在 Truth Social 直接開罵，說 Anthropic 是「激進左派瘋子公司」，命令所有聯邦機構「立即停止使用」Anthropic 的技術，給了六個月過渡期。措辭之強硬，直接威脅「動用總統全部權力」追究民事和刑事責任。

事情的核心沒變：Dario Amodei 拒絕接受國防部長 Hegseth 的新條款，那份條款會讓軍方可以把 Claude 用在大規模國內監控和全自主致命武器上。OpenAI 和 xAI 據報已經接受了，但有趣的是 OpenAI 也在試著跟五角大廈談，想採用跟 Anthropic 一樣的紅線。Google 和 OpenAI 員工聯名公開信力挺 Anthropic 的立場。Dario 的回應依然硬：「這些威脅不會改變我們的立場。」

**為什麼這道浪值得追：**
- 這已經從商業糾紛升級成政治事件——總統親自下場，把 AI 公司的使用條款拉到國安高度
- Anthropic 的聯邦合約不是小數目，六個月過渡期意味著大量政府 AI 專案要緊急遷移到其他平台
- 最微妙的是 OpenAI 的態度：表面接受新條款，暗地裡想談回 Anthropic 的紅線——這說明連 Sam Altman 都不太舒服全自主武器這條路

### [中國 AI 模型 Token 調用量首超美國，全球前五佔四席](https://www.36kr.com/p/3701403165487494)

OpenRouter 平台的數據不會騙人：2 月第三週，中國模型 Token 調用量 5.16 萬億，美國只有 2.7 萬億。全球前五名裡中國佔了四個——MiniMax M2.5、Kimi K2.5、智譜 GLM-5、DeepSeek V3.2。一年前中國模型在這個平台的份額不到 2%。

但這不只是「便宜」的故事。Agent 時代來了，Token 消耗從「對話式」暴增到「流程式」——一個 OpenClaw Agent 跑一天可以吃掉 200 美元 API 費。在這種規模下，Claude 輸出價 15 美元 / 百萬 Token vs MiniMax 1.1 美元，差距是 13.6 倍。一家歐洲工作室的做法很典型：80% 日常用 Kimi，20% 硬骨頭丟給 Claude，月成本從 1500 美元壓到 300 美元以下。

更深層的變化是：中國模型不只是便宜，工程成熟度已經到了生產級。MiniMax 的 Forge 框架把 Agent 強化學習做到原生適配，訓練加速 40 倍；Kimi K2.5 支援 100 個 Agent 分身並行。智譜甚至開始漲價了——GLM Coding Plan 漲 30% 起，上線即售罄。從價格戰進入需求戰，這是質變。

**為什麼這道浪值得追：**
- a16z 合夥人 Martin Casado 透露：用開源模型的美國 AI 新創中，約 80% 跑的是中國模型——這不是 benchmark 刷分，是真金白銀的生產選擇
- Agent 場景讓 Token 消耗呈指數增長，成本敏感度被極端放大，中國模型的價格優勢從「省點錢」變成「決定生死」
- 四家不同團隊（MiniMax、月之暗面、智譜、DeepSeek）同時上榜，說明這不是單一爆款帶節奏，是整個生態的成熟

---

## ⚡ 衝浪快報

- **[xAI 創始團隊大出走：12 人走了 7 個，11 人在 2 月離職](https://www.36kr.com/p/3701395448639617)** — 馬斯克的 AI 夢工廠正在失血，Grok 核心成員 Jiayi Pan 和 Toby Pohlen 48 小時內先後離開，後者還在 X 上陰陽怪氣「沒人比你們更能熬夜」
- **[DeepSeek 發布 DualPath：解決 Agent 推論的 KV 快取瓶頸](https://www.36kr.com/p/3701088020721285)** — 雙路徑載入機制，基本消除 KV 快取 I/O 開銷，這對長流程 Agent 任務是很實際的效能突破
- **[AlphaEvolve 再進化：DeepMind 讓 AI 自動「繁殖」演算法，碾壓人類設計](https://www.36kr.com/p/3701367240519813)** — 用 Gemini 當遺傳算子，讓演算法源碼像基因組一樣進化，結果找到人類研究者根本想不到的反直覺解法
- **[Google Nano Banana 2 全面上線，Pro 級能力 Flash 級速度](https://www.36kr.com/p/3701204558638727)** — 在競技場上超了自家 Pro 版 100 分，主打一個「自己的王座自己搶」
- **[阿里千問將在 MWC 發布 AI 眼鏡，年內還有 AI 指環和耳機](https://www.36kr.com/p/3701435292053637)** — 從春節 APP 大戰直接跳到硬體卡位，千問要做「軟硬一體、跨終端」的 AI 助手
- **[庞若鸣加入 Meta 僅 7 個月就跳槽 OpenAI](https://www.36kr.com/p/3701251069522693)** — 當初蘋果 AI 團隊的核心人物被 Meta 用 2 億美元挖走，現在又被 OpenAI 截胡——Meta 的 AI 人才留不住問題越來越嚴重
- **[ChatGPT 週活躍用戶突破 9 億](https://techcrunch.com/2026/02/27/chatgpt-reaches-900m-weekly-active-users/)** — 配合 1100 億融資一起公布，付費用戶超過 5000 萬，這使用者規模已經是 app 等級的存在
- **[Perplexity 發布 Computer：「統一所有 AI 能力的單一系統」](https://techcrunch.com/2026/02/27/perplexitys-new-computer-is-another-bet-that-users-need-many-ai-models/)** — 又一個押注「多模型聚合」的產品，Perplexity 想把搜尋、生成、Agent 全部打包
- **[AI 音樂平台 Suno 達到 200 萬付費用戶、ARR 3 億美元](https://techcrunch.com/2026/02/27/ai-music-generator-suno-hits-2-million-paid-subscribers-and-300m-in-annual-recurring-revenue/)** — 用自然語言生成音樂的商業模式被驗證了，3 億 ARR 在 AI 應用層裡算是頂級成績
- **[GitHub Copilot CLI 實戰指南：從 idea 到 PR 的完整工作流](https://github.blog/ai-and-ml/github-copilot/from-idea-to-pull-request-a-practical-guide-to-building-with-github-copilot-cli/)** — GitHub 官方出的 CLI 教學，對在終端機工作的開發者來說值得翻一翻

---

## 🏄 深水區

- **[An AI agent coding skeptic tries AI agent coding, in excessive detail](https://simonwillison.net/2026/Feb/27/ai-agent-coding-in-excessive-detail/#atom-everything)** — Max Woolf 從懷疑論者的視角，一步步記錄他用 coding agent 做越來越大膽的專案，讀完你會對「agent 到底能幹嘛」有很具體的體感
- **[On NVIDIA and Analyslop](https://www.wheresyoured.at/on-nvidia-and-analyslop/)** — Ed Zitron 回歸，這次對準 NVIDIA 財報背後的敘事泡沫和分析師的盲從，觀點犀利，不管你同不同意都值得讀
- **[Agentic Engineering Patterns: Hoard things you know how to do](https://simonwillison.net/guides/agentic-engineering-patterns/hoard-things-you-know-how-to-do/#atom-everything)** — Simon Willison 的 Agent 工程模式系列新篇，核心觀點是「把你會做的事情囤起來」，寫 Agent 最關鍵的其實是你自己的知識庫
- **[從最頂級的 30 個 AI Agent 產品裡，看懂了三個趨勢](https://www.36kr.com/p/3701445354074249)** — MIT、哈佛、史丹佛團隊用 45 個維度拆解了 30 個 Agent 系統，如果你想知道 Agent 產業走到哪了，這份報告是最新最全的
