---
title: "Gemma 4 全面開源 Apache 2.0、豆包日燒 120 萬億 Token、微軟自研模型三連發"
date: 2026-04-03
description: "Google 發布 Gemma 4 四款模型並改用 Apache 2.0 授權，字節豆包日均 Token 消耗量突破 120 萬億追平 OpenAI，微軟 MAI 團隊推出語音轉錄、語音生成與圖像三款基礎模型。"
tags: [llm, ai-tools, ai-industry, ai-coding]
---

今天的浪又大又密——Google 終於想通把 Gemma 換上 Apache 2.0，字節的 Token 燃燒速度已經追上 OpenAI 和 Google 的全球級別，微軟則悄悄亮出自研模型的底牌。三家巨頭同一天各自放招，這種密度的 AI 新聞，喝咖啡的手都不敢停。

---

## 🌊 今日浪頭

### [Google announces Gemma 4 open AI models, switches to Apache 2.0 license](https://arstechnica.com/ai/2026/04/google-announces-gemma-4-open-ai-models-switches-to-apache-2-0-license/)

等了整整一年，Google 終於把 Gemma 系列做了一次全面大升級。Gemma 4 一口氣推出四種尺寸——31B Dense、26B MoE、E4B 和 E2B——但真正讓開發者圈炸鍋的不是模型本身，而是授權協議從自家那套限制一堆的 Gemma License 直接換成了 Apache 2.0。這代表你可以自由商用、修改、再分發，Google 不能再單方面改規則。去年一整年開發者對 Gemma 3 授權的抱怨，Google 顯然聽進去了。

**為什麼這道浪值得追：**
- 31B 模型在 Arena AI 排行榜拿下開源模型第三名，但參數量只有前兩名的十分之一——性價比炸裂
- 26B MoE 版本推論時只啟用 3.8B 參數，速度快到飛起，適合需要高吞吐的 Agent 場景
- E2B 和 E4B 專為手機和邊緣裝置設計，能在 Raspberry Pi 上離線跑，下一代 Gemini Nano 4 也將基於這些模型
- 256K context window、支援 140+ 語言、原生 function calling——開源模型的天花板又被墊高了

### [每天燒 120 萬億 Token，這是 AI 圈最新的凡爾賽](https://www.36kr.com/p/3750262409150976)

字節跳動的火山引擎丟出一個讓人倒吸涼氣的數字：豆包大模型日均 Token 使用量突破 120 萬億。三個月前這數字還是 60 萬億，兩年前發布時是現在的千分之一。更猛的是，全球日均 Token 消耗超過 100 萬億的公司只有三家：OpenAI、Google、字節跳動。前兩家靠全球市場，字節主要靠中國市場就追平了。

**為什麼這道浪值得追：**
- Agent 時代的 Token 消耗邏輯徹底變了——一個複雜 Agent 任務的 Token 量是普通對話的幾十到上百倍，OpenClaw 用戶日均消耗是傳統聊天的 20-50 倍
- 中國 AI 大模型周 Token 調用量已連續三週超越美國，全球份額 36%
- 價格也在漲：智譜一季度 API 定價提升 83%，阿里雲、百度、騰訊雲同期集體漲價——Token 正在從「免費午餐」變成「基礎貨幣」
- 火山引擎同步開放 Seedance 2.0 企業版 API，並與 OpenClaw 共建 ClawHub 中國鏡像站

### [Microsoft takes on AI rivals with three new foundational models](https://techcrunch.com/2026/04/02/microsoft-takes-on-ai-rivals-with-three-new-foundational-models/)

微軟的 MAI 超級智慧團隊（去年 11 月由 Mustafa Suleyman 組建）交出了第一份正式答卷：三款自研基礎模型。MAI-Transcribe-1 支援 25 語言語音轉文字，速度是 Azure Fast 的 2.5 倍；MAI-Voice-1 可以一秒生成 60 秒音訊並支援自訂聲音；MAI-Image-2 負責圖像生成。三款模型都強調「比 Google 和 OpenAI 更便宜」這個賣點。

**為什麼這道浪值得追：**
- 微軟在 OpenAI 身上砸了 130 億美元，現在自己也開始做模型了——這不是背刺，但絕對是買保險
- Suleyman 同時表態要追求「超級智慧」，微軟的 AI 野心已經不只是當 OpenAI 的雲端房東
- 定價策略直接對標競品：語音轉錄 $0.36/小時、語音生成 $22/百萬字元——走的是量大管飽路線

---

## ⚡ 衝浪快報

- **[OpenAI acquires TBPN](https://techcrunch.com/2026/04/02/openai-acquires-tbpn-the-buzzy-founder-led-business-talk-show/)** — OpenAI 收購了矽谷當紅科技脫口秀 TBPN，Sam Altman 開始買媒體了，這操作怎麼越來越像某位前任總統
- **[Google Vids 加入 Lyria 3 + Veo 3.1 免費 AI 影片生成](https://blog.google/products-and-platforms/products/workspace/google-vids-updates-lyria-veo/)** — Google Workspace 用戶現在可以免費用 AI 生成高品質影片，Sora 剛收攤 Google 就接手了
- **[Gemini API 推出 Flex 和 Priority 推論層級](https://blog.google/innovation-and-ai/technology/developers-tools/introducing-flex-and-priority-inference/)** — 想省錢用 Flex、想要低延遲用 Priority，Google 終於讓開發者自己選成本和速度的平衡點
- **[Codex 為團隊推出按用量計費方案](https://openai.com/index/codex-flexible-pricing-for-teams)** — ChatGPT Business 和 Enterprise 用戶現在可以按需付費使用 Codex，降低團隊導入門檻
- **[Anthropic 承認 DMCA 誤傷合法 GitHub 倉庫](https://arstechnica.com/ai/2026/04/anthropic-says-its-leak-focused-dmca-effort-unintentionally-hit-legit-github-forks/)** — 昨天的 Claude Code 洩漏事件後續：Anthropic 為了下架洩漏的原始碼，結果「無差別攻擊」誤刪了數千個合法 fork，現已恢復
- **[Microsoft 的「超級智慧」新計畫](https://www.theverge.com/report/905791/mustafa-suleyman-microsoft-ai-transcription-model)** — Suleyman 卸下部分職責專攻超級智慧研究，微軟內部重組後 AI 野心更明確了
- **[OpenAI 股票二級市場遇冷，Anthropic 溢價遭瘋搶](https://www.36kr.com/p/3749514322821639)** — OpenAI 六億美元股份打九折都沒人要，Anthropic 門口卻排著 20 億美元的長龍——市場在用真金白銀投票
- **[Lemonade by AMD：開源本地 LLM 伺服器](https://lemonade-server.ai)** — AMD 推出用 GPU + NPU 跑本地 LLM 的開源方案，HN 242 個讚，終於不是只有 NVIDIA 能玩了
- **[Vibe Coding 是一場生產力騙局嗎？](https://www.36kr.com/p/3750319030108935)** — 從 Node.js 核心貢獻者在 GitHub 上的一次 PR 開始，這個問題被拉上了正式的討論桌面
- **[Cloudflare 工程師用 AI 一個週末複刻 Next.js，成本 1100 美元](https://www.36kr.com/p/3749387382522631)** — 把 Next.js 遷移到 Vite 上做成 Vinext，已能在 Cloudflare Workers 上跑生產環境，冷啟動快 40%
- **[人被做成 .skill——GitHub 新趨勢](https://www.36kr.com/p/3750265177899778)** — 同事.skill、前任.skill、boss.skill 在 GitHub 上爆火，把一個人的聊天記錄和工作風格封裝成 AI Skill

---

## 🏄 深水區

- **[Highlights from my conversation about agentic engineering on Lenny's Podcast](https://simonwillison.net/2026/Apr/2/lennys-podcast/#atom-everything)** — Simon Willison 上了 Lenny Rachitsky 的播客聊 agentic engineering 的現狀，從 dark factory 到自動化時間表，想聽圈內人怎麼看 Agent 趨勢的別錯過
- **[一文讀懂 Harness Engineering](https://www.36kr.com/p/3749464991187458)** — LangChain 的實驗數據顯示，同一個模型換套更好的 Harness 架構，Terminal Bench 通過率從 52.8% 直接拉到 66.5%——模型沒動一個字節，排名狂飆前五。這篇把 14 篇工程文章梳理了一遍
- **[構建 Claude Code 的經驗教訓：從智能體的視角觀察](https://www.36kr.com/p/3749387562550019)** — 深入拆解 Claude Code 的工具設計哲學：是只給一個 bash 就好，還是要 50 個專用工具？動作空間的設計直接決定了 Agent 的天花板
- **[Infinite midwit](https://www.experimental-history.com/p/infinite-midwit)** — 一篇有意思的反直覺觀點：AI 越強，作者反而越不焦慮了。對於靠文字吃飯的人來說，這篇值得花 15 分鐘細讀
