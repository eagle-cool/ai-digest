---
title: "Anthropic DMCA 誤殺八千 repo、Qwen 鎖上閉源大門、百度百台無人車趴窩"
date: 2026-04-02
description: "Anthropic 為了封殺外洩的 Claude Code 原始碼，DMCA 一口氣砍了 8100 個 GitHub repo 結果誤殺一片；阿里 Qwen3.5-Omni 全面閉源，開源生態的蜜月期走到盡頭；百度在武漢上百台無人計程車同時當機，乘客被困環線。"
tags: [llm, ai-tools, ai-industry, agents]
---

今天 AI 圈的浪型很詭異——Anthropic 為了收拾昨天 Claude Code 原始碼外洩的殘局，DMCA 直接砍了 8100 個 GitHub repo，結果連自家的合法 fork 都被誤殺，搞到開發者群情激憤後又緊急撤回。阿里那邊更安靜但更深遠：Qwen3.5-Omni 三個版本全部閉源，開源生態的蜜月期正式劃下句點。而最戲劇性的是百度，武漢上百台蘿蔔快跑無人計程車同時趴窩在馬路上，交警說「我們今天救了很多人」。三件事擺在一起，你會看到 AI 產業正在經歷的三種痛：控制權的失守、商業化的轉向、和現實世界的打臉。

---

## 🌊 今日浪頭

### [Anthropic took down thousands of GitHub repos trying to yank its leaked source code](https://techcrunch.com/2026/04/01/anthropic-took-down-thousands-of-github-repos-trying-to-yank-its-leaked-source-code-a-move-the-company-says-was-an-accident/)

Claude Code 原始碼外洩的後續比外洩本身還精彩。Anthropic 向 GitHub 發出 DMCA 下架通知，一口氣要求移除約 8100 個 repository——問題是，這些 repo 裡面有大量是 Anthropic 自己公開發布的 Claude Code 官方 repo 的合法 fork。開發者們一覺醒來發現自己的專案被砍，X 上瞬間炸鍋。Claude Code 負責人 Boris Cherny 出面承認「失誤」，表示下架通知因為 fork network 的連鎖效應波及了遠超預期的數量，隨後緊急縮小範圍到 1 個 repo 加 96 個含外洩原始碼的 fork。GitHub 已恢復其餘被誤殺的 repo。

但真正耐人尋味的是另一件事：開發者們在那 51 萬行原始碼深處挖出了一個叫 KAIROS 的內部系統，Karpathy 直接斷言這就是 Anthropic 正在全力推進的原生 Agent 框架——也就是 Claude 自己的「龍虾」。加上疑似下一代旗艦模型 Mythos 的 benchmark 跑分也跟著外洩，Anthropic 這週可以說是把家底都晾在了陽光下。對一家正在籌備 IPO 的公司來說，這個時間點不能更尷尬了。

**為什麼這道浪值得追：**
- DMCA 誤殺事件暴露了大規模版權執法的技術困境——fork network 讓你不可能精準打擊，一刀切下去必然誤傷
- KAIROS 的曝光等於讓全世界看到 Anthropic 的 Agent 戰略藍圖，競爭對手拿到了免費的技術情報
- 一週內連續兩次重大外洩加一次 DMCA 失誤，對「最重視安全的 AI 公司」這個品牌形象的傷害是持久性的

### [阿里雲越賺錢，開源生態越危險](https://www.36kr.com/p/3747973772227080)

阿里 3 月 30 日發布了 Qwen3.5-Omni——能同時處理文本、圖像、音訊和影片的多模態模型，支援 113 種語言的語音辨識，多項音訊理解基準超過 Google Gemini 3.1 Pro。技術上很猛，但真正的重點是：Plus、Flash、Light 三個版本全部只能透過 API 呼叫，沒有權重下載，沒有本地部署，沒有 Apache 2.0。上一代 Qwen3-Omni 去年 12 月發布時還是開源的。

這件事不能單獨看。3 月 3 日，Qwen 團隊技術負責人林俊旸離職——他是阿里最年輕的 P10，也是 Qwen 開源生態的靈魂人物。3 月 16 日，ATH（Alibaba Token Hub）事業群正式成立，與電商、雲智能平級，吳泳銘親自帶隊，五條 AI 業務線全部指向同一個方向：token 的生產、分發和變現。半個月後，Qwen3.5-Omni 發布，純閉源。

背後的算術很殘酷：阿里過去四季累計資本開支約 1200 億人民幣，外賣補貼戰和 AI 軍備競賽把現金流吃得乾乾淨淨。當 MaaS（模型即服務）正在成為雲業務最大的收入產品，每開源一個前沿模型，就等於在主動縮小自己的付費市場。開源是信仰，但現在是算術問題。

**為什麼這道浪值得追：**
- 阿里不會停掉開源，但多模態前沿能力——也就是最有商業價值的方向——正在被系統性地鎖進 API 付費牆
- 百煉平台 token 消耗量三個月增長 6 倍，但這增長本身就是過去兩年開源策略的成果，閉源可能反噬
- 這不是阿里獨有的困境：任何以雲收入為生命線的公司，當模型 API 變成最賺錢的產品，都會走到同一個路口

### [Baidu's robotaxis froze in traffic, creating chaos](https://www.theverge.com/ai-artificial-intelligence/905012/baidu-apollo-robotaxi-freeze-china)

3 月 31 日晚間，武漢二環線楊泗港長江大橋附近，上百台百度蘿蔔快跑無人計程車突然同時停擺。車輛閃著雙閃燈停在快車道上動彈不得，乘客被困車內，交警趕到現場手動開門救人。一位現場交警的說法很直白：「蘿蔔快跑系統出故障了，有百八十台。乘客按按鈕車門可以開，但人在環線上下不來。我們今天救了很多人。」

武漢是百度最大的無人計程車營運城市，部署超過 500 台無人車。警方初步認定為「系統故障」，但具體原因還在調查中。Reuters 引述當地新聞報導稱至少 100 台車受影響，其中有人因為緊急變道避開停擺車輛而發生了至少一起交通事故。

這讓人想起幾個月前 Waymo 在美國也發生過的大規模停擺事件。自動駕駛系統在正常情況下運作良好，但一旦遭遇全局性系統故障，所有車輛同時失控的場景比人類駕駛的個別車輛故障要危險得多——因為它是同步的、大規模的、且目前沒有有效的 fallback 機制。

**為什麼這道浪值得追：**
- 百度已在全球 26 個城市部署無人計程車，還跟 Uber 合作進了倫敦和杜拜，這次事故的影響不只在武漢
- 自動駕駛的「長尾問題」再次被證明：不是單車的 edge case，而是整個車隊的系統性風險
- 中國是全球最積極推動自動駕駶的市場之一，這次事故勢必影響監管態度和公眾信心

---

## ⚡ 衝浪快報

- **[Oracle 凌晨 6 點群發裁員信，3 萬人一鍵被辭退](https://www.36kr.com/p/3748150315680521)** — 沒面談、沒預警、沒電話，甲骨文用一封凌晨群發的 email 裁掉了約 18% 的全球員工。26 年資歷的老員工直言「噁心且懦弱」，但這就是 AI 時代大公司「減員增效」的殘酷樣板
- **[微軟股價單季暴跌 23%，2008 年以來最慘](https://www.36kr.com/p/3747926498591237)** — 押注 AI 最重的科技巨頭，在 AI 最火的時代裡交出最差的成績單。核心數字很刺眼：只有 3.3% 的 Microsoft 365 用戶真正為 Copilot 付了錢
- **[TRAE SOLO 獨立成產品，字節正式上了 Agent 牌桌](https://www.36kr.com/p/3747994426897156)** — 字節把 TRAE SOLO 從 IDE 裡拆出來，升級成獨立的執行型 Agent 工具，TRAE 管協作，SOLO 管執行，「龍蝦化」的方向很明確
- **[智谱、MiniMax 上市後首份財報：燒得越猛，市值越高](https://www.36kr.com/p/3747738485015044)** — 智谱 API 營收年增 296%，漲價 83% 後調用量反增 400%，打破了大模型只能打價格戰的共識。MiniMax 則靠海外 C 端走出另一條路
- **[Elgato Stream Deck 加入 MCP 支援，讓 AI 幫你按按鈕](https://www.theverge.com/tech/905021/elgato-stream-deck-mcp-ai-agent-update)** — Stream Deck 7.4 更新引入 Model Context Protocol 支援，Claude 等 AI 助手現在可以直接操控你的實體按鈕面板，MCP 的觸角又延伸了一步
- **[Linux 核心維護者困惑：AI bug 報告一個月內突然變靠譜了](https://www.36kr.com/p/3748150234989061)** — Greg Kroah-Hartman 在 KubeCon 上說「大概一個月前，像是有什麼東西變了」，但沒人知道是哪個模型或工具造成的，挺詭異的
- **[Cognichip 拿下 6000 萬美元，要用 AI 設計 AI 晶片](https://techcrunch.com/2026/04/01/cognichip-wants-ai-to-design-the-chips-that-power-ai-and-just-raised-60m-to-try/)** — 號稱能把晶片設計成本壓低 75%、時程縮短一半，聽起來很瘋但投資人買單了
- **[Holo3：電腦操控 AI 的新突破](https://huggingface.co/blog/Hcompany/holo3)** — H Company 在 Hugging Face 發布 Holo3 模型，主打 Computer Use 場景，跨平台操控電腦的 AI Agent 競賽又多了一個選手
- **[Anthropic 疑似下代旗艦模型 Mythos benchmark 外洩](https://www.36kr.com/p/3748834123448840)** — 一週內第二次外洩，Mythos 被定位為獨立產品線，不在 Claude 4.x/5 序列中，benchmark 跑分暗示性能跨代提升
- **[比全球最強推理引擎還快 2 倍，斯坦福破解大模型「串行魔咒」](https://www.36kr.com/p/3747805945824004)** — SSD 框架實現了推測解碼中 draft 和 verify 的並行化，在 Llama3-70B 上比 vLLM 快了 2.1 倍，這對推理成本的影響是結構性的

---

## 🏄 深水區

- **[The Subprime AI Crisis Is Here](https://www.wheresyoured.at/the-subprime-ai-crisis-is-here/)** — Ed Zitron 又一篇萬字長文，這次的論點是 AI 產業正在經歷一場「次貸危機」——估值建立在永遠不會兌現的營收預期上，而大公司為了維持敘事不得不持續加碼。不管你同不同意結論，裡面對 NVIDIA 財務數據的拆解值得細看
- **[Anthropic 首席產品官萬字分享：AI 時代的「現象級產品」為什麼難產？](https://www.36kr.com/p/3748204044092165)** — Instagram 聯合創始人 Mike Krieger 用 Claude 花兩小時重建了他當年花一整年做的產品，但他的核心問題是：Vibe Coding 帶來的效率狂飆，反而讓開發者離用戶更遠了
- **[Closed Source AI = Neofeudalism](https://geohot.github.io//blog/jekyll/update/2026/03/31/free-intelligence.html)** — geohot 的新文章，論點很尖銳：閉源 AI 本質上是一種新封建主義，智慧被集中在少數公司手中，而開源是唯一的解藥。搭配今天阿里 Qwen 閉源的新聞一起讀，味道更濃
- **[Karpathy：當 AI 接管 80% 代碼，我看清了 AGI 魔法](https://www.36kr.com/p/3747726516601353)** — 去年 11 月他的工作流還是 80% 手寫 20% AI，幾週後比例完全反轉。「最熱門的新程式語言是英語」——這句話從一個前 Tesla AI 負責人嘴裡說出來，份量不一樣
