---
title: "Cursor 偷偷用了 Kimi、亞馬遜晶片搶客戶、騰訊 AI Lab 走入歷史"
date: 2026-03-23
description: "Cursor Composer 2 被抓包基於中國 Kimi 模型打造，亞馬遜 Trainium 晶片拿下 Anthropic、OpenAI、Apple，騰訊解散 AI Lab 全力押注混元 3.0"
tags: [llm, ai-tools, ai-industry, ai-coding]
---

今天的浪有點精彩——Cursor 被抓包偷偷用了中國的開源模型，亞馬遜的自研晶片悄悄拿下了半個 AI 圈的大客戶，而騰訊直接把十年老店 AI Lab 給收了。三件事背後講的其實是同一件事：AI 競爭進入深水區，誰也裝不了了。

---

## 🌊 今日浪頭

### [Cursor admits its new coding model was built on top of Moonshot AI's Kimi](https://techcrunch.com/2026/03/22/cursor-admits-its-new-coding-model-was-built-on-top-of-moonshot-ais-kimi/)

這件事太有戲了。Cursor 本週風光發布 Composer 2，號稱「frontier-level coding intelligence」，結果被一個 X 上的用戶翻出程式碼裡藏著 Kimi 的模型 ID——直接被抓包是基於月之暗面的開源模型 Kimi-k2.5 訓練的。Cursor VP Lee Robinson 倒也爽快承認了：「對，我們從開源基底出發」，但強調四分之三的算力都花在自家訓練上。共同創辦人 Aman Sanger 也坦言「沒在 blog 裡提到 Kimi 是我們的疏忽」。

**為什麼這道浪值得追：**
- 一家估值 293 億美元、年化營收破 20 億的美國 AI 獨角獸，底層用的是中國公司的開源模型——在當前中美 AI 軍備競賽的氛圍下，這劇情比電影還精彩
- 月之暗面的反應很聰明，直接在 X 上恭喜 Cursor，強調這就是開源生態該有的樣子
- 這件事說明了一個趨勢：AI 時代的競爭不再是「從零開始誰做得好」，而是「誰能在開源基底上跑得最快」。Cursor 的護城河不在模型本身，而在產品體驗和 RL 訓練的 know-how

### [An exclusive tour of Amazon's Trainium lab, the chip that's won over Anthropic, OpenAI, even Apple](https://techcrunch.com/2026/03/22/an-exclusive-tour-of-amazons-trainium-lab-the-chip-thats-won-over-anthropic-openai-even-apple/)

TechCrunch 拿到了亞馬遜 Trainium 晶片實驗室的獨家探訪機會，看完之後我覺得 Nvidia 應該要緊張了。目前已經部署了 140 萬顆 Trainium 晶片，其中光是 Anthropic 的 Claude 就跑在超過 100 萬顆 Trainium2 上面。更猛的是，亞馬遜剛跟 OpenAI 簽了 500 億美元的投資協議，承諾提供 2GW 的 Trainium 算力——這個數字大到 Anthropic 和 Bedrock 已經在搶著用都還不夠。

**為什麼這道浪值得追：**
- Trainium3 搭配新的 Neuron 交換器，號稱成本比同級雲端伺服器低 50%——當推論吃掉九成電力時，這個數字是殺手級的
- PyTorch 支援只需「改一行程式碼就能跑」，直接瞄準 Nvidia 的生態護城河
- Bedrock 負責人說了句狠話：「Bedrock 有一天可能跟 EC2 一樣大」——如果這成真，亞馬遜就不只是雲端老大，而是 AI 基礎設施的絕對霸主

### [騰訊 AI 合二為一，姚順雨第一個大模型混元 3.0 穩了？](https://www.36kr.com/p/3733678160229127)

騰訊做了一個很有意思的決定：直接把成立十年的 AI Lab 解散了，人員全部併入混元大模型團隊，由首席 AI 科學家姚順雨統一指揮。沒有公告、沒有解釋，就這樣消失了。但這其實不意外——過去一年騰訊的 AI 團隊一直在重組，馬化騰年會上也坦承「AI 動作慢了」。現在混元 3.0 計畫四月推出，推理和 Agent 能力都有大幅提升。

**為什麼這道浪值得追：**
- 這不只是騰訊的事——字節把 AI Lab 併進 Seed 團隊、阿里把通義併入 Token 事業群，中國大廠正在集體拋棄「獨立 AI 實驗室」模式
- 姚順雨（普林斯頓博士、前 OpenAI 研究員）成為騰訊 AI 的絕對核心，2026 年 AI 投資至少翻倍
- 背後的邏輯很清楚：大模型時代，研究和工程不能分家。分散的實驗室只會製造內耗，所有資源必須集中到一條主線上快速迭代

---

## ⚡ 衝浪快報

- **[Musk says he's building Terafab chip plant in Austin, Texas](https://www.theverge.com/ai-artificial-intelligence/898722/musk-terafab-chip-plant)** — 馬斯克又開大餅了：Tesla/SpaceX/xAI 聯手蓋晶片廠，2nm 製程。不過以他的時程承諾記錄，先保持觀望
- **[Tinybox – Offline AI device 120B parameters](https://tinygrad.org/#tinybox)** — tinygrad 的本地 AI 裝置能跑 1200 億參數模型，HN 348 分。離線跑大模型這件事正在從概念變成產品
- **[Nvidia has an OpenClaw strategy. Do you?](https://techcrunch.com/podcast/nvidia-has-an-openclaw-strategy-do-you/)** — GTC 回顧：黃仁勳預測 AI 晶片 2027 年銷售破兆美元，OpenClaw 正在從玩具變成企業基礎設施
- **[字節 Seedance 2.0 版權危機：為什麼 OpenAI 和 Anthropic 打得贏，字節卻打不贏？](https://www.36kr.com/p/3733929335681798)** — Seedance 2.0 因為拿好萊塢素材訓練被美國電影協會盯上，全球發布暫停。中美 AI 公司在版權戰的待遇差異值得玩味
- **[OpenAI 急招 3500 人反擊](https://www.36kr.com/p/3733799671906307)** — 逆轉之前的縮編計畫，大舉招人補強企業端。看來 Anthropic 和 Google 給的壓力不小
- **[小米 MiMo 團隊揭秘](https://www.36kr.com/p/3730857172238601)** — MiMo-V2-Pro 登上 OpenRouter 調用量榜首，核心團隊幾乎清一色北大精英。小米在模型層的進度比很多人預期的快
- **[AI 應用留不住付費用戶](https://www.36kr.com/p/3733944534040839)** — 數據扎心：AI 應用年度付費留存率只有 21%，比非 AI 應用低 30%。AI 原生產品的變現之路還很長
- **[歐洲資深記者因 AI 生成引言遭停職](https://www.theguardian.com/technology/2026/mar/20/mediahuis-suspends-senior-journalist-over-ai-generated-quotes)** — 用 AI 捏造採訪內容被抓包，新聞業的 AI 倫理紅線越來越清晰
- **[AI 對遊戲開發就業的衝擊](https://darkounity.com/blog-post?id=the-impact-of-ai-on-game-dev-jobs-open-to-work-crisis--1774128585922)** — 大量美術和程式崗位消失，業界正經歷一場靜悄悄的求職寒冬
- **[出版社下架恐怖小說《Shy Girl》](https://arstechnica.com/ai/2026/03/hachette-pulls-shy-girl-horror-novel-after-concerns-about-ai-use/)** — Hachette 出手了，作者否認但多方指控使用 AI 寫作。出版業的 AI 溯源技術戰才剛開始
- **[GDC 2026：AI 無處不在，但遊戲裡看不到](https://www.theverge.com/games/897982/gdc-2026-ai-game-developer-conference)** — AI 工具商攤位擠爆，但真正用 AI 做出創新玩法的遊戲？幾乎沒有。工具有了，創意還沒跟上

---

## 🏄 深水區

- **[Thinking Fast, Slow, and Artificial: How AI Is Reshaping Human Reasoning](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6097646)** — 這篇 SSRN 論文探討 AI 如何改變人類的快思慢想機制，HN 上引發激烈討論。如果你關心 AI 對人類認知的深層影響，這篇值得花時間讀
- **[Using Git with coding agents](https://simonwillison.net/guides/agentic-engineering-patterns/using-git-with-coding-agents/)** — Simon Willison 整理了與 AI 程式代理協同使用 Git 的實戰模式。每天在用 AI 寫 code 的人，這篇是必讀
- **[Profiling Hacker News users based on their comments](https://simonwillison.net/2026/Mar/21/profiling-hacker-news-users/)** — 用 AI 分析 HN 留言自動生成用戶側寫，有趣但也有點毛骨悚然。隱私和 AI 的邊界在哪裡？
- **[Build a Domain-Specific Embedding Model in Under a Day](https://huggingface.co/blog/nvidia/domain-specific-embedding-finetune)** — NVIDIA x HuggingFace 的實作教學，一天搞定領域專屬 Embedding 模型。做 RAG 的人值得收藏
- **[What's New in Mellea 0.4.0 + Granite Libraries Release](https://huggingface.co/blog/ibm-granite/granite-libraries)** — IBM Granite Libraries 正式發布，面向企業 AI 應用的新工具鏈。IBM 在企業端的 AI 佈局比想像中積極
