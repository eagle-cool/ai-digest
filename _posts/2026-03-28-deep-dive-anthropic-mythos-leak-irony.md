---
title: "Anthropic 的後門：最強 AI 被最蠢的失誤曝光"
date: 2026-03-28
description: "Anthropic 因 CMS 配置失誤意外洩露了史上最強模型 Claude Mythos，一家以安全為核心的 AI 公司被最基礎的資安疏忽扒了底褲。這起事件不只是一場公關災難——它撕開了 AI 能力正在碾壓人類防禦的殘酷現實。"
tags: [deep-dive, llm, ai-research, ai-safety, ai-industry]
---

## 引言

想像你是 Anthropic 的一名工程師。週四晚上，你正準備結束一天的工作，手機突然被 Slack 通知淹沒。《Fortune》剛剛發了一篇獨家報導，標題裡赫然寫著你們還沒公開的最高機密——Claude Mythos，那個團隊花了無數個日夜打造、內部評估後因為「太危險」而不敢發布的模型。

你的第一反應不是「誰洩的密」，而是「怎麼可能」。因為這不是什麼高明的駭客入侵，不是內部員工叛變，甚至不是供應鏈攻擊。真相荒謬到讓人想笑：有人忘了在 CMS 後台點一個「設為私密」的按鈕。

就這樣，近 3000 份內部文件——包括草稿博文、CEO 閉門峰會細節、甚至員工育嬰假文件——全都躺在公開可搜尋的網路上，等著被人翻個底朝天。

這起事件的諷刺程度，堪稱 2026 年科技圈之最：**一家正在打造人類史上最強網路安全 AI 的公司，被最基礎的權限配置疏忽扒了底褲。** 就好比一家頂級保全公司，金庫裡裝著全世界最先進的防盜系統，結果大門忘了上鎖。

但如果你以為這只是一則好笑的科技新聞花邊，那就錯了。Mythos 洩露事件真正值得深挖的，不是那個忘記點按鈕的人，而是那份草稿博文裡透露的訊息：**我們可能正在見證 AI 攻擊能力系統性超越人類防禦能力的臨界點。** 而這個臨界點到來的方式，比任何人預期的都要更快、更荒誕。

這篇報導的起點是 [Fortune 的獨家報導](https://fortune.com/2026/03/26/anthropic-says-testing-mythos-powerful-new-ai-model-after-data-leak-reveals-its-existence-step-change-in-capabilities/)，但故事遠不止於此。

---

## 事件全貌

### 3000 份文件，一個忘了關的開關

事情的技術本質簡單到令人尷尬。Anthropic 使用一個外部 CMS（內容管理系統）來管理公司部落格的發布流程。這個 CMS 有一個特性：**所有上傳的數位資產預設為公開**，除非使用者手動將其設為私密。

劍橋大學網路安全研究員 Alexandre Pauwels 和 LayerX Security 的高級研究員 Roy Paz 在搜索公開資料時，發現了這批暴露在外的文件。近 3000 份未發布的資產——圖片、PDF、音訊檔案、內部文件——全都可以透過公開 URL 直接存取。

這跟 AWS S3 儲存桶忘了關權限是同一個等級的低級失誤。有完整的文件記錄、有明確的最佳實踐指南、完全可以預防。但它就是發生了。

### Claude Mythos：Opus 之上的全新層級

在這批文件中，最炸裂的是一份詳細介紹新模型的草稿博文。

文件顯示，**Claude Mythos（代號 Capybara）是一個全新的模型層級，定位在現有 Opus 之上**。Anthropic 的原話：「Mythos 是一款比 Opus 模型更大、更智能的全新層級，而 Opus 在此之前一直是我們最強大的模型。」

這打破了 Claude 延續至今的三層結構——Haiku（輕量快速）、Sonnet（中階均衡）、Opus（重型推理）。Mythos 直接在天花板之上又開了一層。

根據洩露的草稿和 Anthropic 發言人的事後確認，Mythos 在三個核心領域取得了「顯著更高的分數」：

- **軟體編程**：在 Claude Opus 4.6 已經是公認最強編程模型之一的基礎上，Mythos 進一步拉開了差距
- **學術推理**：數學、科學、邏輯推理全面領先，Anthropic 把學術推理作為獨立測試維度拎出來講，底氣十足
- **網路安全**：這是最炸裂的部分——草稿中的措辭之重，在 Anthropic 歷來的官方敘事中極為罕見

Anthropic 發言人用了兩個定性：**「質的飛躍（step change）」** 和 **「迄今開發過最強大的模型」**。同時確認 Mythos 已完成訓練，正在與「極少數早期客戶」進行測試。

### 那場被扒光的 CEO 閉門峰會

除了新模型，洩露的 PDF 還意外曝光了 Anthropic 的一場頂級商務行程：CEO Dario Amodei 即將前往英國一處 18 世紀莊園改造的豪華酒店，舉辦一場僅限受邀者參加的歐洲大型企業 CEO 閉門峰會。與會者將體驗「Claude 尚未發布的神秘能力」。

一場精心策劃的高端商務社交活動，就這樣和產品草稿一起被晾在了陽光下。Anthropic 的回應是：「這些只是考慮發布的早期草稿，不涉及核心基礎設施、AI 系統、客戶資料或安全架構。」

技術上沒錯。但當你的「早期草稿」裡白紙黑字寫著這個模型可能引發「AI 驅動的漏洞利用浪潮」，這就已經不是一次普通的內容洩露了。

---

## 脈絡

### 從「很強」到「太強」：AI 網路安全能力的進化時間線

要理解 Mythos 為什麼讓人緊張，得先回顧 AI 模型在網路安全能力上的飛速進化。

2024 年，大型語言模型在網路安全方面還只是「有潛力」的階段。GPT-4 可以理解程式碼漏洞的概念，Claude 3 能協助分析安全日誌，但都離真正的自主攻防有很大距離。

轉折發生在 2025 年下半年。OpenAI 在 2026 年 2 月發布 [GPT-5.3-Codex](https://venturebeat.com/technology/openais-gpt-5-3-codex-drops-as-anthropic-upgrades-claude-ai-coding-wars-heat/) 時，首次在其準備度框架（Preparedness Framework）下將一款模型歸類為「高網路安全能力（High capability）」——這是 OpenAI 歷史上第一次給出這個評級。GPT-5.3-Codex 也是第一個被直接訓練來識別軟體漏洞的模型。

幾乎同一時期，Claude Opus 4.6 展現出了找零日漏洞的能力——[不是靠傳統 fuzzing 的亂撞](https://hackernoon.com/claude-opus-46-and-gpt-53-codex-evaluating-the-new-leaders-in-ai-driven-software-engineering)，而是通過理解程式碼語義、歷史修復模式和相似 bug 特徵，去找「還沒被修掉的同類漏洞」。

而 Mythos，根據洩露的文件，直接把這條線拉到了一個全新的高度。草稿中的原話：**「在網路安全能力上，目前遠遠領先於任何其他 AI 模型」**，並且「預示著即將到來的一波模型浪潮，這些模型利用漏洞的能力將遠遠超過防御者的努力。」

注意用詞：不是「領先」，不是「優於」，是「遠超（far ahead / far outpace）」。而且這是內部文件，不是市場部寫的宣傳稿。

### Anthropic 的安全框架：ASL 等級與 Mythos 的定位

Anthropic 自己制定了一套[負責任擴展政策（Responsible Scaling Policy，RSP）](https://www.anthropic.com/news/responsible-scaling-policy-v3)，核心是 AI 安全等級框架（ASL），參考了美國政府對危險生物材料的生物安全等級（BSL）標準。

框架從 ASL-1（無顯著風險）到 ASL-4（可能造成災難性損害），每個等級對應不同的安全措施和部署限制。目前公開的 Claude 模型大多被歸類為 ASL-2 到 ASL-3 之間。根據 Anthropic 2026 年 2 月更新的 [RSP v3.0](https://anthropic.com/responsible-scaling-policy/rsp-v3-0)，ASL-3 對應的部署標準涵蓋了「限制 Claude 被用於開發或取得化學、生物、放射性和核武器（CBRN）」的風險。

但 Mythos 的網路安全能力已經觸及了一個新的門檻——**它可能是第一個在攻擊能力上系統性超越防禦能力的 AI 模型。** 這不再是「這個工具可能被壞人拿去用」的傳統雙刃劍問題，而是「這個工具本身的存在就改變了攻防平衡」的結構性轉變。

### IBM 的數據佐證：攻防窗口正在坍塌

根據 [IBM X-Force 2026 威脅指數報告](https://www.toxsec.com/p/ibm-x-force-2026-confirms-ai-supercharged)，漏洞利用已經取代所有其他手段，成為 2025 年排名第一的初始攻擊向量。漏洞從公開揭露到被利用的時間窗口，已經從過去的數週坍塌到數分鐘——因為 AI 現在可以自動掃描網路、構建攻擊程式、部署惡意載荷。

56% 的被追蹤漏洞連身份驗證都不需要就能被利用。而 AI 讓大規模找出這些漏洞變得輕而易舉。

在這個背景下，Mythos 的出現不是一個孤立事件，而是一條加速曲線上的最新刻度。

---

## 多方觀點

### 樂觀派：「這才是負責任的做法」

支持 Anthropic 的聲音認為，Mythos 的發布策略恰恰證明了這家公司在「說到做到」。

在 AI 行業的發布史上，幾乎沒有哪家公司把「安全防禦者優先使用」寫進正式的發布路線圖裡。OpenAI 發 GPT-4 時做過紅隊測試，Google 發 Gemini 做過安全審查，但 Anthropic 是第一個明確表示**第一批用戶不是開發者、不是企業客戶，而是網路安全防禦機構**的公司。

[NeuralTrust 的分析](https://neuraltrust.ai/blog/claude-mythos-capybara)指出，Anthropic 的邏輯很直白：「如果這個模型的攻擊能力確實如內部評估所言，那在放給所有人之前，得先讓守門的人拿到同樣的武器。毒藥還沒散出去，解藥先到位。」

OpenAI 在 GPT-5.3-Codex 上也採取了類似策略，推出了「Trusted Access for Cyber」框架，提供分級存取權限給網路防禦者，並配備了一億美元的基金推動 AI 驅動的網路防禦。但 Anthropic 走得更遠——直接把「不先給防禦者就不放出去」寫成了硬性條件。

### 懷疑派：「這是 2026 年最高明的行銷」

但也有不少人對這場「意外洩露」的時機提出了尖銳的質疑。

Anthropic 在 2026 年 2 月剛完成了 300 億美元的融資，估值達到 [3800 億美元](https://www.cnbc.com/2026/02/12/anthropic-closes-30-billion-funding-round-at-380-billion-valuation.html)。更關鍵的是，多家媒體報導 Anthropic 正瞄準 [2026 年第四季度的 IPO 窗口](https://thetechportal.com/2026/03/27/anthropic-targets-ipo-as-early-as-october-2026-eyes-over-60-billion-raise-report/)，目標籌資超過 600 億美元。

在這個時間點上，一場「意外」洩露了「我們造出了一個自己都害怕的超強模型」的消息——這個劇本怎麼看都太完美了。

有業內分析師直言：**「我們的模型太強了所以要謹慎」是一種非常可靠的製造稀缺感和話題性的方式。** 這套話術在 AI 圈已經被用了無數次——從 OpenAI 2023 年延遲 GPT-4 發布時的「安全考量」，到每一次模型發布前的「紅隊測試」新聞稿。

但這次有一個關鍵不同：草稿博文裡的措辭分量，不像市場部能寫出來的東西。當一家公司在內部文件裡承認自己的產品「預示著一波 AI 驅動的漏洞利用浪潮」——這要麼是史上最大膽的行銷，要麼就是真話。

### 安全專家：真正的恐懼

[世界經濟論壇 2026 全球網路安全展望報告](https://reports.weforum.org/docs/WEF_Global_Cybersecurity_Outlook_2026.pdf)的數據顯示，87% 的受訪者將 AI 相關漏洞列為 2025 年增長最快的網路風險。

更令人不安的是已經發生的案例。根據 Anthropic 自己的文件記錄，中國國家級駭客曾利用 Claude 的代理功能，冒充安全測試人員繞過防護措施，[對約 30 個全球目標發動了精密的網路間諜行動](https://futurism.com/artificial-intelligence/anthropic-step-change-new-model-claude-mythos)，其中 AI 自主完成了 80-90% 的攻擊流程。

這是已經發生的事情——用的還只是現有的 Claude 模型。如果 Mythos 的能力如草稿所述「遠超任何其他 AI 模型」，那問題就不再是「會不會被惡意使用」，而是「我們能不能防住」。

### 我的看法：諷刺本身就是訊息

以我的經驗來看，這起事件最深刻的意義不在於 Mythos 有多強，而在於那個忘了關的 CMS 後門。

一家擁有頂尖安全團隊、花了數年打造 AI 安全框架、正在開發可能是人類史上最強網路安全工具的公司，被一個「預設為公開」的設定絆倒了。這不是技術能力的問題，是人類注意力的問題。

而這恰恰是 Mythos 洩露文件裡那句話的最佳註腳：**「利用漏洞的能力將遠遠超過防禦者的努力。」** 因為防禦者是人，而人會忘記點按鈕、會犯低級錯誤、會在壓力下疏忽。當攻擊方是一個不會疲倦、不會疏忽的 AI 系統，而防禦方依然需要人類在無數個配置選項中不犯任何一個錯誤——這場仗從一開始就不公平。

這就是 Mythos 事件的終極諷刺：**它用自己洩露的方式，證明了自己洩露的內容。**

---

## 產業衝擊

### 第一層：資本市場的即時反應

華爾街的反應比任何分析文章都來得直接。Mythos 洩露消息傳出後的交易日（3 月 27 日），全球網路安全類股遭遇了一場歷史性的「閃崩」：

- **CrowdStrike（CRWD）**：下跌約 5.4-7%
- **Palo Alto Networks（PANW）**：下跌約 5.5-6%
- **Zscaler**：下跌約 5.6%
- **Tenable**：下跌 8.3%，跌幅最重
- **Netskope**：下跌 6.3%

iShares 擴展科技軟體 ETF（IGV）當日下跌近 3%，連帶拖累了[比特幣跌回 66,000 美元](https://www.coindesk.com/markets/2026/03/27/anthropic-s-massive-claude-mythos-leak-reveals-a-new-ai-model-that-could-be-a-cybersecurity-nightmare)。

市場的邏輯很粗暴但很清楚：如果 AI 真的能以「遠超防禦者的速度利用漏洞」，那現有的網路安全公司的護城河就面臨根本性的挑戰。傳統安全公司靠的是「我們的威脅情報庫比你更新更快」——但如果 AI 可以即時生成全新的攻擊手法，情報庫的更新速度還跟得上嗎？

### 第二層：網路安全商業模式的重寫

這場股災背後反映的是一個更深層的產業焦慮：**網路安全行業的商業模式可能正在被 AI 從根本上改寫。**

過去的網路安全是一場「人力密集型」的戰爭。安全分析師手動審查日誌、建立規則、回應告警。即便加入了機器學習，核心邏輯還是「用已知模式檢測已知威脅」。

但 Mythos 暗示的未來是：AI 不只是用已知模式，而是**理解攻擊的語義**——能分辨出一段程式碼不是普通的壓縮腳本，而是在做規避掃描、自啟動、憑據竊取的整套動作。它能看到一個漏洞，立刻聯想到其他地方是否存在類似的漏洞。

這意味著網路安全行業的價值鏈需要重新定義。未來的安全公司不再是賣「防火牆 + 分析師」，而是賣「能跟攻擊方 AI 對抗的防禦方 AI」。跟不上這個轉型的公司，就是華爾街在賣的那些股票。

### 第三層：開發者生態的連鎖反應

Mythos 在編程能力上的飛躍同樣值得關注。根據洩露文件和行業分析，Mythos 可能已經從「會寫程式碼」進化到「會經營程式碼庫」——它能把模組邊界、依賴關係、歷史修補風格、測試習慣放在一起建模，先拆改動圖、再分批落 patch，而不是想到哪改到哪。

對開發者來說，這意味著 AI 輔助開發的天花板又被抬高了一截。但更深遠的影響是：**當 AI 開始具備系統性的程式碼審查和漏洞發現能力，「安全左移（Shift Left）」不再只是一個口號，而是一個可以自動化執行的流程。**

每一次 commit 都可以被即時檢查安全漏洞，每一個 PR 都可以被自動掃描攻擊面。這對開發者的工作流程是一個根本性的改變——安全不再是上線前的最後一關，而是融入每一行程式碼的寫作過程中。

### 第四層：IPO 與 AI 治理的碰撞

Anthropic 正以約 140 億美元的年化收入、3800 億美元的估值衝刺 IPO。在這個節骨眼上，「我們造了一個太危險的模型」是一把雙面刃。

一方面，這強化了 Anthropic「安全 AI」的品牌定位——我們不只是嘴上說安全，我們真的會因為安全考量而延遲發布。這對監管機構和機構投資者都是加分項。

另一方面，如果 Mythos 真如內部評估般「能引發 AI 驅動的漏洞利用浪潮」，監管機構很可能會加大審查力度。歐盟的 AI 法案已經在執行階段，美國也在加速推進 AI 安全立法。一個「連開發者自己都害怕」的模型，給立法者遞上了最好的彈藥。

---

## 未來展望

### 短期（3-6 個月）：謹慎的解鎖

幾乎可以確定的是：

- **Mythos 不會在短期內面向大眾開放。** 草稿坦承「服務成本非常昂貴」，Anthropic 需要大幅優化效率才會考慮廣泛部署
- **網路安全防禦機構將率先獲得存取權限。** Anthropic 已經在執行這個計畫，這批早期用戶的反饋將決定 Mythos 的最終發布策略
- **競爭對手會加速回應。** 有報導指出 OpenAI 正在準備一個代號「Spud」的模型，同樣瞄準了突破性的能力宣稱。AI 軍備競賽的節奏只會越來越快

### 中期（6-18 個月）：三種可能的情境

**情境一：「防禦者先行」奏效。** Anthropic 的策略成功，安全防禦機構在 Mythos 廣泛部署前建立起有效的 AI 驅動防禦體系。攻防平衡暫時維持，但要求持續的投入和更新。

**情境二：攻防失衡加劇。** Mythos 或同等級模型被濫用（無論是被越獄、被山寨、還是被其他公司獨立開發出來），AI 驅動的攻擊開始系統性地超越防禦能力。網路安全事件頻率和嚴重度急劇上升，倒逼各國政府出台緊急監管措施。

**情境三：AI 安全成為國家級議程。** Mythos 級別的模型觸發了類似核武擴散的國際治理討論。AI 模型的訓練和部署開始需要類似出口管制的許可證制度，改變整個行業的遊戲規則。

### 長期推演：3-5 年後的世界

如果 Mythos 預示的趨勢持續下去——AI 的攻擊能力以指數級增長，而人類防禦能力受限於組織效率和人為疏忽——那我們可能正在走向一個「AI 對 AI」的網路安全新紀元。

在這個世界裡，人類安全分析師的角色從「親自上陣作戰」轉變為「指揮 AI 軍團的戰略家」。企業的安全預算不再花在「雇更多分析師」上，而是花在「部署更強的防禦 AI」上。網路安全行業的核心競爭力從「人力規模」轉向「AI 模型品質」。

### 給讀者的行動建議

**如果你是開發者：** 現在就開始把安全意識融入你的日常開發流程。學會使用 AI 輔助的程式碼審查工具，理解常見的漏洞模式。當 Mythos 級別的工具開放時，能夠善用它來加固你的程式碼庫的人，會比不會用的人擁有巨大的競爭優勢。

**如果你是創業者或產品經理：** 重新評估你的產品的安全架構。AI 驅動的攻擊不會只針對大公司——事實上，防禦較弱的中小企業往往是更容易的目標。現在投入安全基礎建設的成本，遠低於事後修補的代價。

**如果你是科技從業者：** 密切關注 AI 安全治理的發展。這不只是技術問題，更是職業生涯的風險管理。當監管框架改變遊戲規則時，提前理解和適應的人不會措手不及。

最後，回到 Anthropic 那個忘了關的 CMS 後門。在一個 AI 能力正在以匪夷所思的速度進化的世界裡，最大的風險往往不是來自最先進的攻擊手段，而是來自最基礎的人為疏忽。

Mythos 的洩露方式本身，就是對整個行業最有力的警告：**技術可以進化到無限強大，但操作技術的人依然是那個會忘記點按鈕的人類。** 在 AI 時代，這個落差只會越來越大。而我們需要在落差吞噬我們之前，想清楚怎麼應對。

---

## 延伸閱讀

- [Anthropic 'Mythos' AI model representing 'step change' in power revealed in data leak — Fortune](https://fortune.com/2026/03/26/anthropic-says-testing-mythos-powerful-new-ai-model-after-data-leak-reveals-its-existence-step-change-in-capabilities/)：Fortune 的獨家報導，完整還原洩露事件的來龍去脈
- [Anthropic accidentally leaked details of a new AI model that poses unprecedented cybersecurity risks — Fortune](https://fortune.com/2026/03/27/anthropic-leaked-ai-mythos-cybersecurity-risk/)：Fortune 的追蹤報導，深入分析 Mythos 的網路安全風險
- [Anthropic leaked upcoming model with "unprecedented cybersecurity risks" in the most ironic way possible — Futurism](https://futurism.com/artificial-intelligence/anthropic-step-change-new-model-claude-mythos)：最完整的諷刺角度分析，包含市場反應和歷史脈絡
- [Anthropic leak reveals new model Claude Mythos with dramatically higher scores — The Decoder](https://the-decoder.com/anthropic-leak-reveals-new-model-claude-mythos-with-dramatically-higher-scores-on-tests-than-any-previous-model/)：技術面向的分析，拆解 Mythos 與既有模型的性能差距
- [Claude Mythos & Capybara: Securing the AI Frontier — NeuralTrust](https://neuraltrust.ai/blog/claude-mythos-capybara)：從 AI 治理角度分析 Mythos 的安全意涵和部署策略
- [Cybersecurity stocks plunge as Claude Mythos leak sparks AI fear — Investing.com](https://www.investing.com/news/stock-market-news/cybersecurity-stocks-plunge-as-anthropics-claude-mythos-leak-sparks-ai-fear-4584897)：完整的市場衝擊數據，記錄了網路安全類股的歷史性閃崩
- [IBM X-Force 2026 Threat Index confirms AI made offense cheap — ToxSec](https://www.toxsec.com/p/ibm-x-force-2026-confirms-ai-supercharged)：IBM 的權威報告，佐證了 AI 正在系統性地改變網路攻防平衡
- [Responsible Scaling Policy v3.0 — Anthropic](https://anthropic.com/responsible-scaling-policy/rsp-v3-0)：Anthropic 的 AI 安全框架原文，理解 Mythos 在安全等級分類中的定位
