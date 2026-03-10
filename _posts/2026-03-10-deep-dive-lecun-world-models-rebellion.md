---
title: "當 AI 教父押注十億美元反叛 LLM：世界模型之戰開打"
date: 2026-03-10
description: "圖靈獎得主 Yann LeCun 離開 Meta、痛批 LLM 是死胡同，帶著 10 億美元創辦 AMI Labs 要用「世界模型」取代大型語言模型。這不只是技術路線之爭，更是 AI 產業未來十年方向的豪賭。"
tags: [deep-dive, llm, ai-research, ai-industry]
---

## 引言

想像一下這個場景：你是 AI 領域最受尊敬的科學家之一，圖靈獎得主，在全球最大的科技公司領導 AI 研究超過十二年。然後有一天，你的老闆請來一個二十九歲、沒有研究經驗的年輕人當你的上司，告訴你要「加速」——你會怎麼做？

Yann LeCun 的答案是：走人，然後帶走十億美元來證明整個產業都走錯了方向。

2026 年 3 月 9 日，LeCun 共同創辦的 [AMI Labs 宣布完成 10.3 億美元融資](https://techcrunch.com/2026/03/09/yann-lecuns-ami-labs-raises-1-03-billion-to-build-world-models/)，估值達到 35 億美元。這家巴黎新創公司的目標不是打造更大的語言模型，而是要建造「世界模型」（World Models）——一種從真實世界學習物理法則、因果關係和空間邏輯的 AI，而不是只會預測下一個字的聊天機器人。

這不是一個普通的創業故事。這是 AI 產業最根本的路線之爭：當全世界都在瘋狂擴大 LLM 規模的時候，一位 AI 教父用真金白銀賭上自己的學術聲譽，說這條路是死胡同。不管他對不對，這場賭局的結果都將重塑整個 AI 產業的走向。

---

## 事件全貌

AMI Labs（Advanced Machine Intelligence Labs）的融資規模遠超最初的預期。2025 年 12 月公司剛曝光時，據 [Bloomberg 報導](https://www.bloomberg.com/news/articles/2026-01-19/yann-lecun-s-ami-labs-draws-investor-interest-from-cathay-hiro)原本只計劃募集 5 億歐元，結果最終到手 8.9 億歐元（約 10.3 億美元），幾乎翻倍。投資者搶著要進場，AMI Labs 反而有了挑選投資人的資本。

領投方包括 Cathay Innovation、Greycroft、Hiro Capital、HV Capital 和 Bezos Expeditions。戰略投資者的名單更是驚人：NVIDIA、Samsung、Sea、Temasek、Toyota Ventures，再加上 Eric Schmidt、Mark Cuban、Tim Berners-Lee 等個人投資者。NVIDIA 的參與尤其值得注意——這家 GPU 巨頭同時也是 LLM 生態系的最大受益者，但它顯然不想錯過世界模型這班車。

AMI Labs 的核心團隊堪稱豪華。LeCun 本人擔任執行主席，CEO 是前 Nabla 創辦人 Alexandre LeBrun，COO 是前 Meta 歐洲副總裁 Laurent Solly，首席科學家是 Saining Xie，首席研究官是 Pascale Fung，世界模型副總裁是 Michael Rabbat。四個據點分布在巴黎（總部）、紐約、蒙特婁和新加坡。

但最有趣的是 LeBrun 的一句話：「我預測『世界模型』將成為下一個流行詞。六個月後，每家公司都會自稱世界模型公司來募資。」他說這話時帶著笑容——因為他知道，大多數蹭概念的公司根本不是在做同一件事。

AMI Labs 的技術核心是 LeCun 在 2022 年提出的 [JEPA 架構](https://www.turingpost.com/p/lejepa)（Joint Embedding Predictive Architecture，聯合嵌入預測架構）。用最白話的方式解釋：LLM 的工作方式是看到前面的字，預測下一個字；JEPA 的工作方式是看到現在的世界狀態，預測下一個世界狀態——但不是在像素層面預測（那太昂貴了），而是在一個更抽象的「表示空間」中預測。它把原始輸入（比如影片畫面）壓縮成捕捉核心特徵的抽象表示，忽略無關的細節，然後學習這些表示之間的動態關係。

打個比方：LLM 就像一個只讀過書但從沒出過門的學者，它可以口若懸河地討論物理學，但讓它接一顆球它不知道該怎麼動。JEPA 更像一個嬰兒學習世界的方式——通過觀察事物如何運動、碰撞、消失和出現，建立一個內在的世界模型，然後用這個模型來預測和規劃。

這也解釋了為什麼 AMI Labs 明確表示短期內不會追求營收。LeBrun 說得很坦白：「AMI Labs 是一個非常有野心的項目，因為它從基礎研究開始。這不是那種三個月出產品、六個月有營收、十二個月做到一千萬 ARR 的典型應用型 AI 新創。」世界模型從理論到商業應用可能需要數年——這是一場基礎研究的長期戰役。

---

## 脈絡

要理解 LeCun 為什麼敢押上一切來反叛 LLM，得先理解他為什麼離開 Meta。

故事要從 2025 年 6 月說起。Mark Zuckerberg 以 140 億美元收購了 Scale AI 49% 的股權，並把 Scale AI 的創辦人 Alexandr Wang 請來擔任 Meta 的首席 AI 官，負責新成立的「超級智慧實驗室」（Superintelligence Labs，代號 TBD Lab）。這個 29 歲的年輕人突然成了 LeCun 的上司。

LeCun 的反應很直接。他在接受 [Financial Times 採訪](https://futurism.com/artificial-intelligence/meta-top-ai-scientist-reason-quit)時說：「你不能告訴一個研究員該做什麼。你當然更不能告訴像我這樣的研究員該做什麼。」他直接稱 Wang「年輕且缺乏經驗」，「對研究毫無經驗，不懂得如何從事研究」。

但衝突的根源不只是人事問題。LeCun 在 Meta 領導的 FAIR（Fundamental AI Research）實驗室曾是全球最頂尖的 AI 研究機構之一，但 Meta 在把研究成果轉化為產品方面一直不太成功。Zuckerberg 對此越來越不耐煩——特別是在 2025 年 4 月 Llama 4 發布後[被批為「到手即過時的失敗品」](https://futurism.com/artificial-intelligence/meta-top-ai-scientist-reason-quit)，還被指控操縱 benchmark。Zuckerberg「基本上對所有相關人員失去了信心」，開始大幅重組 AI 部門。

2025 年 5 月，FAIR 負責人 Joelle Pineau 離職。同年 10 月，[Meta 裁撤了約 600 個 AI 職位](https://www.rdworldonline.com/meta-cuts-600-ai-roles-months-after-reports-of-100m-offers-to-top-recruits/)，其中大量來自 FAIR。LeCun 眼看自己一手建立的研究帝國被拆解，終於在 11 月正式離開。

這個故事的諷刺之處在於：Meta 一邊裁撤研究團隊，一邊用上億美元的薪資從 OpenAI 和 Google 挖人來填充新的「超級智慧實驗室」。LeCun 對此的評價是：「很多人已經離開了，很多還沒離開的人也會離開。」

LeCun 對 LLM 的不滿由來已久。早在 2022 年，他就提出了 JEPA 架構，認為只靠預測下一個 token 永遠無法達到人類水準的智慧。他的核心論點是：LLM 產生一個 token 的計算量是固定的，這本質上是一種「反射式」的 System 1 思考，完全沒有推理能力。「一個 LLM 可以討論物理學，但它並不理解物理學；它可以談論因果關係，但它從未經歷過因果。」

2024 年的一篇研究甚至從數學上證明了 [LLM 無法學習所有可計算函數](https://creati.ai/ai-news/2026-01-26/ai-pioneer-yann-lecun-warns-tech-dead-end-llms/)，因此在作為通用問題求解器使用時必然會產生幻覺。這給了 LeCun 更多的理論彈藥。

---

## 多方觀點

### 世界模型陣營：「LLM 只是暖場」

LeCun 並不孤獨。2026 年初，世界模型突然從學術概念變成了投資熱點。Stanford 教授 Fei-Fei Li 的 [World Labs 在 2 月剛募了 10 億美元](https://techcrunch.com/2026/02/18/world-labs-lands-200m-from-autodesk-to-bring-world-models-into-3d-workflows/)，Autodesk 一家就投了 2 億。Google DeepMind 的 [Genie 3](https://introl.com/blog/world-models-race-agi-2026) 已經能以 24fps 生成可互動的 3D 環境。NVIDIA 的 Cosmos 平台已被下載超過 200 萬次。Waymo 用 DeepMind 的世界模型來模擬自駕場景——包括龍捲風、洪水和路上突然出現一頭大象。

LeCun 的態度很明確：「LLM 太有局限性了。擴大它們的規模不會讓我們」到達 AGI。他認為 LLM 的角色充其量是把抽象思維轉化成語言——它是 AI 系統的「嘴巴」，而不是「大腦」。

AMI Labs CEO LeBrun 則更務實地指出了 LLM 在醫療場景的致命缺陷：當 AI 的幻覺可能造成生命危險時，你需要的是一個真正理解世界如何運作的系統，而不是一個在文字遊戲中統計機率的模型。

### LLM 陣營：「把規模再推大一點」

但另一邊的陣營同樣強大，而且他們手上握著最有力的論據：實際成果。Anthropic CEO Dario Amodei 曾預測，到 2026 年我們就能在資料中心裡擁有「一個由天才組成的國家」——而這個願景完全建立在 LLM 的 scaling law 之上。OpenAI 正在繼續推進更大的模型，Google 的 Gemini 系列也在不斷迭代。

事實上，LLM 在過去兩年展現的能力提升是驚人的。Claude Opus 4.6 能解決 Donald Knuth 花了數週研究的數學開放問題。GPT-5.4 可以直接操控電腦。Cursor 用 LLM 驅動的 AI 編程工具已經做到了 20 億美元的年收入。這些不是實驗室裡的概念驗證，而是每天有數百萬人在使用的真實產品。

LLM 陣營的邏輯很簡單：你說 LLM 不能理解世界，但它已經在改變世界了。什麼時候 JEPA 能拿出同等級的實際應用？在科技產業，「理論上更好」和「實際上更有用」之間，往往隔著一個墳場的距離。

### 學術懷疑派：「先拿出成果再說」

值得注意的是，即使在支持世界模型方向的研究者中，也有人對 JEPA 持保留態度。批評者指出，[JEPA 在潛在空間而非觀察空間中進行監督](https://arxiv.org/html/2507.05169v1)，這帶來了一個風險：模型可能學到的是無意義的表示，而非真正的世界動態——所謂的「表示崩塌」問題。

更關鍵的是，JEPA 至今尚未在 NLP 或整合性 agent benchmark 上展示過決定性的突破。生成式模型已經打破了無數紀錄，而 JEPA 陣營能拿出手的，目前還只是理論上的優越性。「給我看突破性成果」——這是懷疑派最常說的一句話。

還有人指出，JEPA 雖然被包裝成全新的概念，但其核心思想——預測編碼、自動編碼器、能量模型——在機器學習領域已經存在了幾十年。這到底是範式革命，還是漸進式的重新包裝？

### 我的看法

以我的觀察，這場爭論的有趣之處在於：雙方可能都對，但對的時間尺度不同。

短期內（未來 2-3 年），LLM 仍然會是 AI 應用的主力。它們的生態系已經太龐大了，從 ChatGPT 到 Claude 到 Cursor，數十億美元的基礎設施和數百萬開發者都建立在 transformer 架構上。你不會因為 LeCun 說了一句「死胡同」就拆掉這一切。

但長期來看，LeCun 提出的問題是真實的：一個只會操作符號而不理解符號背後物理意義的系統，能走多遠？當 AI 需要操作真實世界——開車、做手術、控制機器人——純語言模型的局限就會暴露。世界模型不是要取代 LLM，而是要補上 LLM 永遠無法填上的那個洞。

---

## 產業衝擊

### 直接受影響者

最直接的影響在人才市場。LeCun 離開 Meta 不是孤立事件——FAIR 的大規模裁員和重組已經讓數百名頂級 AI 研究者流入市場。AMI Labs、World Labs 和其他世界模型新創正在吸收這些人才，形成一個與 LLM 生態系平行的新研究社群。

對 Meta 來說，這是一個戰略性的損失。FAIR 曾經是全球最受尊敬的 AI 研究機構之一，LeCun 是它的靈魂人物。Meta 選擇了「快速出產品」而犧牲了基礎研究的深度，短期可能看不出代價，但如果世界模型真的成為下一個範式，Meta 可能會發現自己又落後了——就像當年錯過移動端一樣。

更值得關注的是，這種人才流動正在重塑 AI 研究的地理版圖。AMI Labs 選擇巴黎作為總部，而非矽谷，這不是巧合。法國政府近年來對 AI 研究的支持力度不斷加大，加上歐洲相對寬鬆的研究環境，正在吸引越來越多的頂級研究者。如果 AMI Labs 成功，巴黎可能會成為世界模型研究的全球中心——這對長期以來由美國壟斷的 AI 研究格局是一個有趣的挑戰。

### 商業模式衝擊

世界模型的商業化路徑與 LLM 截然不同。LLM 的商業模式是 API 按 token 收費，但世界模型的計算需求是 [LLM 推論的 8-32 倍](https://introl.com/blog/world-models-race-agi-2026)。這意味著：

**GPU 需求將再次暴增。** NVIDIA 不管誰贏都是贏家——這也解釋了為什麼它同時投資 AMI Labs 和為 LLM 公司提供晶片。

**雲端服務需要重新設計。** 現有的 AI 推論基礎設施是為文本處理優化的，世界模型需要的是影像級別的即時運算能力，這將驅動新一輪的基礎設施投資。

**應用場景從「文字」轉向「物理」。** LLM 的殺手級應用是聊天和寫作，世界模型的殺手級應用會是自駕、機器人和工業模擬。這兩個市場的規模差距可能是數量級的。

### 開發者生態

對開發者來說，世界模型目前還太早期，不會立刻改變日常工作。但如果你在做以下領域的工作，現在就該開始關注：

- **機器人與自動化：** World Labs 的 Marble 已經能從文字生成可互動的 3D 環境，月費 $0-95。這對遊戲、VFX 和建築視覺化的開發者來說是即戰力。
- **自動駕駛：** Waymo 已經在用世界模型做模擬訓練，這個趨勢會擴散到整個自駕產業。
- **科學模擬：** 理解物理法則的 AI 對藥物發現、材料科學、氣候模型等領域有巨大潛力。

但對大多數做 web 開發、SaaS 產品或行動應用的開發者來說，世界模型短期內不會改變你的技術棧。你用 LLM 做的事情——寫程式、生成文案、分析數據——世界模型並不會做得更好。它們解決的是一個不同的問題集合。這也是為什麼我認為「LLM vs 世界模型」的敘事框架本身就有誤導性——這不是替代關係，更像是 CPU vs GPU：解決不同類型的問題，最終會被整合在同一個系統裡。

### 二階效應

最大的二階效應可能是心理層面的：LeCun 的出走和十億美元融資，給了整個產業一個「合法」的理由去質疑 LLM 至上主義。在此之前，質疑 LLM 的人往往被視為跟不上時代；現在，有一位圖靈獎得主帶著頂級團隊和十億美元說「我跟你們走不同的路」，這改變了整個對話的框架。

未來幾個月，我們可能會看到更多「世界模型」新創出現——就像 LeBrun 預言的那樣，很多只是蹭概念。但在噪音之下，真正的範式競爭已經開始了。

---

## 未來展望

### 短期（3-6 個月）

AMI Labs 會開始組建團隊和搭建計算基礎設施，不會有產品產出。World Labs 的 Marble 會繼續迭代，可能成為世界模型領域第一個被廣泛使用的產品。Google DeepMind 可能會讓 Genie 3 進入更廣泛的測試。

可以幾乎確定的是：「世界模型」會成為 2026 年下半年投資界的新寵，大量新創會湧現。同時，LLM 公司不會坐以待斃——OpenAI 和 Anthropic 很可能會宣布自己的「多模態理解」或「物理世界模型」計劃，試圖搶占敘事。

### 中期（6-18 個月）

情境一：AMI Labs 發布第一批基於 JEPA 的研究成果，在特定領域（如醫療影像、機器人操控）展現出明顯優於 LLM 的能力，引發更大規模的資本流入世界模型賽道。

情境二：LLM 的能力提升速度繼續超出預期，GPT-6 或 Claude 5 在推理和規劃能力上取得突破，讓世界模型的差異化優勢看起來沒那麼明顯。兩條路線進入共存狀態。

情境三：LeCun 選擇開源 AMI Labs 的研究成果（他已經承諾會這麼做），引發一波開源世界模型的浪潮，就像 Meta 當年用 Llama 改變了 LLM 的競爭格局一樣。

### 長期推演（3-5 年）

如果世界模型成功，我們可能會看到一個 AI 技術棧的分層化：LLM 負責語言和推理層，世界模型負責物理理解層，兩者結合成為真正的通用智慧系統。就像 LeCun 自己說的：「LLM 有一個小小的角色——把抽象思維轉化成語言。」他甚至預測：「那將是一個互動的機器社會⋯⋯如果一個系統行為不當，會有其他更聰明的 AI 系統把它拿下。」

這個未來如果實現，AI 對社會的影響將遠超我們現在的想像。LLM 改變的主要是知識工作——寫作、編程、分析。世界模型改變的將是物理世界的自動化——製造、運輸、醫療、建築。LeCun 說「AI 將對社會產生類似十五世紀印刷術的變革性影響」，如果世界模型成功，這個類比可能還太保守了。

如果失敗呢？LeCun 會成為 AI 歷史上最昂貴的逆行者——一位偉大的科學家，看到了正確的問題，但押注了錯誤的解法。歷史上這種案例並不罕見：很多人正確地指出了現有範式的局限，但提出的替代方案最終也沒有走通。不管結果如何，這場賭局本身就很值得尊敬：在所有人都往同一個方向跑的時候，敢停下來說「你們搞錯了」，這需要的不只是學術勇氣，還有把身家押上的膽量。

### 給讀者的行動建議

**如果你是開發者：** 不需要現在就轉向世界模型，但值得花時間理解 JEPA 的基本概念和世界模型的思維框架。如果你做的是機器人、3D、模擬相關的工作，World Labs 的 Marble 值得一試。

**如果你是創業者：** 世界模型的應用層幾乎是空白的——從工業模擬到教育，到遊戲世界生成，到科學研究輔助。但要注意，這個賽道的計算成本極高，起步門檻不低。

**如果你是一般科技從業者：** 最重要的是理解一件事：AI 的未來不一定是「更大的聊天機器人」。LeCun 可能對，也可能錯，但他提出的問題——「AI 需要理解世界，而不只是理解文字」——無論如何都值得認真思考。

AI 產業正站在一個分叉口。一邊是繼續沿著 LLM 的路走下去，靠規模解決一切；另一邊是從根本上重新思考 AI 應該如何理解世界。十億美元只是入場券——真正的賭注，是整個產業的下一個十年。

---

## 延伸閱讀

- [Yann LeCun's AMI Labs raises $1.03 billion to build world models — TechCrunch](https://techcrunch.com/2026/03/09/yann-lecuns-ami-labs-raises-1-03-billion-to-build-world-models/)：本文的起點，AMI Labs 融資的完整報導
- [Yann LeCun's new venture is a contrarian bet against large language models — MIT Technology Review](https://www.technologyreview.com/2026/01/22/1131661/yann-lecuns-new-venture-ami-labs/)：MIT 科技評論的深度分析，LeCun 為何認為 LLM 是錯誤的方向
- [Mark Zuckerberg's Former Top AI Scientist Reveals Exactly Why He Quit — Futurism](https://futurism.com/artificial-intelligence/meta-top-ai-scientist-reason-quit)：LeCun 離開 Meta 的內幕，與 Alexandr Wang 的衝突細節
- [AI Godfather calls Meta AI boss Alexander Wang 'inexperienced' — CNBC](https://www.cnbc.com/2026/01/05/ai-godfather-calls-meta-ai-boss-alexander-wang-inexperienced-.html)：LeCun 公開批評 Wang 的完整報導
- [World Models Race 2026: How LeCun, DeepMind, and others compete — Introl](https://introl.com/blog/world-models-race-agi-2026)：世界模型賽道的全面競爭分析，含技術比較
- [World Labs lands $1B from Autodesk to bring world models into 3D workflows — TechCrunch](https://techcrunch.com/2026/02/18/world-labs-lands-200m-from-autodesk-to-bring-world-models-into-3d-workflows/)：Fei-Fei Li 的 World Labs 融資和 Marble 產品進展
- [AI 'Godfather' Yann LeCun: LLMs Are Nearing the End — Newsweek](https://www.newsweek.com/nw-ai/ai-impact-interview-yann-lecun-artificial-intelligence-2054237)：LeCun 的完整訪談，關於 LLM 的局限和世界模型的願景
- [Critiques of World Models — arXiv](https://arxiv.org/html/2507.05169v1)：世界模型的學術批評，JEPA 的潛在問題分析
