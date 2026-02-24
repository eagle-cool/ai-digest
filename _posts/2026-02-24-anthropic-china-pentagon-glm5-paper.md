---
title: "Anthropic 腹背受敵、GLM-5 開源稱王"
date: 2026-02-24
description: "Anthropic 怒揭中國三大 AI 廠用假帳號蒸餾 Claude，同時五角大廈下最後通牒要求開放軍用。GLM-5 論文全公開，開源模型首度在多項基準追平 Claude Opus。"
tags: [llm, agents, ai-industry, ai-safety]
---

今天 AI 圈最忙的公司毫無疑問是 Anthropic——前面在告中國三大 AI 廠偷它家的 Claude，後面美國國防部長直接下傳票要 Dario Amodei 去五角大廈談判。腹背受敵這詞大概就是為今天的 Anthropic 發明的。另一邊，智谱把 GLM-5 的 40 頁技術論文全丟出來了，開源模型首次在多項基準追平閉源頂級選手，這波操作讓整個社群都在認真讀論文了。

---

## 🌊 今日浪頭

### [Anthropic accuses Chinese AI labs of mining Claude as US debates AI chip exports](https://techcrunch.com/2026/02/23/anthropic-accuses-chinese-ai-labs-of-mining-claude-as-us-debates-ai-chip-exports/)

這件事的規模比我預期的大很多。Anthropic 直接點名了三家中國 AI 公司——DeepSeek、Moonshot AI（Kimi）、MiniMax——透過超過 24,000 個假帳號，對 Claude 進行了累計超過 1600 萬次的對話蒸餾（distillation）。蒸餾的目標非常精準：agentic reasoning、tool use、coding——全是 Claude 最強的地方。其中 MiniMax 最狠，累計 1300 萬次交互，而且被 Anthropic 抓到在新模型上線時把近半流量導過來吸能力。

**為什麼這道浪值得追：**
- 這不只是「抄作業」的問題——蒸餾出來的模型可能剝離安全護欄，讓危險能力無限制擴散
- Anthropic 明確把蒸餾攻擊跟晶片出口管制掛鉤：「這些規模的蒸餾需要先進晶片才能執行」
- 時間點很微妙——美國剛允許 Nvidia H200 出口中國，這份報告等於在打臉鬆綁政策

### [Defense Secretary summons Anthropic's Amodei over military use of Claude](https://techcrunch.com/2026/02/23/defense-secretary-summons-anthropics-amodei-over-military-use-of-claude/)

美國國防部長 Pete Hegseth 直接傳召 Dario Amodei 週二去五角大廈，談的是 Claude 的軍事用途。背景是這樣的：Anthropic 去年夏天簽了一份兩億美元的國防部合約，Claude 今年一月還被用在了抓捕委內瑞拉總統 Maduro 的特種作戰中。但 Anthropic 拒絕讓國防部用 Claude 做大規模監控和全自動武器——五角大廈威脅要把 Anthropic 列為「供應鏈風險」，這個標籤通常是留給外國敵對勢力的。

**為什麼這道浪值得追：**
- 這是 AI 安全理念和國家軍事需求正面對撞的經典案例
- 「供應鏈風險」標籤一旦落下，不只 Anthropic 的合約作廢，其他國防夥伴也必須全面棄用 Claude
- Anthropic 正同時面對兩個方向的壓力：中國在偷它的技術，美國在逼它放棄原則——這劇本比小說還精彩

### [智谱 GLM-5 技术论文全公开](https://www.36kr.com/p/3695400723394178)

智谱把 GLM-5 背後的 40 頁技術論文完全公開了，標題直接叫「告別 Vibe Coding，邁入 Agentic Engineering」。我看了一下技術細節，三個關鍵創新確實猛：第一，引入 DeepSeek 同款稀疏注意力（DSA），KV Cache 開銷直降 75%，推理速度提升 3 倍；第二，全新的異步強化學習框架，把生成和訓練解耦，GPU 利用率從業界常見的 20-30% 大幅提升；第三，超過一萬個可驗證的真實世界環境，涵蓋 9 種程式語言。SWE-bench Verified 拿到 77.8%，開源 SOTA。

**為什麼這道浪值得追：**
- 這是開源模型首次在 Artificial Analysis Intelligence Index 達到 50 分——以前這個分數只有閉源模型拿得到
- 匿名測試時 25% 的人猜它是 Claude Sonnet 5——沒人想到是中國開源模型
- 完全適配華為昇騰等國產晶片，在中美 AI 晶片戰的背景下，這個技術路線的戰略意義不言而喻

---

## ⚡ 衝浪快報

- **[With AI, investor loyalty is (almost) dead: At least a dozen OpenAI VCs now also back Anthropic](https://techcrunch.com/2026/02/23/with-ai-investor-loyalty-is-almost-dead-at-least-a-dozen-openai-vcs-now-also-back-anthropic/)** — AI 領域的 VC 忠誠度已經是個笑話了，至少十幾家 OpenAI 的投資者同時也投了 Anthropic，利益衝突？不存在的
- **[OpenAI announces Frontier Alliance Partners](https://openai.com/index/frontier-alliance-partners)** — OpenAI 找來四大顧問公司推企業 AI Agent 落地，從 pilot 階段推進到 production，企業 AI 的戰場正式開打
- **[MiniMax 春节杀疯了：Tokens 周调用破 3T，港股暴涨](https://www.jiqizhixin.com/articles/2026-02-23-5)** — MiniMax 春節期間 token 週調用量突破 3 兆，股價單日漲 14.52%，難得看到需求側的爆發帶動資本市場
- **[星际之门 $500B 计划陷入停滞](https://www.jiqizhixin.com/articles/2026-02-23-6)** — 去年高調宣布的 5000 億美元 Stargate 計畫傳出項目停滯、算力暗鬥，這燒錢速度連 OpenAI 都有點吃不消？
- **[Google restricting AI Pro/Ultra subscribers for using OpenClaw](https://discuss.ai.google.dev/t/account-restricted-without-warning-google-ai-ultra-oauth-via-openclaw/122778)** — Google 開始限制透過 OpenClaw 使用 Gemini API 的付費用戶，不少人帳號直接被封，社群一片譁然
- **[Samsung is adding Perplexity to Galaxy AI](https://www.theverge.com/tech/882921/samsung-is-adding-perplexity-to-galaxy-ai)** — Galaxy S26 用戶除了 Bixby 和 Gemini，現在還能呼叫 Perplexity，三星的 AI 策略就是：全都要
- **[Guide Labs debuts a new kind of interpretable LLM](https://techcrunch.com/2026/02/23/guide-labs-debuts-a-new-kind-of-interpretable-llm/)** — 開源了 80 億參數的 Steerling-8B，用全新架構讓模型行為可解釋——AI 黑箱問題總算有人認真在解了
- **[Data center builders vs. American farmers](https://arstechnica.com/tech-policy/2026/02/im-not-for-sale-farmers-refuse-to-take-millions-in-data-center-deals/)** — 科技巨頭以為農民會乖乖賣地蓋資料中心，結果被狠狠打臉：「我不賣」
- **[AIs can generate near-verbatim copies of novels from training data](https://arstechnica.com/ai/2026/02/ais-can-generate-near-verbatim-copies-of-novels-from-training-data/)** — 頂級 AI 模型可以幾乎逐字複製暢銷小說，「合理使用」的辯護越來越站不住腳了
- **[Pinterest is drowning in a sea of AI slop](https://www.404media.co/pinterest-is-drowning-in-a-sea-of-ai-slop-and-auto-moderation/)** — Pinterest 已經被 AI 生成的垃圾內容淹沒，自動審核形同虛設，又一個平台淪陷
- **[Spotify rolls out AI-powered Prompted Playlists to UK and more](https://techcrunch.com/2026/02/23/spotify-ai-prompted-playlists-uk-markets/)** — Spotify 的 AI 歌單功能擴展到英國等市場，用自然語言描述心情就能生成播放清單

---

## 🏄 深水區

- **[Writing about Agentic Engineering Patterns](https://simonwillison.net/2026/Feb/23/agentic-engineering-patterns/#atom-everything)** — Simon Willison 開始系統性整理 Agentic Engineering 的模式和最佳實踐，如果你正在用 coding agent 開發，這系列文章值得追蹤收藏
- **[Ladybird adopts Rust, with help from AI](https://simonwillison.net/2026/Feb/23/ladybird-adopts-rust/#atom-everything)** — Ladybird 瀏覽器從 C++ 遷移到 Rust，而且大量使用 AI coding agent 來協助轉換——這可能是目前最大規模的 AI 輔助語言遷移案例
- **[The Claude C Compiler: What It Reveals About the Future of Software](https://simonwillison.net/2026/Feb/22/ccc/#atom-everything)** — Anthropic 用平行 Claude 從零打造了一個 C 編譯器，Chris Lattner（LLVM 之父）的評價讓這個實驗更值得深思
- **[How many AIs does it take to read a PDF?](https://www.theverge.com/ai-artificial-intelligence/882891/ai-pdf-parsing-failure)** — The Verge 深度報導 AI 在處理 PDF 時的荒謬失敗率，兩萬頁國會文件的解析之旅比你想像的慘烈得多
