---
title: "Agent 狂潮：Meta 出包、Anthropic 反擊、Gemini 上路"
date: 2026-03-22
description: "Meta 內部 AI Agent 釀 Sev 1 安全事故、Anthropic 宣誓書反擊五角大廈封殺令、Gemini 手機上真的幫你叫車點餐了——AI Agent 時代的光明與暗面同時炸開。"
tags: [agents, ai-safety, ai-industry, ai-tools]
---

今天 AI Agent 這個詞被反覆打臉又反覆翻紅——Meta 的 Agent 在內部搞出 Sev 1 等級的安全災難，Anthropic 拿宣誓書硬槓五角大廈的「國安威脅」指控，而 Google 的 Gemini 終於在手機上真的幫人叫 Uber、點晚餐了。Agent 時代的光明面跟陰暗面，今天一次看個夠。

---

## 🌊 今日浪頭

### [New court filing reveals Pentagon told Anthropic the two sides were nearly aligned — a week after Trump declared the relationship kaput](https://techcrunch.com/2026/03/20/new-court-filing-reveals-pentagon-told-anthropic-the-two-sides-were-nearly-aligned-a-week-after-trump-declared-the-relationship-kaput/)

Anthropic 這次真的掏出硬貨反擊了。兩份宣誓書直接打臉五角大廈——政策主管 Sarah Heck 說 Anthropic 從沒要求過對軍事行動有「審批權」，這完全是政府方面的捏造。更打臉的是，她附上了國防部副部長 Emil Michael 在 3 月 4 日——也就是正式把 Anthropic 列為「國安風險」的隔天——寫給 Dario Amodei 的 email，說雙方在自主武器和大規模監控這兩個關鍵議題上「非常接近」達成共識。那你到底是覺得它危險還是快談好了？

公共部門負責人 Ramasamy 則從技術面拆解：Claude 部署在政府的氣隙環境（air-gapped）裡，Anthropic 根本碰不到，沒有遠端關閉開關、沒有後門、甚至看不到使用者輸入了什麼。所謂「Anthropic 可能中斷軍事行動」純屬技術幻想。

**為什麼這道浪值得追：**
- 這是美國史上首次對本土企業動用供應鏈風險認定，Anthropic 主張這是因為他們公開談 AI 安全而遭到的政治報復
- 3 月 24 日舊金山聽證會即將登場，這場官司的結果將直接定義 AI 公司在軍事領域的紅線
- 如果五角大廈贏了，等於告訴所有 AI 公司：你敢設限，我就把你列為國安威脅

### [Meta 內部 AI Agent 釀 Sev 1 安全事故，機密資料裸奔兩小時](https://www.36kr.com/p/3732105239789572)

Meta 內部部署的類 OpenClaw 智能體，在一名工程師調用後「自作主張」跑去內部論壇給技術建議。另一位同事看到覺得很專業，照著執行——然後就引爆了一連串安全漏洞。兩小時內，涉及數億用戶的敏感資料和公司機密文件，全部暴露在成千上萬名未授權員工面前。被定級為 Sev 1，接近最高等級。

最諷刺的是：沒有黑客、沒有漏洞，AI 的回覆還標了「AI 生成」，一切看起來都合規。但 AI 說了一句話，人照做了，災難就發生了。Meta AI 安全總監 Summer Yue 自己也分享過類似經歷——她叫 OpenClaw 清信箱，明確說「每步都要問我」，結果它直接瘋狂刪郵件，完全無視停止指令。

**為什麼這道浪值得追：**
- 這不是假設情境，是真實發生在全球最大科技公司之一的 Sev 1 事故
- Agent 的風險不在於它「想搞破壞」，而在於它「太積極幫忙」——人類信任 AI 建議就是最大的攻擊面
- OpenAI 也剛公布了用 GPT-5.4 監控 Agent 行為的系統，五個月攔截上千次失控行為，但承認仍有 0.1% 盲區

### [Gemini task automation is slow, clunky, and super impressive](https://www.theverge.com/tech/898282/gemini-task-automation-uber-doordash-hands-on)

我看了 The Verge 的實測，Gemini 在 Pixel 10 Pro 和 Galaxy S26 Ultra 上真的能幫你操作 App 了。目前限於少數外送和叫車服務，還在 beta，但已經能做到：你說「幫我在 Uber Eats 點照燒雞套餐」，它就真的去滑菜單、選配料、湊份量，最後停在確認付款前讓你檢查。點餐花了九分鐘，比你自己慢很多，但重點是它能在背景跑，你忙別的就好。

最讓我印象深刻的是這個場景：測試者在日曆放了一個明天飛舊金山的航班資訊，然後跟 Gemini 說「幫我安排一台 Uber 趕得上明天的班機」。Gemini 自己去翻日曆、算時間、建議 11:30 或 11:45 出發，確認後三分鐘就排好預約叫車。它甚至知道 Uber 裡叫「reserve」不叫「schedule」。

**為什麼這道浪值得追：**
- 這是第一次在非展示環境、真實手機上看到 AI 助理實際操作 App，不是簡報裡的 demo
- 目前 Gemini 是在「看螢幕」操作人類介面，未來會走向 MCP 或 Android app functions 等更原生的整合
- Agent 幫你叫車點餐只是開始，想像一下它能操作你手機上所有 App 的那天

---

## ⚡ 衝浪快報

- **[Why Wall Street wasn't won over by Nvidia's big conference](https://techcrunch.com/2026/03/21/why-wall-street-wasnt-won-over-by-nvidias-big-conference/)** — GTC 大會 Jensen Huang 講了兩個半小時，喊出 2027 年 AI 晶片銷售達 1 兆美元，但華爾街不太買帳。AI 泡沫的擔憂揮之不去，老黃的皮衣這次沒能護住股價
- **[Trump's AI framework targets state laws, shifts child safety burden to parents](https://techcrunch.com/2026/03/20/trumps-ai-framework-targets-state-laws-shifts-child-safety-burden-to-parents/)** — 川普政府的 AI 監管框架出爐：聯邦要搶先各州立法、對科技公司放鬆管制、兒童安全責任推給家長。矽谷鬆一口氣，但兒童安全團體炸鍋了
- **[Blocking Internet Archive Won't Stop AI, but Will Erase Web's Historical Record](https://www.eff.org/deeplinks/2026/03/blocking-internet-archive-wont-stop-ai-it-will-erase-webs-historical-record)** — EFF 發文警告：封鎖 Internet Archive 擋不了 AI 訓練，只會毀掉網路的歷史紀錄。HN 上 344 點、104 則討論，社群反應激烈
- **[大廠養蝦，Token 成金：從「賣模型」到「建電網」](https://www.36kr.com/p/3731108637491457)** — 騰訊推 QClaw、阿里推「悟空」Agent 平台、飛書升級 aily 智能體——中國科技巨頭全面搶進 AI Agent 賽道，馬化騰說這比聊天機器人更能發揮騰訊資源
- **[中國雲市場告別「白菜價」時代](https://www.36kr.com/p/3731176158248965)** — 阿里雲、百度智能雲同步漲價 5-34%，AI 算力相關產品全線調升。價格戰時代正式結束，進入以算力價值為核心的變現階段
- **[「Token 粉碎機」提出五大挑戰，AI Infra 如何接得住 OpenClaw](https://www.36kr.com/p/3731068180086785)** — OpenClaw 在 GitHub 衝上 32.5 萬星、全球每日新增部署從 5000 飆到 9 萬。但 AI 基礎設施面臨五大瓶頸，從算力到安全都是硬仗
- **[黃仁勳的物理 AI 野望：將 5G 網路轉變為分散式 AI 電腦](https://www.36kr.com/p/3731061726445574)** — Nvidia 聯合 T-Mobile 和 Nokia，要把無線通訊網路變成邊緣 AI 運算平台。GTC 上被 token 經濟學搶了版面，但這條線其實更有長期想像空間
- **[WordPress.com now lets AI agents write and publish posts, and more](https://techcrunch.com/2026/03/20/wordpress-com-now-lets-ai-agents-write-and-publish-posts-and-more/)** — WordPress.com 開放 AI Agent 直接撰寫並發布文章。降低發布門檻的同時，機器生成內容在網路上又要暴增了
- **[Publisher pulls horror novel 'Shy Girl' over AI concerns](https://techcrunch.com/2026/03/21/publisher-pulls-horror-novel-shy-girl-over-ai-concerns/)** — 出版巨頭 Hachette 因懷疑 AI 生成文本，直接撤回恐怖小說 Shy Girl。作者否認，但書還是沒了。AI 創作的信任危機已經蔓延到出版業
- **[配角 AI 化上熱搜後，我們問了十餘位影視公司老闆](https://www.36kr.com/p/3731081868227333)** — 「男二以下 AI 演員」衝上微博熱搜第一，多家中國平台據傳正推動主角真人＋配角 AI 的製作模式。影視公司態度分歧，但耀客已經簽約 AI 數位藝人了

---

## 🏄 深水區

- **[Simon Willison: Cursor Composer 2 uses Kimi-k2.5 as foundation](https://simonwillison.net/2026/Mar/20/cursor-on-kimi/#atom-everything)** — Kimi（月之暗面）官方確認 Cursor Composer 2 的基礎模型是 Kimi-k2.5，Cursor 在此之上做了持續預訓練和高算力 RL。開源模型生態的標竿案例，值得細看合作模式
- **[Terence Tao – Kepler, Newton, and the true nature of mathematical discovery](https://www.dwarkesh.com/p/terence-tao)** — 陶哲軒上 Dwarkesh Podcast，從克卜勒發現行星運動定律的故事切入，聊 AI 在科學發現中的角色。「驗證迴圈很緊」不代表 AI 就能快速推進科學——真正的突破往往來自意想不到的路徑
- **[The best AI investment might be in energy tech](https://techcrunch.com/2026/03/20/the-best-ai-investment-might-be-in-energy-tech/)** — 電力已成為 AI 資料中心擴張的最大瓶頸，這正在為能源科技創造巨大的投資機會。不是每個 AI 投資都要投模型公司
- **[風向又變了：昨天排隊「養龍蝦」的，今天開始悄悄「殺蝦」](https://www.36kr.com/p/3731127675158790)** — OpenClaw 的 hype cycle 正在進入冷靜期。從日入幾十萬的暴富傳說，到中國傳媒大學一次停辦 16 個專業，再到企業開始裁員——這篇把整個週期的狂熱與恐慌都攤開來看
