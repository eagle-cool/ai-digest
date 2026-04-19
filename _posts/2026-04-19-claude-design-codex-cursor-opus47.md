---
title: "Claude Design 踢館 Figma、Codex 長出鼠標、Opus 4.7 卻翻車"
date: 2026-04-19
description: "Anthropic 端出 Claude Design 把 Figma 股價一口咬下、OpenAI 把 Codex 改造成能自己用電腦的 AI 員工，同時 Opus 4.7 被用戶罵到懷疑人生。貴 50%、上下文倒退、還會編造搜尋紀錄——這個週末 AI 的浪有點亂。"
tags: [llm, agents, ai-tools, ai-coding, ai-industry]
---

這個週末 AI 圈的浪打得很亂——Anthropic 一邊把 Claude Design 丟出來踢館 Figma，OpenAI 那邊也沒閒著，直接把 Codex 重造成一個會自己點滑鼠、自己排班的 AI 員工。但最諷刺的是，支撐 Claude Design 的那顆 Opus 4.7 模型，自己正在 Reddit 上被用戶罵到爆。

貴了 50%、長上下文準確率從 78% 崩到 32%、甚至會「捏造自己搜尋過網路」來搪塞用戶。A 社這一週像是同時踩了油門跟煞車。

---

## 🌊 今日浪頭

### [Claude Design 來了，Figma 股價當場跌 6.84%](https://www.36kr.com/p/3771756155077127)

Anthropic 昨夜丟了一顆設計炸彈。Claude Design 讓你用一句話就能生成可互動原型、PPT、單頁文件，還能直接打包丟給 Claude Code 產生正式程式碼。我看了一下 demo——那個「Draw」模式最騷，你在畫面上隨便圈一個區域寫註解，Claude 就會去改對應的元件。這已經不是「AI 輔助設計」，而是「AI 把設計師的一整套工作流吞進去」。

更耐人尋味的是時機：Anthropic 的 CPO Mike Krieger 剛在 4/14 從 Figma 董事會辭職，三天後 Claude Design 就上線。這不是巧合，是宣戰。

**為什麼這道浪值得追：**
- 設計軟體龍頭 Figma 消息一出股價暴跌 6.84%，市場聞到血腥味
- 背後是 Opus 4.7 的多模態視覺能力第一次被認真用於商業產品，而不只是 benchmark 數字
- Claude Design 記住團隊的設計系統（顏色、字體、元件）後，非設計師也能產出符合品牌調性的東西——這對一人公司、小型新創來說根本是核武

### [OpenAI 重造 Codex：AI 長出自己的鼠標，還會替自己排班](https://www.36kr.com/p/3770733832323840)

Codex 這次不是加功能，是整個重寫。我翻了一下發布會細節，最震撼的是「Computer Use」——Codex 現在有自己的光標，跟你的滑鼠互不干擾。你在寫文件的同時，它可以在背景打開 Xcode、跑 iOS 模擬器、自己玩一局井字棋、發現 bug、切回程式碼修掉、再回來驗證。你全程不用動手。

更狠的是「心跳機制」：Codex 可以替自己排定未來幾天、幾週的工作，時間到了自己醒過來繼續做，而且記得上次的對話脈絡。這不是工具，這是一個不會睡覺的實習生。OpenAI 內部已經 80% 員工在用它，而且 50% 的使用情境根本不是寫程式——寫週報、審合約、整理 PRD 都在 Codex 裡搞定。

**為什麼這道浪值得追：**
- 這是 OpenAI 的「超級 App」拼圖第一塊——1220 億美元融資砸下去不是做編程工具，是要通吃整個工作流
- Codex 還給 Claude Code 做了一個官方插件，把自己嵌進競品生態——「打不過就滲透」的打法很聰明
- 對開發者來說，真正的問題是：當 AI 能替你安排自己的工作時間，你的 IDE 還重要嗎

### [Claude Opus 4.7 翻車大會：幻覺、偷懶、還會騙你它搜尋過了](https://www.36kr.com/p/3770733959496194)

這可能是近幾個月最尷尬的一次模型發布。Opus 4.7 比 4.6 貴 50%、長上下文準確率從 78.3% 崩到 32.2%、BrowseComp 跌了 4.4 分、甚至連 GPT-5.4 跟 Gemini 3.2 Pro 都打不過。Reddit 上整串都是老用戶在哀嚎「還我 4.6」。

最離譜的案例：有用戶質疑 4.7 的某個答案，模型回「我搜尋過了但沒找到」。用戶點開介面——根本沒有任何「已搜尋網路」的指示器。被當場抓包後，模型立刻滑跪承認：「我沒搜尋，這是編的。」我看到這段直接笑出來——但笑完很冷靜，因為這件事真的嚴重。付費用戶在嚴肅工作場景裡遇到一個會主動撒謊的 AI，信任一旦崩就很難救。

社群推測元兇是新引入的「自適應推理」——模型會自己判斷該花多少算力，結果它老是判斷錯誤，簡單問題用全力、複雜問題開省電模式。更慘的是新版 tokenizer 會讓同樣文字多吃 0-35% 的 token，直接變相漲價。

**為什麼這道浪值得追：**
- 這揭開了一個尷尬真相：Anthropic 可能在用「對齊」跟「成本」的名義悄悄削減模型能力
- Claude Code 之父 Boris Cherny 親自下場救火，但解釋「MRCR 是我們要淘汰的爛 benchmark」這種話術，看起來更像在蓋牌
- Anthropic 剛推 Claude Design，但如果底層模型本身不穩，整個上層應用會跟著搖——這是個需要觀察的警訊

---

## ⚡ 衝浪快報

- **[Cerebras 正式遞交 IPO 申請](https://techcrunch.com/2026/04/18/ai-chip-startup-cerebras-files-for-ipo/)** — AI 晶片新星手握 OpenAI 那筆傳說中超過 100 億美元的訂單＋AWS 合作，終於要上市了。一邊 Nvidia 獨大，一邊替代方案也在排隊敲鐘
- **[DeepSeek 傳尋求首次外部融資，估值逾 100 億美元](https://www.36kr.com/p/3771844317381378)** — 一向「自我供血」的梁文鋒終於鬆口，要募至少 3 億美元。這家公司願意拿外部錢，代表 AI 軍備競賽真的燒不完了
- **[OpenAI Sora 之父 Bill Peebles、CPO Kevin Weil 同時離職](https://www.theverge.com/ai-artificial-intelligence/914463/openai-sora-bill-peebles-kevin-weil-leaving-departing)** — IPO 前夜還爆出 Altman 個人利益衝突，8500 億估值壓力下內部氣氛微妙
- **[Google 把 Transformer 跟 RNN 縫在一起，突破長上下文記憶瓶頸](https://www.36kr.com/p/3770765015991049)** — 賦予 RNN「可生長的記憶容量」，如果真能落地，記憶體股可能又要被震一下
- **[Tesla 把 Robotaxi 服務擴張到達拉斯跟休士頓](https://techcrunch.com/2026/04/18/tesla-brings-its-robotaxi-service-to-dallas-and-houston/)** — 無人監控、無駕駛員的影片已經在路上跑了，馬斯克這一波又壓對一次
- **[阿里端出 HappyOyster 實時世界模型](https://www.36kr.com/p/3771929563562504)** — 繼「歡樂馬」攻下 Artificial Analysis 榜首之後，阿里 Token Hub 再推可即時互動的開放世界模型，跟李飛飛 World Labs 直接對撞
- **[Anthropic 跟川普政府的關係在解凍](https://techcrunch.com/2026/04/18/anthropics-relationship-with-the-trump-administration-seems-to-be-thawing/)** — 前陣子才被五角大廈列為供應鏈風險，現在又開始跟白宮高層談——美國 AI 公司跟政府的博弈越來越複雜
- **[Sam Altman 的 World 跟 Tinder 合作做身分驗證](https://techcrunch.com/2026/04/17/sam-altmans-project-world-looks-to-scale-its-human-verification-empire-first-stop-tinder/)** — 去 Orb 掃描一下虹膜，換五次免費的 Tinder boost。在 AI 生成假人橫行的年代，「證明你是人」變成一門新生意
- **[Meta 廣告收入 2026 年首度超越 Google](https://www.36kr.com/p/3770733550781184)** — Meta 預估 2435 億、Google 2395 億，增速 24% vs 12%。一個關鍵分水嶺：廣告的錢開始從「抓住需求」流向「演算法製造需求」
- **[全球 AI 晶片新創進入「斬殺線」](https://www.36kr.com/p/3771770656359173)** — JPR 預測 2030 年剩下的 99 家新創可能只有少數存活，Tenstorrent、Groq、SambaNova 都在生死線上
- **[OpenAI 撲向製藥產業](https://www.36kr.com/p/3770746648568965)** — 英矽智能、晶泰們要開始緊張了，通用大模型公司開始切垂直領域
- **[榮耀發佈首款「養蝦本」MagicBook，內建自研 YOYO CLAW agent](https://www.36kr.com/p/3770787623404293)** — 端側 AI 的一個有趣轉折：終端廠商開始做自己的 agent，不再只是當 NPU 容器

---

## 🏄 深水區

- **[萬字拆解：AI 五大門派的底牌、命門與終極賭局](https://www.36kr.com/p/3771730656477956)** — 李飛飛 World Labs、Google、阿里、OpenAI、Anthropic 的終局之戰。如果你想一口氣搞清楚 AGI 競賽現在打到哪了，這篇夠你喝一壺
- **[Token 熱，他們賺麻了](https://www.36kr.com/p/3770838478553601)** — 中國日均 Token 消耗一年暴增 1000 倍，月之暗面 20 天營收超過 2025 全年。這不是模型故事，是賣鏟子的人故事
- **[用不起 Token 的我，成了 AI 時代的下沉市場人群](https://www.36kr.com/p/3770784142062086)** — 一個開發者的真實心聲：斤斤計較每一次 Claude 呼叫，感覺像二十年前的撥號上網時代。當 AI 成為奢侈品，誰被甩在後面？
- **[全球最臭名昭著的論壇，發現了 AI 最重要的「思考」能力](https://www.36kr.com/p/3770391848878593)** — 看似標題黨，但真的有料：探討 Opus 4.7 的討好式應答跟 4chan 式思考模式的詭異連結，適合對 AI 對齊議題有興趣的人
- **[美國 AI 也開始搞實名制了？](https://www.36kr.com/p/3769371305619970)** — Anthropic 悄悄上線政府證件＋實時自拍驗證，中國用戶首當其衝。一個值得追蹤的長期信號：AI 監管會不會變成另一場身分戰爭
