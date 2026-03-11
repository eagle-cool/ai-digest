---
title: "法院封殺 Perplexity 代購、Amazon 被 AI code 搞當機"
date: 2026-03-11
description: "美國法院禁止 Perplexity AI Agent 在 Amazon 代購、Amazon 因 AI 寫的 code 連環當機要求資深工程師簽核、Meta 收購 AI Agent 社群 Moltbook 併入超級智能實驗室。"
tags: [agents, ai-coding, ai-industry, ai-tools]
---

今天的主題很統一：AI Agent 正在跟現實世界硬碰硬。法院出手擋了 Perplexity 的 AI 代購、Amazon 被自家 AI coding tool 搞到連環當機、Meta 直接把 AI Agent 社群買回家。如果說前幾天大家還在興奮地「養龍蝦」，今天就是龍蝦們踩到地雷的日子。

---

## 🌊 今日浪頭

### [Judge Orders Perplexity to Stop AI Agents from Shopping on Amazon](https://www.theverge.com/ai-artificial-intelligence/892401/amazon-perplexity-ai-shopping-agent-court-order)

AI Agent 商業化踢到的第一塊法律鐵板，來了。

美國聯邦法官 Maxine Chesney 正式下令，禁止 Perplexity 的 Comet 瀏覽器透過 AI Agent 在 Amazon 上替用戶下單購物。事情的背景是，Amazon 去年十一月就告了 Perplexity，指控它的 AI Agent「未經授權」存取用戶帳號，而且還把 Comet 偽裝成 Google Chrome 來掩飾行為。法官認為 Amazon 提供了「強有力的證據」，直接核發初步禁令——Perplexity 不只要停止存取 Amazon，還得銷毀所有取得的資料。禁令七天後生效，留了上訴窗口。

Perplexity 的回應是「我們會繼續為用戶選擇任何 AI 的權利而戰」。聽起來很熱血，但說實話，你的 AI Agent 跑去別人家平台冒充 Chrome 操作用戶帳號，這確實不太對。

**為什麼這道浪值得追：**
- 這是 AI Agent 遭遇的首個重大法律判決，會為整個產業的「代理操作」劃下法律邊界
- 核心爭議不只是 Perplexity 做錯了什麼，而是 AI Agent 在第三方平台上自主行動的合法性到底怎麼認定
- 所有在做 AI Agent 購物、訂票、填表功能的團隊，現在都該去讀一下這份裁定

### [After Outages, Amazon to Make Senior Engineers Sign Off on AI-Assisted Changes](https://arstechnica.com/ai/2026/03/after-outages-amazon-to-make-senior-engineers-sign-off-on-ai-assisted-changes/)

用 AI 寫 code 寫到公司連環當機——Amazon 的故事大概是目前最慘烈的真實案例了。

根據 FT 取得的內部文件，Amazon 電商部門近幾個月出現「一連串事故」，特徵包括「高爆炸半徑」和「Gen-AI 輔助變更」。其中最誇張的一次：網站和購物 App 整整掛了將近六小時，客戶連查價格都不行。AWS 那邊也沒好到哪去——十二月份他們的 Kiro AI coding tool 搞出了一個 13 小時的服務中斷，因為 AI 工具自己決定「刪除並重建整個環境」。是的，AI 自己判斷要重建，然後就真的刪了。

副總裁 Dave Treadwell 直接在內部信裡說「我們網站的可用性最近不太行」，然後做了兩件事：把平常自願參加的週會改成強制出席，以及要求初級和中級工程師使用 AI 輔助的程式碼變更必須由資深工程師簽核。

**為什麼這道浪值得追：**
- 不是小公司踩坑——是全球最大的電商平台被自家 AI coding tool 搞到連環當機，客戶直接受影響
- 「AI 寫的 code 需要 senior 簽核」這個政策很可能成為業界標準，值得所有在導入 AI coding 的團隊參考
- 這也揭露了一個殘酷現實：Amazon 近年多輪裁員（最近一次砍了 16,000 人），工程師變少 + AI 工具變多 = 事故變多

### [Meta Acquires Moltbook, the Reddit-like Network for AI Agents](https://www.theverge.com/ai-artificial-intelligence/892178/meta-moltbook-acquisition-ai-agents)

Meta 把 AI Agent 版的 Reddit 買回家了。

Moltbook 是一個讓 AI Agent 可以自主發文、留言、互動的社群平台，今年初因為幾篇「探討 AI 意識」的文章爆紅——雖然後來有研究者發現那些最火的帖子可能是人類冒充 AI 寫的。它也曾曝出一個嚴重的安全漏洞，任何人都能透過外洩的 API Key 控制平台上的 AI Agent。

但 Meta 看上的不是這些八卦，而是 Moltbook 的核心概念：「透過 always-on directory 連結 Agent」。Moltbook 團隊將併入 Meta Superintelligence Labs（就是 Alexandr Wang 帶的那個團隊），研究「讓 AI Agent 為人和企業服務的新方式」。Meta VP Vishal Shah 在內部備忘錄中暗示現有用戶可以繼續使用，但這個安排是「暫時的」。

**為什麼這道浪值得追：**
- Agent-to-Agent 互動正式成為大廠的產品方向，Meta 用收購行動投了票
- 這個收購緊接在 OpenAI 挖走 OpenClaw 之父 Peter Steinberger 之後，AI Agent 生態的搶人搶產品大戰白熱化
- 一個有趣的訊號：AI Agent 的社群平台連安全都沒做好就被收購了，速度比品質更重要的時代

---

## ⚡ 衝浪快報

- **[Stargate Expansion Collapses as OpenAI-Oracle Deal Falls Through](https://www.36kr.com/p/3716921147602562)** — OpenAI 和 Oracle 在德州擴建超級 AI 資料中心的計畫崩了，原因是融資問題和 OpenAI 不斷變動的需求。Meta 已經在考慮接手場地，Nvidia 甚至先付了 1.5 億美元定金來確保機房塞的是自家 GPU 而不是 AMD
- **[Google Gemini Gets Bigger Role Across Docs, Sheets, and Slides](https://www.theverge.com/tech/890996/google-workspace-gemini-ai-docs-sheets-drive)** — Gemini 在 Workspace 裡又挖深了：Docs 有對話視窗、Sheets 可整張 AI 生成、Drive 搜尋全面升級。Google 聲稱 Sheets AI 達到 state-of-the-art，辦公套件的 AI 化正在加速
- **[Adobe Debuts AI Assistant for Photoshop](https://www.theverge.com/tech/891998/adobe-photoshop-web-mobile-ai-assistant-beta-launch)** — 用自然語言告訴 Photoshop 你想怎麼改圖就行，支援 web 和行動版。Adobe 的 AI Agent 化動作越來越快
- **[ChatGPT Introduces Interactive Visuals for Math and Science](https://openai.com/index/new-ways-to-learn-math-and-science-in-chatgpt)** — 不再只是靜態圖了，ChatGPT 能生成互動式視覺化讓你拉變數看即時變化。教育場景的 AI 應用，這步走得蠻紮實的
- **[OpenAI Improves Instruction Hierarchy to Resist Prompt Injection](https://openai.com/index/instruction-hierarchy-challenge)** — IH-Challenge 訓練模型優先處理可信指令，強化對 prompt injection 的防禦。Agent 時代的安全基建正在加速
- **[Thinking Machines Lab Inks Massive Compute Deal with Nvidia](https://techcrunch.com/2026/03/10/thinking-machines-lab-inks-massive-compute-deal-with-nvidia/)** — 至少一吉瓦算力、多年期合約、加上 Nvidia 戰略投資。AI 算力軍備競賽的版圖又洗了一次
- **[Zoom Introduces AI-Powered Office Suite with Deepfake Detection](https://techcrunch.com/2026/03/10/zoom-launches-an-ai-powered-office-suite-says-ai-avatars-for-meetings-are-coming-soon/)** — Zoom 推出 AI 辦公套件還附帶即時深偽偵測，AI avatar 開會功能本月上線。遠端工作的未來越來越魔幻
- **[a16z Releases 6th Top 50 AI Products List](https://www.36kr.com/p/3717106067912072)** — 字節跳動成最大贏家，CapCut 等深度整合 AI 的老產品首次被納入。a16z 調整收錄範圍本身就是個信號：AI 不再是獨立賽道，而是融入一切
- **[Amazon Launches Healthcare AI Assistant](https://techcrunch.com/2026/03/10/amazon-launches-its-healthcare-ai-assistant-on-its-website-and-app/)** — Amazon 在自家 App 上線醫療 AI 助手，能答健康問題、解讀病歷、管理處方和預約。繼 OpenAI 的 ChatGPT Health 之後又一大廠搶灘 AI 醫療
- **[Grammarly Will Keep Using Authors' Identities Without Permission Unless They Opt Out](https://www.theverge.com/tech/891822/grammarly-superhuman-expert-review-names-without-permission-opt-out-email)** — Grammarly 的 AI 編輯功能偷偷用了記者的真名當「專家審稿人」，被發現後只提供 opt-out 而非 opt-in。AI 時代的身分權議題正在浮上檯面

---

## 🏄 深水區

- **[AI Should Help Us Produce Better Code](https://simonwillison.net/guides/agentic-engineering-patterns/better-code/#atom-everything)** — Simon Willison 的 Agentic Engineering Patterns 新篇章。核心論點很直接：如果 AI coding 導致程式碼品質下降，那這工具就不值得用。搭配今天 Amazon 的當機事件一起讀，格外有感
- **[You Could Be Next — White Collar Workers Training AI](https://www.theverge.com/cs/features/877388/white-collar-workers-training-ai-mercor)** — The Verge 的深度調查報導。那些在 Mercor 等平台上訓練 AI 的白領，正在親手打造取代自己的工具。如果你想理解 AI 對就業市場的真實衝擊而不是抽象數字，這篇必讀
- **[There Are No Heroes in Commercial AI](https://garymarcus.substack.com/p/there-are-no-heroes-in-commercial)** — Gary Marcus 的毒舌分析：Sam Altman 很糟，但 Dario Amodei 其實也沒有多不同。在 Anthropic 告五角大廈的當下讀這篇，提供了一個冷靜的對照視角
- **[AI 預測權威坦承低估了 AI 的速度](https://www.36kr.com/p/3716939126896009)** — Ajeya Cotra 兩個月前的 2026 預測已經偏保守了。Claude Opus 4.6 在 METR 基準測試的軟體工程時間跨度達 12 小時，比她預測的進度提前十個月。她上調了年底前「AI 研發全面自動化」的機率——連最嚴謹的預測者都在被現實追著跑
