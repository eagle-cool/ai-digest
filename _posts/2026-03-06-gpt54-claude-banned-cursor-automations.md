---
title: "GPT-5.4 原生操控電腦、五角大廈封殺 Claude、Cursor 自動化 Agent 上線"
date: 2026-03-06
description: "OpenAI 發布 GPT-5.4 首度內建電腦操控能力與百萬 token 上下文；五角大廈正式將 Anthropic 列為供應鏈風險，Claude 被踢出美國國防體系；Cursor 推出 Automations 讓 AI Agent 全天候自動審核代碼，營收三個月翻倍破 20 億美元。"
tags: [llm, agents, ai-tools, ai-industry, ai-coding]
---

今天的浪真的猛——OpenAI 甩出 GPT-5.4，第一次讓模型原生操控電腦，直接朝 Agent 時代全力衝刺。另一邊更戲劇性：五角大廈正式把 Anthropic 列為「供應鏈風險」，Claude 被踢出整個美國國防體系，而諷刺的是幾天前 Claude 才剛在美國打擊伊朗的行動中立了大功。Cursor 也沒閒著，推出了 Automations 功能讓 AI Agent 24 小時自動幫你審代碼，營收三個月翻倍到 20 億美元。

---

## 🌊 今日浪頭

### [OpenAI 發布 GPT-5.4：首款原生電腦操控模型，百萬 token 上下文](https://openai.com/index/introducing-gpt-5-4/)

我看了一下 GPT-5.4 的規格，這次的重點不只是「更聰明」，而是模型本身開始能操控電腦了。GPT-5.4 可以透過鍵盤滑鼠指令搭配截圖回饋來操作你的電腦，這是 OpenAI 第一個內建 computer use 能力的模型，直接把 Agent 能力焊進了模型底層。

除了 computer use，GPT-5.4 還有幾個值得注意的升級：百萬 token 上下文窗口、在投行級別的試算表建模任務上從 68.4% 飆到 87.3%、虛假資訊比 GPT-5.2 少了 33%。編碼能力也直接超越了專門的 GPT-5.3-Codex，讓人好奇 Codex 這條產品線是不是要被合併了。API 定價比 GPT-5.2 稍高，超過 272K token 後還有額外加價。同步推出的 GPT-5.4 Thinking 則是 ChatGPT 用戶的推理模型，支援在回應過程中即時調整方向。

**為什麼這道浪值得追：**
- 原生 computer use 代表 AI Agent 不再只是「能寫程式的聊天機器人」，而是真的能幫你操作軟體完成工作
- 百萬 token 上下文讓整個 codebase 或長文件一次丟進去變得可行，對開發者的工作流影響巨大
- OpenAI 正在把所有能力整合進一個統一模型，而非散落在各專門模型裡——這個策略方向值得觀察

### [五角大廈正式將 Anthropic 列為「供應鏈風險」，Claude 被踢出美國國防體系](https://www.theverge.com/ai-artificial-intelligence/890347/pentagon-anthropic-supply-chain-risk)

這件事的戲劇性程度簡直可以拍電影。美國國防部正式將 Anthropic 列為「供應鏈風險」——這個標籤通常是用在跟敵對國家有關聯的外國公司身上，Anthropic 是第一家被貼上這個標籤的美國公司。這意味著所有國防承包商如果在產品中使用 Claude，將被取消國防合約。

衝突的核心是什麼？Anthropic 拒絕讓五角大廈在兩個場景使用 Claude：沒有人類監督的自主致命武器，以及大規模監控。國防部長 Pete Hegseth 更放話，任何跟 Anthropic 有「任何商業往來」的公司都會被取消國防合約——Anthropic 直接說這違法，並宣布將提起訴訟。最諷刺的是，就在幾天前美國打擊伊朗的行動中，Claude 驅動的情報工具在精準打擊中發揮了關鍵作用。你剛立了戰功，轉頭就被封殺。

**為什麼這道浪值得追：**
- 這是 AI 安全理念與國家安全需求的正面對撞，Anthropic 用實際行動證明了它的紅線不是說說而已
- 供應鏈風險標籤的影響範圍可能遠超國防領域，如果 Hegseth 的寬泛解釋成立，整個 Anthropic 的商業生態都會受衝擊
- 這場訴訟將成為 AI 公司與政府權力邊界的標誌性案例，每個 AI 從業者都該關注

### [Cursor 推出 Automations：永不下線的 AI Agent 自動審代碼，營收三個月破 20 億](https://techcrunch.com/2026/03/05/cursor-is-rolling-out-a-new-system-for-agentic-coding/)

Cursor 推出了 Automations，讓 AI Agent 不再需要你手動發 prompt 才啟動。現在你可以設定觸發條件：每次 push 新代碼就自動審查、PagerDuty 收到告警就自動查 log、甚至設定計時器定期跑安全掃描。用 Cursor 工程負責人 Jonas Nelle 的話說：「人類不再是發起者，而是在需要的時候被叫進來。」

這其實是把 BugBot 的概念大幅擴展。以前 BugBot 只在你提交代碼時自動查 bug，現在整個流程都可以自動化——安全審計、事故回應、每週 codebase 變更摘要，全部用 MCP 連接，每小時跑數百個自動化任務。搭配 Bloomberg 剛報的數字：Cursor 年營收三個月內從 10 億翻到 20 億美元，市佔率穩定在 AI 工具用戶的 25%。這個增長速度在 SaaS 歷史上幾乎找不到先例。

**為什麼這道浪值得追：**
- Automations 把 AI coding 從「人驅動 Agent」推進到「Agent 驅動 + 人監督」，這是 agentic coding 的下一個形態
- 跟 OpenAI Codex 和 Claude Code 的競爭白熱化，三家各有路線：OpenAI 走模型整合、Anthropic 走 Agent 框架、Cursor 走工作流自動化
- 營收三個月翻倍的背後，是整個軟體工程行業正在被 AI 重新定價

---

## ⚡ 衝浪快報

- **[Anthropic 發布報告：AI 已覆蓋 75% 程式設計任務](https://www.36kr.com/p/3711060790096001)** — Anthropic 推出「AI 失業預警系統」，調查顯示程式設計 75% 的任務已被 AI 覆蓋，客服和數據錄入緊隨其後，22-25 歲族群首當其衝，但報告也說這是場長達十年的溫水煮青蛙
- **[Luma AI 推出 Uni-1 統一圖像模型，叫板 GPT Image 和 Nano Banana Pro](https://techcrunch.com/2026/03/05/exclusive-luma-launches-creative-ai-agents-powered-by-its-new-unif)** — 15 人華人小隊做出的黑馬，DDIM 之父帶隊，角色姿態遷移、故事板生成、草稿轉漫畫樣樣來，部分任務表現達到世界領先
- **[arXiv 創始人親測 13 個 LLM 造假能力：Grok 最配合，Claude 最有底線](https://www.36kr.com/p/3710916695650694)** — Paul Ginsparg 因為 arXiv 投稿量暴增決定親自下場測試，結果 Claude Opus 4.6 生成可造假內容的比例僅約 1%，Grok 則幾乎來者不拒
- **[xAI 創始成員離職後爆料：Grok 是 36 小時極限肝出來的](https://www.36kr.com/p/3710751595065479)** — 離職工程師透露 Grok 初版的開發過程堪稱瘋狂，36 小時不眠不休從零到可用，這就是 Musk 式的「不可能任務」文化
- **[博通 AI 晶片營收翻倍達 84 億美元，定制 ASIC 正在撕裂 NVIDIA 護城河](https://www.36kr.com/p/3711039962493705)** — 2026 財年 Q1 AI 晶片收入同比暴增 106%，大廠紛紛透過博通做定制晶片減少對 NVIDIA 的依賴，預計 2027 年突破千億
- **[Netflix 收購 Ben Affleck 的 AI 電影製作公司 InterPositive](https://www.theverge.com/streaming/889973/netflix-ben-affleck-interpositive-ai)** — 好萊塢正式擁抱 AI 電影製作，Netflix 買下 Affleck 的 AI 新創，AI 從輔助工具走向內容生產的核心
- **[Meta AI 眼鏡被控將敏感影像送交肯亞人工審核員](https://www.theverge.com/tech/889637/meta-ai-smart-glasses-human-reviewers-kenya)** — 使用者不知情的情況下，包含裸露畫面的影像被送到海外人工審核，隱私爭議再度引爆
- **[美國考慮推出全面性新晶片出口管制](https://techcrunch.com/2026/03/05/us-reportedly-considering-sweeping-new-chip-export-controls/)** — 繼之前的管制措施後，美國政府正在評估更全面的晶片出口限制方案，AI 算力的地緣政治角力持續升溫
- **[阿里緊急成立「大模型支持小組」穩定千問局勢](https://www.36kr.com/p/3710010523595523)** — 繼昨天報導的林俊旸出走後，阿里集團層級介入，成立專門小組確保千問開發不中斷，但人才流失的傷口不是靠組織調整就能補的
- **[AWS 推出專為醫療場景設計的 AI Agent 平台](https://techcrunch.com/2026/03/05/aws-amazon-connect-health-ai-agent-platform-health-care-providers/)** — Amazon Connect 整合醫療 AI Agent，專攻醫療服務提供者的工作流，AI Agent 正在逐步滲透到每個垂直產業

---

## 🏄 深水區

- **[Clinejection：用一個 Issue 標題的 Prompt Injection 就攻破了 Cline 的生產發布流程](https://simonwillison.net/2026/Mar/6/clinejection/#atom-everything)** — Adnan Khan 展示了一條精巧的攻擊鏈：在 GitHub Issue 標題裡埋入 prompt injection，誘導 Cline 的 AI 驅動 Issue 分類器執行惡意操作，直接影響生產發布。如果你的團隊在用 AI 做自動化，這篇是必讀的安全警示
- **[Coding Agent 能透過「無塵室」實作來重新授權開源代碼嗎？](https://simonwillison.net/2026/Mar/5/chardet/#atom-everything)** — Simon Willison 深入探討一個越來越尖銳的問題：AI coding agent 生成的「從零實作」到底算不算 clean room implementation？這牽涉到開源授權的根基，1982 年 Compaq 複製 IBM BIOS 的故事正在以 AI 的形式重演
- **[Anthropic 研究：AI 對勞動市場的影響——新量測方法與早期證據](https://www.anthropic.com/research/labor-market-impacts)** — 不同於媒體標題黨式的報導，這是 Anthropic 的完整研究論文，提出了量測 AI 對就業影響的新框架，數據紮實，結論比新聞標題寫的「75% 取代」要細緻得多，值得花時間看原文
- **[406.fail：一套標準協議，專門處理和丟棄低品質 AI 生成的 Pull Request](https://406.fail/)** — AI 生成的垃圾 PR 已經成為開源維護者的新噩夢，這個專案提出了一套標準化的處理協議，用 HTTP 406 狀態碼優雅地拒絕，開源社群的自我防禦機制正在成形
