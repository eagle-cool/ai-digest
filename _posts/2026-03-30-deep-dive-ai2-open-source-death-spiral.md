---
title: "美國開源 AI 最後的堡壘倒了：AI2 的瓦解與一場靜悄悄的投降"
date: 2026-03-30
description: "艾倫人工智能研究所核心團隊集體出走微軟，開源模型 OLMo 前途未卜。當訓練一個前沿模型要燒掉數億美元，非營利機構還能撐起真正開源的旗幟嗎？從 AI2 的瓦解，看美國開源 AI 的東升西落。"
tags: [deep-dive, llm, ai-research, ai-industry]
---

## 引言

上週，Hannaneh Hajishirzi 還在英偉達 GTC 大會的舞台上，和黃仁勳談笑風生，暢聊開源模型的未來。她是 OLMo——全世界最透明的開源大型語言模型——的聯合負責人，也是一個耗資 1.52 億美元、由美國國家科學基金會和英偉達聯合資助的開源科學 AI 計畫（OMAI）的聯合首席研究員。

那場對話的畫面看起來充滿希望，彷彿開源 AI 的未來一片光明。

然後，不到一週，她和 AI2（艾倫人工智能研究所）的整個核心領導團隊——前 CEO Ali Farhadi、前 COO Sophie Lebrecht、多模態模型專家 Ranjay Krishna——被打包送進了微軟 Mustafa Suleyman 的「超級智能」團隊。與此同時，AI2 宣布削減開源模型開發資金，戰略重心從建構基礎模型轉向 AI 應用。

X（前 Twitter）上一片哀鳴：**美國開源 AI 最後的旗幟，倒了。**

這不是一場突發事件，而是一場醞釀已久的結構性崩塌。當訓練一個前沿模型的成本從數千萬美元飆升到數億美元、即將突破十億美元大關，一家靠慈善資金運作的非營利研究所，要怎麼和手握千億現金流的科技巨頭正面對決？

這篇報導的起點是[量子位對 AI2 事件的報導](https://www.36kr.com/p/3744774263095560)，但故事遠不止於此。AI2 的瓦解不只是一家機構的興衰，它折射出的是整個開源 AI 運動正在經歷的存亡危機——而這場危機的贏家和輸家，可能會重新定義未來十年的 AI 產業格局。

---

## 事件全貌

### 一場有預謀的「大遷徙」

3 月 12 日，Ali Farhadi 正式卸任 AI2 CEO，結束了超過兩年半的任期。Farhadi 是計算機視覺領域的頂尖專家，也是華盛頓大學保羅·艾倫計算機科學與工程學院的教授——沒錯，這所學院就是以 AI2 的創辦人保羅·艾倫的名字命名的。

他的離開本身就已經是個震撼彈。但真正讓業界感到不安的，是接下來發生的事：Farhadi 並非孤身離去，他帶走了 AI2 最核心的研究力量。

[根據 GeekWire 的報導](https://www.geekwire.com/2026/microsoft-hires-former-ai2-ceo-ali-farhadi-and-key-researchers-for-suleymans-ai-team/)，隨他一同加入微軟的包括：

- **Hannaneh Hajishirzi**：OLMo 開源語言模型的聯合負責人，全球被引用次數最多的自然語言處理研究者之一，OMAI 計畫聯合首席研究員
- **Ranjay Krishna**：主導了 AI2 的多模態模型 Molmo 等多個關鍵項目
- **Sophie Lebrecht**：前 COO，擁有布朗大學認知神經科學博士學位，曾共同創立 Xnor.ai 和 Neon Labs

四人將加入 Mustafa Suleyman 在微軟��超級智能團隊，同時保留他們在華盛頓大學的教職。Suleyman 在 LinkedIn 上高調歡迎他們，稱 Farhadi 帶領 AI2 在一年內發布了超過 100 個模型，而 Hajishirzi 是「全球被引用次數最多的 NLP 研究者之一，毫無疑問」。

AI2 則由創始成員 Pete Clark 接任臨時 CEO，董事會開始尋找永久繼任者。

### 錢的問題

為什麼要走？答案很直白：**錢不夠了**。

AI2 董事會主席 Bill Hilf 的說法毫不遮掩。他說，Farhadi 希望在 AI 的最前沿進行研究，但 OpenAI、Google 這些公司動輒花數十億美元訓練一個最先進的模型。對一家非營利組織而言，用慈善資金訓練出對標巨頭的模型，還要完全開源——這條路越來越走不通了。

Hilf 承認，董事會必須權衡：**慈善資金是否還應該用來「追趕進度」？**

更關鍵的變化來自 AI2 的金主。AI2 最初由保羅·艾倫的 Vulcan 公司資助，艾倫 2018 年去世後由其遺產繼續支持。目前的最大資助方是**科學與技術基金會（FFST）**，由艾倫遺產設立，規模達 31 億美元。

2024 年，Linda Stuart 博士接任 FFST CEO 後，資助策略發生了根本性轉向。Stuart 是醫生科學家出身，曾領導華盛頓大學蛋白質設計研究所，她更傾向於支持有明確科學應用和可量化社會影響的項目。

具體來說，FFST 將從**提供年度整體資助**轉向**基於項目提案的資助模式**。這個轉變聽起來只是行政流程的調整，實際影響卻是致命的。

在年度整體資助下，研究機構有高度自主權，可以承擔長期風險、靈活調配資源。而基於提案的模式引入了更強的成果導向和短期問責——每個資助週期都需要明確的可交付成果和影響力指標。對於開源基礎模型開發這種「週期長、成本高、商業回報不直接」的工作來說，這基本上就是判了死刑。

有知情人士透露，FFST 未來的資助將**更傾向於 AI 的實際應用，而非構建開源基礎模型**。

這完美解釋了為什麼專注於模型開發的研究人員紛紛選擇離開。他們不是被微軟的薪水挖走的——他們是被自己機構的未來預期逼走的。

---

## 脈絡

### 保羅·艾倫的遠見

要理解 AI2 的隕落為何讓人痛心，得先回到它的起點。

2014 年，微軟聯合創始人保羅·艾倫創立了艾倫人工智能研究所。艾倫的初衷很明確：他認為 AI 早期研究中有大量關於常識推理的重要工作被擱置了，而商業公司不會去做這些「不賺錢但重要」的基礎研究。他想建立一個不受利潤驅動的機構，專注於推動 AI 造福人類。

「我們沒有股東，沒有創始人跳出來說『來吧，讓我們一起打造下一個十億美元的公司』」——這是 AI2 領導層曾經引以為傲的自我定位。

艾倫的投資是慷慨的。AI2 迅速成長為擁有近 300 名研究員、工程師和職員的機構，累計發表超過 1,000 篇 AI 論文，推出了 Semantic Scholar（AI 驅動的學術搜尋引擎）、AllenNLP（開源 NLP 框架）、AI2-THOR（具身 AI 平台）等一系列影響深遠的項目。

但艾倫於 2018 年因非霍奇金淋巴瘤去世後，AI2 的命運就系在了遺產基金會的決策上。而遺產基金會的新領導層，顯然對「燒錢做開源模型」這件事的熱情，遠不如艾倫本人。

### OLMo：開源的黃金標準

AI2 最具標誌性的遺產，是 OLMo（Open Language Model）系列。

在「開源 AI」這個詞已經被各大公司用濫的今天，OLMo 是少數真正配得上「完全開源」四個字的模型。[根據 AI2 官方的說法](https://allenai.org/blog/hello-olmo-a-truly-open-llm-43f7e7359222)，它不只開源模型權重——這只是最基本的——而是從數據處理、預訓練、微調到評測，**全流程公開透明**，並且始終採用對開發者最友好的 Apache 2.0 授權。

為什麼這很重要？因為沒有訓練數據，研究者就無法科學地理解一個模型是怎麼運作的。這就像做藥物研發卻不做臨床試驗，或者研究太陽系卻沒有望遠鏡。OLMo 搭配它的訓練數據集 Dolma，讓學術界第一次能夠深入分析預訓練數據和模型表現之間的關係——這在 AI 社群中是一個極少被公開研究的課題。

2025 年 11 月發布的 OLMo 3 更進一步，推出了 Base、Instruct、Think 和 RL Zero 四個變體，涵蓋 7B 和 32B 參數規模。其中 OLMo 3-Think 32B 被宣傳為「該規模首個完全開源推理模型」。更難得的是，AI2 發布了完整的「模型流程」——包括訓練日誌、中間檢查點、完整代碼和配置，以及升級版的 OlmoTrace 工具，允許研究者把模型的推理步驟回溯到具體影響它的數據和訓練決策。

這種透明度，在整個 AI 產業中是獨一無二的。Meta 的 Llama 只開源權重，不公開訓練數據；Mistral 部分數據閉源；Google 的 Gemma 提供權重但沒有完整訓練流程。只有 OLMo 做到了真正的「從頭到尾透明」。

而現在，帶領 OLMo 的核心團隊去了微軟，AI2 的資金方對基礎模型開發失去興趣。這個開源領域的黃金標準，前途未卜。

### 訓練成本的指數級暴漲

AI2 的困境不是個案，而是結構性問題。

[根據 Epoch AI 的研究](https://epoch.ai/blog/how-much-does-it-cost-to-train-frontier-ai-models)，前沿 AI 模型的訓練成本在過去八年裡以每年 2-3 倍的速度增長。具體數字觸目驚心：Google 的 Gemini Ultra 訓練成本約 1.91 億美元，GPT-4 約 7,800 萬美元，Meta 的 Llama 3.1 405B 約 1.7 億美元。而 Anthropic CEO Dario Amodei 曾表示，到 2028 年，前沿模型的訓練成本可能達到 **100 億美元**。

有趣的是，這裡存在一個悖論：訓練「GPT-4 等級」模型的成本其實在快速下降——從 2023 年的 7,900 萬美元降到 2026 年的 500-1,000 萬美元。但問題是，前沿的定義一直在往前移。你今天花幾百萬能訓練出去年的頂級模型，但要跟上今年的前沿，還是得燒數億美元。

AI2 的年度運營預算雖未公開，但 OMAI 計畫的 1.52 億美元是五年期、多機構共享的專項資助，年均約 3,000 萬美元——這大概只夠訓練一個前沿模型的一小部分。跟巨頭相比，是數量級的差距。

用 Bill Hilf 的話說：在大模型開發的最高規模上與科技巨頭競爭，**已經變得異常困難**。

---

## 多方觀點

### 悲觀派：非營利開源 AI 已死

一批業內人士認為，AI2 的遭遇只是證實了一個殘酷的事實：用非營利方式做頂級開源模型這條路，從經濟學上就站不住腳。

論點很簡單。前沿模型訓練成本以指數級增長，硬體（AI 加速器晶片、伺服器、互連設備）佔總成本的 47-67%，研發人員成本佔 29-49%。這不是靠募款能解決的問題。當 OpenAI 一年的資本支出以百億美元計、Google DeepMind 和 Meta AI 背後有千億級的企業資源，一家年預算可能只有幾千萬的非營利機構，拿什麼打？

更何況，人才市場的競爭同樣殘酷。微軟、Google、Meta 開出的薪酬包裹動輒數百萬美元，還能提供世界級的算力資源。AI2 作為非營利機構，在薪酬上本來就沒有優勢，現在連研究資源都在縮水，核心團隊出走幾乎是必然的。

[The Decoder 的分析指出](https://the-decoder.com/microsoft-hires-top-ai-researchers-from-allen-institute-for-ai-for-suleymans-superintelligence-team/)，這次事件「加速了一個整合趨勢：前沿模型開發越來越集中在資金雄厚的科技公司，而非研究機構」。

### 樂觀派：火種還在，形式在變

但也有人不認為天塌了。

首先，AI2 並沒有完全關門。臨時 CEO Pete Clark 強調，AI2 仍致力於其使命，與 NSF 和 Nvidia 的合作關係（包括 OMAI 計畫）持續進行，背後有經驗豐富的團隊保障工作延續。Hajishirzi 等人雖然去了微軟，但保留了華盛頓大學的教職，意味著學術層面的開源研究不會完全斷裂。

其次，開源 AI 的形態正在演化。Hugging Face 的 SmolLM 系列由社區驅動，雖然缺乏大規模訓練資源，但在小型模型領域持續創新。英偉達的 Nemotron 系列近期越來越開放，發布了更多開源數據和開放授權。而在中國，DeepSeek、通義千問（Qwen）、Kimi 等模型正以驚人的速度崛起——它們證明了開源 AI 不需要靠非營利機構才能存活。

再者，「GPT-4 等級」模型的訓練成本在快速下降。也許兩年後，今天的前沿水準就成了「平價品」，屆時小型團隊和研究機構又能重新參與競爭。

### 實務工作者的聲音：開源的定義早就模糊了

對於每天使用這些模型的開發者來說，AI2 的故事更多是一聲嘆息而非警鐘。

現實是，大多數開發者使用的「開源」模型——Llama、Mistral、Qwen——本來就不是 AI2 那種級別的「完全開源」。它們開源權重，但不公開訓練數據和完整流程。在實務層面，開發者關心的是模型能不能用、好不好用、便不便宜，而不是能不能看到訓練日誌。

一位在 Hacker News 上的評論說得很直白：「OLMo 的完全透明對學術研究有巨大價值，但對 99% 的應用開發者來說，Llama 或 Qwen 就夠了。」

這引出了一個更深層的問題：**開源 AI 的核心價值到底是什麼？** 是學術意義上的完全透明和可重現？還是商業意義上的免費使用和可修改？AI2 的衰落，某種程度上是前者輸給了後者。

### 我的看法

以我的觀察，AI2 的故事其實揭示了一個更深層的矛盾：**真正的開源需要的不只是善意，還需要可持續的經濟模型**。

保羅·艾倫的遠見沒有錯，但他低估了一件事——或者說他去世得太早，來不及見證——AI 訓練成本的指數級增長速度，遠超任何慈善基金的承受能力。2014 年創立 AI2 時，訓練一個語言模型可能只要幾十萬美元。2026 年，這個數字已經是數億美元。

非營利機構做開源基礎模型，就像拿弓箭跟航空母艦對射。不是你射箭的技術不好，是武器代差太大。

但這也不代表開源 AI 就此完蛋。它更可能的演化路徑是：**開源從「獨立研究機構的理想」變成「商業巨頭的競爭武器」**。中國的 DeepSeek 和阿里的 Qwen 就是最好的例子——它們的開源不是出於慈善，而是出於戰略。這個轉變的好壞，值得所有人深思。

---

## 產業衝擊

### 第一層：微軟的超級智能棋局

AI2 人才流向微軟，不是偶然。這是微軟一盤精心布局的大棋的最新一步。

自 2025 年 11 月起，Suleyman 就開始組建超級智能團隊，已從 Google DeepMind、Meta、OpenAI、Anthropic 等巨頭挖角了大量研究人員。AI2 團隊的加入，帶來的不只是人才，更是開源模型開發和訓練效率方面的深厚積累。

為什麼微軟要這麼做？因為[微軟正在全力減少對 OpenAI 的依賴](https://www.windowscentral.com/artificial-intelligence/microsoft-confirms-plan-to-ditch-openai-as-the-chatgpt-firm-continues-to-beg-big-tech-for-cash)。

Suleyman 在接受《金融時報》採訪時明確表示，微軟的目標是實現「AI 自給自足」。公司已經在開發自己的基礎模型（Phi-4 系列和大規模的 MAI 模型），推出了第二代 AI 加速器晶片 Maia 200，並在建設 Fairwater 網路的 AI 資料中心。

2026 年 3 月的組織重組更是進一步明確了方向：Suleyman 從管理消費級 Copilot 產品轉為專注領導超級智能研究。[微軟官方部落格的公告](https://blogs.microsoft.com/blog/2026/03/17/announcing-copilot-leadership-update/)顯示，這是一次全面的戰略調整。

微軟和 OpenAI 的合約確保了到 2032 年仍能存取 OpenAI 的最新模型，包括 AGI 後的模型。但這更像是一份保險——微軟真正的賭注，是在此之前建立起完全自主的 AI 能力。

從這個角度看，AI2 的核心團隊對微軟的價值是巨大的。他們不只帶來了頂尖的研究能力，更帶來了從零開始訓練模型的完整經驗——包括數據處理、訓練基礎設施、評估框架——這些正是微軟建立獨立模型開發能力最需要的東西。

### 第二層：Meta 的退縮與開源的信任危機

如果說 AI2 的故事是「非營利開源打不下去了」，Meta 的故事就是「商業開源也在動搖」。

[根據多家媒體報導](https://winbuzzer.com/2025/12/09/meta-pivots-from-llama-to-closed-ai-models-abandoning-open-source-roots-xcxwbn/)，Meta 正在開發代號「Avocado」的新模型，而這個模型可能以閉源形式發布——這是對 Llama 系列開源策略的重大轉向。原因很直白：Llama 4 的市場反應不如預期，而 Llama 的架構已經被中國的 DeepSeek 等公司充分利用，Meta 開始擔心開源帶來的架構暴露問題。

Meta 還成立了由首席 AI 官 Alexandr Wang 領導的 TBD Lab 精英團隊，招募了前 GitHub CEO Nat Friedman 等重量級人物。Avocado 將在更嚴格的控制下開發，標誌著 Meta 從「AI 界的 Android」自我定位的後退。

這形成了一幅諷刺的圖景：**美國最大的兩個開源 AI 力量——一個非營利（AI2），一個商業（Meta Llama）——幾乎在同一時間走向了「去開源化」。**

### 第三層：中國開源的全面崛起

美國這邊在退縮，大洋彼岸的中國卻在全面進攻。

數字說明一切。[根據南華早報引用的數據](https://www.scmp.com/tech/tech-trends/article/3335602/chinas-open-source-models-make-30-global-ai-usage-led-qwen-and-deepseek)，中國開源大模型的全球使用份額從 2024 年底的 1.2% 飆升至 2025-2026 年的近 **30%**。在 Hugging Face 上，阿里巴巴的通義千問（Qwen）系列截至 2026 年 1 月累計下載量超過 7 億次，超越 Meta 的 Llama 成為全球下載量最高的開源 AI 系統。

[MIT 和 Hugging Face 的聯合報告](https://www.technologyreview.com/2026/02/12/1132811/whats-next-for-chinese-open-source-ai/)顯示，過去一年中國開源模型的全球下載量佔比達到 17.1%，首次反超美國。Andreessen Horowitz 的一位合夥人估計，**80% 的美國新創公司正在使用中國的基礎模型來開發衍生產品**。連 Airbnb CEO Brian Chesky 都公開承認，公司使用 Qwen 來驅動 AI 客服聊天機器人。

更令人玩味的是，上週 Cursor 發布新模型 Composer 2 被曝套壳月之暗面的 Kimi K2.5，另一家新創 Deep Cogito 的 Cogito v2.1 也被發現基底是 DeepSeek。美國的 AI 新創公司，正在悄悄地建立在中國開源模型的地基上。

[美中經濟與安全審查委員會（USCC）2026 年 3 月的報告](https://www.uscc.gov/sites/default/files/2026-03/Two_Loops--How_Chinas_Open_AI_Strategy_Reinforces_Its_Industrial_Dominance.pdf)更進一步指出，中國的開源 AI 策略已形成「雙循環」效應——國內的技術迭代和國際的生態擴張相互強化，正在系統性地鞏固中國在 AI 產業鏈中的主導地位。

這才是 AI2 事件最深層的地緣政治意涵：**美國正在失去開源 AI 的陣地，而這塊陣地正在被中國快速佔領。**

### 第四層：對開發者的實質影響

對全球開發者來說，AI2 的衰落有幾個直接影響：

**學術研究受創最深。** OLMo 是全球唯一提供完整訓練流程的大型語言模型，對於研究 LLM 行為、安全性、偏見等議題的學者來說，這是不可替代的資源。如果 OLMo 的開發停滯或縮減，AI 的可解釋性研究將失去最重要的實驗平台。

**開源的定義進一步稀釋。** 當真正的「完全開源」模型消失，剩下的都是「半開源」——開放權重但不開放數據和訓練流程。這意味著開發者能用，但不能真正理解和驗證。對於關注 AI 安全和可信度的應用場景（醫療、金融、政府），這是個問題。

**中國模型依賴加深。** 如果美國的開源選項進一步減少（AI2 縮編 + Meta 可能轉閉源），開發者將更多轉向中國的 Qwen、DeepSeek 等模型。這在地緣政治緊張的背景下，對美國政策制定者來說是個棘手的問題；但對開發者來說，好用又免費的模型就是最好的模型。

---

## 未來展望

### 短期（3-6 個月）：AI2 進入「休養期」，微軟加速建模

幾乎可以確定會發生的事：

- AI2 會在 Pete Clark 的領導下進行戰略重整，從基礎模型開發轉向 AI 應用和科學研究。OMAI 計畫會繼續，但規模和野心可能縮減。
- 微軟的超級智能團隊將利用前 AI2 團隊的經驗，加速自研基礎模型的開發。微軟的 MAI 系列模型可能在 2026 年下半年亮相。
- Meta 的 Avocado 模型將在 5-6 月前後推出，如果確認是閉源，將正式宣告 Llama 開源路線的終結。
- 中國開源模型的全球份額將繼續攀升，DeepSeek V4 和 Qwen 3 等下一代模型已經在路上。

### 中期（6-18 個月）：開源 AI 的分水嶺

**情境一：企業開源接棒。** 英偉達的 Nemotron 系列變得更加開放，成為新的「準開源」標桿。但這種開源本質上服務於硬體生態，而非學術透明。開源 AI 從「理想主義驅動」全面轉向「商業戰略驅動」。

**情境二：社區力量崛起。** 隨著訓練 GPT-4 等級模型的成本降至數百萬美元，Hugging Face、EleutherAI 等社區組織獲得新的生命力。也許我們會看到一種「分散式開源」的新模式——不是一家機構從頭訓練，而是全球社區協作、分攤成本。

**情境三：政府介入。** 歐盟或美國政府意識到開源 AI 的戰略重要性，開始提供國家級資金支持。法國、印度、阿聯酋等國已經在用 Llama 作為「主權 AI」的基礎，如果 Llama 轉閉源，這些國家可能會推動建立政府資助的開源 AI 計畫。

### 長期推演：3-5 年後的世界

如果當前趨勢持續，3-5 年後的 AI 產業可能是這樣的：

前沿模型開發完全集中在 5-6 家超大型科技公司手中（OpenAI、Google、Microsoft、Anthropic，加上中國的阿里巴巴和字節跳動）。「開源」模型繼續存在，但它們不是前沿——而是前沿模型的「降級版」或「上一代回收品」。真正的「完全開源」（像 OLMo 那樣公開一切）可能只存在於學術領域和小型模型。

中國在開源 AI 生態系統中的主導地位將進一步鞏固。全球開發者——包括美國開發者——越來越依賴中國的開源模型作為開發基礎。這將創造一個奇特的依賴關係：美國公司在中國開源模型上構建產品，就像 90 年代中國在 Windows 上構建軟體產業一樣。只不過角色互換了。

### 給讀者的行動建議

**如果你是開發者：**
- 不要把雞蛋放在一個籃子裡。學會在多個模型之間切換（Llama、Qwen、DeepSeek、Gemma），建立模型無關的架構。
- 如果你做的是對可解釋性要求高的應用，趁 OLMo 還在，趕緊下載並備份它的完整訓練流程和數據集。這些資源一旦消失，可能不會再有。
- 認真評估中國開源模型。拋開地緣政治偏見，Qwen 和 DeepSeek 在很多場景下已經是最優選擇。

**如果你是創業者或產品經理：**
- 把「開源模型供應鏈風險」加入你的技術評估框架。今天的開源明天可能變閉源（參見 Meta），今天的免費模型明天可能因為地緣政治被禁用。
- 考慮為你的產品建立模型抽象層，讓底層模型可以快速替換。
- 如果你的商業模式建立在某個特定開源模型上，現在就開始制定 Plan B。

**如果你是一般科技從業者：**
- 理解一個趨勢：AI 的核心技術正在加速集中化。這不一定是壞事（集中化帶來效率），但它意味著未來的 AI 生態系統將由少數巨頭主導。你的職業規劃應該考慮到這一點。
- 關注開源 AI 的政策討論。各國政府正在形成對開源 AI 的不同態度，這些政策決定將直接影響你能用什麼模型、怎麼用、以什麼成本用。

保羅·艾倫在 2014 年種下了一顆種子，希望 AI 的發展是開放的、透明的、為全人類服務的。十二年後，這顆種子結出的果實正在被商業巨頭摘走。AI2 的核心團隊去了微軟，OLMo 的未來不確定，而中國的開源模型正在填補美國留下的空白。

這是不是意味著保羅·艾倫的理想失敗了？也許。但也許更準確的說法是：**他的理想沒有錯，只是這個時代的經濟現實太殘酷了。**

當訓練一個 AI 模型的成本和造一艘航空母艦差不多的時候，「開源」這個詞的意義，注定要被重新定義。問題是：被誰定義？為了誰的利益？

這才是 AI2 的故事真正留給我們的問題。

---

## 延伸���讀

- [Microsoft hires former Ai2 CEO Ali Farhadi and key researchers for Suleyman's AI team — GeekWire](https://www.geekwire.com/2026/microsoft-hires-former-ai2-ceo-ali-farhadi-and-key-researchers-for-suleymans-ai-team/)：最完整的第一手報導，包含 Bill Hilf 和 Suleyman 的直接引述
- [Microsoft hires top AI researchers from AI2 for Suleyman's Superintelligence team — The Decoder](https://the-decoder.com/microsoft-hires-top-ai-researchers-from-allen-institute-for-ai-for-suleymans-superintelligence-team/)：從產業整合角度分析這次人才流動的意義
- [China's open-source models make up 30% of global AI usage — South China Morning Post](https://www.scmp.com/tech/tech-trends/article/3335602/chinas-open-source-models-make-30-global-ai-usage-led-qwen-and-deepseek)：中國開源 AI 崛起的全面數據
- [How much does it cost to train frontier AI models? — Epoch AI](https://epoch.ai/blog/how-much-does-it-cost-to-train-frontier-ai-models)：最權威的 AI 訓練成本分析，解釋為什麼非營利機構跟不上
- [Meta Pivots from Llama to Closed AI Models — WinBuzzer](https://winbuzzer.com/2025/12/09/meta-pivots-from-llama-to-closed-ai-models-abandoning-open-source-roots-xcxwbn/)：Meta 從 Llama 轉向閉源 Avocado 的策略分析
- [The Open Source AI Paradox: Why Meta and Mistral Give Away Models Worth Billions — Trensee](https://www.trensee.com/en/blog/deep-dive-opensource-ai-business-model-2026-03-15)：深度剖析商業開源 AI 的經濟學邏輯
- [Two Loops: How China's Open AI Strategy Reinforces Its Industrial Dominance — USCC](https://www.uscc.gov/sites/default/files/2026-03/Two_Loops--How_Chinas_Open_AI_Strategy_Reinforces_Its_Industrial_Dominance.pdf)：美中經濟與安全審查委員會報告，分析中國開源 AI 的戰略意圖
- [Hello OLMo: A truly open LLM — AI2](https://allenai.org/blog/hello-olmo-a-truly-open-llm-43f7e7359222)��OLMo 的原始發布文章，了解什麼是「真正的開源」
