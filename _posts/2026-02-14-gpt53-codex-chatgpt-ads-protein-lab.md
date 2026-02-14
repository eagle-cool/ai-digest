---
title: "GPT-5.3-Codex 終於合體、ChatGPT 開始賣廣告、GPT-5 自己跑實驗了"
date: 2026-02-14
description: "OpenAI 發布 GPT-5.3-Codex 合併 coding 與推理能力，ChatGPT 正式開始測試廣告，GPT-5 搭配 Ginkgo Bioworks 自主實驗室跑了 36,000 次生物實驗、成本降 40%。"
tags: [llm, ai-coding, ai-industry, agents]
---

這幾天 OpenAI 的動作密度有點嚇人——GPT-5.3-Codex 把 coding 和通用推理合成一個模型、ChatGPT 正式開始塞廣告（對，你沒看錯）、GPT-5 甚至自己跑起了蛋白質合成實驗。當 AI 不只是幫你寫 code，而是開始自己做科學實驗的時候，我覺得我們真的到了一個轉折點。

---

## 🌊 今日浪頭

### [Introducing GPT-5.3-Codex](https://openai.com/index/introducing-gpt-5-3-codex)

OpenAI 把 GPT-5.2-Codex 的 coding 能力和 GPT-5.2 的通用推理能力合成了一個模型——GPT-5.3-Codex。速度比前代快 25%，在 SWE-Bench Pro 和 Terminal-Bench 上都創下新高。但最讓我印象深刻的不是 benchmark，而是這個模型可以一邊工作一邊跟你互動——像個同事而不是個工具。你可以在它跑 task 的中途插話、討論方向、即時調整策略，不需要等它跑完再重來。

更有意思的是，GPT-5.3-Codex 是第一個「幫忙打造自己」的模型——OpenAI 團隊用它的早期版本來 debug 自己的訓練流程、管理部署、診斷測試結果。聽起來有點遞迴的浪漫。

**為什麼這道浪值得追：**
- Coding + 推理合一，不用再選模型——一個打天下
- 即時互動式 agent，從「等結果」變成「跟它聊」
- 社群反饋分歧：有人說快了很多，也有人回報比 5.2 慢，穩定性還在磨合期

### [Testing ads in ChatGPT](https://openai.com/index/testing-ads-in-chatgpt)

這事遲早要來——OpenAI 正式開始在 ChatGPT 裡測試廣告。目前僅限美國的 Free 和 Go 方案用戶，Plus、Pro、Business、Enterprise 不受影響。廣告會根據你的對話主題和過去的聊天紀錄來配對，但 OpenAI 強調廣告不會影響回答內容，廣告主也看不到你的對話。

我的觀察是：這標誌著 ChatGPT 從「訂閱制工具」正式走向「免費增值 + 廣告」的混合商業模式。對用戶來說，免費版可能會越來越「熱鬧」；對產業來說，AI 搜尋廣告這塊餅正式開切了——Google 該緊張了。

**為什麼這道浪值得追：**
- 僅限 Free / Go 方案，付費用戶暫時不受影響
- 廣告不影響回答內容，但會根據對話主題和歷史聊天記錄做個人化配對
- 可以一鍵刪除廣告數據、管理個人化設定——至少隱私控制做得不差

### [GPT-5 lowers the cost of cell-free protein synthesis](https://openai.com/index/gpt-5-lowers-protein-synthesis-cost)

這個可能是近期最讓我興奮的應用。OpenAI 和 Ginkgo Bioworks 合作建了一個自主實驗室——GPT-5 負責設計實驗、分析數據、決定下一步，Ginkgo 的雲端自動化系統負責執行。六個迭代週期、36,000 個實驗條件跑下來，把無細胞蛋白質合成的成本降了 40%，每克蛋白質壓到 422 美元。

更關鍵的是，Ginkgo 已經開始在自家試劑商店販售這個 AI 優化過的反應配方了——這不是論文裡的概念驗證，是真的在賣的東西。當 AI 可以像實驗科學家一樣設計和迭代實驗，生物科技的研發速度和成本結構都會被重新定義。

**為什麼這道浪值得追：**
- GPT-5 像實驗科學家一樣運作：設計 → 執行 → 分析 → 迭代，全自動
- 36,000 次實驗、6 輪迭代、成本降 40%——不是 demo，是實際成果
- 已商業化販售——AI 驅動的實驗成果直接變成產品

---

## ⚡ 衝浪快報

- **[Introducing OpenAI Frontier](https://openai.com/index/introducing-openai-frontier)** — OpenAI 推出企業級 AI agent 平台，支援共享上下文、權限管理和治理——瞄準的是企業 AI 部署的「最後一哩路」
- **[Introducing the Codex app](https://openai.com/index/introducing-the-codex-app)** — macOS 版 Codex app 正式登場，多 agent 並行、長時間任務、一個 app 搞定所有 AI coding 工作流
- **[Retiring GPT-4o, GPT-4.1, GPT-4.1 mini, and o4-mini](https://openai.com/index/retiring-gpt-4o-and-older-models)** — 2 月 13 日起 ChatGPT 正式退役一批舊模型，API 暫不受影響——時代的眼淚
- **[Bringing ChatGPT to GenAI.mil](https://openai.com/index/bringing-chatgpt-to-genaimil)** — OpenAI 把 ChatGPT 部署到美國國防部的 GenAI.mil 平台，AI 進軍國防不再是新聞，但規模在擴大
- **[Transformers.js v4 Preview](https://huggingface.co/blog/transformersjs-v4)** — Hugging Face 的瀏覽器端 ML 框架出 v4 了，對想在前端跑模型的開發者是個好消息
- **[GPT-5.3-Codex System Card](https://openai.com/index/gpt-5-3-codex-system-card)** — 安全卡揭露 GPT-5.3-Codex 在網路安全方面的能力提升，以及 OpenAI 對應的防護措施
- **[Snowflake and OpenAI partner — $200M agreement](https://openai.com/index/snowflake-partnership)** — 兩億美金的合作案，把 frontier AI 直接塞進企業數據平台——錢的方向永遠最誠實
- **[Advancing AI benchmarking with Game Arena](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/kaggle-game-arena-updates/)** — Google 擴展 Game Arena 加入撲克和狼人殺，Gemini 3 Pro 在西洋棋排行榜上領先
- **[Introducing Trusted Access for Cyber](https://openai.com/index/trusted-access-for-cyber)** — OpenAI 推出信任存取框架，讓經過驗證的資安團隊能使用更強大的 frontier cyber 能力
- **[Harness engineering: leveraging Codex](https://openai.com/index/harness-engineering)** — 看看企業端怎麼在 agent-first 世界裡把 Codex 整合進工程流程

---

## 🏄 深水區

- **[Unrolling the Codex agent loop](https://openai.com/index/unrolling-the-codex-agent-loop)** — 技術底層的好文：Codex CLI 怎麼串接模型、工具、prompt 和效能優化。想自己建 agent 的人，這篇值得花 20 分鐘細讀
- **[Inside OpenAI's in-house data agent](https://openai.com/index/inside-our-in-house-data-agent)** — OpenAI 自己怎麼用 GPT-5 + Codex + memory 建了個內部數據分析 agent，幾分鐘內處理海量數據集——從自己的實戰經驗學 agent 架構，這種文章最有料
- **[The Future of the Global Open-Source AI Ecosystem: From DeepSeek to AI+](https://huggingface.co/blog/huggingface/one-year-since-the-deepseek-moment-blog-3)** — DeepSeek 爆發一年後，開源 AI 生態走到哪了？Hugging Face 的觀察角度永遠值得一讀
- **[Community Evals: Because we're done trusting black-box leaderboards](https://huggingface.co/blog/community-evals)** — 受夠了不透明的排行榜？Hugging Face 推出社群評測機制，讓大家自己定義什麼是「好模型」
