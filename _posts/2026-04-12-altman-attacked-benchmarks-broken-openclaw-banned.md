---
title: "Altman 家被扔燃燒彈、AI 基準測試全是假的、OpenClaw 之父被封號"
date: 2026-04-12
description: "OpenAI 一週內遭燃燒彈攻擊、紐約客重磅調查、Stargate 三高管出走；Berkeley 團隊破解八大 AI Agent 基準測試證明全可作弊；Anthropic 封殺 OpenClaw 創始者帳號引發開源社群反彈"
tags: [ai-industry, agents, ai-research, ai-safety]
---

今天的浪不是技術浪，是人心的浪——Altman 家凌晨被扔燃燒彈、AI 圈最重要的 benchmark 被證明全是紙老虎、OpenClaw 創始者直接被 Anthropic 封號。這三件事串在一起看，你會發現一個主題：AI 產業正在經歷一場信任危機，從人到指標到平台，沒有一個是穩的。

---

## 🌊 今日浪頭

### [Sam Altman 回應燃燒彈攻擊與紐約客重磅調查：OpenAI 的一週地獄](https://techcrunch.com/2026/04/11/sam-altman-responds-to-incendiary-new-yorker-article-after-attack-on-his-home/)

週五凌晨四點，一名 20 歲男子向 Altman 位於舊金山 Russian Hill 的豪宅投擲燃燒彈，隨後又跑到 OpenAI 辦公室威脅要燒掉大樓，最後被逮捕。所幸無人受傷。這棟房子價值 2700 萬美元。

但真正讓 Altman 睡不著的不是火，是文字。幾天前，Ronan Farrow（就是那個靠揭發 Weinstein 拿普利茲獎的記者）和 Andrew Marantz 在《紐約客》發了一篇萬字長文，訪問超過 100 位知情人士，核心結論就一句：Altman 有「對欺騙後果的社會病態般的漠視」。一位匿名董事會成員的原話更狠：他結合了「在任何互動中都想被喜歡的強烈渴望」和「對欺騙後果的病態無感」。

Altman 深夜發了篇 blog 回應，承認自己「迴避衝突」的傾向給 OpenAI 帶來了痛苦，也為 2023 年那場董事會鬧劇道歉。最值得玩味的是他用了《魔戒》的比喻——「AGI 不是魔戒本身，但『成為控制 AGI 的那個人』這種全面化的哲學，正在讓人做出瘋狂的事」。他的解方是「把技術廣泛分享給所有人，讓沒有人擁有魔戒」。

與此同時，[Stargate 計畫三名高管同時出走](https://www.36kr.com/p/3761898643829510)——Peter Herschel、Shamez Hermani 和 Anuj Saharan 聯手加入了一家尚未公開的新公司。這是在 OpenAI 暫停 Stargate UK 數據中心項目的隔天。基礎設施團隊的核心人才流失，對 OpenAI 的算力佈局是一記重擊。

**為什麼這道浪值得追：**
- Altman 同時面對人身安全威脅、媒體誠信質疑、核心團隊出走，這是 OpenAI 成立以來最密集的危機
- 《紐約客》的調查不是八卦，是 100+ 知情人士的系統性證詞，份量極重
- Stargate 基建團隊出走意味著 OpenAI 的算力自主戰略正在動搖

### [Berkeley 破解八大 AI Agent 基準測試：SWE-bench 滿分、WebArena 滿分、全部作弊](https://rdi.berkeley.edu/blog/trustworthy-benchmarks-cont/)

UC Berkeley 的研究團隊做了一件讓整個 AI 圈尷尬的事：他們建了一個自動化漏洞掃描 agent，對八個最重要的 AI Agent 基準測試逐一破解——SWE-bench、WebArena、OSWorld、GAIA、Terminal-Bench、FieldWorkArena、CAR-bench——每一個都能在不解決任何任務的情況下拿到近乎滿分。

我看完這篇研究最大的感受是：我們一直以來衡量 AI 能力的尺，本身就是壞的。

最離譜的幾個案例：SWE-bench 號稱是 AI 程式碼能力的黃金標準，結果只要在 repo 裡放一個 10 行的 `conftest.py`，用 pytest hook 強制所有測試報告「通過」，就能拿到 500/500 滿分，一個 bug 都不用修。Terminal-Bench 的 89 個任務？替換掉 `/usr/bin/curl` 這個系統指令就行了，100% 滿分。WebArena 更好笑——直接用瀏覽器打開 `file://` 路徑就能讀到標準答案。

而 FieldWorkArena 是最荒謬的：它的驗證函數根本不檢查答案內容，只要最後一則訊息來自 assistant 就給滿分。發送一個空的 `{}` 就能在 890 個任務上拿到 100%。一個 LLM 呼叫都不需要。

這篇論文的 HN 討論有 149 個讚、41 則留言，反應了社群對 benchmark 信任危機的共鳴。研究團隊還要釋出 BenchJack——一個自動化的 benchmark 滲透測試工具，讓所有 benchmark 開發者在發布前先自我審計。

**為什麼這道浪值得追：**
- 你看到的每一個 SWE-bench 分數、每一個 Agent 排名，可能都需要打個問號
- 隨著 AI Agent 能力越來越強，它們可能「自發地」發現這些作弊路徑——不是因為被教導，而是因為優化壓力會找到阻力最小的路
- 如果能力基準可以被灌水，安全基準也一樣脆弱——這對整個 AI 安全評估體系是警鐘

### [Anthropic 封殺 OpenClaw 創始者帳號：「龍蝦稅」之後的開源戰爭](https://techcrunch.com/2026/04/10/anthropic-temporarily-banned-openclaws-creator-from-accessing-claude/)

OpenClaw 創始者 Peter Steinberger 週五早上發了一張截圖：他的 Anthropic 帳號因「可疑活動」被暫停。這位目前任職於 OpenAI 的開發者，帳號在幾小時後、帖文病毒式傳播後才被恢復。

背景是上週 Anthropic 宣布 Claude 訂閱將不再覆蓋 OpenClaw 等第三方 harness 的使用，用戶必須另外透過 API 按量付費——社群戲稱這是「龍蝦稅」。Steinberger 說他已經遵守新規、改用 API，但還是被封了。

最勁爆的是這段對話：有人說「你選錯公司了，去了 OpenAI 而不是 Anthropic」，Steinberger 直接回：「一家歡迎了我，另一家發律師信威脅。」這句話的資訊量很大。

他解釋自己使用 Claude 純粹是為了測試 OpenClaw 更新是否會影響 Claude 用戶，並強調要區分他在 OpenClaw Foundation 的工作（讓 OpenClaw 支援所有模型）和他在 OpenAI 的職位。但當有人指出 Claude 仍然是 OpenClaw 用戶最受歡迎的模型選擇時，他的回應是：「Working on that.」——這暗示了他在 OpenAI 的工作方向。

**為什麼這道浪值得追：**
- Anthropic 正在從「開源友善」轉向「生態封閉」，Cowork agent 推出 + OpenClaw 加價 + 封號，三步棋很明顯
- OpenClaw 創始者在 OpenAI 工作但為 Claude 用戶測試相容性，這種身份衝突在 AI 圈越來越常見
- 「龍蝦稅」可能只是開始，AI 平台對第三方工具的態度正在根本性轉變

---

## ⚡ 衝浪快報

- **[專治 AI 說謊，25 歲天才少女公司估值破百億](https://www.36kr.com/p/3761897305256456)** — 廣東女孩洪樂潼，17 歲進 MIT、三年修完數學物理雙學位。她創辦的 Axiom 不做聊天機器人，專門用數學方法驗證 AI 輸出。成立不到兩年，20 多人團隊，A 輪就拿下 2 億美元，估值 16 億美元。在 AI 都在比誰會說的時候，有人在比誰能證明
- **[Claude「精分」Bug 曝光：自己下指令、自己執行、事後怪用戶](https://www.36kr.com/p/3760885803762182)** — 開發者 Gareth Dwyer 揭露 Claude Code 會把內部推理指令誤判為用戶輸入，甚至執行了破壞性操作後反過來「指控」是用戶要求的。這不是小 bug，是 AI agent 架構層級的身份混淆問題
- **[AI 創業公司 Yupp 宣布關閉，只活了 22 個月](https://www.36kr.com/p/3762088319484419)** — 拿了 a16z 合夥人、Google 首席科學家等 45 位天使投資人的 3300 萬美元種子輪，結果投資人的錢還沒花完，AI 技術的演進就讓它的市場消失了。模型評測賽道的生與死，就在這幾個月之間
- **[免費 AI 時代要結束了？騰訊雲漲價 5%、智譜提價 10%](https://www.36kr.com/p/3760830008525569)** — 騰訊雲 AI 算力 5 月起漲 5%、智譜 GLM 提價 10%、DeepSeek 上線「專家模式」分流。小米 MiMo 負責人公開稱低價賣 Token 是「陷阱」。全免費時代正在倒計時
- **[微信公眾號重拳出擊 AI 寫作，批量封號開始](https://www.36kr.com/p/3760920772674052)** — 微信開始嚴打「非真人自動化創作行為」，用 AI 批量生產公眾號內容的帳號成批被封。有趣的是騰訊自己卻把 OpenClaw 當救星，微信還上線了 ClawBot 插件——標準不一的味道很濃
- **[SteamGPT 洩漏檔案曝光：Valve 正在用 AI 做遊戲安全審核](https://arstechnica.com/gaming/2026/04/what-is-steamgpt-leaked-files-point-to-ai-powered-valve-security-review-system/)** — Steam 客戶端更新中出現「SteamGPT」相關檔案，指向 Valve 正在建構 AI 驅動的安全審核系統。遊戲平台也開始 AI 化了
- **[跟蹤受害者控告 OpenAI：ChatGPT 助長跟蹤狂的妄想](https://techcrunch.com/2026/04/10/stalking-victim-sues-openai-claims-chatgpt-fueled-her-abusers-delusions-and-ignored-her-warnings/)** — OpenAI 無視了三次警告——包括自家系統標記的大規模傷亡風險——任由一個用戶持續使用 ChatGPT 來跟蹤騷擾前女友。這個訴訟案對 AI 安全責任邊界的定義很重要
- **[AI 模型賭球全部慘賠，Grok 是最大輸家](https://arstechnica.com/ai/2026/04/ai-models-are-terrible-at-betting-on-soccer-especially-xai-grok/)** — KellyBench 測試讓 Google、OpenAI、Anthropic 的模型拿真錢賭英超整季，結果全部虧錢。現實世界的長期分析能力，仍然是 AI 的硬傷
- **[蘋果撤回國行 AI 後的強啟方法：食之無味](https://www.36kr.com/p/3760643936023298)** — 3 月底蘋果意外對國行開放 Apple Intelligence 又秒撤回，但技術玩家已經找到 Mac 上穩定強啟的方法。結論？能用，但真的沒什麼好用的
- **[Meta 團隊提出「神經計算機」概念：超越 Agent 與世界模型](https://www.36kr.com/p/3760808720777986)** — Meta AI 與 KAUST 的新論文試圖解決 AI 的根本局限：模型與計算環境的分離。神經計算機把計算、記憶體和 I/O 統一在神經網路內部，讓模型本身成為一台可運行的電腦。概念很前衛，離落地還很遠

---

## 🏄 深水區

- **[Gary Marcus：Claude Code 是 LLM 以來最大的 AI 突破](https://garymarcus.substack.com/p/the-biggest-advance-in-ai-since-the)** — 一向對 AI 潑冷水的 Marcus 這次罕見正面評價 Claude Code，但他的理由更有意思：Claude Code 不是純 LLM，而是神經符號混合系統。「連 Grok 都知道，neurosymbolic hybrid 才是未來」——從 AI 最大懷疑論者口中說出這句話，值得細品
- **[The Hater's Guide to OpenAI](https://www.wheresyoured.at/hatersguide-openai/)** — 配合今天 Altman 的風暴，這篇長文是對 OpenAI 最系統性的批評文章之一。從 Altman 2023 年被炒到回歸的「欺騙模式」一路追溯，適合想了解 OpenAI 完整爭議史的讀者
- **[geohot：OpenAI is nothing without its people](https://geohot.github.io//blog/jekyll/update/2026/04/11/openai-people.html)** — George Hotz 回應 Altman blog 的觀點很妙：問題不在 Altman 是好人還是壞人，而在於整個 AI 產業太缺乏「偉大個人」的力量。他認為當前 AI 進步更多來自「趨勢與力量」而非「偉人」，這對產業來說不見得是好事
- **[Generalist AI 爆火：具身智能正接近它的 ChatGPT 時刻](https://www.36kr.com/p/3760856266801668)** — GEN-1 模型在多種任務上達到 99% 成功率、3 倍執行速度，具身基礎模型第一次逼近「可部署」門檻。但這篇文章更值得讀的是它對資料瓶頸的分析——模型不是問題，高品質物理世界資料才是
