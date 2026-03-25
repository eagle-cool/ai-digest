---
title: "Sora 收攤了、Arm 35 年首顆自研晶片、LiteLLM 被下毒"
date: 2026-03-25
description: "OpenAI 宣布全面關停 Sora 影片平台，Arm 破天荒推出自研 AI 資料中心 CPU，LiteLLM 爆發惡意套件供應鏈攻擊——今天的浪型有點複雜。"
tags: [llm, ai-tools, ai-industry, ai-coding]
---

今天的浪型挺特別——一個大產品直接收攤、一家 35 年沒自己做過晶片的公司突然掏出 CPU、然後你常用的 AI 套件被人下了毒。三道浪同時打過來，而且每一道都跟你切身相關。

---

## 🌊 今日浪頭

### [Sora 宣布關停，史上最貴 AI 表情包生成器只撐了七個月](https://www.36kr.com/p/3737580650823945)

去年九月底 Sora 2 上線那天，Altman 大手一揮把自己的 cameo 功能開放給所有人，結果被網友做成各種 AI 迷因瘋傳，「AI 影片元年」的口號喊得震天響。七個月後，他親手簽了 Sora 的死亡通知書。

根據《華爾街日報》報導，Altman 在內部信中宣布 Sora 影片平台全面停運——不只消費端 App，連開發者 API、ChatGPT 裡的影片生成功能，統統砍掉。乾淨利落，不留餘地。Sora 官方也在 X 上發文告別了。

我的觀察是：Sora 的問題從來不是技術不夠強，而是找不到商業模式。使用者新鮮感一過就不碰了，企業端也沒有殺手級應用場景。OpenAI 現在的策略很明顯——把資源集中到 ChatGPT 核心和 Agent 生態上，影片生成這種燒錢但不賺錢的東西，直接砍。

**為什麼這道浪值得追：**
- 從 Sora 首次驚豔亮相到完全關停，整個生命週期不到兩年——AI 產品的生死速度比你想像的更快
- 影片生成賽道不會消失，但 OpenAI 退出意味著短期內沒有超級大廠撐場，Runway、Pika、可靈們反而迎來喘息空間
- 配合最近的 IPO 文件和組織重整，OpenAI 正在進入「盈利優先」的新階段，不賺錢的產品線會被更果斷地砍掉

### [Arm 發布 35 年來首顆自研晶片：3nm、136 核、專為 AI 打造](https://techcrunch.com/2026/03/24/arm-is-releasing-its-first-in-house-chip-in-its-35-year-history/)

這個消息一出來我整個人都清醒了。Arm——對，就是那個授權 IP 給全世界手機晶片廠商的 Arm——居然自己做晶片了。而且不是做著玩的，是認真要賣的。

這顆叫 Arm AGI CPU 的晶片，專為 AI 資料中心打造，採用台積電 3nm 製程、雙 Chiplet 設計，單顆最多 136 個 Arm 核心。首個合作夥伴和客戶是 Meta。Arm 高管說這顆晶片將帶來數十億美元的收入——對一家過去只賺授權費的公司來說，這句話的份量非同小可。

Arm 過去 35 年的商業模式就是「我設計 IP，你們去做晶片」。現在它直接跳下場自己做，等於是跟自己的客戶們搶生意。不過市場對 AI 算力的需求大到現有模式已經不夠用了，這或許是 Arm 不得不做的選擇。

**為什麼這道浪值得追：**
- 這是 Arm 商業模式 35 年來最大的轉變——從純 IP 授權到自研晶片銷售，直接衝擊 Intel、AMD、甚至自家客戶高通的地盤
- Meta 是首個客戶，考慮到 Meta 正砸數千億美元搞 AI 基建，這顆晶片的規模化前景值得關注
- 命名「AGI CPU」不是巧合——整個晶片產業正在把 AI 推論需求當作下一個十年的核心戰場

### [LiteLLM v1.82.8 被植入惡意程式，安裝就觸發憑證竊取](https://simonwillison.net/2026/Mar/24/malicious-litellm/#atom-everything)

如果你是 AI 開發者，這條請立刻看。

LiteLLM v1.82.8 在 PyPI 上被動了手腳，裡面藏了一個用 base64 編碼的憑證竊取程式，塞在 `litellm_init.pth` 檔案裡。最恐怖的是——你甚至不需要 `import litellm`，光是安裝就會觸發。v1.82.7 也中招了，只是那版要 import 才會啟動。

被偷的東西清單讓人頭皮發麻：SSH 金鑰、Git 憑證、AWS 設定、Kubernetes 配置、Azure / Docker / npm 憑證、shell 命令歷史記錄、加密貨幣錢包、資料庫憑證⋯⋯基本上你機器上所有的 secret 都被掃了一遍。

攻擊鏈是這樣的：先攻破安全掃描工具 Trivy，偷到 PyPI 的上傳憑證，再用這個憑證直接把惡意版本推上 PyPI。PyPI 在發現後幾小時內隔離了套件，但受影響的時間窗口裡安裝的人都需要立即處理。

**為什麼這道浪值得追：**
- LiteLLM 是很多 AI 開發者的核心依賴——用來統一呼叫各家 LLM API 的中間層，影響範圍極廣
- 「安裝即觸發」的攻擊手法比一般惡意套件更危險，連 CI/CD 環境都逃不掉
- 如果你在過去幾天安裝或升級過 LiteLLM，請立刻移除 v1.82.7 / v1.82.8，並輪換所有受影響機器上的憑證

---

## ⚡ 衝浪快報

- **[Anthropic 給 Claude Code 開了「自動模式」，讓 AI 自主操作你的電腦](https://techcrunch.com/2026/03/24/anthropic-hands-claude-code-more-control-but-keeps-it-on-a-leash/)** — Claude Code 和 Cowork 現在可以自動開檔案、瀏覽網頁、填表單，你只要用手機下指令。安全繩還在，但已經鬆了不少
- **[OpenAI IPO 文件把微軟列為「潛在風險」](https://www.36kr.com/p/3736692639858695)** — 拿人家的錢、用人家的算力，然後在招股書裡說對方是風險因素，這關係也太微妙了
- **[從現在開始，得像研究 DeepSeek 一樣認真對待 Kimi](https://www.36kr.com/p/3736870910968065)** — 月之暗面正以 180 億美元估值融資，Kimi 的多模態和程式碼能力讓重度用戶都開始側目
- **[OpenAI 聯手 MIT 證實：ChatGPT 用越多越孤獨](https://www.36kr.com/p/3736752091906305)** — 981 名受試者、四週追蹤、30 萬條對話——史上最大規模 AI 心理影響研究，結論讓 OpenAI 自己都尷尬
- **[ChatGPT 推出 Agentic Commerce Protocol，要幫你買東西](https://openai.com/index/powering-product-discovery-in-chatgpt)** — 視覺化購物、商品比較、商家串接一條龍，跟 Google Gemini 搶電商入口的戰爭正式開打
- **[Spotify 測試新工具防止 AI 生成音樂冒用真人藝人名義](https://techcrunch.com/2026/03/24/spotify-tests-new-tool-to-stop-ai-slop-from-being-attributed-to-real-artists/)** — AI slop 已經氾濫到平台必須出手了，讓藝人自己決定哪些歌可以掛在他們名下
- **[Databricks 收購兩家 AI 安全新創 Antimatter 和 SiftD.ai](https://techcrunch.com/2026/03/24/databricks-buys-two-startups-lakewatch-antimatter-siftd-ai-security/)** — 剛募完 50 億美元就開始掃貨，AI 安全正在成為資料平台的標配功能
- **[OpenClaw 大更新翻車：12 小時內緊急發新版](https://www.36kr.com/p/3736768002015233)** — v3.22 暴力拆除舊 API 導致 UI 崩潰，連 DeepSeek 和 Qwen 的正式接入都差點被拖下水
- **[騰訊挖角多位字節 Seed 團隊骨幹，向姚順雨匯報](https://www.36kr.com/p/3736935323254785)** — 字節視覺 AI 和 Infra 核心人員轉投騰訊混元，中國大模型的人才戰越打越激烈
- **[OpenAI Foundation 宣布至少投資 10 億美元於疾病治療和社會公益](https://openai.com/index/update-on-the-openai-foundation)** — IPO 前夕的公益佈局，誠意幾分見仁見智，但 10 億美元確實是大手筆

---

## 🏄 深水區

- **[哈佛物理教授用 Claude 4.5 兩週寫完博士生一年的論文](https://www.36kr.com/p/3736752148988168)** — 不是 toy project，是已發表在頂刊的量子場論研究。教授說 AI 當研究者的時代已經來了，讀完你會重新思考 PhD 的意義
- **[前 Google TPU 工程師首次揭秘：TPU 到底能不能撼動 NVIDIA？](https://www.36kr.com/p/3736564173468417)** — Apple、Anthropic、Meta 都在用 TPU，這篇從內部視角拆解了 Google 這張低調但可怕的算力底牌
- **[Streaming Experts：在記憶體不夠的硬體上跑大型 MoE 模型](https://simonwillison.net/2026/Mar/24/streaming-experts/#atom-everything)** — 把需要的 expert 權重從 SSD 串流進 RAM，讓消費級硬體也能跑巨型模型，技術思路很有意思
- **[Is anybody else bored of talking about AI?](https://blog.jakesaunders.dev/is-anybody-else-bored-of-talking-about-ai/)** — HN 上 231 個讚的逆風文。當所有人都在聊 AI 的時候，有人問：我們是不是聊太多了？值得在亢奮中冷靜一下
