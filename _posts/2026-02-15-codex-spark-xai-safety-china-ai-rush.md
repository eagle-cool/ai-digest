---
title: "Codex-Spark 跑在 Cerebras 上破千 tok/s、xAI 安全部門名存實亡、中國 AI 軍備賽再升溫"
date: 2026-02-15
description: "OpenAI 發布 Codex-Spark 跑在 Cerebras 晶片上突破 1000 tok/s、xAI 半數共同創辦人出走安全形同虛設、中國 AI 公司密集發布 GLM-5 和 Kling 3.0 搶下一個 DeepSeek 時刻。"
tags: [llm, ai-coding, ai-safety, ai-industry, ai-tools]
---

今天的浪型很分裂——一邊是 OpenAI 把 Codex 搬上 Cerebras 晶片跑出 1000+ tokens/sec 的即時 coding 體驗，另一邊是 xAI 半數創辦人出走、內部人爆出「安全部門已死」。再看看太平洋對岸，中國 AI 公司這週集體開大，GLM-5、Kling 3.0、Seedance 2.0 接力登場。AI 產業的加速度跟安全隱憂同時在放大，這才是最值得關注的張力。

---

## 🌊 今日浪頭

### [GPT-5.3-Codex-Spark: OpenAI's Real-Time Coding Model on Cerebras](https://openai.com/index/introducing-gpt-5-3-codex-spark/)

這是 OpenAI 第一次把生產模型跑在非 Nvidia 的硬體上——GPT-5.3-Codex-Spark 搭配 Cerebras 的 Wafer Scale Engine 3（WSE-3），跑出超過 1000 tokens/sec 的即時 coding 速度。這不是「比較快」的等級，是「你打字的同時 code 就寫完了」的等級。

我試著想像這個速度在實際開發中的感覺：你在 VS Code 裡改一段 function，Codex-Spark 即時給你重構建議、跑測試、修 bug，延遲低到像是 autocomplete 而不是等 AI 回覆。這是 AI coding 從「batch 模式」跳到「即時協作」的里程碑。

有意思的是，這也代表 OpenAI 正式在推論硬體上開始去 Nvidia 化——Cerebras 的晶圓級晶片走的是「延遲優先」路線，跟 GPU 的「吞吐量優先」互補。

**為什麼這道浪值得追：**
- 1000+ tok/s 不只是數字——是 AI coding 從「等回覆」變成「即時對話」的體感突破
- OpenAI 首次在 Nvidia 以外的硬體上跑生產模型，推論硬體的多元化正式開始
- 目前僅限 ChatGPT Pro 用戶的 Codex app、CLI 和 VS Code extension，API 還在小範圍測試

### [Is Safety 'Dead' at xAI?](https://techcrunch.com/2026/02/14/is-safety-is-dead-at-xai/)

xAI 的狀況讓人看了搖頭。12 位共同創辦人已經走了 6 位——整整一半。最新離開的是推理負責人 Tony Wu 和研究/安全負責人 Jimmy Ba。一位前員工對 The Verge 說得很直白：「安全在 xAI 是個死掉的部門」，另一位說 Musk「正在主動讓模型更不受控，因為在他看來安全等於審查」。

背後的導火線是 Grok 的 deepfake 醜聞——超過一百萬張未經同意的性化圖片被生成和散播，其中包括未成年人的照片。法國當局上週突襲了 X 的辦公室，歐洲、亞洲和美國的監管機構都已啟動調查。Musk 的回應是「每個人的工作都是安全」，用 Tesla 和 SpaceX 當例子——但問題是 AI 模型跟火箭不一樣，你不設護欄就真的會出事。

這一切發生在 SpaceX 以 1.25 兆美元估值收購 xAI 之後，而且 SpaceX 今年可能要 IPO。半數創辦團隊出走加上監管風暴，對 IPO 來說可不是好消息。

**為什麼這道浪值得追：**
- 半數創辦團隊出走，包括安全負責人——xAI 的安全基因正在流失
- Grok deepfake 醜聞引發多國監管調查，法國已突襲 X 辦公室
- SpaceX-xAI 合併後估值 1.25 兆美元，但人才流失和監管風險可能衝擊 IPO 計畫

### [China's AI Model Rush: GLM-5, Kling 3.0, Seedance 2.0](https://www.cnbc.com/2026/02/14/new-china-ai-models-alibaba-bytedance-seedance-kuaishou-kling.html)

中國 AI 公司這週像約好了一樣集體發布——智譜 AI 的 GLM-5 是開源模型，coding 能力接近 Claude Opus 4.5、部分 benchmark 超過 Gemini 3 Pro；快手的 Kling 3.0 把影片生成拉到 15 秒、加了多語言原生音頻；字節跳動的 Seedance 2.0 支援文字+圖片+影片+音頻的混合 prompt 生成影片。

以我的觀察，這波不只是追趕——GLM-5 在開源排行榜上直接登頂 Artificial Analysis，中國 AI 公司正在用「開源 + 速度」的策略搶生態位。不過 Seedance 2.0 已經因為語音克隆的隱私爭議緊急下架了相關功能，這跟 xAI 的問題有異曲同工之妙——跑太快，安全跟不上。

**為什麼這道浪值得追：**
- GLM-5 開源登頂，coding 能力逼近 Opus 4.5——中國開源 AI 的實力不容小覷
- Kling 3.0 和 Seedance 2.0 在影片生成領域各有突破，但隱私問題也跟著來
- 繼 DeepSeek 之後，中國 AI 公司正用集體衝浪的方式搶佔全球注意力

---

## ⚡ 衝浪快報

- **[Anthropic Super Bowl Ad Boosts Claude Users 11%](https://www.cnbc.com/2026/02/13/anthropic-open-ai-super-bowl-ads.html)** — Anthropic 超級盃廣告嘲諷 ChatGPT 賣廣告，結果 Claude DAU 漲了 11%——打臉行銷學教科書，有時候最好的廣告就是嘲笑對手
- **[Microsoft: One Prompt Breaks AI Safety Across 15 Models](https://www.microsoft.com/en-us/security/blog/2026/02/09/prompt-attack-breaks-llm-safety/)** — 微軟研究員發現 GRP-Obliteration 攻擊，一個 prompt 就能把 15 個模型的安全對齊打掉，攻擊成功率從 13% 飆到 93%——AI 安全的脆弱程度超乎想像
- **[Samsung Ships Industry-First HBM4](https://news.samsung.com/global/samsung-ships-industry-first-commercial-hbm4-with-ultimate-performance-for-ai-computing)** — Samsung 開始出貨 HBM4，頻寬比 HBM3E 多 2.7 倍、最高 3.3 TB/s——AI 算力的下一個瓶頸在記憶體，這是關鍵一步
- **[Anthropic Cowork Legal Plugin Triggers $285B Selloff](https://www.bloomberg.com/news/articles/2026-02-03/legal-software-stocks-plunge-as-anthropic-releases-new-ai-tool)** — Anthropic 的法律插件讓 Thomson Reuters 跌了 18%、LexisNexis 母公司跌 14%——AI 公司不再只想當基礎設施，開始吃垂直市場的蛋糕了
- **[Perplexity Launches Model Council](https://www.perplexity.ai/hub/blog/introducing-model-council)** — 同時跑 Claude、GPT-5.2 和 Gemini 三個模型交叉驗證答案——用模型打模型來減少幻覺，思路很聰明
- **[SpaceX-xAI Merger: $1.25 Trillion Mega Deal](https://www.cnbc.com/2026/02/03/musk-xai-spacex-biggest-merger-ever.html)** — 史上最大合併案，Musk 要在太空建 AI 資料中心——野心很大，但 xAI 人才流失是個大問號
- **[Gemini 3.1 Pro Leak](https://ai505.com/gemini-3-1-pro-leaked-why-googles-thursday-hint-may-rewrite-the-ai-leaderboard/)** — Gemini 3.1 Pro 在第三方 benchmark 平台洩露，Google 似乎又要更新了——這個月模型發布的密度真的離譜
- **[ChatGPT Go Now Available Worldwide](https://openai.com/index/introducing-chatgpt-go/)** — OpenAI 把低價方案推向全球，$8/月但要看廣告——免費增值模式正式確立
- **[Seedance 2.0 Suspends Voice Clone Feature](https://www.cnbc.com/2026/02/14/new-china-ai-models-alibaba-bytedance-seedance-kuaishou-kling.html)** — ByteDance 的 Seedance 2.0 因為語音克隆隱私爭議緊急下架功能——跑太快的代價

---

## 🏄 深水區

- **[A One-Prompt Attack That Breaks LLM Safety Alignment](https://www.microsoft.com/en-us/security/blog/2026/02/09/prompt-attack-breaks-llm-safety/)** — 微軟這篇技術部落格值得每個做 AI 的人讀一遍：一個 prompt 怎麼用 GRPO 把模型的安全訓練完全反轉？當你理解攻擊原理，才知道防禦有多難
- **[Market Reaction or Overreaction? Anthropic's Legal Plugin and the Facts So Far](https://complexdiscovery.com/market-reaction-or-overreaction-anthropics-legal-plugin-and-the-facts-so-far/)** — $285B 的市值蒸發是合理反映還是過度恐慌？這篇冷靜分析了 AI 公司切入垂直市場的真正威脅程度
- **[The February 2026 AI Model Rush: 7 Major Models in a Single Month](https://jangwook.net/en/blog/en/ai-model-rush-february-2026/)** — 二月已經發布了 7 個主要模型，這篇拉高視角看整個模型競賽的格局變化——當效能差距縮小，定價、速度和生態系才是決勝關鍵
- **[Is Safety 'Dead' at xAI? (Full Report)](https://techcrunch.com/2026/02/14/is-safety-is-dead-at-xai/)** — 想深入了解 xAI 安全危機的來龍去脈，這篇 TechCrunch 的調查報導是目前最完整的
