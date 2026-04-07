---
title: "GPT-6 下週見？GEN-1 機器人量產級、Claude 秒破最安全 OS"
date: 2026-04-07
description: "GPT-6 代號 Spud 傳聞 4/14 發布、Generalist GEN-1 機器人達 99% 成功率邁入量產、Claude 4 小時自主攻破 FreeBSD 內核——AI 的浪今天又大了一圈"
tags: [llm, agents, ai-tools, ai-research, ai-industry]
---

今天 AI 圈的浪有點猛——GPT-6 的消息像篩子一樣漏了出來，一家機器人公司宣稱達到量產級成功率，而 Claude 則用 4 小時幹了以前國家級駭客團隊才幹得出來的事。每一條都夠震撼，但湊在一起看，你會發現 AI 正在同時往三個方向全速推進：更聰明的腦、更靈巧的手、更鋒利的牙。

---

## 🌊 今日浪頭

### [GPT-6，曝光了](https://www.36kr.com/p/3754726863012361)

代號 Spud（土豆），據傳 4 月 14 日發布。我看了一下這波爆料，細節多到不像是空穴來風——性能比 GPT-5.4 暴漲 40%、原生多模態（文本音頻圖像視頻一把抓）、2M 上下文窗口，定價居然沒比 GPT-5.4 貴多少，每百萬 Token 輸入 $2.5、輸出 $12。

更關鍵的是 OpenAI 對這個模型的定位：把 ChatGPT、Codex 和 Atlas 瀏覽器融合成一個統一智能體，打造桌面級超級應用。內部員工的說法是「這是 AGI 的最後一公里」。Sora 被砍、迪士尼合約泡湯，全是為了把資源壓在這一把。

**為什麼這道浪值得追：**
- 預訓練據稱 3 月 17 日已完成，隨時可以上線——如果屬實，這速度比所有人預期的都快
- Brockman 自己說 AGI 進度 80%，OpenAI 內部認為 GPT-6 就是剩下的 20%
- 當然，爆料者的準確度見仁見智，但大方向上「OpenAI 砍光旁支 All-in 下一代模型」這件事是確定的

### [From folding boxes to fixing vacuums, GEN-1 robotics model hits 99% reliability](https://arstechnica.com/ai/2026/04/generalists-new-physical-robotics-ai-brings-production-level-success-rates/)

Generalist 發布 GEN-1，號稱在摺紙箱、包裝手機、維修掃地機器人等精密操作上達到 99% 成功率，速度是前代 GEN-0 的三倍。這不只是數字好看——它真正讓我興奮的是「即興應變」能力。塑膠袋太軟塞不進去？機器人會自己搖一搖讓東西滑進去，這動作根本不在訓練資料裡。

背後的秘密武器是一副叫「data hands」的穿戴式夾子，捕捉人類操作時的微動作和視覺資訊，已經累積超過 50 萬小時的物理互動數據。Generalist 說這是機器人領域的「GPT-3 時刻」——部分任務開始跨過經濟可行性的門檻。

**為什麼這道浪值得追：**
- 以前機器人要嘛預編程、要嘛只會單一任務，GEN-1 用一個模型處理多種任務還能從錯誤中恢復
- 對比 Tesla Optimus 至今還沒做到有用的工作，Generalist 的進展顯得格外實在
- 只需約一小時的適配訓練就能部署到新機器人本體上，這對商業落地至關重要

### [Claude 4小時血洗全球最安全系統](https://www.36kr.com/p/3754727404389121)

FreeBSD——Netflix CDN、PlayStation OS、WhatsApp 基礎設施背後的系統——被 Claude 在 4 小時內自主攻破。安全研究員 Nicholas Carlini 用 Claude 從零構建了兩條完整的內核遠程攻擊鏈，直接拿到 root 權限。CVE-2026-4747 的致謝欄寫著「Nicholas Carlini 使用 Claude 發現」。

以我的理解，這件事之所以炸裂，是因為以前寫內核級漏洞利用程式是 NSA 等級的「藝術活」，需要頂尖專家花數週到數月、成本數百萬美元。現在一個研究員加一個 AI，幾百美金算力費，4 小時搞定。更可怕的是 Lyptus 的最新研究顯示，AI 網路攻擊能力每 5.7 個月翻一倍。

**為什麼這道浪值得追：**
- 這是首份確鑿證據：AI 能自主生成國家級進攻能力，不是理論推演
- 防守方的補丁部署週期還是以月計算，但攻擊方的能力已經用小時計算了
- 網路安全正從「人類智力博弈」降維成「Token 消耗戰」——這改變了整個產業的遊戲規則

---

## ⚡ 衝浪快報

- **["The problem is Sam Altman": OpenAI Insiders don't trust CEO](https://arstechnica.com/tech-policy/2026/04/the-problem-is-sam-altman-openai-insiders-dont-trust-ceo/)** — The New Yorker 丟出重磅調查，OpenAI 內部對 Altman 的信任正在崩塌，IPO 前夕這劇情也太刺激了
- **[Iran threatens Stargate AI data centers](https://techcrunch.com/2026/04/06/iran-threatens-stargate-ai-data-centers/)** — 伊朗直接威脅要用飛彈打 OpenAI 在阿布達比的 Stargate 資料中心，AI 基建現在也是地緣政治目標了
- **[OpenAI's vision for the AI economy: robot taxes and a four-day workweek](https://techcrunch.com/2026/04/06/openais-vision-for-the-ai-economy-public-wealth-funds-robot-taxes-and-a-four-day-work-week/)** — OpenAI 提出 AI 經濟政策白皮書：對 AI 利潤課稅、公共財富基金、週休三日，認真的嗎
- **[iPhone本地跑Gemma 4火了，0 token時代還有多遠？](https://www.36kr.com/p/3754860403294985)** — Google 開源的 Gemma 4 E2B/E4B 可以直接在手機上本地跑，128K 上下文，放進口袋的 Gemini 平替
- **[疯狂的Skill](https://www.36kr.com/p/3752193867809283)** — GitHub 上 .skill 專案瘋狂爆發，「同事.skill」5 天拿 6.6k 星，這股 AI 人格複製的浪潮破圈到小紅書微博了
- **[AI會感到絕望？Anthropic最新研究給出了一個更嚇人的說法](https://www.36kr.com/p/3752096553677574)** — Anthropic 提出「功能性情緒」概念，AI 不是有喜怒哀樂，但確實會被 PUA 話術影響表現，這研究方向很有意思
- **[Claude訂閱封殺龍蝦背後的計費哲學](https://www.36kr.com/p/3754978719220486)** — Anthropic 禁止訂閱用戶透過 OpenClaw 使用額度，Agent 時代的計費模型需要重新設計
- **[互聯網最驕傲的事，正在被AI一點點拆掉](https://www.36kr.com/p/3752091174433283)** — 四大科技巨頭年燒 $6500 億在 AI 基建上，快追上全球半導體產業年營收了，互聯網正在從「輕」變「重」
- **[萝卜快跑停摆，Robotaxi面临安全大考](https://www.36kr.com/p/3754828003639811)** — 武漢萝卜快跑集體宕機，多輛車停在馬路中間，L4 無人駕駛的「十重安全冗餘」形同虛設
- **[Real-time AI (audio/video in, voice out) on an M3 Pro with Gemma E2B](https://github.com/fikrikarim/parlor)** — HN 爆紅 244 分，在 Mac 本地跑 Gemma E2B 實現即時音視頻 AI 對話，完全離線
- **[Google quietly launched an AI dictation app that works offline](https://techcrunch.com/2026/04/06/google-quietly-releases-an-offline-first-ai-dictation-app-on-ios/)** — Google 用 Gemma 模型做了一個離線語音轉文字 App，瞄準 Wispr Flow 市場

---

## 🏄 深水區

- **[Eight years of wanting, three months of building with AI](https://simonwillison.net/2026/Apr/5/building-with-ai/#atom-everything)** — Lalit Maganti 花八年想做的事，用 AI 三個月就做出來了——這篇關於 agentic engineering 的長文是近期最值得讀的實戰分享
- **[Sam Altman, unconstrained by the truth](https://garymarcus.substack.com/p/sam-altman-unconstrained-by-the-truth)** — 搭配 New Yorker 的調查一起讀效果更好，Gary Marcus 系統性整理了 Altman 的信任危機脈絡
- **[AI，為什麼也需要睡覺？](https://www.36kr.com/p/3754827335205385)** — 從 Claude Code 源碼洩漏中發現的 autoDream 功能切入，探討 AI 記憶管理和「做夢」機制，腦洞很大但分析有料
- **[Suno is a music copyright nightmare](https://www.theverge.com/ai-artificial-intelligence/906896/sunos-copyright-ai-music-covers)** — Suno 號稱阻擋侵權但實測漏洞百出，AI 音樂的版權灰色地帶比想像中更混亂
