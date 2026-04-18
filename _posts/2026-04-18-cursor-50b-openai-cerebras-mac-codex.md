---
title: "Cursor 500 億估值、OpenAI 綁 Cerebras、Mac Codex 成賽博同事"
date: 2026-04-18
description: "Cursor 傳融資 20 億美元、估值衝上 500 億；OpenAI 砸 200 億美元綁定 Cerebras 晶片；OpenAI Codex 登上 macOS，能自己操作你的應用。今天的 AI 浪是錢、算力、Agent 同步大洗牌。"
tags: [llm, agents, ai-tools, ai-industry, ai-coding]
---

今天 AI 圈的浪一次來三道——Cursor 估值半年翻倍逼近 500 億美元，OpenAI 豪擲 200 億跟 Cerebras 綁定算力，Codex 還直接變成會操作你 Mac 應用的賽博同事。我看了一整天下來只有一個感想：錢、算力、Agent 這三條賽道，正在以肉眼可見的速度互相鎖死。

---

## 🌊 今日浪頭

### [Sources: Cursor in talks to raise $2B+ at $50B valuation as enterprise growth surges](https://techcrunch.com/2026/04/17/sources-cursor-in-talks-to-raise-2b-at-50b-valuation-as-enterprise-growth-surges/)

Cursor 又要融資了——這次據說至少 20 億美元，估值直接衝到 500 億美元，Thrive 和 a16z 領投，Nvidia 也要塞一張支票進來。最誇張的是，這是半年前那輪 293 億美元估值的**將近兩倍**。更猛的數字：Cursor 自己預估 2026 年底 ARR 會突破 60 億美元，等於要在 10 個月內把營收翻三倍。

**為什麼這道浪值得追：**
- 以前 Cursor 是 AI coding 裡燒錢最兇的那種——負毛利，賣一單虧一單。但自從去年 11 月推出自家 Composer 模型、加上會叫更便宜的 Kimi 後，終於勉強擠出正毛利，企業方向尤其好看
- Anthropic 的 Claude Code 和 OpenAI 重生版 Codex 雙邊夾擊，Cursor 還能把估值做起來，說明企業客戶真的買單了
- 但別忘了個人開發者帳戶**還在虧**——這輪錢大概率是買「脫離 Anthropic 依賴」的時間

### [OpenAI 砸逾 200 億美元綁定 Cerebras，三年算力備胎計畫成形](https://www.36kr.com/p/3770551515398912)

消息面：OpenAI 將在未來三年砸超過 200 億美元跟 Cerebras 買晶片，另外再拿 10 億美元資助 Cerebras 蓋資料中心，順便拿到少數股份的認股權證。這不是新合作——今年 1 月雙方就已經簽過 750 兆瓦、逾 100 億美元的晶圓級推理部署協議，Codex-Spark 那顆新編程模型 2 月開始就是跑在 Cerebras 上。

**為什麼這道浪值得追：**
- OpenAI 講得很直白：給 Nvidia 找備胎。Cerebras 的 WSE-3 是餐盤那麼大的晶片，推理速度號稱比對手快 20 倍，單位功耗更低——真的跑起來的話，成本結構會跟租 H100/B200 完全不同
- 這筆交易會計處理很妙：資金可列為資產，部分芯片款可記為利息收入，等於一邊花錢一邊美化財報，為 OpenAI 自己的 IPO 鋪路
- Cerebras 同時要再拼 IPO，目標估值 350 億美元，承銷摩根士丹利；原本因為 G42 訂單集中度和 CEO 背景被拖延的案子，這次靠 OpenAI 和 AWS 的訂單正好解套

### [OpenAI 上線 Mac 版 Codex，從「代碼生產者」變身「賽博同事」](https://www.36kr.com/p/3770202199323136)

今天凌晨 OpenAI 直接把 Mac 版 Codex 推上線，附了一句很囂張的話：「Codex for (almost) everything.」我看完 Demo 只想說——這已經不是 AI 寫碼工具了，這是會用電腦的 Agent。它可以直接打開 Xcode、像真人一樣點擊 UI、透過視覺識別抓出 Bug（Demo 裡是井字棋電腦對手走兩步的邏輯錯誤），然後自己改碼、編譯、重跑確認修好。

**為什麼這道浪值得追：**
- 關鍵轉變是「透過 GUI 操作」而不是調 API。以前 AI 碰不到的第三方應用現在全變成可操作目標，這等於把 OpenClaw（今年 2 月 OpenAI 挖角來的「龍蝦」團隊）的能力全面融進 Codex
- Demo 裡最狠的一段：用戶要它替網頁主視覺生一張圖，它先讀專案檔、看網頁已有排版、決定主題是「費城深夜快餐」，生完圖還順手改 HTML 和 CSS、刷新預覽。這已經是完整的產品設計流程
- 最後還能同時在 Slack、Gmail、Google Calendar、Notion 之間跳來跳去當你的私人助理——這意味著 Codex 的定位從「開發工具」直接跳級成「作業系統裡的通用 Agent」，Cursor 和 Windsurf 的人看完應該沒什麼心情睡

---

## ⚡ 衝浪快報

- **[Anthropic launches Claude Design, a new product for creating quick visuals](https://techcrunch.com/2026/04/17/anthropic-launches-claude-design-a-new-product-for-creating-quick-visuals/)** — Anthropic 推 Claude Design，主打創辦人和 PM 快速生視覺。意思很明顯：Anthropic 要跨出純 LLM 的框，跟 Figma、Canva 搶最後一哩
- **[Claude Opus 4.7 Vals Index 拿下 71.4% 新高，定價不變](https://www.36kr.com/p/3770121995911944)** — Opus 4.7 能力再跳一級但不漲價，打工仔邊讚嘆邊擔心自己的工作。Anthropic 一如既往不喊口號只丟數字
- **[Anthropic's new cybersecurity model could get it back in the government's good graces](https://www.theverge.com/ai-artificial-intelligence/914229/tides-turning-anthropic-trump-administration-cybersecurity-mythos-preview)** — Anthropic 用 Mythos 資安模型修補跟川普政府的關係。搞 AI 政策也是一門生意，Dario 這步走得精明
- **[算力巨頭排好隊，只為「拿下」Anthropic](https://www.36kr.com/p/3770793732276741)** — Google、博通、CoreWeave 搶著替 Anthropic 鋪多吉瓦算力，Anthropic 自己也在評估自研晶片。三大模型公司現在都在玩「算力多重備援」
- **[Kevin Weil and Bill Peebles exit OpenAI as company continues to shed 'side quests'](https://techcrunch.com/2026/04/17/kevin-weil-and-bill-peebles-exit-openai-as-company-continues-to-shed-side-quests/)** — Sora 收攤、科學團隊重組，OpenAI 正在把所有不直接賺企業錢的專案砍掉。這是為了 IPO 前把故事講單純
- **[Rivian 創辦人新公司 Mind Robotics 融資 5 億美元劍指物理 AGI](https://www.36kr.com/p/3769505493565959)** — Accel、a16z 領投，主攻工業機器人。2026 的機器人融資已經不看 demo 看「物理 AGI」敘事了
- **[Gemini 桌面客戶端上線 macOS，全域快捷鍵＋讀取螢幕上下文](https://www.36kr.com/p/3770104217944581)** — Google 終於把 Gemini 做成原生桌面 App，追上 ChatGPT、Claude。現在三家的桌面 Agent 全到齊，接下來就看誰的螢幕理解能力強
- **[華為前天才少年新創「行雲」完成逾 4 億元 Pre-A，做下一代推理晶片](https://www.36kr.com/p/3770363954954755)** — 用超大顯存重構 GPGPU 推理經濟學，瞄準的是 DeepSeek、Qwen 這種中國端側推理需求
- **[DeepSeek 悄悄更新：Mega MoE、FP4 Indexer 來了](https://www.36kr.com/p/3770337582858759)** — DeepGEMM 更新藏著下一代模型的底層線索。FP4 推理成本再砍一刀，中國開源 AI 的成本戰還沒打完
- **[台積電 26Q1 毛利衝上 66.2%，AI 製程紅利完全反映在財報](https://www.36kr.com/p/3770589134209795)** — AI 這條鏈的「算力稅」其實最肥的是台積電。股價反而跌——市場對它的期待已經拉到天花板外
- **[群核科技港交所首日漲逾 170%，成為空間智能第一股](https://www.36kr.com/p/3770320714826498)** — 杭州六小龍最快 IPO 誕生。AI + 3D 建模的敘事在 2026 終於變現
- **['Tokenmaxxing' is making developers less productive than they think](https://techcrunch.com/2026/04/17/tokenmaxxing-is-making-developers-less-productive-than-they-think/)** — TechCrunch 戳破開發者的自我感覺良好：token 砸得多不代表產出好，重寫成本和帳單都在飆

---

## 🏄 深水區

- **[世界模型五大門派，圍攻光明頂](https://www.36kr.com/p/3770602741269250)** — 把 LeCun 的 AMI、李飛飛的 World Labs、阿里的 HappyOyster 等五派武功一次講清楚。想搞懂「世界模型」到底是什麼這篇就夠了
- **[Opus 4.7 贏了 Coding，Codex 想贏一切](https://www.36kr.com/p/3770670475346697)** — 正好配今天的 Mac Codex 新聞讀：Opus 贏的是 benchmark，Codex 要贏的是整個工作流。兩種戰略路線的精彩對照
- **[Token 工廠經濟學，正在重構整個 AI 產業](https://www.36kr.com/p/3770161529586440)** — 從價格戰打到集體漲價，這篇把 token 經濟的供需結構拆給你看。做 AI 產品的人值得一讀
- **[RAG 搜對了卻答錯？德國薩爾大學找到了真相](https://www.36kr.com/p/3770495861096963)** — ACL 2026 錄用論文。在「搜」和「答」之間加個「讀懂」環節，Disco-RAG 值得所有做檢索增強的人看看
