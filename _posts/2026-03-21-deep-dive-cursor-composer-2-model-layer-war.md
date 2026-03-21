---
title: "Cursor 自研模型打趴 Claude：當你最大的客戶變成你最強的對手"
date: 2026-03-21
description: "Cursor 基於中國開源模型 Kimi k2.5 打造的 Composer 2，以十分之一的價格超越 Claude Opus 4.6。這不只是一款新模型——這是應用層吞噬模型層的第一槍，整個 AI 價值鏈正在重新洗牌。"
tags: [deep-dive, ai-coding, llm, ai-industry, agents]
---

## 引言

想像你是 Anthropic 的商務主管。你的最大客戶每年貢獻數億美元營收，你們的關係看似穩固——直到某天早上，這個客戶發布了一款自研模型，不僅在編程基準測試上打敗了你的旗艦產品，價格還只有你的十分之一。

這不是假設情境。2026 年 3 月 19 日，AI 程式碼編輯器 Cursor 正式發布 Composer 2，一款專為編程打造的 AI 模型。在 CursorBench 上，它以 61.3 分超越 Claude Opus 4.6 的 58.2 分；在 Terminal-Bench 2.0 上也以 61.7 分勝出。但真正讓業界倒吸一口涼氣的不是分數——是價格。Composer 2 的輸入價格為每百萬 token 0.5 美元，輸出價格 2.5 美元。對比 Claude Opus 4.6 的 5 美元和 25 美元，這不是腰斬，是「腳踝斬」。

更耐人尋味的是這款模型的底層基座——不是來自 OpenAI，也不是 Google，而是中國月之暗面（Moonshot AI）的開源模型 Kimi k2.5。一家美國最火的 AI 編程工具公司，用一個中國開源模型，打敗了自己最大供應商的旗艦產品。這個故事的每一層都值得細看。

這篇報導的起點是[量子位對 Cursor Composer 2 的報導](https://www.36kr.com/p/3730749500539142)，但故事遠不止於此。Composer 2 背後折射出的，是 AI 產業最核心的結構性問題：**在這場價值數兆美元的競賽中，到底是做模型的人贏，還是做產品的人贏？**

---

## 事件全貌

### Composer 2：不是通才，是專才

Cursor 共同創辦人 Aman Sanger 對 Composer 2 的定位說得很直白：「它不會幫你報稅，也不會幫你寫詩。」這句話道出了 Composer 2 和 Claude、GPT 等通用模型最大的差異——它是一款純粹為編程而生的模型。

在基準測試上，Composer 2 的表現相當亮眼：

- **CursorBench**：61.3 分（Claude Opus 4.6 為 58.2，GPT-5.4 Thinking 為 63.9）
- **Terminal-Bench 2.0**：61.7 分（Claude Opus 4.6 在 Claude Code 環境下為 58.0）
- **SWE-bench Multilingual**：73.7 分（這項測試 Claude Opus 4.6 以 77.8 分略勝）

換句話說，Composer 2 在多數編程基準上超越了 Claude Opus 4.6，但在 SWE-bench 上仍然落後，而且整體還追不上 GPT-5.4。它不是全方位的王者，而是在性價比這個維度上，打出了一個讓所有人都要重新算帳的價格。

但 Composer 2 真正讓人驚艷的是它處理超長任務的能力。Cursor 團隊展示了一個經典的壓力測試：讓模型把 Doom 遊戲移植到 MIPS 架構上運行。這需要模型自己改寫程式碼、編譯、除錯、反覆試錯——大多數模型在這種長鏈條任務中會逐漸「忘記」自己在做什麼。Composer 2 在經過 170 輪交互後成功完成，過程中將超過 10 萬個 token 的上下文壓縮到 1000 個。

### 「做筆記」的強化學習

Composer 2 能處理超長任務的秘密武器，是一種名為「自我總結強化學習」（compaction-in-the-loop RL）的新訓練方法。

傳統的上下文壓縮有兩種做法：做摘要（容易丟關鍵資訊）或滑動窗口（直接丟棄舊內容）。兩種方法的共同問題是：任務越長，模型越容易跑偏。

Cursor 的做法不同。他們讓模型在執行長任務的過程中，主動暫停下來為自己「寫筆記」——總結目前的進度、剩餘任務、關鍵決策。而且，這種總結能力不是靠提示詞引導的推理技巧，而是在強化學習訓練中被「寫死」進模型的能力：

- 總結得好 → 後續任務完成率更高 → 獎勵更高
- 總結丟了關鍵資訊 → 任務失敗 → 被懲罰

結果是，傳統方法的壓縮提示詞需要幾千個 token，壓縮後的輸出平均 5000+ token。Composer 2 只需一句「Please summarize the conversation」，壓縮後的輸出平均只有 1000 個 token。**Token 用量降到傳統方法的五分之一，壓縮帶來的錯誤率減少約 50%。**

### Kimi k2.5：中國開源模型的逆襲

Composer 2 的底層基座來自月之暗面的 Kimi k2.5。這是一個基於 Mixture-of-Experts 架構的開源模型，總參數量達 1 兆（1 trillion），但每次推理只啟動 320 億個參數，讓它在保持前沿能力的同時維持合理的推理成本。

月之暗面在 Composer 2 發布後公開表示：「我們很自豪看到 Kimi k2.5 為 Composer 2 提供了基礎。看到我們的模型通過 Cursor 的持續預訓練和高算力 RL 訓練被有效整合，正是我們所支持的開源模型生態。」

整個技術棧的結構是：月之暗面提供開源基座模型 → [Fireworks AI](https://fireworks.ai/blog/kimi-k2p5) 提供託管的 RL 訓練和推理平台 → Cursor 在上面做持續預訓練和領域特化的強化學習。

這是一個值得仔細品味的組合：**一家中國公司提供開源基座，一家美國基礎設施公司提供算力和工具，另一家美國應用公司在上面訓練出了打敗 Anthropic 的模型。** 開源生態的力量在這裡展現得淋漓盡致。

---

## 脈絡

### 從零到 500 億美元的飛速成長

Cursor 背後的公司 Anysphere 由四位 MIT 學生於 2022 年創立。CEO Michael Truell 今年才 25 歲。這家公司的成長曲線幾乎不合常理：

- 2025 年 6 月：以 99 億美元估值融資 9 億美元
- 2025 年 11 月：以 293 億美元估值融資 23 億美元，ARR 突破 10 億美元
- 2026 年 3 月：[據 Bloomberg 報導](https://www.bloomberg.com/news/articles/2026-03-19/ai-coding-startup-cursor-plans-new-model-to-rival-anthropic-openai)，正在洽談以約 500 億美元估值的新一輪融資，ARR 已超過 20 億美元

Cursor 目前擁有超過 100 萬日活用戶，包括 Stripe、Figma 在內的 5 萬家企業客戶，內部自研模型每天處理超過 5 億次推理呼叫。

### 一段複雜的供應商與競爭者關係

Cursor 和 Anthropic 的關係，是 AI 產業裡最微妙的商業關係之一。

Cursor 早期的崛起很大程度上靠的是 Claude 模型——Claude 在編程任務上的表現讓 Cursor 在 IDE 大戰中脫穎而出。據 [VentureBeat 報導](https://venturebeat.com/ai/anthropic-revenue-tied-to-two-customers-as-ai-pricing-war-threatens-margins)，Cursor 和 GitHub Copilot 合計為 Anthropic 貢獻了約 12 億美元的年營收，而 Cursor 是其中最大的單一客戶。有分析指出，Cursor 在 API 呼叫上的支出甚至超過了它自己的營收——也就是說，它一度在「倒貼」給 Anthropic 和 OpenAI。

但與此同時，Anthropic 和 OpenAI 都在做自己的程式碼工具：Anthropic 有 Claude Code（[年化營收已達 25 億美元](https://www.nxcode.io/resources/news/anthropic-380b-valuation-super-bowl-claude-code-2026)），OpenAI 有 Codex。你的供應商同時是你的競爭對手——這種結構性矛盾，終究要爆發。

Composer 2 就是這場矛盾的爆發點。

### AI 編程工具的三國時代

2026 年的 AI 編程工具市場已經形成了三種截然不同的競爭路線：

**Claude Code 路線：模型即產品。** Anthropic 把 Claude 的能力直接包裝成開發者工具，不需要 IDE，在終端裡就能運行。它的競爭力完全取決於 Claude 模型本身的能力——當 Opus 4.5 發布時，Claude Code 的能力是跳躍式提升的。在開發者滿意度調查中，[Claude Code 以 46% 的好感度遙遙領先](https://www.nxcode.io/resources/news/cursor-vs-windsurf-vs-claude-code-2026)。

**Cursor 路線：平台即護城河。** Cursor 整合多個模型供應商，提供最好的 IDE 體驗。現在又加上了自研模型，試圖在產品和模型兩個維度同時建立壁壘。

**GitHub Copilot 路線：分發即王道。** 靠 GitHub 的 1 億開發者用戶基礎，Copilot 已有 470 萬付費訂閱用戶和 90% 的財富 100 強企業採用率。它不一定最好，但最無處不在。

三條路線的共同問題是：**誰能在性能和成本之間找到最佳平衡點？** Composer 2 的出現，讓 Cursor 在這個問題上搶到了暫時的話語權。

---

## 多方觀點

### 樂觀派：應用公司的勝利

Cursor CEO Michael Truell 的態度很明確：Cursor 不是純粹的應用程式開發商，也不是模型提供商——它是一種新型態的公司。他此前在接受 [TechCrunch 採訪](https://techcrunch.com/2025/12/09/why-cursors-ceo-believes-openai-anthropic-competition-wont-crush-his-startup/)時表示，他相信 OpenAI 和 Anthropic 的競爭不會壓垮 Cursor，因為「打造最好的程式設計體驗」需要的不僅僅是最好的模型。

這種觀點有其道理。Composer 2 證明了一件事：**在垂直領域，專才可以打敗通才。** 一個只會寫程式的模型，可以用十分之一的成本打敗一個什麼都會的模型。這對所有做垂直 AI 應用的公司來說，都是一劑強心針。

矽谷知名投資人 Chamath Palihapitiya 也[在 X 上分享](https://x.com/chamath/status/2029634071966666964)了客戶視角：「自 2025 年 11 月以來，我們的 AI 成本已經增加了兩倍多，目前每年支出數百萬美元，趨勢是超過 1000 萬美元。」當企業 AI 支出以這種速度增長，任何能夠降低成本的方案都會受到熱烈歡迎。

### 質疑派：基準測試不是一切

然而，Hacker News 和開發者社群中的反應更加謹慎。

首先是基準測試的公正性問題。CursorBench 是 Cursor 自己設計的基準，Terminal-Bench 2.0 針對的也正好是 Cursor 模型所特化的 agentic 終端操作任務。在自家考場出的題目上考贏別人，說服力打了折扣。而且在 SWE-bench Multilingual 這個更通用的基準上，Composer 2 的 73.7 分仍然落後於 Claude Opus 4.6 的 77.8 分。所謂「超越 Claude」，其實是有條件的超越。

其次是推理深度的質疑。有開發者指出：「在純編程之外的任務上，比如長期運行的系統維護，Composer 沒有 Opus 4.6 的推理深度。」這不是小問題——現實中的軟體工程工作，很大一部分是理解遺留程式碼的設計意圖、在多個方案之間做取捨、處理含糊不清的需求。這些需要的不是「寫程式」的能力，而是「思考」的能力。一個專注於編程的模型在這些維度上天生就有短板。

還有可靠性的問題。2026 年 3 月初，Cursor 被確認存在程式碼回退 bug——也就是說，AI 幫你改了程式碼之後，某些情況下會把你的修改覆蓋掉。對一個日活超過百萬的開發者工具來說，這種 bug 的殺傷力不亞於任何基準測試上的失分。加上持續的穩定性問題，一些開發者對把核心工作流交給 Cursor 仍有顧慮。

### 實務開發者的聲音

在 [Cursor 社群論壇](https://forum.cursor.com/t/share-your-experience-with-composer-2/155289)上，早期使用者的回饋呈現出一個有趣的分化：

多檔案編輯和長時間重構任務上，改進是顯著的、可感知的——這不是「基準測試劇場」，而是真實的生產力提升。但在需要深度推理的複雜場景中，許多人仍然會切換到 Claude Opus 4.6。

一位開發者的評價很到位：「如果 Composer 2 真的像看起來那麼好，Anysphere 在 2026 年就是真的來了。」——但這個「如果」仍然帶著問號。

### 我的看法

以我自己用 AI 寫程式的經驗來說，Composer 2 的策略是對的——但「對」和「夠」之間還有距離。

編程是一個特別適合做模型特化的領域：任務邊界清晰、評估標準明確、訓練資料豐富。如果你只需要一個「幫你寫程式」的模型，付十倍的價格去買一個「什麼都會」的通用模型確實不划算。但問題是，真實世界的編程工作從來不只是寫程式——你還要讀文件、理解業務邏輯、做架構決策、和人溝通。Composer 2 在這些維度上的能力如何，目前還看不清楚。

更關鍵的是，模型領域的「護城河」是出了名的淺。今天你領先，明天 Anthropic 就可能推出一個更便宜的 Claude 編程特化版本把你打回原形。Cursor 真正的護城河不是模型，而是產品體驗和用戶生態。Composer 2 是錦上添花，不是護城河本身。

---

## 產業衝擊

### 第一層：Anthropic 的營收警報

這件事對 Anthropic 的直接影響是明確的：**它最大的客戶正在減少對它的依賴。**

Anthropic 目前的年化營收已達約 200 億美元，估值 3800 億美元。但如果 Cursor 這個最大客戶逐步用自研模型取代 Claude，那麼 Anthropic 在 API 業務上的營收增長故事就會出現裂痕。更糟的是，這可能是一個趨勢的開端——如果 Cursor 可以這麼做，其他大型 API 客戶為什麼不行？

好消息是，Anthropic 不再只是一家 API 公司。Claude Code 已經是一個年化營收 25 億美元的獨立產品線，直接面向開發者。在開發者滿意度調查中，Claude Code 以 46% 的好感度遙遙領先 Cursor 的 19%。它的殺手鐧在於，每次 Claude 模型升級，Claude Code 的能力就自動跳升——這是任何依賴第三方模型的工具都無法複製的結構性優勢。

但這也意味著 Anthropic 正在經歷一場身份轉換：從「模型供應商」變成「開發者工具公司」。這個轉型的時間窗口正在縮小——如果更多大客戶像 Cursor 一樣走上自研模型的道路，Anthropic 的 API 業務營收增長就會承壓，而 Claude Code 必須足夠強大來接住這個缺口。

### 第二層：開源模型的戰略價值重估

Composer 2 的故事還有一個容易被忽略的主角：月之暗面的 Kimi k2.5。

一個中國公司的開源模型，成為美國最火 AI 編程工具的底層基座，這本身就是一個值得玩味的地緣政治隱喻。它證明了開源模型的戰略價值不只是「免費替代品」——**它是讓應用層公司擺脫對閉源供應商依賴的武器。**

Fireworks AI 在這個生態中扮演的角色也值得注意。它提供了託管的 RL 訓練和推理平台，讓 Cursor 不需要從零開始搭建訓練基礎設施。這意味著，未來任何有足夠資金和工程能力的應用公司，都可以拿一個開源基座模型，在 Fireworks 這樣的平台上做領域特化，然後打造自己的垂直模型。

**模型提供商最害怕的場景正在成為現實：開源模型 + 雲端 RL 平台 + 應用公司的領域知識 = 不再需要買最貴的閉源模型。**

### 第三層：AI 定價經濟學的重塑

2026 年初以來，隨著 OpenClaw 等 AI agent 爆火，全球大模型 token 消耗量呈指數級增長，雲端廠商和模型公司紛紛漲價。在這個大環境下，Cursor 卻反其道而行——把價格打到地板。

Composer 2 的定價策略揭示了一個結構性的變化：**通用模型的定價邏輯正在被垂直模型挑戰。** 如果一個專為編程設計的模型可以在編程任務上和通用模型打平甚至更好，而價格只有十分之一，那開發者為什麼還要為通用能力買單？

這個邏輯可以推廣到所有垂直領域。如果有人做出一個專門寫法律文件的模型、一個專門做數據分析的模型、一個專門處理客服對話的模型——每一個都可能在各自的領域以更低的成本打敗通用模型。通用模型的溢價空間，正在被一個個垂直特化模型蠶食。

### 第四層：開發者工作流程的再分化

Composer 2 的出現讓 AI 編程工具市場進入了一個新的分化期。

過去，開發者的選擇相對簡單：選一個 IDE，選一個模型，開始寫程式。現在，他們面臨的是一個更複雜的決策矩陣：

- 需要深度推理和大型重構？→ Claude Code + Opus 4.6
- 需要高性價比的日常編程？→ Cursor + Composer 2
- 需要企業合規和穩定性？→ GitHub Copilot
- 需要最快的速度？→ Windsurf + SWE-1.5

每個工具的最佳使用場景越來越分化，這對開發者的工具選擇能力提出了新的要求——**以後評價一個開發者的標準，可能不只是他寫程式的能力，還包括他選擇和搭配 AI 工具的能力。**

這種分化還有一個更深層的影響：它正在改變軟體公司的成本結構。過去，AI 編程的成本主要是訂閱費——Cursor Pro 每月 20 美元，GitHub Copilot 每月 10 美元。但現在，隨著 agent 模式的普及和 token 消耗量的暴增，真正的成本在 API 呼叫上。Chamath 提到他們公司的 AI 支出已經趨近每年 1000 萬美元。在這種規模下，Composer 2 帶來的十倍價格差異，不是「省一杯咖啡」，而是「省一個工程團隊的年薪」。

---

## 未來展望

### 短期（3-6 個月）

**Composer 3 即將到來。** Cursor 研究員已經開始放出 Composer 3 的消息。以 Cursor 從 Composer 1.5 到 Composer 2 的迭代速度來看（大約兩個月），Composer 3 很可能在 2026 年中期發布。如果它能在 SWE-bench 和推理任務上也超越 Claude Opus 4.6，那故事就完全不同了。

**Anthropic 幾乎確定會有反應。** 不管是推出編程特化版的 Claude，還是在 API 定價上做出調整，Anthropic 不可能坐視自己最大的客戶逐步脫離。我們可能會看到一波針對編程場景的模型降價潮。

**更多應用公司會跟進。** Cursor 的路線已經被驗證了——拿開源模型做底座、在雲端平台上做領域特化。接下來，法律科技、醫療、金融等領域的應用公司都可能嘗試類似的策略。

### 中期（6-18 個月）

**情境一：Cursor 成功建立模型 + 產品的雙重護城河。** 如果 Composer 系列持續進化，Cursor 可能逐步減少對外部模型的依賴，從一個「IDE 公司」變成一個「AI 編程平台公司」。500 億美元的估值可能只是起點。

**情境二：模型軍備競賽加劇，Cursor 的模型優勢被抹平。** Anthropic、OpenAI、Google 都有能力推出編程特化模型，而且它們的資源遠超 Cursor。如果 Claude 的編程特化版本在性能和價格上都追上 Composer，Cursor 的模型故事就會褪色，回歸到產品體驗的競爭。

**情境三：開源模型持續進化，模型層的價值被持續壓縮。** 如果 Kimi k3、Llama 5 等下一代開源模型繼續提升，那所有閉源模型的溢價空間都會被壓縮。在這個情境下，Cursor 受益（因為它可以持續用最新的開源模型做特化），而 Anthropic 和 OpenAI 的 API 定價權力被削弱。

### 長期推演

如果 Cursor 的路線被證明是對的，3-5 年後我們可能會看到 AI 產業的一個根本性轉變：**模型層變成「公用事業」，真正的價值在應用層。**

這不是沒有先例。雲端運算的早期，AWS、Azure、GCP 是絕對的王者。但隨著雲端基礎設施的商品化，真正賺錢的是建立在雲端之上的 SaaS 應用。AI 產業可能正在走同一條路——模型是必要的基礎設施，但不是最終的價值捕獲點。

### 給不同角色的建議

**如果你是開發者：** 現在就開始學習如何評估和搭配不同的 AI 編程工具。不要只押注一個工具——學會在不同場景下切換。深度推理用 Claude Code，日常編碼用 Composer 2，快速原型用 Copilot。工具選擇能力正在成為一項核心技能。

**如果你是創業者或產品經理：** Composer 2 證明了一條路——用開源基座模型 + 領域數據 + 雲端 RL 平台做垂直特化。如果你的產品有大量的使用者行為數據和領域專業知識，現在可能是開始考慮自研模型的時機。不需要從零開始，開源生態已經幫你走完了最難的那段路。

**如果你是在模型公司工作：** 注意你們最大客戶的動向。Cursor 不會是最後一個走上自研模型道路的大客戶。思考如何讓你的模型在「不可替代」的維度上建立價值——不是在編程這種可以被特化模型取代的任務上，而是在需要廣泛推理能力的複雜場景上。

回到最初的問題：當你最大的客戶變成你最強的對手，你該怎麼辦？Anthropic 的答案可能是：**讓自己在客戶無法自建的維度上變得更強。** 通用推理能力、安全性、可靠性——這些是 Cursor 用一個開源模型做特化所無法輕易複製的。

但這場賽跑的窗口正在收窄。Composer 3 已經在路上了。

---

## 延伸閱讀

- [Cursor's new coding model Composer 2 is here — VentureBeat](https://venturebeat.com/technology/cursors-new-coding-model-composer-2-is-here-it-beats-claude-opus-4-6-but)：最完整的 Composer 2 技術分析和基準測試比較
- [Cursor takes on OpenAI and Anthropic with Composer 2 — The Decoder](https://the-decoder.com/cursor-takes-on-openai-and-anthropic-with-composer-2-a-code-only-model-built-to-match-rivals-at-a-fraction-of-the-cost/)：深入分析 Cursor 的商業策略和與模型公司的競爭關係
- [Kimi K2.5 Is Live on Fireworks — Fireworks AI Blog](https://fireworks.ai/blog/kimi-k2p5)：了解 Kimi k2.5 的技術規格和 Fireworks 的全參數 RL 訓練能力
- [AI Coding Startup Cursor Plans New Model to Rival Anthropic, OpenAI — Bloomberg](https://www.bloomberg.com/news/articles/2026-03-19/ai-coding-startup-cursor-plans-new-model-to-rival-anthropic-openai)：Bloomberg 對 Cursor 500 億美元估值融資談判的獨家報導
- [Claude Code Hits Inflection Point — The Meridiem](https://www.themeridiem.com/ai-machine-learning/2026/1/22/claude-code-hits-inflection-point-as-anthropic-shifts-to-product-led-revenue)：Anthropic 從 API 公司轉向產品驅動的營收模式分析
- [Anthropic revenue tied to two customers — VentureBeat](https://venturebeat.com/ai/anthropic-revenue-tied-to-two-customers-as-ai-pricing-war-threatens-margins)：Anthropic 營收結構的風險分析，揭示對 Cursor 和 GitHub Copilot 的依賴
- [Why Cursor's CEO believes OpenAI, Anthropic competition won't crush his startup — TechCrunch](https://techcrunch.com/2025/12/09/why-cursors-ceo-believes-openai-anthropic-competition-wont-crush-his-startup/)：Michael Truell 對 Cursor 競爭策略的完整闡述
- [Kimi.ai on Composer 2 — Simon Willison](https://simonwillison.net/2026/Mar/20/cursor-on-kimi/)：月之暗面對 Cursor 使用 Kimi k2.5 作為基座模型的官方回應
