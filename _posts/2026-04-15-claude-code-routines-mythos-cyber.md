---
title: "Claude Code 變雲端員工、Mythos 首破企業網路防線"
date: 2026-04-15
description: "Anthropic 推出 Routines 讓 Claude Code 全天候雲端自動化、Opus 4.7 本週登場，英國 AISI 證實 Mythos 首破企業網路攻擊模擬，Stanford HAI 報告中美 AI 差距僅 2.7%"
tags: [llm, agents, ai-tools, ai-industry, ai-safety]
---

今天 Anthropic 連開兩槍——Claude Code 桌面端砍掉重練，加上 Routines 雲端自動化直接變成全天候員工；然後 Opus 4.7 被爆料本週就要上線，還順便帶一個要幹掉 Figma 的設計工具。另一邊，英國 AI 安全研究所丟出 Mythos 的獨立評測報告，證實這東西真的能攻破企業網路。浪打浪，今天的水位有點高。

---

## 🌊 今日浪頭

### [Introducing Routines in Claude Code](https://claude.com/blog/introducing-routines-in-claude-code)

Anthropic 今天同時丟出兩個大更新，我看完之後的感想是：他們是真的想把開發者綁在這個平台上走不了。

第一個是 Claude Code 桌面端徹底重構。並行多個 Claude 會話、內建終端、原生程式碼編輯、全新 diff viewer——基本上就是把 IDE 該做的事全攬過來了。你可以一邊讓 Claude 修 bug，一邊在另一個窗口跑測試，拖拽排列，不用在 VS Code 和終端之間反覆跳窗。Alex Albert 直接說他現在連終端都不用開了。

第二個更炸：Routines。簡單說就是把 Claude Code 變成一個合上筆電也能照常上班的雲端員工。你寫好一份「工作說明書」（prompt + 程式碼庫 + 連接器），然後掛上觸發器，Claude 就在 Anthropic 的雲端基礎設施上自己開會話幹活。三路觸發器一次全開——定時排程（每晚凌晨兩點自動拉最高優先級 bug 開 PR）、HTTP API（直接接進 Datadog、Sentry 等告警系統，一個 POST 就能讓 Claude 去查 trace 定位問題）、GitHub Webhook（每個 PR 開一個專屬會話持續追蹤，新 commit、新評論、CI 掛了全部自動 feed 回同一個會話）。

更刺激的是，The Information 獨家爆料 Opus 4.7 將在本週上線，內部代號 capybara-v2，同時還有一款 AI 設計工具要正面挑戰 Figma 和 Adobe。消息一出，Adobe 和 Wix 股價應聲跌超 2%。

**為什麼這道浪值得追：**
- Routines 是 Anthropic 從「賣模型」到「賣 AI 員工」的關鍵轉折——你的整個開發工作流建在上面，遷移成本就不只是換個 API key
- 三路觸發器同時上線意味著 Claude Code 可以接進任何能發 HTTP 請求的系統，從告警到 CI/CD 到內部工單
- 還記得兩週前 Claude Code 源碼洩漏裡那個代號 KAIROS 的功能嗎？技術描述幾乎和 Routines 一一對應，從洩漏到正式發布只隔了兩週

### [UK Gov's Mythos AI Tests Help Separate Cybersecurity Threat from Hype](https://arstechnica.com/ai/2026/04/uk-govs-mythos-ai-tests-help-separate-cybersecurity-threat-from-hype/)

上週 Anthropic 說 Mythos 太危險所以限制發布，很多人覺得是行銷話術。現在英國 AI 安全研究所（AISI）的獨立評測出來了，結果很有意思——既沒有那麼恐怖，但也絕對不是在吹牛。

在單項 CTF 挑戰上，Mythos 跟 GPT-5.4、Opus 4.6 差距不大，都能拿到 85% 以上的通過率。這個水平不足以讓人驚慌。但真正拉開差距的是「The Last Ones」（TLO）——一個模擬 32 步企業網路滲透攻擊的測試，設計上等同於一個受過訓練的人類攻擊者需要 20 小時才能完成的任務。Mythos 成為第一個從頭到尾完整攻破這個測試的 AI 模型。雖然只在 10 次嘗試中成功了 3 次，但平均每次都能完成 22 個步驟，比 Claude 4.6 的 16 步顯著提升。

不過也別太緊張。在更困難的「Cooling Tower」電廠控制系統模擬中，Mythos 還是過不了。而且 AISI 也坦承，他們的測試環境沒有模擬主動防禦者和防禦工具，真實世界的企業系統通常比這難打得多。

**為什麼這道浪值得追：**
- 從「完全做不到」到「能攻破弱防禦企業系統」只花了兩年，這個進步曲線才是真正該關注的
- AISI 明確建議：防守方也該用 AI 來加固防禦，網路安全正式進入 AI vs AI 的時代
- 這是第一次有獨立政府機構公開驗證了 AI 大廠的網安能力聲明，不再只是自說自話

### [Stanford HAI 2026 AI Index Report](https://hai.stanford.edu/ai-index)

Stanford HAI 丟出了 423 頁的 2026 年度 AI 報告，這是 AI 圈最權威的年度體檢單。核心結論只有一句：AI 在衝刺，人類還在找鞋。

幾個讓我倒抽一口氣的數字。中美最強模型的 Elo 評分差距只剩 2.7%——Anthropic 1503、xAI 1495、Google 1494、OpenAI 1481，四家擠在極窄的區間裡。「誰的模型更強」這個問題已經快要失去意義了，競爭焦點正在轉向成本、可靠性和場景覆蓋。

就業數據更扎心。22-25 歲軟體開發者的就業人數自 2022 年以來下降了近 20%，而年長群體仍在成長。McKinsey 調查顯示三分之一的組織預計未來一年會因 AI 裁員。生成式 AI 三年內達到 53% 的人口採納率，超越了 PC 和網際網路的擴散速度。

但最反直覺的一點：花錢最多的國家用得最少。美國在 AI 投資上領先全球（$2,859 億），但人口採納率只有 28.3%，全球排第 24。阿聯酋 64% 居首。另外，42% 的 GSM8K 數學基準測試題目被發現是無效的——我們用來衡量 AI 有多聰明的尺本身就是歪的。

**為什麼這道浪值得追：**
- 前沿模型性能趨同，這解釋了為什麼所有大廠都在瘋狂收購和做平台化——模型本身已經不是護城河
- 初階開發者就業下降 20% 是第一個硬數據支撐「AI 取代工作」的論述，不再只是恐慌
- AI 投資 $5,817 億但應用端回報遠未兌現，泡沫警訊越來越明顯

---

## ⚡ 衝浪快報

- **[Cursor 3.0 被逆向工程，Claude Code 套殼實錘](https://www.36kr.com/p/3766536116732416)** — 開發者 Jason Kneen 在 GitHub 發布了 Cursor 3.0 的逆向分析報告，結論很殘酷：大量核心邏輯直接來自 Claude Code，改了改變數名就上架了。500 億估值，靠 Ctrl+H？
- **[Chrome now lets you turn AI prompts into repeatable 'Skills'](https://www.theverge.com/tech/911658/google-chrome-gemini-ai-skills-availability-launch)** — Google 在 Chrome 裡加了 AI Skills 功能，讓你把常用的 Gemini 指令存成一鍵工具跨網頁重複使用。用全球市佔率最高的瀏覽器推 AI，這招很 Google
- **[Linus Torvalds 拍板：Linux 核心正式為 AI 代碼立規矩](https://www.36kr.com/p/3766613187150601)** — 吵了幾個月終於塵埃落定。AI 生成的代碼可以進 Linux 核心，但提交者必須為代碼品質全權負責。很 Linus 的風格：務實，但不降標準
- **[Hermes Agent 衝上 OpenRouter 榜首，一週暴漲 367%](https://www.36kr.com/p/3766369604203267)** — Nous Research 的 Hermes Agent 在 OpenRouter 上用量暴增到 149B tokens，成為最熱門的編程 Agent。反「龍蝦」情緒的一次集體投票
- **[OpenAI 收購 AI 理財新創 Hiro Finance](https://www.36kr.com/p/3766385735090953)** — OpenAI 又買了一家公司，這次是做 AI 個人理財的 Hiro。團隊約 10 人，4 月 20 日關閉服務，全員加入 OpenAI。AI 離你的錢包越來越近了
- **[SaaS 產業蒸發兩兆美元市值](https://www.36kr.com/p/3766358596600326)** — Claude Cowork 發布以來，ServiceNow 年內跌 41%、Salesforce 跌 39%、Snowflake 跌近一半。IGV 軟體 ETF 從去年高點回撤近 30%，SaaS 的護城河正在被 AI 一層層剝開
- **[金融時報：OpenAI 8,520 億估值遭投資人質疑](https://www.36kr.com/p/3767246332297730)** — FT 重磅長文揭露 OpenAI 內部的焦慮和撕裂。握著 10 億用戶、年增長 50-100%，但早期投資人已經開始倒苦水。估值太高，故事越來越難講
- **[MiniMax 悄改 M2.7 開源授權，社群炸鍋](https://www.36kr.com/p/3766344490746628)** — M2.7 剛以對標頂級閉源模型之姿登場，轉頭就把商業使用改成需要書面授權，MIT 標識卻沒完全撤下。開源界最怕的就是這種「先甜後鹹」
- **[AI 視頻三國殺：阿里 HappyHorse 登頂、字節開放 Seedance 2.0 API](https://www.36kr.com/p/3766278017385216)** — 阿里的匿名模型 HappyHorse 在 Artificial Analysis 盲測榜上登頂，字節的 Seedance 2.0 同日全面開放 API。中國 AI 視頻的價格戰正式開打
- **[Google DeepMind 設立首個 AI 哲學家職位](https://www.36kr.com/p/3767248265691913)** — 劍橋大學學者 Henry Shevlin 五月入職，研究機器意識和 AGI 準備度。頭部 AI 實驗室第一次承認：AGI 不只是工程問題
- **[The attacks on Sam Altman are a warning for the AI world](https://www.theverge.com/ai-artificial-intelligence/911778/ai-violence-sam-altman-home)** — 一名 20 歲男子因害怕 AI 導致人類滅絕，向 Altman 住宅投擲燃燒瓶。AI 恐慌從網路鍵盤戰升級到現實暴力，這個趨勢比任何模型能力都更讓人不安

---

## 🏄 深水區

- **[Anthropic 內部到底在發生什麼：100 個產品原型同時跑、Mythos 斷層領先](https://www.36kr.com/p/3766359456907781)** — Claude Cowork 工程負責人 Felix Rieseberg 在最新播客裡透露，Mythos 帶來的不是常規提升而是「斷層式躍遷」。同時 Anthropic 內部正在同時跑超過 100 個產品原型。想理解這家公司的野心和節奏，這篇值得花時間讀
- **[Steve Yegge: Google Engineering's AI Adoption](https://simonwillison.net/2026/Apr/13/steve-yegge/#atom-everything)** — Steve Yegge 跟在 Google 幹了 20 年的朋友聊了一下 Google 內部的 AI 採用情況，結論讓人大跌眼鏡：「Google 工程團隊的 AI 採用程度，跟 John Deere 那個賣拖拉機的差不多。」大公司的 AI 轉型，可能比你想的慢得多
- **[Cybersecurity Looks Like Proof of Work Now](https://simonwillison.net/2026/Apr/14/cybersecurity-proof-of-work/#atom-everything)** — Simon Willison 結合英國 AISI 對 Mythos 的評測，提出一個觀點：當 AI 能自動化攻擊鏈，網路安全開始變得像 proof of work——防守方必須持續投入運算資源才能維持安全。思路很清晰的一篇分析
- **[Claude Mythos, Evaluated](https://garymarcus.substack.com/p/claude-mythos-evaluated)** — Gary Marcus 拿到 AISI 的評測報告後寫的分析。他的結論是：Mythos 沒有某些人說的那麼可怕，但也確實代表了能力的實質跳躍。對 AI 安全議題想聽不同聲音的人，這篇必讀
