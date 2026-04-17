---
title: "五十億美金壓上桌，但沒人說得清世界模型到底是什麼"
date: 2026-04-17
description: "2026 年 4 月 16 日，阿里和騰訊同一天丟出世界模型；兩個月前，李飛飛 World Labs 拿到 10 億美元，Yann LeCun 的 AMI Labs 用 10.3 億美元種子輪刷新歐洲紀錄。世界模型成了 AI 下一個十年的賭桌，但走進去看，五個派系互相矛盾、技術標準根本沒人定義、商業化時間表從一年到五年差距巨大。這篇文章帶你看清這場混亂的背後在發生什麼。"
tags: [deep-dive, ai-industry, ai-research, agents]
---

## 引言

2026 年 4 月 16 日，台北時間下午，兩條新聞幾乎同時跳上各家科技媒體：阿里巴巴推出開放式世界模型 Happy Oyster，瞄準遊戲與影視內容生產；騰訊把 HY-World 2.0 整包丟到 GitHub 和 Hugging Face 上開源，可以直接輸出 Mesh、3D Gaussian Splatting、點雲，丟進 Unity、Unreal Engine、Blender、Isaac Sim 都能用。

兩家中國互聯網巨頭，同一天，幾乎同一個時間點，宣告自己要在世界模型這條跑道上佔位。隔幾天前，李飛飛的 World Labs 才剛拿到 10 億美元融資，AMD、Autodesk（單獨砸了 2 億美元）、NVIDIA、Fidelity 一字排開；再往前一個月，Yann LeCun 才剛宣佈離開 Meta 創立的 AMI Labs 拿到 10.3 億美元種子輪，估值 35 億美元，創下歐洲史上最大種子輪紀錄。

把這幾筆錢加一加，光是過去三個月，全球資本砸在「世界模型」這四個字上的金額就超過 50 億美元。如果你再算上 NVIDIA 把 Cosmos 平台免費開放給開發者下載超過 200 萬次的隱性投入、Google DeepMind 用 Genie 3 直接餵給 Waymo 訓練自駕、Wayve 用 150 億參數的 GAIA-3 做自駕評估，加總會更可怕。

但這場狂歡有一個很尷尬的事實：**走進去問每一個玩家「世界模型到底是什麼」，會得到一堆彼此矛盾的回答**。有人說是可互動的 3D 世界，有人說是理解物理因果律的模型，有人說是機器人訓練用的數位仿真器，還有人乾脆說就是更高級的影片生成。這不是學術會議上的健康分歧，這是整個賽道在認知上的混亂。

更關鍵的是，當所有人都在喊「後 LLM 時代」的時候，幾乎沒有人停下來問一個更基本的問題：**這次砸進去的錢，到底在賭什麼？什麼時候、以什麼形式回得來？**

這篇的起點是 36 氪那篇 [《世界模型元年啟示錄：動機、亂戰與暗礁》](https://www.36kr.com/p/3769670392541961)，但故事遠不只一場熱錢追逐。我想帶你看清五個派系真正的差異、這場熱潮的真實技術瓶頸、誰會是真正的贏家，以及為什麼這波浪頭很可能不會像 LLM 那樣一年內就見分曉。

---

## 事件全貌

先把過去三個月的時間軸壓縮成一張圖。

**2026 年 2 月 18 日**：World Labs 宣布完成 10 億美元融資。投資人名單一眼就看出端倪——AMD、NVIDIA 兩家最大的 GPU 供應商同時下注，Autodesk 直接砸 2 億美元並擔任顧問，Sea Group 從東南亞跨海加碼。這不是一筆純財務投資，是把整條工業設計、遊戲、東南亞市場的供應鏈通道全部串起來。同一天，World Labs 的旗艦產品 Marble 正式進入商業化階段，從 2025 年 11 月的 limited beta 升級到 freemium + 付費分層，輸出格式包括 mesh、3D Gaussian Splatting、影片，[直接喊話 VFX、遊戲、VR 三大目標市場](https://techcrunch.com/2025/11/12/fei-fei-lis-world-labs-speeds-up-the-world-model-race-with-marble-its-first-commercial-product/)。

**2026 年 3 月 9 日**：Yann LeCun 的 AMI Labs 宣布 10.3 億美元種子輪，估值 35 億美元 pre-money。[投資人陣容更誇張](https://techcrunch.com/2026/03/09/yann-lecuns-ami-labs-raises-1-03-billion-to-build-world-models/)：Cathay Innovation、Greycroft、Hiro Capital、HV Capital、Bezos Expeditions 共同領投，個人投資者名單裡還有 Tim Berners-Lee、Mark Cuban、Eric Schmidt、Xavier Niel。LeCun 在發布會上講得很直白：他要證明 LLM 這條路徑是錯的，AI 真正的未來在 JEPA（Joint Embedding Predictive Architecture）這種抽象隱空間預測架構上。第一個合作夥伴是法國數位醫療公司 Nabla，但 LeCun 自己也承認，「真正能看到產品要 1 到 2 年，要做到通用智能要 3 到 5 年」。

**2026 年 4 月 16 日**：阿里和騰訊在同一天動手。阿里的 Happy Oyster 主打「導演模式」——用戶可以在影片播放途中隨時用文字指令改變劇情、切換鏡頭，[號稱要把內容生產從「被動生成」改成「主動模擬」](https://www.implicator.ai/alibaba-turns-happy-oyster-into-real-time-ai-world-model-for-games/)。騰訊的 [HY-World 2.0 直接開源](https://github.com/Tencent-Hunyuan/HY-World-2.0)，把所有東西丟到 GitHub 上，輸出可以直接導入 Unity 和 Unreal Engine，遊戲開發者拿來就能用。

NVIDIA 一直站在這條跑道的另一個位置上：它不下場做世界模型，它做「做世界模型的工具」。Cosmos 平台到 2026 年 2 月已經發到 Predict 2.5 和 Reason 2 版本，[模型下載數突破 200 萬次](https://www.nvidia.com/en-us/ai/cosmos/)，採用名單包括 1X、Agility、Figure AI、Galbot、Hillbot、Neura Robotics、Skild AI、XPENG、Waabi、Uber——基本上你能想到的具身智能或自駕公司，都在用 Cosmos 做合成資料生成。

更微妙的是 Waymo。今年 2 月，[Waymo 宣布它的全新模擬器 Waymo World Model 直接建立在 Google DeepMind 的 Genie 3 之上](https://waymo.com/blog/2026/02/the-waymo-world-model-a-new-frontier-for-autonomous-driving-simulation/)，能同時生成相機畫面和 LiDAR 資料，專門用來訓練自駕系統面對「現實中很少見」的場景：龍捲風、淹水街道、馬路上的大象。Wayve 則用 150 億參數的 GAIA-3 做評估與驗證，把自駕測試從「在路上跑幾百萬英里」變成「在生成的世界裡跑幾億次」。

把這些事件拼起來，你會看到一個非常清楚的訊號：**世界模型不是一個產品，是一整層新的技術堆疊**。從基礎模型（World Labs、AMI、阿里、騰訊）到工具平台（NVIDIA Cosmos、Genie 3）到下游應用（Waymo、Wayve、所有具身智能公司），每一層都有人在搶位置，每一層都有人剛拿到大錢。

---

## 脈絡

要理解世界模型為什麼突然成了 AI 圈的新賭桌，得先回到 LLM 撞牆的那個時刻。

過去兩年，ChatGPT 們展示了驚人的語言能力，也暴露了一個越來越無法迴避的缺陷：**它們不懂物理世界**。你問 LLM「把杯子推到桌子邊緣會怎樣」，它會回答「杯子會掉下去摔破」，但這不是因為它理解重力、慣性、碰撞，是因為訓練資料裡這種句子出現過幾百萬次。

2026 年初有一份研究指出，幻覺不是資料問題，也不是訓練問題，[是 LLM 架構本身的內在缺陷](https://medium.com/@ilyurek/beyond-next-token-prediction-yann-lecuns-jepa-and-the-quest-for-ai-common-sense-where-92150bed9dfd)——在 token 層級上做下一個字預測，本質上就是在表面形式上做機率估計，跟「理解世界怎麼運作」是兩件事。LeCun 最常用的例子是這樣：一個五歲小孩看了爸媽倒水兩次就知道杯子會滿、會溢出來；一個 LLM 看了幾百萬個跟「倒水」相關的句子，還是會在某個對話裡跟你說「水可以倒進已經滿的杯子裡而不溢出」。

這個缺陷在純文本任務裡也許可以忍。寫文案錯一句話沒事，翻譯出小錯校稿就好。但 AI 一旦要進入真實世界——操控機器人、開車、在工廠裡作業——「大概正確」就不夠了。你不能讓自駕系統「大概」正確地判斷前面有沒有障礙物，你不能讓工業機器人「差不多」預測零件下一秒在哪裡。這些場景對因果預測的要求是 99.99%，不是 95%。

於是一個更根本的需求浮出水面：我們需要一個能理解物理因果律的 AI。它不只要能說，還要能做；不只要看見，還要能預判動作後的世界狀態變化。這就是世界模型被推到聚光燈下的根本原因。

把時間拉得再遠一點，這條技術線其實有自己的歷史。世界模型這個詞最早可以追溯到 2018 年 David Ha 和 Jürgen Schmidhuber 那篇經典論文〈World Models〉，他們用 RNN 做了一個能在「夢境」裡學駕駛賽車的小 demo。當時這個方向太前沿、算力又不夠，大部分研究者沒有跟上。後來注意力被 Transformer 和 LLM 全部吸走了，世界模型在學術圈邊緣晃了五年。直到 2024 年下半年——LLM 開始顯露 plateau 跡象、Scaling Law 邊際效益遞減的訊號越來越明顯——世界模型才從邊緣回到舞台中央。

順著這條線看，你會發現 2026 年的世界模型熱潮跟 2022 年底 ChatGPT 的爆發有一個關鍵差別：**ChatGPT 是一個產品突然證明了一條技術路線可行；世界模型則是一群人賭一條還沒被證明可行的技術路線**。這個差別決定了接下來幾年的玩法會非常不一樣。LLM 那波是「先看到結果，再追趕」，世界模型這波則是「還沒看到結果，就先把錢押進去」。

歷史上類似的賭局有過幾次。2014 年的深度學習熱、2016 年的 VR/AR 熱、2018 年的區塊鏈熱、2021 年的元宇宙熱——每一次都是資本看到一條可能改變世界的技術路線，在還沒看到產品的時候先砸錢。其中深度學習贏了，VR/AR 撞牆撞了十年現在才慢慢爬起來，區塊鏈和元宇宙的故事大家也知道了。世界模型這波會走哪條路？沒人說得準，但至少從押注的金額和玩家陣容來看，這次的賭注比前幾次都大。

---

## 多方觀點

把這場熱潮的玩家攤開來看，會發現**至少有五個技術派系在用「世界模型」這四個字包裝自己的東西**，而且彼此的邏輯互相矛盾。

**第一派：抽象隱空間派（JEPA / AMI Labs）**

LeCun 的路線最反直覺。他的 [JEPA 架構刻意丟掉像素細節](https://createbytes.com/insights/jepa-vs-llm-ai-collaboration)，只在抽象的隱空間裡做預測。最新發布的 LeWorldModel 只有 1500 萬參數，單張 GPU 幾小時就能訓練完，但規劃速度比傳統方法快 48 倍。

他的論點是：真正的智能不需要模擬每一片樹葉飄落，只需要理解「風會吹落樹葉」這個因果。輸出人類看不懂沒關係，反正 AI 自己懂就行了。這條路最學術、最遠離商業化，但如果賭對了，就是一個全新的計算範式——而不只是一個更好的工具。

矽谷對 LeCun 這個賭法的反應很兩極。有人覺得這就是 deep learning 該往前走的方向，圖靈獎得主的直覺值得跟；有人覺得這是「研究員浪漫主義」，10 億美元種子輪的估值意味著 LP 至少要看到 100 億美元退出才划得來，但 LeCun 自己都說產品要 3 到 5 年，這個時間表跟 VC 基金的 10 年週期幾乎打平。

**第二派：3D 顯式空間派（World Labs / Marble）**

李飛飛的選擇剛好相反。她相信智能必須建立在三維空間的顯式理解之上。Marble 能從一張照片或一段文字生成可編輯、可導航的 3D 世界，使用者可以自由移動視角，World Labs 還[把渲染引擎 Spark 2.0 開源](https://www.fastcompany.com/91503667/world-labs-most-innovative-companies-2026)，讓普通瀏覽器都能流暢加載上億個 3D 點。

但 Marble 有一個被刻意低調處理的軟肋：**它擅長重建空間的「樣子」，但對空間裡會發生什麼的理解很薄弱**。你可以走進它生成的房間，但你推不動裡面的椅子，也打不翻桌上的杯子。它是一個靜態世界的複刻者，不是動態物理的模擬器。對 VFX 和遊戲場景生成來說綽綽有餘——一位 VFX 業界人士說 Marble 把概念設計流程加速了 40 倍——但對機器人訓練、自駕模擬這些動態場景，Marble 還差一大截。

**第三派：生成派（Genie 3 / Happy Oyster / HY-World）**

谷歌的 Genie 3、阿里的 Happy Oyster、騰訊的 HY-World 2.0 都屬於這一類。他們的賭注是：只要生成的畫面夠逼真、互動夠流暢，物理規律自然會被學出來。這個假設背後有個哲學立場——所謂的「理解」其實是「在表面層面上產生符合期待的行為」。

但這類產品有兩個共同的軟肋。第一是長時序一致性：[Genie 3 演示很驚艷，但官方坦承每段互動只能持續幾分鐘](https://deepmind.google/blog/genie-3-a-new-frontier-for-world-models/)，公開 demo 限制 60 秒，超過就會走樣。第二是物理準確性：場景看起來對，不代表物理規律對。一個球從桌上滾下來會不會以正確的拋物線軌跡掉到地上？目前的 demo 大多選擇性展示，極限條件下的失敗則藏起來。

**第四派：自駕專用派（Waymo / Wayve）**

Waymo 和 Wayve 的玩法務實得多。他們不追求通用世界模型，只專注在「跟駕駛相關的世界」。Waymo 直接把 Genie 3 拿來當底座，加上自己的後訓練把 2D 影片資料翻譯成 3D LiDAR 輸出。Wayve 的 GAIA-3 走 150 億參數路線，重點在「可重複、可控」——讓自駕測試可以在生成的世界裡跑幾億次邊緣案例。

這是目前商業化最清楚的一派。自駕公司有錢、有明確的訓練資料需求、有清楚的 ROI 計算公式（每模擬 1000 萬英里替代真實路測能省多少錢），世界模型對他們來說不是「未來的夢」，是「明天就能省錢」的工具。

**第五派：賣鏟人（NVIDIA Cosmos）**

NVIDIA 這手最聰明。它不押任何一條技術路線，它把所有路線需要的工具——資料處理管線、影片 tokenizer、預訓練基礎模型——全部免費開放下載。[Cosmos 模型下載已經超過 200 萬次](https://nvidianews.nvidia.com/news/nvidia-launches-cosmos-world-foundation-model-platform-to-accelerate-physical-ai-development)，黃仁勳的算盤很清楚：無論哪條路線最後勝出，訓練和推理都需要 NVIDIA 的 GPU。賣鏟子的人從不下場挖金礦——這是 1849 年加州淘金熱就證明過的商業智慧。

---

我自己怎麼看這五派？老實講，我覺得**短期內最賺錢的是第四派和第五派，最有可能改變 AI 範式的是第一派，最會被資本市場高估的是第三派，最會被低估的是第二派**。

第四派和第五派賺錢，因為他們解決的是真實付費客戶的具體問題（自駕模擬、機器人訓練），不需要等通用智能誕生。第一派如果賭贏，整個 LLM 範式都會被翻盤——這是 LeCun 的賭注合理性的根源。第三派——也就是阿里、騰訊、Google 這幾家——的問題是，他們的產品既不夠強到能訓練機器人，又跟既有的影片生成模型 differentiate 不夠清楚，很容易被罵成「只是更貴的 Sora」。

第二派被低估的原因是，3D 內容生成這個市場其實比大家想像的大。AAA 遊戲一個場景的美術成本動輒幾十萬美元，VR/AR 內容生產的瓶頸從來都是內容稀缺。Marble 如果能把這條成本曲線壓到原來的 1/10，會直接改寫遊戲、VFX、數位孿生三個產業的單位經濟學。

---

## 產業衝擊

把鏡頭從「誰會贏」拉開到「整個產業會怎麼變」，這場世界模型熱潮會在四個層面產生連鎖反應。

**第一層：直接受益者與直接受損者**

最直接受益的是兩類公司：**具身智能公司**和**自駕公司**。Agility Robotics 的 Digit 是目前唯一在商業場景產生實際營收的人形機器人，[已經在 GXO 倉庫搬了超過 10 萬個物流箱](https://www.agilityrobotics.com/content/digit-moves-over-100k-totes)，跟 Toyota、Mercado Libre 都有付費合約。它的訓練數據從哪來？很大一部分就是從 Cosmos 這類世界模型生成的合成資料。Figure AI 估值已經喊到 390 億美元、累積融資 19 億美元，背後同樣靠世界模型支撐訓練。

直接受損的是傳統的 3D 建模工具公司、CGI 工作室、純人工資料標註公司。一個 VFX 場景過去要 5 個美術畫一週，現在 Marble 一個 prompt 三分鐘搞定。一個自駕邊緣案例過去要租真車找空地拍幾百次，現在 Waymo World Model 在伺服器裡跑一晚上。中間消失的那些工作不會回來。

**第二層：商業模式衝擊**

這是最有意思的一層。世界模型重新定義了「內容」的單位經濟學。過去內容是一次性製作、長期變現（一部電影拍完賣十年）；世界模型把內容變成「即時生成、按互動付費」（玩家走進每一個場景都在當下生成）。這個改變直接影響三個產業的定價邏輯：

- **遊戲**：內容生成成本從「美術人力 × 時間」變成「GPU 算力 × token 數」。AAA 大作的開發成本曲線會重新洗牌，中小團隊有機會用 AI 拉平跟 EA、Activision 的內容差距。
- **影視**：VFX 鏡頭定價會從「按複雜度計費」滑向「按算力計費」。好萊塢工會現在還在打字幕公司，下一波要打的可能是世界模型公司。
- **教育、培訓、模擬**：飛行員訓練、外科手術模擬、危險作業培訓——這些過去需要昂貴硬體模擬器的場景，會被生成式世界模型攻擊。

**第三層：開發者生態**

這層最容易被低估。世界模型一旦成熟，整個遊戲開發、機器人開發、AR/VR 開發的工具鏈都會重組。過去你要做一個機器人 demo，需要懂 ROS、Gazebo、URDF、強化學習；未來你可能只需要在 Cosmos 裡寫個 prompt，加上幾段 Python 把感測器資料接出來。Unity 和 Unreal Engine 這幾年大力擁抱 AI 不是為了好玩，是因為他們知道遊戲開發的 IDE 之爭會在世界模型時代重新開打。

對軟體工程師個人來說，這代表一個新的技能交叉路口：如果你過去寫 backend，現在可能要學一點 3D 表示（NeRF、Gaussian Splatting）；如果你過去做遊戲開發，現在可能要學一點生成模型微調；如果你做 ML，物理模擬和 differentiable rendering 會變成必修。

**第四層：二階效應**

這層才是真正的長期變數。當 AI 真的能模擬物理世界，會觸發兩個非常不直觀的後果：

第一，**真實資料的價值會兩極化**。一方面，能精確標註動作-結果三元組的真實資料（例如機器人遙操作影片）會變得超級值錢，因為它是訓練世界模型的稀缺燃料；另一方面，普通的 YouTube 影片會被合成資料淹沒，網路上會充斥分不清楚是 AI 生成還是真實拍攝的「世界片段」。

第二，**內容真實性的法律框架會崩潰**。當任何人都能在筆電上生成 4K 解析度、物理正確、長時序連貫的「3D 世界片段」，現有的 deepfake 偵測技術基本失效。一個逼真的虛假災難現場、一段「拍到」政治人物在不存在的場景裡的 3D 重建——這些不是科幻劇本，是 18 個月內就會發生的事。

世界模型的倫理框架和法律邊界，遠遠落後於技術發展速度。當資本和媒體聚焦於「誰能造出最逼真的虛擬世界」時，沒有人在認真討論這個問題。

---

## 未來展望

那麼接下來會發生什麼？我把它分成短中長三個時間段。

**短期（3 到 6 個月，2026 年 Q3-Q4）**

幾乎可以確定的事：

1. 至少還會有 2 到 3 家世界模型公司宣布億美元級融資，因為矽谷 VC 不能不在這個 thesis 裡押注，FOMO 比理性更強。
2. NVIDIA 會繼續強化 Cosmos 平台，加上跟 Omniverse 更深度的整合。Q3 財報會議上，黃仁勳會把 Cosmos 下載數當成「物理 AI 採用率」的代理指標來講。
3. Waymo World Model、Wayve GAIA-3 會至少有一家發出第一個生產環境採用案例（已經在某個城市的測試車隊用上）。
4. 影視業會出現第一個用世界模型完成主要視覺特效的好萊塢電影，引爆 SAG-AFTRA 工會的下一輪抗爭。

**中期（6 到 18 個月，2026 Q4 到 2027 年中）**

這個區間有幾條可能的路徑：

- **路徑一（樂觀）**：World Labs 或 AMI Labs 至少一家拿出能讓開發者「直接用得上」的產品，世界模型從研究進入生產，年化 ARR 突破億美元。
- **路徑二（中性）**：技術繼續進步但商業化緩慢，幾家中小型世界模型新創開始裁員、被併購，市場從「五十家百花齊放」收斂到「三五家領跑」。
- **路徑三（悲觀）**：物理準確性的瓶頸被證明比預期更難突破，整個賽道進入「VR 化」——技術可行但找不到 killer app，資本退潮。

我自己賭路徑二的機率最高，大概 50-60%。理由是：歷史上每一次 AI 範式轉移都有一個 18-24 個月的「demo 很驚艷、但從 demo 到產品要爬一座大山」的階段。LLM 從 GPT-3 demo 到 ChatGPT 用 27 個月，世界模型沒理由更快。

**長期推演（3 到 5 年，2028-2030）**

如果這條線真的走通了，3 到 5 年後的世界會長什麼樣？

- 機器人在工廠、倉儲、餐廳、家庭裡的滲透率，會從 2026 年的「零星試點」變成「主流選項」，類似電動車從 2018 到 2024 的曲線。
- 自駕計程車從少數城市試營運變成大部分一線城市的日常服務，跟 Uber、Lyft 並列為交通選項。
- 遊戲產業會出現「全程 AI 生成的 AAA 大作」，定價從一次性 70 美元變成訂閱制，因為內容是無限的。
- 真實世界訓練資料變成國家級戰略資源，類似今天的稀土。中、美、歐會在「機器人遙操作資料庫」這件事上展開新一輪角力。

當然，這些都建立在「世界模型這條技術路線真的走得通」的前提上。如果走不通——也就是物理準確性永遠跨不過某個門檻——那麼上面這些預測就要全部打折，AI 進入物理世界的時間表會延後 5 到 10 年。

---

**所以，作為一個讀者，現在該怎麼辦？**

如果你是**開發者**：花一個週末搞清楚 Gaussian Splatting 和 NeRF 的基本原理，玩一下 Marble、Genie 3、HY-World 2.0 的 demo，建立直覺。如果你做遊戲或機器人，認真評估把 Cosmos 加進開發流程的可能性。不需要 all-in，但不能完全不碰。

如果你是**創業者或產品經理**：忘掉「世界模型」這個 buzzword，回到具體場景去問——我的客戶有什麼問題是「需要 AI 理解物理世界」才能解的？如果想不出來，這波熱潮跟你關係不大；如果想得出來，現在就是上車的時候，因為基礎模型團隊正在找 design partner。

如果你是**一般科技從業者**：不需要焦慮。世界模型不會像 ChatGPT 那樣三個月後就改變你的工作流程。但兩年後，你看影片、玩遊戲、坐車、跟機器人互動的方式，會跟今天非常不一樣。把這件事當成一個慢動作的、持續 5 年的範式轉移來追，不要追每一個發布會的 demo。

---

最後拋一個問題給你：當所有人都把錢押在「讓 AI 理解物理世界」上的時候，沒有人問——**讓 AI 真正理解物理世界，是 AI 進化的必經之路，還是只是矽谷下一個共同幻覺？**

也許答案要等到 2030 年才看得清楚。但接下來這 3 到 5 年的 50 億美元賭局，會把這個問題的答案一點一點逼出來。

我會持續追下去。

---

## 延伸閱讀

- [世界模型元年啟示錄：動機、亂戰與暗礁 — 36 氪](https://www.36kr.com/p/3769670392541961)：本文的觸發點，把五大派系的混亂講得最清楚的中文長文
- [Yann LeCun's AMI Labs raises $1.03 billion to build world models — TechCrunch](https://techcrunch.com/2026/03/09/yann-lecuns-ami-labs-raises-1-03-billion-to-build-world-models/)：AMI Labs 種子輪細節，包含投資人名單和商業化時間表
- [Fei-Fei Li's World Labs speeds up the world model race with Marble — TechCrunch](https://techcrunch.com/2025/11/12/fei-fei-lis-world-labs-speeds-up-the-world-model-race-with-marble-its-first-commercial-product/)：Marble 商業化的第一手報導，含 VFX 業界使用案例
- [The Waymo World Model: A New Frontier For Autonomous Driving Simulation — Waymo Blog](https://waymo.com/blog/2026/02/the-waymo-world-model-a-new-frontier-for-autonomous-driving-simulation/)：自駕公司怎麼真的把世界模型用起來，最具體的落地案例
- [Genie 3: A new frontier for world models — Google DeepMind](https://deepmind.google/blog/genie-3-a-new-frontier-for-world-models/)：Genie 3 官方技術說明，含已知的限制（60 秒上限、地理準確性問題）
- [NVIDIA Cosmos World Foundation Models — NVIDIA](https://www.nvidia.com/en-us/ai/cosmos/)：Cosmos 平台官方說明，看 NVIDIA 怎麼定位「世界模型基礎設施」這層
- [Tencent HY-World 2.0 — GitHub](https://github.com/Tencent-Hunyuan/HY-World-2.0)：騰訊開源世界模型的程式碼倉庫，可以直接 clone 下來用
- [Critiques of World Models — arXiv](https://arxiv.org/abs/2507.05169)：學術界對世界模型現有研究的系統性批評，從資料、表示、架構、目標、用法五個維度提出問題
- [JEPA vs LLM: The 2026 Guide to AI's Next Revolution — CreateBytes](https://createbytes.com/insights/jepa-vs-llm-ai-collaboration)：把 JEPA 跟 LLM 的根本差異講清楚，看 LeCun 為什麼這麼堅持
- [Digit Moves Over 100,000 Totes in Commercial Deployment — Agility Robotics](https://www.agilityrobotics.com/content/digit-moves-over-100k-totes)：人形機器人真實商業營運的第一個里程碑，看世界模型的下游應用長什麼樣
