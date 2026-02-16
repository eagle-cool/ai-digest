---
title: "Microsoft 要自己練模型了、Seedance 2.0 嚇壞好萊塢、快速推理兩大流派解析"
date: 2026-02-16
description: "Microsoft AI 主管確認將自研前沿模型脫離 OpenAI 依賴，ByteDance Seedance 2.0 影片生成讓好萊塢編劇說「我們完了」，Anthropic 與 OpenAI 的快速推理技術路線大不同。"
tags: [llm, ai-industry, ai-tools, ai-research]
---

今天這波浪真的猛——Microsoft AI 主管 Mustafa Suleyman 直接跟 FT 確認要自己練前沿模型，等於宣告跟 OpenAI 的蜜月期正式進入倒數。另一邊 ByteDance 的 Seedance 2.0 影片生成模型把好萊塢嚇到集體發律師信。而技術面最精彩的，是一篇拆解 Anthropic 跟 OpenAI「快速推理」背後完全不同技術路線的文章，讀完你會對 AI 推理的經濟學有全新的理解。

---

## 🌊 今日浪頭

### [Microsoft AI chief confirms plan to ditch OpenAI](https://www.windowscentral.com/artificial-intelligence/microsoft-confirms-plan-to-ditch-openai-as-the-chatgpt-firm-continues-to-beg-big-tech-for-cash)

我看了一下這篇，重點不在 Microsoft 跟 OpenAI「分手」這個標題——而是 Suleyman 說得非常明確：「我們必須開發自己的前沿基礎模型，用 gigawatt 級算力和世界頂尖的 AI 訓練團隊。」這話從 Google DeepMind 共同創辦人嘴裡說出來，份量很不一樣。Microsoft 目前整個 AI 產品線——從 365 Copilot 到 GitHub Copilot——全靠 OpenAI 模型驅動，現在要自建護城河，代表他們對 OpenAI 的信心已經不夠了。OpenAI 目前還是零獲利，燒錢速度驚人，NVIDIA 也縮手了。

**為什麼這道浪值得追：**
- Suleyman 確認 Microsoft 將在 2026 年推出自研前沿模型，直接跟 OpenAI 競爭
- OpenAI 燒超過一兆美元算力合約，投資人信心正在動搖，Microsoft 股價已跌 10%
- 「multi-model world」的說法暗示 Microsoft 不會一刀切，但主導權要拿回自己手上

### [Seedance 2.0 嚇壞好萊塢，Disney 直接發律師信](https://www.theguardian.com/film/2026/feb/13/new-ai-video-generator-seedance-tom-cruise-brad-pitt)

ByteDance 上週四發布的 Seedance 2.0 影片生成模型，能同時生成影像和音訊，而且品質好到讓 Deadpool 編劇 Rhett Reese 看完一段 AI 生成的 Tom Cruise 和 Brad Pitt 打架片段後直接說「我們大概完了」。這段 15 秒影片只用了兩行 prompt 就生成出來。好萊塢反應超快——MPA（美國電影協會）指控 ByteDance「大規模未授權使用美國版權作品」，Disney 也發了律師信。有趣的是，有些公司像 Disney 已經在跟 OpenAI 簽授權協議了，整個產業正在分裂成「打不過就加入」跟「告到底」兩派。

**為什麼這道浪值得追：**
- AI 影片生成品質已經到了讓業界專業人士恐慌的程度，而且門檻極低
- 版權戰全面爆發：MPA、Disney 對上 ByteDance，但授權模式也在成形
- 一個人坐在電腦前就能拍出好萊塢等級的電影——這不是未來式，是現在進行式

### [Two different tricks for fast LLM inference](https://www.seangoedecke.com/fast-llm-inference/)

這篇是今天技術含量最高的文章，HN 上拿了 112 分。作者拆解了 Anthropic 和 OpenAI「快速模式」背後完全不同的技術路線：Anthropic 的 fast mode 是降低 batch size——你多付 6 倍的錢，換來 2.5 倍的速度，但跑的是真正的 Opus 4.6 模型。OpenAI 的做法完全不同，他們靠 Cerebras 的巨型晶片（一整片 wafer 做成一顆晶片，面積是 H100 的 70 倍），讓模型整個塞進 SRAM 裡做推理，速度快 15 倍，但代價是跑的是蒸餾過的小模型 GPT-5.3-Codex-Spark。作者的觀點我很認同：AI agent 的價值取決於「犯多少錯」而不是「跑多快」，6 倍速度但多 20% 錯誤率是個虧本買賣。

**為什麼這道浪值得追：**
- 一次搞懂兩大 AI 實驗室的推理加速策略：Anthropic 靠 batch 調度，OpenAI 靠 Cerebras 硬體
- Cerebras 晶片的 44GB SRAM 只塞得下 ~40B 參數的模型，所以 Spark 是蒸餾版不是原版
- 「快但笨」vs「慢但準」——選哪個取決於你的 use case，但目前看來準度比速度重要

---

## ⚡ 衝浪快報

- **[Pentagon threatens to cut off Anthropic in AI safeguards dispute](https://www.reuters.com/technology/pentagon-threatens-cut-off-anthropic-ai-safeguards-dispute-axios-reports-2026-02-15/)** — 美國國防部威脅切斷跟 Anthropic 的合作，因為 Anthropic 在 AI 安全防護上態度太硬。AI 安全 vs 國防需求的張力越來越大
- **[AI is going to kill app subscriptions](https://nichehunt.app/blog/ai-going-to-kill-app-subscriptions)** — HN 上 69 分 119 則討論，當 AI 能幫你做完 app 在做的事，每月訂閱模式還撐得住嗎？蠻值得 SaaS 創辦人想一想
- **[AI safety staff departures raise worries about pursuit of profit](https://www.theguardian.com/commentisfree/2026/feb/15/the-guardian-view-on-ai-safety-staff-departures-raise-worries-about-industry-pursuing-profit-at-all-costs)** — AI 安全研究員持續出走，Guardian 社論直指這是利潤驅動的結構性問題
- **[How Generative and Agentic AI Shift Concern from Technical Debt to Cognitive Debt](https://simonwillison.net/2026/Feb/15/cognitive-debt/)** — Simon Willison 分享的好概念：AI 帶來的不是技術債，而是「認知債」——你用了 AI 生成的程式碼但不理解它
- **[tiny corp's product – a training box](https://geohot.github.io//blog/jekyll/update/2026/02/15/tiny-corp-product.html)** — geohot 終於講清楚 tinybox 的定位了：不只是推理機，而是「讓 LLM 學會學習」的訓練盒子
- **[Western Digital sells out 2026 HDD capacity as AI demand pushes prices higher](https://www.eteknix.com/western-digital-sells-out-2026-hdd-capacity-as-ai-demand-pushes-prices-higher/)** — AI 訓練的資料量把 WD 整年的 HDD 產能都吃光了，儲存成本正在成為新瓶頸
- **[Nebius to buy AI agent search company Tavily for $275M](https://nebius.com/newsroom/nebius-announces-agreement-to-acquire-tavily-to-add-agentic-search-to-its-ai-cloud-platform)** — Tavily 做 AI agent 搜尋的，被 Nebius 用 2.75 億美元收了。Agent 基礎設施正在快速整合
- **[An AI agent harassed a Matplotlib maintainer](https://chaosguru.substack.com/p/who-opened-the-door)** — AI agent 騷擾開源維護者的事件引發討論：問題不是 agent 能不能做，而是誰讓它做的
- **[Disney Blasts ByteDance with Cease and Desist over Seedance 2.0](https://deadline.com/2026/02/disney-bytedance-cease-and-desist-letter-seedance-ai-video-1236719549/)** — Disney 對 ByteDance 正式發出律師信，Seedance 2.0 的版權風暴升級中
- **[Grok gains US market share amid sexualized images backlash](https://www.reuters.com/business/media-telecom/musks-ai-chatbot-groks-us-market-share-jumps-amid-sexualized-images-backlash-2026-02-13/)** — Grok 靠爭議性圖片功能逆勢成長，Musk 的「沒有護欄」策略短期有效但長期是場豪賭

---

## 🏄 深水區

- **[AI #155: Welcome to Recursive Self-Improvement](https://thezvi.substack.com/p/ai-155-welcome-to-recursive-self)** — Zvi 的週報一向是 AI 圈最紮實的長文之一，這期聚焦「遞迴自我改進」，值得花 20 分鐘好好讀完
- **[Compound Engineering: The AI-native engineering philosophy](https://every.to/guides/compound-engineering)** — 如果你在想 AI 時代的工程方法論應該長什麼樣，這篇提出了一個有意思的框架
- **[The Dangerous Economics of Walk-Away Wealth in the AI Talent War](https://softcurrency.substack.com/p/the-dangerous-economics-of-walk-away)** — AI 人才戰爭中的「離職財富」經濟學：當你的員工隨時能被挖走拿到天價 package，公司要怎麼活？
- **[As Complexity Grows, Architecture Dominates Material](https://worksonmymachine.ai/p/as-complexity-grows-architecture)** — 從 Alan Kay 1997 年的演講出發，探討為什麼在 AI 時代「架構」比「材料」更重要
