---
title: "Cursor 自研模型反超 Opus、OpenAI 急推超級應用搶 Anthropic 客戶、騰訊撤銷 AI Lab"
date: 2026-03-21
description: "Cursor 發布 Composer 2.0 在 Terminal-Bench 反超 Claude Opus 4.6 且價格僅十分之一；OpenAI 計劃合併 ChatGPT、Codex、Atlas 為桌面超級應用反攻企業市場；騰訊撤銷 AI Lab 全面併入混元"
tags: [llm, ai-coding, ai-tools, ai-industry]
---

今天的浪打得很集中——AI coding 戰場全面升級。Cursor 掏出自研模型 Composer 2.0 直接在 benchmark 上幹掉了 Claude Opus 4.6，價格還便宜十倍；OpenAI 那邊則被 Anthropic 打到受不了，決定把 ChatGPT、Codex、Atlas 塞進同一個桌面超級應用裡反攻；而在中國，騰訊直接撤銷了成立十年的 AI Lab，全面押注混元大模型。三件事擺在一起看，你會發現 AI 的競爭已經進入「不做就死」的階段。

---

## 🌊 今日浪頭

### [Cursor 自研新模型 Composer 2.0 反超 Opus 4.6，價格打一折](https://www.36kr.com/p/3731223131176960)

Cursor 放了個大招——自研第二代編程模型 Composer 2.0 正式上線。在 Terminal-Bench 2.0 這個專門測試真實終端操作能力的 benchmark 上，Composer 2 反超了 Claude Opus 4.6。讓我最意外的不是性能，而是定價：普通版輸入 0.5 美元、輸出 2.5 美元，對比 Opus 4.6 的 5 美元和 25 美元——整整便宜十倍。

有開發者拿三個模型做了同一個任務實測：用指定技術棧生成 X 的克隆應用。Composer 2 花了 5 分鐘、6.04 美元，生成的應用直接能跑；Opus 和 GPT-5.4 則分別花了 19 和 22 分鐘，還卡在 CORS 問題上需要額外除錯。代碼品質其實差不多，但效率和成本的差距非常明顯。

但這裡有個更深的故事。Cursor 做自研模型不是為了炫技，而是為了活命。當 Claude Code 和 Codex 這類 CLI agent 越來越強，開發者直接把任務丟給 agent 自己跑，IDE 的中心地位正在被掏空。Cursor 的護城河——「把最強模型裝進最好的 IDE」——在模型廠商自己下場做產品後變得越來越淺。所以 Cursor 必須有自己的模型、自己的 agent 架構，否則就只是個殼。值得注意的是，Composer 2 底層用的是 DeepSeek、Kimi、Qwen 等中國開源模型做二次訓練——中國開源模型正在成為全球 AI 產品的基底。

**為什麼這道浪值得追：**
- IDE 公司自研模型反超頂級 AI 實驗室旗艦，這在一年前不可想像
- 十分之一的價格意味著 AI coding 的成本門檻又降了一個數量級
- Cursor 的生存危機折射出整個 AI 工具鏈的權力重組：模型廠往下吃、agent 往外繞，中間層壓力山大

### [OpenAI 推出「超級應用」，開搶 Anthropic 的企業客戶](https://www.36kr.com/p/3731116431523846)

OpenAI 終於承認被 Anthropic 打痛了。據《華爾街日報》報導，OpenAI 正計劃將 ChatGPT、Codex 和 Atlas 瀏覽器整合為一款桌面級「超級應用」。Sam Altman 和高管們連夜開會重新梳理產品優先級——夺回企業和開發者客戶成為第一要務。

報導裡有個數字很扎心：根據費用管理公司 Ramp 的數據，2026 年 1 月 Anthropic 的模型佔據了近 80% 的 API 支出市場份額。在企業級大模型支出中，Anthropic 約 40%，OpenAI 只有 27%。Claude Code 半年內做到了超 25 億美元的年化收入，全球約 4% 的 GitHub 公開提交代碼由它生成。OpenAI 自己的 Codex 週活 200 萬，下載量剛過百萬——差距很明顯。

有意思的是同一時間 Anthropic 也在動。Claude Cowork 推出了 Dispatch 功能，用手機就能遠程指揮電腦上的 Claude 處理任務。兩家都在做同一件事：把 AI 從聊天框推向桌面工作流入口。而這場貼身肉搏的背後，是雙方衝刺 IPO 的緊迫感——OpenAI 考慮今年 Q4 上市、估值衝擊萬億美元，Anthropic 預計 2028 年收支平衡，比 OpenAI 早兩年。

**為什麼這道浪值得追：**
- Anthropic 在企業 API 市場吃下 80% 份額，OpenAI 被逼到必須「收縮戰線、聚焦核心」
- ChatGPT + Codex + Atlas 合體，標誌著 OpenAI 從「遍地開花」回歸務實路線
- 兩家同時衝刺 IPO，這場企業 AI 戰爭的結果將直接影響千億美元級的估值

### [突發：騰訊 AI Lab 撤銷，部分人員併入混元](https://www.36kr.com/p/3731173493702918)

騰訊做了一個很果斷的決定：直接撤銷成立十年的 AI Lab，把人員併入混元大模型團隊。成立於 2016 年的 AI Lab 曾經是騰訊最重要的 AI 研究陣地，做出過「絕悟」（王者榮耀 AI）、騰訊覓影等明星項目，吸引過張潼、張正友等頂級科學家。但在大模型時代，獨立的研究實驗室模式已經跟不上了。

併入的方向很明確——向 27 歲的姚順雨匯報。這位去年 12 月從 OpenAI 加入騰訊的年輕研究員，頭銜是「CEO/總裁辦公室首席 AI 科學家」，直接向劉熾平匯報。騰訊的意思很清楚：所有 AI 力量往混元大模型集中，不再分散。

同一天還有個消息值得注意：DeepSeek 的核心成員郭達雅（參與過 DeepSeek-V3、R1 等重大項目）已經離職。從騰訊 AI Lab 撤銷、阿里千問負責人林俊暘卸任，到 DeepSeek 人才流動——中國 AI 公司的競爭已經進入了「不留情面、全面重組」的階段。研究歸研究的時代結束了，現在只有一個問題：你的大模型能不能打？

**為什麼這道浪值得追：**
- 十年研究實驗室一朝撤銷，騰訊 All-in 混元大模型的決心很明確
- 27 歲的前 OpenAI 研究員統領騰訊 AI 核心，人才爭奪戰白熱化
- DeepSeek 核心成員離職，中國 AI 人才大洗牌正在加速

---

## ⚡ 衝浪快報

- **[OpenCode – The open source AI coding agent](https://opencode.ai/)** — 又一個開源 AI coding agent，HN 上 266 分 118 則留言，看起來社群很買帳。能不能跟 Claude Code 搶人就看後續了
- **[Google Search is now using AI to replace headlines](https://www.theverge.com/tech/896490/google-replace-news-headlines-in-search-canary-coal-mine-experiment)** — Google 開始用 AI 改寫搜尋結果裡的新聞標題，這個操作讓新聞業又緊張了一波
- **[Trump takes another shot at dismantling state AI regulation](https://www.theverge.com/ai-artificial-intelligence/898055/trump-new-ai-policy-framework)** — Trump 推出七點 AI 監管框架，核心訊息就一個：聯邦政府輕管、各州別亂管
- **[Claude Code 新增 Channels 功能：手機遠程遙控寫代碼](https://www.36kr.com/p/3730899849773313)** — 透過 Telegram 或 Discord 直連 Claude Code 會話，躺在床上用手機就能讓 Mac Mini 狂敲代碼，龍蝦化（OpenClaw 化）又進一步
- **[貝佐斯籌資 1000 億美元，設立基金收購製造企業並引入 AI](https://www.36kr.com/p/3730942149902599)** — 1000 億美元收購製造業 + AI，貝佐斯要用 AI 重塑實體經濟，格局比賣雲大多了
- **[黃仁勳開啟 Token 時代：OpenRouter 年化吞吐破千萬億 Token](https://www.36kr.com/p/3730899885998344)** — 僅 OpenRouter 一個平台的年化 Token 量就破了一千萬億，按每百萬 Token 1 美元算是年化 10 億美元推理支出
- **[Microsoft rolls back some of its Copilot AI bloat on Windows](https://techcrunch.com/2026/03/20/microsoft-rolls-back-some-of-its-copilot-ai-bloat-on-windows/)** — 微軟終於聽到使用者的怒吼，開始減少 Windows 上的 Copilot 入口點。Photos、Widgets、Notepad 先撤
- **[AI 風越大，雲計算越貴：阿里雲百度雲集體漲價](https://www.36kr.com/p/3731181375697670)** — 阿里雲算力卡漲 5-34%，百度智能雲跟進漲 5-30%。AI 需求推高成本，雲計算近 20 年來首次集體漲價
- **[第一批被 AI 裁掉的大廠人已經返崗了](https://www.36kr.com/p/3730984041873665)** — Block 裁掉 4000 人說「AI 改變了一切」，結果不到一個月就開始回召。AI 替代人類這件事，現實比想像骨感
- **[「男二以下全換 AI」吵翻全網](https://www.36kr.com/p/3731154098454537)** — 中國影視圈爆出「主角真人 + 配角 AI」模式，AI 數位藝人已經開始簽約了。聽起來很科幻但離落地還有段距離

---

## 🏄 深水區

- **[8 萬人對話 Claude 後，Anthropic 發現人類對 AI 的真實渴望](https://www.36kr.com/p/3731116933087241)** — 一週內 80,508 人、159 個國家、70 種語言，可能是史上最大規模的 AI 用戶定性研究。有人被 AI 幫助確診了九年未解的病，也有人因為跟 AI 聊太多失去了現實中的朋友——值得靜下心來讀
- **[阿里、Kimi、螞蟻集體押注，混合注意力從可選項變必答題？](https://www.36kr.com/p/3731179814519046)** — 小米 Mimo-V2 Pro 用 1:7 混合注意力比例做到接近 Opus 4.6 能力但只要五分之一價格，蚂蟻、阿里、月之暗面全都在走這條路。下一代模型架構的共識正在形成
- **[Why people really hate AI](https://www.theverge.com/podcast/897900/ai-trust-gap-killer-app-vergecast)** — The Verge 探討 AI 信任鴻溝：公司拚命塞 AI 進每個產品，但一般人對 AI 的態度越來越負面。問題不在技術，在於沒人問用戶「你到底需不需要這個」
- **[What happened at Nvidia GTC: NemoClaw, Robot Olaf, and a $1 trillion bet](https://techcrunch.com/video/what-happened-at-nvidia-gtc-nemoclaw-robot-olaf-and-a-1-trillion-bet/)** — GTC 大會精華回顧：老黃預估 2027 前 AI 晶片銷售破 1 兆美元、每家公司都需要 OpenClaw 策略，最後還搬了個 Olaf 機器人出來。皮衣男的舞台功力依舊
