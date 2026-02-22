---
title: "Claw 正式出道、Meta AI 封號暴走、AI 駭客打穿 600 防火牆"
date: 2026-02-22
description: "Karpathy 正式定義 Claw 為 LLM Agent 上的新堆疊層，Meta AI 自動化系統瘋狂封殺合法廣告代理商，AWS 揭露 AI 駭客 5 週攻破 600 台 FortiGate 防火牆。"
tags: [agents, ai-tools, ai-industry, ai-safety]
---

今天 AI 圈同時在造神和翻車——Karpathy 一句話讓 "Claw" 從地下術語變成正式的技術堆疊層，Meta 的 AI 審核系統瘋到連花了幾百萬美金的廣告代理商都封，然後 AWS 安全團隊發了一份報告，說有駭客用 AI 在 5 週內打穿了 600 台防火牆。AI 的能力邊界在同時往兩個方向擴張。

---

## 🌊 今日浪頭

### [Claws are now a new layer on top of LLM agents](https://simonwillison.net/2026/Feb/21/claws/)

Karpathy 又造了一個會流傳開來的概念。他說 "Claw" 已經是 LLM agent 之上的一個新層級——負責排程、上下文管理、工具呼叫和持久化，簡單說就是讓 AI agent 從「你叫它做事」進化到「它自己安排什麼時候做什麼事」。目前已經冒出一堆實作：NanoClaw、zeroclaw、ironclaw、picoclaw，都跑在個人硬體上，核心引擎只有大約 4000 行程式碼就能審計完。

**為什麼這道浪值得追：**
- Karpathy 之前定義了「vibe coding」和「agentic engineering」，這些詞都變成了業界共識——"Claw" 很可能是下一個
- 這代表 AI 不再只是你對話的對象，而是一個跑在你機器上、有自己排程和記憶的常駐系統，概念上更接近作業系統的 daemon
- 135 分、564 則留言的 HN 討論量說明社群已經在認真對待這個分類，不是一時的 hype

### [Meta Deployed AI and It Is Killing Our Agency](https://mojodojo.io/blog/meta-is-systematically-killing-our-agency/)

這篇 131 分的 HN 爆文來自一間每年在 Meta 上花幾百萬美金廣告費的代理商。他們的遭遇很荒謬：每次新員工建立工作帳號，上傳身份證、駕照、出生證明、做完人臉掃描之後，帳號在五分鐘到十小時內就被 AI 自動封禁。這種事已經重複發生了幾十次。申訴工具在平台內部，但帳號被封就登不進去——所以你根本無法申訴。Meta 客服的回覆永遠是「建一個新帳號」或「提交申訴」，然後新帳號又被封。

**為什麼這道浪值得追：**
- Meta 客服已經確認帳號管理「幾乎完全由 AI 處理」，內部工單也無法觸及有權限的人類審核者——這是 AI 自動化做過頭的教科書案例
- 從 2008 年就開始在 Facebook 投廣告、花了幾百萬美金的客戶都能被這樣對待，那一般使用者遇到問題根本沒有任何指望
- Google 和 TikTok 都沒有這個問題，這不是「AI 就是這樣」，是 Meta 選擇了完全不留人類兜底的路線

### [AI-augmented threat actor accesses FortiGate devices at scale](https://aws.amazon.com/blogs/security/ai-augmented-threat-actor-accesses-fortigate-devices-at-scale/)

AWS 安全團隊發布了一份報告，揭露了一個用 AI 輔助的攻擊者在短短 5 週內攻破了超過 600 台 FortiGate 防火牆。這不是理論上的威脅模型，是 Amazon 在自家雲端上觀察到的真實攻擊事件。AI 讓攻擊者能夠以前所未有的速度掃描、利用漏洞並橫向移動。

**為什麼這道浪值得追：**
- 5 週 600 台——這種攻擊規模和速度在 AI 輔助之前是很難想像的，攻擊方的 AI 加速已經是現實
- FortiGate 是企業防火牆的主流品牌之一，被攻破的不是什麼小眾設備
- 防禦方也需要用 AI，但目前攻守雙方的 AI 軍備競賽，攻擊方明顯跑在前面

---

## ⚡ 衝浪快報

- **[GPT-5.3-Codex-Spark 速度提升 30%，推論達 1200 tokens/sec](https://simonwillison.net/2026/Feb/21/thibault-sottiaux/#atom-everything)** — OpenAI 悄悄把 GPT-5.3-Codex-Spark 加速了三成，coding 場景的推論速度又往前推了一大步
- **[Nvidia GB10 Superchip 讓你在客廳跑嚴肅的 AI 模型](https://www.pcmag.com/news/nvidia-gb10-superchip-running-ai-models-in-my-living-room)** — PCMag 實測 Nvidia GB10，在自己家就能跑大型模型，Local AI 硬體終於有了消費級的真正選項
- **[Amazon 正式回應：AWS 停機是人為錯誤不是 AI 問題](https://www.aboutamazon.com/news/aws/aws-service-outage-ai-bot-kiro)** — Amazon 發文反駁 FT 報導，堅持 Kiro 那次只是「權限設定錯誤」，但工程師們的說法可不是這樣
- **[硬碟今年全部售罄，AI 是元兇](https://www.theregister.com/2026/02/20/ai_blamed_again_as_hard_drives_sell_out/)** — AI 訓練和推論吃掉了全球硬碟產能，今年的硬碟已經賣完了——你沒看錯，整年的
- **[Sanders 警告美國對 AI 革命的速度和規模毫無準備](https://www.theguardian.com/us-news/2026/feb/21/ai-revolution-bernie-sanders-warning)** — Bernie Sanders 出來喊話了，認為美國政府對 AI 帶來的就業衝擊完全沒有準備
- **[Google AI Studio 停擺超過 4 天](https://aistudio.google.com/status)** — Google 自家的 AI 開發平台掛了 4 天以上，開發者叫苦連天，Google 的 AI 基礎設施穩定性令人擔憂
- **[EFF 發布開源專案的 LLM 貢獻政策](https://www.eff.org/deeplinks/2026/02/effs-policy-llm-assisted-contributions-our-open-source-projects)** — EFF 正式表態 LLM 輔助的開源貢獻該怎麼處理，開源社群終於有了一個有份量的參考標準
- **[Librsvg 收到第一個 AI slop PR](https://viruta.org/librsvg-ai-slop.html)** — 老牌開源專案 Librsvg 收到了第一個明顯由 AI 產生的低品質 PR，開源維護者的新日常
- **[Cord: 協調 AI Agent 樹狀結構的新框架](https://www.june.kim/cord)** — 66 分的 HN 討論，提出用樹狀結構來協調多個 AI agent，解決 agent 之間打架的問題
- **[Go 核心團隊討論如何處理 AI 產生的程式碼變更](https://groups.google.com/g/golang-dev/c/4Li4Ovd_ehE/m/8L9s_jq4BAAJ)** — Go 語言的開發者在 golang-dev 上認真討論 AI 生成 CL 的品質問題，這個討論本身就是時代的縮影

---

## 🏄 深水區

- **[Tim O'Reilly – Why AI Needs Us](https://timoreilly.substack.com/p/why-ai-needs-us)** — Tim O'Reilly 論述為什麼 AI 的發展離不開人類的判斷和引導，不是反 AI，是提醒我們別把方向盤放掉
- **[The Future of Math Research in the Age of AI](https://siliconreckoner.substack.com/p/the-future-of-math-research-in-the)** — 當 AI 開始能做數學研究時，數學家的角色會怎麼變？這篇深入探討了 AI 對純粹學術研究的衝擊
- **[Opinion: How to Solve AI's 'Jagged Intelligence' Problem](https://undark.org/2026/02/19/opinion-jagged-intelligence/)** — AI 的能力分布極度不均勻——有些事做得比人好十倍，有些事又蠢到不行，這篇分析了這個「鋸齒狀智能」問題的根源和可能的解法
- **[The AI security nightmare is here and it looks suspiciously like lobster](https://www.theverge.com/ai-artificial-intelligence/881574/cline-openclaw-prompt-injection-hack)** — The Verge 深度報導 AI coding 工具的 prompt injection 安全噩夢，用了一個很生動的龍蝦比喻來描述這場亂局
