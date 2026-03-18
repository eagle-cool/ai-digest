---
title: "GPT-5.4 mini 殺瘋了、Mistral Forge 讓企業自建 AI、Gemini 個人化全美開放"
date: 2026-03-18
description: "OpenAI 深夜突襲發布 GPT-5.4 mini 與 nano，三分之一價格逼近滿血效能；Mistral 推出 Forge 平台讓企業從零訓練模型；Google 將 Gemini 個人化功能開放全美用戶。"
tags: [llm, ai-tools, ai-industry, agents]
---

今天 AI 圈的浪頭打到人臉上——OpenAI 半夜不聲不響丟了 GPT-5.4 mini 和 nano 兩顆炸彈，價格砍到滿血版的三分之一，效能卻追到九成以上。Mistral 那邊在 GTC 上宣布 Forge 平台，直接讓企業客戶自己從零開始訓練模型。而 Google 也不甘寂寞，把 Gemini 的 Personal Intelligence 從付費限定解鎖給全美所有用戶。這個週三，誰敢不開電腦？

---

## 🌊 今日浪頭

### [GPT-5.4 mini+nano 突襲，1/3 價格逼近滿血版，OpenAI 徹底殺瘋](https://www.36kr.com/p/3727696735468423)

OpenAI 真的很愛搞突襲。沒有預熱、沒有倒數，GPT-5.4 mini 和 nano 就這樣直接上線了。我看完跑分數據的第一反應是：這還叫「mini」？SWE-Bench Pro 拿下 54.4%，距離滿血版 GPT-5.4 的 57.7% 只差 3.3 個百分點。更誇張的是電腦使用能力——OSWorld 72.1% 直逼滿血版的 75%，而上一代 GPT-5 mini 只有 42%，一代之間翻了快一倍。

定價才是真正的殺招：mini 輸入 $0.75/百萬 token、輸出 $4.50/百萬 token，大概是滿血版的三分之一；nano 更狠，輸入 $0.20、輸出 $1.25，只有滿血版的十二分之一。而且 mini 速度比上一代快了兩倍，400K context window，免費用戶也能用。

最值得注意的是 OpenAI 推的「子智能體」架構：GPT-5.4 負責規劃和決策，mini 負責執行，在 Codex 裡 mini 只消耗 GPT-5.4 配額的 30%。大腦思考、手腳幹活，同樣預算能跑三倍任務。這不只是發了兩個小模型，這是在定義未來 AI 系統的分層協作範式。

**為什麼這道浪值得追：**
- mini 在編碼、工具調用、電腦使用上全面逼近旗艦，但長上下文是明顯短板（128K 以上跟滿血版差 40 個百分點）
- nano 的 SWE-Bench Pro 52.4% 直接碾壓上一代 mini 的 45.7%——蒸餾的進化速度驚人
- 「大模型決策、小模型執行」的分層架構正在成為產業共識，開發者的架構思維要跟著變

### [Mistral Forge：讓企業從零訓練自己的 AI 模型，正面挑戰 OpenAI 和 Anthropic](https://techcrunch.com/2026/03/17/mistral-forge-nvidia-gtc-build-your-own-ai-enterprise/)

Mistral 在 GTC 上丟出了一個很有野心的東西——Forge 平台。跟市面上大多數「企業 AI」解決方案不同的是，Forge 不只是微調或 RAG，而是讓企業從頭訓練自己的模型。這差別很大：微調是在別人的地基上裝修，Forge 是讓你自己打地基。

這招很聰明。大部分企業 AI 專案失敗，不是缺技術，而是通用模型根本不理解幾十年累積下來的內部文件和工作流程。Forge 讓客戶用 Mistral 的開源模型庫（包括剛發布的 Small 4）作為起點，搭配駐場工程師一起搞。合作夥伴陣容也很硬：Ericsson、歐洲太空總署、ASML，加上新加坡的 DSO 和 HTX。

值得一提的是 Mistral 今年 ARR 預計破 10 億美元。一家靠企業客戶活的法國 AI 公司，在 OpenAI 和 Anthropic 瘋狂搶消費者市場的時候默默把企業這塊吃下來，這策略夠穩。

**為什麼這道浪值得追：**
- 從零訓練 vs 微調/RAG，本質上是「租房 vs 蓋房」的差別，對高合規產業極具吸引力
- 駐場工程師模式像 Palantir，高接觸但高黏性，企業一旦用上就很難換
- 開源模型 + 企業訓練平台的組合拳，是目前唯一真正對抗 OpenAI/Anthropic 閉源壁壘的可行路徑

### [Google Gemini 個人化功能全美開放：你的 Gmail、Photos、YouTube 都成了 AI 記憶](https://www.theverge.com/ai-artificial-intelligence/896107/google-expands-personal-intelligence)

Google 終於把 Personal Intelligence 從付費牆後面放出來了。之前只有 AI Pro 和 AI Ultra 訂閱者能用，現在全美所有免費用戶都能讓 Gemini 連接 Gmail、Google Photos 和 YouTube，然後根據你的個人數據提供客製化回應。

聽起來很美好，但以我的觀察，這步棋的戰略意義大於技術意義。Google 最大的護城河不是模型能力——那個大家都在追——而是它手上握著幾十億人的 email、照片和觀看紀錄。當 Gemini 能讀你的信箱推薦購物、看你的照片回答「我上次去日本是什麼時候」，這種個人化的黏性是 ChatGPT 和 Claude 短期內很難追上的。

當然也有隱私疑慮。Google 說不會用你的信箱和相簿來訓練模型，只用「特定提示和回應」，而且功能是 opt-in 可隨時關閉。信不信就看你了。

**為什麼這道浪值得追：**
- Google 的真正武器不是 Gemini 模型本身，而是十幾年累積的個人數據圖譜
- 免費開放是為了跑量——越多人用，個人化效果越好，飛輪轉起來競爭者更難追
- 目前限個人帳號（不含企業/教育），但企業版開放只是時間問題

---

## ⚡ 衝浪快報

- **[Anthropic 逼急奧特曼：OpenAI 自砍副業，死磕 Claude 主場](https://www.36kr.com/p/3727696878910596)** — OpenAI 戰略大收縮，砍掉邊緣項目全力聚焦編程和企業市場，Anthropic 的壓力果然見效了
- **[OpenAI 與 AWS 簽署政府合約，進軍美國機密 AI 系統](https://techcrunch.com/2026/03/17/openai-expands-government-footprint-with-aws-deal/)** — 從消費者到企業再到政府，OpenAI 的版圖越鋪越大，但也越來越像傳統科技巨頭了
- **[五角大廈正在開發 Anthropic 替代方案](https://techcrunch.com/2026/03/17/the-pentagon-is-developing-alternatives-to-anthropic-report-says/)** — 與 Anthropic 決裂後，美國國防部積極尋找新 AI 供應商，政府 AI 採購格局正在洗牌
- **[Garry Tan 的 Claude Code 設定爆紅又引戰](https://techcrunch.com/2026/03/17/why-garry-tans-claude-code-setup-has-gotten-so-much-love-and-hate/)** — YC 總裁在 GitHub 分享 Claude Code 配置引發社群熱議，連各大 AI 模型自己都來湊熱鬧
- **[微軟再換 Copilot 主管，AI 領導層持續震盪](https://www.theverge.com/news/895963/microsoft-copilot-leadership-changes-consumer-commercial)** — 又一次高層重組，Copilot 到底要往哪走，微軟自己可能也還在想
- **[Sam Altman 的 World 推出 AI Agent 人類身份驗證工具](https://techcrunch.com/2026/03/17/world-launches-tool-to-verify-humans-behind-ai-shopping-agents/)** — 當 AI 購物代理人滿天飛，「證明你是人類」反而成了新生意
- **[Unsloth Studio 開源上線：無代碼本地訓練 AI 模型](https://www.reddit.com/r/AIDeveloperNews/comments/1rwjt6b/unsloth_introduces_unsloth_studio_an_opensource/)** — 不用寫一行程式就能在本地訓練、跑、導出模型，開源社群的禮物
- **[前騰訊 AI 大牛劉威的 Video Rebirth 融了 8000 萬美元，蘇姿丰也投了](https://www.36kr.com/p/3727714507635587)** — 前騰訊混元大模型負責人的 AI 視頻創業，AMD CEO 都來背書，但產品都還沒發布
- **[Karpathy 點讚：Transformer 權重內嵌計算機，每秒 3 萬 Token](https://www.36kr.com/p/3726664578202246)** — 在模型權重裡直接塞一台可執行的虛擬計算機，解出世界最難數獨，Karpathy 親自轉發
- **[Kimi 新深度軸注意力架構，17 歲高中生第一作者](https://www.36kr.com/p/3726664644082308)** — 繼昨天 Altman 判 Transformer 死刑，月之暗面直接交出了一個具體的替代方案，第一作者還是高中生

---

## 🏄 深水區

- **[GPT-5.4 mini and GPT-5.4 nano, which can describe 76,000 photos for $52](https://simonwillison.net/2026/Mar/17/mini-and-nano/#atom-everything)** — Simon Willison 的第一手評測：nano 用 52 美元就能描述 7.6 萬張照片，想了解 mini/nano 的實際性價比就看這篇
- **[Subagents — Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/subagents/#atom-everything)** — Simon Willison 系統整理了子代理模式的設計哲學，如果你在做 agent 開發，這篇是必讀級別的指南
- **[Polynomial Time Factoring Algorithm](https://geohot.github.io//blog/jekyll/update/2026/03/16/polynomial-time-factoring.html)** — George Hotz 記錄 AI 輔助發現多項式時間質因數分解的過程，如果這東西是真的，RSA 加密就要重新想了
