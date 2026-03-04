---
title: "GPT-5.3 治好 AI 爹味、Gemini 3.1 Flash-Lite 四分之一價碾壓"
date: 2026-03-04
description: "OpenAI 連夜推出 GPT-5.3 Instant 反擊 Google，幻覺率砍 27% 爹味全消；Gemini 3.1 Flash-Lite 以 363 tokens/s 和四分之一價格碾壓同級；Apple M5 Max AI 性能暴漲四倍。"
tags: [llm, ai-tools, ai-industry]
---

今天 AI 模型戰場的節奏有點瘋——Google 深夜丟出 Gemini 3.1 Flash-Lite，不到兩小時 OpenAI 就祭出 GPT-5.3 Instant 反擊。最妙的是，兩家打法完全不同：一個卷性價比，一個卷體驗。然後 Apple 在旁邊默默掏出 M5 Max，說你們繼續吵，我先把 AI 算力暴漲四倍。

---

## 🌊 今日浪頭

### [GPT-5.3 Instant: 治好爹味、砍掉廢話、幻覺率降 27%](https://openai.com/index/gpt-5-3-instant)

我看了一下 GPT-5.3 Instant 的更新，這次 OpenAI 做了一件很聰明的事——不卷跑分，專治用戶最受不了的那些毛病。以前問個正常問題，模型先甩一段免責聲明再拒絕你，現在直接回答「沒問題，我能幫你」。搜尋結果也不再甩一串連結了事，而是用自己的知識補充背景。最讓人印象深刻的是情商升級：不再動不動「停下來，深呼吸」，不再居高臨下揣測你的情緒。

從數據面看，高風險領域（醫學、法律、金融）聯網時幻覺率降了 26.8%，用戶回報的事實錯誤也少了 22.5%。寫作能力也開竅了——以前寫詩用抽象感傷的套路「告訴」你該感動了，現在會用具體細節讓你自己去感受。OpenAI 同時放話 GPT-5.4 比你想得更快來，在 Gemini 和 Claude 輪番登頂的當下，這場貼身肉搏的火藥味越來越濃。

**為什麼這道浪值得追：**
- 不卷 benchmark 改卷用戶體驗，這個策略轉向值得關注——當跑分分不出勝負，誰能讓人「用起來舒服」誰贏
- 幻覺率降 27% 是實打實的進步，尤其在醫療法律等高風險場景意義重大
- GPT-5.4 預告暗示 OpenAI 要加速迭代節奏，模型更新週期正在從季度縮短到月度

### [Gemini 3.1 Flash-Lite: 363 tokens/s、四分之一價格碾壓全場](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-1-flash-lite/)

這個數字讓我看了兩遍——363 tokens/s，是 GPT-5 mini 的 5 倍、Claude 4.5 Haiku 的 3.4 倍。輸出價格 $1.50/百萬 token，只有 Claude 4.5 Haiku 的不到三分之一。更離譜的是跑分：GPQA Diamond 86.9% 碾壓 GPT-5 mini 的 82.3%，事實準確性 SimpleQA 上 43.3% 對 GPT-5 mini 的 9.5%——將近 4.5 倍的差距，這已經不是碾壓，是降維打擊。

以我的觀察，Flash-Lite 在 Chatbot Arena 的 Elo 分數 1432，跟 OpenAI 的旗艦推理模型 o3 打平。一個定價 $0.25/M 輸入的輕量模型，跟人家旗艦打平手，這個性價比足以改變整個市場格局。不過代碼生成仍是短板，LiveCodeBench 72% 被 GPT-5 mini 的 80.4% 明顯拉開。

**為什麼這道浪值得追：**
- 性價比戰爭正式開打——以前卷「誰最強」，現在卷「誰又強又便宜」，開發者的 API 成本可能直接腰斬
- Elo 1432 跟 o3 平手意味著輕量模型正在逼近旗艦效能，模型分級的舊秩序正在瓦解
- 思考深度可調（thinking levels）讓同一個模型能應對從批量翻譯到複雜推理的全場景，架構設計邏輯要重新想了

### [Apple M5 Pro/Max MacBook Pro: AI 性能暴漲四倍、Chiplet 首次上筆電](https://www.36kr.com/p/3707756341801349)

Apple 這次的刀法有點不一樣。M5 Max 的每個 GPU 核心都塞進了神經網路加速器，加上統一記憶體頻寬升級到 614GB/s，AI 峰值效能比上代暴漲了 4 倍。更值得關注的是首次在筆電上用了「拼好芯」Chiplet 架構——兩顆 3nm 晶粒合二為一，CPU 全部 18 核大核心設計，這在 PC 端是真的猛。

實際場景的提升很直觀：AI 圖片生成快 4 倍、LLM prompt 處理大幅提升、SSD 讀寫速度翻倍到 14.5GB/s。Apple 官網特別提到 Msty Studio 和 LM Studio 這些本地大模型應用，等於在說：跑本地模型這件事，我們認真的。起售價 17,999 元（14 吋 M5 Pro），頂配拉滿 64,719 元——比上代漲了 2,300 元，但起步就給 24GB+1TB，這次算是加量加價。

**為什麼這道浪值得追：**
- 本地 AI 推論算力四倍提升意味著更多 AI 任務可以在端側完成，隱私和延遲都受益
- Chiplet 架構進筆電是半導體業的里程碑，後續 M5 Ultra 的效能天花板會更高
- 24 小時續航 + 4 倍 AI 效能，Apple 在「AI PC」敘事上開始認真出牌了

---

## ⚡ 衝浪快報

- **[Alibaba's Qwen tech lead steps down after major AI push](https://techcrunch.com/2026/03/03/alibabas-qwen-tech-lead-steps-down-after-major-ai-push/)** — 千問掌舵人林俊旸在 Qwen3.5 發布後突然卸任，同事直言「不是他自己的選擇」，大模型團隊的高壓與人才流動再次浮上檯面
- **[AI Agent 五天搞定菲爾茲獎成果形式化，20 萬行 Lean 代碼已公開](https://www.36kr.com/p/3707141045366916)** — Math 公司的 Gauss AI 獨立完成原本需要半年的工作，被數學家稱為「自動形式化領域的 ImageNet 時刻」
- **[三家具身智能企業同日融資共 38 億元](https://www.36kr.com/p/3707043535778177)** — 銀河通用 25 億、松延動力 10 億、UniX AI 3 億，中國今年已完成 88 起融資超 200 億元，具身智能瘋狂燒錢中
- **[吳恩達：AI 很熱，但別把 AGI 說早了](https://www.36kr.com/p/3707873392390662)** — 吳恩達直言 AGI 定義正被行銷話術濫用，與其等超級智能降臨，不如聚焦 Agentic Workflows 做實際的事
- **[LLMs can unmask pseudonymous users at scale](https://arstechnica.com/security/2026/03/llms-can-unmask-pseudonymous-users-at-scale-with-surprising-accuracy/)** — Princeton 研究證實 LLM 能大規模去匿名化社群帳號，你的匿名小號可能沒你想的那麼安全
- **[開源 AI 駭客 Agent「Shannon」：自動找漏洞還能真的打進去](https://www.reddit.com/r/AIDeveloperNews/comments/1rjxskx/someone_just_open_sourced_a_fully_autonomous_ai/)** — 不只掃描，是真的注入、繞過認證、拿到資料庫，AI 安全攻防進入全自動時代
- **[Google Pixel 更新讓 Gemini 幫你叫外送和叫車](https://www.theverge.com/tech/888295/google-gemini-pixel-drop-march-2026)** — Gemini 終於能替你「做事」了，不只回答問題，還能下單訂菜和預約行程
- **[X 將暫停未標註 AI 生成武裝衝突內容的創作者收益](https://techcrunch.com/2026/03/03/x-says-it-will-suspend-creators-from-revenue-sharing-program-for-unlabeled-ai-posts-of-armed-conflict/)** — 三個月禁令加累犯永久封殺，deepfake 戰爭內容的管制力道升級了
- **[AI 公司砸 1.25 億美元阻擋推動 AI 監管的前科技高管選國會](https://techcrunch.com/2026/03/03/ai-companies-are-spending-millions-to-thwart-this-former-tech-execs-congressional-bid/)** — 科技億萬富翁支持的超級 PAC 全力打壓 AI 監管派候選人，錢和政治的遊戲越來越赤裸
- **[AI 新創用同一股權賣兩個價格製造獨角獸](https://techcrunch.com/2026/03/03/why-ai-startups-are-selling-the-same-equity-at-two-different-prices/)** — 新型估值機制讓 AI 新創能在紙面上製造獨角獸地位，聰明還是泡沫？

---

## 🏄 深水區

- **[Sycophantic AI distorts belief, manufacturing certainty where there should be doubt](https://garymarcus.substack.com/p/breaking-sycophantic-ai-distorts)** — Princeton 最新研究揭示討好型 AI 如何系統性扭曲使用者信念，從教育到科研到政治決策都受影響，每個 AI 重度用戶都該讀
- **[AI 會擁有審美嗎？Claude 設計負責人的答案出乎意料](https://www.36kr.com/p/3707777344795010)** — Anthropic 的 Jenny Wen 從 Figma 設計總監到 Claude Co-work 負責人，她不是在預測未來，是在描述設計師每天正在被 AI 改變的現實
- **[2026 編程大分流：執行者 vs 編排者，你選哪邊？](https://www.36kr.com/p/3674148254475140)** — AI 時代程式設計師正在分成兩條路：被代碼淹沒的執行者，或是駕馭智能體的編排者，你站哪邊？
- **[AI 國防：一個被低估的新風口](https://www.36kr.com/p/3707157440557190)** — 從 Anduril 到 Palantir，AI 正在重新定義軍工產業的商業模式，用軟體定義武器系統的時代已經來了
