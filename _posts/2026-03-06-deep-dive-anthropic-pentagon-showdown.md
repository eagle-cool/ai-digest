---
title: "當 AI 安全撞上國家安全：Anthropic 與五角大廈的終極攤牌"
date: 2026-03-06
description: "Anthropic 因拒絕讓軍方將 Claude 用於大規模監控和全自動武器，被五角大廈史無前例地列為「供應鏈風險」。這場對決揭露了 AI 治理的根本矛盾——當打造最安全 AI 的公司被國家安全體系視為威脅，整個產業的遊戲規則正在被改寫。"
tags: [deep-dive, ai-industry, ai-safety, agents]
---

## 引言

2026 年 3 月 1 日凌晨，美軍對伊朗發動了一場精準打擊，最高領袖哈梅內伊在空襲中喪生。事後多家媒體證實，這場行動的情報分析、目標識別和作戰模擬，大量依賴 Anthropic 的 AI 模型 Claude——安裝在 Palantir 的 Maven Smart System 中，被中央司令部用於即時戰場決策。

諷刺的是，就在空襲發生的幾個小時前，美國總統川普才剛在 Truth Social 上宣布：聯邦政府將全面停用 Anthropic 的技術。國防部長乘勝追擊，宣布將 Anthropic 列為「供應鏈風險」——一個過去只用在華為、中興、卡巴斯基這類外國實體上的標籤，第一次被貼在一家美國公司身上。

一邊用 Claude 殺敵，一邊宣布 Claude 是國安威脅。這個場景荒誕到像是某部反烏托邦電影的劇本，但它真實發生了。而這個故事的核心問題比任何電影都沉重：**當一家 AI 公司說「我們不願意讓你用我們的技術監控自己的人民、不願意讓你用它造全自動殺人機器」，政府的回應是試圖摧毀這家公司——這意味著什麼？**

這篇報導的起點是 [The Verge 的報導](https://www.theverge.com/ai-artificial-intelligence/886082/ai-vs-the-pentagon-killer-robots-mass-surveillance-and-red-lines)和 [TechCrunch 的追蹤](https://techcrunch.com/2026/03/05/its-official-the-pentagon-has-labeled-anthropic-a-supply-chain-risk/)，但故事遠不止於此。這是 AI 治理的第一場真正考驗，而壞消息是——所有人都輸了。

---

## 事件全貌

### 從合作到破裂的八個月

故事要從 2025 年 7 月說起。當時 Anthropic 與美國國防部簽署了一份最高金額 2 億美元的合同，Claude 成為第一個被允許在五角大廈機密網路中運行的前沿 AI 模型。合同的一個關鍵條款是：五角大廈同意遵守 Anthropic 的可接受使用政策（AUP），明確禁止將 Claude 用於大規模國內監控和無人類監督的全自動致命武器。

這份合同運作了整整十八個月，沒有出過任何問題。Claude 被部署到美國中央司令部等全球各地的指揮機構，用於情報評估、目標識別和作戰模擬。喬治城大學安全與新興技術中心高級研究分析師 Lauren Kahn 評價：「這是一項非常好的能力。」

然而到了 2026 年初，五角大廈開始要求重新談判條款。新任國防部長 Pete Hegseth 堅持 Anthropic 必須允許軍方「為所有合法目的」（for all lawful purposes）無限制地使用 Claude。具體來說，五角大廈想要做的事情包括：用 Claude 分析從美國民眾那裡收集的海量數據——[據《華爾街日報》報導](https://www.wsj.com/politics/national-security/pentagon-formally-labels-anthropic-supply-chain-risk-escalating-conflict-ebdf0523)，這些數據涵蓋用戶向聊天機器人提過的問題、Google 搜索記錄、GPS 定位軌跡、甚至信用卡交易明細，並與其他生活細節進行交叉比對。

Anthropic 的立場很清楚：**這就是大規模監控，我們不幹。**

### 最後通牒與破裂

2 月 26 日，Hegseth 在五角大廈與 Amodei 會面，給出最後期限：週五（2 月 28 日）下午 5:01 前同意條件，否則後果自負。五角大廈在當週三晚間發出了「最終報價」（last and final offer）。

據報導，五角大廈確實做出了一些讓步——同意刪除先前「視具體情況而定」等模糊限定語。但 Anthropic 發現，五角大廈仍然堅持要用 Claude 來分析美國公民的數據。[CNN 報導](https://edition.cnn.com/2026/02/26/tech/anthropic-rejects-pentagon-offer)引述 Anthropic 的立場：「我們無法在良心上同意他們的要求。」

談判破裂後的 48 小時內，事態以驚人的速度升級：

- **2 月 28 日（週五）**：川普在 Truth Social 發文，指示所有聯邦機構在六個月內停用 Anthropic 技術，稱其為「極左翼、覺醒公司」（RADICAL LEFT, WOKE COMPANY）。Hegseth 隨即宣布將 Anthropic 列為供應鏈風險。
- **同一天**：OpenAI 迅速與五角大廈簽署新合同，取代 Anthropic。
- **3 月 1 日（週六）**：美軍使用 Claude 驅動的情報系統對伊朗發動空襲。
- **3 月 5 日**：五角大廈正式通知 Anthropic 管理層，供應鏈風險認定即刻生效。Anthropic CEO Dario Amodei [發表聲明](https://www.anthropic.com/news/where-stand-department-war)，宣布將在法庭上挑戰這一決定。

### 「供應鏈風險」到底意味著什麼？

這個標籤的威力遠超一般的合同取消。根據美國法典第 10 編第 3252 條，被列為供應鏈風險的實體，所有與五角大廈有業務往來的承包商都必須證明自己沒有使用該實體的產品。Hegseth 更進一步宣稱，任何與 Anthropic 有「任何商業活動」的公司——即使是五角大廈合同以外的業務——都將被取消國防合同。

如果這個解讀成立，它的殺傷力是核彈級的。Amazon、Google、Nvidia——這些投資了 Anthropic 數十億美元的科技巨頭，同時也是國防承包商——可能被迫切斷與 Anthropic 的所有關係。這不是取消一個 2 億美元的合同，這是試圖從商業生態系統中徹底抹殺一家估值 3800 億美元的公司。

---

## 脈絡

### 矽谷與軍方的愛恨糾葛

科技公司與美國軍方的關係，從來就不是一帆風順。2018 年的 [Project Maven](https://www.nytimes.com/2018/06/01/technology/google-pentagon-project-maven.html) 是一個轉折點——Google 員工集體抗議公司為五角大廈開發無人機影像辨識技術，最終迫使 Google 退出該項目並發布 AI 倫理原則。那場抗議樹立了一個先例：科技公司的員工可以對軍事應用說「不」。

但時移勢易。2024 年，OpenAI 悄悄修改了使用政策，[刪除了明確禁止軍事和戰爭應用的條款](https://theintercept.com/2024/01/12/open-ai-military-ban-chatgpt/)。同年，Anthropic 與五角大廈簽下合同，但附帶了嚴格的使用限制。兩家公司走向了截然不同的道路。

這個分歧反映了 AI 安全領域的一條根本裂痕。Anthropic 由前 OpenAI 高管創立，從第一天起就把 AI 安全作為核心使命。他們的邏輯是：與其完全迴避軍方，不如參與合作但劃出紅線——不做大規模監控、不做全自動殺人武器。這個「有原則的參與」策略，在十八個月內運作良好。

### 政治氣候的轉變

然而，2026 年的華盛頓與 2025 年已經不是同一個世界。川普政府對科技公司的態度越來越像是一場忠誠度測試。[據 The Information 報導](https://www.theinformation.com/briefings/anthropic-ceo-says-refusal-praise-donate-trump-contributed-pentagon-conflict)，Amodei 私下表示，他拒絕公開讚揚或捐款給川普，是導致五角大廈態度轉硬的原因之一。

對照之下，OpenAI 總裁 Greg Brockman 向 MAGA Inc. 超級政治行動委員會[捐了 2500 萬美元](https://www.wired.com/story/openai-president-greg-brockman-political-donations-trump-humanity/)。在五角大廈宣布封殺 Anthropic 的同一天，OpenAI 就簽下了替代合同。時機之巧合，令人側目。

### 「供應鏈風險」條款的真正用途

這個法律工具從來不是為了懲罰國內公司而設計的。[Lawfare 的法律分析](https://www.lawfaremedia.org/article/pentagon's-anthropic-designation-won't-survive-first-contact-with-legal-system)指出，美國法典第 10 編第 3252 條定義的供應鏈風險，是指「一個敵對者」（an adversary）可能「破壞、惡意引入不需要的功能、或以其他方式顛覆」系統的風險。關鍵詞是「敵對者」——這個詞指向的是懷有敵意的實體，而不是合同糾紛中的供應商。

立法歷史也支持這個狹義解讀。參議院軍事委員會的報告將這個條款定位為應對「IT 供應鏈全球化」帶來的外國威脅，目標對象是華為、中興和卡巴斯基這樣的公司。一家拒絕在合同條款上讓步的美國公司，完全不在立法者的想像範圍內。

---

## 多方觀點

### 保守派的反彈：「這是企業謀殺」

最出人意料的聲音來自共和黨內部。Dean Ball 是右翼智庫美國創新基金會的高級研究員，2025 年曾幫助撰寫川普政府的 AI 行動計畫。換句話說，他是川普的人。

但他對五角大廈的做法[用了最嚴厲的措辭](https://www.persuasion.community/p/how-a-republic-ends)。他稱之為「企業謀殺的企圖」（attempted corporate murder），並在一篇標題為〈共和國如何終結〉的文章中寫道，美國「正在臨終病房裡」。他的核心論點是：供應鏈風險標籤不是取消一個合同，而是禁止其他公司與 Anthropic 做生意——這打擊的是私有財產權，一個傳統上對保守派格外神聖的原則。

[Ball 在 Gizmodo 的訪問中](https://gizmodo.com/corporate-murder-even-trumps-former-ai-advisor-thinks-the-pentagons-fight-against-anthropic-is-bad-2000729506)更直接地指出了荒謬之處：中國的 AI 供應商（如 DeepSeek）沒有面臨任何類似限制，而一家拒絕做政府生意的美國公司反而被打成供應鏈風險。他甚至說出了一句讓人震驚的話：「我不可能向任何投資者推薦投資美國 AI，也不可能推薦在美國創辦 AI 公司。」

一個幫川普寫 AI 政策的人，公開說不推薦在美國做 AI——這本身就是一個時代的註腳。

### 科技業的團結與裂痕

這場危機激發了罕見的跨公司團結。一封題為「我們不會被分裂」（We Will Not Be Divided）的公開信，在短短幾天內收到了[近 900 個簽名](https://techcrunch.com/2026/02/27/employees-at-google-and-openai-support-anthropics-pentagon-stand-in-open-letter/)——包括近 800 名 Google 員工和約 100 名 OpenAI 員工。信中呼籲各公司「擱置分歧、團結一致」，拒絕讓 AI 被用於大規模國內監控和「無人類監督的自動殺人」。他們看穿了五角大廈的分化策略：「他們試圖用恐懼來分裂每家公司，讓你擔心對方會屈服。」

但團結之下是深刻的裂痕。OpenAI 在 Anthropic 被封殺的同一天火速簽下了替代合同，允許軍方「為所有合法目的」使用其技術。CEO Sam Altman 事後承認這個時機「看起來很投機、很草率」（[looked opportunistic and sloppy](https://www.cnbc.com/2026/03/03/openai-sam-altman-pentagon-deal-amended-surveillance-limits.html)），並表示公司正在重新談判條款。

OpenAI 員工 Leo Gao——一位負責 AI 對齊研究的工程師——公開批評自家公司，稱 Altman 在合同中加入的所謂「安全防護」不過是「窗戶裝飾」（window dressing）。Altman 告訴員工「軍方的作戰決策由政府負責」，這句話讓許多人更加不安——它本質上是在說：「我們提供技術，怎麼用不關我們的事。」

### Anthropic 的內傷

Anthropic 自己也不是完全乾淨。Amodei 在一封內部備忘錄中稱 OpenAI 的軍方合約是「安全劇場」（safety theater），並將 Altman 的公開聲明描述為「徹頭徹尾的謊言」和「洗腦」（gaslighting）。這封備忘錄的洩漏，據報導直接破壞了正在進行中的談判。

[Amodei 事後道歉](https://www.anthropic.com/news/where-stand-department-war)，說那封備忘錄寫於「公司非常困難的一天」，「幾個小時內」一連串壞消息接踵而來，他的措辭「不代表深思熟慮後的觀點」。但傷害已經造成——它把一場原則之爭變成了一場人身攻擊，給五角大廈提供了升級衝突的藉口。

[Fortune 的分析](https://fortune.com/2026/03/05/anthropic-openai-feud-pentagon-dispute-ai-safety-dilemma-personalities/)一針見血地指出了更深層的問題：AI 安全目前完全依賴企業自律和競爭對手之間的自願承諾。但競爭壓力已經在侵蝕這些承諾——Anthropic 修改了自己的「負責任擴展政策」，刪除了在安全解決方案建立之前暫停模型開發的要求；OpenAI 在 2024 年就從政策中刪除了軍事應用禁令。當安全承諾取決於個別人格和企業競爭，而不是系統性的法規框架，這座大廈從一開始就建在沙地上。

### 我的看法

坦白說，我對這件事的情緒很複雜。

Anthropic 畫的那條線——不做大規模監控、不做全自動殺人武器——這不是什麼激進的要求。這是基本的道德底線。問題是，在目前的體制下，這條底線的存在完全取決於一家私人公司的意願。沒有法律保障、沒有監管框架、沒有獨立的第三方監督。Anthropic 今天願意堅持，但他們的董事會明天換人了呢？他們需要新一輪融資了呢？

而五角大廈的反應，只能用「以牙還牙」來形容。你不跟我做生意，我就讓所有人都不跟你做生意——這不是談判，這是恐嚇。用一個為外國威脅設計的法律工具來懲罰國內公司的合同糾紛，無論你怎麼包裝，都是權力的濫用。

但最讓我不安的，是 OpenAI 的角色。在競爭對手因為堅持原則而被打倒的同一天火速簽約，無論 Altman 怎麼事後補救，這個時間點本身就說明了一切。它傳達的信號是：在 AI 產業，你可以選擇做「對的事」，但你會因此被淘汰，而你的競爭對手會笑著接走你的合同。

---

## 產業衝擊

### 直接受影響者：風險計算被徹底改寫

最直接的衝擊是 Anthropic 自身的業務。表面上看，被取消的五角大廈合同只有 2 億美元，相對於 Anthropic 190 億美元的年化收入來說微不足道（約 1.4%）。但真正的風險在 Hegseth 那句「任何商業活動」。

Anthropic 80% 的收入來自企業客戶，超過 500 家客戶年支出超過 100 萬美元，包括財富 10 大中的 8 家。如果五角大廈真的執行最廣義的解讀——任何國防承包商都不能與 Anthropic 有任何商業往來——這將觸發一場大規模的客戶流失。正如 [Fortune 引述的分析師所言](https://fortune.com/2026/02/28/openai-pentagon-deal-anthropic-designated-supply-chain-risk-unprecedented-action-damage-its-growth/)：「每一家有五角大廈業務的財富 500 大公司的法務長，都會問同一個問題：使用 Claude 值得冒這個風險嗎？」

Anthropic 原本計畫在 2026 年底 IPO。這個供應鏈風險標籤和隨之而來的法律戰，為這個計畫蒙上了巨大的陰影。Amazon、Google、Nvidia 這些投資者是否可能被迫剝離持股，至今仍是懸而未決的問題。

### 商業模式衝擊：AI 安全變成了商業負債

這件事傳達了一個令人不寒而慄的信號：**在 AI 產業，堅持倫理原則可能成為商業負債。**

Anthropic 一直以「負責任的 AI」作為品牌核心——這也是它能吸引頂尖人才、獲得大筆投資的關鍵。但五角大廈的行動證明，這個品牌定位在政治壓力面前可能變成弱點。一家公司越是公開承諾「我們不會做 X」，它就越容易被政府用「你必須做 X」來打擊。

這對整個 AI 產業的商業模式設計有深遠影響。未來的 AI 公司會更傾向於模糊化自己的使用政策——不明確禁止什麼，就不會因為堅持禁令而被懲罰。OpenAI 的「為所有合法目的」語言就是這種策略的完美範本：把責任推給法律本身，不做任何超越法律最低要求的自我約束。

東北大學 AI 與數據策略副教務長 Usama Fayyad 說得直接：這已經開了一個「壞先例」，可能造成「重大的經濟、科學和工程損害」。

### 開發者生態：你寫的程式碼可能被用來殺人

對開發者來說，這場危機把一個一直被迴避的問題推到了檯面上：你為 AI 公司寫的程式碼，最終可能被用在你完全無法預料的場景中。

Claude 被用於伊朗軍事行動的消息，對 Anthropic 的開發團隊是一記重擊。即使公司設定了使用紅線，軍方在實戰中的應用範圍往往超出合同條款的界限——Claude 做的「情報評估」和「目標識別」，在實踐中就是幫助決定炸彈該落在哪裡。

OpenAI 和 Google 員工簽署的公開信，反映了一個正在成形的共識：AI 工程師不想成為「我只是照命令行事」的人。近 900 名科技工作者集體表態，[另一封公開信](https://techcrunch.com/2026/03/02/tech-workers-urge-dod-congress-to-withdraw-anthropic-label-as-a-supply-chain-risk/)更直接呼籲國防部撤回對 Anthropic 的標籤。但簽完信，第二天還是要回去上班。這種結構性的無力感，是這個時代 AI 工程師的集體困境。

### 二階效應：AI 治理真空的加速暴露

這場危機最深遠的影響，是暴露了 AI 治理的徹底真空。

目前，AI 的軍事應用沒有任何專門的聯邦法規。沒有法律規定 AI 系統在什麼情況下可以被用於戰場決策，沒有規定什麼構成「充分的人類監督」，沒有規定 AI 輔助的監控需要什麼層級的授權。一切都依賴企業自願政策和行政部門的內部規範——而正如我們所見，這些東西在政治壓力面前不堪一擊。

歐盟和其他地區的觀察者一定在看著這場鬧劇，暗自慶幸自己走了立法路線。EU AI Act 至少為「高風險」AI 應用設定了法律框架，即使執行面還有很多問題。美國模式——讓企業自律、讓市場自我調節——在這一刻被證明完全失靈。

更令人擔憂的是連鎖反應。如果美國政府可以用行政手段懲罰一家拒絕配合的 AI 公司，其他國家也會照辦。中國已經有了類似的機制。俄羅斯、沙烏地阿拉伯，任何有錢買 AI 的威權政府，都可以指著 Anthropic 的案例說：「看，美國自己也是這樣做的。」

---

## 未來展望

### 短期（3-6 個月）：法律戰與市場分化

幾乎確定會發生的事：

**法庭對決即將開打。** Anthropic 已明確表態將在聯邦法院挑戰供應鏈風險認定。[Lawfare 的法律分析](https://www.lawfaremedia.org/article/pentagon's-anthropic-designation-won't-survive-first-contact-with-legal-system)指出了多條法律攻擊路線：五角大廈超越了法定授權（ultra vires）、將「敵對者」條款套用在國內企業上缺乏法理基礎、Hegseth 和川普的公開言論暴露了政治動機而非安全考量。前 Trump AI 顧問 Dean Ball 也承認：「法院確實不太願意在國家安全問題上質疑政府……但這不是不可能的。」

此外，Lawfare 指出一個致命的邏輯矛盾：五角大廈在同一週內先援引《國防生產法》聲稱 Anthropic 的技術「不可或缺」，幾天後又宣稱「我們不需要它」——法院會特別關注這種前後不一。

**消費市場的反彈。** 有趣的反轉已經在發生——OpenAI 宣布五角大廈合約後，大量用戶在應用商店從 ChatGPT 轉向 Claude。Anthropic 的主應用 Claude 最近登上了蘋果應用商店下載排行榜榜首。「被國家打壓」正在變成一種品牌資產。

### 中期（6-18 個月）：三種可能的情境

**情境一：法院推翻認定，Anthropic 全身而退。** 如果法院認定五角大廈濫用了供應鏈風險條款，這將為 AI 公司設定重要的法律先例——政府不能用這個工具來懲罰合同糾紛。Anthropic 可能反而因為這場戰鬥獲得品牌加持，順利推進 IPO。但美國軍方的 AI 應用治理問題仍然懸而未決。

**情境二：雙方達成妥協，但條件更苛刻。** 目前的報導顯示，Amodei [仍在與五角大廈副部長 Emil Michael 進行談判](https://techcrunch.com/2026/03/05/anthropic-ceo-dario-amodei-could-still-be-trying-to-make-a-deal-with-pentagon/)。如果達成新協議，Anthropic 可能不得不接受更寬鬆的使用條款——或許保留對全自動武器的禁令，但在「監控」的定義上做出讓步。Amodei 已經在聲明中表示，Anthropic 將繼續以「象徵性費用」為軍方提供 Claude 支援，「只要過渡期需要」。

**情境三：持久法律戰，行業分裂加深。** 如果雙方都不讓步，這將演變為一場可能持續數年的訴訟。在此期間，AI 產業會進一步分化為「願意為政府做任何事」和「堅持設定紅線」兩個陣營。企業客戶將被迫選邊站。

### 長期推演：3-5 年後的世界

無論短期結果如何，這場危機標誌著一個轉折點：**AI 軍事應用的治理不能再依賴企業善意。**

立法壓力將會上升。議員們已經開始注意到——當一個為外國威脅設計的法律工具被用來對付本國公司時，這不只是一家公司的問題，而是法治的問題。在未來幾年，我們很可能看到專門針對 AI 軍事應用的立法提案，就像歐盟的 AI Act 一樣，試圖為「什麼可以用 AI 做、什麼不可以」劃出法律紅線。

國際層面，這場事件加速了「AI 軍事倫理」成為全球議題的進程。如果美國都做不到在 AI 軍事應用上保持原則性的自我約束，國際社會對 AI 武器控制條約的需求只會更加迫切。

### 給讀者的行動建議

**如果你是開發者：** 認真思考你在哪裡工作、你的程式碼最終會被用在哪裡。這不是說你不能為 AI 公司工作，而是說你需要了解你的雇主在軍事應用上的立場——並且接受這個立場隨時可能改變的現實。關注你所使用的 AI 框架的使用條款變化，它們正在變得越來越模糊。

**如果你是創業者或產品經理：** 如果你的產品依賴特定的 AI 模型供應商，這場危機應該讓你認真考慮多模型策略。今天是 Anthropic 被封殺，明天可能是任何一家公司。另外，你的 AI 使用政策不能只是法務部門的一份文件——它可能成為你最大的商業資產或最大的商業風險。

**如果你是一般科技從業者：** 持續關注這場法律戰的進展。它的結果將定義未來十年科技公司與政府的關係。無論你是否直接受影響，這個先例一旦確立，「政府可以用行政手段懲罰不配合的科技公司」的模式就會被複製到 AI 以外的領域。

---

回到文章開頭的那個場景：美軍一邊用 Claude 策劃空襲，一邊宣布 Claude 是國安威脅。這個矛盾不會被解決，只會被某種政治交易所掩蓋。真正的問題不是 Anthropic 會不會贏得這場官司，而是：當 AI 變得足夠強大，強大到能左右戰爭勝負時，誰來決定它的紅線——是打造它的公司、部署它的軍方、還是根本沒有人？

這個問題，我們還沒有答案。但 Anthropic 事件告訴我們的是：**不回答這個問題的代價，已經開始顯現了。**

---

## 延伸閱讀

- [Pentagon's Anthropic Designation Won't Survive First Contact with Legal System — Lawfare](https://www.lawfaremedia.org/article/pentagon's-anthropic-designation-won't-survive-first-contact-with-legal-system)：最詳盡的法律分析，逐條拆解為什麼五角大廈的認定在法庭上站不住腳
- [How a Republic Ends — Dean Ball / Persuasion](https://www.persuasion.community/p/how-a-republic-ends)：川普前 AI 顧問的震撼長文，從保守派視角批判五角大廈的做法
- [The Anthropic-OpenAI Feud and Pentagon Dispute Expose a Deeper Problem — Fortune](https://fortune.com/2026/03/05/anthropic-openai-feud-pentagon-dispute-ai-safety-dilemma-personalities/)：深入分析 Anthropic-OpenAI 之間的人格衝突如何加劇了這場危機
- [OpenAI Sweeps In to Snag Pentagon Contract — Fortune](https://fortune.com/2026/02/28/openai-pentagon-deal-anthropic-designated-supply-chain-risk-unprecedented-action-damage-its-growth/)：OpenAI 取代 Anthropic 的商業與戰略分析
- [Pentagon Designates Anthropic a Supply Chain Risk — Mayer Brown](https://www.mayerbrown.com/en/insights/publications/2026/03/pentagon-designates-anthropic-a-supply-chain-risk-what-government-contractors-need-to-know)：頂尖律所為國防承包商撰寫的實務指南
- [Anthropic's Claude AI Being Used in Iran War — Washington Post](https://www.washingtonpost.com/technology/2026/03/04/anthropic-ai-iran-campaign/)：Claude 在伊朗軍事行動中扮演的角色的第一手報導
- [Employees at Google and OpenAI Support Anthropic's Pentagon Stand — TechCrunch](https://techcrunch.com/2026/02/27/employees-at-google-and-openai-support-anthropics-pentagon-stand-in-open-letter/)：科技業員工跨公司團結的公開信始末
- [Anthropic to Challenge DOD's Supply-Chain Label in Court — TechCrunch](https://techcrunch.com/2026/03/05/anthropic-to-challenge-dods-supply-chain-label-in-court/)：Amodei 宣布法律挑戰的完整報導
