---
title: "Claude Mythos 太猛被封印、Anthropic 三百億反超 OpenAI"
date: 2026-04-08
description: "Anthropic 發布史上最強模型 Claude Mythos 但不敢公開，同時年營收飆破 300 億美元超越 OpenAI，DeepSeek 則悄悄上線雙模式暗示 V4 即將到來"
tags: [llm, agents, ai-tools, ai-industry, ai-research, ai-safety]
---

今天 AI 圈的浪是真的猛——Anthropic 一天丟了兩顆炸彈，一顆是強到自己都不敢公開的 Claude Mythos，另一顆是年營收 300 億美元直接超車 OpenAI。然後 DeepSeek 在沒有任何公告的情況下，悄悄在網頁端上線了雙模式，V4 的影子已經很清楚了。

---

## 🌊 今日浪頭

### [Project Glasswing: Securing critical software for the AI era](https://www.anthropic.com/glasswing)

Anthropic 今天發布了他們迄今為止最強的模型 Claude Mythos Preview——然後告訴你：不好意思，這個不賣。

我仔細看了一下，這不是行銷話術。Mythos 在幾週內就找到了**數千個零日漏洞**，涵蓋每一個主流作業系統和瀏覽器。其中有一個 OpenBSD 的漏洞藏了 27 年——OpenBSD 可是以安全聞名的系統；還有個 FFmpeg 的漏洞存在了 16 年，自動化測試工具跑了五百萬次都沒抓到，Mythos 一眼就看穿了。更猛的是，它自主發現並串聯了 Linux kernel 的多個漏洞，從普通用戶權限一路提升到完全控制。

**為什麼這道浪值得追：**
- Mythos 在 CyberGym 漏洞重現測試拿下 83.1%，Opus 4.6 只有 66.6%；SWE-bench Pro 更是 77.8% 對 53.4%，差距不是擠牙膏而是代差
- AWS、Apple、Google、Microsoft、NVIDIA、CrowdStrike 等 12 家巨頭組成 Project Glasswing 聯盟，Anthropic 砸 1 億美元 credits + 400 萬美元捐贈給開源安全組織
- 這件事的意義在於：AI 找漏洞的能力已經超越絕大多數人類，攻守天平正在傾斜，誰先用 AI 加固防線誰就佔上風

### [Anthropic ups compute deal with Google and Broadcom amid skyrocketing demand](https://techcrunch.com/2026/04/07/anthropic-compute-deal-google-broadcom-tpus/)

Anthropic 的年化營收從 2025 年底的 90 億美元，三個多月內飆到 300 億美元——233% 的增長，直接超越 OpenAI 的 250 億。這個數字讓我看了三遍確認沒看錯。

同時他們跟 Google 和 Broadcom 簽下了 3.5 GW 的 TPU 算力大單，2027 年上線。上次的協議才 1 GW 多，這次直接翻了好幾倍。背後的邏輯很簡單：Claude 的企業客戶需求爆炸了，超過 1,000 家企業年花費超過百萬美元。

**為什麼這道浪值得追：**
- 一家沒有 ChatGPT 級消費者入口的公司，靠企業端和 API 就把營收做到全球獨立 AI 公司第一，這完全顛覆了「C 端才是王道」的敘事
- $380B 估值、$30B Series G——Anthropic 現在的體量已經不是 startup，而是跟 Google Cloud、AWS 平起平坐的算力買家
- 3.5 GW 算力是什麼概念？大約等於一座中型核電廠的輸出，AI 軍備競賽的規模已經到了能源等級

### [DeepSeek 大升級，V4 真的不遠了](https://www.36kr.com/p/3757399317283593)

DeepSeek 最 DeepSeek 的操作來了——沒有發布會、沒有 blog、連推文都沒發，就在網頁端悄悄加了兩個圖標：閃電（快速模式）和鑽石（專家模式）。

我試了一下，差異是真實的。物理模擬任務上，專家模式的表現明顯優於快速模式，球的彈跳軌跡更符合物理直覺。數學推理也是，專家模式會一步一步把推導過程寫出來，快速模式就直接給答案。從各種跡象來看，快速模式背後跑的是 V4 Lite，專家模式則路由到更大的模型——很可能就是 V4 的某個形態。

**為什麼這道浪值得追：**
- 前端代碼被逆向後還發現了第三個「Vision 模式」，DeepSeek 的多模態佈局正在浮出水面
- 更重要的是，DeepSeek 開始做產品分層了——這是邁向商業化的第一步，免費到底不是可持續的商業模式
- V4 正式版據報四月亮相，屆時大概率仍是開源最強，但差距可能不會是碾壓級的

---

## ⚡ 衝浪快報

- **[Intel signs on to Elon Musk's Terafab chips project](https://techcrunch.com/2026/04/07/intel-signs-on-to-elon-musks-terafab-chips-project/)** — Intel 加入 Musk 的德州 Terafab 晶片廠計畫，聯手 SpaceX 和 Tesla。Intel 要靠代工翻身，Musk 要自己造 AI 晶片，雙方各取所需
- **[GPT-4o 之母 Joanne Jang 宣布離開 OpenAI](https://www.36kr.com/p/3756573443588609)** — 在 OpenAI 待了四年半，親手塑造 4o 人格的靈魂工程師走了。繼 CFO 內訌、COO 轉任之後，OpenAI 的人才流失問題越來越嚴重
- **[Meta 員工每天燒掉兩萬億 Token](https://www.36kr.com/p/3756573545693703)** — Zuckerberg 下令用 AI 重寫代碼庫，8.5 萬員工瘋搶「Token Legend」稱號，排行榜第一名一個月燒了 2810 億 Token。這是內捲還是創新？我傾向前者
- **[Testing suggests Google's AI Overviews tells millions of lies per hour](https://arstechnica.com/google/2026/04/analysis-finds-google-ai-overviews-is-wrong-10-percent-of-the-time/)** — 測試顯示 Google AI Overviews 的錯誤率高達 10%，換算下來每小時產出數百萬條錯誤資訊。搜尋引擎的信任基石正在被 AI 侵蝕
- **[國產大模型稱霸 OpenRouter：前十佔六席](https://www.36kr.com/p/3756517273895689)** — 小米 MiMo-V2-Pro 以 4.82 萬億 Token 調用量登頂全平台第一，中國模型在全球開發者市場的存在感已經不容忽視
- **[Neuralink 腦晶片新突破：ALS 患者用意念說話](https://www.36kr.com/p/3756553842885127)** — 不只是打字，是直接用「原聲」與人交流。腦機介面從科幻走向臨床的速度比想像中快
- **[三星單季利潤暴漲 755%](https://www.36kr.com/p/3756590863991305)** — Q1 利潤 57.2 萬億韓元，95% 來自記憶體。HBM 的需求有多瘋狂？看三星的財報就知道了，AI 軍備競賽的最大贏家可能是賣鏟子的
- **[Netflix 發布視頻模型：不只擦除，而是重寫物理世界](https://www.36kr.com/p/3756719276835586)** — 移除影片中的物體後，模型會推演「如果這個物體從未存在過」場景會怎樣。因果推理能力用在影片編輯上，Netflix 這個切入點很聰明
- **[Anthropic 封殺 OpenClaw，龍蝦絕境爆發](https://www.36kr.com/p/3756316944925445)** — Anthropic 切斷免費接口後，OpenClaw 48 小時內上線原生視頻生成和「睡眠記憶」系統，還切換到 GPT-5.4。開源社群的韌性永遠不要低估
- **[Claude Code 越更越廢？AMD AI 負責人甩出 23 萬次調用記錄](https://www.36kr.com/p/3756572218376964)** — 思考深度從 2200 字元暴跌到 560 字元，降幅 67%。這不是體感問題，是有數據佐證的退化。Anthropic 需要認真面對這個信任危機

---

## 🏄 深水區

- **[GLM-5.1: Towards Long-Horizon Tasks](https://simonwillison.net/2026/Apr/7/glm-51/#atom-everything)** — Z.ai 放出 754B 參數的 GLM-5.1，MIT 授權，已上 OpenRouter。如果你對開源大模型的天花板在哪裡感興趣，這篇值得花時間讀
- **[OpenAI CFO: Not Ready for IPO](https://www.wheresyoured.at/openai-cfo-news/)** — OpenAI CFO 親口說公司還沒準備好上市，擔心營收增長撐不住支出承諾。在 Anthropic 營收反超的背景下讀這篇，別有一番滋味
- **[第一批用 AI 的人，已經染上了 AI 疲憊症](https://www.36kr.com/p/3756409475969539)** — Token 大爆炸時代，不燒十幾萬 Token 都不好意思說自己懂 AI。但工具越強大，人卻越焦慮越疲憊，這個悖論值得每個 AI 重度使用者反思
- **[AI 邪修時刻：Meta 聯手 MIT「投毒」訓練反而讓模型變強](https://www.36kr.com/p/3756290083799815)** — 用 67% 錯誤率的數據訓練模型，結果推理能力反而提升。這篇論文顛覆了「數據品質至上」的常識，對 RL 訓練方法論有重要啟示
