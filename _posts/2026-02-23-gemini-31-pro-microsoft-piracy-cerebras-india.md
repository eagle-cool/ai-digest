---
title: "Gemini 3.1 Pro 以小搏大、微軟哈利波特盜版教學翻車"
date: 2026-02-23
description: "Google 放出 Gemini 3.1 Pro Preview，小數點升級卻帶來推理能力翻倍；微軟官方部落格被抓包教人用盜版哈利波特訓練 AI；G42 聯手 Cerebras 在印度部署 8 exaflops 算力。"
tags: [llm, ai-industry, ai-tools]
---

今天最讓我驚訝的不是哪個大模型又刷榜了——而是 Google 居然用一個 ".1" 的版號升級，就把推理能力翻了一倍。Gemini 3.1 Pro Preview 看起來低調，但社群裡已經玩瘋了。同一時間，微軟那邊出了個讓人哭笑不得的烏龍：官方部落格竟然教人用盜版哈利波特來訓練 AI 模型，被 Hacker News 抓包後火速刪文。

---

## 🌊 今日浪頭

### [Gemini 3.1 Pro Preview：最「小」的一次迭代，最猛的一波提升](https://www.36kr.com/p/3691440567087619)

Google 這次玩了一招「扮豬吃老虎」。從 Gemini 3.0 到 3.1，版號看起來只動了一個小數點，但實際能力提升相當驚人。ARC-AGI-2 推理測試的驗證分數從前代翻了一倍以上達到 77.1%，GPQA Diamond 科學測試拿下 94.3%——這些成績都超過了 Anthropic 的 Opus 4.6 和 OpenAI 的 GPT-5.2。更關鍵的是，定價跟前代 Gemini 3 Pro 完全一樣，算下來運行成本不到 Opus 4.6 的一半。這個性價比直接把競爭推向了「誰更會過日子」的階段。

**為什麼這道浪值得追：**
- 社群已經用它手搓出 3D 汽車懸架模擬器、互動式 ISS 軌道追蹤器，代碼生成能力直逼工程級原型
- 建構在 Gemini 3 Deep Think 技術之上，把深度推理能力下放到更廣泛可用的 Pro 模型
- 這還只是 Preview 版本——正式版來了恐怕又是一波震盪

### [Microsoft deletes blog telling users to train AI on pirated Harry Potter books](https://arstechnica.com/tech-policy/2026/02/microsoft-removes-guide-on-how-to-train-llms-on-pirated-harry-potter-books/)

這故事荒謬到我差點以為是洋蔥新聞。微軟的一位資深產品經理在 2024 年 11 月寫了一篇官方部落格，教開發者用 Azure SQL DB + LangChain 建 AI 應用——然後貼心地附上了一個 Kaggle 資料集連結，裡面塞了七本哈利波特全集，標記為「公共領域」。部落格甚至示範了怎麼用這些書訓練模型生成同人小說，其中一段讓哈利在霍格華茲特快車上遇到一個跟他推銷「微軟 Native Vector Support」的新朋友。放了超過一年沒人管，直到被 Hacker News 社群抓包才火速刪文。

**為什麼這道浪值得追：**
- 一篇放了超過一年的官方部落格，用了明顯侵權的素材卻無人審核——大公司的內容管理漏洞比你想的大
- 法律教授分析微軟可能面臨「間接侵權」責任，因為等於在鼓勵用戶下載盜版素材來用自家產品
- AI 訓練資料的版權灰色地帶還在擴大，這種事只會越來越常見

### [UAE's G42 teams up with Cerebras to deploy 8 exaflops of compute in India](https://techcrunch.com/2026/02/20/uaes-g42-teams-up-with-cerebras-to-deploy-8-exaflops-of-compute-in-india/)

印度 AI 基礎建設的軍備競賽正在白熱化。阿布達比的 G42 聯手美國晶片商 Cerebras，在印度部署 8 exaflops 超級電腦系統。但這只是冰山一角——Adani 承諾砸 1,000 億美元建資料中心、Reliance 要投 1,100 億美元、OpenAI 跟 Tata 合作搶 100MW 算力、印度政府喊出要在兩年內吸引超過 2,000 億美元基礎建設投資。美國科技巨頭已經累計承諾在印度投入約 700 億美元，這個市場的胃口大得嚇人。

**為什麼這道浪值得追：**
- 印度正在快速崛起為全球 AI 算力新據點，不只是外包寫程式的地方了
- 「主權 AI」是這波投資的關鍵詞——資料留在印度、遵守當地法規，這會是各國效仿的範本
- Cerebras 的 wafer-scale 晶片拿到巨大實戰場景，對抗 NVIDIA 的戰線又拉長了一段

---

## ⚡ 衝浪快報

- **[Our First Proof submissions](https://openai.com/index/first-proof-submissions)** — OpenAI 公開了 AI 模型挑戰數學證明的嘗試，測試研究級推理能力在專家級問題上到底行不行
- **[Cloudflare introduces Code Mode MCP server](https://www.reddit.com/r/AIDeveloperNews/comments/1radmbu/cloudflare_has_introduced_the_code_mode_model/)** — Cloudflare 推出 Code Mode MCP server，讓 AI agent 只用約 1,000 tokens 就能存取整個 Cloudflare API，這效率太香了
- **[NVIDIA Dynamo v0.9.0](https://www.reddit.com/r/AIDeveloperNews/comments/1r9octj/dynamo_v090_is_an_opensource_inference_library/)** — NVIDIA 開源推論加速函式庫 Dynamo 0.9.0，專為 AI factory 級別推理場景設計
- **[CVPR 2026 放榜](https://www.jiqizhixin.com/articles/2026-02-21-5)** — 計算機視覺頂會收到 16,092 篇投稿、錄取 4,090 篇，錄用率 25.42%，CV 圈這卷度真的沒在開玩笑
- **[谷歌再投 12,400 億衝刺 AI 王座](https://www.36kr.com/p/3693821399084937)** — Alphabet 持續加碼 AI 投資，用真金白銀表態要跟 OpenAI、Anthropic 正面硬剛
- **[中國春節 AI 大戰砸了 80 億](https://www.36kr.com/p/3693887791459976)** — 阿里千問、騰訊元寶、百度文心、字節豆包春節搶發紅包搶用戶，AI App 下載量輪番衝上榜首
- **[Grok is now pretty good at answering questions about Baldur's Gate](https://techcrunch.com/2026/02/20/great-news-for-xai-grok-is-now-pretty-good-at-answering-questions-about-baldurs-gate/)** — xAI 高級工程師被調去確保 Grok 能好好回答柏德之門的問題，這優先級安排讓人一言難盡
- **[Peak XV raises $1.3B, doubles down on AI](https://techcrunch.com/2026/02/20/peak-xv-raises-1-3b-doubles-down-on-ai-as-global-vc-rivalry-in-india-heats-up/)** — 前紅杉印度 Peak XV 募了 13 億美元重押 AI 和 fintech，印度 VC 競爭進入白熱化
- **[Show HN: Paragent – Run 10 AI coding agents in parallel](https://paragent.app/)** — 描述需求、自動分支、寫完開 PR，一次跑十個 AI coding agent——野心不小，實用性待驗證
- **[Anthropic-funded group backs candidate attacked by rival AI super PAC](https://techcrunch.com/2026/02/20/anthropic-funded-group-backs-candidate-attacked-by-rival-ai-super-pac/)** — AI 公司開始玩政治了，Anthropic 資助的團體力挺提出 RAISE Act 的紐約候選人

---

## 🏄 深水區

- **[How I think about Codex](https://simonwillison.net/2026/Feb/22/how-i-think-about-codex/#atom-everything)** — Simon Willison 拆解 OpenAI「Codex」這個名詞到底指的是什麼——模型？產品？平台？讀完你會發現 OpenAI 的命名策略本身就是一道推理題
- **[ThunderKittens 2.0 by Hazy Research](https://www.reddit.com/r/AIDeveloperNews/comments/1ra9cke/thunderkittens_20_by_hazy_research_faster_kernels/)** — Hazy Research 放出 ThunderKittens 2.0，BF16/MXFP8/NVFP4 GEMM 效能追平甚至超越 cuBLAS，搞推論底層優化的人不能錯過
- **[AI's promise to indie filmmakers: Faster, cheaper, lonelier](https://techcrunch.com/2026/02/20/ais-promise-to-indie-filmmakers-faster-cheaper-lonelier/)** — AI 讓獨立電影製作更快更便宜，但也更孤獨——當效率成為唯一指標，創意正在被 AI 生成的低品質內容洪流淹沒
- **[AI 招聘市場正經歷「亂紀元」](https://www.jiqizhixin.com/articles/2026-02-22-5)** — 矽谷 AI 人才市場的荒謬現況：公司招不到人、在職的人坐立不安、新人覺得門檻越來越高，值得每個 AI 從業者讀一讀
