---
title: "當醫生主動教 AI 取代自己：一個價值 170 億美元的矛盾產業"
date: 2026-02-19
description: "史丹佛急診醫師正在教 AI 如何診斷、開處方。她不是唯一一個——全球三萬多名專業人士正在領著高薪，親手訓練自己的替代者。這個產業值 170 億美元，但它能撐多久？"
tags: [deep-dive, ai-industry, agents, llm]
---

## 引言

想像你是一位在急診室裡工作了二十年的醫生。你見過數不清的創傷、做過無數次即時判斷、在凌晨三點靠直覺救回過很多條命。現在，有人給你一份時薪兩百美元的工作——教一台機器做你做了一輩子的事。

你會接嗎？

Alice Chiao 接了。這位史丹佛大學醫學院的前急診醫學教授，現在是 AI 訓練平台 Mercor 的數萬名專家之一。她的工作內容很直白：用自己二十年的臨床經驗，一題一題地教 AI 模型如何思考、診斷和開處方。她會丟出真實遇過的急診情境——從小孩發燒咳嗽到醫師看到的專業術語——然後給 AI 的回答打分數，告訴它哪裡安全、哪裡危險、哪裡會誤導病人。

這不是科幻小說的情節。這是 2026 年最炙手可熱的新型工作。

根據 Pitchbook 資深 AI 分析師 Dimitri Zabelin 的估計，這個被稱為「強化學習人類回饋」（RLHF）的產業，規模已經[至少達到 170 億美元](https://www.cnn.com/2026/02/17/business/ai-experts-training-jobs)。OpenAI、Google、Anthropic——幾乎所有 AI 前沿實驗室都在用 Mercor CEO Brendan Foody 口中的「大規模專家軍團」來打磨自己的模型。而 Mercor 每天付給這些專家的報酬，超過 150 萬美元。

但這裡有一個讓人坐立不安的問題：這些專業人士——醫生、律師、金融分析師、軟體工程師——他們到底是在「確保 AI 安全可靠」，還是在「親手訓練自己的替代者」？

這篇報導的起點是 [CNN 的一篇深度報導](https://www.cnn.com/2026/02/17/business/ai-experts-training-jobs)，但故事遠不止於此。

---

## 事件全貌

### Mercor：從大學生創業到百億美元帝國

故事要從三個高中辯論隊的隊友說起。Brendan Foody、Adarsh Hiremath 和 Surya Midha 曾在聖荷西的 Bellarmine 預備學校一起打政策辯論。2023 年，他們在聖保羅的一場黑客松上碰出了一個簡單的商業模式：幫企業媒合海外的技術人才，收一點佣金。九個月內，他們就做到了年營收 100 萬美元。

然後 AI 浪潮來了。

當 OpenAI、Anthropic 等公司開始砸錢找人做 RLHF——也就是讓真人專家來評判 AI 的回答品質，一遍又一遍地教它什麼是好、什麼是爛——Mercor 意識到自己手上那個從招聘平台累積來的[專業人才資料庫](https://techcrunch.com/2025/10/27/mercor-quintuples-valuation-to-10b-with-350m-series-c/)，就是 AI 實驗室最需要的東西。他們快速轉型，從幫人找工作變成幫 AI 找老師。

數字的成長曲線令人瞠目結舌。不到兩年時間，Mercor 的營收從年化 100 萬美元暴漲到超過 5 億美元。2025 年 10 月，由 Felicis Ventures 領投的 3.5 億美元 C 輪融資，讓公司估值一舉突破 100 億美元——是八個月前 B 輪 20 億美元估值的五倍。Forbes 隨即把 22 歲的 Foody 和他的兩位共同創辦人封為「[全球最年輕的白手起家億萬富翁](https://fortune.com/2025/11/12/brendan-foody-mercor-interview-ai-adarsh-hiremath-surya-midha-youngest-self-made-billionaires/)」——自 Mark Zuckerberg 23 歲上榜以來的最年輕紀錄。

### 專家們在做什麼？

Mercor 平台上超過三萬名專業人士的工作流程大致是這樣的：AI 模型會針對某個專業領域生成回答——比如一個病人的診斷建議、一份法律合約的條款分析、一個投資組合的風險評估。專家們會根據事先和同領域團隊共同制定的評分標準，逐條審閱這些回答，判斷它們是否準確、安全、有用。這些評分被回饋給模型，模型學習「追求高分」。

最搶手的專家領域依序是：軟體工程、金融、醫學、法律。但 Mercor 的觸角遠不止於此——從記者到汽車技師，從喜劇演員到品酒師，什麼都有。平均時薪 81 美元，資深領域專家可以拿到[每小時 200 美元以上](https://time.com/7322386/ai-mercor-professional-tasks-data-annotation/)，換算成全年大約 40 萬美元。

Mercor 也不是唯一的玩家。Meta 去年砸了 143 億美元投資 Scale AI，順便把其創辦人 Alexandr Wang 挖去當公司第一任[首席 AI 長](https://fortune.com/2025/06/22/inside-rise-scale-alexandr-wang-meta-zuckerberg-14-billion-deal-acquihire-ai-supremacy-race/)。Surge AI、Micro1 等競爭者也在這個領域快速成長，養出了一批新生代的年輕科技富豪。

---

## 脈絡

### 從肯亞血汗工廠到矽谷高薪：RLHF 的兩張面孔

要理解 Mercor 為什麼能爆發式成長，得先回溯 AI 訓練的黑暗史前時代。

早期的 AI 資料標註工作，長期被外包給開發中國家的低薪勞工。肯亞、菲律賓、委內瑞拉——這些國家有大量受過教育但找不到好工作的年輕人，成了 AI 訓練的隱形勞動力。根據 [CBS 60 Minutes 的調查報導](https://www.cbsnews.com/news/ai-work-kenya-exploitation-60-minutes/)，在肯亞替 OpenAI 做內容審核的工人，時薪只有 1.5 到 2 美元——而 OpenAI 付給外包商 Sama 的價格是每小時 12.5 美元。差價被層層中間商吃掉了。

更糟糕的是工作內容本身。這些工人被分配去審核 AI 訓練資料中最極端的內容——謀殺、兒童虐待、性暴力。一名肯亞工人告訴記者：「我發現哭比說話更容易。」另一名工人說這份工作毀了他的婚姻。2024 年 3 月，Scale AI 旗下的 Remotasks 平台突然關閉了肯亞業務，數千名依賴平台生存的年輕人一夜之間失去收入。約 200 名工人已經[對 Sama 和 Meta 提起訴訟](https://privacyinternational.org/explainer/5357/humans-ai-loop-data-labelers-behind-some-most-powerful-llms-training-datasets)。

但 AI 模型變得越來越聰明以後，簡單的「對/錯」標註已經不夠了。模型需要的不再是判斷「這張圖是不是貓」，而是判斷「這個法律建議是否準確」「這個診斷路徑是否安全」「這段程式碼的架構是否合理」。這種判斷，只有真正的領域專家才做得了。

這就是 Mercor 模式崛起的底層邏輯：**當 AI 從識別圖片進化到模擬專業判斷，訓練它的人也必須從低薪標註員升級為高薪領域專家。**

### 二月風暴：當華爾街突然認真了

2026 年二月的頭兩週，幾件事密集發生，讓「AI 取代白領工作」從遙遠的預言變成了眼前的恐慌。

首先是 Anthropic 在 2 月 3 日推出了 [Claude Cowork](https://www.cnn.com/2026/02/04/investing/us-stocks-anthropic-software)——一個可以像同事一樣讀文件、整理資料夾、起草文件的 AI 工具，並且附帶針對法律、金融、銷售等特定產業的外掛。消息一出，軟體股血流成河。Thomson Reuters 單日暴跌 15.83%，創下史上最大單日跌幅；LegalZoom 跌了 19.68%；Goldman Sachs 的美國軟體股指數[單日下跌 6%](https://www.cnbc.com/2026/02/06/ai-anthropic-tools-saas-software-stocks-selloff.html)，是自關稅風暴以來最慘的一天。整個板塊一週內蒸發了近一兆美元市值。

接著，AI 創業者 Matt Shumer 在社群媒體上發表了一篇〈[Something Big Is Happening](https://techstartups.com/2026/02/14/something-big-is-happening-why-the-viral-ai-essay-is-capturing-82-million-views-and-sparking-global-anxiety/)〉的文章，把 AI 對工作的衝擊比喻成 2020 年二月的新冠疫情——「所有人都還在聳肩，但加速已經開始了」。這篇文章在 X 上獲得超過 8000 萬次瀏覽，3.6 萬次轉發，引爆了全球性的焦慮討論。

在這個背景下，CNN 報導了 Chiao 醫師和 Mercor 的故事。一個急診醫師主動教 AI 做她的工作，在 2026 年二月的氛圍裡，這已經不只是一則產業新聞——它成了一個時代的隱喻。

---

## 多方觀點

### 樂觀派：「AI 是助手，不是替代者」

Chiao 醫師自己的說法代表了一大群專業人士的立場。她告訴 CNN：「醫生被選出來，是因為我們真心想幫助人。想治癒、想花時間傾聽。我不想把它看成 AI 搶我們的工作，我想把它看成 AI 接手那些讓我們無法當好醫生的事情——填表格、寫病歷、讀影像。」

這個「AI 是工具不是威脅」的敘事，也是 Mercor CEO Foody 主推的論述。他把 AI 訓練框架成一個讓人類更有生產力的過程：「我們需要治癒癌症、解決氣候變遷。讓每個人的生產力提高十倍，會對社會進步帶來巨大的好處。」

從投資人的角度，Pitchbook 分析師 Zabelin 認為 Mercor 和競爭對手的高估值，反映了市場相信「人類回饋和專家測試將成為 AI 系統永久且不可或缺的一部分」。換句話說，AI 越聰明，就越需要聰明的人來把關。

### 悲觀派：「你們在挖自己的墳」

但批評者看到的是一幅完全不同的圖景。

ZeroHedge 的一篇分析文章直接用了〈[New Gig Economy Job: Train AI That Replaces You](https://www.zerohedge.com/markets/new-gig-economy-job-train-ai-replaces-you)〉這個標題。文中指出，這些合約工「知道自己在建造用來自動化自己領域的模型，但還是接了工作，因為短期收入比存在性焦慮更實際」。

Anthropic CEO Dario Amodei 的預測讓這個矛盾更加刺耳。他在 2025 年中公開警告：AI 可能在一到五年內[消滅 50% 的入門級白領工作](https://fortune.com/2025/05/28/anthropic-ceo-warning-ai-job-loss/)，並將失業率推高到 10% 至 20%。他甚至提出了「token 稅」的概念——要求 AI 公司將 3% 的營收交給政府，用於補償被取代的勞工。

Microsoft AI 負責人 Mustafa Suleyman 更激進，他在 2026 年 2 月預測，AI 在 [18 個月內就能達到「人類水準的表現」](https://fortune.com/2026/02/13/when-will-ai-kill-white-collar-office-jobs-18-months-microsoft-mustafa-suleyman/)，適用於「大多數、甚至所有」的專業任務。他點名了會計、法律服務、行銷和專案管理。

Klarna CEO Sebastian Siemiatkowski 則提供了一個來自第一線的案例。他公開表示自己「[比較站在 Dario 那一邊](https://fortune.com/2026/02/17/klarnas-ceo-dario-amodei-ai-white-collar-workforce-shrink-2030/)」，並計劃透過自然流動的方式，將 Klarna 的員工人數從不到 3,000 人在 2030 年前縮減到 2,000 人以下。

### 數據怎麼說？

這裡出現了一個有趣的矛盾。

根據 [TIME 的報導](https://time.com/7322386/ai-mercor-professional-tasks-data-annotation/)，Mercor 自己開發的專業任務基準測試顯示：GPT-4o（2024 年 5 月）在 200 個任務上的得分率只有 35.9%，而 GPT-5（2025 年 5 月）跳到了 64.2%——一年內幾乎翻倍。但即使是 GPT-5，也只在 200 個任務中的 2 個拿到了滿分。

OpenAI 自己的基準測試則顯示，專家評估者在 220 個任務中有 47.6% 的情況偏好 AI 的輸出——這意味著 AI 已經有將近一半的時間表現得和人類專家一樣好或更好。而且這個「勝率」在 2024 年 6 月到 2025 年 9 月之間翻了一倍以上。

但 Thomson Reuters 的一份 2025 年報告顯示，專業人士目前只是在「嘗試性地」將 AI 用於特定任務，如文件審閱。更令人意外的是，一項 METR 研究發現，軟體開發者使用 AI 輔助時，完成任務的時間反而[增加了 20%](https://fortune.com/2026/02/13/when-will-ai-kill-white-collar-office-jobs-18-months-microsoft-mustafa-suleyman/)。

以我的經驗來看，這些數據告訴我們的是：**AI 的能力正在以非線性的速度追趕人類專家，但距離全面取代還有一段距離——問題是，這段距離正在以月為單位縮短。**

### 我自己的看法

說實話，我覺得 Chiao 醫師的論述——「我在確保 AI 安全」——和 Foody 的論述——「我在讓人類更有生產力」——都不算錯，但都有一種刻意避開房間裡那頭大象的感覺。

那頭大象就是：**如果 AI 真的學會了你教它的一切，它就不再需要你了。**

這不是惡意的預言，而是這門生意的邏輯終點。你教得越好、打分越精確、回饋越專業，模型就進步得越快，你對它的價值就下降得越多。Mercor 的商業模式建立在「AI 永遠需要人類把關」的假設上，但 AI 的發展軌跡恰恰指向相反的方向。

這是一場和時間賽跑的交易。

---

## 產業衝擊

### 第一層：直接受影響者

**受益者（短期）：**

最明顯的受益者就是這三萬多名在 Mercor、Scale AI 等平台上工作的領域專家。時薪 81 到 200 美元以上，工作時間彈性，不用通勤——對於許多已經在正職之外尋找額外收入的專業人士來說，這是一份相當理想的兼職。尤其是在醫療、法律這些本身就有大量行政負擔的行業，能把專業知識「出租」給 AI 公司，是一種全新的收入來源。

**受損者（已經開始）：**

入門級白領工作正在消失。這不是預測，而是正在發生的事。美國的專業領域招聘——金融、科技、諮詢、行銷、法律的[初階職位](https://www.marketingaiinstitute.com/blog/dario-amodei-ai-entry-level-jobs)——已經明顯放緩。2026 屆的畢業生可能會進入一個 AI agent 在入門級任務上表現得比他們更好的就業市場，而公司開始悄悄停止提供這些職位。

Mercor 的基準測試無意中揭露了一個殘酷的趨勢：2023 年的軟體工程基準測試與初階程式設計師的就業數據高度相關——隨著 AI 在這些測試上的分數飆升，對應的人類職位就開始萎縮。

### 第二層：商業模式衝擊

**SaaS 行業的地震：** Anthropic Claude Cowork 引爆的那場軟體股崩盤不是市場過度反應——它預示了一個真實的結構性轉變。當 AI 可以直接執行法律研究、金融分析、文件管理等任務時，那些把這些功能包裝成 SaaS 產品來賣的公司，商業模式就面臨根本性的威脅。Thomson Reuters、LexisNexis、LegalZoom——這些公司賣的本質上是「幫專業人士更有效率地做事的工具」。但如果 AI 可以直接做那件事本身呢？

**RLHF 產業本身的弔詭：** Mercor 和 Scale AI 的估值建立在一個前提上：AI 模型需要持續的人類專家回饋才能進步。但 AI 研究界正在積極開發 [RLAIF（Reinforcement Learning from AI Feedback）](https://arxiv.org/abs/2309.00267)——讓 AI 自己評判 AI、自己生成訓練資料的技術。最新的研究顯示，RLAIF 在某些任務上已經達到了和 RLHF 相當甚至更好的表現。如果這條路走通了，Mercor 那三萬名時薪百美元的專家，需求可能會在幾年內大幅萎縮。

Bloomberg 的一篇評論文章直接問了這個問題：〈[AI White-Collar Gig Economy Is Booming. Can It Last?](https://www.bloomberg.com/opinion/articles/2026-02-03/ai-white-collar-gig-economy-is-booming-can-it-last)〉。答案取決於 AI 自我訓練技術的進展速度。

### 第三層：開發者生態

軟體工程師是 Mercor 最搶手的專家類別，這件事本身就值得玩味。

開發者正在做一件前所未有的事：系統性地教 AI 如何寫程式、如何 debug、如何做架構決策。而 Mercor 的基準測試顯示，AI 在軟體工程任務上的進步速度最快。這意味著，軟體工程師群體可能是這波浪潮中最先完成「自我替代訓練」的專業社群。

但也有反轉的可能。Mercor 的測試同時發現，AI 在「範圍明確的交付物」上表現最好，但在需要判斷力的開放性工作上仍然有明顯差距。而且擬定一個夠好的 prompt 來讓 AI 完成複雜任務——正如前美銀分析師 Matt Seck 所說——「比自己做還麻煩」。

這暗示了一個可能的未來：**會用 AI 的專業人士會取代不會用 AI 的專業人士，而不是 AI 取代所有專業人士。** 至少在中短期是這樣。

### 第四層：二階效應

**新型職業不平等：** 一端是 Mercor 上時薪 200 美元的史丹佛醫師，另一端是肯亞時薪 2 美元的資料標註員。兩者都在「訓練 AI」，但境遇天差地遠。這個產業正在複製——甚至放大——全球既有的專業階層差距。高技能的專家在淘金潮中撈金，低技能的勞工在被壓榨後被拋棄。

**「專家」這個概念的貶值：** 當你的二十年臨床經驗可以被拆解成一系列可打分的 rubric，再餵給一個語言模型……「專家」這個身分本身會發生什麼變化？以前，專業知識是累積性的、不可替代的。現在，它變成了可以被提取、數位化、轉移的資產。長遠來看，這可能從根本上改變人們對「學習一門專業」的投資意願。

**教育體系的危機：** 如果入門級白領工作大量消失，傳統的「學位→實習→初階職位→資深專家」的職業階梯就斷了一截。但 AI 訓練又需要「有 7.25 年平均經驗的領域專家」。如果新一代的年輕人沒有機會累積那 7.25 年的經驗，未來誰來訓練 AI？這是一個自我毀滅的循環。

---

## 未來展望

### 短期（3-6 個月）：淘金熱持續

Mercor 和類似平台的需求在短期內不會減少。AI 模型的迭代速度越來越快，每一代新模型都需要新一輪的人類回饋和品質測試。特別是隨著 AI 進入更多垂直領域——醫療、法律、教育、金融——對各領域專家的需求只會增加。

如果你是一名有數年經驗的專業人士，現在是加入這個市場的好時機。報酬高、需求大、進入門檻（相對於你已經花了好幾年累積的專業知識而言）不高。

### 中期（6-18 個月）：分岔路

**情境 A：RLAIF 突破，專家需求萎縮。** 如果 AI 自我訓練技術在接下來一年內取得突破性進展，簡單的評分和品質把關工作會首先被自動化。Mercor 的低階任務量可能開始下降，平台會把重心轉向更高端、更複雜的評估工作——那些 AI 還無法自我判斷的邊緣案例。

**情境 B：AI 能力瓶頸，RLHF 持續剛需。** 如果像 METR 研究暗示的那樣，AI 在真實世界的複雜任務上遇到瓶頸，那「人類在迴圈中」的重要性可能會維持更長時間。Mercor 的估值會得到驗證，可能還會出現更多類似的平台。

**情境 C：混合模式。** 最可能的情況：RLAIF 會處理大量的常規訓練工作，但在高風險領域（醫療決策、法律建議、金融判斷），人類專家的角色會從「大量標註」轉變為「最終審核」。工作量減少，但單位價值提高。

### 長期推演：3-5 年後的世界

如果 AI 的能力曲線繼續按照過去兩年的軌跡發展——而目前沒有明確的理由認為它會停下——那我們可能正在見證人類歷史上最獨特的勞動現象之一：**一整個世代的專業人士，自願且有酬地參與了自己職業的自動化。**

這在人類的勞動史上沒有先例。工業革命時代的織布工人沒有被邀請去教蒸汽織布機怎麼織布。汽車裝配線上的工人沒有被付費去調校機器手臂。但在 AI 時代，知識工作者正在被付以高薪，系統性地將自己的判斷力、經驗和直覺轉化為模型的訓練資料。

三到五年後，最有可能的結局是：**Mercor 式的 RLHF 產業會經歷一個劇烈的收縮和轉型。** 大部分常規的訓練工作會被自動化，但會出現一個更小、更精英的「AI 品質保證」專家群體——他們的工作不是教 AI 做事，而是在最關鍵的場景中判斷 AI 做得對不對。從「老師」變成「考官」。

### 給讀者的行動建議

**如果你是開發者：** 不要只學怎麼寫程式——學怎麼「指導」和「審核」AI 寫的程式。能精確描述需求、能判斷 AI 輸出品質、能在 AI 犯錯時立刻看出問題——這些能力在未來可能比從零寫程式更有價值。同時，趁現在 RLHF 平台報酬還高，去了解這個市場也不是壞事。

**如果你是創業者或產品經理：** 認真思考你的產品在「AI 可以直接做這件事」的世界裡還有沒有存在意義。如果你的核心價值只是「幫專業人士更有效率地做事」，那你可能有麻煩了。考慮轉向 AI 做不好的事——關係建立、信任、高風險決策中的最終判斷。

**如果你是一般科技從業者：** 密切關注你所在領域的 AI 基準測試分數。當 AI 在你的專業領域從 35% 漲到 65% 時，你大概有一到兩年的緩衝期。當它從 65% 漲到 85% 時，你可能需要認真重新定義自己的職業價值。不要等到 95% 才開始行動。

最後，我想引用 Chiao 醫師的一段話作為結尾：「有一種直覺是來自經驗的，來自坐在病人面前、看著他們的眼睛，看到一些超越病史、檢驗數值、言語能表達的東西。AI 不是醫生，不是人。」

她說得對。但問題是——在一個 AI 在 47.6% 的專業任務上已經被專家評為「表現更好」的世界裡，光靠「人的溫度」還能維持多久的價值？

這不是一個有標準答案的問題。但它是我們這個時代最需要面對的問題之一。

---

## 延伸閱讀

- [This doctor is training AI to do her job. And it's a booming business — CNN](https://www.cnn.com/2026/02/17/business/ai-experts-training-jobs)：本文的核心報導，深入描繪了 Chiao 醫師和 Mercor 的故事
- [AI Is Learning to Do the Jobs of Doctors, Lawyers, and Consultants — TIME](https://time.com/7322386/ai-mercor-professional-tasks-data-annotation/)：Mercor 基準測試的獨家數據，GPT-5 在專業任務上的表現分析
- [Mercor quintuples valuation to $10B with $350M Series C — TechCrunch](https://techcrunch.com/2025/10/27/mercor-quintuples-valuation-to-10b-with-350m-series-c/)：Mercor 融資歷程和商業模式的詳細拆解
- [Kenyan workers with AI jobs thought they had tickets to the future — CBS News](https://www.cbsnews.com/news/ai-work-kenya-exploitation-60-minutes/)：AI 訓練產業光鮮外表下的勞動剝削真相
- [Microsoft AI chief gives it 18 months for all white-collar work to be automated — Fortune](https://fortune.com/2026/02/13/when-will-ai-kill-white-collar-office-jobs-18-months-microsoft-mustafa-suleyman/)：Suleyman 的 18 個月預測與市場現實的落差分析
- [AI could make half of all entry-level white-collar jobs vanish — Fortune](https://fortune.com/2025/05/28/anthropic-ceo-warning-ai-job-loss/)：Amodei 對入門級白領工作的預測和他提出的「token 稅」方案
- [Klarna CEO agrees with Dario Amodei on AI workforce shrinkage — Fortune](https://fortune.com/2026/02/17/klarnas-ceo-dario-amodei-ai-white-collar-workforce-shrink-2030/)：第一線 CEO 如何用「自然流動」策略縮減 AI 時代的人力
- [RLAIF vs. RLHF: Scaling Reinforcement Learning from Human Feedback with AI Feedback — arXiv](https://arxiv.org/abs/2309.00267)：AI 自我訓練技術的最新研究，可能動搖整個 RLHF 產業的根基
