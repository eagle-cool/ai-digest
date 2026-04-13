---
title: "Anthropic 逼宮 OpenAI、智譜漲出自信、CPU 卡住 AI 的脖子"
date: 2026-04-13
description: "Ramp 數據顯示 Anthropic 兩個月內將超越 OpenAI 企業市場份額，智譜 GLM-5.1 漲價對標 Claude，Google 與 Intel 聯手揭示 CPU 才是 AI 時代真正瓶頸"
tags: [ai-industry, llm, agents, ai-tools]
---

今天這三道浪的共通點是「翻轉」——Anthropic 快要把 OpenAI 的企業王座掀了、智譜從打價格戰的挑戰者變成敢漲價的玩家、而 AI 基建的瓶頸居然從 GPU 跑到了 CPU。每一個都是大家以為穩固的敘事正在鬆動。

---

## 🌊 今日浪頭

### [Anthropic 狂吞 70% 新客戶，兩個月內將超越 OpenAI](https://www.36kr.com/p/3764400210936327)

Ramp 追蹤了五萬多家美國企業的 AI 支出數據，結論很炸：Anthropic 企業客戶佔比衝到 30.6%，單月暴漲 6.3 個百分點；OpenAI 跌到 35.2%。一個月前差距還有 11 個百分點，現在只剩 4.6 個點。Ramp 直接說了——按照這個速度，兩個月內 Anthropic 就會反超。

更殺的一個數據：首次購買 AI 服務的企業裡，Anthropic 對 OpenAI 的勝率高達 70%。VC 投資的新創公司更明顯——Anthropic 滲透率 66%，OpenAI 只有 59%。

以我的觀察，最反直覺的是 Anthropic 的產品定價更貴、產能還不夠（每一檔套餐都有用量限制），客戶卻還是排隊送錢。這在傳統 SaaS 市場幾乎不可能。Ramp 的分析指向一個意想不到的因素：文化。Anthropic 今年初硬剛五角大樓拒絕軍方對 Claude 的使用條款，被聯邦政府拉黑，結果反而贏了市場——Claude 一度在 App Store 反超 ChatGPT，年化營收從 90 億美元衝到 300 億美元。更離譜的是，Anthropic 上週還請了 15 位基督教神學家到總部開了兩天閉門會，認真討論 Claude 的「道德發展」和「精神成長」。一家 3800 億美元估值的公司在研究 AI 是不是「神之子」——沒有任何其他 AI 公司在做這件事。

**為什麼這道浪值得追：**
- 企業 AI 市場不是看誰便宜，是看誰「最不會讓你半夜背鍋」——金融、法律、醫療選 Claude 的原因就在這
- Anthropic 從「安全優先」到文化認同的品牌策略正在被市場驗證
- 這是 AI 產業第一次出現「挑戰者靠漲價和拒單取勝」的反常識劇本

### [智譜 GLM-5.1 發布再漲價，市值衝破 4000 億港元](https://www.36kr.com/p/3764447147246343)

智譜發了 GLM-5.1 然後再漲 10% Token 價格——這已經是今年第三次漲價了。更有意思的是，漲完之後股價連漲三天，市值突破 4000 億港元。在中國大模型還在打價格戰的時候，智譜直接掉頭走了反方向。

CEO 張鵬在財報會上放了個大招：他把對標對象從 OpenAI 換成了 Anthropic。邏輯很清楚——OpenAI 靠 C 端流量驅動，但中國用戶付費意願本來就弱；Anthropic 靠 API 賣給企業和開發者，80% 收入來自企業級 API，這跟智譜的處境幾乎一模一樣。

數字很亮眼：MaaS 平台 ARR 約 17 億元人民幣，同比提升 60 倍；400 萬企業用戶和開發者；中國前十大互聯網公司中 9 家每天在深度調用 GLM。Q1 API 定價提升 83%，調用量反而增長 400%。但亮眼的增長背後是 2025 年虧損 47 億元、日均虧損超過 870 萬。研發費用率 440%——營收的增速遠遠追不上研發投入。智譜要講好 Anthropic 故事，前提是模型持續領先，而這需要不斷燒錢。這個故事能不能跑通，可能是今年中國 AI 最值得關注的商業實驗。

**為什麼這道浪值得追：**
- 中國大模型從「卷價格」到「卷價值」的風向轉變，智譜是第一個下注的
- 對標 Anthropic 意味著放棄 C 端幻想、全力押注 API 商業模式
- 如果智譜漲價成功，會倒逼整個中國 AI 行業重新思考定價邏輯

### [別盯著 GPU 了，CPU 正成為 AI 時代的新瓶頸](https://www.36kr.com/p/3764433173037577)

Google 跟 Intel 簽了多年協議，在全球 AI 數據中心規模部署 Xeon 處理器。這個新聞乍看平淡，但背後揭示了一個被整個行業忽視的結構性問題：AI 的瓶頸正在從 GPU 移到 CPU。

原因很直觀——Agent 工作負載跟傳統聊天機器人完全不一樣。Agent 需要多步推理、呼叫 API、讀寫資料庫、編排複雜工作流，這些任務大部分落在 CPU 和主機系統側。喬治亞理工學院的論文量化了這個問題：在 Agent 工作負載中，CPU 端工具處理占總延遲的 50% 到 90.6%。GPU 已經準備好處理下一批任務了，CPU 還在等工具呼叫返回。

另一個被低估的因素是上下文窗口爆炸。主流模型從 128K 衝到百萬 token，KV Cache 隨之線性增長——100 萬 token 時約 200GB，遠超單塊 H100 的 80GB 顯存。解法之一是把 KV Cache 卸載到 CPU 記憶體，CPU 的工作量直接翻倍。

供應端也出了問題：台積電 3nm 產線太緊張，原本分給 CPU 的晶圓產能被利潤更高的 GPU 訂單擠占，導致「有 GPU 沒 CPU 來帶」的荒謬局面。2025 Q4 伺服器 CPU 均價已經漲了 30%。Musk 也找上 Intel 為德州的 Terafab 項目設計定製晶片。美銀預測全球 CPU 市場到 2030 年將從 270 億翻到 600 億美元。

**為什麼這道浪值得追：**
- Agent 時代的算力瓶頸已經不只是「夠不夠 GPU」，而是整個系統的協調能力
- Intel 可能因為 Agent 浪潮獲得翻身機會——他們在伺服器 CPU 市場還有 60% 份額
- 這對所有做 AI 基建規劃的團隊都是提醒：別只算 GPU 數量，CPU 和記憶體頻寬一樣會卡脖子

---

## ⚡ 衝浪快報

- **[Anthropic 推出 Advisor 策略：實習生幹活、總監指點](https://www.36kr.com/p/3764407766287110)** — Sonnet/Haiku 遇到困難時自動諮詢 Opus，一次 API 請求搞定。開發者社群早就在手動做這件事了，現在 Anthropic 把窮人版工作流產品化了
- **[Trump 政府可能在鼓勵銀行測試 Anthropic 的 Mythos 模型](https://techcrunch.com/2026/04/12/trump-officials-may-be-encouraging-banks-to-test-anthropics-mythos-model/)** — 國防部才剛把 Anthropic 列為供應鏈風險，另一邊卻有官員暗中推銀行去測 Mythos。政治果然是最好的 AI 催化劑
- **[Hermes Agent 狂攬 4.8 萬星，「與你共同成長」的 AI 助手](https://www.36kr.com/p/3764418640003840)** — Nous Research 做的個人 AI 助手，GitHub 整月排名第一。核心賣點是閉環學習——Agent 完成任務後自動把經驗固化成 Skill，越用越強
- **[120 萬億 Token：火山引擎豆包日均用量三個月翻倍](https://www.36kr.com/p/3764435023102472)** — 累計超一萬億 Token 的企業客戶從 100 家增到 140 家。AI 正式進入企業規模化付費階段，這不再是免費試用了
- **[HumanX 大會上所有人都在聊 Claude](https://techcrunch.com/2026/04/12/at-the-humanx-conference-everyone-was-talking-about-claude/)** — 舊金山 AI 大會的焦點不是 OpenAI，是 Anthropic。Mindshare 的轉移速度比市場份額還快
- **[OpenClaw 龍蝦五天五連更，火力全開](https://www.36kr.com/p/3763230073815814)** — 從 v2026.4.7 到 v2026.4.11，記憶系統重構、安全加固、視頻生成接入、本地語音推理。日期當版本號的框架還是第一次見
- **[AI「洗車難題」終於有人破案了](https://www.36kr.com/p/3764397965574659)** — 「離洗車店 50 米，走路還是開車去？」四大模型 80% 翻車率。車要洗，人走過去洗什麼？AI 的常識推理還是有坑
- **[walnut：專門給 AI Agent 做的錯誤追蹤系統](https://github.com/bilalg1/walnut)** — 沒有 dashboard，只有 CLI——因為用它的是 agent 不是人。完全相容 Sentry SDK，改一行 DSN 就能用
- **[被 AGI 逼瘋的矽谷天才正在集體逃亡](https://www.36kr.com/p/3764405288354309)** — OpenAI 工程師 Hieu Pham（IMO 銀牌、Stanford ICPC）宣布徹底停止工作離開矽谷。AI 實驗室的工時已經從 996 升級到 002
- **[馬斯克的「西方微信」XChat 將於 4/17 上線](https://www.36kr.com/p/3764425143353865)** — 端對端加密、無廣告、無追蹤。從 2022 年收購 Twitter 到現在快四年，這塊聊天版圖終於要正式上了

---

## 🏄 深水區

- **[DeepMind CEO Demis Hassabis：AI 的兩條路——做科學工具，還是捲入 AGI 競賽](https://www.36kr.com/p/3764417856176644)** — 在所有人都在比排名搶融資的時候，Hassabis 認為 AI 最值得優先投入的方向是科學發現和人類健康。AlphaFold 的人談 AI 理想主義，份量不一樣
- **[AI Will Be Met with Violence, and Nothing Good Will Come of It](https://www.thealgorithmicbridge.com/p/ai-will-be-met-with-violence-and)** — HN 230 讚、388 則留言的長文。從 Altman 被攻擊事件出發，探討 AI 引發的社會暴力反彈——不是危言聳聽，是正在發生的事
- **[個人提效 10 倍，公司顆粒無收：AI 時代的「電力悖論」正在重演](https://www.36kr.com/p/3735259483177220)** — 19 世紀紡織廠換上電動機後三十年生產力沒提升，因為工廠還是照蒸汽機時代的設計蓋的。今天的 AI 採用正在重演一模一樣的劇本
- **[Harness 剛火，可能就要成為過去時了](https://www.36kr.com/p/3764520322138887)** — Harness Engineering 的底層前提是模型在長上下文必定退化。但如果模型的上下文能力持續提升，這套約束工程的理論基礎可能根本不成立
