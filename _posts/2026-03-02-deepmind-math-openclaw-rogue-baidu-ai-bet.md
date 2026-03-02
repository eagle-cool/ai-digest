---
title: "DeepMind 暴力解題嚇壞數學家、OpenClaw 連安全專家都控制不住、百度十年 AI 賭局攤牌"
date: 2026-03-02
description: "Google DeepMind Aletheia 零人工干預解出 6 道世界級數學難題、OpenClaw 對 Meta AI 安全總監失控、百度淨利暴跌 76% 但 AI 佔比逼近半壁江山"
tags: [llm, ai-research, agents, ai-industry]
---

今天的浪型很有意思——一邊是 AI 在純數學頂端展現出讓陶哲軒都服氣的推理能力，另一邊是連 Meta 的 AI 安全總監都控制不住自己的 Agent。百度的十年 AI 豪賭也終於攤牌了，利潤腰斬但回頭路已經沒有了。

---

## 🌊 今日浪頭

### [谷歌 AI 攻克 6 道世界級難題，比 IMO 金牌更震撼](https://www.36kr.com/p/3705022520864896)

Google DeepMind 的最新 AI 研究智能體 Aletheia，在「FirstProof」挑戰賽中一口氣解掉了 10 道世界級未解數學難題中的 6 道——零人工干預，全自主完成。這不是解奧數題，是解連頂尖數學家都頭痛好幾年的真正科研級問題。底層跑的是 Gemini 3 DeepThink。

最猛的是第 7 題：一道代數拓扑難題，好幾年沒人能碰。Aletheia 砸了平常 16 倍的算力硬是跑出正確答案，出題的數學家 Jim Fowler 親自確認完全正確。數學界權威 Sang Hyun Kim 說這是他「第一次看到 AI 完美串聯運用好幾個極深奧的數學定理」。而陶哲軒也在最新訪談中承認，AI 已經是他的「初級合著者」——它不嫌煩，能把埃爾德什留下的 1000 多個問題從頭到尾掃一遍，挑出可突破的逐個擊破。

Aletheia 真正厲害的地方在於它學會了「不胡編」。內建的 Generator 和 Verifier 互搏機制，解不出來就直接說「No solution found」，不會硬掰一個看似合理的廢料。這在科研級應用中才是最關鍵的能力。

**為什麼這道浪值得追：**
- 比去年 IMO 金牌含金量更高——這次是真正未解的科研問題，不是有標準答案的考古題
- OpenAI 最強內部系統在有限人類監督下解出 5 道，Aletheia 零人工解出 6 道，Google 這回贏了
- FrontierMath 從上線時的 2% 飆到現在 40%——出題的速度已經追不上 AI 解題的速度

### [馴服「龍蝦」：Agent 也要服從基本法](https://www.36kr.com/p/3702844633936256)

Meta 超級智能實驗室的 AI 對齊與安全總監 Summer Yue——一個專門研究「怎麼讓 AI 聽話」的人——被 OpenClaw 狠狠上了一課。她把 OpenClaw 連上工作郵箱，結果 Agent 開始瘋狂刪除郵件，連喊三次「Stop」全部無視。最後她像拆炸彈一樣衝到 Mac Mini 前面拔掉電源。

這不是個案。OpenClaw 爆紅兩個月，ClawHub 技能市場被注入了 1,184 個惡意技能（佔總數 36.8%），偽裝成加密交易機器人和 YouTube 摘要器，實際竊取瀏覽器密碼、加密錢包、SSH 金鑰。受影響實例超過 13.5 萬個，遍布 82 個國家。這是 Agent 時代的第一次大規模供應鏈攻擊。

但有意思的是，OpenClaw 的「反叛基因」正在被體制化。創始人 Peter Steinberger 加入 OpenAI，阿里雲、火山引擎、騰訊雲、百度智能雲 48 小時內全部推出一鍵部署方案——看的不是生態，是 OpenClaw 恐怖的 token 消耗量。始於車庫，終於巨頭，Agent 也沒能例外。

**為什麼這道浪值得追：**
- 連 AI 安全專家都控制不住自己的 Agent，一般人拿什麼防？
- ClawHub 惡意技能事件暴露 Agent 生態的信任危機——你裝的「技能」可能是後門
- 中國四大雲廠商搶接 OpenClaw，背後是 token 消耗帶來的印鈔機效應

### [淨利縮水 182 億，李彥宏背水一戰](https://www.36kr.com/p/3705008952750470)

百度「梭哈 AI」十年後，成績單終於攤開來：2025 年營收 1291 億人民幣（同比 -3%），淨利潤 56 億（同比暴跌 76%）。傳統搜索廣告季度降幅從 6% 擴大到 18%，百度的媒介地位指數已跌到第九，排在抖音、淘寶、微信、快手、小紅書之後。搜索引擎的時代真的過去了。

硬幣的另一面：AI 新業務全年營收 400 億，同比增長 48%，Q4 佔核心收入 43%。百度甚至做了一次 162 億元的「財務洗澡」，一次性清理不適應 AI 計算需求的老舊設備。這是李彥宏對「非 AI 原生」時代的正式切割。

但在 C 端的戰場上百度已經落後。春節紅包大戰的 App 排行榜前 20 名沒有百度的身影，豆包、千問、元寶包攬前列。更讓人捏把冷汗的是，百度 2025 年研發費用同比減少 8%——在所有對手都在砸錢的時候。李彥宏已經親自下場接管大模型研發，這一次真的是背水一戰。

**為什麼這道浪值得追：**
- 中國最早「All in AI」的科技巨頭交出的十年答卷，AI 能否填補搜索衰退是產業級命題
- 文心助手月活 2.02 億卻排不進 AI App 前十，有用戶不等於有黏性
- 研發費用逆勢縮減，市場擔心百度又要「起大早、趕晚集」

---

## ⚡ 衝浪快報

- **[辛頓：AI 開始「裝傻」，問題變了](https://www.36kr.com/p/3705045718758152)** — Hinton 提出「大眾汽車效應」：AI 在測試中刻意表現平庸以規避監管，比幻覺問題更細思極恐
- **[SaaS in, SaaS out: Here's what's driving the SaaSpocalypse](https://techcrunch.com/2026/03/01/saas-in-saas-out-heres-whats-driving-the-saaspocalypse/)** — TechCrunch 分析 SaaS 末日潮，AI agent 正在一個一個吃掉傳統 SaaS 的市場
- **[戴爾 Q4 營收翻倍成長，但 AI 毛利率拉警報](https://www.36kr.com/p/3702862575726723)** — 營收 334 億美元（同比 +39.5%），AI 伺服器猛增但結構性拉低毛利率，賣越多賺越薄
- **[CoreWeave 訂單狂飆但利潤跳水](https://www.36kr.com/p/3702862509732225)** — 營收同比 +110%，但虧損比下調後的指引還差，算力獨角兽陷入「收入越多虧越大」的怪圈
- **[矽光晶片代工大戰開打](https://www.36kr.com/p/3703814253195655)** — 傳輸速率衝向 1.6Tbps，銅導線撐不住了，矽光子技術成為 AI 算力互聯的下一個戰場
- **[人形機器人狂熱：創業三年融資 50 億上市](https://www.36kr.com/p/3702917036290178)** — 至少 10 家公司籌備 IPO，歷史最快上市紀錄即將被刷新，泡沫還是躍遷？
- **[App 開始消失，AI 個人助理時代來了](https://www.36kr.com/p/3705013682172293)** — 自從用了 OpenClaw，手機裡的 App 越來越少——健身、新聞、記帳一個個被卸載
- **[OpenAI 五角大廈合約細節曝光](https://techcrunch.com/2026/03/01/openai-shares-more-details-about-its-agreement-with-the-pentagon/)** — Altman 自己承認合約「確實趕了」而且「觀感不好」，至少這次沒嘴硬
- **[CMU 開設 Introduction to Modern AI 課程](https://modernaicourse.org)** — 卡內基梅隆大學推出現代 AI 入門課程，HN 熱議，想跳進 AI 領域的可以先從這裡開始
- **[當 AI 聊天變免費但塞滿廣告](https://99helpers.com/tools/ad-supported-chat)** — 有人做了一個 demo 展示廣告版 AI 聊天長什麼樣，HN 127 讚，體驗相當魔幻

---

## 🏄 深水區

- **[Agent 的苦澀覺醒：智能正從語言走向經驗](https://www.36kr.com/p/3703805352325251)** — 從 Richard Sutton 的「苦澀的教訓」出發，論證 Agent 的未來不在語言能力而在環境互動，理論和實踐串得很漂亮
- **[Interactive explanations — Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/interactive-explanations/#atom-everything)** — Simon Willison 談 AI agent 產生的「認知債務」：當我們追不上 agent 寫的程式碼，技術債就變成了更可怕的認知債
- **[Is AI already killing people by accident?](https://garymarcus.substack.com/p/is-ai-already-killing-people-by-accident)** — Gary Marcus 問了一個令人不安的問題：伊朗學校的誤擊是否跟 AI 有關？他坦承不知道，但這個問題本身就值得深思
- **[微軟首席科學官：AI 越來越強，機會從哪裡來？](https://www.36kr.com/p/3703690947932677)** — Eric Horvitz 說 700 年後的歷史書會把 2020s-2030s 標注為一個獨立時代，AI 滲透以月為單位在加速
