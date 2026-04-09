---
title: "Meta Muse Spark 重返戰場、Cursor 3 把 IDE 降級、HappyHorse 屠榜之謎"
date: 2026-04-09
description: "Meta 推出 Muse Spark 模型重返 AI 競賽，Cursor 3 以 Agent 控制台取代傳統 IDE，神秘視頻模型 HappyHorse 斷層碾壓 Seedance 2.0 登頂全球第一"
tags: [llm, agents, ai-tools, ai-industry, ai-coding]
---

今天的浪型很有意思——Meta 終於不再只靠 Llama 撐場面，Muse Spark 是 Zuckerberg 砸了幾十億重組 AI 團隊後的第一個成果。Cursor 直接把 IDE 降級成備用工具，Agent 控制台成了主介面，這對寫了幾十年程式的人來說衝擊不小。但最讓我好奇的，是一匹叫 HappyHorse 的馬從天而降屠了視頻 AI 榜單，到現在還沒人認領。

---

## 🌊 今日浪頭

### [Meta is reentering the AI race with a new model called Muse Spark](https://www.theverge.com/tech/908769/meta-muse-spark-ai-model-launch-rollout)

Meta Superintelligence Labs 終於交出了重組後的第一份答卷——Muse Spark。這是 Zuckerberg 去年因為 Llama 4 的慘敗而大刀闊斧改組 AI 部門之後，全新 Muse 系列的開山之作。目前已經在美國的 Meta AI app 和網站上線，接下來幾週會陸續推到 WhatsApp、Instagram、Facebook、Messenger 以及 Meta 的智慧眼鏡上。

我看了一下它的定位：跟 Google Gemini 的策略類似，Muse Spark 是「為 Meta 產品量身打造」的模型。支援多模態輸入（文字+圖片）、可以跑多個子 Agent 來處理查詢、還有「Instant」和「Thinking」兩種模式切換。Meta 特別強調了健康領域的應用——可以分析食物照片估算熱量、回答涉及圖表的健康問題，明顯是要跟 ChatGPT Health 和 Claude for Healthcare 搶市場。

**為什麼這道浪值得追：**
- Llama 4 的失敗讓 Meta 幾乎被踢出 AI 頂級玩家名單，Muse Spark 是他們證明自己還活著的關鍵一步
- 未來版本計劃開源，加上會整合 Instagram、Facebook、Threads 上的推薦內容——這是其他 AI 公司沒有的社交數據優勢
- Meta 手握全球最大的社交平台矩陣，如果 Muse 系列品質跟上來，分發優勢會非常可怕

### [Cursor 3 發布：IDE 不重要了，智能體控制台上位](https://www.36kr.com/p/3757888158384899)

Cursor 發了一個讓我看了兩遍才確認的產品——Cursor 3（代號 Glass），一個從零開始構建的 Agent 管理控制台，而傳統 IDE 被降級成「備選視圖」。原本放檔案樹的地方，現在是 prompt 輸入框。

這不是小打小鬧的 UI 改版。Cursor 的邏輯是：工程師未來的主要工作是「調度 Agent、審查輸出、決定發布哪些任務」，而不是一行行敲程式碼。所有本地和雲端 Agent 顯示在統一側邊欄，支援從手機、Slack、GitHub、Linear 啟動的會話。最殺手級的功能是 Cloud Handoff——可以把正在跑的 Agent 從本機丟到雲端繼續跑，筆電關了也不影響，回來再拉回本地。

**為什麼這道浪值得追：**
- Cursor 年營收剛突破 20 億美元，但 Claude Code 用一年多就衝到 25 億，逼得 Cursor 一個月連發三款產品
- 目前四大玩家的路線分歧很清楚：Anthropic 走終端派、OpenAI 走全平台派、Google 和 Cursor 走 IDE 內建 Agent 控制台派
- 自研模型 Composer 2 的 token 成本比 Claude/GPT 低很多，對跑幾十個並行 Agent 的團隊來說，這比 UI 偏好更重要
- 文章裡一句話說得到位：「軟體工程師的角色正在向應用層系統運維者融合」——這個趨勢已經不可逆了

### [斷層碾壓 Seedance 2.0：神秘「歡樂馬」空降榜首](https://www.36kr.com/p/3757999597257220)

在 OpenAI 停了 Sora、所有人以為 Seedance 2.0 要一統天下的時候，一個叫 HappyHorse-1.0 的匿名模型從天而降，在 Artificial Analysis 的 AI Video Arena 上直接登頂。

這個「斷層」到底有多誇張？HappyHorse 在文字生視頻的 Elo 積分飆到 1347，領先 Seedance 2.0 整整 74 分——而從第二名到第十九名的總分差加起來才 70 分。而且 Artificial Analysis 的排名全靠全球用戶盲測投票，不是跑分能刷的。我看了幾個測試案例：呼拉圈從腰滑到膝蓋再掉地上撿起來重試、貓盯著烤麵包機看自己的倒影然後伸爪拍——物理動態的連貫性確實猛。

目前主流猜測指向阿里淘天未來生活實驗室，由前快手 Kling 一號位張迪帶隊。有人已經翻出了 happyhorseai.net 的官網和定價頁面。按照匿名屠榜的慣例，官方通常會在一週內認領，我賭這幾天就會揭曉。

**為什麼這道浪值得追：**
- 視頻生成賽道的競爭已經進入白熱化，Sora 退場後 Seedance 2.0 才稱霸五天就被超越
- 如果真是從快手 Kling 團隊出來的人做的，說明中國的視頻 AI 人才密度已經高到溢出來了
- 這匹馬如果開放 API，會直接衝擊目前字節、阿里、快手三足鼎立的格局

---

## ⚡ 衝浪快報

- **[阿里 AI 急什麼？設技術委員會、通義升級事業部、李飛飛出任阿里雲 CTO](https://www.36kr.com/p/3758804323808007)** — 四十天內動作密度超過去年一年，ATH 事業群成立加上千億美元公開承諾，阿里這次是認真要 All in AI 了
- **[羅福莉再發聲：Agent 時代模型訂閱制涼了？](https://www.36kr.com/p/3758022815445765)** — 小米 MiMo 負責人直言「搞清楚 coding plan 怎麼定價不虧錢之前，不要盲目打價格戰」，Anthropic 切斷 Claude 訂閱對 OpenClaw 的支持就是活生生的教訓
- **[Google Deep Think 八語奧賽屠榜，自主攻克 4 大未解難題](https://www.36kr.com/p/3757764511269379)** — 一個 AI、一個大腦、八張不同語言的試卷全部高分交卷，從 IMO 金牌到區域賽全覆蓋，推理能力的演進曲線越來越陡
- **[GPT-6 要來了，但 AI 行業早不跟 OpenAI 玩了](https://www.36kr.com/p/3757661357916931)** — 代號 Spud 的 GPT-6 據傳性能暴漲 40%、200 萬 token 上下文，但同時 Sora 連 API 都要全面下線，OpenAI 在做取捨
- **[三星單季狂賺 2600 億：營業利潤同比暴增 755%](https://www.36kr.com/p/3757778983600649)** — HBM 需求把三星推上史上最強單季，一季度利潤直接超越 2025 全年，花旗預估今年年度利潤可能逼近 2060 億美元
- **[公有雲漲價，我們親歷的第一次 AI 通脹](https://www.36kr.com/p/3757997540672256)** — Google、AWS 帶頭漲，阿里雲、百度智能雲、騰訊雲跟進，免費 perk 時代結束了，token 成本正式成為企業 AI 支出的大頭
- **[英特爾加入馬斯克 Terafab 計劃，聯手一起造晶片](https://www.36kr.com/p/3758008667685637)** — Tesla、SpaceX、xAI 每年所需 AI 晶片呈幾何級增長，台積電產能不夠用，馬斯克決定自己建廠，英特爾正式入夥
- **[國內首個瀏覽器「龍蝦」QBotClaw 上線](https://www.36kr.com/p/3757747029672713)** — 騰訊雲出品，QQ 瀏覽器側邊欄安裝即用，相容 OpenClaw 技能，支援國內各大模型 API Key，免費用
- **[馬斯克死磕奧特曼：賠款全捐，但他必須離開 OpenAI 董事會](https://www.36kr.com/p/3757764134568710)** — 馬斯克修訂訴訟，宣布勝訴的話一分錢賠款都不要全捐給 OpenAI 非營利機構，唯一訴求就是把奧特曼趕走
- **[被 Anthropic 封殺之後，OpenClaw 如何反擊？](https://www.36kr.com/p/3757715237597698)** — 真實故事是 OpenClaw 過去五個月一步步把自己從依賴 Claude 的工具變成多模型平台，4 月 4 日的封殺只是一次公開驗證

---

## 🏄 深水區

- **[What should we take from Anthropic's (possibly) terrifying new report on Mythos?](https://garymarcus.substack.com/p/what-should-we-take-from-anthropics)** — Gary Marcus 對 Mythos 的冷靜拆解，不吃 hype 也不盲目恐慌，值得在一堆聳動標題中看一篇有邏輯的分析
- **[The day you get cut out of the economy](https://geohot.github.io//blog/jekyll/update/2026/04/08/the-day-you-get-cut-out.html)** — geohot 的最新文章，探討當 AI 模型越來越強，企業計算「怎麼用 AI 賺錢最有效率」的那天，普通人會被怎樣擠出經濟循環
- **[The vibes are off at OpenAI](https://www.theverge.com/ai-artificial-intelligence/908513/the-vibes-are-off-at-openai)** — The Verge 的深度分析：OpenAI 剛融了 1220 億美元估值 8520 億，但消費端被 ChatGPT 疲勞侵蝕、內部士氣低落，這個巨獸的故事遠沒有數字看起來那麼美
- **[Anthropic's Project Glasswing — restricting Claude Mythos to security researchers](https://simonwillison.net/2026/Apr/7/project-glasswing/#atom-everything)** — Simon Willison 對 Glasswing 限制發布策略的評析，認為這是負責任 AI 發展的必要之舉，觀點清晰值得一讀
