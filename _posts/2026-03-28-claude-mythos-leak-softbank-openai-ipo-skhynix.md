---
title: "Claude Mythos 洩漏嚇壞 Anthropic、軟銀 400 億美元豪賭 OpenAI IPO"
date: 2026-03-28
description: "Anthropic 意外洩漏比 Opus 4.6 更強的 Claude Mythos 模型，因網安能力太強不敢發布；軟銀借 400 億美元押注 OpenAI IPO；SK hynix 計畫赴美上市終結 RAMmageddon 記憶體危機。"
tags: [llm, ai-industry, ai-safety, ai-tools]
---

今天 AI 圈的浪有點魔幻——Anthropic「手滑」洩漏了一個連自己都不太敢發布的超強新模型 Claude Mythos，結果全網搶著截圖；軟銀直接跟 JPMorgan 和高盛借了 400 億美元，就為了跟 OpenAI 這場豪賭 all in；SK hynix 則準備赴美上市，想用一場百億級 IPO 終結折磨整個產業的記憶體荒。今天的主題很明確：AI 的賭注越來越大，而且越來越真實。

---

## 🌊 今日浪頭

### [Claude Mythos 意外曝光：強到 Anthropic 自己都不敢發](https://www.36kr.com/p/3741093726634240)

Anthropic 這次「手滑」的規模有點誇張——不是洩漏一篇文件，而是 3000 多個未發布的內容資源（頁面、圖片、PDF）全部被丟在一個沒設權限的公共資料湖裡，被搜尋引擎直接索引。兩個資安研究員先發現的，一個來自資安公司，一個來自劍橋。

洩漏的核心是 Anthropic 已經訓練完成的下一代模型 **Claude Mythos**（內部代號 Capybara，水豚）。根據洩漏的草稿文件，Mythos 在軟體編程、學術推理和**網路安全**測試中都顯著超越 Opus 4.6。但最讓人倒吸一口涼氣的是——Anthropic 自己說這個模型的「黑客能力」太強，他們打算「比以往更慢、更漸進」地發布，先從一小批早期客戶開始。這不是謙虛，是真的怕。

想想看：編程能力讓模型「看懂系統」、推理能力讓它「規劃攻擊路徑」、網安能力讓它知道「漏洞在哪裡」——這三者組合起來就是一條完整的攻擊鏈。Anthropic 之前就披露過有國家背景的駭客用 Claude Code 滲透了約 30 家機構，現在 Mythos 比那個版本還強一個檔次。

**為什麼這道浪值得追：**
- 這是 AI 產業首次有廠商公開承認「模型太強不敢發」——安全不再是公關話術，而是真實的產品決策
- Mythos 被定位為比 Opus 更高的新層級，也更貴——Anthropic 正在打造一個分層更細的模型產品線
- 洩漏時機剛好碰上 Anthropic 推進 IPO，這個「意外」的公關效果其實相當微妙

### [軟銀借 400 億美元，押注 OpenAI 今年 IPO](https://techcrunch.com/2026/03/27/why-softbanks-new-40b-loan-points-to-a-2026-openai-ipo/)

軟銀向 JPMorgan、高盛和四家日本銀行借了 400 億美元的**無擔保貸款**，期限只有 12 個月——就是為了兌現它在 OpenAI 上個月 1100 億美元融資中承諾的 300 億美元投資。加上之前的投入，軟銀對 OpenAI 的總押注已經超過 600 億美元。

這筆交易最耐人尋味的是結構：無擔保、12 個月到期。華爾街的銀行家們不是慈善家，願意做這種交易只有一個原因——他們相信 OpenAI 年底前會 IPO，而且會是史上最大規模的上市之一。屆時軟銀可以靠 IPO 帶來的流動性輕鬆還債。這不是投資決策，這是對 IPO 時間表的一場巨額押注。

**為什麼這道浪值得追：**
- 400 億美元無擔保借款基本上等於華爾街在賭 OpenAI 年底 IPO——金融市場比任何分析師都誠實
- 軟銀累計 600 億美元押注 OpenAI，這個數字已經超過很多國家的年度科技預算
- 如果 OpenAI IPO 不成或延遲，軟銀 12 個月內要找到 400 億的再融資，孫正義又要上演高空走鋼索

### [SK hynix 赴美上市，要用百億 IPO 終結 RAMmageddon](https://techcrunch.com/2026/03/27/memory-chip-giant-sk-hynix-could-help-end-rammageddon-with-blockbuster-us-ipo/)

全球 HBM（高頻寬記憶體）的絕對霸主 SK hynix 已經秘密向美國 SEC 遞交了 F-1 表格，目標今年下半年在美上市，預計募集 100 至 140 億美元。這不只是一場 IPO——它可能是解決整個 AI 產業「記憶體荒」的關鍵一步。

背景是所謂的「RAMmageddon」——AI 對記憶體的需求暴增導致全球供應緊缺，DRAM 漲 80-95%，HBM 漲超 170%，連消費者的電腦和手機都被波及。Nature 預估這場危機至少持續到 2027 年。SK hynix 的 CEO 在 3/25 股東大會上直接說了：要攢 750 億美元現金來支撐長期投資，包括 2050 年前在龍仁投入 4000 億美元建半導體群聚。

昨天我們聊的 Google TurboQuant 是軟體端的解法——壓縮記憶體用量；今天 SK hynix 赴美上市是硬體端的解法——擴大產能。這場 RAMmageddon 正在從兩端同時被攻克。

**為什麼這道浪值得追：**
- SK hynix 赴美上市可能帶動三星也跟進，整個韓國晶片業要搬家了
- 募來的錢直接砸向 ASML EUV 光刻機和新廠——79 億美元的 ASML 訂單已經簽了
- 記憶體是 AI 基建的真正瓶頸，比 GPU 更隱蔽但影響更廣——你手機漲價的元兇就在這裡

---

## ⚡ 衝浪快報

- **[Anthropic 砸開 IPO 大門：3800 億美元估值，衝刺全球第二大 IPO](https://www.36kr.com/p/3740899535844096)** — 上面 Mythos 洩漏是技術面，這邊是資本面：Anthropic G 輪估值 3800 億美元，計畫募資超 600 億——OpenAI 不是唯一在衝 IPO 的
- **[Anthropic 告贏川普政府，法院勒令撤銷國防部限制令](https://techcrunch.com/2026/03/26/anthropic-wins-injunction-against-trump-administration-over-defense-department-saga/)** — 聯邦法官裁定川普政府對 Anthropic 的國防部限制違法，必須撤銷——Anthropic 最近運勢真的很旺
- **[智元機器人突破一萬台量產，搶在特斯拉前面](https://www.36kr.com/p/3740987466399753)** — 距離上次宣布 5000 台才一個季度就翻倍，中國人形機器人賽道的量產速度已經不是 PPT 等級了
- **[蘋果首款 AI 硬體曝光，長得像 AI Pin 但依附 iPhone](https://www.36kr.com/p/3740685687321351)** — AirTag 大小的穿戴裝置，給 Siri 加「眼睛」——但必須靠 iPhone 才能活，這是配件不是產品
- **[蘋果終於想通：iOS 27 將開放 Siri 接入 ChatGPT、Gemini、Claude](https://www.36kr.com/p/3740759301046274)** — 多年自研無果後全面開放，任何 AI 服務都能透過 App Store 接入 Siri——AI 版 App Store 的雛形浮現了
- **[蘋果砸數十萬美元留人，防 OpenAI 挖走 iPhone 設計團隊](https://www.36kr.com/p/3740654994440453)** — 每人最高 40 萬美元 RSU 特別獎金——OpenAI 搞硬體的野心大到讓蘋果緊張
- **[GitHub 大改 Copilot 規則：4/24 起預設拿你的程式碼訓練 AI](https://www.36kr.com/p/3740652375916805)** — 不主動退出就等於同意，還搬出 Anthropic 當擋箭牌說資料會交給他們——個人版用戶要注意了
- **[Meta 同一天裁 700 人又給高管發 9 億美元激勵](https://www.36kr.com/p/3741078319857927)** — 企業文化的精分時刻：樓下發遣散費、樓上發股票——元宇宙團隊首當其衝
- **[美國 AI 沙皇 David Sacks 卸任](https://techcrunch.com/2026/03/26/david-sacks-is-done-as-ai-czar-heres-what-hes-doing-instead/)** — 川普政府第一任 AI 政策掌門人走了，下一站離華盛頓權力中心更遠了
- **[字節 Seedance 2.0 死磕影片生成「不可能三角」](https://www.36kr.com/p/3740655324525062)** — Sora 死了、Seedance 接棒，但模型規模、生成時長、推理速度三者仍難兼得——字節在啃硬骨頭
- **[Claude Code 上線雲端自修 bug 功能，PR 自己綠了](https://www.36kr.com/p/3740796239921411)** — 52 天 73 個產品的更新頻率，Claude Code 現在能自動幫你修 CI 失敗——程式設計師離合法摸魚又近一步

---

## 🏄 深水區

- **[林俊旸離開千問後首發萬字長文：AI 正從「推理式思維」邁向「智能體思維」](https://www.36kr.com/p/3740825962135558)** — 前阿里千問技術負責人的離職首文不談八卦，直接丟出一套 AI 下一階段的技術框架——從 Reasoning 到 Agentic Thinking 的轉向，讀完會重新理解為什麼所有大廠都在瘋 Agent
- **[Simon Willison：用 M5 MacBook Pro 搭配 LLM Vibe Coding SwiftUI App](https://simonwillison.net/2026/Mar/27/vibe-coding-swiftui/#atom-everything)** — Simon 拿到 128GB M5 後嫌 Activity Monitor 太爛，直接用 vibe coding 搓了幾個替代工具——過程記錄完整，是理解「AI 輔助開發到底長什麼樣」最好的實戰案例之一
- **[Karpathy 破防：寫程式碼 AI 沒門檻了，但部署環節真的難](https://www.36kr.com/p/3740793369624585)** — Karpathy 公開吐槽 AI Coding 的真正瓶頸不是生成程式碼，而是部署那一堆服務——身為過來人，深有同感
- **[Science 封面：AI 的過度順從正在削弱人類的自我反思能力](https://www.36kr.com/p/3740676705599494)** — 斯坦福和 CMU 的研究發現，AI 聊天機器人幾乎永遠站在你這邊，結果是你越來越不會反思——這篇論文讓我對自己跟 AI 互動的方式產生了不小的警覺
