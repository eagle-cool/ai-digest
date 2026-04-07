---
title: "當 AI Agent 把訂閱制撐爆：一場正在改寫軟體經濟學的定價危機"
date: 2026-04-07
description: "Anthropic 封殺 OpenClaw、SaaS 市值蒸發 2,850 億美元、OpenAI 承認定價是「意外」——當 AI Agent 真的 7×24 小時工作，按人類使用習慣設計的訂閱制正在從根基崩塌。這不只是一次規則調整，而是軟體產業三十年商業模式的結構性危機。"
tags: [deep-dive, agents, ai-industry, ai-tools, ai-coding]
---

## 引言

想像一個場景：你付了每月 200 美元的 Claude Max 訂閱，然後把它接上一個 AI Agent 框架，讓它 24 小時不間斷地幫你工作——瀏覽網頁、管理行事曆、回覆訊息、寫程式碼。你睡覺的時候它在跑，你開會的時候它在跑，週末你出去玩的時候它還是在跑。

你沒有違規。你只是把 AI 真的當成了一個員工。

然後在 2026 年 4 月 4 日，Anthropic 突然告訴你：不好意思，你不能再這樣用了。

這就是 Anthropic 封殺 OpenClaw 事件的核心。表面上看，這是一家公司調整了一條使用政策。往深裡看，這是 AI 產業第一次公開承認一個殘酷的事實——**那套按人類正常使用強度設計出來的訂閱制，根本扛不住 Agent。**

大家喊了兩年的「讓 AI 替人工作」，真有人這麼幹了，結果第一個受不了的不是被取代的人類，而是賣 AI 的平台自己。

這篇報導的起點是[〈AI的訂閱制，被Agent用崩了〉](https://www.36kr.com/p/3756224204816896)，但故事遠不止於此。從 OpenClaw 的 13.5 萬個實例，到 SaaS 產業 2,850 億美元市值蒸發，再到 OpenAI 承認自家定價是「意外」——我們正在見證軟體產業三十年來最大的商業模式危機。

---

## 事件全貌

### OpenClaw：一個「太會用」的工具

故事要從一個奧地利開發者 Peter Steinberger 說起。2025 年 11 月，他以「Clawdbot」為名發布了一個開源專案，讓使用者可以透過 WhatsApp、Telegram 等通訊軟體，把 Claude 變成一個持續運作的私人 AI 助理。三天之內改名為 OpenClaw，接著在 GitHub 上一路狂飆——[不到 48 小時就衝破 10 萬顆星](https://thenextweb.com/news/anthropic-openclaw-claude-subscription-ban-cost)，到 2026 年 3 月已經累積 24.7 萬顆星和 4.77 萬個 fork。

OpenClaw 做的事情其實很直覺：它不是幫你多問幾個問題，而是替你養一個永遠不下班的 AI 員工。這個員工自己接任務、自己拆解、自己調用模型、做完一輪再接著跑下一輪。

問題在於，這種使用方式和 Anthropic 設計訂閱制時的假設完全相反。

### 帳算不攏了

Claude Max 訂閱每月 200 美元。但一個全天候運作的 OpenClaw 實例，[每天消耗的 API 等值成本在 1,000 到 5,000 美元之間](https://thenextweb.com/news/anthropic-openclaw-claude-subscription-ban-cost)，取決於任務負載。也就是說，一個月 200 美元的訂閱，可能在一天之內就燒掉了遠超這個數字的算力。

更要命的是規模。Anthropic 宣布限制時，[市場上估計有超過 13.5 萬個 OpenClaw 實例在運行](https://thenextweb.com/news/anthropic-openclaw-claude-subscription-ban-cost)，其中約 60% 是用訂閱額度在跑。業界分析師估算，重度 Agent 用戶在訂閱制下的實際支出，與同等 API 使用量的費用之間，存在超過[五倍的差距](https://thenextweb.com/news/anthropic-openclaw-claude-subscription-ban-cost)。

小米 MiMo 大模型負責人羅福莉在 X 上點出了一個關鍵的技術細節：OpenClaw 這類框架的上下文管理效率很差，一個查詢往往會被拆成多輪低價值調用，而且每次都帶著很長的上下文。Anthropic 的 Claude Code 等第一方工具會最大化 prompt cache 命中率來大幅降低運算成本，但第三方框架經常完全繞過這層優化，意味著每次模型調用都是全額成本。

Claude Code 負責人 Boris Cherny 的聲明很直白：**「Anthropic 的訂閱制不是為這些第三方工具的使用模式設計的。算力是我們審慎管理的資源。」**

### 時機的微妙

讓這件事更加耐人尋味的是時間線。2026 年 2 月 14 日，Peter Steinberger 宣布離開自己創建的專案，加入 OpenAI。Sam Altman 公開表示 Steinberger 將「推動下一代個人 Agent」的開發，OpenClaw 也將移交給一個由 OpenAI 支持的開源基金會。

Anthropic 的限制措施在幾週後就生效了。

這到底是純粹的成本管控，還是夾帶了競爭策略？答案可能兩者都是。

---

## 脈絡

### 訂閱制的隱藏假設

SaaS 訂閱制能夠運作三十年，靠的不是什麼精密的商業邏輯，而是一個從未被明說的前提：**使用者是人。**

人會累，會分心，會把電腦關掉去吃飯。一個月付 20 美元的用戶，實際消耗的運算資源往往遠低於這個數字。平台收的是固定費用，付出的是一個平均成本——只要大部分用戶的真實消耗低於訂閱費，這門生意就能轉下去。

這個模式在人類使用者的世界裡運行了幾十年，從 Office 365 到 Netflix，從 Salesforce 到 Notion。每家公司都知道有些人訂了不用（平台最愛的客戶），有些人用得比較多，但平均下來，經濟模型是成立的。

直到 Agent 出現。

### SaaSpocalypse：2,850 億美元的驚醒

2026 年 2 月 3 日，Anthropic 發布 Claude Cowork——一個展示 AI Agent 能夠執行持續性、自主性知識工作的產品，不只是回答問題，而是端到端完成多步驟商業流程。

華爾街的反應是史無前例的恐慌。

接下來 48 小時內，[全球軟體和數據類股蒸發了約 2,850 億美元市值](https://cashandcache.substack.com/p/the-saas-death-spiral-how-ai-agents)，這是 SaaS 歷史上最大的單次 AI 觸發的重新定價事件，媒體稱之為「SaaSpocalypse」。投資人的邏輯很直接：如果 AI Agent 可以做 10 個人的工作，為什麼企業還要買 10 個座位的授權？

具體數字觸目驚心。Atlassian [股價下跌 36%](https://cashandcache.substack.com/p/the-saas-death-spiral-how-ai-agents)，並且報告了公司歷史上首次企業座位數量下滑——對一家整個營收模式建立在座位擴張上的公司而言，這是地震級的訊號。Salesforce [年初至今股價暴跌 31.3%](https://markets.financialcontent.com/stocks/article/marketminute-2026-2-18-the-death-of-the-seat-how-ai-agents-triggered-the-2026-saaspocalypse-for-salesforce-and-adobe)，投資人擔心自主 Agent 將完全繞過 Salesforce 的使用介面。Monday.com 的 CEO 更是直接宣布[用 AI Agent 取代了 100 名銷售開發代表](https://cashandcache.substack.com/p/the-saas-death-spiral-how-ai-agents)。

到 2026 年 3 月，[公開市場的 B2B 軟體股已經壓縮了 25%](https://cashandcache.substack.com/p/the-saas-death-spiral-how-ai-agents)，是自 2022 年利率升息以來最劇烈的修正。估值倍數從 6-10 倍 ARR 跌到 3-5 倍。SaaS 歷史上第一次，軟體股的交易估值低於 S&P 500。

### 推論成本的悖論

與此同時，一個看似矛盾的事實正在發生：AI 推論的單位成本在暴跌。

2022 年底，運行一個 GPT-4 等級模型的成本大約是每百萬 token 20 美元。到 2026 年初，等效性能的成本[降到了每百萬 token 0.40 美元](https://www.gpunex.com/blog/ai-inference-economics-2026/)——1,000 倍的下降。這個降幅比微處理器革命時期的 PC 運算成本下降還快，比 dotcom 時期的頻寬成本下降還快。

但諷刺的是，企業的 AI 總帳單不降反升。因為企業從實驗性的聊天機器人轉向了生產級的 Agent 部署，而 [Agent 消耗 token 的方式是任何傳統預算模型都沒預料到的](https://oplexa.com/ai-inference-cost-crisis-2026/)。2026 年，AI 推論成本佔企業 AI 預算的 85%。

單價暴跌，總帳暴漲——這就是 Agent 時代的經濟悖論。

---

## 多方觀點

### Anthropic：先止血再說

Anthropic 的立場很明確：這是生存問題，不是態度問題。Boris Cherny 的聲明雖然措辭客氣，但訊息很直白——算力是有限資源，必須優先保障自家產品和 API 客戶。

從商業角度看，這個決定完全合理。如果不限制，這種玩法只會被迅速複製。今天是 OpenClaw，明天就會有十個類似的框架，後天每個 Max 訂閱用戶都會想辦法掛一個 Agent 在後台跑。到那時候，Anthropic 面對的就不是一群偶爾上來聊幾句的訂閱用戶，而是一批掛著「個人會員」名義的小型算力工廠。

### 開發者社群：割裂的反應

OpenClaw 創始人 Peter Steinberger 的回應帶著明顯的火藥味：[**「他們先把一些熱門功能複製到自己的封閉框架裡，然後再把開源鎖在門外。」**](https://thenextweb.com/news/anthropic-openclaw-claude-subscription-ban-cost)

Ruby on Rails 創始人 DHH 稱這是「非常敵視客戶的做法」。George Hotz 撰文〈Anthropic 正在犯一個巨大的錯誤〉，認為這些限制[「不會把人拉回 Claude Code，只會把人推向其他模型供應商」](https://thenextweb.com/news/anthropic-openclaw-claude-subscription-ban-cost)。The Pragmatic Engineer 作者 Gergely Orosz 則下了一個更直接的結論：Anthropic「對 Claude 周圍幾乎沒有生態系統這件事感到很開心」。

但也有比較務實的聲音。開發者 Artem K 指出，這次處理方式[「已經是最溫和的了」](https://thenextweb.com/news/anthropic-openclaw-claude-subscription-ban-cost)——只是一封禮貌的通知，而不是直接封號或追溯收取 API 費用。

GitHub 上超過 147 則回應、Hacker News 上超過 245 分的討論，社群反應快速且兩極：有人已經取消訂閱以示抗議，有人則承認 Anthropic 其實別無選擇。

### OpenAI：我們也扛不住

Anthropic 不是唯一面對這個問題的公司。OpenAI CEO Sam Altman 在 2026 年 3 月公開承認，ChatGPT 目前的定價模式是[「意外形成的」](https://winbuzzer.com/2026/03/18/openai-rethinks-chatgpt-pricing-accidental-model-xcxwbn/)，暗示這不是一個深思熟慮的商業策略，而是產品演化過程中的偶然產物。OpenAI 已經在程式碼中出現了一個 100 美元/月的「Pro Lite」方案，[無限制存取正在被重新審視](https://winbuzzer.com/2026/03/18/openai-rethinks-chatgpt-pricing-accidental-model-xcxwbn/)。

當兩家頂尖 AI 公司幾乎同時承認自家定價有結構性問題，這就不是個案了——這是產業級的訊號。

### 中國市場：低價策略的另一面

拉回亞洲看，中國的大模型廠商走的是截然不同的路線。Qwen3.5 的 API 定價約為每百萬 token 0.20 美元，[是 Claude 的二十五分之一](https://ai-coding.wiselychen.com/china-ai-models-2026-lunar-new-year-comparison/)。大多數中國開源模型採用 Apache 2.0 或 MIT 協議，允許高度客製化和商業使用。

這種策略短期內確實能搶佔市場，但也面臨同樣的結構性問題——價格壓得越低、接口越開放，Agent 帶來的邊際成本問題就越尖銳。如果第三方框架的效率很差、上下文浪費嚴重、任務拆解粗糙，平台表面上在做增長，背後可能是在替低品質消耗買單。

### 我的看法

我覺得 Anthropic 這次的決定是對的，但方式可以更好。

封殺 OpenClaw 在商業邏輯上無可指摘——你不能讓 13.5 萬個算力黑洞掛在 200 美元/月的訂閱上持續失血。但把它和 OpenClaw 創始人跳槽到 OpenAI 的時間點放在一起看，很難不讓人覺得這裡面有競爭策略的成分。

更關鍵的是，這件事暴露出一個整個產業都在迴避的根本問題：**AI 公司一邊在推銷「AI 即員工」的願景，一邊卻在用「AI 即工具」的定價模式收費。** 當用戶真的把 AI 當員工來用，平台反而受不了了——這不是用戶的問題，是定價模式的問題。

---

## 產業衝擊

### 第一層：SaaS 公司的生存危機

最直接的受害者是所有靠 per-seat 收費的軟體公司。Publicis Sapient 報告[傳統 SaaS 授權被削減了約 50%](https://cashandcache.substack.com/p/the-saas-death-spiral-how-ai-agents)，替代方案是 AI 工具和內部 chatbot。這不是個別案例——當一個 Agent 可以做十個人的工作，企業不會傻到繼續買十個座位。

Salesforce 正在用 Agentforce 奮力轉型，號稱已經[完成 29,000 筆交易、達到 8 億美元 ARR](https://cashandcache.substack.com/p/the-saas-death-spiral-how-ai-agents)。但投資人的疑慮很明確：如果自主 Agent 可以直接存取 CRM 資料、執行銷售流程，誰還需要登入 Salesforce 的介面？

[McKinsey 2025 年 9 月的分析](https://www.chargebee.com/blog/pricing-ai-agents-playbook/)顯示，150 家全球軟體供應商中，68% 仍然依賴固定費用計價模式，只有 2% 成功轉型到 outcome-based 定價。這意味著絕大多數公司還在舊的經濟邏輯上運作，等到 Agent 真的全面滲透，衝擊會更加劇烈。

### 第二層：新定價模式的崛起

在舊模式崩塌的廢墟上，新的定價邏輯正在冒出來。

最具代表性的案例是 Intercom 的 Fin AI Agent。它採用 outcome-based 定價——[每次成功解決客戶問題收費 0.99 美元](https://www.chargebee.com/blog/pricing-ai-agents-playbook/)，如果 AI 解決失敗，客戶不用付錢。這個模式聽起來簡單，效果卻驚人：Fin 現在每週解決超過 100 萬個客戶問題，[從 100 萬美元成長到超過 1 億美元 ARR](https://gtmnow.com/how-intercom-built-the-highest-performing-ai-agent-on-the-market-using-outcome-based-pricing-with-archana-agrawal-president-at-intercom/)，甚至提供最高 100 萬美元的績效保證。

Replit Agent 則是按動作計費，[一個複雜的情境任務大約收費 1 美元](https://www.chargebee.com/blog/pricing-ai-agents-playbook/)。Cursor 從「不限量」轉向混合模式：基礎訂閱 + 進階模型使用量限制。Relevance AI 採用固定費用 + 包含額度 + 超額計費的三層結構。

這些新模式的共同點是：**不再假設使用者是人**，而是直接量化 AI 實際完成的工作來計費。

### 第三層：開發者生態的重新洗牌

對開發者而言，這場定價危機的影響比想像中更深遠。

首先是工具鏈的碎片化。過去你可以用一個訂閱搞定大部分 AI 需求，現在你必須精算每個 Agent 框架的 token 消耗效率、prompt cache 命中率、上下文管理策略。寫 Agent 不再只是寫邏輯，還要寫成本控制。

其次是「便宜的推論，昂貴的 Agent」悖論。單位 token 成本在暴跌，但 Agent 的多步驟、多輪次、帶長上下文的調用模式，讓實際帳單遠高於直覺預期。一個看似簡單的「改一個按鈕顏色」的請求，在 Replit Agent 上[因為需要重新處理所有先前聊天上下文而產生了約 1 美元的成本](https://www.chargebee.com/blog/pricing-ai-agents-playbook/)。

最後是平台鎖定風險的升級。Anthropic 這次的行動清楚表明，在第一方工具和第三方框架之間，平台會優先保護自家生態。這讓建構在任何單一模型供應商上的 Agent 框架都面臨隨時被切斷的風險。

### 第四層：二階效應

連鎖反應已經開始。CFO 們正在重新審視整個 AI 預算結構。過去 per-seat 定價讓財務團隊可以[精確預測成本](https://www.pymnts.com/artificial-intelligence-2/2026/cfos-scramble-as-ai-pricing-breaks-traditional-saas-billing-model/)，現在 AI 帳單更像動態的電費帳單，隨著實驗週期、模型重新訓練、自動化採用程度而劇烈波動。超過八成大型企業的 CFO [要嘛已經在使用 AI、要嘛正在考慮採用](https://www.pymnts.com/artificial-intelligence-2/2026/cfos-scramble-as-ai-pricing-breaks-traditional-saas-billing-model/)，但「財務可操作性」已經取代技術準備度，成為 AI 部署的最大門檻。

更長遠來看，這可能催生一個全新的中間層產業——專門做 Agent 成本優化、token 消耗監控、推論路由的工具和服務。就像雲端運算催生了 FinOps 一樣，Agent 時代可能催生「AgentOps」或「InferenceOps」。

---

## 未來展望

### 短期（3-6 個月）：混合定價成為主流

幾乎可以確定的是，所有主要 AI 供應商都會在 2026 年下半年推出某種形式的混合定價方案——基礎訂閱 + 使用量上限 + 超額計費。Anthropic 已經開始了（pay-as-you-go 的額外費用層），OpenAI 正在朝這個方向走。

「無限量」這個詞在 AI 訂閱方案中會逐漸消失，取而代之的是更精細的使用量分級和透明的超額費率。對用戶來說，這意味著 AI 訂閱的可預測性會下降，但定價會更誠實。

### 中期（6-18 個月）：三種路徑並行

**路徑一：Outcome-based 定價崛起。** Intercom 已經證明這條路走得通。當越來越多的 AI Agent 能夠交付可衡量的成果（解決客服問題、完成程式碼審查、產生銷售線索），按結果收費會變得更有吸引力。但這要求 AI 的能力足夠可靠，而且「成功」的定義足夠清晰。

**路徑二：Agent marketplace 平台化。** Anthropic 在 2026 年 3 月推出了 Claude Marketplace，零抽成的分發平台。如果這個模式成功，AI 公司可能從「賣算力」轉型為「賣平台」——讓第三方 Agent 在自家基礎設施上跑，但從流量、數據、附加服務中獲利。

**路徑三：開源模型分流需求。** 中國的低價策略和開源模型的持續改進，會讓一部分 Agent 工作負載從商業 API 轉向自建基礎設施。[a16z 的研究](https://www.chargebee.com/blog/pricing-ai-agents-playbook/)顯示 LLM 推論成本每年下降約 10 倍，這意味著自建的可行性會越來越高。

### 長期推演：3-5 年後的世界

如果這個趨勢持續下去，我們可能會看到 AI 服務的定價邏輯從根本上被重新發明。不再是「你用了多少」而是「你完成了什麼」。不再是按人頭算，而是按 Agent 的工作產出算。

最終，**AI 服務的定價可能會更像雇用一個員工，而不是訂閱一個工具**——你為結果付費，而不是為存取權付費。

### 給不同角色的建議

**如果你是開發者：** 現在就開始關注 Agent 的 token 效率。學會測量和優化 prompt cache 命中率、上下文管理、任務拆解策略。這不是純技術問題，而是直接影響你的 Agent 能不能在商業上存活。不要把 Agent 建構在單一模型供應商上——這次 OpenClaw 事件就是最好的警示。

**如果你是創業者或產品經理：** 認真研究 Intercom 的 outcome-based 定價模式。不要一開始就用「無限量」來吸引用戶——這是定時炸彈。從第一天就建立透明的使用量追蹤和計費機制。

**如果你是一般科技從業者：** 理解這場定價危機背後的含義：AI 的真實成本比訂閱費暗示的要高得多。當你在評估 AI 工具時，不要只看月費，要算清楚你的實際使用模式在 pay-as-you-go 模型下會花多少錢。

---

有一個問題值得所有人在腦中反覆咀嚼：**當我們真的造出了能像員工一樣工作的 AI，我們準備好為它付員工等級的費用了嗎？** 訂閱制的崩壞告訴我們，享受 AI 勞動力的人和承擔 AI 算力成本的平台之間，那個巨大的落差，遲早要有人來填——要嘛是更高的價格，要嘛是更聰明的商業模式。而這場填補的過程，才剛剛開始。

---

## 延伸閱讀

- [Anthropic blocks OpenClaw from Claude subscriptions in cost crackdown — TNW](https://thenextweb.com/news/anthropic-openclaw-claude-subscription-ban-cost)：最完整的 OpenClaw 封殺事件報導，包含關鍵數據和開發者反應
- [The SaaS Death Spiral: How AI Agents Are Rewriting Software Economics — Cash & Cache](https://cashandcache.substack.com/p/the-saas-death-spiral-how-ai-agents)：深入分析 SaaSpocalypse 事件和 SaaS 商業模式的結構性危機
- [Selling Intelligence: The 2026 Playbook For Pricing AI Agents — Chargebee](https://www.chargebee.com/blog/pricing-ai-agents-playbook/)：AI Agent 定價模式的全面指南，附具體公司案例和決策框架
- [CFOs Scramble as AI Pricing Breaks Traditional SaaS Billing Model — PYMNTS](https://www.pymnts.com/artificial-intelligence-2/2026/cfos-scramble-as-ai-pricing-breaks-traditional-saas-billing-model/)：從 CFO 視角看 AI 定價對企業預算管理的衝擊
- [OpenAI Rethinks ChatGPT Pricing, Calls Current Model 'Accidental' — WinBuzzer](https://winbuzzer.com/2026/03/18/openai-rethinks-chatgpt-pricing-accidental-model-xcxwbn/)：OpenAI 承認定價問題的關鍵報導
- [AI Inference Economics: The 1,000× Cost Collapse Reshaping GPUs — GPUnex](https://www.gpunex.com/blog/ai-inference-economics-2026/)：AI 推論成本暴跌的數據分析和對硬體產業的影響
- [The Subscription Model Is Architecturally Broken for AI Agents — Medium](https://medium.com/@jonassaraivasantos/the-subscription-model-is-architecturally-broken-for-ai-agents-and-the-fix-is-already-here-8a430553ddb9)：從架構層面分析訂閱模式為何無法適應 Agent 使用模式
- [GTM 178: How Intercom Built the Highest-Performing AI Agent Using Outcome-Based Pricing — GTM Now](https://gtmnow.com/how-intercom-built-the-highest-performing-ai-agent-on-the-market-using-outcome-based-pricing-with-archana-agrawal-president-at-intercom/)：Intercom 的 outcome-based 定價成功案例深度訪談
