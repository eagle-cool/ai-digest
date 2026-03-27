---
title: "ARC-AGI-3 血洗大模型、Google TurboQuant 嚇崩記憶體股"
date: 2026-03-27
description: "ARC-AGI-3 新基準測試讓所有頂尖模型得分低於 1%，Google TurboQuant 記憶體壓縮技術引爆存儲晶片拋售潮，NeurIPS 將 873 家中國機構排除在外引發學術界反彈。"
tags: [llm, ai-research, ai-industry, ai-tools, ai-coding]
---

今天 AI 圈被兩記重拳打醒——ARC-AGI-3 直接把所有大模型打回原形，人類滿分、AI 連 1% 都拿不到；Google 丟出 TurboQuant 記憶體壓縮技術，存儲晶片股一天蒸發超 6200 億人民幣。另外 NeurIPS 把 873 家中國機構踢出學術圈的事也炸了鍋，這浪今天有點大。

---

## 🌊 今日浪頭

### [ARC-AGI-3 出爐：人類滿分、AI 全線低於 1%](https://www.36kr.com/p/3739700584644867)

我看完 ARC-AGI-3 的結果，整個人是震撼的。上一代 ARC-AGI-2 裡還能拿 69.2% 的 Opus 4.6，這次直接跌到 0.2%。不是小數點打錯——就是零點二。人類玩家？輕鬆拿下 100%。

這次測試從「靜態題目」升級成了 150 多個互動式遊戲環境，超過 1000 個關卡。沒有任何說明、沒有提示，AI 被丟進去只能自己摸索規則。評分公式更狠：(人類步數/AI步數)²，也就是說 AI 多走一步，分數就斷崖式下跌。

最反直覺的發現是：排行榜前三名全是非 LLM 方案——CNN、規則搜索、幀圖匹配。參數量越大的模型反而越容易「腦補」錯誤框架然後一路死磕。簡單說，現在的大模型是「記了很多答案的應試高手」，但完全不會「學習怎麼學習」。

**為什麼這道浪值得追：**
- 這是目前全球唯一尚未被 AI 飽和的基準測試，85 萬美元獎金池等著突破者
- 暴露了 LLM 最深的裂縫：缺乏元認知能力，不知道自己不知道
- 黃仁勳剛說我們已經實現 AGI，ARC-AGI-3 直接打臉——或許連 1% 都沒到

### [Google TurboQuant 記憶體壓縮 6 倍，存儲股一天蒸發 6200 億](https://www.36kr.com/p/3740464246784001)

Google Research 發布 TurboQuant 向量量化壓縮演算法，號稱在不損失準確率的前提下把 LLM 的 KV Cache 記憶體佔用壓到 3-bit——原本的六分之一。科技圈直接把它捧成「真實版 Pied Piper」和「Google 版 DeepSeek」。

但資本市場反應更激烈：三星、SK 海力士、美光等存儲巨頭市值一天蒸發超 900 億美元。閃迪盤中暴跌 6.5%，美光跌 4%。市場邏輯很直接——如果記憶體需求被壓縮六倍，那晶片還賣給誰？

不過華爾街分析師們反倒很淡定，直接喊「抄底」。Lynx Equity 指出 8 倍性能提升是跟過時的 32-bit 模型比的，現有推理模型早就用 4-bit 量化了。摩根士丹利更搬出了傑文斯悖論：效率提升降低成本 → 更多場景落地 → 總需求反而增加。以我的觀察，這更像是 DeepSeek 事件的翻版——短期恐慌，長期利多。

**為什麼這道浪值得追：**
- TurboQuant 在 H100 上實現最高 8 倍性能提升，對推理成本影響巨大
- 只影響推理階段的 KV Cache，不影響訓練和模型權重的 HBM 需求
- 效率革命的真正意義不是「用更少」，而是「讓更多人用得起」

### [NeurIPS 封殺 873 家中國機構，學術圈怒了](https://www.36kr.com/p/3739574779838728)

AI 三大頂會之一的 NeurIPS 今年新增條款，根據美國 OFAC 制裁名單，禁止相關機構投稿，連審稿、擔任編輯等學術服務都一併切斷。受影響的包括華為、商汤、曠視、大疆、中芯國際、三大電信商等 873 個條目，基本上把中國 AI 核心力量一刀切掉了。

中國計算機學會（CCF）立刻開砲，倡議全體中國學者拒絕投稿和審稿，並警告若不改正將把 NeurIPS 移出推薦目錄。多位學者公開拒絕擔任領域主席，有人直接發出措辭強烈的拒審信。

這事最荒謬的地方在於：NeurIPS 2025 裡清華大學以 390 篇論文位列全球第一，很多受影響企業過去多年還是 NeurIPS 的贊助方。收錢的時候不嫌棄，發論文的時候就翻臉，這操作確實讓人說不出話。

**為什麼這道浪值得追：**
- 這是繼 2019 年 IEEE 事件後，AI 學術圈最大規模的地緣政治衝突
- NeurIPS 是唯一採取此政策的頂會，ICML 和 ICLR 目前未跟進
- 中國 AI 論文產出已佔全球頂會重要份額，學術脫鉤的代價雙方都承受不起

---

## ⚡ 衝浪快報

- **[Cursor 放出 Composer 2 技術報告，坦承基於 Kimi K2.5 微調](https://www.36kr.com/p/3740414075011328)** — 上次被抓包「套殼」後終於學乖，老老實實署名基底模型，還跟 Kimi 官方達成和解了
- **[千問前負責人林俊旸離職後首發長文，反思推理模型到 Agent 的轉向](https://www.36kr.com/p/3740411566276871)** — 坦承「我們沒有全做對」，Qwen3 的混合思維模式最終 thinking 變得囉嗦猶豫，這反思挺真誠的
- **[Apple 將在 iOS 27 開放第三方 AI 聊天機器人接入 Siri](https://www.theverge.com/tech/902048/apple-siri-ai-chatbot-update-ios-27)** — 不只 ChatGPT，未來 Claude、Gemini 都能當 Siri 的大腦，Apple 終於想通了
- **[Google 發布 Gemini 3.1 Flash Live 語音模型](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-1-flash-live/)** — 主打更自然的即時語音對話，已部署到多個 Google 產品，Ars Technica 說聽起來越來越難分辨是不是機器人了
- **[GitHub Copilot 新規：4 月起預設用你的程式碼訓練 AI](https://www.36kr.com/p/3739631774892295)** — Free、Pro、Pro+ 用戶的互動數據將成訓練素材，Business 和 Enterprise 不受影響，又是個 opt-out 陷阱
- **[Kimi（月之暗面）傳考慮赴港 IPO，估值衝上 180 億美元](https://www.36kr.com/p/3740465529684233)** — 三個月內三輪融資、估值翻四倍，速度快到連創始人之前說的「短期不急上市」都打了臉
- **[xAI 聯合創辦人 11 人走了 10 人，只剩特斯拉嫡系獨苗](https://www.36kr.com/p/3739403701420037)** — 馬斯克自己都承認「xAI 一開始就沒建對」，現在要從根基重來，這人才流失率也是沒誰了
- **[微信首頁上線 AI 插件 Clawbot，各類「龍蝦」產品的接入入口](https://www.36kr.com/p/3739641264177155)** — 微信一向謹慎克制，這次居然把 AI 放到首頁，雖然功能還很陽春，但信號意義巨大
- **[歐盟投票延後 AI Act 關鍵條款，同時禁止 nudify 換臉脫衣 App](https://www.theverge.com/ai-artificial-intelligence/901315/eu-ai-act-delays-ban-nudify-apps)** — 合規期限往後推但裸照 App 禁令先行，歐盟的 AI 監管節奏越來越微妙
- **[Wikipedia 正式禁止 AI 生成文章](https://www.theverge.com/tech/901461/wikipedia-ai-generated-article-ban)** — 理由是 AI 寫作違反多項核心內容政策，人類知識庫對 AI 內容畫下紅線
- **[字節跳動 Seedance 2.0 AI 影片生成模型登陸 CapCut](https://techcrunch.com/2026/03/26/bytedances-new-ai-video-generation-model-dreamina-seedance-2-0-comes-to-capcut/)** — Sora 剛死、字節就加碼，還內建了真人臉部和智財權保護機制
- **[Mistral 發布開源語音生成模型](https://techcrunch.com/2026/03/26/mistral-releases-a-new-open-source-model-for-speech-generation/)** — 讓企業自建語音 Agent，直接對標 ElevenLabs 和 OpenAI，語音 AI 的開源競爭正式白熱化

---

## 🏄 深水區

- **[Quantization from the Ground Up](https://simonwillison.net/2026/Mar/26/quantization-from-the-ground-up/#atom-everything)** — 今天 TurboQuant 炸場之後讀這篇剛好，Sam Rose 做了一篇超級精美的互動式長文解釋 LLM 量化的底層原理，連浮點數的視覺化解釋都做到了極致，是我見過最好的量化入門教材
- **[Thoughts on Slowing the Fuck Down](https://simonwillison.net/2026/Mar/25/thoughts-on-slowing-the-fuck-down/#atom-everything)** — Pi agent 框架作者 Mario Zechner 的逆風發言：我們在 Agent 狂熱中放棄了所有紀律和主體性，變成了一種癮。在大家都在衝浪的時候，偶爾需要有人提醒你浪也會把你打翻
- **[軟體淪為廉價「管道」後：上下文為王](https://www.36kr.com/p/3715450505359752)** — SaaS 的黃金時代正在終結，AI 讓軟體本身變得廉價，但「指揮」軟體的上下文層正在成為兆級新戰場。如果你在做 SaaS，這篇值得認真讀完
