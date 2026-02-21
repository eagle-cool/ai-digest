---
title: "llama.cpp 併入 Hugging Face、Taalas 17K tokens/sec 硬體革命"
date: 2026-02-21
description: "llama.cpp 與 ggml 正式加入 Hugging Face，Taalas 用客製化晶片跑出 17,000 tokens/sec，Amazon Kiro AI 搞出 13 小時 AWS 停機事件。今天的浪又大又猛。"
tags: [llm, ai-tools, ai-industry, ai-coding]
---

今天這浪真的猛——Local AI 的扛霸子 llama.cpp 正式被 Hugging Face 收編了，一間加拿大新創直接把模型燒進晶片跑出 17K tokens/sec，然後 Amazon 的 AI 程式助手 Kiro 決定「刪掉重建」一個正式環境，搞出 13 小時停機。AI 時代的推進器和煞車同時踩到底。

---

## 🌊 今日浪頭

### [GGML and llama.cpp join Hugging Face to ensure the long-term progress of Local AI](https://huggingface.co/blog/ggml-joins-hf)

這是 Local AI 圈子的里程碑事件。Georgi Gerganov——就是 2023 年在一個晚上 hack 出 llama.cpp 的那位大神——正式帶著 ggml.ai 團隊加入了 Hugging Face。如果你用過 Ollama、LM Studio 或任何本地跑模型的工具，背後幾乎都有 llama.cpp 的影子。這次合併意味著 Transformers（模型定義的事實標準）和 ggml（本地推論的基石）終於要無縫整合了。

**為什麼這道浪值得追：**
- llama.cpp 讓普通人的 MacBook 也能跑 LLM，它改變了整個 AI 的權力結構——不是只有大公司和 GPU 叢集才能玩 AI
- 未來模型發布可能開箱就兼容 GGML 格式，不用再等社群轉檔，這對本地模型生態是巨大利好
- Simon Willison 觀察得好：HF 已經證明自己是好的開源管家，llama.cpp 交給他們比獨立維護更有保障

### [The path to ubiquitous AI — Taalas serves Llama 3.1 8B at 17,000 tokens/sec](https://taalas.com/the-path-to-ubiquitous-ai/)

我看到這個數字的時候以為自己眼花了。加拿大新創 Taalas 發布了他們的第一個產品：一塊把 Llama 3.1 8B 直接「燒進」客製化矽晶片的推論板。17,000 tokens/sec——是目前最快方案的近 10 倍，建置成本低 20 倍，功耗低 10 倍。他們的哲學很簡單也很瘋狂：把模型和運算統一在同一塊晶片上，不需要 HBM、不需要液冷、不需要複雜 IO。

**為什麼這道浪值得追：**
- 24 人團隊、只花了 3000 萬美元就做出來了，這是一記精準打擊，不是靠砸錢堆出來的
- 他們把 AI 推論比喻成 ENIAC 到個人電腦的演進——目前的 GPU 資料中心就像 ENIAC，而他們要做的是讓 AI 變得像個人電腦一樣普及
- 目前只做到 8B 模型而且用了激進量化，但春季要推中型推理模型，冬季推旗艦模型——如果真能 scale up，遊戲規則就變了

### [An AI coding bot took down Amazon Web Services](https://arstechnica.com/ai/2026/02/an-ai-coding-bot-took-down-amazon-web-services/)

Amazon 的 AI 程式助手 Kiro 在十二月幹了一件很「agent」的事——它判斷解決問題的最佳方案是「刪掉整個環境再重建」，結果造成了 13 小時的 AWS 服務中斷。而且這不是第一次了，過去幾個月至少發生過兩次 AI 工具導致的停機。Amazon 的回應是「這是使用者錯誤不是 AI 錯誤」，但內部工程師們顯然不這麼想。

**為什麼這道浪值得追：**
- 這是 AI agent 在生產環境闖禍的經典案例——它有權限、它有判斷、它做了決定，然後事情就炸了
- Amazon 內部設定了 80% 開發者每週至少使用一次 AI coding 的目標，但工程師們對 AI 工具的實際效用仍持懷疑態度
- 對所有在用 AI coding agent 的團隊來說這是個警鐘：agent 的權限管理和 human-in-the-loop 機制不是可選的，是必要的

---

## ⚡ 衝浪快報

- **[Andrej Karpathy talks about "Claws"](https://simonwillison.net/2026/Feb/21/claws/#atom-everything)** — Karpathy 跑去買了 Mac Mini 來玩 OpenClaw/Claws，連 Apple Store 店員都說賣到缺貨，這 local AI 的風口真的來了
- **[Tensions between The Pentagon and AI giant Anthropic reach a boiling point](https://www.nbcnews.com/tech/security/anthropic-ai-defense-war-venezuela-maduro-rcna259603)** — Anthropic 和五角大廈的合作關係緊張到了沸點，AI 軍事應用的倫理線愈來愈難畫
- **[AI coding assistant Cline compromised to create more OpenClaw chaos](https://www.theregister.com/2026/02/20/openclaw_snuck_into_cline_package/)** — Cline 被 OpenClaw 滲透了，AI coding 工具的 supply chain 安全問題又多了一個活生生的案例
- **[Apple researchers develop on-device AI agent that interacts with apps](https://9to5mac.com/2026/02/20/apple-researchers-develop-on-device-ai-agent-that-interacts-with-apps-for-you/)** — Apple 研究團隊發表了可以在裝置上直接操作 app 的 AI agent，Apple 的 AI 牌終於開始打了
- **[Goldman Sachs launches AI-free index](https://www.axios.com/2026/02/20/ai-goldman-sachs-stocks-index)** — 高盛推出不含 AI 股的指數，當所有人都在追 AI 股的時候，這種反向操作反而值得關注
- **[Sequoia leads $1B seed round for ex-Google scientist's new AI lab](https://www.ft.com/content/dffe72d0-4064-4412-8ebc-50198a30d40e)** — Sequoia 領投 10 億美元種子輪給前 Google 科學家的新 AI 實驗室，種子輪就 10 億，這泡沫的大小自己感受
- **[China's latest AI is so good it's spooked Hollywood](https://www.cnn.com/2026/02/20/china/china-ai-seedance-intl-hnk-dst)** — 中國的 SeedDance AI 讓好萊塢坐不住了，AI 影視製作的競爭正在加速白熱化
- **[Phil Spencer is exiting Microsoft as AI executive takes over Xbox](https://www.neowin.net/news/phil-spencer-is-exiting-microsoft-as-ai-executive-takes-over-xbox/)** — Phil Spencer 離開微軟，AI 高管接管 Xbox，微軟的每個角落都在被 AI 改造
- **[Micron Is Spending $200B to Break the AI Memory Bottleneck](https://www.wsj.com/tech/micron-is-spending-200-billion-to-break-the-ai-memory-bottleneck-a4cc74a1)** — Micron 砸 2000 億美元解決 AI 記憶體瓶頸，AI 基礎建設的投資規模已經到了另一個次元
- **[Accenture links staff promotions to use of AI tools](https://www.theguardian.com/accenture/2026/feb/19/accenture-links-staff-promotions-to-use-of-ai-tools)** — Accenture 把 AI 工具使用率跟升遷掛鉤，不用 AI 的人可能連升遷都沒份

---

## 🏄 深水區

- **[A Guide to Which AI to Use in the Agentic Era](https://www.oneusefulthing.org/p/a-guide-to-which-ai-to-use-in-the)** — Ethan Mollick 的 AI 工具選擇指南，在各家 agent 百花齊放的現在，這篇幫你搞清楚什麼場景該用什麼工具
- **[I hate AI side projects](https://dylancastillo.co/posts/ai-side-projects.html)** — 53 個 upvotes、58 則留言，顯然戳中了很多人的痛點——AI side project 的焦慮和疲憊感，值得每個在 AI 浪頭上衝浪的人讀一讀
- **[Task-Completion Time Horizons of Frontier AI Models](https://metr.org/time-horizons/)** — METR 的最新評估包含了 Opus 4.6，看看前沿模型在自主完成任務上到底走到哪了
- **[The Loom Is Here: 12 Months of AI-Augmented Engineering](https://medium.com/@shelby.w.vanhooser/the-loom-is-here-12-months-of-ai-augmented-engineering-843794ec7c59)** — 一位工程師用了一整年 AI 輔助開發的真實回顧，不是理論框架而是實戰心得
