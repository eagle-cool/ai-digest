---
title: "付了 15 億美元盜版罰款的 Anthropic，轉頭指控中國 AI「偷竊」"
date: 2026-02-25
description: "Anthropic 指控 DeepSeek、月之暗面和 MiniMax 對 Claude 發動「工業級蒸馏攻擊」，但這家靠盜版書籍訓練起家的公司，真的有資格當 AI 時代的版權警察嗎？一場關於 AI 知識邊界、地緣政治與產業壟斷的深度剖析。"
tags: [deep-dive, llm, ai-industry, ai-research, ai-safety]
---

## 引言

2025 年 9 月，Anthropic 掏出 15 億美元和解金，為自己從盜版網站 LibGen 下載數百萬本書籍來訓練 Claude 的行為買單。這是 AI 產業有史以來最大的版權和解案，[金額之巨，甚至差點讓這家公司破產](https://www.npr.org/2025/09/05/g-s1-87367/anthropic-authors-settlement-pirated-chatbot-training-material)。

五個月後，2026 年 2 月 24 日，同一家公司在官方部落格和 X 平台上義正辭嚴地宣布：我們抓到中國人偷東西了。

Anthropic 指控 DeepSeek、月之暗面（Moonshot AI）和 MiniMax 三家中國 AI 實驗室，[透過約 24,000 個虛假帳號、超過 1,600 萬次交互，對 Claude 進行「工業級規模的蒸餾攻擊」](https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks)。他們聲稱，這些公司系統性地提取 Claude 在推理、工具調用和程式撰寫方面的核心能力，用來訓練和改進自己的模型。

馬斯克第一時間在 X 上反諷：「絕了，他們怎麼敢偷 Anthropic 從人類程式設計師那裡『偷』來的東西？」AI 評論家 Gary Marcus 則直言這是「肆無忌憚的盜賊抱怨自己被搶劫了」。

這不只是一場企業之間的口水戰。當你拉開距離看，會發現這起事件觸及了 AI 時代最根本的幾個問題：AI 模型的輸出到底算不算知識產權？蒸餾技術的法律邊界在哪裡？以及——一家靠「偷」起家的公司，有沒有資格定義什麼是「偷」？

這篇報導的起點是[智東西的報導](https://www.36kr.com/p/3697136714739330)，但我想帶你看到更完整的圖景。

---

## 事件全貌

### Anthropic 的指控：精確到個位數的「罪證」

Anthropic 在官方部落格中詳細描述了三家中國 AI 實驗室的「蒸餾攻擊」行為，數據精確得像是一份檢察官的起訴書。

**MiniMax** 是三者中規模最大的「嫌疑犯」，貢獻了超過 1,300 萬次交互，主要針對 Claude 的 agentic coding 和工具調度能力。Anthropic 還特別提到一個細節：[當他們發布新模型時，MiniMax 在 24 小時內就切換了攻擊目標](https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks)，顯示出高度的組織性和即時性。

**月之暗面**（Moonshot AI）進行了超過 340 萬次交互，聚焦於 agentic 推理、工具使用、程式撰寫與資料分析、computer-use agent 開發以及電腦視覺。

**DeepSeek** 的規模相對較小，約 15 萬次交互，主要針對基礎邏輯與對齊能力，特別是「繞過審查的政策敏感查詢替代方案」。

三家實驗室的操作模式有幾個共同特徵：使用所謂的「九頭蛇叢集」（hydra clusters），同時操控數萬個帳號，將請求分散到不同的 API 金鑰和雲端供應商；透過代理服務繞過地理限制；腳本化的長對話被設計來提取詳細的逐步回答，結構與正常使用模式明顯不同。

Anthropic 聲稱已經加強了偵測和防禦機制，包括建立流量模式識別與行為指紋系統、加強帳號驗證流程，並正在開發模型層面的反蒸餾技術。

### 值得注意的時機

這份指控的發布時機耐人尋味。就在幾週前，[OpenAI 也向美國國會提交了公開信](https://www.investing.com/news/stock-market-news/openai-accuses-deepseek-of-distilling-us-models-to-gain-advantage-bloomberg-news-reports-4504138)，聲稱觀察到「DeepSeek 持續嘗試蒸餾 OpenAI 及其他美國前沿實驗室的模型」的跡象。兩大美國 AI 巨頭在同一時期、對同一批中國公司發出類似指控，很難不讓人聯想到協同的產業策略。

更巧的是，這些指控恰好出現在美國國內激烈辯論是否放鬆對華 AI 晶片出口管制的時刻。2026 年 1 月，[川普政府將 NVIDIA H200 等先進晶片的出口審查從「推定拒絕」改為「逐案審查」](https://www.mayerbrown.com/en/insights/publications/2026/01/administration-policies-on-advanced-ai-chips-codified)，這讓 Anthropic CEO Dario Amodei 公開抨擊這是一個「重大錯誤」，將帶來「難以置信的國安影響」。

而在 [OpenRouter 平台上，中國模型已經佔據了 61% 的 token 消耗量](https://wealthari.com/chinese-ai-models-capture-majority-of-openrouter-token-volume-as-minimax-m2-5-surges-to-the-top/)。MiniMax M2.5 單週創下 2.45 兆 token 的使用記錄，Kimi K2.5 緊隨其後。這些模型的價格是 Claude 的十分之一到二十分之一，正在全球開發者社群中快速搶佔市場。

Anthropic 選在這個節點公開指控，是巧合，還是一步精心計算的棋？

---

## 脈絡

### 蒸餾：一項誕生於 2015 年的合法技術

要理解這場爭議，得先搞清楚「蒸餾」到底是什麼。

2015 年，圖靈獎得主 Geoffrey Hinton 與 Google 的 Oriol Vinyals、Jeff Dean 聯合發表了經典論文 [《Distilling the Knowledge in a Neural Network》](https://arxiv.org/abs/1503.02531)，正式建立了知識蒸餾的理論框架。核心概念很直觀：用一個大型「教師模型」的輸出來訓練一個小型「學生模型」，讓學生不只學到正確答案，還學到教師對不同答案的「信心分佈」——Hinton 稱之為「暗知識」（dark knowledge）。

打個比方：傳統的機器學習訓練像是讓學生只看標準答案的「對或錯」，而蒸餾讓學生看到老師批改試卷時的思考過程——「這題答案是 A，但 B 也有 30% 的可能性，C 完全不對」。這種細膩的概率分佈包含了大量關於問題本質的資訊，讓小模型能以遠低於從零訓練的成本，達到接近大模型的表現。

這項技術被廣泛應用，而且各家 AI 實驗室自己也在大量使用。Anthropic 在自己的部落格中坦言：「蒸餾本身是一種廣泛應用且合法的技術，許多前沿實驗室都會用更強大的模型訓練體量更小、成本更低的模型版本。」OpenAI 的 GPT-4o mini、Google 的 Gemini Flash、Meta 的 Llama 系列——幾乎所有主要的小型化模型都是透過某種形式的蒸餾產生的。

所以問題不在於蒸餾本身，而在於：**用別人家的模型來蒸餾，算不算犯規？** 這裡有一個關鍵的區分：用自己的大模型蒸餾自己的小模型，是公認合法的工程實踐；但用競爭對手的模型輸出作為訓練資料，就進入了一個法律和倫理都模糊不清的灰色地帶。

### OpenAI 的先例：一場沒有下文的指控

Anthropic 不是第一個對中國 AI 實驗室提出蒸餾指控的公司。

2025 年初，當 DeepSeek 的 R1 模型以極低的研發成本震驚全球時，OpenAI 迅速跳出來聲稱掌握了 DeepSeek 蒸餾其模型的「證據」。Sam Altman 向美國眾議院特別委員會提交備忘錄，稱觀察到「與 DeepSeek 員工相關的帳號正在開發繞過 OpenAI 存取限制的方法」。

但有趣的是，Altman 在 DeepSeek R1 發布時曾公開稱讚這是一個「令人印象深刻的模型」，而且後來也[明確表示「沒有計畫起訴 DeepSeek」](https://www.scmp.com/tech/tech-war/article/3297248/openais-altman-says-no-plans-sue-chinas-deepseek)。為什麼？因為一旦走法律程序，OpenAI 自身的訓練資料來源也會被攤在陽光下接受審視——那可不是什麼好看的畫面。

這個先例很重要。它告訴我們，美國 AI 公司對蒸餾指控的態度是：在社群媒體上聲量要大，在法庭上動作要小。因為這場遊戲裡，沒有人的手是乾淨的。

### Anthropic 的 15 億美元「原罪」

要完整理解 Anthropic 指控的荒謬性，必須回顧他們自己的「黑歷史」。

2025 年，多位美國作家發起了 Bartz v. Anthropic 集體訴訟，指控 Anthropic 在訓練 Claude 系列模型時，從盜版網站 LibGen 和 Sci-Hub 的鏡像站下載了至少 500 萬本受版權保護的書籍。這不是從合法管道購買的電子書——而是直接從地球上最大的盜版圖書館批量下載。

Anthropic 曾試圖用「合理使用」原則為自己辯護，聲稱將書籍用於 AI 訓練是一種「轉換性使用」。但法官明確裁定：如果資料從一開始就是透過非法手段取得的，後續的使用不能再以「合理使用」來豁免。[據法律分析師估算，如果官司打到底，Anthropic 面臨的罰金可能高達數十億美元，「足以讓公司破產」](https://legalblogs.wolterskluwer.com/copyright-blog/the-bartz-v-anthropic-settlement-understanding-americas-largest-copyright-settlement/)。

最終，Anthropic 以 15 億美元達成和解，覆蓋約 50 萬部作品，平均每本書的「贖身價」約 3,000 美元。作為和解條件，Anthropic 還被要求銷毀所有從盜版管道取得的訓練資料。

這是 AI 領域有史以來金額最大的版權和解案。它把 Anthropic 這家一直以「AI 安全與倫理」領軍者自居的公司，永遠地釘在了「竊取資料」的耻辱柱上。

### Dario Amodei 的一貫立場

要理解 Anthropic 的行為，不能不看其 CEO Dario Amodei 的政治傾向。

Amodei 長期以來是美國 AI 圈中最鮮明的「對華鷹派」。他曾公開將中國共產黨描述為[「通往 AI 賦能極權主義噩夢的最清晰路徑」](https://darioamodei.com/post/on-deepseek-and-export-controls)。在 2026 年 1 月川普放寬晶片出口管制後，Amodei [公開抨擊這是「重大錯誤」](https://siliconangle.com/2026/01/20/anthropic-boss-dario-amodei-slams-trump-crazy-decision-sell-advanced-ai-chips-china/)，並主張美國應該利用出口管制來「維持和強化 AI 領導地位」。

在這次蒸餾指控的部落格中，Anthropic 明確將蒸餾與出口管制掛鉤，聲稱「大規模蒸餾可能削弱美國的技術領先優勢」，呼籲「強化出口管制的合理性」。

這不是一個普通的商業糾紛聲明，這是一份政策遊說文件。[甚至有 Anthropic 的研究員因為不認同公司的對華立場而選擇離職](https://elephas.app/blog/ai-researcher-quits-anthropic-over-china)。

---

## 多方觀點

### 馬斯克和科技圈：「賊喊捉賊」

對 Anthropic 指控最猛烈的反擊，來自了一個意想不到的方向——Elon Musk。

馬斯克的反諷精準且致命：「他們怎麼敢偷 Anthropic 從人類程式設計師那裡『偷』來的東西？」他進一步補充：「Anthropic 已經犯有大規模竊取訓練資料的罪行，他們必須為其盜竊行為支付數十億美元的賠償金。這就是事實。」

考慮到 xAI 和 Anthropic 是直接競爭對手，馬斯克的動機當然不純粹。但他的論點確實擊中了要害——Anthropic 的道德制高點建立在流沙之上。

知名科技部落客 Gergely Orosz 也發表了類似看法：「抱歉，Anthropic 不能兩面討好。別忘了 Claude 是怎麼訓練出來的——用的是受版權保護的書籍，直到被起訴後才向版權方付費。」

AI 訓練平台 Prime Intellect 的工程師 Will Brown 則提出了一連串尖銳的問題：使用 Claude 貢獻的開源 GitHub 程式碼來訓練模型，算不算蒸餾？把 Claude 的輸出公開分享到網路上，違不違反使用者協定？用 Claude Code 寫訓練程式碼來訓練競爭模型呢？

這些問題目前沒有明確答案。但它們暴露了 Anthropic 邏輯的根本矛盾：如果 Claude 的輸出在被發布到公共網路後成為了「可被抓取的資料」，那麼其他模型在訓練時「間接」包含了 Claude 生成的內容，到底算不算蒸餾？

### 法律界：灰色地帶一片

從法律角度看，模型蒸餾的合法性至今沒有定論。這可能是 AI 時代最大的法律真空之一。

[Fenwick 律師事務所的分析](https://www.fenwick.com/insights/publications/deepseek-model-distillation-and-the-future-of-ai-ip-protection)指出，美國版權局和大多數法院的立場是：缺乏充分人類創造性輸入的 AI 輸出通常不受版權保護。這意味著，Claude 的輸出本身可能不具有版權保護資格，用它來訓練其他模型在版權法框架下不一定構成侵權。

AI 公司目前主要依賴**服務條款**（ToS）而非版權法來禁止蒸餾。OpenAI、Anthropic、Mistral 和 xAI 都在使用者條款中加入了嚴格的「反競爭蒸餾」條款。但服務條款的約束力與版權法完全不同——[違反 ToS 是合同糾紛，不是刑事犯罪](https://www.winston.com/en/insights-news/is-ai-distillation-by-deepseek-ip-theft)。違反服務條款最多是民事責任，而 Anthropic 卻試圖把它包裝成類似於「工業間諜」的國安威脅。

[柏克萊大學法律學院的一篇分析](https://sites.law.berkeley.edu/thenetwork/2025/03/30/the-innovation-dilemma-ai-distillation-in-openai-v-deepseek/)更進一步指出了「創新困境」：如果嚴格禁止蒸餾，可能會扼殺技術創新和知識流動；但如果完全放任，又會破壞前沿研發的經濟激勵。現有的法律框架——無論是版權法、專利法還是商業秘密法——都無法完美適用於 AI 蒸餾這個全新的場景。

這正是為什麼 Anthropic 選擇在社群媒體上「公審」而非在法庭上起訴。在法律框架下，他們能做的頂多是封禁帳號和追討違約賠償——這遠不如在輿論場上把事情上升到「國家安全威脅」來得有效。正如一位 Reddit 使用者精準的評論：「蒸餾不違法，即便違法，Claude 本身也是非法構建的。這就是為什麼 Anthropic 向政府抱怨，而不是直接起訴。」

### 被指控的三家中國公司

截至目前，DeepSeek、MiniMax 和月之暗面均未對 Anthropic 的最新指控做出正式回應。

但歷史上的回應提供了一些線索。DeepSeek 在 2025 年的 Nature 論文中曾澄清，[其基座模型使用的資料全部來自公開網路，雖然可能包含 GPT-4 生成的結果，但「絕非有意而為之，更沒有專門的蒸餾環節」](https://www.36kr.com/p/3697136714739330)。

月之暗面 CEO 楊植麟則針對 Kimi K2.5 曾自稱 Claude 的現象做過解釋：這是因為預訓練階段對最新程式碼資料進行了上取樣，而這些資料與「Claude」這個 token 的關聯性較強。值得一提的是，Claude Sonnet 4.6 也曾出現自稱 DeepSeek 的情況——當你的訓練資料來自整個網路，這種「身份錯亂」幾乎是不可避免的。

### 我的看法

說實話，在這場爭議裡，我覺得雙方都不完全乾淨，但 Anthropic 的姿態特別讓人反感。

不是說蒸餾行為可以被一概而論地正當化。如果真的有公司透過數萬個虛假帳號系統性地提取競爭對手的模型能力，這確實違反了服務條款，平台進行封禁和技術防禦完全合理。

但 Anthropic 的問題在於——他們不只是在做商業防禦，而是在做政治操作。把一個本質上是「違反服務條款」的商業糾紛，包裝成「國家安全威脅」和「強化出口管制的論據」，這已經不是在維護自身權益，而是在借題發揮，試圖利用地緣政治緊張來打壓競爭對手。

更諷刺的是，Anthropic 自己的「原罪」——從盜版網站下載數百萬本書籍來訓練模型——其性質遠比 API 蒸餾嚴重得多。前者是直接的版權侵犯，後者在法律上連定性都困難。用一句 Reddit 使用者的話：「你去餐廳吃飯，記住了廚師的味道，回家自己做了一頓飯，就被扣上『非法蒸餾攻擊』的帽子。」

AI 產業的真正問題，不在於誰偷了誰，而在於整個產業都建立在一種「先佔先贏、事後買單」的邏輯上。先拿了再說，被抓到再付錢。Anthropic 付了 15 億美元，算是為自己的「原罪」買了一張贖罪券。但贖罪券不是道德免罪符——你不能一邊擦著偷吃的嘴，一邊義正辭嚴地指責別人白嫖。

---

## 產業衝擊

### 第一層：AI 模型的「護城河」焦慮

Anthropic 的指控，本質上暴露了閉源 AI 模型最深層的焦慮：**模型的智慧一旦通過 API 釋出，就很難阻止別人學習它**。

傳統軟體的知識產權保護相對清晰——你可以保護原始碼、演算法、專利。但 AI 模型的「智慧」存在於它的輸出中，而輸出是公開的。每一次 API 調用，都相當於讓教師公開授課。你可以在合約上禁止學生錄影，但你無法阻止他們記住課堂內容。

這對閉源模型的商業模式是一個根本性挑戰。如果蒸餾無法被有效阻止，那麼投入數十億美元訓練前沿模型的經濟邏輯就會被動搖。為什麼要花大錢做最強的模型，如果競爭對手可以用你的模型輸出來快速追趕？

Anthropic 的回應是雙管齊下：技術上加強反蒸餾機制，政治上推動出口管制。但技術手段永遠是道高一尺魔高一丈，而政治手段的副作用是——一旦你把商業競爭升級為國家安全議題，局面就會失控。

而且，把中國模型的進步全部歸因於蒸餾，本身就是對這些實驗室研發能力的嚴重低估。DeepSeek 在 V3 上展現的 MoE（Mixture of Experts）架構創新、MiniMax 在多模態上的突破、月之暗面在長上下文視窗上的工程進展——這些都不是靠蒸餾 Claude 的 API 輸出就能學到的。把所有能力提升都歸因於「抄近路」，要嘛是無知，要嘛是故意的。

### 第二層：開源 vs. 閉源的分水嶺

這場爭議正在加深 AI 產業中開源與閉源陣營之間的鴻溝。

一個被廣泛引用但少有人深入分析的事實是：[Andreessen Horowitz（a16z）的合夥人 Martin Casado 估計，約 80% 使用開源技術堆疊的年輕 AI 公司，現在都在使用中國製造的模型](https://wealthari.com/chinese-ai-models-capture-majority-of-openrouter-token-volume-as-minimax-m2-5-surges-to-the-top/)。MiniMax M2.5 的 API 定價是每百萬 input token 0.30 美元、每百萬 output token 1.10 美元，而 Claude Opus 4.6 是 5 美元和 25 美元——差距高達 10 到 20 倍。

如果你是一個預算有限的新創公司，你會選哪個？這不是一道需要思考的題目。

Anthropic 把蒸餾問題上升到國家安全層面，某種程度上也是在為自己的定價模式辯護。如果便宜又好用的中國模型被貼上「用偷來的技術打造」的標籤，那客戶在選擇時就會多一層顧慮。這是一種非常精明的市場策略——用地緣政治焦慮來創造人為的競爭壁壘。

### 第三層：出口管制的新戰線

Anthropic 在部落格中明確提出，蒸餾攻擊「強化了出口管制的合理性」。這不是隨口一提——這是 Anthropic 一貫政策遊說策略的延續。

[Dario Amodei 在 2026 年 1 月公開抨擊川普政府放寬 H200 晶片出口管制的決定](https://siliconangle.com/2026/01/20/anthropic-boss-dario-amodei-slams-trump-crazy-decision-sell-advanced-ai-chips-china/)，但他的遊說未能阻止政策轉向。現在，蒸餾指控為他提供了新的彈藥：看吧，即使你限制了晶片出口，中國公司還是可以通過蒸餾來獲取前沿能力。所以不僅要限制硬體，還要限制軟體和 API 存取。

這個邏輯一旦被接受，影響將是巨大的。它意味著 AI 服務可能被納入出口管制的範疇——不僅僅是晶片，連 API 調用都可能需要審查。這將徹底改變全球 AI 產業的競爭格局，把一個原本開放的技術生態變成一個以國籍劃界的分裂市場。

### 第四層：開發者生態的連鎖反應

如果 Anthropic 的邏輯被推到極致，最受傷的可能不是中國的 AI 實驗室，而是全球的獨立開發者。

想想 Will Brown 提出的那些問題：用 Claude 寫的程式碼算不算蒸餾？用 Claude 產生的資料做研究呢？如果 Claude 的輸出被視為不可用於訓練的「受保護資產」，那整個 AI 輔助開發的工作流程都可能被牽連。

目前，全球大量的開源程式碼是用 AI 工具輔助撰寫的，包括 Claude Code 和 GitHub Copilot。這些程式碼被上傳到 GitHub 後，成為公共語料庫的一部分。如果 Anthropic 堅持其對蒸餾的廣義定義，那麼任何使用這些「被 Claude 污染」的程式碼的模型訓練，理論上都可能觸犯其邊界。

這是一條滑坡——但 Anthropic 已經站在坡頂，手裡拿著推的姿勢。

---

## 未來展望

### 短期（3-6 個月）：技術軍備競賽升級

可以確定的是，閉源模型公司會加速部署反蒸餾技術。Anthropic 已經宣布正在開發模型層面的反蒸餾機制——在不影響正常使用者體驗的前提下，降低模型輸出被用於訓練的價值。OpenAI 也會跟進。具體做法可能包括：在模型輸出中嵌入統計水印、對高頻自動化請求進行降級處理、或在回應中加入只有在被用於訓練時才會影響模型行為的隱性「毒藥」。

但這是一場注定不對稱的戰爭。防守方需要在每一個可能的漏洞上做到完美，而攻擊方只需要找到一個突破口。更何況，任何降低蒸餾價值的手段，都有可能同時降低正常使用者的體驗。如果 Claude 的回答為了防蒸餾而變得「含糊」或「有毒」，真正受害的是付費使用者，不是蒸餾者。

與此同時，真正有實力的 AI 實驗室——無論在美國還是中國——完全可以靠自己的研發能力追趕。DeepSeek V3.2 和 MiniMax M2.5 的技術進步，遠不是簡單的蒸餾能解釋的。

### 中期（6-18 個月）：法律框架的建立

兩條可能的路徑正在浮現：

**路徑 A：立法限制蒸餾。** 美國國會可能在出口管制法案中加入針對 AI 服務蒸餾的條款，這將是前所未有的——等於把「使用別人的 API 輸出」上升到與「出口敏感技術」同等的管制層級。Anthropic 顯然在推動這個方向。

**路徑 B：行業自律與合約機制。** AI 公司透過更嚴格的服務條款、更強的存取控制和行業間的情報共享來處理蒸餾問題，但不將其上升到國家安全層面。這條路徑更務實，但對閉源公司的保護力度較弱。

我認為最終的結果可能是兩者的混合——針對「有組織的工業級蒸餾」進行法律規範，但不會全面禁止正常的 API 使用和研究活動。不過鑒於目前的政治氛圍，路徑 A 的成分可能會多一些。

### 長期推演：誰在定義 AI 時代的規則？

把時間線拉長到三到五年，這場爭議指向了一個更根本的問題：**AI 時代的知識產權框架，最終會由誰來定義？**

目前的狀況是：AI 公司先跑起來，法律在後面追。Anthropic 先用盜版書訓練模型，事後付錢了事；中國公司先用蒸餾追趕能力，被抓到再處理。整個產業都在「先斬後奏」的灰色地帶中運作。

但灰色地帶不會永遠存在。當 AI 模型的經濟價值達到數千億美元級別時，清晰的法律框架將不可避免地被建立。問題是：這個框架會是由美國主導、服務於閉源巨頭利益的單邊規則？還是一個多邊協商、平衡創新與保護的全球共識？

### 給讀者的行動建議

**如果你是開發者**：密切關注你使用的 AI 工具的服務條款變化。如果你在用 Claude Code 或 Copilot 輔助開發，確保你理解你的程式碼在法律上的歸屬。開源社群可能需要建立新的標準，來標註和管理 AI 生成的程式碼。

**如果你是創業者**：不要把所有雞蛋放在同一個模型供應商的籃子裡。在中美 AI 分裂的趨勢下，多模型策略不只是技術選擇，更是風險管理。同時要注意，如果你的產品依賴特定模型的輸出作為訓練資料，法律風險正在升高。

**如果你是一般科技從業者**：這場爭議的核心不在於誰偷了誰，而在於 AI 時代的知識邊界正在被重新劃定。關注蒸餾、API 使用權限、AI 生成內容的版權歸屬這些議題——它們將直接影響你未來使用 AI 工具的方式和成本。

最後，我想說的是：當一家付了 15 億美元盜版罰款的公司站出來指責別人「偷竊」時，我們真正應該關注的不是他的控訴是否屬實，而是——在一個所有參與者都有「原罪」的產業中，誰有資格當法官？

答案可能是：沒有人。所以我們需要法律，不是輿論戰。

---

## 延伸閱讀

- [Anthropic 官方部落格：Detecting and Preventing Distillation Attacks](https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks)：Anthropic 對蒸餾攻擊的第一手描述，包括技術細節和每家實驗室的具體數據
- [NPR：Anthropic to pay authors $1.5 billion in settlement](https://www.npr.org/2025/09/05/g-s1-87367/anthropic-authors-settlement-pirated-chatbot-training-material)：Anthropic 盜版書籍和解案的完整報導，了解「原罪」的全貌
- [Fenwick：DeepSeek, Model Distillation, and the Future of AI IP](https://www.fenwick.com/insights/publications/deepseek-model-distillation-and-the-future-of-ai-ip-protection)：從法律角度分析模型蒸餾的知識產權問題，最清晰的法律框架解讀
- [Latent Space：AINews 分析](https://www.latent.space/p/ainews-anthropic-accuses-deepseek)：AI 社群對 Anthropic 指控的深度分析，包括產業反應和技術細節
- [Dario Amodei：On DeepSeek and Export Controls](https://darioamodei.com/post/on-deepseek-and-export-controls)：Anthropic CEO 對中國 AI 和出口管制的完整立場，理解其政治動機的必讀
- [Wealthari：Chinese AI Models Capture Majority of OpenRouter Token Volume](https://wealthari.com/chinese-ai-models-capture-majority-of-openrouter-token-volume-as-minimax-m2-5-surges-to-the-top/)：中國模型在 OpenRouter 上的市佔數據，量化中國模型對全球開發者生態的實際影響
- [SCMP：Anthropic's distilling charges expose AI training grey area](https://www.scmp.com/tech/tech-war/article/3344499/anthropics-distilling-charges-against-chinese-firms-expose-ai-training-grey-area)：南華早報從亞洲視角的分析，平衡報導中美雙方立場
- [Futurism：Anthropic Furious at DeepSeek for Copying Its AI](https://futurism.com/artificial-intelligence/anthropic-deepseek-copying-ai)：科技媒體對 Anthropic 雙重標準最直白的批評
