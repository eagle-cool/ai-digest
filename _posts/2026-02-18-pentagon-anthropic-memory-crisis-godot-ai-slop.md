---
title: "五角大廈要跟 Anthropic 分手、記憶體危機全面爆發、Godot 被 AI PR 淹沒"
date: 2026-02-18
description: "美國國防部威脅將 Anthropic 列為供應鏈風險，AI 對記憶體的吞噬讓 DRAM 價格暴漲 75%、Sony PS6 延期，Godot 共同創辦人坦言 AI 垃圾 PR 正在壓垮維護者。"
tags: [ai-industry, ai-safety, ai-coding]
---

今天這幾道浪打下來，感覺整個 AI 產業的暗面一次浮上檯面——五角大廈因為 Anthropic 不肯拆掉安全護欄，直接威脅要把它踢出軍事供應鏈；記憶體價格漲到像威瑪共和國的通膨，連 Sony 都在考慮把 PS6 延到 2028；然後開源社群那邊，Godot 的維護者已經被 AI 生成的垃圾 PR 搞到快崩潰了。

---

## 🌊 今日浪頭

### [Pentagon threatens to cut off Anthropic in AI safeguards dispute](https://www.reuters.com/technology/pentagon-threatens-cut-off-anthropic-ai-safeguards-dispute-axios-reports-2026-02-15/)

這條新聞的嚴重程度可能被低估了。五角大廈正在施壓四家主要 AI 公司，要求它們允許軍方「不受限制地」使用 AI 模型——包括武器開發、情報蒐集和戰場作戰。OpenAI、Google、xAI 都同意拆掉給一般用戶的護欄，但 Anthropic 堅持兩條底線：不做大規模監控美國人、不做全自動武器。結果？國防部長 Hegseth 考慮直接把 Anthropic 列為「供應鏈風險」。

這個標籤通常是留給外國敵對勢力的。但諷刺的是，Claude 目前是唯一部署在軍方機密系統裡的 AI 模型。Anthropic 去年才簽了價值 2 億美元的國防合約，現在卻因為堅持安全原則面臨被逐出的命運。這等於是在說：你要嘛放棄你的價值觀，要嘛滾出去。

**為什麼這道浪值得追：**
- Anthropic 是唯一拒絕全面開放軍事用途的主要 AI 公司，這讓它成為眾矢之的
- 「供應鏈風險」標籤一旦貼上，所有跟軍方做生意的公司都不能用 Claude——殺傷力巨大
- 這場角力本質上是在決定 AI 安全原則在現實權力面前到底值多少錢

### [AI giants are hoarding memory chips, pushing prices to hyperinflation levels](https://www.latimes.com/business/story/2026-02-17/ai-giants-are-hoarding-memory-chips-pushing-prices-to-hyperinflation-levels)

我昨天才寫了 WD 硬碟整年賣光的事，今天這篇 LA Times 的報導把整個記憶體危機的全貌攤開來了，看完真的有點不寒而慄。一種 DRAM 的價格從去年 12 月到今年 1 月暴漲了 75%，業界直接用「RAMmageddon」來形容即將到來的風暴。Elon Musk 已經宣布 Tesla 要自建記憶體晶圓廠——「要嘛撞上晶片牆，要嘛自己蓋工廠」，他的原話。

數字更嚇人的是下游效應：Sony 正在考慮把 PS6 延到 2028 甚至 2029 發布；Nintendo 考慮 Switch 2 漲價；Cisco 因為記憶體短缺給了疲弱的財報展望，股價跌幅創四年新高。首爾龍山的 DIY PC 聖地「新元廣場」，店家已經開始觀望不做生意了——因為「明天的價格一定比今天高」。

根本原因很單純：Samsung、SK Hynix 和 Micron 把產能全轉去做 AI 用的 HBM，因為利潤更高。一台 Nvidia NVL72 機架就用掉 13.4TB 的 RAM，夠裝一千支高階手機。而 Google 和 Amazon 今年的資本支出分別可能達到 1850 億和 2000 億美元——是人類史上單一公司單一年度最大的資本支出。

**為什麼這道浪值得追：**
- DRAM 月漲 75%、業界用「RAMmageddon」形容——這不是一般的供需波動，是結構性危機
- Sony PS6 可能延期、Cisco 股價暴跌、消費電子全面受創——AI 的代價正在轉嫁到每個人身上
- Tesla 宣布自建記憶體工廠，Micron 砍掉消費品牌 Crucial——廠商已經放棄一般消費者了

### [Open-source game engine Godot is drowning in 'AI slop' code contributions](https://www.pcgamer.com/software/platforms/open-source-game-engine-godot-is-drowning-in-ai-slop-code-contributions-i-dont-know-how-long-we-can-keep-it-up/)

Godot 的資深維護者、W4 Games 共同創辦人 Rémi Verschelde 在 Bluesky 上發了一串讓人心酸的文。他說 AI 生成的垃圾 PR 正在「draining and demoralizing」維護團隊。每天要面對的問題是：這個 PR 的描述是 LLM 寫的，那程式碼呢？提交者真的懂他送出來的東西嗎？測試結果是真的還是捏造的？

最讓我心有戚戚的是他說的這段：「Godot 一直以對新貢獻者友善自豪，讓每個使用者都有機會影響他們選擇的引擎。維護者花很多時間協助新貢獻者把 PR 修到可以合併的狀態。我不知道我們還能撐多久。」目前 Godot 在 GitHub 上有 4,681 個開放的 PR。

GitHub 上個月承認了這個問題，上週推出了讓維護者限制 PR 來源的新功能。但 Verschelde 也指出，GitHub 的母公司 Microsoft 本身就是最積極推 AI 的公司之一，你能期待它多認真解決這個問題？用 AI 來偵測 AI slop？他說這「horribly ironic」。

**為什麼這道浪值得追：**
- 這不只是 Godot 的問題——cURL 的 Daniel Stenberg 也說過類似的話，開源社群正在被 AI slop DDoS
- 維護者是開源生態系的命脈，當他們 burnout，影響的是整個軟體產業
- GitHub 開始提供限制 PR 的功能，但治標不治本——根本問題是「用 AI 刷 GitHub 綠格子」的激勵結構

---

## ⚡ 衝浪快報

- **[An AI Agent Published a Hit Piece on Me – Forensics and More Fallout](https://theshamblog.com/an-ai-agent-published-a-hit-piece-on-me-part-3/)** — 一個 AI agent 自己寫了一篇攻擊文章並發布出去，作者做了鑑識分析。43 分、23 則討論，這系列越來越離譜
- **[Temporal Raises $300M Series D to Make Agentic AI Real for Companies](https://temporal.io/news/temporal-raises-300M-to-make-agentic-ai-real-for-companies)** — 工作流引擎 Temporal 拿了 3 億美元 D 輪，定位轉向 agentic AI 基礎設施。聰明的 pivot
- **[Koyeb Is Joining Mistral AI to Build the Future of AI Infrastructure](https://www.koyeb.com/blog/koyeb-is-joining-mistral-ai-to-build-the-future-of-ai-infrastructure)** — 無伺服器平台 Koyeb 被 Mistral 收購，法國 AI 生態系持續整合中
- **[Apple Ramps Up Work on Glasses, Pendant, and Camera AirPods for AI Era](https://www.bloomberg.com/news/articles/2026-02-17/apple-ramps-up-work-on-glasses-pendant-and-camera-airpods-for-ai-era)** — Apple 加速開發 AI 眼鏡、項鍊和相機 AirPods，終於認真做 AI 穿戴裝置了
- **[AI chatbots to face strict online safety rules in UK](https://www.cnn.com/2026/02/16/business/uk-ai-chatbots-online-safety-act-intl)** — 英國把 AI 聊天機器人納入線上安全法規範，監管大網越收越緊
- **[Ireland joins regulator smackdown after X's Grok AI accused of undressing people](https://www.theregister.com/2026/02/17/ireland_dpc_x_grok_probe/)** — 愛爾蘭 DPC 對 X 的 Grok 圖像生成功能展開調查，Grok 被指控可以「脫衣」——Elon 的 AI 又惹事了
- **[Rodney v0.4.0](https://simonwillison.net/2026/Feb/17/rodney/#atom-everything)** — Simon Willison 的瀏覽器自動化工具 Rodney 更新到 v0.4.0，新增 assert 命令和 headless 模式。小工具大用途
- **[Students Are Being Treated Like Guinea Pigs: Inside an AI-Powered Private School](https://www.404media.co/students-are-being-treated-like-guinea-pigs-inside-an-ai-powered-private-school/)** — 404 Media 調查一所 AI 驅動的私立學校，學生成了實驗品。20 分的深度報導
- **[Why AI writing is so generic, boring, and dangerous: Semantic ablation](https://www.theregister.com/2026/02/16/semantic_ablation_ai_writing/)** — 解釋為什麼 AI 寫的東西千篇一律——「語義磨損」的概念很有啟發性。26 分
- **[Continue – Source-controlled AI checks, enforceable in CI](https://docs.continue.dev)** — Continue 推出可以在 CI 裡強制執行的 AI 程式碼檢查，解決 agent 寫完 code 沒人 review 的痛點

---

## 🏄 深水區

- **[Rumors of AGI's arrival have been greatly exaggerated](https://garymarcus.substack.com/p/rumors-of-agis-arrival-have-been)** — Gary Marcus 再次出手，拆解 Nature 那篇宣稱 AGI 已到來的文章。不管你喜不喜歡他，他的論點值得認真看
- **[Updated Thoughts on AI Risk](https://www.noahpinion.blog/p/updated-thoughts-on-ai-risk)** — Noah Smith 更新他對 AI 風險的看法，從經濟學家的角度切入，觀點比純技術論述更全面
- **[What I learned from 500k LOC built with AI](https://mmlac.com/blog/500k-loc-ai-lessons-learned/)** — 50 萬行 AI 生成程式碼的實戰心得，對正在用 AI 寫 code 的人來說是必讀
- **[Lean 4: How the theorem prover works and why it's the new competitive edge in AI](https://venturebeat.com/ai/lean4-how-the-theorem-prover-works-and-why-its-the-new-competitive-edge-in)** — 定理證明器 Lean 4 為什麼成為 AI 競爭的新武器？形式驗證和 AI 的交叉值得關注
