---
title: "Opus 4.7 自審程式碼、Codex 反撲桌面、黃仁勳硬戰 TPU"
date: 2026-04-17
description: "Claude Opus 4.7 帶著 /ultrareview 上線、OpenAI Codex 直接殺進你的桌面、黃仁勳 103 分鐘專訪不避 TPU 問題——今天 AI 圈三波大浪同時打來。"
tags: [llm, agents, ai-coding, ai-tools, ai-industry]
---

今天的浪有點猛——Anthropic 和 OpenAI 幾乎同一天砸出重磅更新，一個丟出 Opus 4.7 還配上能讓 AI 審自己程式碼的 `/ultrareview`，另一個則把 Codex 直接送進你的 Mac 桌面，開始點來點去。中間黃仁勳還抽空上了 Dwarkesh 的節目聊了 103 分鐘，把 TPU 威脅、2500 億美元供應鏈承諾、為什麼死都不做雲服務一次講清楚。AI Coding 的戰場今天真的是火光四射。

---

## 🌊 今日浪頭

### [AI可以自审代码了，Opus 4.7出手解决"屎山"](https://www.36kr.com/p/3770156143493892)

我認真讀完 Opus 4.7 的公告後第一反應是：Anthropic 這次玩的不是「我比你強」，而是「我故意弱一點給你看」。官方直接講這是「第一款用來測試新網路安全護欄的公開模型」，訓練時還實驗性地削弱了網安能力——因為上週剛宣布的 Mythos Preview 強到不敢公開。跑分當然有進步（SWE-Bench Verified 從 80.8% 拉到 87.6%、SWE-Bench Pro 從 53.4% 直上 64.3%），但真正的戲肉是 Claude Code 同步新增的兩個功能：`auto mode` 幫你處理低風險權限決策、`/ultrareview` 開一個專門的會話審 AI 自己寫的程式碼。

**為什麼這道浪值得追：**
- 指令遵循變「太聽話」反而會讓舊提示詞壞掉——Opus 4.7 現在會嚴格按字面執行，以前被模型自動忽略的小細節現在會被認真當回事，升級前務必重測提示詞。
- 價格沒變（輸入 $5/M、輸出 $25/M）但新 tokenizer 會讓相同輸入吃掉 1.0–1.35 倍的 token，加上強思考模式會想更久，實際帳單很可能變貴——現在買的不是一次回答，而是一整個會思考會試錯的任務過程。
- `/ultrareview` 把 AI Coding 推進下一階段：從「AI 寫程式」進化到「AI 審自己的程式」。Claude Code 補上第二雙眼睛後，寫＋審的閉環基本成形，這大概就是多數工程師日常用 Claude Code 的標準流程。

### [OpenAI takes aim at Anthropic with beefed-up Codex that gives it more power over your desktop](https://techcrunch.com/2026/04/16/openai-takes-aim-at-anthropic-with-beefed-up-codex-that-gives-it-more-power-over-your-desktop/)

Anthropic 才剛把 Claude Code 吹成 AI Coding 霸主，OpenAI 隔沒幾週就把 Codex 大改版丟回去。這次最猛的是 Codex 可以在你 Mac 背景執行，打開任何 app、用滑鼠點擊、用鍵盤輸入，而你還能同時用自己的機器做別的事。這幾乎是 Claude 和 Cowork 上個月剛推的遠端操控 Mac 功能的正面翻版，OpenAI 這次沒再裝矜持，直接貼臉開打。

**為什麼這道浪值得追：**
- Codex 現在內建瀏覽器、可以跨前端遊戲開發用例操作 web app，還加了 111 個外掛整合（CodeRabbit、GitLab Issues 等），連看 Slack 加 Google Calendar 幫你排待辦都包辦——Codex 不只是 coding 工具，而是要當企業工作流樞紐。
- 新增的「memory」功能讓 Codex 跨會話記得你怎麼工作；這個特性和 Opus 4.7 強化的檔案系統記憶方向一致，看來兩家都認為 agent 從「聰明臨時工」升級到「穩定同事」的關鍵是長期記憶。
- TechCrunch 一句話點破現實：「Claude Code has been dubbed the tool of choice for many businesses」——OpenAI 這次是追擊而不是炫技，背後的焦慮藏不住。

### [黄仁勋最新深度专访：英伟达的护城河、TPU威胁与生态建设](https://www.36kr.com/p/3770191914959624)

黃仁勳上 Dwarkesh 的節目 103 分鐘，被劈頭就問：「你們根本只是在寫軟體，晶片給台積電做、內存給 SK 海力士、組裝給 ODM，如果軟體被 AI 商品化，你會不會也被商品化？」他的回答很黃仁勳：「輸入是電子，輸出是 Token，中間是輝達。」這場訪談我覺得是這個月最值得完整看一遍的產業訪談，他把供應鏈、TPU 威脅、為什麼死都不做雲端一次講清楚。

**為什麼這道浪值得追：**
- 他承認 Claude 和 Gemini 都在 TPU 上訓練，但他不慌——輝達的賣點是「加速運算」不是「張量處理」，AI 只是其中一塊，新的注意力機制、SSM、擴散＋自回歸融合都需要可編程的底層，ASIC 鎖死一種算法很快會被超車。
- SemiAnalysis 爆出的 2500 億美元供應鏈承諾他沒否認，反而點出真正讓他睡不著的瓶頸是「能源政策」——因為建電網比建晶圓廠還久，這也解釋了為什麼輝達死命優化每瓦效能。
- 被問到為什麼不直接做超大規模雲端跳過中間商時他直接了斷：一旦變成 hyperscaler 就跟現有雲客戶變競爭關係，自毀生態。這是對照 OpenAI、Anthropic 最近動作看特別有意思的一段。

---

## ⚡ 衝浪快報

- **[Factory hits $1.5B valuation to build AI coding for enterprises](https://techcrunch.com/2026/04/16/factory-hits-1-5b-valuation-to-build-ai-coding-for-enterprises/)** — 企業級 AI 編碼新創 Factory 募到 1.5 億美元、估值衝上 15 億，Khosla 領投；當 Claude Code 和 Codex 已經互相對打，還能卡進企業級市場的獨角獸值得關注。
- **[Physical Intelligence says its new robot brain can figure out tasks it was never taught](https://techcrunch.com/2026/04/16/physical-intelligence-a-hot-robotics-startup-says-its-new-robot-brain-can-figure-out-tasks-it-was-never-taught/)** — Physical Intelligence 丟出 π0.7，號稱能執行沒被訓練過的任務；機器人 foundation model 這把火越燒越旺。
- **[OpenAI starts offering a biology-tuned LLM](https://arstechnica.com/science/2026/04/openai-starts-offering-a-biology-tuned-llm/)** — OpenAI 推出首款專給生物學工作流的 GPT-Rosalind，命名致敬 Rosalind Franklin，垂直領域模型戰爭開打。
- **[Gemini can now create personalized AI images by digging around in Google Photos](https://arstechnica.com/ai/2026/04/gemini-can-now-create-personalized-ai-images-by-digging-around-in-google-photos/)** — Gemini Nano Banana 2 直接翻你相簿生成個人化圖像，Google 把個人資料當武器用這招只有它們敢玩。
- **[Google's AI Mode update lets you open links without leaving the page](https://www.theverge.com/tech/913109/google-ai-mode-tabs-sources)** — Chrome AI Mode 加了側邊預覽，點連結不用離開對話；小功能但透露搜尋正在從「連結導流」變成「答案原地讀完」。
- **[超30亿，中国迄今最大具身智能融资诞生](https://www.36kr.com/p/3768920808391176)** — 它石智航 Pre-A 輪吞下 4.5 億美元，高瓴、紅杉、美團並肩下注，創下中國具身智能單輪紀錄，這邊的機器人熱度一點都不輸美國。
- **[InsightFinder raises $15M to help companies figure out where AI agents go wrong](https://techcrunch.com/2026/04/16/insightfinder-raises-15m-to-help-companies-figure-out-where-ai-agents-go-wrong/)** — Agent 觀測與故障診斷新創募到 1500 萬美元，這個賽道開始熱是因為真的有人開始在生產環境被 agent 搞出事。
- **[Upscale AI in talks to raise at $2B valuation](https://techcrunch.com/2026/04/16/upscale-ai-in-talks-to-raise-at-2b-valuation-says-report/)** — 成立七個月估值衝 20 億美元的 AI 基礎設施公司，不看業績看題目的投資邏輯現在是常態。
- **[Anthropic CPO leaves Figma's board after reports he will offer a competing product](https://techcrunch.com/2026/04/16/anthropic-cpo-leaves-figmas-board-after-reports-he-will-offer-a-competing-product/)** — Mike Krieger 退出 Figma 董事會，原因是 Anthropic 要做設計工具競品；SaaSpocalypse 這次是真刀真槍的版本。
- **[Cloudflare's AI Platform: an inference layer designed for agents](https://blog.cloudflare.com/ai-platform/)** — Cloudflare 推 Agent 專用推論平台，主打邊緣部署和低延遲；基礎建設層也在為 agent 時代重寫。
- **[Canva's AI assistant can now call various tools to make designs for you](https://techcrunch.com/2026/04/16/canvas-ai-assistant-can-now-call-various-tools-to-make-designs-for-you/)** — Canva AI 2.0 上線，AI 助理會自己呼叫工具做可編輯稿；Figma 是不是該緊張看今天這組新聞就懂。
- **[Runway CEO says AI could help Hollywood make 50 films instead of one $100M blockbuster](https://techcrunch.com/2026/04/16/runway-ceo-says-ai-could-help-hollywood-make-50-films-instead-of-one-100m-blockbuster/)** — Runway CEO 說 AI 會讓好萊塢從拍一部億元大片改拍 50 部，這個比喻比數字有說服力。

---

## 🏄 深水區

- **[What I learned this week — Pretraining parallelisms, distillation, cyber equilibrium](https://www.dwarkesh.com/p/what-i-learned-april-15)** — Dwarkesh 自己的一週學習筆記，從預訓練平行化、蒸餾能不能被擋、Mythos 事件後的資安平衡到 pipeline RL；當一個每天採訪頂尖研究者的人願意寫下他學到什麼，這種副產品比正餐還香。
- **[Qwen3.6-35B-A3B on my laptop drew me a better pelican than Claude Opus 4.7](https://simonwillison.net/2026/Apr/16/qwen-beats-opus/)** — Simon Willison 拿自己的鵜鶘騎腳踏車基準測試，讓 Alibaba Qwen 3.6 和今天剛發的 Opus 4.7 同台，結果本機跑的 Qwen 贏了；開源追上閉源的真實溫度計就是這種小玩意。
- **[AI安全得查祖宗三代？Anthropic登Nature揭秘大模型潜意识传染](https://www.36kr.com/p/3769362609783560)** — Anthropic 登 Nature：模型可以透過看起來無害的數字序列「遺傳」隱藏偏好甚至失對齊傾向，意思是你訓練時挑的資料血統不乾淨會出事；AI 安全的邊界又被往外推了一格。
- **[We gave an AI a 3 year retail lease and asked it to make a profit](https://andonlabs.com/blog/andon-market-launch)** — Andon Labs 把 Claude Sonnet 4.6 推上 CEO 位，10 萬美金加三年實體零售店合約，看 AI 能不能真的活下來；這種「別寫報告，直接開店」的評測形式比跑分誠實一百倍。
- **[算力通胀元年：DeepSeek越便宜，这轮涨价越难停](https://www.36kr.com/p/3770191910208001)** — DeepSeek 把推理成本壓到近零，中國三大雲同一週卻集體漲價 20–30%；這篇把「成本下降卻漲價」的結構性矛盾拆得很清楚，看完你會對今年算力市場的動向有完全不同的直覺。
