---
title: "Copilot 關掉註冊那一夜：補貼式 AI 的派對正式結束"
date: 2026-04-21
description: "4 月 20 日，GitHub Copilot 停止收新客戶、把 Opus 踢出 10 美元方案、並預告轉向按 token 計費。內部文件顯示，這個產品每週的跑動成本自 1 月以來幾乎翻倍。這不是一次鐵定價策略調整——這是整個 AI 產業被迫承認：那套按月 10 塊美元就能無限燒 Opus 的補貼派對，已經沒有下一輪了。"
tags: [deep-dive, ai-coding, ai-industry, ai-tools, agents, llm]
---

## 引言

想像一個畫面：2026 年 4 月 21 日的清晨，一位剛從 bootcamp 畢業的新開發者，興沖沖地打開 GitHub，想訂閱 Copilot Pro，準備用 AI 配合他的履歷專案。按下 Subscribe，跳出一個冷冰冰的訊息：**「新帳戶註冊暫停中。」**

不是你的信用卡被拒、不是網路故障、不是 GitHub 當機。是 Microsoft——那家市值三兆美元、現金流堪比印鈔機、把 AI 喊成公司未來的巨頭——**主動把門關起來，不收新錢了**。

Pro、Pro+、學生方案，一起停收。Opus 系列模型從 10 美元的 Pro 方案整組拔掉。用 Opus 4.7 的 request multiplier 被暫時調到 7.5 倍——你問一次 AI 寫程式，實際上是吃掉七次半的額度。而最讓產業震動的，是一份被 Ed Zitron 拿到的內部文件揭露的一行字：**從 1 月到 4 月，Copilot 每週的運行成本幾乎翻了一倍。**

這不是 Copilot 一個產品的定價調整，這是整個 AI 補貼時代走到盡頭的煙火秀。過去兩年我們被「一個月 10 美元無限用」慣壞了：訂閱一個帳戶，就可以讓 AI 幫你寫程式、改 bug、重構整個 repo，模型越挑越貴、token 越燒越兇，背後的帳單全是 Microsoft、Anthropic、OpenAI 在扛。現在帳單攤開了。

這篇文章想帶你看清楚三件事——**Microsoft 為什麼被迫按下暫停鍵、這個訊號為什麼不只關於 Copilot、以及當「AI 按月吃到飽」變成「AI 按表計費」之後，開發者、創業者、整個軟體產業會被怎麼重塑**。故事的起點是 Ed Zitron 拿到的那份內部文件（[Microsoft To Shift GitHub Copilot Users To Token-Based Billing](https://www.wheresyoured.at/news-microsoft-to-shift-github-copilot-users-to-token-based-billing-reduce-rate-limits-2/)），但這件事的震央遠遠不只在 Redmond。

---

## 事件全貌

先把事情的骨架擺清楚。

**4 月 20 日當天，GitHub 在[官方 changelog](https://github.blog/changelog/2026-04-20-changes-to-github-copilot-plans-for-individuals/) 一次丟出三顆炸彈：**

第一，**暫停新註冊**。Pro（10 美元/月）、Pro+（39 美元/月）、以及免費教育方案裡的 Student 方案，全部停收新帳戶。既有訂閱者可以繼續用，也可以升級方案，但新臉孔暫時進不來。官方的說法很官腔：「為了確保我們能以可預期的品質服務既有付費客戶。」

第二，**把 Opus 從 Pro 方案整組踢掉**。10 美元的 Pro 用戶從今以後沒有 Anthropic 任何一代 Opus 可以選。Opus 4.7 只留在 Pro+，而 Pro+ 的 Opus 4.5、4.6 也會在未來幾週內被下架，只剩 4.7。

第三，**進一步收緊速率限制**，並且宣告要往 **token-based billing（按 token 計費）** 的方向走。官方還沒宣布切換日期，但方向定了。

比這份官方公告更關鍵的，是 Zitron 拿到的那份內部文件。裡頭有一句話，等於是整份文件的引信：「**自 1 月以來，GitHub Copilot 每週運行成本（week-over-week cost）幾乎翻倍。**」也就是說，從農曆年到現在這三個多月，這個產品燒掉的算力成本以接近指數的速度往上爬。

GitHub 產品副總 Joe Binder 在接受《The Register》訪問時，[把這件事講得更直白](https://www.theregister.com/2026/04/20/microsofts_github_grounds_copilot_account/)：「Agentic workflows 從根本上改變了 Copilot 的算力需求——agent 正在做更多的事，有越來越多客戶撞到為了維持服務可靠性而設計的使用上限。」他還補了一句殺傷力更大的：**「現在很常見的情況是，少數幾次 request 產生的成本就會超過整個月方案的價格。**」

一個月付 10 美元的客戶，幾次 request 就吃掉 Microsoft 超過 10 美元的成本——這是 GitHub 自己官方承認的。

關於 7.5x multiplier，背景是這樣：Copilot 本來用「premium request」當計費單位，Pro 一個月 300 次、Pro+ 一個月 1500 次。不同模型有不同的 multiplier，代表一次 request 實際換算成多少額度。GPT-5.4 Mini 的 multiplier 是 0.33（輕量、一次當 1/3 次），被下架的 Opus 4.6 Fast 是 30（重到離譜），標準版 Opus 4.6 是 3。現在 Opus 4.7 上場，起跳 7.5——也就是說，[allthings.how 的分析指出](https://allthings.how/claude-opus-4-7-lands-in-github-copilot-at-a-7-5x-premium-request-rate/)，你之前在 Opus 4.6 一個月可以跑的工作量（從 3 倍 multiplier 吃 1500 次額度≈ 500 turns），換成 Opus 4.7 變成剩下 200 turns 左右。

這一切還有一個值得一提的前情：就在這波動作前幾天，Microsoft 才把 Opus 4.6 Fast 從 Pro+ 下架，當時的官方說法是「把資源集中在用戶最常用的模型上」。現在回頭看，那句話其實是「我們沒辦法繼續賠錢給你用重型模型了」的公關版翻譯。

---

## 脈絡

這件事不能只看 Microsoft。這是整個產業正在一起翻桌。

**Anthropic 已經先走一步。** 根據 [The Information 的報導](https://www.theinformation.com/articles/anthropic-changes-pricing-bill-firms-based-ai-use-amid-compute-crunch)，Anthropic 從 2025 年 11 月開始，陸續把續約的企業客戶改到「usage-based」方案。到了 2026 年初，[Implicator.ai 整理出的新結構](https://www.implicator.ai/anthropic-shifts-enterprise-billing-to-per-token-pricing-the-flat-fee-era-is-over/) 已經很清楚：原本 Premium 和 Standard 兩個企業 tier 被拆成兩個產品——Claude Code 20 美元/人/月（給工程師）、Claude.ai 10 美元/人/月（給業務），但這兩個錢只買「平台存取權」，所有 Claude、Claude Code、Cowork 的使用量都按 API 標準費率另外計。白話說就是：**座位費照收，token 錢照算，飯店房卡和 mini bar 分開算帳。**

Anthropic 這麼做的底氣是它的收入：年化營收從 2025 年底的 90 億美元，衝到 2026 年 4 月的 300 億美元，四個月翻三倍；超過 1,000 家客戶一年付他們超過 100 萬美元。但它的成本壓力也是真的——[Ed Zitron 的《Subprime AI Crisis》分析](https://www.wheresyoured.at/the-subprime-ai-crisis-is-here/) 點出：Anthropic 至今賺了 50 億美元，但花在算力的錢已經 100 億。也就是**每賺一塊，燒兩塊。**

**OpenAI 也動了。** Codex 在 4 月初悄悄改成 token metering；Google 對 Gemini 的開發者工具祭出類似的高峰時段節流政策；Windsurf 在 3 月把「credits」改成「daily quotas」。[一份 CNBC 的產業觀察](https://www.cnbc.com/2026/04/17/ai-tokens-anthropic-openai-nvidia.html) 甚至直接下了個結論：**Anthropic 是少數誠實把需求數字講出來的公司，其他家都還在粉飾太平。**

為什麼是現在？三個宏觀數字講清楚了：

- **Blackwell 的租賃價格兩個月內漲了 48%**。CoreWeave 漲價超過 20%，對中小買家還開始要求三年合約。
- **OpenAI 的 token 消耗量從 2025 年 10 月的每分鐘 60 億，衝到 2026 年 3 月底的 150 億**。五個月，**兩倍半**。
- **PJM（美國東部電網營運商）估計到 2027 年初需要再多 15 GW 供電才夠 AI 用**。這不是軟體問題了，這是實體電網問題。

把這些串起來：**模型越做越強（GPT-5.4、Opus 4.7、Mythos）→ 推理變深（chain-of-thought 會吃掉指數倍的 token）→ agentic workflow 普及（一次任務跑四千次 tool call）→ 推理需求爆炸 → GPU/電力/冷卻跟不上 → 成本上漲 → 訂閱制吃不住 → 轉按量計費**。這不是誰的選擇，這是熱力學。

對了，我在一週前也寫過另一個前情節——[Anthropic 封殺 OpenClaw、SaaS 市值蒸發 2,850 億美元的那場定價危機](/posts/deep-dive-ai-agent-subscription-pricing-crisis/)。那時的震央是 Agent 工具繞過訂閱制的漏洞。今天這件事是同一條故事線的下一集：**不只是 Agent 在撐爆訂閱，連個人開發者正常使用 Copilot 都已經撐爆了它。**

---

## 多方觀點

這件事沒有一個誰是壞人的版本。不同位置的人看到的是不同的風景。

**開發者的聲音：憤怒、迷惑、但也有人清醒。** 在 GitHub 的 community discussion 和 Reddit r/GithubCopilot 上，開發者對 7.5x multiplier 的反應最直接：「The 7.5x multiplier is absolutely outrageous, the value has completely disappeared.」有人做了很直白的數學：**Opus 4.7 真的比 4.6 好 2.5 倍嗎？** 因為這就是 multiplier 從 3 跳到 7.5 要求你接受的溢價比例。一個 Pro+ 用戶用 Opus 4.7 一個月只能跑大約 200 個 turns，三月前同樣的錢可以跑 500 個。更糟的是[有人回報請款明細裡出現自己根本沒用過的模型](https://github.com/orgs/community/discussions/192911)——這種帳單爭議再往前推演，是個 PR 災難。

**微軟的官方立場：「為了既有客戶的體驗。」** Joe Binder 說的「agentic workflows 改變了算力需求」其實是真話——agent 真的燒 token，agent 真的不是給訂閱制設計的。但這個話術同時也是一種風險轉嫁：把問題從「我們的定價模型沒算到這個」包裝成「客戶的使用方式變了」。這兩個其實是同一件事，只是責任方向相反。

**Zitron 與批評者的聲音：派對結束了。** 這派的核心論點是——**過去兩年所有的 AI 訂閱價格都是假的**。[Zitron 的原文寫道](https://www.wheresyoured.at/subprimeai/)：「每一個 AI 新創都在讓你每 1 美元訂閱費燒掉高達 8 美元的 token。」AI 需求之所以存在，很大程度上是因為成本被補貼掉了——當真實成本被還原，需求會評估。把這件事放回 subprime 2008 的類比：次貸不是「壞產品」，次貸是「用錯價格賣好產品」。AI 的問題差不多。

**Anthropic 和 OpenAI 的立場：我們願意誠實，但價格只會往上。** Anthropic 的 CFO 在幾個場合都講過類似的話——flat fee 無法反映實際使用，按量是唯一可永續的方式。OpenAI 悄悄動手，嘴上不承認，但動作方向一致。他們其實都希望整個產業一起轉——因為如果只有一家這麼做，那家會先掉客戶。

**實務工作者的第一線反饋：Cursor 的處境像一面鏡子。** [Cursor 2026 年 2 月年化營收衝到 20 億美元](https://aifundingtracker.com/cursor-revenue-valuation/)，兩百萬使用者、一百萬付費客戶，但毛利率**接近零**——幾乎每一塊錢進來都再付給 Anthropic 或 OpenAI。這讓它被迫在 2025 年 6 月改定價、2025 年 7 月為此公開道歉。Cursor 的位置是所有 AI SaaS 應用的縮影：**你可以做得很大，但做不出毛利，除非你自己是模型公司。**

**我自己的看法（用矽谷浪人的調性講）：** 我其實不覺得這件事是壞消息。從 2023 年到 2025 年，我們都活在一個幻覺裡——10 美元無限 Opus、200 美元 Claude Max 當 Agent 奴隸 24 小時跑、Cursor Pro $20 燒 Frontier 模型像喝水。那不是科技突破，那是金融工程。而且是次級金融工程——有人在前端說「AI 會改變世界」，後端在貼錢維持體驗，中間夾著一堆 VC 盼著 IPO 退場。現在帳攤開了，開發者至少看得到真實價格了。這是誠實，不是災難。要說有災難，是接下來那些已經把補貼價格內建進商業計劃書的 B 輪 C 輪 AI 公司。

---

## 產業衝擊

把這件事的漣漪拆成四層來看。

**第一層：直接受影響的人。** 最先被打到的是**個人開發者和學生**。印度、東南亞、拉丁美洲的獨立開發者，10 美元 Copilot Pro 本來是他們進 AI 編程賽道的門票；現在這個方案拿掉了 Opus，只能用 GPT-5.4 Mini 那一級輕量模型。重度用戶——也就是 Zitron 形容「一次請求燒掉整個月訂閱費」的那批——會被動轉到 token-based 計費。我大膽預測：**至少 20% 的個人訂閱者會在 4 月底退訂。**GitHub 主動在公告裡寫明可以退費，本身就是在預期這件事。學生受衝擊最明顯：免費的 Student 方案也停了新註冊，這代表**下一屆 CS 畢業生學寫程式的起跑線，從「有 AI 助手」退回「沒有」。**

**第二層：商業模式衝擊。** Flat-rate AI SaaS 基本上死了。接下來的 AI 產品會朝兩個方向走：**（1）成本透傳 + 固定加成**，像 AWS 那種「我收 20% margin，token 真實成本直接過給你」；**（2）座位費 + 使用量**，像 Anthropic 的新企業方案那樣把平台存取和消耗分開計算。無論哪個，傳統 SaaS 那套「高毛利、低邊際成本、規模化打死一切」的劇本結束了——AI 每多一個使用者就是一筆真實的 GPU 成本，邊際成本不趨近零。SaaS 估值模型要重寫。我預期未來半年會看到**一輪 AI SaaS 的下修**，尤其那些毛利被披露接近零的公司。

**第三層：開發者生態的重塑。** 這是最有意思的一層。因為當官方工具變貴，**BYOK（Bring Your Own Key）工具會大爆發**。Continue.dev、Tabby、Kilo Code 這類開源 IDE 插件開始被認真對待，因為它們讓你自己接模型——Claude、Gemini、DeepSeek、本地 Qwen 都可以。更有意思的是**本地 LLM 的回潮**：[各種評測已經顯示](https://localaimaster.com/blog/best-local-ai-models-programming) DeepSeek Coder 33B 和 Qwen 2.5 Coder 32B 在一張 RTX 4090 上跑可以達到 GPT-4o 級別的 coding 表現。一年前這件事是 hobbyist 在玩的；當 Opus 的 multiplier 被調到 7.5 倍時，這件事會變成 serious developer 的認真選項。接下來你會聽到更多「我把 Copilot 退了，自己架 Continue + Qwen」的故事。

**第四層：二階效應。** 幾個比較遠、但推得出來的影響——

- **Prompt cache 會變成一種新技能**。過去開發者不用管這個，反正是平台吃成本。現在成本透傳給你，cache hit rate 就是你的錢包。這會變成 AI 編程圈的新性能指標。
- **小規模實驗空間萎縮**。過去你可以亂試 prompt、亂試 refactor、亂跑 agent，試錯成本被補貼掉了。接下來每一次試錯都會反映在月底帳單上。這會改變工程師的 AI 使用習慣——**從「總是開著」變成「精準開啟」**。
- **高年資 vs 初階工程師的分化加劇**。公司會把有限的 AI 預算優先分給能把預算用在刀口上的資深工程師。初階工程師最依賴 AI 補完經驗的那段，反而可能被切掉補給線。這個諷刺非常殘酷。
- **NVIDIA 繼續躺贏**。所有這些都是在說「算力供給不足」。算力不足 → GPU 需求維持 → NVIDIA 的印鈔機繼續轉。

---

## 未來展望

**短期（未來 3–6 個月），幾乎確定會發生：**

所有主流 AI 編程工具會在 Q3 前全面轉向 token-based 或混合計費。**Cursor、Windsurf、Replit 這批都會跟進**——他們沒得選，因為上游 Anthropic 和 OpenAI 自己都在收緊。更多「服務品質保護」的節流會出現，形式可能是鎖峰時段、壓 context window、或把某些模型限定給高方案。會有**第二輪、第三輪 Copilot 式的暫停註冊**，只是換別家公司名字。個人開發者的儀表板上，「token budget」會取代「API calls」變成日常關注指標。

**中期（6–18 個月），三種可能的劇本：**

- **劇本一：效率戰勝成本。** 小模型進步速度超過推理需求，2026 年底我們看到在某類工作上 GPT-5 Mini 等級的模型以十分之一價格取代 Opus。這個劇本最樂觀，但需要模型端真的大幅突破。
- **劇本二：企業專屬化。** AI 編程工具的個人訂閱慢慢枯萎，主戰場完全搬到企業方案——有採購預算、有用量監控、有合規需求的地方才養得起。個人開發者被推向免費 tier 或自架本地模型。
- **劇本三：開源接盤長尾。** DeepSeek、Qwen、Llama 這類開源模型疊加 BYOK 工具，吃掉個人開發者和 SMB 市場；商用閉源模型上收到大企業。這會是一個類似 Linux/Windows 分化的市場結構。

我個人押劇本二和劇本三的混合。

**長期（3–5 年）的推演：**

AI 會從「訂閱服務」變成「基礎建設」——像電、像雲端、像自來水。價格透明、用量可度量、有 SLA、有預算週期。那時候「每個月多少錢」這個問題會被「每個 feature 多少 token」取代。誰能把 token 單位成本壓到最低，誰贏；誰能做出最好的「用最少 token 做最多事」的 agent 設計模式，誰也贏。這個階段**邊緣 / 本地運算可能會復興**——當雲端推理成本太貴，把部分推理拉回 M4 Mac、RTX 5090、本地 NPU 就變得合理。AI 不會完全回到本地，但重度使用者會往混合架構走。

**給讀者的行動建議：**

- **如果你是開發者：** 現在就學會監控你的 token 用量。試試 Continue.dev + DeepSeek Coder 的本地或混合組合。把 prompt cache 和 context 壓縮當成一項新技能。如果你在用 Copilot Pro，認真考慮是不是要升級、退訂、或轉 BYOK。
- **如果你是創業者或產品經理：** 把你的單位經濟學重新算一次，**算兩版——補貼價版和真實成本版**。如果真實成本版不成立，你要問自己一個尷尬問題：當上游收斂到 API 標準價，你還剩什麼。盡快把定價模型轉成「成本透傳 + 使用量」，不要等你被迫在 PR 災難中改。
- **如果你是一般科技從業者：** 你即將看到「AI 預算」變成你公司帳本上的一個具體科目。學著把它當差旅費或雲端費用來看。理解「每次 Claude 對話大概燒多少錢」會變成和「每趟飛機票多少錢」一樣需要認知的常識。

補貼期的那兩年，我們以為 AI 很便宜，甚至以為它快要免費。現在帳單攤開在桌上，一個更誠實、但也更不浪漫的 AI 時代開始了。**這才是真正的實驗：當它不是送的，它值多少？**

---

## 延伸閱讀

- [Exclusive: Microsoft To Shift GitHub Copilot Users To Token-Based Billing — Where's Your Ed At](https://www.wheresyoured.at/news-microsoft-to-shift-github-copilot-users-to-token-based-billing-reduce-rate-limits-2/)：Ed Zitron 拿到內部文件的原始獨家報導，整個討論的起點。
- [Changes to GitHub Copilot plans for individuals — GitHub Blog](https://github.blog/changelog/2026-04-20-changes-to-github-copilot-plans-for-individuals/)：GitHub 自己的官方公告，看他們怎麼講這件事。
- [Microsoft's GitHub suspends Copilot account sign-ups — The Register](https://www.theregister.com/2026/04/20/microsofts_github_grounds_copilot_account/)：補了 Joe Binder 訪談和產業橫向對比。
- [Anthropic shifts enterprise billing to per-token pricing — Implicator.ai](https://www.implicator.ai/anthropic-shifts-enterprise-billing-to-per-token-pricing-the-flat-fee-era-is-over/)：把 Anthropic 已走過的路整理清楚，包含算力供需的宏觀數字。
- [The Subprime AI Crisis Is Here — Ed Zitron](https://www.wheresyoured.at/the-subprime-ai-crisis-is-here/)：補貼式 AI 與 2008 次貸的類比，理論框架最完整。
- [Claude Opus 4.7 lands in GitHub Copilot at 7.5x premium request rate — allthings.how](https://allthings.how/claude-opus-4-7-lands-in-github-copilot-at-a-7-5x-premium-request-rate/)：詳細算了 multiplier 對實際用量的影響，開發者怒氣的起點。
- [AI demand is inflated, and only Anthropic is being realistic — CNBC](https://www.cnbc.com/2026/04/17/ai-tokens-anthropic-openai-nvidia.html)：從股市分析師角度解讀產業為何被迫轉向按量計費。
- [Cursor Revenue: How the $29B AI Coding Tool Makes Money — AI Funding Tracker](https://aifundingtracker.com/cursor-revenue-valuation/)：Cursor 的單位經濟學是所有 AI SaaS 的一面照妖鏡。
- [Best Local AI for Coding 2026 — Local AI Master](https://localaimaster.com/blog/best-local-ai-models-programming)：當補貼結束時，本地 LLM 的認真選項有哪些，適合想脫離訂閱地獄的開發者。
