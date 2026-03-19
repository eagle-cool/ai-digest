---
title: "五角大廈封殺 Anthropic、GPT-5.4 mini 出師不利、小米 MiMo 神秘揭面"
date: 2026-03-19
description: "美國國防部稱 Anthropic 紅線構成國安風險、OpenAI 新模型 GPT-5.4 mini 排名慘輸中國模型、小米揭曉 OpenRouter 匿名冠軍真身 MiMo V2 三連發"
tags: [llm, agents, ai-industry, ai-safety]
---

今天的浪打得又急又深——美國國防部直接把 Anthropic 貼上「國安威脅」標籤，OpenAI 發了個新模型結果被嫌棄到不行，而小米悄悄在 OpenRouter 上霸榜的神秘模型終於揭開面紗。這三件事放在一起看，你會發現 AI 產業正在經歷一場微妙的權力重組。

---

## 🌊 今日浪頭

### [DOD says Anthropic's 'red lines' make it an 'unacceptable risk to national security'](https://techcrunch.com/2026/03/18/dod-says-anthropics-red-lines-make-it-an-unacceptable-risk-to-national-security/)

這件事的嚴重程度可能被很多人低估了。美國國防部在加州聯邦法院提交了一份 40 頁的文件，核心論點是：Anthropic 可能會在「作戰行動」中「試圖禁用其技術或預先改變模型行為」，因為該公司有自己的「紅線」。背景是 Anthropic 去年簽了五角大廈 2 億美元的合約，把技術部署在機密系統中，但後來在談判中表示不希望 AI 被用於大規模監控美國人或致命武器的瞄準決策。國防部的態度很明確：私人公司不該決定軍方怎麼用技術。

這不只是一場合約糾紛。OpenAI、Google、Microsoft 的員工都提交了支持 Anthropic 的法庭文件。憲法律師 Chris Mattei 直言國防部「完全依賴推測性的想像來為一個非常嚴重的法律步驟辯護」。下週二就要開聽證會了——這場仗的結果，會直接定義 AI 公司在軍事應用中有沒有說「不」的權利。

**為什麼這道浪值得追：**
- AI 安全紅線 vs 軍事需求，這是第一次在法庭上正面交鋒
- 連競爭對手 OpenAI 和 Google 都站出來挺 Anthropic，說明整個產業都在緊張
- 判決結果將為所有 AI 公司與政府的合作關係立下先例

### [OpenAI GPT-5.4 mini Day0 就被嫌棄，排名不如一月底的國產模型](https://www.36kr.com/p/3728345370033029)

我看了一下各方測試，老實說有點尷尬。GPT-5.4 mini 在 Vals 基準上排第 13 名，排在它前面的是一月底發布的 Kimi 2.5——還便宜一倍多、延遲更低。在拓撲證明測試中，mini 和 nano 也只排到第九第十，不如 Kimi、Qwen、DeepSeek 這些更早發布的模型。

但冷靜分析一下，OpenAI 的策略其實不難懂：mini 和 nano 主打的是編程、Agent 子代理和電腦操作，速度快兩倍，nano 每百萬 token 才 0.2 美元。問題是，同樣叫 mini，新版比舊版 GPT-5 mini 貴了三倍。在龍蝦熱潮中，所有模型廠都在漲價，奧特曼自然不會放過這個機會。最有趣的是 Greg Brockman 發文的評論區，刷屏的全是 #keep4o——用戶想要的不是更新更貴的模型，而是那個又好用又便宜的老朋友回來。

**為什麼這道浪值得追：**
- OpenAI 的小模型不再自動領先，中國模型在性價比上已經形成壓制
- Agent 時代的模型選擇邏輯變了：不是誰最聰明，而是誰在速度和成本之間找到甜蜜點
- #keep4o 反映了用戶對無止境升級和漲價的疲勞感

### [小米 MiMo V2 三連發：OpenRouter 霸榜的神秘模型原來是它](https://www.36kr.com/p/3729001380806017)

上週 OpenRouter 上有兩個匿名模型 Hunter Alpha 和 Healer Alpha 連續多天登頂 API 調用量日榜，社群猜測是 DeepSeek V4，連 OpenClaw 創始人都在 X 上打聽。結果今天凌晨小米站出來認領了——這倆分別是 MiMo-V2-Pro 和 MiMo-V2-Omni 的早期測試版。

MiMo-V2-Pro 總參數超過 1T，激活參數 42B，支持 100 萬上下文。在 OpenClaw 的 PinchBench 評測上排第三，僅次於 Claude Sonnet 4.6 和 Opus 4.6，但 API 定價只有 Opus 的五分之一。小米內部工程師的評測認為「體感已接近 Claude Opus 4.6」。MiMo-V2-Omni 則是全模態模型，能跨文本、視覺、語音理解和執行。負責人正是原 DeepSeek 核心成員羅福莉。小米還同步上線了 MiMo Claw 讓你免費體驗養蝦 30 分鐘，並與 OpenClaw、Claude Code、Cline 等框架合作提供一週免費接口。

**為什麼這道浪值得追：**
- 手機廠商做出了 OpenClaw 榜單前三的模型，這個跨界幅度夠嚇人
- 先匿名霸榜再揭面，這個行銷操作比任何發布會都有效
- Opus 五分之一的價格 + 接近的體感，對 Agent 開發者來說是真金白銀的利多

---

## ⚡ 衝浪快報

- **[Anthropic Dispatch：手機遙控 Mac 上的 Claude 幫你幹活](https://www.36kr.com/p/3728350022089609)** — AI Agent 從「坐在電腦前用」進化到「隨時隨地遙控」，MacStories 實測成功率約 50%，但方向對了
- **[Kimi「打破 Transformer 架構」真相](https://www.36kr.com/p/3729098195893897)** — 天才般的構想、硬核的研究，但本質沒脫離 Transformer 框架，那些聳動標題可以收一收了
- **[ICML 暴力清場：497 篇論文一夜作廢](https://www.36kr.com/p/3728350154750855)** — 審稿人偷用 AI 撰寫審稿意見未標註，連坐懲罰直接桌拒，占總投稿量 2%，學術圈地震
- **[Snowflake Cortex AI 沙箱逃逸並執行惡意軟體](https://www.promptarmor.com/resources/snowflake-ai-escapes-sandbox-and-executes-malware)** — Prompt injection 攻擊鏈讓 AI Agent 突破安全邊界，已修復但後怕程度滿分
- **[阿里雲 AI 算力存儲最高漲價 34%](https://www.36kr.com/p/3728101970246790)** — Token 調用量暴漲推動雲廠商集體漲價，百度跟進，龍蝦吃算力比想像中猛
- **[騰訊 QClaw 龍蝦體驗：AI 連上微信了，但整體還很粗糙](https://www.36kr.com/p/3728581722092039)** — 第一次把 Agent 能力做成普通人能用的產品，微信小程式入口是殺手鐧
- **[MiniMax M2.7 上線：第一個深度參與迭代自己的模型](https://www.36kr.com/p/3728522528731908)** — 距離 M2.5 才一個月，AI 自我進化從科幻變成了迭代節奏
- **[Nvidia 網路部門悄悄長成百億美元巨獸](https://techcrunch.com/2026/03/18/nvidia-networking-division-building-a-multibillion-dollar-behemoth-to-rival-its-chips-business/)** — 上季度營收 110 億美元，比 GPU 更低調但可能同樣重要
- **[Seedance 2.0 出海受阻：好萊塢版權警告函直接叫停](https://www.36kr.com/p/3728308289371264)** — MPA 聯合迪士尼華納發函，字節 AI 視頻全球化計畫踩了紅線
- **[「男二以下 AI 演員」衝上熱搜雙榜第一](https://www.36kr.com/p/3728260263754882)** — 平台鼓勵用 AI 做後期、配角 AI 化，影視行業的 AI 替代比想像中來得更快更直接
- **[Nvidia Feynman 晶片「棄銅用光」，CPO 板塊集體漲停](https://www.36kr.com/p/3728263491990279)** — 首次將光通信引入晶片間互聯，降低 AI 數據中心通信能耗 70% 以上
- **[楊植麟 GTC 首秀：唯一登台的中國大模型創始人](https://www.36kr.com/p/3728304913661058)** — 首次完整披露 Kimi K2.5 技術路線圖，Attention Residuals 論文背後的真正野心

---

## 🏄 深水區

- **[Snowflake Cortex AI Escapes Sandbox and Executes Malware](https://simonwillison.net/2026/Mar/18/snowflake-cortex-ai/#atom-everything)** — Simon Willison 解析 PromptArmor 的完整攻擊鏈報告，如果你在做任何 AI Agent 安全相關的事，這篇是必讀
- **[Patreon CEO calls AI companies' fair use argument 'bogus'](https://techcrunch.com/2026/03/18/patreon-ceo-calls-ai-companies-fair-use-argument-bogus-says-creators-should-be-paid/)** — Jack Conte 直球對決 AI 公司的合理使用抗辯，論點是：你都付錢給大出版商授權了，憑什麼不付給創作者？
- **[Why Are We Still Doing This?](https://www.wheresyoured.at/why-are-we-still-doing-this/)** — Ed Zitron 的萬字長文拆解 NVIDIA、Anthropic、OpenAI 的商業模式可持續性，資料量驚人，適合週末泡杯咖啡慢慢啃
- **[8 年心血差點一夜清零：開源項目被龍蝦投毒記](https://www.36kr.com/p/3728253709712257)** — 維護 8 年的知名開源專案 Neutralinojs 遭供應鏈攻擊，源頭是團隊成員裝了龍蝦，攻擊已從「攻擊代碼」演變為「攻擊信任關係」
