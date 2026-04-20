---
title: "DeepSeek 100億估值放風、中國大模型集體轉賣 Token、記憶體荒撐到 2030"
date: 2026-04-20
description: "DeepSeek 終於鬆口融資但 100 億估值低得不合常識；中國六家大模型公司同時棄 C 端轉賣 Token，但 Cursor 模式根本搬不過來；記憶體短缺直接被定性為結構性，AI 把好東西全拿走了。"
tags: [llm, ai-industry, ai-tools, mlops]
---

今天 AI 圈的浪有點怪——不是某個新模型炸場，而是三條線同時收緊：DeepSeek 終於開放融資但估值低得詭異、中國六家大模型公司同步棄 C 端轉賣 Token、記憶體被 AI 吃乾淨到 2030 年才有救。三件事看似無關，拼起來才是 2026 年中國 AI 產業真正的底圖。

---

## 🌊 今日浪頭

### [DeepSeek 百億美元估值融資傳聞背後的四重邏輯判斷](https://www.36kr.com/p/3774394570982144)

DeepSeek 傳出要以 100 億美元估值放出 3% 股權、融資約 3 億美元，這是梁文鋒從 2023 年成立以來的首輪外部融資。我看了一下這個數字組合，越看越覺得有意思——對標一下：智譜港股市值 507 億美元、MiniMax 344 億美元、月之暗面 180 億美元，DeepSeek 100 億的估值低得不像話。但這恰恰是創辦人主動設下的篩選機制，過低的價格能直接過濾掉那些對財務回報斤斤計較的機構。更精妙的是 3 億美元剛好等於幻方量化過去三年對 DeepSeek 的累計投入——這輪融資完成後，DeepSeek 在財務意義上正式從幻方獨立出來。

**為什麼這道浪值得追：**
- 真正的目的不是融錢，是給員工期權做市場化定價——過去一年 DeepSeek 被精準挖走五個核心成員（V2 關鍵作者羅福莉去小米千萬年薪、R1 核心郭達雅去字節近億總包），人才保衛戰已經打不下去了
- 「外人拿不到份額」說明這是一場規則完全由梁文鋒設定的遊戲，外部資本只是配角
- V4 一直推遲、市場信心鬆動，這時候放融資消息本身就是「組織進化」對沖「技術節奏不確定」的訊號操作，比 3 億美元現金更值錢

### [國產大模型集體轉身](https://www.36kr.com/p/3774435677766151)

這篇真的把過去 60 天中國 AI 圈的暗流講透了。智譜、MiniMax、阿里、字節、DeepSeek、百度六家公司，幾乎在同一時間集體做同一件事——從賣算力、做專案，轉向賣 Token、做訂閱。表面上看大家都在抄 Anthropic 的 Claude Code 和 Cursor 的訂閱模式（Claude Code 三個月年化從 10 億翻到 25 億、Cursor 估值從 293 億飆到 500 億），但作者的拆解很犀利：海外那套商業模式根本搬不過來。

**為什麼這道浪值得追：**
- 智譜押「付費習慣可以教育」，半年漲價三次，最高檔從 80 美元飆到 160 美元，硬是要證明中國開發者也願意為 Coding 工具持續買單
- 阿里的吳泳銘親自下場合併五個事業群成立 ATH 事業群，目標從「賣算力」直接改成「賣 Token」，下血本押規模
- 三道致命的坎：中國開發者二十年的「免費」肌肉記憶、海外位置已被 Cursor 這類玩家佔死（Cursor 用 Kimi K2.5 當底座壓成本，Cursor 賺 500 億估值，Kimi 喝湯）、國產 Token 單價只有 Claude 的 1/5 到 1/12，訂閱制的數學根本算不通

### [記憶體不夠用這件事，可能要持續到 2030 年](https://www.36kr.com/p/3773256167572229)

Nikkei Asia 報告直接把記憶體短缺定性為「結構性」，不是短期漲價。即便到 2027 年底，三星、SK 海力士、美光全力擴產，也只能滿足全球 60% 的需求。SK 集團董事長更悲觀，直接說可能要拖到 2030 年。原因講白了就一句話——AI 把所有好東西都拿走了。新建的晶圓廠絕大部分產能流向利潤更高的 HBM（高頻寬記憶體），消費級 DRAM 只能撿剩的。

**為什麼這道浪值得追：**
- AI 數據中心對 HBM 的胃口無底洞，OpenAI 那批巨頭直接包走全球將近一半的 DRAM 月產量
- 谷歌上個月發的 TurboQuant 壓縮算法雖然能讓大模型記憶體佔用減 6 倍以上（一度讓美光、西部數據股價閃崩），但軟體優化追不上物理產能缺口
- 對消費者的實際影響：智慧型手機、筆電、VR 頭顯、遊戲掌機全要漲價或「隱形降級」，原本 16GB 升 32GB 的節奏會被打亂，Meta Quest 已經宣布漲價 50–100 美元了

---

## ⚡ 衝浪快報

- **[Vercel was hacked](https://www.theverge.com/tech/914723/vercel-hacked)** — 主流前端部署平台 Vercel 被攻破，自稱 ShinyHunters 成員的駭客在叫賣資料。如果你的 side project 託管在上面，今晚記得檢查一下環境變數
- **[更新越頻繁，Claude Code 與 Codex 越像](https://www.36kr.com/p/3773678223262467)** — OpenAI 發 GPT-5.4-Cyber，目標客群、應用場景、宣發策略幾乎完全對標 Anthropic 的 Claude Mythos。連紐約時報都點破了「貼身肉搏」這四個字
- **[巨頭都在搶光芯片](https://www.36kr.com/p/3773208573723397)** — NVIDIA 一天內向 Lumentum 和 Coherent 各砸 20 億、三週後再給 Marvell 20 億，光通訊產業 M&A 節奏密集到讓人眼花。電子的物理極限快到了，光算開始登場
- **[核電的價值重估：從電力基荷到 AI 終極能源](https://www.36kr.com/p/3773456925377026)** — Meta 一個月內連簽三份核電大單合計近 4500 兆瓦，微軟、Google、Amazon、Oracle 全部跟進。AI 軍備競賽的主角從晶片變成核電廠
- **[OpenAI's former Sora boss is leaving](https://www.theverge.com/ai-artificial-intelligence/914463/openai-sora-bill-peebles-kevin-weil-leaving-departing)** — Sora 團隊負責人 Bill Peebles 上週五宣布離開 OpenAI。一個月前 OpenAI 才剛放棄 Sora 影片生成工具，現在連帶頭的人也走了
- **[楊立昆開噴 Anthropic CEO](https://www.36kr.com/p/3773691953230336)** — LeCun 轉發 Dario「AI 一到五年內會消滅 50% 科技工作」的影片並補刀「別信那個賣 AI 的人」。AI 大佬內鬥已經不演了，直接公開撕
- **[十一個為什麼，看懂亦莊機器人馬拉松](https://www.36kr.com/p/3773382357971713)** — 去年的冠軍「天工 Ultra」今年衝過終點線後沒減速，直接歪頭衝進綠化帶，工程師用擔架把它抬走。現場觀眾笑說「機器人也被勝利沖昏了頭」，但這場賽事本身才是值得追的產業節點
- **[AI 廠商的 Token 經濟學：先養龍蝦再養馬](https://www.36kr.com/p/3773626643694081)** — Hermes Agent 一夜爆紅，OpenRouter Token 消耗日榜衝到第二，僅次於 OpenClaw。Token 消耗榜現在比下載榜還能反映 AI 工具的真實使用熱度
- **[Building a Fast Multilingual OCR Model with Synthetic Data](https://huggingface.co/blog/nvidia/nemotron-ocr-v2)** — NVIDIA 發 Nemotron OCR v2，多語言 OCR 用合成資料訓練，做 RAG/文檔處理的可以收藏
- **[「理想系」開始批量生產獨角獸](https://www.36kr.com/p/3773140530938375)** — 李想一邊喊「把出走的人招回來」一邊投錢給前 AI 首席科學家陳偉創辦的具身智慧公司「斜躍智能」。理想系人才正在變成比車本身更值錢的資產
- **[宇樹證明了自己，現在輪到智元了](https://www.36kr.com/p/3773109807985159)** — 智元機器人辦了一場規格高得反常的行業大會，2500 個座位坐滿，34 國客戶到場，四種語言同傳。創辦人鄧泰華直接公開核心經營數據，這在新創公司很少見

---

## 🏄 深水區

- **[Headless everything for personal AI](https://simonwillison.net/2026/Apr/19/headless-everything/)** — Simon Willison 引用 Matt Webb 的觀察：當 personal AI 變主流，無頭服務（headless services）會比有 UI 的服務更搶手。一個關於下一代 SaaS 形態的小型預言，值得花十分鐘讀
- **[Changes in the system prompt between Claude Opus 4.6 and 4.7](https://simonwillison.net/2026/Apr/18/opus-system-prompt/)** — Anthropic 是唯一公開 user-facing system prompt 的大廠，而且還做了 archive。Simon 直接把 4.6 到 4.7 的 diff 拆給你看，做 prompt engineering 的必讀
- **[30% 跌幅只是開始？AI 正在吞噬應用軟體](https://www.36kr.com/p/3736699113455625)** — 從 ChatGPT 發布以來上市軟體 ETF 累積漲幅在 2026 年初被一次抹平。文章不只是哭天喊地，而是論證真正的 SaaS 護城河剛剛才浮出水面，軟體業才剛要變大
- **[果然，最恨 AI 的人，是大學畢業生](https://www.36kr.com/p/3773230505820930)** — Pew 和蓋洛普的數據都指向同一件事：Z 世代雖然每天用 AI，但對 AI 的恨意也是所有世代裡最高的。「使用」與「認同」之間的裂縫，可能比你想像中更危險
- **[Agent 時代，訓練師的核心技能不再是寫 Prompt](https://www.36kr.com/p/3774392528454406)** — Prompt 工程師這個職位的熱度今年明顯降溫，取而代之的是系統思維、工具理解、異常處理。如果你還在練 prompt 黑話，這篇可以當作職涯預警
