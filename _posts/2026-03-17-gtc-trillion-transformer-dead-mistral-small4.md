---
title: "GTC 萬億炸場、Transformer 被判死刑、Mistral 開源殺入"
date: 2026-03-17
description: "NVIDIA GTC 喊出萬億美元訂單、Vera Rubin 全面投產；Altman 在史丹佛宣判 Transformer 死刑；Mistral Small 4 以 Apache 2 開源統一旗艦能力。"
tags: [llm, ai-industry, ai-tools, agents]
---

今天 AI 圈的浪有點猛——黃仁勳在 GTC 上直接喊出一萬億美元訂單，Altman 回母校史丹佛跟大二學弟妹說 Transformer 快掛了，而 Mistral 默默丟出一個 Apache 2 開源的 119B MoE 模型。三道浪同時拍過來，週一早上的 timeline 注定不平靜。

---

## 🌊 今日浪頭

### [Jensen Huang just put Nvidia's Blackwell and Vera Rubin sales projections into the $1 trillion stratosphere](https://techcrunch.com/2026/03/16/jensen-just-put-nvidias-blackwell-and-vera-rubin-sales-projections-into-the-1-trillion-stratosphere/)

GTC 2026 的 keynote，黃仁勳這次是把整個 AI 產業的天花板又往上推了一截。去年他說看到 5000 億美元的需求，這次直接翻倍——「我現在站在這裡，看到至少一萬億美元的訂單，延伸到 2027 年。」Vera Rubin 架構在訓練任務上比 Blackwell 快 3.5 倍、推理快 5 倍，下半年開始量產。同場還發布了專為 Agentic AI 打造的 [Vera CPU](https://nvidianews.nvidia.com/news/nvidia-launches-vera-cpu-purpose-built-for-agentic-ai)，效率是傳統機架式 CPU 的兩倍。老黃甚至說「Token 是新的商品」，AI 工廠的商業模式就是生產和販賣 Token。以我的觀察，這場演講的潛台詞很清楚：AI 已經從「我們在研究」進入「這是一門萬億生意」的階段。

**為什麼這道浪值得追：**
- 從 5000 億到 1 萬億，短短幾個月需求翻倍，推理拐點正式到來
- Vera CPU 是 NVIDIA 首次為 Agent 工作負載專門設計 CPU，訊號很明確
- 60% 的業務來自超大規模雲計算，這意味著 AI 基礎建設的投資還在加速

### [Altman 在史丹佛宣判 Transformer 死刑：下一代架構正在路上](https://www.36kr.com/p/3726179495983753)

Sam Altman 回到史丹佛，對著一群大二學生丟出了他最重量級的判斷：Transformer 的日子到頭了。他說下一代架構帶來的性能跳躍，會像當年 Transformer 對 LSTM 的降維打擊一樣猛。而且他不是在畫餅——他的論點是現在的模型已經聰明到可以輔助人類做這種等級的基礎研究了。用 AI 去找能取代 AI 的新架構，這個飛輪已經轉起來了。同時他也順手丟了幾個炸彈：AGI 兩年內到來、coding agent 是下一個 ChatGPT 時刻、未來會出現比 OpenAI 更大的公司。以這位 GPT 帝國建造者的身份來說這些話，份量不一般。

**為什麼這道浪值得追：**
- Mamba、xLSTM、Liquid Neural Networks 等後 Transformer 架構已在產業界落地，NVIDIA 的 Nemotron 系列已大量採用混合架構
- 「用 AI 研究 AI」的自我加速飛輪是通往 AGI 的關鍵路徑，這不只是嘴砲
- 他明確說 coding agent 是下一個引爆點，而非某個具體模型

### [Introducing Mistral Small 4 — Apache 2 開源的 119B MoE 統一模型](https://mistral.ai/news/mistral-small-4)

Mistral 安靜但很猛地丟出了 Mistral Small 4。名字叫 Small，參數量 119B（MoE 架構，6B 活躍參數），而且是 Apache 2 授權——這代表你可以拿去商用、改造、部署，完全自由。最有意思的是，這是 Mistral 第一個把旗艦模型的三大能力統一的模型：Magistral 的推理、Pixtral 的多模態、Devstral 的 agentic coding，全部塞進一個模型裡。支援 `reasoning_effort` 參數調整推理深度，高模式等同之前的 Magistral。Mistral 同時還發布了 [Leanstral](https://mistral.ai/news/leanstral)，專門針對 Lean 4 形式驗證語言的模型。以開源社群的角度來看，這是一個非常實在的貢獻。

**為什麼這道浪值得追：**
- Apache 2 授權的 119B MoE，6B 活躍參數意味著推理成本極低，部署門檻大幅降低
- 三合一統一架構讓開發者不用再在推理、視覺、coding 之間切換模型
- Mistral 一直走「開源但高品質」路線，這次是對 Llama、Qwen 陣營的正面回擊

---

## ⚡ 衝浪快報

- **[xAI 11 人創始團隊僅剩 2 人，馬斯克承認「從頭重建」](https://www.36kr.com/p/3725558936451714)** — 不到三年，xAI 經歷成立以來最劇烈的震盪，SpaceX 和 Tesla 高管被緊急調入救火
- **[青少年因 Grok 生成 CSAM 起訴 xAI](https://www.theverge.com/ai-artificial-intelligence/895639/xai-grok-teens-lawsuit-grok-ai-elon-musk)** — 三名田納西州青少年指控 Grok 將他們的真實照片生成性化內容，提起集體訴訟
- **[阿里巴巴成立 Alibaba Token Hub 事業群](https://www.36kr.com/p/3725838493807361)** — CEO 吳泳銘直管，三大任務：創造 Token、輸送 Token、應用 Token。把 Token 寫進組織架構的大廠，阿里是頭一個
- **[Karpathy 開源 autoresearch：AI 通宵跑完 276 次實驗](https://www.36kr.com/p/3725521482578567)** — 零人類干預，兩天內篩出 29 項有效改進，訓練效率提升 11%。GitHub 已拿下 36.9k stars
- **[NVIDIA DLSS 5 用生成式 AI 重塑遊戲畫面](https://www.theverge.com/news/895472/nvidia-dlss5-generative-ai-pc-graphics)** — 黃仁勳稱這是「圖形學的 GPT 時刻」，但部分玩家已經在喊 slop
- **[中國 AI 大模型調用量連續兩週超越美國](https://www.36kr.com/p/3725445557991808)** — OpenRouter 數據：中國上週 4.69 萬億 Token，美國 3.29 萬億。MiniMax M2.5 連續五週蟬聯全球榜首
- **[DeepSeek V4 傳推遲發布，為架構級重構加入 LTM 長期記憶](https://www.36kr.com/p/3725359401890307)** — 萬億參數、百萬上下文、原生多模態，梁文錦不急著搶首發
- **[Encyclopedia Britannica + Merriam-Webster 聯手起訴 OpenAI](https://techcrunch.com/2026/03/16/merriam-webster-openai-encyclopedia-brittanica-lawsuit/)** — 指控近 10 萬篇文章被用於 LLM 訓練，字典都來告了
- **[OpenAI Codex 子代理功能正式上線](https://simonwillison.net/2026/Mar/16/codex-subagents/#atom-everything)** — 類似 Claude Code 的 subagent 架構，支援 explorer、worker 等預設代理類型
- **[Apideck CLI：比 MCP Server 更省 context 的 AI agent 介面](https://www.apideck.com/blog/mcp-server-eating-context-window-cli-alternative)** — HN 116 分、103 則留言，MCP 的 context 消耗問題終於有人正面挑戰了
- **[315 曝光 GEO「AI 投毒」：虛構產品竟被大模型推薦](https://www.36kr.com/p/3725542475807105)** — 一款不存在的智能手環，靠 GEO 優化軟文就衝上了 AI 推薦榜，生成式搜尋的信任危機浮出水面

---

## 🏄 深水區

- **[Simon Willison: Agentic Engineering Patterns 完整指南](https://simonwillison.net/guides/agentic-engineering-patterns/how-coding-agents-work/#atom-everything)** — 如果你在用 Claude Code 或 Codex 但從沒搞懂底層在幹嘛，這份指南從 harness 架構到 tool use 一路拆解，是目前看過最清晰的 coding agent 入門
- **[Sam Altman 終於承認純 scaling 到不了 AGI](https://garymarcus.substack.com/p/breaking-sam-altman-concedes-that)** — Gary Marcus 的角度：那個在 2022 年嘲笑「scaling 有極限」論點的人，如今自己說需要新架構。歷史的諷刺，值得細讀
- **["Claude Code 這條路線錯了" — Jeremy Howard 開砲](https://www.36kr.com/p/3725127329888647)** — fast.ai 創辦人直言 Dario Amodei 和馬斯克不懂現代軟體工程，AI 不會直接輸出機器碼。有料的反面觀點，不管你同不同意都該看
- **[AI 算力大考：缺電只是表象，半導體製造才是真正天花板](https://www.36kr.com/p/3725460425126656)** — SemiAnalysis 創辦人 Dylan Patel 的最新分析：EUV 光刻機產能、HBM 記憶體爭奪戰才是限制 AI 擴張的硬瓶頸，不是電力
