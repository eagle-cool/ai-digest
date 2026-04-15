---
title: "Linus 的務實豪賭：AI 代碼正式進入 Linux 內核，開源世界的遊戲規則正在改寫"
date: 2026-04-15
description: "Linux 內核正式發布 AI 輔助代碼政策，允許 AI 生成的代碼進入世界上最關鍵的開源專案，但人類必須承擔全部責任。這不是妥協，而是一場關於開源社會契約的深層重構。"
tags: [deep-dive, ai-coding, ai-tools, ai-industry]
---

## 引言

想像你是一個 Linux 內核的維護者。每天早上打開信箱，迎面而來的是一堆補丁——有些來自你認識了十年的老戰友，有些來自素未謀面的新人。你的工作是判斷每一行代碼是否值得被合進這個運行著全球超過 90% 伺服器、驅動著無數 Android 手機和嵌入式設備的作業系統核心。

現在，這些補丁裡有一些是 AI 寫的。你可能看不出來。

2026 年 4 月，經過數個月的激烈辯論，Linus Torvalds 和 Linux 內核維護者團隊正式發布了 Linux 內核第一套 AI 輔助代碼政策。這套規則的核心訊息簡單得不能再簡單：**AI 可以用，但出了事，人來扛。**

這聽起來像是常識，但背後的意義遠比字面深刻得多。這是全球最重要的開源專案——一個定義了「什麼是好代碼」長達三十多年的社群——第一次正式承認 AI 已經成為開發流程中不可忽視的一部分。而做出這個決定的人，正是那個以對代碼品質要求嚴苛到近乎偏執聞名的 Linus Torvalds。

但如果你以為這是 Torvalds 的妥協，那你就低估了這個男人。仔細看這套政策的設計，你會發現它比任何 AI 禁令都更精明——它沒有試圖阻擋一股擋不住的浪潮，而是重新定義了浪潮中人類的角色和責任。這篇報導的起點是 [InfoQ 的深度報導](https://www.36kr.com/p/3766159271117570)，但故事遠不止於此。

---

## 事件全貌

Linux 內核的 AI 代碼政策於 2026 年 4 月初正式合入 Torvalds 的代碼樹，文件位於 `Documentation/process/coding-assistants.rst`。[根據 Tom's Hardware 報導](https://www.tomshardware.com/software/linux/linux-lays-down-the-law-on-ai-generated-code-yes-to-copilot-no-to-ai-slop-and-humans-take-the-fall-for-mistakes-after-months-of-fierce-debate-torvalds-and-maintainers-come-to-an-agreement)，文件維護者 Jonathan Corbet 合入這份文件後等了一段時間，看看有沒有人反對——結果沒有人跳出來。

這套政策定了三條核心規則。

**第一條：AI 不能簽名。** 只有人類才能添加 `Signed-off-by` 標籤。這個標籤對應的是 Linux 內核自 2004 年以來使用的開發者來源證明（Developer Certificate of Origin，DCO），它是確保代碼許可合規的法律機制。換句話說，不管你的補丁有多少是 AI 寫的，法律責任只在你身上，而不在 OpenAI、Anthropic 或 Google 身上。

**第二條：必須標注 AI 參與。** 如果在開發過程中使用了 AI 工具，就必須在提交訊息中加入 `Assisted-by` 標籤，格式如下：

```
Assisted-by: AGENT_NAME:MODEL_VERSION [TOOL1] [TOOL2]
```

比如用了 Claude 和 coccinelle 靜態分析工具，就要寫成 `Assisted-by: Claude:claude-3-opus coccinelle sparse`。這裡的設計相當精細——日常基礎工具（如 git、gcc、make）不需要標注，但 AI 模型和專門的分析工具必須寫清楚。

**第三條：人類承擔一切後果。** 這是前兩條的邏輯總結。AI 生成的代碼有沒有經過完整審查？許可證是不是合規？後續出了 bug 或安全漏洞？全部由提交代碼的人負責。

值得注意的是 `Assisted-by` 這個名稱的選擇。社群在討論過程中考慮過 `Generated-by`（生成者）和 `Co-developed-by`（共同開發者），最終選擇了 `Assisted-by`（輔助者）。[根據 Implicator 的分析](https://www.implicator.ai/linux-didnt-approve-ai-kernel-code-it-made-the-human-submitter-the-fuse/)，這個選擇基於三個考量：更準確地反映 AI 作為工具的角色、與現有的 `Reviewed-by`、`Tested-by` 標籤格式一致、以及使用中性表達——既說明了工具參與，又不暗示代碼「不可信」或「低一等」。

同一週，Torvalds 發布了 Linux 內核 7.0。在發布說明中，他寫了一句意味深長的話：「我懷疑，接下來一段時間，大家大量使用 AI 工具，還會不斷幫我們把各種邊角問題翻出來，所以這可能會成為一段時間裡的『新常態』。」

---

## 脈絡

要理解這套政策為什麼在 2026 年 4 月出現，而不是更早或更晚，你得先看清三條交匯的時間線。

### 第一條線：AI 代碼從垃圾到真貨

2025 年，開源世界面對的 AI 問題主要是「AI slop」——那些由 AI 生成的、品質低劣的安全報告和 Pull Request。[cURL 的創始人 Daniel Stenberg 因為 AI 垃圾報告太多](https://www.theregister.com/2026/03/26/greg_kroahhartman_ai_kernel/)，一度暫停了漏洞賞金計畫。[根據 The New Stack 報導](https://thenewstack.io/ai-slop-open-source/)，有開發者估計，審查和修正一個 AI 生成的 Pull Request 所花的時間，是用 AI 生成它的 **12 倍**。Jazzband 專案的首席維護者甚至因為 AI 垃圾 PR 的洪水而直接關閉了整個專案。

但在 2026 年 2 月，某個看不見的轉折點出現了。

Linux 穩定內核維護者 Greg Kroah-Hartman 在接受 The Register 採訪時描述了這個變化：「幾個月前，我們收到的還是所謂的『AI slop』，那些明顯不對、品質很低的 AI 安全報告。當時甚至還有點好笑，也不太讓人擔心。」然後，大約在 2 月份，「某個節點發生了變化，整個世界都切換了。現在我們收到的，是『真的』報告了。」

而且不只是 Linux。所有主要開源專案的安全團隊都同時觀察到了同樣的變化。被問到原因時，Kroah-Hartman 坦承：「我們也不知道。沒人知道為什麼。可能是很多工具突然變好了，也可能是大家開始認真用這些工具了。」

這段話的潛台詞很明確：**AI 代碼工具已經跨過了某個品質門檻，你不能再假裝它們不存在了。**

當 Kroah-Hartman 用基本提示詞測試 AI 補丁生成時，結果顯示：60 個生成的補丁中約 66% 是可用的（雖然需要人類精修），33% 有錯誤但仍然指出了真實的問題。Google 捐贈給 Linux 基金會的 AI 代碼審查工具 Sashiko 更進一步——在一個 1,000 個補丁的測試集上達到了 53% 的 bug 偵測率，而人類審查者的偵測率是零。

### 第二條線：Sasha Levin 的「坦白從寬」

這整場政策辯論的導火線，是 NVIDIA 工程師、知名 Linux 內核開發者 Sasha Levin 的一個決定。

2024 年底到 2025 年初，Levin 向 Linux 6.15 提交了一個補丁——代碼完全由 LLM 生成，連 changelog 也是。他審查和測試了代碼，但並沒有親自編寫，**而且他沒有向審查者披露這個事實**。

這件事在社群內引起了軒然大波。有趣的是，社群的憤怒主要不是因為他用了 AI，而是因為他**沒說**。在 2025 年北美開源峰會上，Levin 公開分享了他的做法，並開始倡導建立正式的透明規則。他把 LLM 比作「下一代編譯器」——過去開發者寫組合語言，後來有了高階語言，當時也有人說「真正的開發者應該自己分配暫存器」。LLM 也是類似的演進。

Levin 在 2025 年 7 月提交了 AI 政策的第一版提案，最初建議使用 `Co-developed-by` 來標記 AI 參與。經過 LKML（Linux Kernel Mailing List）上的反覆討論，最終演變成了今天的 `Assisted-by`。

### 第三條線：Torvalds 自己也開始用 AI 了

2026 年 1 月，Torvalds 發布了一個叫做 AudioNoise 的個人專案——一個探索數位音訊效果的開源工具。[根據 It's FOSS 報導](https://itsfoss.com/news/linus-torvalds-vibe-coding/)，他用 C 語言自己寫了核心的 DSP 代碼，但 Python 視覺化工具的部分，他直接用了 Google 的 AI IDE「Antigravity」（一個基於 Windsurf 的分支，底層用 Google Gemini）。

在專案的 README 裡，Torvalds 寫道：「注意，Python 視覺化工具基本上是 vibe-coding 寫出來的⋯⋯我對類比濾波器的了解——雖然也不多——比我對 Python 的了解還多。」

這是一個極其微妙的信號。Linux 的創造者——那個會在郵件列表上對爛代碼破口大罵的人——自己也在用 AI 寫代碼了。但他很清楚地畫了一條線：個人玩具可以 vibe-coding，但 Linux 內核的品質標準一分也不會降。

這三條線交匯在一起，就構成了 2026 年 4 月政策出台的完整背景：AI 工具已經好到不能忽視、社群已經因為缺乏規則而產生衝突、而連 Torvalds 自己都在用 AI——是時候定規矩了。

---

## 多方觀點

### 務實派：AI 只是工具，別大驚小怪

Torvalds 的立場最能代表這一派。他在 LKML 上明確表示：「我不希望內核開發文檔變成某種 AI 立場聲明。『世界要完了』和『AI 會徹底改變軟體工程』這兩種聲音已經夠多了。我不希望文檔站隊。對我來說，它就應該是——AI 只是一個工具。」

[根據 Tom's Hardware 的報導](https://www.tomshardware.com/software/linux/linux-lays-down-the-law-on-ai-generated-code-yes-to-copilot-no-to-ai-slop-and-humans-take-the-fall-for-mistakes-after-months-of-fierce-debate-torvalds-and-maintainers-come-to-an-agreement)，Torvalds 更進一步指出，禁止 AI 使用是「毫無意義的姿態」——壞人不會讀文檔，更不會遵守你的禁令。與其試圖管控開發者在自己電腦上裝了什麼軟體，不如把焦點放在代碼品質和人的責任上。

Sasha Levin 也站在這一邊，但更激進。他認為 LLM 在處理「小而明確」的任務上已經非常出色——比如 API 遷移、格式轉換、簡單的 bug 修復。他展示了一個從舊哈希 API 切換到新 API 的補丁，LLM 不僅正確理解了需要把「大小」改為「2 的冪表示」，還自動識別並刪除了一個多餘的 mask 操作。

### 保守派：禁令才是正確答案

並非所有開源專案都選擇了 Linux 的務實路線。[NetBSD 的官方指南](https://hackaday.com/2026/04/14/new-linux-kernel-rules-put-the-onus-on-humans-for-ai-tool-usage/)將 LLM 輸出視為「推定受污染的」（presumed tainted），直接禁止 AI 生成的提交。Gentoo 也採取了類似立場，理由是 AI 代碼可能在其套件發行模型中造成授權污染的連鎖反應。

這些專案的擔憂並非沒有道理。它們大多使用 BSD 或其他寬鬆許可證，而不是 Linux 的 GPL-2.0-only。[Implicator 的分析](https://www.implicator.ai/linux-didnt-approve-ai-kernel-code-it-made-the-human-submitter-the-fuse/)指出了一個關鍵的法律不對稱：如果 AI 工具（如 Copilot）「吐出」了 GPL 訓練數據中的代碼到一個 BSD 許可的專案中，那個專案就產生了無法合法再授權的代碼。但 Linux 內核使用 GPL-2.0-only 授權，最壞的情況不過是「AI 生成的代碼恰好也符合 GPL」——這根本不構成法律風險。

換句話說，**Linux 有能力對 AI 代碼開放，部分原因恰恰是因為它的許可證本來就是最嚴格的那種。**

### 開源維護者的血淚控訴

離開 Linux 這個有大量企業支持的巨型專案，中小型開源專案面對的 AI 衝擊要殘酷得多。

[The New Stack 的調查](https://thenewstack.io/ai-slop-open-source/)揭示了一組令人震驚的數字：96% 的商業代碼庫包含開源組件，但 60% 的維護者是無薪志工。在 AI 時代，這些志工面對的是指數級增長的低品質提交。

Godot 引擎的 Rémi Verschelde 形容管理 AI 提交「讓人精疲力竭、士氣低落」。Jazzband 專案因 AI 垃圾 PR 不堪負荷而直接關閉。Node.js 和 OCaml 社群出現了超過 10,000 行的 AI 生成 PR，引發了關於專案未來方向的存在性辯論。

更極端的案例是 GZDoom。2024 年，首席開發者 Graf Zahl 在未披露的情況下使用 AI 提交補丁，引發社群分裂，最終催生了新的 UZDoom 分支——不是因為 AI 代碼品質差，而是因為**信任被破壞了**。

### 法律界的警告

美國版權局已經認定，純粹由 AI 生成的代碼不受版權保護，因為它缺乏人類的創意輸入。2026 年 3 月，[美國最高法院拒絕審理相關案件](https://www.morganlewis.com/pubs/2026/03/us-supreme-court-declines-to-consider-whether-ai-alone-can-create-copyrighted-works)，維持了「人類作者要求」的立場。

這對開源的影響是深遠的。[Quippd 的分析](https://www.quippd.com/writing/2026/04/08/ai-code-is-hollowing-out-open-source-and-maintainers-are-looking-the-other-way.html)指出了一個令人不安的邏輯鏈：如果 AI 生成的代碼屬於公共領域，那麼當這些代碼被合入 GPL 或 LGPL 專案時，copyleft 條款在這些代碼上**就不再有效**。這意味著任何人都可以不受限制地使用這些部分，而不需要遵守開源許可證的互惠要求。用文章的話說：「價值從專案中流失了。」

一個具體案例：chardet 函式庫的維護者用 Claude 在一週內重寫了整個函式庫，然後在未經原始作者 Mark Pilgrim 同意的情況下，將授權從 LGPL 改為 MIT。Pilgrim 明確反對，但維護者聲稱這是「無塵室」（clean-room）重寫，儘管 AI 的訓練數據幾乎可以確定包含了原始代碼。

### 我的看法

以我的觀察，Linux 內核的做法是目前所有方案中最聰明的一個——但它之所以能成立，有很強的特殊性。

Linux 有三個其他專案不具備的優勢：一、GPL-2.0-only 授權提供了天然的法律護城河；二、龐大的維護者社群提供了足夠的人力來做代碼審查；三、Torvalds 本人的權威和「不好惹」的名聲是最強的威懾力——你真的不想因為提交 AI 垃圾代碼而被他在郵件列表上公開處刑。

但對那些只有一兩個維護者的小型專案來說，Linux 的模式根本無法複製。`Assisted-by` 標籤對他們來說就像是在洪水中掛了一塊「請自律」的牌子。

---

## 產業衝擊

### 第一層：開發者角色的根本轉變

Linux 內核的政策本質上重新定義了「開發者」這個角色。在這套規則下，提交代碼的人不再只是「寫代碼的人」，而是「為代碼負責的人」。這兩者之間的差異看似微妙，實際上是天翻地覆的。

Sasha Levin 說得最到位：LLM 是「下一代編譯器」。過去我們從組合語言升級到高階語言時，沒有人因此被降級——反而是所有人的生產力都提升了。但「下一代編譯器」的類比也暗示了一個殘酷的現實：如果 LLM 能處理「小而明確」的任務，那麼大量初級開發者的日常工作——API 遷移、格式轉換、簡單 bug 修復——正是最容易被自動化的部分。

[Hackaday 的評論區](https://hackaday.com/2026/04/14/new-linux-kernel-rules-put-the-onus-on-humans-for-ai-tool-usage/)有一個數字值得深思：有經驗的開發者每次能可靠審查大約 500 行代碼，但 LLM 工具可以瞬間生成 50,000 行以上的代碼。這中間的差距——審查能力遠遠跟不上生成速度——是一個結構性的品質瓶頸。

### 第二層：開源的社會契約正在被改寫

開源軟體的運作基於一個隱性的社會契約：你貢獻代碼，社群幫你審查和改進，你的貢獻受到版權保護和許可證的約束，大家互惠互利。

AI 正在從多個方向侵蝕這個契約。

**從貢獻端：** AI 降低了「貢獻」的門檻到接近零——任何人都可以讓 ChatGPT 生成一個 PR 然後提交。這直接衝擊了開源社群傳統的「信任積累」模式，因為一個有 100 個 commit 歷史的貢獻者和一個用 AI 批量生成 PR 的新帳號，在 GitHub 的介面上看起來差別不大。

**從授權端：** 如前所述，AI 生成的代碼可能屬於公共領域，這讓 copyleft 許可證的互惠機制失效。原始貢獻者選擇 GPL 或 LGPL 是因為他們相信衍生作品也會保持開放——但 AI 改寫繞過了這個前提。

**從維護端：** 維護者被迫花更多時間在「分辨垃圾」而不是「推進專案」上。Anaconda 的 Steve Croce 警告：「如果不積極管理 AI 時代的貢獻品質，我們就是在把整個生態系統置於危險之中。」

### 第三層：`Assisted-by` 標籤的隱藏價值

表面上看，`Assisted-by` 只是一個透明機制。但 Implicator 的分析指出了它更深層的設計意圖：**它是一個用於「bug 考古學」的鑑識工具。**

想像一下，幾年後，內核開發者回頭分析某類 bug 的分佈時，發現標記了 `Assisted-by: Claude:claude-3-opus` 的補丁在記憶體安全問題上的發生率明顯高於人工撰寫的補丁，或者某個特定模型版本的補丁有系統性的邏輯錯誤。這種數據的價值是巨大的——它可以指導未來的審查策略、影響工具選擇，甚至為 AI 公司提供改進模型的反饋。

但這個標籤也有明顯的漏洞：它沒有區分「用 AI 自動補全了一行代碼」和「整個補丁都是 AI 生成的」。這個灰色地帶幾乎必然會被利用——開發者可能策略性地低報 AI 的參與程度。

### 第四層：二階效應的連鎖反應

Linux 內核的決策將產生遠超 Linux 本身的漣漪效應。

**對其他開源專案的示範效應：** Linux 是開源世界的精神領袖。它的政策選擇——接受但要求透明——將成為許多其他專案的參考模板。已經有跡象顯示，Firefox、WordPress、Fedora 等專案正在制定類似的 AI 披露政策。根據調查，目前已有 63 個正式的 AI 政策分佈在各基金會和專案中，14 個專案直接禁止 AI 貢獻，12 個仍在觀望。

**對企業的影響：** 大量商業軟體建立在 Linux 之上。如果 AI 生成的代碼可以合法進入內核，那企業自己的代碼政策也需要跟上。Red Hat 已經發表分析，警告 DCO（開發者來源證明）在 LLM 訓練數據涉及 GPL 代碼時可能產生法律不確定性。

**對 AI 公司的影響：** `Assisted-by` 標籤直接點名了模型和版本。這意味著 AI 公司的產品品質將在最嚴格的代碼審查環境中被公開追蹤。如果某個模型反覆出現在有問題的補丁中，這對該公司的品牌將是致命打擊。

---

## 未來展望

### 短期（3-6 個月）：新常態的磨合期

可以幾乎確定的是，`Assisted-by` 標籤將開始出現在越來越多的內核補丁中。隨著 Sashiko 等 AI 審查工具在更多子系統部署，AI 將同時出現在代碼生成和代碼審查的兩端——這本身就是一個值得深思的狀態。

Kroah-Hartman 提到的 AI 安全報告品質提升「沒有放緩的跡象」。這意味著維護者將需要開發新的工作流來處理 AI 生成的高品質報告——這些報告的數量可能遠超人類審查的產能。

同時，其他主要開源專案將被迫表態。目前的 63 個正式政策在六個月內可能翻倍。有些專案會效仿 Linux 的務實路線，有些會選擇 NetBSD 的禁令路線，但「不做決定」已經不再是一個選項。

### 中期（6-18 個月）：三條可能的路徑

**情境一：透明機制成功。** `Assisted-by` 標籤被廣泛採用，AI 代碼的品質數據開始積累，社群根據數據調整審查策略。AI 公司主動改進模型以提高在內核場景下的表現。這是最樂觀的路徑。

**情境二：灰色地帶擴大。** 大量開發者選擇不標注 AI 使用，或策略性地低報。Torvalds 自己也承認：「討論 AI 垃圾代碼沒有意義，因為寫這些的人不會主動標注。」如果透明機制被架空，政策可能需要演進到更強制的方向——比如要求所有提交通過某種 AI 使用的自動檢測。

**情境三：法律炸彈引爆。** 如果美國國會或歐盟通過了關於 AI 生成代碼的新法規——比如要求披露 AI 訓練數據的來源、或對 AI 代碼的版權地位做出新的裁定——整個開源世界可能需要從頭重新思考它與 AI 的關係。目前已經有價值 15 億美元的 AI 版權訴訟在進行中。

### 長期推演：3-5 年後的世界

如果 AI 代碼工具繼續以目前的速度進步，3-5 年後的內核開發可能看起來完全不同。

想像一個場景：維護者的主要工作不再是審查人寫的代碼，而是監督和驗證 AI 生成的代碼。`Assisted-by` 標籤從例外變成常態——大多數補丁都有 AI 參與，純人工撰寫的補丁反而變成少數。Levin 提到的「用 AI 做合入前自動審查」在成本下降後變得可行，AI 同時負責生成和審查代碼。

在這個世界裡，Torvalds 在 2023 年說的那句話會變得更加重要：**「評判他人的代碼，需要一定的品味。」** 當 AI 能寫出正確的代碼時，「品味」——對架構優雅性的判斷、對長期維護成本的直覺、對安全風險的嗅覺——才是人類開發者最不可替代的能力。

### 給讀者的行動建議

**如果你是開發者：** 開始建立系統性地使用和審查 AI 代碼的能力。不是「學怎麼用 Copilot」那麼簡單——而是培養判斷 AI 輸出品質的「品味」。理解你使用的 AI 工具的弱點：它在什麼情境下容易犯錯？它的輸出在哪些方面需要特別小心？Linux 內核的 `Assisted-by` 模式告訴我們，未來的開發者價值不在於能寫多快，而在於能為多少代碼背書。

**如果你是開源維護者：** 你現在就需要一個 AI 政策，不管你的專案多小。Linux 的模板是一個好的起點，但記住它有特殊條件（GPL 授權、大型維護團隊、Torvalds 的威懾力）。對小型專案來說，可能需要更嚴格的規則——比如要求 AI 生成的 PR 附帶人工測試證明，或限制單次 PR 的行數上限。

**如果你是科技從業者：** 關注 AI 代碼的法律風險。你的公司使用的開源軟體裡，可能已經包含了 AI 生成的代碼——這些代碼的版權狀態可能是模糊的。確保你的法律團隊了解這個問題，特別是如果你的產品依賴 copyleft 許可的開源元件。

Linux 內核對 AI 代碼的態度，本質上是一個古老問題的最新版本：**當新工具出現時，我們是選擇恐懼還是選擇駕馭？** Torvalds 選擇了駕馭，但他加了一個條件——駕馭的人必須為方向負責。在 AI 正在改變一切規則的時代，這可能是唯一清醒的立場。但清醒不等於安全。這場實驗剛剛開始，而結局取決於每一個提交代碼的人，是否真的準備好為那個 `Signed-off-by` 背後的承諾負責。

---

## 延伸閱讀

- [AI Coding Assistants — Linux 內核官方文件](https://docs.kernel.org/process/coding-assistants.html)：政策原文，Linux 內核對 AI 工具使用的正式規範
- [Linux kernel czar says AI bug reports aren't slop anymore — The Register](https://www.theregister.com/2026/03/26/greg_kroahhartman_ai_kernel/)：Greg Kroah-Hartman 描述 AI 報告品質轉折的第一手訪談，資料密度極高
- [Linux lays down the law on AI-generated code — Tom's Hardware](https://www.tomshardware.com/software/linux/linux-lays-down-the-law-on-ai-generated-code-yes-to-copilot-no-to-ai-slop-and-humans-take-the-fall-for-mistakes-after-months-of-fierce-debate-torvalds-and-maintainers-come-to-an-agreement)：政策出台的完整時間線和社群辯論回顧，包含多個專案的對比
- [Linux Kernel Permits AI Code, Pins Liability on the Human — Implicator](https://www.implicator.ai/linux-didnt-approve-ai-kernel-code-it-made-the-human-submitter-the-fuse/)：最深入的法律和政策分析，解釋了 GPL 授權如何成為 Linux 的護城河
- [AI Code is Hollowing Out Open Source — Quippd](https://www.quippd.com/writing/2026/04/08/ai-code-is-hollowing-out-open-source-and-maintainers-are-looking-the-other-way.html)：AI 代碼對 copyleft 許可證的侵蝕效應，附 chardet 案例分析
- [96% of codebases rely on open source, and AI slop is putting them at risk — The New Stack](https://thenewstack.io/ai-slop-open-source/)：AI 垃圾提交對開源生態的衝擊全景，包含維護者調查數據和各專案應對策略
- [Even Linux Creator Linus Torvalds is Using AI to Code — It's FOSS](https://itsfoss.com/news/linus-torvalds-vibe-coding/)：Torvalds 個人使用 AI 的細節，AudioNoise 專案和「vibe coding」的故事
- [Supporting kernel development with large language models — LWN.net](https://lwn.net/Articles/1026558/)：Sasha Levin 在開源峰會上的演講紀錄，技術細節最為豐富
