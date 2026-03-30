---
title: "xAI 創始團隊全滅、Mythos 5.0 悄悄開測、Karpathy 押注反 Scaling Law"
date: 2026-03-30
description: "馬斯克 xAI 11 位聯合創始人全部離職，Claude Mythos 5.0 Beta 開始內測推送，Karpathy 站台 Flapping Airplanes 挑戰算力暴力路線"
tags: [llm, agents, ai-industry, ai-research, ai-coding, ai-tools]
---

今天 AI 圈的浪打得特別狠——馬斯克的 xAI 創始天團直接團滅，11 個聯合創始人一個不剩；Anthropic 這邊則是偷偷把 Mythos 5.0 Beta 塞進了部分開發者的 Claude Code 裡，還沒正式發布就已經讓人脊背發涼。而 Karpathy 站出來力挺一群 25 歲的年輕人，說他們要掀翻整個 Scaling Law 的桌子。週末的消息量，比工作日還猛。

---

## 🌊 今日浪頭

### [只剩馬斯克自己，xAI 11 個聯合創始人跑光了](https://www.36kr.com/p/3744588844302343)

3 月 28 日，Ross Nordeen 安靜地摘掉了 X 平台上的 xAI 員工認證，發了張「摸草」的照片就走了。他是 xAI 除馬斯克外最後一位聯合創始人——負責統籌公司運營、一手搭建了 20 萬張 H100 的超算集群 Colossus。他走了，意味著 2023 年馬斯克親手拉起的 11 人創始天團，三年內 100% 離職，一個不剩。

這事的震撼點不只是人走了，而是這些人來自 Google DeepMind、OpenAI、Google Brain——AI 界最頂尖的人才組合。其中 Jimmy Ba 是 Adam 優化器論文的聯合作者（引用量 9.5 萬次），據報離職跟馬斯克對模型性能的嚴厲要求有關。馬斯克自己 3 月 13 日也罕見坦白：「xAI 第一次沒搭對，正在從地基重建。」一家估值 2500 億美元的公司，創始人自己說要推倒重來——這在矽谷 CEO 發言史上堪稱名場面。

**為什麼這道浪值得追：**
- 11 人創始團隊 100% 離職率，在矽谷創業史上極為罕見
- 馬斯克從 Cursor 挖了兩名高管補血，但研究團隊的默契和方法論不是招幾個人就能恢復的
- AI 人才市場白熱化——Meta 為留人開出 4 年 3 億美元的薪酬包，xAI 的人才外流將直接改變行業版圖

### [Claude Mythos 5.0 Beta 驚現內測，90 分鐘攻破 20 年 Linux 漏洞](https://www.36kr.com/p/3744583655145473)

泄漏才過兩天，Anthropic 就急不可待了。開發者們曬出截圖——Claude Mythos 5.0 Beta 已開始灰度推送，在 Claude 和 Claude Code 中同時現身，被官方標註為「規模更大、更智能」的下一代模型。Polymarket 預測 6 月正式上線的機率高達 73%。

但更讓我頭皮發麻的是 Opus 4.6 當前的實力展示。在舊金山的 [un]prompted 大會上，安全研究員 Nicholas Carlini 現場演示：Claude 在 90 分鐘內自主發現了 Ghost CMS 的盲 SQL 注入漏洞，竊取了管理員 API 密鑰；接著又在 Linux 內核的 NFSv4 守護程序中挖出了 2003 年就存在的堆緩衝區溢出漏洞——連資深安全專家手動審計都極難發現的那種。Carlini 直言：「這相當、相當可怕。」而 Mythos 5.0 比這還強，強到 Anthropic 自己都怕了。

**為什麼這道浪值得追：**
- Mythos 5.0 內部訓練已完成，遲遲不發布的原因是「太強大也太危險」
- Anthropic 內部已進入「完全 AI 對齊」模式——Claude Code 創建者 Boris Cherny 自去年 11 月起 100% 代碼由 AI 生成
- AI 自主發現零日漏洞的能力正在跨越門檻，攻防格局將被徹底改寫

### [Karpathy 緊急叫停：別再餵數據了，AGI 方向全錯](https://www.36kr.com/p/3744588433162504)

Karpathy 在 X 上翻牌了一家叫 Flapping Airplanes 的新實驗室——三個平均年齡 25 歲的年輕人，剛拿了 GV、紅杉和 Index Ventures 的 1.8 億美金種子輪。他們的核心論點很簡單也很狂：人腦只需要 20 瓦就能搞定邏輯和創造力，而 GPT-5 得燒掉半個核電站才能陪你聊天，中間差了 6 個數量級的能效比。現在的 Scaling Law 就像給飛機黏上羽毛強行拍翅膀，而不是去理解空氣動力學。

他們的技術武器叫 Megakernels——把 LLM 推理的所有計算和通信融合進單個 GPU 核，消除指令流轉的空隙，推理速度直接暴拉 6.7 倍。Karpathy 的評價一針見血：10 倍性能提升的機率依然很高，但不是靠堆更多 Rubin 晶片，而是靠改變數學本質。

**為什麼這道浪值得追：**
- Epoch AI 預測高品質互聯網數據已接近枯竭，「大力出奇跡」的路線正在撞牆
- Megakernels 技術實現 6.7 倍推理加速，不需要更多硬體
- 如果效率突破成真，靠賣算力和賣電活著的萬億市值巨頭將面臨存在性威脅

---

## ⚡ 衝浪快報

- **[Bluesky's new app is an AI for customizing your feed](https://www.theverge.com/ai-artificial-intelligence/903190/bluesky-attie-ai-custom-feeds)** — Bluesky 推出 Attie，用 Claude 驅動的 AI 助手幫你打造個人化演算法，去中心化社交 + AI 的組合拳蠻有意思的
- **[Google TurboQuant 論文塌房，被曝抄襲華人學者成果](https://www.36kr.com/p/3743978774921472)** — 幹崩存儲股的那篇論文反轉了，蘇黎世聯邦理工博士後高健揚指出三大問題：系統性迴避與 RaBitQ 的相似性、錯誤描述理論結果、貶低原創貢獻
- **[AI 教父 Hinton 不用 ChatGPT 了](https://www.36kr.com/p/3744688405823494)** — 2024 諾貝爾物理學獎得主公開表示已棄用 ChatGPT，花了 60 分鐘解釋他最擔心的三件事：失控、失業、貧富差距加大
- **[25 歲退學生造出 110 億獨角獸 Axiom](https://www.36kr.com/p/3744583895023872)** — 洪樂潼讓大模型推理像數學證明一樣嚴格可驗證，Menlo Ventures 領投 2 億美元 A 輪，估值 16 億美元，成立不到一年就進獨角獸俱樂部
- **[AI 人臉辨識冤枉逮捕田納西州女子](https://www.cnn.com/2026/03/29/us/angela-lipps-ai-facial-recognition)** — 北達科他州的案件讓田納西州女子被錯誤逮捕，HN 86 分熱議，AI 執法的誤判風險再次被推上風口浪尖
- **[Miasma：讓 AI 爬蟲掉進無盡毒坑的開源工具](https://github.com/austin-weeks/miasma)** — HN 177 分爆款，一個反 AI 爬蟲的陷阱生成器，用 AI 生成的垃圾內容餵養那些未經授權的爬蟲
- **[大模型摧毀線上教育商業模式](https://www.36kr.com/p/3744662537093124)** — Chegg 股價從 2021 年高點 113 美元跌到 0.57 美元，跌幅超過 99%，成為 AI 浪潮吞噬傳統商業模式的最鮮明注腳
- **[馬斯克 Terafab 晶片計劃啟動招聘](https://www.36kr.com/p/3744613041651717)** — 年薪 233 萬人民幣招光刻工程師，目標年產 1 太瓦算力（全球 AI 算力年產出的 50 倍），SpaceX 定義為「邁向銀河文明的下一步」
- **[OpenClaw 引爆賽博大屠殺風險](https://www.36kr.com/p/3744583116996873)** — 有開發者直接開放銀行帳戶、iMessage、2FA 給 AI 助手，只為問家裡還剩幾袋凍餃子，「生產力色情」的定義被重新整理了
- **[電費只佔 5%，GPU 才是吃掉算力成本的怪獸](https://www.36kr.com/p/3743467139170568)** — 沐曦披露 1GW 數據中心成本分析：總擁有成本 550 億美元，GPU 佔 250 億，電費才 27.5 億，「中國電價優勢」的敘事被推翻了

---

## 🏄 深水區

- **[The mirage of visual understanding in current frontier models](https://garymarcus.substack.com/p/the-mirage-of-visual-understanding)** — Stanford 新論文揭露前沿模型的「視覺理解海市蜃樓」：模型會對根本沒提供的圖片生成詳細描述和推理過程，包括帶偏見的臨床發現。Gary Marcus 轉發加碼，值得細讀
- **[What if AI doesn't need more RAM but better math?](https://adlrocha.substack.com/p/adlrocha-what-if-ai-doesnt-need-more)** — HN 128 分，從數學角度探討 AI 效率瓶頸，跟今天 Karpathy 站台 Flapping Airplanes 的邏輯完美呼應，可以對照著看
- **[The first 40 months of the AI era](https://lzon.ca/posts/other/thoughts-ai-era/)** — HN 150 分，一篇冷靜的 AI 時代回顧：從 ChatGPT 發布到現在 40 個月，哪些預測對了、哪些錯了、我們學到了什麼
- **[模型已經有了內省能力，但過去它的心門上了鎖](https://www.36kr.com/p/3744622642954498)** — 推翻了「推理鏈是事後敘事」的共識，Emory 大學新研究發現模型確實在用推理鏈驅動輸出，不只是編好看的故事
