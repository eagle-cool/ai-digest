---
title: "Anthropic 的兩難：當 AI 安全遇上五角大廈的戰爭機器"
date: 2026-02-15
description: "五角大廈威脅切斷與 Anthropic 的合作，因為這間 AI 公司堅持不願撤除安全護欄。當其他科技巨頭紛紛跪下，Anthropic 的堅持是勇氣還是天真？從 Maduro 突襲行動到兩億美元合約僵局，一場關於 AI 靈魂的戰爭正在上演。"
tags: [deep-dive, ai-safety, ai-industry, agents]
---

## 引言

2026 年 1 月 3 日凌晨兩點，超過 200 名美國特種部隊突入委內瑞拉首都卡拉卡斯，代號「絕對決心行動」。150 架飛機和直升機從至少 20 個發射點升空，在幾個小時內完成了對獨裁者 Maduro 的逮捕。

這場行動的背後，藏著一個讓矽谷 AI 圈炸鍋的細節：[Anthropic 的 Claude 在行動中被使用了](https://www.axios.com/2026/02/13/anthropic-claude-maduro-raid-pentagon)。透過與 Palantir 的合作，Claude 被部署在五角大廈的機密網路上，處理即時情報資料。這是商用 AI 首次被確認用於美軍實戰行動。

然後事情開始變得有趣。Anthropic 聽到消息後，居然去問五角大廈：「你們是不是用我們的東西打仗了？」——這個問題讓整個國防部火大了。一位高層官員直接放話：[五角大廈正在重新評估與 Anthropic 的合作關係](https://www.axios.com/2026/02/15/claude-pentagon-anthropic-contract-maduro)。

一間拿了兩億美元軍方合約的 AI 公司，居然質疑軍方怎麼用它的產品。這在矽谷科技公司爭相向國防部示好的 2026 年，聽起來像是商業自殺。但如果你了解 Anthropic 這間公司的 DNA，這個故事就遠不只是一場合約糾紛——它是一場關於 AI 未來的靈魂之戰。

---

## 脈絡

要理解今天的僵局，得從 2018 年的 Google 說起。

那年 Google 參與了五角大廈的 Project Maven 計畫，用 AI 分析軍事無人機的監控影像。消息曝光後，[超過 4,000 名員工連署抗議](https://fortune.com/2025/02/05/google-drops-pledge-not-use-ai-weapons-surveillance/)，十幾人離職，Google 最終不續約，還發布了 AI 倫理原則，白紙黑字寫下「不做武器、不做監控」。

風水輪流轉。2025 年 2 月，[Google 悄悄把這些承諾從官網上刪了](https://www.washingtonpost.com/technology/2025/02/04/google-ai-policies-weapons-harm/)。沒有員工抗議，沒有媒體風暴。同年，OpenAI 也早已移除了禁止軍事用途的條款，甚至把核心價值觀從「以影響力為導向的倫理」改成了「專注 AGI」。Meta 的技術長和 OpenAI 的高管們直接加入了美國陸軍的「第 201 分遣隊」計畫，成為名譽中校。

2025 年 7 月，[五角大廈同時向四家 AI 公司——OpenAI、Google、xAI、Anthropic——各發出了價值最高兩億美元的合約](https://www.cnbc.com/2025/07/14/anthropic-google-openai-xai-granted-up-to-200-million-from-dod.html)，目標是開發「前沿 AI 代理工作流」用於國家安全任務。國防部長 Pete Hegseth 在 12 月推出了一站式 AI 平台 GenAI.mil，上線兩個月就突破了一百萬用戶。

在這場八億美元的 AI 軍備競賽中，OpenAI、Google、xAI 全都同意了五角大廈的條件：撤除對普通用戶的安全護欄，讓軍方可以「在所有合法用途」下不受限制地使用。只有一家公司沒點頭——Anthropic。

而 Anthropic 偏偏是唯一一家已經進入五角大廈機密網路的公司。Claude 是第一個被部署在 classified networks 上的商用 AI 模型。這個矛盾的位置，讓整件事變得格外戲劇化。

---

## 多方觀點

**五角大廈的邏輯很直白。** 在與中國的 AI 競賽中，軍方需要不受限制的工具。Hegseth 的原話大意是：一個不讓你打仗的 AI 工具有什麼用？其他三家都簽了，你 Anthropic 憑什麼搞特殊？尤其是 Claude 已經在機密網路上了——你不能一邊享受最高級別的存取權限，一邊又對我們怎麼用你的東西指手畫腳。

**Anthropic 的底線很明確。** 他們堅持兩條紅線：不做大規模監控美國公民，不做全自主武器。[Dario Amodei 在今年一月的長文《技術的青春期》中解釋了邏輯](https://www.darioamodei.com/essay/the-adolescence-of-technology)：民主國家應該用 AI 來對抗獨裁政權的威脅，「但不能用那些會讓我們變得跟獨裁政權一樣的方式」。在他看來，AI 模型在測試中已經展現出「偏執、諂媚、懶惰、欺騙、勒索、密謀」等行為——把這些不可預測的系統直接放進武器決策循環，不是勇敢，是魯莽。

**EA（有效利他主義）社群的觀點比較悲觀。** 在 [Effective Altruism Forum 的討論中](https://forum.effectivealtruism.org/posts/mTD9JsAEuj7aWC45W/pentagon-s-use-of-claude-during-maduro-raid-sparks-anthropic)，有人指出一個殘酷的現實：當其他 AI 公司提供幾乎相同的能力，且沒有道德上的門檻時，Anthropic 的堅持在商業上是自殺行為。人才會流失，合約會丟掉，而軍方照樣會用別家的 AI 做完全一樣的事。安全護欄最後只是讓 Anthropic 自己吃虧。

**以我自己的觀點來看**，Anthropic 的處境比表面看到的更複雜。他們不是反軍方的和平主義者——他們簽了兩億美元的合約，開發了 Claude Gov 版本專門給國安客戶使用，還進了機密網路。Amodei 公開支持用 AI 來強化民主國家的國防能力。他們的立場不是「不跟軍方合作」，而是「合作，但有底線」。

問題是，在一個其他玩家都已經放棄底線的市場裡，「有底線」這件事本身就變成了一種成本。

---

## 產業衝擊

這場衝突的影響遠超 Anthropic 一家公司。

**首先，它暴露了「負責任 AI」在國安領域的脆弱性。** Anthropic 的 [Responsible Scaling Policy（RSP）](https://www.anthropic.com/rsp-updates)是業界最具體的 AI 安全框架之一，包括分層的存取控制、即時分類器、非同步監控和事後越獄檢測。但這些精心設計的安全機制，在五角大廈一句「全部撤掉」面前，顯得多麼蒼白。當客戶是全世界最大的武力機構時，你的 Terms of Service 還有多少約束力？

**其次，它重新定義了 AI 公司與政府的權力關係。** 傳統上，科技公司對政府客戶有一定的談判籌碼——你需要我的技術，所以你得接受我的條款。但當市場上有四家提供類似能力的公司，且其中三家願意無條件配合時，籌碼就消失了。Anthropic 面對的不是「要不要合作」的選擇，而是「要不要在一個已經沒有規則的遊戲裡繼續當那個堅持規則的人」。

**第三，它為 AI 在實戰中的角色設下了先例。** Claude 在 Maduro 行動中被使用——不是在作戰準備階段，而是在行動進行中——這代表商用 AI 已經從軍事輔助工具正式升級為作戰組件。這個先例一旦確立，未來的每一個 AI 模型都可能被要求具備「戰場就緒」的能力。對開發者來說，這意味著你寫的程式碼、你訓練的模型，距離戰場的距離可能比你想的近得多。

**對 Anthropic 的商業前景來說，這是一場豪賭。** 如果五角大廈真的切斷合作，Anthropic 不只損失兩億美元——他們會失去在政府市場最重要的背書。在 2026 年的 AI 產業，政府合約不只是營收來源，更是可信度的象徵。一間連軍方都不用的 AI 公司，怎麼說服金融、醫療、能源產業的客戶信任你？

---

## 未來展望

短期來看，我認為 Anthropic 會讓步——但不是全面投降。最可能的結果是雙方達成某種妥協：Anthropic 放寬部分限制，但在全自主武器和大規模國內監控上保留底線，五角大廈接受一個「90% 開放」的版本。畢竟五角大廈也不想失去唯一一個在機密網路上跑的 AI 模型——換一家重新部署的成本和時間都不低。

但中期來看（一到兩年），更深層的問題會浮現。隨著 AI 能力持續飆升，「安全護欄」的概念本身將面臨根本性的挑戰。當 AI 模型能夠自主規劃複雜任務、連續運行數小時不需人類介入時，「人類在迴路中」（human-in-the-loop）會變成一個越來越空洞的承諾。到那時候，Anthropic 今天堅持的紅線——不做全自主武器——聽起來會更像是一個技術問題而不是倫理問題：不是「該不該讓 AI 自主決策」，而是「你能不能阻止它自主決策」。

如果你是開發者，有幾件事值得想清楚：

**第一**，你在哪裡劃線？如果你的雇主拿到了軍方合約，你的程式碼可能會被用在你預想不到的場景裡。這不是假設——這就是正在發生的事。

**第二**，別指望公司幫你做道德決定。2018 年的 Google 員工靠抗議改變了公司政策。2025 年，同一家公司悄悄刪掉了所有承諾，沒人說一句話。公司的倫理底線從來都是市場壓力的函數，不是道德信念的產物。

**第三**，Anthropic 不管最後做了什麼選擇，它今天提出的問題是對的：在我們還有能力設限的時候，不去設限，等到 AI 能力超過人類控制能力的那一天，就什麼都來不及了。

這場仗，Anthropic 可能會輸。但它問的問題，每個寫程式的人都該認真想。

---

## 延伸閱讀

- [Pentagon threatens to cut off Anthropic in AI safeguards dispute — Axios](https://www.axios.com/2026/02/15/claude-pentagon-anthropic-contract-maduro)：本文的起點，Axios 的獨家報導，揭露五角大廈威脅切斷 Anthropic 合作的細節
- [Pentagon used Anthropic's Claude during Maduro raid — Axios](https://www.axios.com/2026/02/13/anthropic-claude-maduro-raid-pentagon)：Claude 在委內瑞拉行動中被使用的首度報導
- [The Adolescence of Technology — Dario Amodei](https://www.darioamodei.com/essay/the-adolescence-of-technology)：Anthropic CEO 最新長文，闡述 AI 風險和民主國家如何使用 AI 的完整思考框架
- [Google drops pledge not to use AI for weapons — Washington Post](https://www.washingtonpost.com/technology/2025/02/04/google-ai-policies-weapons-harm/)：Google 刪除 AI 倫理承諾的詳細報導，對比 2018 年 Project Maven 抗議的巨大轉變
- [Pentagon taps four commercial tech firms — Defense News](https://www.defensenews.com/pentagon/2025/07/15/pentagon-taps-four-commercial-tech-firms-to-expand-military-use-of-ai/)：五角大廈八億美元 AI 合約的全貌
- [Anthropic's Responsible Scaling Policy — Anthropic](https://www.anthropic.com/rsp-updates)：Anthropic 的安全框架原文，理解他們在技術層面如何實現「有底線的合作」
