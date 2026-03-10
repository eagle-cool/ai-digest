---
title: "Anthropic 正式提告、LeCun 帶十億美元出走建 AI 第三極"
date: 2026-03-10
description: "Anthropic 對美國國防部提起訴訟，OpenAI 和 Google 員工聯名聲援；OpenAI 收購 AI 安全新創 Promptfoo；楊立昆的 AMI Labs 拿下 10.3 億美元，要用世界模型挑戰 LLM 霸權。"
tags: [ai-industry, ai-safety, llm, agents, ai-tools]
---

今天 AI 圈的浪打得特別猛，而且不是技術浪，是政治浪——Anthropic 對美國國防部正式提告了，Jeff Dean 帶著一票 OpenAI 和 Google 的人跳出來聲援。另一邊，楊立昆帶著十億美元和一票 FAIR 老戰友，要在巴黎建一個不屬於美國也不屬於中國的 AI 第三極。OpenAI 則悄悄把 AI 安全新創 Promptfoo 收了。三件事加起來，你能嗅到整個 AI 產業正在重新洗牌。

---

## 🌊 今日浪頭

### [Anthropic is suing the Department of Defense](https://www.theverge.com/ai-artificial-intelligence/891377/anthropic-dod-lawsuit)

這不是一般的商業糾紛——Anthropic 在加州法院正式對美國國防部提起訴訟，指控川普政府因為 Anthropic 堅持 AI 安全紅線而進行非法報復。事情的起因大家應該都知道了：Anthropic 拒絕讓 Claude 被用於國內大規模監控和全自主殺傷性武器，結果被國防部打上「供應鏈風險」標籤——這個標籤通常是用來對付外國公司的。更猛的是，訴訟提出幾小時後，將近 40 位來自 OpenAI 和 Google 的員工——包括 Google 首席科學家 Jeff Dean——就聯名提交了法庭之友意見書，聲援 Anthropic 的立場。

**為什麼這道浪值得追：**
- 這是 AI 安全議題第一次從白皮書走進法庭，Anthropic 主張第一修正案保護其對 AI 安全的立場表達
- OpenAI/Google 員工跨公司聲援是前所未見的，意見書明確指出「AI 驅動的大規模監控對民主治理構成深層風險」
- 實際衝擊已經開始：GSA 終止了 OneGov 合約，財政部、國務院也陸續切斷與 Anthropic 的合作

### [OpenAI to acquire Promptfoo](https://techcrunch.com/2026/03/09/openai-acquires-promptfoo-to-secure-its-ai-agents/)

OpenAI 收購了 AI 安全新創 Promptfoo，這家 2024 年成立的公司專門做 LLM 安全漏洞檢測，超過 25% 的 Fortune 500 企業都在用。收購前估值才 8600 萬美元、總融資 2300 萬——以 OpenAI 的體量來說根本是零錢。但重要的不是金額，而是信號：當 AI Agent 開始在企業裡自主執行任務，安全就不再是「加分項」，而是「沒有就別上線」的硬需求。Promptfoo 的技術會整合進 OpenAI Frontier 企業平台，提供自動化紅隊測試、Agent 工作流安全評估、風險監控。

**為什麼這道浪值得追：**
- AI Agent 安全正式從「最佳實踐」升級為「基礎建設」，OpenAI 直接把它買進來內建
- Promptfoo 的開源工具會繼續維護——這對整個生態是好事
- 暗示 OpenAI Frontier 平台的企業客戶對 Agent 安全有極大焦慮，不然不會這麼急著補這塊

### [Yann LeCun's AMI Labs raises $1.03 billion to build world models](https://techcrunch.com/2026/03/09/yann-lecuns-ami-labs-raises-1-03-billion-to-build-world-models/)

楊立昆離開 Meta 後的新公司 AMI（Advanced Machine Intelligence，法語裡是「朋友」的意思，他特別要求用法語發音）拿下了 10.3 億美元融資，投前估值 35 億。投資陣容像是 AI 圈的復仇者聯盟：Nvidia、貝佐斯家族辦公室、淡馬錫、軟銀、Eric Schmidt、三星、Tim Berners-Lee。DiT 架構的共同作者謝賽寧加入擔任首席科學官，六位核心創始人有四位來自 Meta FAIR。楊立昆的核心論點沒變：LLM 理解不了物理世界，世界模型（JEPA 架構）才是通往真正智慧的路。他直接喊話學界：「別做 LLM，你們趕不上業界。去發明新技術。」

**為什麼這道浪值得追：**
- 十億美元級別的「LLM 反對票」——這不是嘴砲，是真金白銀的路線之爭
- AMI 定位為 AI「第三極」：不依附美國也不依附中國，總部巴黎，路線開源
- 謝賽寧加入是關鍵信號，他的 DiT 架構是 Sora 等視覺模型的底層基礎，現在跑去做世界模型了

---

## ⚡ 衝浪快報

- **[Anthropic launches Code Review for Claude Code](https://techcrunch.com/2026/03/09/anthropic-launches-code-review-tool-to-check-flood-of-ai-generated-code/)** — Anthropic 推出多 Agent 程式碼審查系統，自動抓 AI 生成程式碼的邏輯錯誤。AI 寫的 code 讓 AI 來 review，元到不行但確實需要
- **[OpenAI hardware exec Caitlin Kalinowski quits over Pentagon deal](https://techcrunch.com/2026/03/07/openai-robotics-lead-caitlin-kalinowski-quits-in-response-to-pentagon-deal/)** — OpenAI 機器人團隊負責人因為公司與國防部的交易而辭職。對比 Anthropic 的態度，OpenAI 內部顯然不是每個人都買帳
- **[中國「龍蝦」狂潮全面引爆：騰訊、字節、阿里齊下場](https://www.36kr.com/p/3716551371240200)** — OpenClaw 在中國掀起群眾 AI 時刻，騰訊 Qclaw、字節 ArkClaw、阿里 CoPaw 同步上線。深圳騰訊大廈門口排了近千人的隊，小學生都來了
- **[Nscale raises $2B at $14.6B valuation](https://techcrunch.com/2026/03/09/sandberg-clegg-join-nscale-board-as-this-stargate-norway-startup-hits-14-6b-valuation/)** — 被稱為「Stargate Norway」的英國 AI 基建新創再拿 20 億，Sheryl Sandberg 和 Nick Clegg 加入董事會。AI 基建軍備競賽沒有要停的意思
- **[Is legal the same as legitimate: AI reimplementation and the erosion of copyleft](https://writings.hongminhee.org/2026/03/legal-vs-legitimate/)** — HN 上 410 分、449 則留言的重量級討論：AI 重新實作開源軟體是否侵蝕了 copyleft 精神？合法不等於正當
- **[Under the hood: Security architecture of GitHub Agentic Workflows](https://github.blog/ai-and-ml/generative-ai/under-the-hood-security-architecture-of-github-agentic-workflows/)** — GitHub 官方揭露如何在 Agent 有 repo 存取權限的情況下做安全護欄，對開發者很實用的參考架構
- **[Granite 4.0 1B Speech: Compact, Multilingual, and Built for the Edge](https://huggingface.co/blog/ibm-granite/granite-4-speech)** — IBM 推出 10 億參數的多語言語音模型，專為邊緣裝置設計。小而精的路線
- **[X says you can block Grok from editing your photos](https://www.theverge.com/tech/891352/x-grok-xai-edit-blocker-photo-toggle)** — X 終於讓你可以阻止別人用 Grok 修改你的照片，但注意看小字——限制比你想的多
- **[Qualcomm's partnership with Neura Robotics](https://techcrunch.com/2026/03/09/qualcomms-partnership-with-neura-robotics-is-just-the-beginning/)** — Qualcomm 的 IQ10 處理器 + Neura Robotics，晶片大廠正式進軍具身智能
- **[LeRobot v0.5.0: Scaling Every Dimension](https://huggingface.co/blog/lerobot-release-v050)** — Hugging Face 的開源機器人框架大更新，具身 AI 的開源生態正在成形

---

## 🏄 深水區

- **[Perhaps not Boring Technology after all](https://simonwillison.net/2026/Mar/9/not-so-boring/#atom-everything)** — Simon Willison 探討 LLM 是否會把所有人推向同樣的技術棧。兩年前確實如此，但現在情況正在改變——值得每個做技術選型的人讀一讀
- **[Vibe Coding Trip Report: Making a sponsor panel](https://xeiaso.net/blog/2026/vibe-coding-sponsor-panel/)** — Xe Iaso 手術休養期間用 vibe coding 完成了一個之前卡了好幾個月的專案。真實的使用體驗紀錄，不是行銷文
- **[Agentic Critical Training](https://arxiv.org/abs/2603.08706)** — 這篇論文指出模仿學習只教 Agent「做什麼」但不教「為什麼」，提出讓 Agent 在成功和失敗之間建立對比理解的訓練方法
- **[Learnings from paying artists royalties for AI-generated art](https://www.kapwing.com/blog/learnings-from-paying-artists-royalties-for-ai-generated-art/)** — Kapwing 真的付了版稅給藝術家，然後分享他們學到了什麼。HN 上 95 分、53 則討論，在 AI 版權爭議中這是少見的實際行動派
