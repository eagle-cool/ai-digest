---
title: "百元 ChatGPT Pro 殺到、Agent 中間層全線潰敗"
date: 2026-04-10
description: "OpenAI 終於在 $20 和 $200 之間塞了個 $100 方案對標 Claude，Meta 砸 350 億美元找 CoreWeave 買算力，Anthropic Managed Agents 直接把一票 Agent 創業公司送進 ICU"
tags: [llm, agents, ai-industry, ai-tools]
---

今天 AI 圈的浪不是一道大的，而是三道連環浪同時拍過來——OpenAI 終於想通了定價策略、Meta 繼續用鈔票砸算力、Anthropic 則悄悄把刀遞到一堆 Agent 創業公司的脖子上。最讓我有感的是第三道：你辛苦搭了一年的 Agent 基礎設施，上游一個產品發布就全歸零，這遊戲真的太殘酷了。

---

## 🌊 今日浪頭

### [ChatGPT finally offers $100/month Pro plan](https://techcrunch.com/2026/04/09/chatgpt-pro-plan-100-month-codex/)

OpenAI 終於做了一件所有 power user 等了很久的事——在 $20 的 Plus 和 $200 的 Pro 之間，塞進一個 $100/月的 Pro 方案。說實話，之前那個定價跳躍真的很離譜，$20 不夠用、$200 又太貴，中間空了一大截，逼得一堆重度用戶去找替代方案。

這次 $100 Pro 的賣點很明確：Codex 用量是 Plus 的 5 倍。OpenAI 自己也毫不掩飾地說，這就是衝著 Anthropic 的 Claude $100/月方案來的。官方原話是「跟 Claude Code 比，Codex 每一塊錢能給你更多 coding capacity」——直球對決，連客套都省了。不過有個小坑要注意：到 5 月 31 日之前 $100 方案會有額外加量，所以如果你這個月試了覺得很爽，之後限額可能會縮回來。

另一個值得關注的數字：全球每週有超過 300 萬人在用 Codex，過去三個月用量翻了 5 倍，月增長超過 70%。AI coding 這條賽道的成長曲線，已經不是「有潛力」而是「正在爆發」。

**為什麼這道浪值得追：**
- $100 價格帶是 AI coding 訂閱的兵家必爭之地，OpenAI 補上這個缺口等於正式向 Anthropic 宣戰
- 原本 $200 方案門檻太高，$100 方案會把大量觀望的開發者拉進 Codex 生態
- 這也暗示 OpenAI 意識到 Claude Code 在開發者市場的威脅比想像中大

### [Meta 追加 210 億美元 AI 雲協議](https://www.36kr.com/p/3760285070213889)

Meta 又掏錢了。這次是跟 CoreWeave 追加 210 億美元的 AI 基礎設施協議，加上之前已經簽的 142 億，兩家的合作總額來到 350 億美元。合約期限從 2027 年跑到 2032 年——五年，350 億，光想就覺得數字大到不真實。

CoreWeave 的機房裡塞了幾十萬顆 Nvidia GPU，專門跑大型 AI 模型。明明 Meta 自己也在蓋資料中心——今年三月才說要花 100 億在德州蓋一座——但還是得找 CoreWeave 補算力。CEO Mike Intrator 講了一句很到位的話：「他們當然可以自己蓋，但品質上我們更好，所以他們還是來找我們。」

Meta 今年的資本支出預估在 1150 到 1350 億美元之間，幾乎是去年的兩倍。Muse Spark 剛發布，後面還有更大的模型要訓，算力需求只會越來越猛。這筆交易也幫 CoreWeave 分散客戶集中度——微軟去年佔他們營收 62%，未來單一客戶不會超過 35%。

**為什麼這道浪值得追：**
- 350 億美元的規模讓 CoreWeave 從「GPU 二房東」正式升級為 AI 基礎設施的核心玩家
- Meta 一邊自建資料中心一邊大量外購算力，說明 AI 算力需求的增長速度遠超自建能力
- 這也側面印證了 Muse Spark 只是開胃菜，Meta 在 AI 上的野心遠不止於此

### [Anthropic 親自下場，又一批 Agent 創業公司死掉了](https://www.36kr.com/p/3759441190597385)

這才是今天最讓我感慨的一條。Anthropic 發布 Claude Managed Agents，直接把 Agent 的運行層做成平台服務——容器、沙箱、安全執行、長任務運行、權限隔離，全包了，按小時付費。

翻譯成白話：以前你要做一個能上線的 Agent，得自己扛 6 到 12 個月的工程周期去搭基礎設施。現在 Anthropic 說不用了，用我的就好。一個原本要幾個月才能上線的 Agent，現在幾天就能投入生產。

這刀砍的是誰？文章列了三類即將陣亡的公司：第一是 API 中轉商（國內一堆靠「幫你連 Claude」活著的公司）、第二是通用 Agent 編排平台（StackAI、E2B、Dify.ai 這些）、第三是無差異化的編排框架（LangChain、CrewAI）。這些公司過去一年靠「幫開發者省工程」賺得盆滿缽滿，但現在這層價值被上游直接吃掉了。

但也不是所有 Agent 公司都會死——做垂直閉環的反而會活得更好。金融風控、醫療病例庫、工業 IoT，這些有專有數據和場景深度的公司，護城河在模型之外。

**為什麼這道浪值得追：**
- 這不只是 Anthropic 一家在幹，微軟 Foundry Agent Service 和 Google Vertex AI Agent Engine 也在做同樣的事
- AI 創業最殘酷的劇本又上演了：你不是輸給同行，而是輸給上游產品路線圖裡還沒點亮的那一格
- 對開發者來說反而是好消息——Agent 開發的門檻大幅降低，重點可以放在業務邏輯而不是基礎設施

---

## ⚡ 衝浪快報

- **[Trump-appointed judges refuse to block Trump blacklisting of Anthropic AI tech](https://arstechnica.com/tech-policy/2026/04/trump-appointed-judges-refuse-to-block-trump-blacklisting-of-anthropic-ai-tech/)** — 聯邦上訴法院拒絕暫停 Trump 政府對 Anthropic 的黑名單令，但同意加速審理，5 月 19 日口頭辯論。美國政府黑自家 AI 公司，這劇本真的很魔幻
- **[Is Anthropic limiting Mythos to protect the internet — or Anthropic?](https://techcrunch.com/2026/04/09/is-anthropic-limiting-the-release-of-mythos-to-protect-the-internet-or-anthropic/)** — TechCrunch 這篇角度很毒：Mythos 限制發布與其說是為了安全，不如說是防止中國公司蒸餾。三大實驗室已經聯手封殺蒸餾者
- **[Google and Intel deepen AI infrastructure partnership](https://techcrunch.com/2026/04/09/google-and-intel-deepen-ai-infrastructure-partnership/)** — Google 和 Intel 要聯合開發客製化晶片，全球 CPU 供應緊張的背景下這合作很有戰略意義
- **[Meta AI app climbs to No. 5 on the App Store](https://techcrunch.com/2026/04/09/meta-ai-app-climbs-to-no-5-on-the-app-store-after-muse-spark-launch/)** — Muse Spark 發布前 Meta AI 排 57 名，現在衝到第 5 名還在往上爬，模型品質上來之後分發優勢立刻體現
- **[DeepMind 創始人：AGI 或 5 年內實現](https://www.36kr.com/p/3759632158179840)** — Hassabis 說過去十五年支撐 AI 產業 90% 關鍵突破都出自 Google 系團隊，未來差距會越拉越大。自信是有了，就看能不能兌現
- **[Google Gemma 4 遭破解，有求必應](https://www.36kr.com/p/3759354864120324)** — 開源模型上線就被越獄，偽造支票、找盜版電影都行。安全護欄在開源世界的脆弱性再次暴露
- **[Florida AG announces investigation into OpenAI](https://techcrunch.com/2026/04/09/florida-ag-investigation-openai-chatgpt-shooting/)** — 佛州檢察總長調查 OpenAI，起因是去年 FSU 槍擊案嫌犯據報用 ChatGPT 策劃攻擊。受害者家屬計劃起訴
- **[狂攬 4 萬星，Hermes Agent 正在取代 OpenClaw](https://www.36kr.com/p/3759493153653253)** — Nous Research 的開源 Agent 從二月上線至今 GitHub 超過 4 萬星，平均不到一週一個大版本，240+ 貢獻者，社群說「記憶力屌打龍蝦」
- **[Token 消耗暴增千倍，雲廠商開始慌了](https://www.36kr.com/p/3759451924808452)** — 微軟 Azure 季度營收破 500 億還被拋售、AWS 最快增速股價反跌 11%，原因就一個字：AI 帳單失控了
- **[Claude Opus 4.6 差評如潮，思考深度暴跌 67%](https://www.36kr.com/p/3759493168513538)** — AMD 總監用 6852 次日誌數據打臉，Claude 輸出變淺、token 飆升、stop hook 頻繁觸發，Anthropic 始終沒正面回應

---

## 🏄 深水區

- **[普利策得主萬字起底奧特曼](https://www.36kr.com/p/3759247068398340)** — Ronan Farrow（就是扳倒 Weinstein 那位）在《紐約客》發了重磅調查，採訪 100 多人、翻出 Ilya 整理的數十頁 Slack 記錄，Anthropic CEO Dario 也受訪了。AI 圈今年最具破壞力的一顆深水炸彈
- **[The AI industry's race for profits is now existential](https://www.theverge.com/podcast/909042/ai-monetization-cliff-anthropic-openai-profitable-ai-existential-moment)** — The Verge 的 Decoder Podcast 深度探討 AI 產業的獲利懸崖：幾家最大的公司能不能在燒完錢之前變成真正賺錢的生意？數據和分析都很紮實
- **[AI Is Really Weird](https://www.wheresyoured.at/ai-is-really-weird/)** — Ed Zitron 的最新長文，5000 到 18000 字的深度拆解，涵蓋 Nvidia、Anthropic 等巨頭，觀點一如既往地犀利不留情面
- **[無需強化學習，蘋果團隊「簡單自蒸餾」實現 Coding 模型自進化](https://www.36kr.com/p/3759092647002633)** — Apple 提出 Simple Self-Distillation（SSD），不靠 RL、不靠教師模型，讓模型從自身採樣學習。Qwen3-30B 在 LiveCodeBench 上從 42.4% 提升到 55%，方法極簡但效果驚人
