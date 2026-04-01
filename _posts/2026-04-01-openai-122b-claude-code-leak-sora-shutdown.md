---
title: "OpenAI 1220 億美元到手、Claude Code 原始碼外洩、Sora 正式收攤"
date: 2026-04-01
description: "OpenAI 完成史上最大私募融資 1220 億美元估值破 8520 億、Anthropic 的 Claude Code 原始碼因 npm source map 意外全數曝光、OpenAI 關停 Sora 將算力轉投 AGI——今天 AI 圈的浪一波接一波。"
tags: [llm, ai-industry, ai-tools, ai-coding]
---

今天 AI 圈的浪有點猛——OpenAI 一口氣吞下 1220 億美元成為人類商業史上最大單輪私募，Anthropic 那邊則因為一個 source map 檔案把 Claude Code 51 萬行原始碼全曝光了，而 Sora 在燒掉每天 1500 萬美元之後正式收攤。這三件事加在一起，大概就是 2026 年 AI 軍備競賽的最佳縮影。

---

## 🌊 今日浪頭

### [OpenAI raises $122 billion in new funding](https://openai.com/index/accelerating-the-next-phase-ai)

1220 億美元。單輪。私募。我反覆看了三遍確認沒多打一個零。OpenAI 這輪融資由 Amazon、NVIDIA 和 SoftBank 領投，三家合計承諾 1100 億，其中 Amazon 一家就砸了 500 億——但有個巧妙的設計：150 億先到帳，剩下 350 億要等 OpenAI 完成 IPO 或達成他們自己定義的「AGI」才解鎖。融資後估值落在 8520 億美元，距離萬億只差臨門一腳。更有意思的是，這輪還開放了 30 億給散戶投資人，這在 pre-IPO 階段幾乎前所未見。

**為什麼這道浪值得追：**
- 人類商業史上最大單輪私募，比原先公布的 1100 億又多出 120 億，代表後來搶進的機構比預期多
- Amazon 的「AGI 對賭條款」很有意思——等於讓 OpenAI 自己定義什麼時候達標，這合同怎麼寫的我很好奇
- IPO 節奏越來越清晰，這大概是上市前最後一次大規模私募，Stargate 資料中心計畫也有了彈藥

### [Entire Claude Code CLI source code leaks thanks to exposed map file](https://techcrunch.com/2026/03/31/anthropic-is-having-a-month/)

Anthropic 真的在上演連續劇。Claude Code v2.1.88 發布到 npm 的時候，一個 60MB 的 source map 檔案被意外打包進去，結果超過 1900 個檔案、51.2 萬行 TypeScript 原始碼全數曝光。安全研究者 Chaofan Shou 發現後一發推文，幾個小時內瀏覽量破 780 萬，備份倉庫瞬間拿了 2 萬多星。Anthropic 官方的說法是「發布打包問題導致的人為失誤，不是安全漏洞」——但這已經是一週內第二次出包了，上週四才剛被報導有 3000 份內部文件意外公開，裡面還包含未發布模型的細節。

**為什麼這道浪值得追：**
- 對手和社群第一次完整看到頂級 AI Agent 產品的工程架構，包括未發布功能、內部邏輯、工程師手寫注釋
- 一週兩次資料外洩，對於一家以「最謹慎的 AI 公司」自居、估值 3500 億的公司來說，這時間點實在尷尬——IPO 前夕欸
- 這不是模型權重外洩，但工程架構的曝光對競爭對手來說也是一份免費的技術藍圖

### [Sora 跌倒，字節吃飽：OpenAI 關停 Sora 的算力經濟學](https://www.36kr.com/p/3746785722958599)

Sora 死了。從驚艷全球到正式收攤，只花了 25 個月。3 月 24 日 OpenAI 毫無預警地全面關停——App 下架、API 斷線、ChatGPT 入口移除。背後的數字很殘酷：每天營運成本 1500 萬美元，年化 54 億，但上線六個月累計營收才 210 萬。30 天留存率不到 1%，60 天趨近於零。在 IPO 估值 8520 億的壓力下，華爾街要的是清晰的獲利路徑，Sora 顯然不在那條路上。而大洋彼岸，字節的 Seedance 2.0 趁勢上位，原生 2K 解析度加上導演級鏡頭語言控制，在 Text-to-Video 排行榜上已經排到第一。中國 AI 視頻工具集體漲價——即夢積分從 45 漲到 120，小雲雀漲了 167%。

**為什麼這道浪值得追：**
- Sora 的失敗本質上是 C 端 AI 視頻的商業模式失敗——高算力成本 vs 近乎零的用戶留存，這道題目前沒人解得開
- Disney 10 億美元投資和 200+ IP 授權協議一起泡湯，據路透社報導，公告前半小時 Disney 高管還在開會
- 中國廠商的優勢在於生態閉環——字節有抖音和剪映，算力成本可以透過廣告和電商 GMV 轉化來攤平

---

## ⚡ 衝浪快報

- **[Microsoft Copilot 引入多模型：GPT 寫稿、Claude 審稿](https://www.36kr.com/p/3746797166428675)** — 單模型時代結束了，Copilot Researcher 現在預設 GPT 寫初稿、Claude 當專家評審，微軟的策略很明確：不管誰贏，流量都經過我
- **[Claude Code 新增 Computer Use 能力](https://www.36kr.com/p/3746567168311816)** — 在原始碼外洩的同時，Anthropic 也發布了 Claude Code 的 Computer Use 功能，直接從 CLI 操控你的 Mac，從寫程式到驗證的完整閉環
- **[國行蘋果 AI 凌晨偷跑又緊急撤回](https://www.36kr.com/p/3746574781854215)** — 凌晨悄悄上線，早上光速消失，彭博社 Gurman 確認是誤操作，蘋果 AI 在中國仍未獲監管批准
- **[DeepSeek 史詩級宕機 13 小時後隔天又崩](https://www.36kr.com/p/3746760162689799)** — 從 3/29 晚到 3/30 上午整整 13 小時停擺，隔天下午又崩了一小時，種種跡象指向 V4 可能在悄悄部署
- **[Microsoft 發布 Harrier 開源模型家族](https://www.reddit.com/r/AIDeveloperNews/comments/1s8xfw0/microsoft_releases_harrier_oss_models_27b_270m/)** — 三個規格：27B、270M、0.6B，基於 Gemma3 架構，瞄準本地部署場景
- **[Google 發布 Veo 3.1 Lite 視頻生成模型](https://blog.google/innovation-and-ai/technology/ai/veo-3-1-lite/)** — Sora 收攤的同一天，Google 推出最具性價比的視頻生成模型，透過 Gemini API 提供付費預覽
- **[GitHub Copilot 在 PR 裡偷塞廣告](https://www.36kr.com/p/3746701509280517)** — 讓 Copilot 改個拼寫錯誤，結果它順手在文末塞了自己和 Raycast 的廣告，這植入水準有點熟練
- **[Block 裁員 40% 約 4000 人，CEO 直言 AI 可替代](https://www.36kr.com/p/3746701346423559)** — Jack Dorsey 連演都不演了，自研 AI Agent「Goose」讓 6000 人做 10000 人的工作，股價暴漲 20%
- **[氛圍編程（Vibe Coding）淹沒 App Store](https://www.36kr.com/p/3746764444025608)** — 審核等待從 48 小時暴增到 45 天，AI 生成的垃圾 App 大量湧入，程式設計的「民科時代」來了
- **[Apple Siri 將變身開放平台，iOS 27 接入所有 AI 聊天機器人](https://www.36kr.com/p/3746464344998409)** — WWDC 2026 將推出 Siri Extensions，Gemini、Claude 都能直接從 Siri 呼叫，蘋果要收 AI 版的「蘋果稅」了
- **[ChatGPT 登陸 Apple CarPlay](https://www.theverge.com/ai-artificial-intelligence/904676/apple-carplay-openai-chatgpt)** — iOS 26.4 開放語音對話 App 支援，開車時可以直接從車機叫 ChatGPT

---

## 🏄 深水區

- **[Two Worlds — geohot](https://geohot.github.io//blog/jekyll/update/2026/03/30/two-worlds.html)** — Claude Mythos「戲劇性地」超越 Opus 4.6 vs AI 泡沫正在破裂，這兩件事怎麼同時為真？geohot 用 1850 年帶智慧型手機穿越的比喻來拆解這個矛盾，值得花十分鐘想想
- **[Agentic AI: From Tantrums to Trust](https://www.reddit.com/r/AIDeveloperNews/comments/1s8wd1h/agentic_ai_from_tantrums_to_trust/)** — AI Agent 在生產環境的失敗模式是現有 benchmark 完全沒覆蓋到的：context 遺失、跨 handoff 漂移、遇到敏感場景不會減速，這篇把問題拆得很清楚
- **[How did Anthropic measure AI's "theoretical capabilities" in the job market?](https://arstechnica.com/ai/2026/03/how-did-anthropic-measure-ais-theoretical-capabilities-in-the-job-market/)** — Anthropic 那張「AI 對就業市場理論能力」的圖最近到處流傳，Ars Technica 這篇仔細拆解了他們的方法論和數據來源
- **[Small note about AI 'GPUs'](https://xeiaso.net/notes/2026/ai-gpus-cant-process-graphics/)** — 等著 AI 泡沫破裂撿便宜 GPU 來打遊戲的人可能要失望了——伺服器級 GPU 根本不能輸出畫面，Xe Iaso 這篇科普值得轉給你那些在等的朋友
