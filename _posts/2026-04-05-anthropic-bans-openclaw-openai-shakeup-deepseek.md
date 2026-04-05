---
title: "Anthropic 封殺 OpenClaw、OpenAI 高層大地震、DeepSeek 癱了 12 小時"
date: 2026-04-05
description: "Anthropic 直接把 OpenClaw 踢出 Claude 訂閱，OpenAI 三位高管同時異動，DeepSeek 史上最長宕機暴露算力瓶頸。AI 產業的裂縫正在同時裂開。"
tags: [llm, agents, ai-industry, ai-tools]
---

今天 AI 圈的浪有點亂——Anthropic 週五傍晚偷偷丟了一顆深水炸彈，直接把 OpenClaw 從 Claude 訂閱裡踢出去；OpenAI 那邊更熱鬧，AGI 部署負責人請病假、COO 轉做特殊專案、CMO 因抗癌辭職，三把交椅同時空出來。另一邊太平洋這頭，DeepSeek 上週末直接癱了 12 小時，「養龍蝦」的人把算力吃光了。三件事看似獨立，但都指向同一個問題：AI 的成長速度正在把自己的基礎設施和組織架構撐到極限。

---

## 🌊 今日浪頭

### [Anthropic essentially bans OpenClaw from Claude by making subscribers pay extra](https://www.theverge.com/ai-artificial-intelligence/907074/anthropic-openclaw-claude-subscription-ban)

Anthropic 選了一個經典的「週五晚間新聞傾倒」時間點，宣布從 4 月 4 日起，Claude 訂閱用戶不能再用訂閱額度跑 OpenClaw 等第三方工具了。想繼續用？請走 pay-as-you-go，額外付費。Claude Code 主管 Boris Cherny 的說法是「訂閱方案本來就不是為這些第三方工具的使用模式設計的」，翻成白話就是：你們用太兇了，我們撐不住。

以我的觀察，這步棋下得很精準但也很危險。OpenClaw 創辦人 Peter Steinberger 已經跳槽到 OpenAI 了——你的競爭對手的人在開發一個工具，瘋狂消耗你的算力，你當然不爽。Steinberger 自己也承認他和 OpenClaw 董事 Dave Morin「試圖跟 Anthropic 講理，最多只爭取到延後一週」。但問題是，OpenClaw 幫 Claude 帶了多少用戶？把這些人推走，他們可能直接轉投 OpenAI 的懷抱。

**為什麼這道浪值得追：**
- Anthropic 給每位訂閱者一次性補償一個月訂閱費的 credit，還開放全額退款——這等於承認會有用戶流失
- 這是 AI 平台經濟的第一次「斷奶」事件：當第三方生態的算力消耗超過平台能承受的範圍，平台會毫不猶豫地切斷
- Anthropic 自家的 Claude Cowork 正好在這時候推廣，意圖再明顯不過——想用 Agent？用我自己的

### [OpenAI's AGI boss is taking a leave of absence](https://www.theverge.com/ai-artificial-intelligence/906965/openais-agi-boss-is-taking-a-leave-of-absence)

OpenAI 的 C-suite 又地震了。AGI 部署負責人 Fidji Simo 因為神經免疫疾病復發，宣布請數週病假。她在內部信裡坦承「從入職前就復發了，一直硬撐到現在」，連必要的醫療檢查都延後了好幾個月。她不在的期間，Greg Brockman 接手產品方向，Jason Kwon、Sarah Friar、Denise Dresser 分管商業營運。

同時，COO Brad Lightcap 也卸任，轉做向 Sam Altman 直接匯報的「特殊專案」。CMO Kate Rouch 則因為抗癌需要，辭去行銷長一職。三位高管同時異動，對一家正在衝刺 IPO 的公司來說，震撼程度不小。

**為什麼這道浪值得追：**
- 這是 OpenAI 連續第二季出現高管大規模異動——年初通訊長 Hannah Wong 離職，一月才砍掉 Sora，現在又是三人同時走
- Simo 的坦白信讓人意外地感動，但也暴露了矽谷高層「帶病上陣」的文化問題。她說「為了不錯過一天工作，把所有醫療都往後推」
- Brad Lightcap 從 COO 轉做「特殊專案」，在矽谷語言裡這通常不是升遷。加上昨天收購 TBPN 的消息，OpenAI 的戰略方向看起來越來越分散

### [DeepSeek 癱瘓 12 小時，國產大模型的算力已經跟不上野心了？](https://www.36kr.com/p/3750856080863749)

3 月 29 日晚上 9 點 35 分開始，DeepSeek 的網頁端和 App 幾乎同時掛掉。最痛苦的不是直接崩，而是「反覆橫跳」——23 點短暫恢復、零點再次崩盤、凌晨緊急修復，直到隔天早上才穩定。整整 12 小時，刷新了 DeepSeek 的宕機紀錄。

官方的解釋是「用戶太多」，但實際月活大約 1.5 億，並沒有突然暴增。真正的放大器是「養龍蝦」——基於 Agent 框架的自動化調用，每分鐘甚至每秒都在打 API，少量用戶就能製造巨大的算力壓力。這跟 Anthropic 封��� OpenClaw 的邏輯一模一樣：Agent 時代的使用模式，正在把為聊天設計的基礎設施打爆。

**為什麼這道浪值得��：**
- V4 即將到來，上下文從 128K 跳到百萬級、多模態和 Agent 能力同步增強——算力需求只會更大，不會更小
- MiniMax 已經開始在高峰期限制調用頻率，阿里雲也在調整定價。不只 DeepSeek，整個中國 AI 基礎設施都在承壓
- AI 競爭正在從「模型層」遷移到「基礎設施層」——誰能穩定地跑、跑得起，比跑分高更重要

---

## ⚡ 衝浪快報

- **[Anthropic is having a moment in the private markets; SpaceX could spoil the party](https://techcrunch.com/2026/04/03/anthropic-is-having-a-moment-in-the-private-markets-spacex-could-spoil-the-party/)** — Anthropic 成了二級市場最搶手的標的，有機構說「接觸幾百家投資人，一個願意買 OpenAI 的都沒有」。馬斯克聽到馬上來嘴：「不意外。」SpaceX IPO 可能吸走大量資金
- **[OpenClaw gives users yet another reason to be freaked out about security](https://arstechnica.com/security/2026/04/heres-why-its-prudent-for-openclaw-users-to-assume-compromise/)** — OpenClaw 最近修了一個安全漏洞，但安全專家的建議是「假設自己已經被入侵」。一個月前就有人警告了，現在才有人聽
- **[OpenAI buys tech-focused talk show TBPN for "low hundreds of millions"](https://arstechnica.com/ai/2026/04/openai-takes-on-another-side-quest-buys-tech-focused-talk-show-tbpn/)** — 11 個人的公司賣了小幾億美元，OpenAI 說要「推動圍繞 AI 變革的建設性對話」。明明說好不搞 side quest 了，結果又買了一家媒體公司
- **[Seedance 2.0 正式開放、120 萬億 tokens 打底](https://www.36kr.com/p/3750643774456320)** — 火山引擎宣布豆包大模型日均 Token 使用量突破 120 萬億，三個月翻一倍。Seedance 2.0 的鋼琴演奏 demo 音畫同步到讓人起雞皮疙瘩
- **["Cognitive surrender" leads AI users to abandon logical thinking](https://arstechnica.com/ai/2026/04/research-finds-ai-users-scarily-willing-to-surrender-their-cognition-to-llms/)** — 新研究發現，部分 AI 使用者完全放棄了自己的邏輯思考，把所有判斷都交給 LLM。研究者用了一個詞：「認知投降」
- **[華人博士揪出 Claude Code 51 萬行源碼洩露](https://www.36kr.com/p/3750770295898630)** — 安全研究員 Chaofan Shou 在 npm 發布包裡發現 Anthropic 忘了刪 source map，51 萬行核心架構一覽無遺。Anthropic 已請求下架超 8000 個 GitHub repo，承認是人為失誤
- **[華爾街六大行裁員萬人，AI 重塑人力格局](https://www.36kr.com/p/3750989309477384)** — 富國銀行連續 22 季削減員工，摩根大通在紐澤西裁超 250 人，美銀 CEO 直接說要用 AI「調整員工人數」。金融業的 AI 替代不再是預測，是現在進行式
- **[Karpathy 解鎖大模型新玩法：個人知識庫](https://www.36kr.com/p/3751033456263943)** — 卡神親自出手搭建 AI 驅動的個人知識庫，重點是這個知識庫會自己更新、越用越聰明。他自己都說「大部分 Token 已經不跑程式碼了，都拿來跑知識庫」
- **[光通信供應鏈告急，台積電產能成瓶頸](https://www.36kr.com/p/3750921724461829)** — 博通直言台積電的產能限制已經扼制了 2026 年光通信供應鏈。日本 Granopt 大幅縮減法拉第旋光片產能，交付週期從數週拉長到 6-9 個月。AI 的算力飢渴正在沿供應鏈向上傳導
- **[大廠 AI 敘事走向殊途：京東務實、騰訊變狠、快手最危險](https://www.36kr.com/p/3750765941731840)** — 財報季結束，中國大廠的 AI 故事開始分化。百度、騰訊、阿里、快手股價紛紛掉頭向下，唯有京東逆勢上漲。資本不再買「我在做 AI」的故事，要看「AI 幫你賺了多少」

---

## 🏄 深水區

- **[Premium: AI Isn't Too Big To Fail](https://www.wheresyoured.at/premium-ai-isnt-too-big-to-fail/)** — Ed Zitron 最新長文直接挑戰「AI 就像早期 Uber/AWS」的類比邏輯，逐條拆解為什麼這次泡沫不一樣。如果你對 AI 投資泡沫有任何疑慮或好奇，這篇是目前最完整的反方論述
- **[The two wildest stories today in tech](https://garymarcus.substack.com/p/the-two-wildest-stories-today-in)** — Gary Marcus 抓到微軟的 Mustafa Suleyman 悄悄把「超級智慧」的定義從「比最聰明的人類更聰明」降級成「能為數百萬人創造產品價值的 AI」。定義降級了，目標就自動達成了，對吧？
- **[GitHub 活動量暴增：年化 140 億 commits、Actions 週用量 21 億分鐘](https://simonwillison.net/2026/Apr/4/kyle-daigle/#atom-everything)** — GitHub 平台負責人 Kyle Daigle 分享的數據讓人瞠目：2025 年 10 億 commits，現在週均 2.75 億，年化 140 億。GitHub Actions 從 2023 年的 5 億分鐘/週飆到 21 億。AI coding 工具的普及正在用數據證明自己
- **[龍蝦本紀](https://www.36kr.com/p/3750917106319878)** — 一篇寫得極好的 OpenClaw「龍蝦」興衰史。從一夜爆火到全民冷卻，龍蝦最大的遺產不是它自己，而是驗證了 Agent 這條路是走得通的。「其興也勃焉，其衰也忽焉」——如果未來有一部《AI 史記》，其中必有一篇《龍蝦本紀》
