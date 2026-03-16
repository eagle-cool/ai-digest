---
title: "AlphaEvolve 踏平十年數學紀錄、xAI 承認搭錯重頭來、Kimi 三個月估值翻四倍"
date: 2026-03-16
description: "Google DeepMind 的 AlphaEvolve 一口氣刷新五個拉姆齊數下界，馬斯克親口認錯要重建 xAI 並從 Cursor 挖角，月之暗面 Kimi 估值飆上 180 億美元創紀錄。"
tags: [llm, ai-research, ai-industry, ai-coding, agents]
---

今天的浪真的又大又雜——Google DeepMind 那邊直接讓 AI 自己寫算法去破數學難題，馬斯克這邊終於承認 xAI 從頭搭錯了，而中國這頭 Kimi 三個月融了三輪直接把估值拉到 180 億美元。最讓我震撼的其實是 AlphaEvolve，因為它做的事情已經不是「解題」而是「發明解題方法」了。

---

## 🌊 今日浪頭

### [Google DeepMind AlphaEvolve 一次刷新五個拉姆齊數下界，踏平十年數學紀錄](https://www.36kr.com/p/3724789441575555)

拉姆齊數有多難？數學家 Paul Erdős 說過，如果外星人要求人類算出 R(5,5) 否則毀滅地球，人類最理性的選擇大概是投降。而 DeepMind 的 AlphaEvolve 剛剛一口氣改進了五個經典拉姆齊數的下界——R(3,13)、R(3,18)、R(4,13)、R(4,14)、R(4,15)，其中最久的紀錄已經塵封 20 年。

重點不只是結果，而是方法。AlphaEvolve 不是在圖空間裡暴力搜索，而是用 Gemini 在「算法空間」裡做演化——它生成、變異、篩選搜索算法本身，最終為每個問題量身定制出一套搜索策略。論文中展示了四大算法家族，從暴力退火到代數結構播種到循環圖引導，風格迥異但全是 AI 自己摸索出來的。其中 R(4,10) 的策略，論文作者直言「在已有文獻中根本找不到先例」。

**為什麼這道浪值得追：**
- 這不是 AI 解題，是 AI 發明解題方法——元搜索（meta-search）的概念正式從理論走向實戰
- AlphaEvolve 此前已破 56 年矩陣乘法紀錄、優化 Google 資料中心排程，現在又攻下純數學
- Hassabis 說的飛輪效應正在成真：Gemini 寫算法 → 算法優化基礎設施 → 更強的 Gemini → 更好的算法

### [馬斯克親口承認 xAI 從一開始就搭錯了，急挖 Cursor 兩位核心高管反攻 AI Coding](https://www.36kr.com/p/3724759367383685)

「xAI 在一開始構建時，便並不正確。」——這句話出自馬斯克本人。xAI 創始團隊 12 人目前只剩 3 人，五位華人聯創全部離開，前 CFO 入職 102 天就跑去 OpenAI，離職感言提到「每週工作超過 120 小時」。Macrohard 專案負責人接手 16 天就走人，Grok Imagine 主管也跟著離開。

但馬斯克不是坐以待斃。他從 Cursor 挖來了兩位核心高管 Jason Ginsberg 和 Andrew Milich——這兩人之前共同創辦了 Skiff（被 Notion 收購），又一起把 Cursor 的年化營收推到 20 億美元。他們將直接向馬斯克彙報，目標很明確：AI Coding。馬斯克在 Abundance 大會上說，要確保年中之前在編程能力上全面超越競爭對手。

**為什麼這道浪值得追：**
- 承認失敗的時間點很微妙——就在說服 Tesla 董事會投了 20 億美元、SpaceX 以 2500 億估值收購 xAI 之後
- Claude Code 年化收入已超 25 億美元，OpenAI Codex 五個月增長 20 倍，xAI 在 AI Coding 賽道嚴重落後
- 從 Cursor 挖人釋放的信號是：xAI 可能從研究導向轉為產品工程導向，這對整個 AI Coding 競爭格局影響很大

### [Kimi 三個月三輪融資，估值從 43 億飆到 180 億美元，創中國大模型紀錄](https://www.36kr.com/p/3724849709906568)

月之暗面的融資速度讓人看傻了。去年底估值還是 43 億美元，一個月前 100 億，現在直接 180 億美元——三個月翻了四倍多。而支撐這個估值的不只是故事，是實打實的數據：K2.5 發布後，Stripe 支付訂單數環比增長 8280%，1 月底以來 20 天收入超過 2025 全年，海外收入已經超過國內。

以我的觀察，Kimi 能吃到這波紅利不是運氣。早在 2025 年 9 月他們就開始做 Agent 產品，當其他家還在卷 Chatbot 的時候，Kimi 已經在探索「讓 AI 替人幹活」。K2.5 的 Agent 集群能同時調度 100 個分身、並行處理 1500 個步驟。OpenClaw 爆發的時候，Kimi 是全球調用量最多的模型之一，Kimi Claw 衝上龍蝦榜全球 TOP2。

**為什麼這道浪值得追：**
- 港股上市的智譜、MiniMax 市值已在 340-450 億美元區間，Kimi 的 180 億反而顯得保守
- Agent 商業模式跑通意味著最殘酷的軍備競賽正式開始——所有人都在搶同一個未來
- 楊植麟的內部信目標：K3 模型等效算力提升至少一個數量級，營收實現數量級增長

---

## ⚡ 衝浪快報

- **[Anthropic Claude Code 年化收入超 25 億美元，OpenAI Codex 約 10 億——Agentic AI 時代 OpenAI 不再穩坐第一](https://www.36kr.com/p/3724781731543431)** — AI Coding 的王座悄悄換人了，Claude Code 的收入直接是 Codex 的 2.5 倍，Anthropic 當年從 OpenAI 出走的那批人正在打臉老東家
- **[Meta 傳裁員 20%、新模型「酪梨」延到五月，扎克伯格的 AI 牌越打越亂](https://www.36kr.com/p/3722443132056066)** — 新模型不夠好所以延期，成本太高所以裁人，但「為 AI 輔助型員工帶來的效率提升做準備」這個說法怎麼聽都像是在美化裁員
- **[NVIDIA GTC 前夕風向微變：Stargate 停滯、中東地緣風險衝擊資料中心建設](https://www.36kr.com/p/3723580265740677)** — 過去兩年 NVIDIA 一卡難求，現在算力需求的信號開始出現微妙變化，但別太早下結論——GTC 才要開幕
- **[315 晚會曝光 AI 大模型「投毒」亂象：GEO 優化讓虛假資訊成為 AI 標準答案](https://www.36kr.com/p/3724770946677121)** — 有人用 GEO 工具捏造假智慧手環，兩小時後 AI 就開始認真推薦這個根本不存在的產品，這比 SEO 作弊可怕多了
- **[OpenAI 開除員工：利用公司核心機密在 Polymarket 下注牟利](https://www.36kr.com/p/3723784474081925)** — 調查發現過去一年有 60 個神秘錢包做了 77 次精準到離譜的內幕押注，AI 公司的資訊安全問題不只是模型安全
- **[DeepSeek V4 與騰訊混元新模型四月交卷，梁文峰 vs 姚順雨正面對決](https://www.36kr.com/p/3723883117376256)** — 一個量化私募出身的初創、一個巨頭最高規格請回的學術派，四月的中國 AI 圈會很精彩
- **[BAT 集體搶灘 OpenClaw 生態：百度出紅手指 Operator、騰訊一口氣推五款龍蝦產品](https://www.36kr.com/p/3721249863973507)** — 龍蝦大戰已經從「技術展示」進入「平台卡位」階段，巨頭們的速度比想像中快得多
- **[ByteDance 暫停 Seedance 2.0 影片生成器全球發布](https://techcrunch.com/2026/03/15/bytedance-reportedly-pauses-global-launch-of-its-seedance-2-0-video-generator/)** — 工程師和律師正在合力避免更多法律問題，AI 影片生成的版權地雷越來越難閃
- **[25 歲 Axiom AI 創辦人洪樂潼完成 2 億美元 A 輪，估值 16 億美元](https://www.36kr.com/p/3722536093858434)** — 廣州出生、MIT + Oxford + Stanford 背景，Menlo Ventures 領投，年紀小但履歷和融資一樣猛
- **[AI 公司開始招即興表演演員來訓練 AI 的情緒表達能力](https://www.theverge.com/ai-artificial-intelligence/893931/ai-companies-handshake-improv-actors-training-data)** — 不是在劇場表演，而是為 AI 提供情緒訓練數據，演員的新職業路徑又多了一條
- **[Show HN: LLVM-Z80 — 用 AI 完整寫出一個 LLVM 後端](https://github.com/llvm-z80/llvm-z80)** — 兩年前用 AI 寫 LLVM 後端被認為不可能，現在一個人真的做到了，AI Coding 的天花板還在不斷被推高

---

## 🏄 深水區

- **[Gary Marcus: Expensive New Evidence That Scaling Is Not All You Need](https://garymarcus.substack.com/p/breaking-expensive-new-evidence-that)** — Scaling 假說的最大唱衰者又出手了，這次拿了兩位世界首富的昂貴實驗當證據，不管你同不同意他，這篇的論點值得認真想想
- **[Simon Willison 在 Pragmatic Summit 的 Agentic Engineering 爐邊談話](https://simonwillison.net/2026/Mar/14/pragmatic-summit/#atom-everything)** — Simon 是少數能把 AI Agent 的實際工程經驗講清楚的人，這場談話涵蓋了 AI 採用的各個階段，實戰派必看
- **[OpenAI 董事長 Bret Taylor 深度訪談：花店老闆不需要 AGI，但客服成本可以降 100 倍](https://www.36kr.com/p/3724789796043141)** — Sierra CEO 兼 OpenAI 董事長的 101 分鐘深度對談，系統闡述了對 AI Agent、企業軟體和未來交互方式的判斷，是少見的高密度內容
- **[The Appalling Stupidity of Spotify's AI DJ](https://www.charlespetzold.com/blog/2026/02/The-Appalling-Stupidity-of-Spotifys-AI-DJ.html)** — HN 上 167 個讚、136 則留言，Charles Petzold 把 Spotify AI DJ 的蠢拆解得淋漓盡致，如果你也覺得它很煩，這篇會讓你覺得不孤單
- **[Ask HN: How is AI-assisted coding going for you professionally?](https://news.ycombinator.com/item?id=47388646)** — 拋開「我們完蛋了」跟「AI 沒用」的兩極討論，這個 HN 帖想知道大家實際用 AI 寫程式的真實體驗，留言區很值得挖
