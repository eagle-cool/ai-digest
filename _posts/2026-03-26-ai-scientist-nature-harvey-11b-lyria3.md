---
title: "AI 自己發了篇 Nature、Harvey 估值飆破 $11B"
date: 2026-03-26
description: "Sakana AI 的 AI Scientist 登上 Nature 實現端到端自動化科研，Harvey 估值飆到 110 億美元 Sequoia 三度加碼，Google Lyria 3 Pro 讓 AI 寫三分鐘完整歌曲。"
tags: [ai-research, ai-industry, ai-tools, llm]
---

今天的浪有股學術味——AI 不只會寫 code、會聊天，現在連科學論文都自己從頭寫到尾、還通過了同行評審。與此同時，法律 AI 獨角獸 Harvey 的估值在一年內翻了 3.5 倍，Sequoia 都忍不住三度加碼。Google 那邊也沒閒著，Lyria 3 Pro 要讓 AI 幫你寫出完整的三分鐘歌曲。

---

## 🌊 今日浪頭

### [The AI Scientist 登上 Nature：端到端自動化 AI 科研時代來臨](https://www.36kr.com/p/3738564116021512)

我看到這篇的時候停下來想了很久。Sakana AI 和牛津大學、UBC 合作打造的 The AI Scientist，不是那種「幫你查文獻」的半吊子工具——它是真的從零開始：自己想研究題目、自己寫 code 跑實驗、自己畫圖分析數據、自己寫完整論文，最後還自己做同行評審。整套科研流程，全自動。

最猛的是，研究團隊把 3 篇完全由 AI 生成的論文提交到 ICLR 2025 研討會，採盲審——審稿人只知道裡面有 AI 寫的，但不知道是哪幾篇。結果其中一篇拿到了 6.33 分（三位審稿人給 6、7、6），高於平均錄取線，如果不是因為「AI 生成」被撤回，幾乎確定會被收錄。這篇研究現在正式發表在 Nature 上。

當然也得冷靜看——另外兩篇沒過，系統還有不少失敗模式：想法太淺、code 有 bug、引用會幻覺。但趨勢很明確：隨著底層模型變強，AI Scientist 的產出品質也在跟著往上走。

**為什麼這道浪值得追：**
- 這是 AI 首次以完全自動化的方式通過頂級 ML 會議的同行評審——不是靠人類潤稿，是從頭到尾全自動
- 自動審稿人的表現居然跟人類審稿人旗鼓相當，甚至在部分指標上更好，這對學術界的衝擊可能比論文本身更大
- 科研效率的天花板正在被重新定義——問題不再是「AI 能不能做研究」，而是「多快能做到頂級水準」

### [Harvey 估值確認 $11B，Sequoia 三度領投加碼](https://techcrunch.com/2026/03/25/harvey-confirms-11b-valuation-sequoia-triples-down/)

法律 AI 這條賽道，Harvey 已經跑到讓人瞠目結舌的地步了。

公司確認完成新一輪 $200M 融資，由新加坡 GIC 和 Sequoia 共同領投，估值來到 $11B。上一輪是去年 12 月的 $8B（a16z 領投），再上一輪是去年 6 月的 $5B，再再上一輪是 2025 年 2 月的 $3B。一年之內，估值翻了 3.5 倍。累計融資已經超過 $10 億。

Sequoia 合夥人 Pat Grady 自己都承認，從 Series A 開始三度共同領投同一家公司，在 Sequoia 的歷史上是極不尋常的。但他們就是忍不住加碼。以我的觀察，這說明一件事：AI 在法律領域的商業化不是願景，是已經在發生的事。

**為什麼這道浪值得追：**
- 一年 3.5 倍的估值增長不是靠 hype，是靠真實的企業客戶付費——法律事務所對這東西是真的買單
- Sequoia 三次加碼的信號意義巨大：這家以挑剔著稱的 VC 認為 Harvey 的護城河已經深到值得反覆下注
- AI + 垂直產業的故事，Harvey 可能是目前最有說服力的案例之一

### [Google 推出 Lyria 3 Pro，AI 作曲進入三分鐘完整歌曲時代](https://techcrunch.com/2026/03/25/google-launches-lyria-3-pro-music-generation-model/)

還記得一個月前 Lyria 3 只能生成 30 秒嗎？Google 直接把時間拉到 3 分鐘——這不是 demo 片段了，是一首完整的歌。

Lyria 3 Pro 不只是時間變長，模型對歌曲結構的理解也跳了一個台階。你可以在 prompt 裡指定前奏、主歌、副歌、過門，它會按結構去編排。如果你提到某位藝人，它會取「廣泛靈感」（Google 的措辭很小心）但不會直接模仿。所有生成的音軌都會用 SynthID 標記。

目前 Lyria 3 Pro 會在 Gemini 付費用戶、Google Vids、ProducerAI，以及 Vertex AI / Gemini API / AI Studio 上推出。Google 把先前收購的 ProducerAI 也整合進來了，顯然是要把 AI 音樂做成一條完整的產品線。

**為什麼這道浪值得追：**
- 從 30 秒到 3 分鐘不只是量變——這代表模型能維持長時間的音樂連貫性，技術門檻明顯不同
- 同一週 Spotify 推出防 AI 冒名工具、Deezer 推出 AI 音樂辨識——產業攻防已經全面展開
- API 開放意味著開發者可以開始在自己的產品裡內建 AI 作曲功能，這個生態才剛開始

---

## ⚡ 衝浪快報

- **[OpenAI 公開 Model Spec 完整框架，揭秘模型行為怎麼被定義](https://openai.com/index/our-approach-to-the-model-spec)** — 想知道 ChatGPT 為什麼有些事做有些事不做？這份文件就是答案，是目前最透明的 AI 行為規範說明
- **[Google TurboQuant 壓縮演算法亮相，網友直呼「這不就是 Pied Piper 嗎」](https://techcrunch.com/2026/03/25/google-turboquant-ai-memory-compression-silicon-valley-pied-piper/)** — Google 發布新的 AI 記憶體壓縮技術，HBO Silicon Valley 的粉絲集體興奮了
- **[Sanders 和 AOC 提案全面禁止新建資料中心](https://techcrunch.com/2026/03/25/bernie-sanders-and-aoc-propose-a-ban-on-data-center-construction/)** — 能源消耗和環境影響終於炸到國會了，雖然通過機率不高，但政治信號很明確
- **[美國參議員要把 Anthropic 的「不做自主武器」承諾寫進法律](https://www.theverge.com/policy/900341/senator-schiff-anthropic-autonomous-weapons-mass-surveillance)** — Schiff 參議員推動立法，禁止 AI 用於自主武器和大規模監控，Anthropic 的自律正在變成監管框架
- **[Zuckerberg、黃仁勳加入 Trump 新科技顧問團](https://www.theverge.com/policy/900340/trump-tech-panel-mark-zuckerberg-jensen-huang)** — Meta、NVIDIA、Oracle 高層都進了白宮科技小組，AI 政策的風向標又要動了
- **[Granola 融 $125M 估值飆到 $1.5B，從會議筆記工具轉型企業 AI](https://techcrunch.com/2026/03/25/granola-raises-125m-hits-1-5b-valuation-as-it-expands-from-meeting-notetaker-to-enterprise-ai-app/)** — 六個月估值翻六倍，證明 AI 在企業端的需求爆發力有多猛
- **[Reddit 出手：可疑的 bot 帳號以後要「證明你是人類」](https://www.theverge.com/tech/900363/reddit-human-verification-bots-crackdown)** — AI bot 氾濫已經逼到平台不得不對自己的用戶做真人驗證了
- **[EvoClaw 研究揭露：AI Agent 持續開發的成功率只有 13.37%](https://www.36kr.com/p/3738221486096392)** — 別被 demo 騙了，讓 Agent 持續維護一個專案的真實表現還很慘，現實比想像的骨感
- **[Sora 沒了，但字節的 Seedance 還不能躺平](https://www.36kr.com/p/3738203168256515)** — OpenAI 退出影片生成賽道，短期利好中國選手，但 Seedance 面對的挑戰一點沒少
- **[LiteLLM 攻擊後續：46 分鐘內被下載了 47,000 次](https://simonwillison.net/2026/Mar/25/litellm-hack/#atom-everything)** — 有人用 BigQuery PyPI 資料算出了精確數字，兩個惡意版本在 46 分鐘窗口內被下載近 47K 次，影響範圍比預期更大

---

## 🏄 深水區

- **[The AI Industry Is Lying To You](https://www.wheresyoured.at/the-ai-industry-is-lying-to-you/)** — Ed Zitron 的長文分析，拆解 AI 產業裡的數字灌水和故事包裝。不管你同不同意他的結論，裡面對 NVIDIA、OpenAI 的財務分析值得花時間看
- **[NeurIPS 2026 新規引爆中國 AI 學術圈：被制裁機構論文不收](https://www.36kr.com/p/3737916477734920)** — NeurIPS 對被制裁機構說不、ICML 審稿品質崩盤——兩大頂會的爭議讓人重新思考 AI 學術生態的健康度
- **[「寫 code 最難的部分從來不是打字」](https://simonwillison.net/2026/Mar/23/david-abram/#atom-everything)** — 在所有人都在歡呼 AI 能寫 code 的時候，這段話提醒我們：理解系統、除錯、架構設計——這些真正難的事，AI 還差得遠
