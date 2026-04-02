---
title: "百車趴窩武漢環線：Robotaxi 安全神話的第一道裂縫"
date: 2026-04-02
description: "百度蘿蔔快跑百輛無人車在武漢環線集體癱瘓，乘客受困高架橋上。這不只是一次系統故障——它暴露了 Robotaxi 產業從規模競賽到安全基建的根本斷層，也迫使我們重新思考：當自動駕駛成為城市基礎設施，誰來為「不會出錯」的承諾買單？"
tags: [deep-dive, ai-industry, agents]
---

## 引言

3 月 31 日晚上九點，武漢二環線楊泗港長江大橋附近，一位剛上車準備去上班的乘客盧先生，發現自己搭的蘿蔔快跑突然不動了。車停在三環高架的車道正中央，螢幕上跳出一行字：「駕駛系統異常，工作人員預計 5 分鐘到達。」

他按了車內的 SOS 按鈕。沒有回應。

他打了客服電話。等了三十分鐘，客服說「不清楚狀況，請提供車號」。

他繼續等。高架橋上沒有紅綠燈，貨車和轎車從兩側呼嘯而過。一個小時過去了，承諾的工作人員沒有出現。最後，是交通警察把他從車裡救出來的。

盧先生不是唯一的受害者。同一個晚上，超過一百輛蘿蔔快跑的 Robotaxi 在武漢全城集體「趴窩」——閃著雙閃燈，橫亙在環線的快車道上，像一群突然斷電的機器殭屍。一位現場交警事後對媒體說：「有百八十台，系統故障了。乘客按按鈕可以開門，但人在環線上下不來。[我們今天救了很多人。](https://www.36kr.com/p/3749027010691590)」

這是中國首次出現 Robotaxi 大規模集體癱瘓事件。沒有人受傷——但這個「沒有」，靠的不是技術，而是運氣和警察的反應速度。

這篇報導的起點是[雷科技對這起事件的報導](https://www.36kr.com/p/3749027010691590)，但故事遠不止於此。當一個部署了超過千輛無人車的城市在一個晚上經歷百車癱瘓，問題已經不再是「系統什麼時候能修好」，而是：我們對 Robotaxi「安全」的理解，是不是從一開始就錯了？

---

## 事件全貌

### 一場靜默的癱瘓

根據多家媒體整理的時間線，3 月 31 日晚間約 8:45 至 9:00 之間，武漢市二環線、三環線及多條主幹道上的蘿蔔快跑 Robotaxi 開始陸續停擺。車輛在行駛途中突然停止，車內螢幕顯示「駕駛系統異常」警告。[社群媒體上迅速湧出大量影片和照片](https://www.scmp.com/tech/article/3348654/baidus-robotaxi-breakdown-wuhan-strands-riders-raises-safety-concerns)，顯示多輛無人車停在高架道路的行車道上，造成後方車流壅塞，部分路段甚至發生追撞事故。

根據[南華早報的報導](https://www.scmp.com/tech/article/3348654/baidus-robotaxi-breakdown-wuhan-strands-riders-raises-safety-concerns)，乘客盧先生的車在晚間 8:45 左右停擺，他直到 10:40 才在警方協助下脫困——整整被困了將近兩個小時。另一位周女士的車也在中間車道停下，兩側車輛高速通過，她不敢開門下車。多位乘客反映，車內的 SOS 按鈕「完全沒有作用」，客服電話長時間無人接聽，而百度承諾派出的現場工作人員遲遲未到。

更諷刺的是，至少有一位乘客在被困結束後，收到了全額車費的帳單。

武漢交警在事後通報中將此事定性為「系統故障所致」，百度方面則對多家國際媒體表示原因是「網路問題導致車輛駕駛系統異常」。但[截至事件發生後超過 24 小時](https://carnewschina.com/2026/04/01/apollo-gos-robotaxi-fleet-suffers-mass-paralysis-stranding-passengers-on-elevated-highways/)，百度未發布任何正式公開聲明——沒有道歉，沒有技術說明，沒有改善承諾。

### 這不是第一次，也不會是最後一次

把武漢事件放到全球 Robotaxi 的事故時間軸上，你會發現一個令人不安的模式：

**2023 年 10 月**，通用汽車旗下的 Cruise 在舊金山發生嚴重事故——一輛 Robotaxi [將一名被其他車輛撞倒的行人拖行了約 6 公尺](https://www.freightwaves.com/news/why-robotaxis-keep-failing-while-av-trucks-take-the-slow-road-to-safety)，因為車底感測器未能偵測到被壓在車下的人體。加州監管機構撤銷了 Cruise 的營運許可，CEO 辭職，通用最終在 2024 年 12 月宣布關閉整個 Cruise 部門——這家曾估值 300 億美元、[燒掉超過 100 億美元](https://finance.yahoo.com/news/gms-cruise-robotaxi-exit-a-result-of-serious-problems-from-scaling-too-fast-and-continued-high-costs-151115166.html)的公司，就這樣消失了。

**2025 年 12 月**，舊金山遭遇大規模停電，大量 Waymo 無人車因無法識別失效的交通號誌而啟動雙閃原地停滯，[一度阻擋了應急通道](https://techcrunch.com/2026/03/25/waymo-robotaxi-roadside-assistance-emergency-first-responders/)。事後調查發現，在至少六次事件中，第一線救護人員不得不親自操控 Waymo 車輛將其移出車道——其中一次，警察正在處理大規模槍擊案現場。

**2025 年全年**，Waymo 在奧斯汀的 Robotaxi 被記錄到至少 [19 次違規通過停靠中的校車](https://www.therobotreport.com/waaymo-recalls-robotaxi-software-after-school-bus-safety-failures/)——無視閃爍的紅燈、展開的停止臂和過馬路的孩童。其中五次發生在 Waymo 聲稱已推送修復更新之後。NHTSA 最終要求召回。

**2026 年 2 月**，洛杉磯暴雨中兩輛 Waymo 在洪水中趴窩，被網友調侃「Waymo water than I was expecting」。

從舊金山到奧斯汀到洛杉磯再到武漢，Robotaxi 的「集體癱瘓」已經是一個跨地域、跨平台、跨技術路線的系統性現象。每一次，業者都說這是「偶發事件」；但當偶發事件的頻率高到這種程度，它就不再是偶發——它是結構性的。

---

## 脈絡

### 一場速度與安全的豪賭

要理解武漢事件為什麼不只是「一次系統故障」，必須先看清整個 Robotaxi 產業正在經歷的瘋狂加速。

武漢是百度 Apollo Go 的全球最大部署城市，[截至 2026 年初運營超過 1,000 輛無人車](https://cnevpost.com/2025/05/22/baidu-apollo-go-robotaxi-1000-milestone/)。2025 年第三季度，蘿蔔快跑的全球訂單量達到 310 萬單，同比增長 212%。到 2025 年第四季度，[這個數字跳升到 340 萬單](https://seekingalpha.com/news/4523549-baidu-aims-for-expanded-global-robotaxi-reach-and-accelerated-ai-monetization-as-apollo-go)，單週訂單峰值突破 30 萬筆。累計至 2026 年 2 月，Apollo Go 在全球完成超過 2,000 萬次無人駕駛服務。

這些數字背後是一場殘酷的規模競賽。就在武漢事故發生的同一個月：小鵬汽車宣布成立獨立 Robotaxi 事業部，計劃 2026 下半年載客營運；滴滴與廣汽聯合開發的 Robotaxi 已在廣州南沙和上海嘉定商業化運營，放出「[2027 年底部署 10 萬輛](https://www.36kr.com/p/3749027010691590)」的豪言；文遠知行 2025 年財報顯示 Robotaxi 營收同比暴漲 209.6%；小馬智行在去年第四季度首次扭虧為盈。僅廣州一個城市，就匯聚了小鵬、文遠知行、小馬智行、百度 Apollo、滴滴五家 Robotaxi 企業。

這讓人想起 2020-2023 年的 Cruise。通用旗下的 Cruise 在舊金山瘋狂擴張，[利用加州寬鬆的監管框架](https://www.freightwaves.com/news/why-robotaxis-keep-failing-while-av-trucks-take-the-slow-road-to-safety)，在「舊金山消防局長、警察局和交通官員的明確反對下」取得了 24/7 無限制營運許可。結果呢？一場行人拖行事故，100 億美元打水漂，整個部門被關閉。

市場研究機構的預測更是火上加油。Fortune Business Insights 估計全球 Robotaxi 市場在 2026 年規模約 [182 億美元](https://www.fortunebusinessinsights.com/robo-taxi-market-103661)，到 2034 年將暴增至超過 2 兆美元，年複合增長率超過 80%。AnalystView 則預測到 2032 年市場規模達 [1,587 億美元](https://www.globenewswire.com/news-release/2026/02/26/3245215/0/en/Explosive-Growth-Ahead-Robotaxi-Market-Set-to-Hit-US-158-73-Billion-by-2032-Expanding-at-a-Decent-CAGR-of-78-5-2025-2032-Powered-by-Breakthroughs-in-Level-4-Autonomy-and-Next-Gener.html)，CAGR 達 78.5%。

當兆級市場誘惑擺在面前，「安全」就成了一個被集體低估的成本項目。每家公司都在比誰跑得快、誰覆蓋的城市多、誰的訂單量大——但沒有人在比誰的應急機制更完善、誰的失效保護更可靠。

### 監管正在追趕，但還沒追上

中國工信部在 2026 年 2 月發布了[首份強制性自動駕駛安全國家標準草案](https://carnewschina.com/2026/02/26/new-chinese-regulations-push-l3-autonomous-vehicles-closer-to-l4-capabilities-with-enhanced-safety-protocols/)，提出 L3 和 L4 車輛必須具備「最低風險機動」能力——當系統故障或駕駛員無法接管時，車輛必須能自主安全停靠。草案也要求所有自動駕駛車輛安裝類似飛機「黑盒子」的數據記錄系統。

但這份標準預計 2027 年 7 月才會正式實施。在此之前，Robotaxi 企業基本上是在自律的框架下運營。武漢事件證明了一件事：在監管落地之前的真空期，企業的「自律」是不夠的。

---

## 多方觀點

### 樂觀派：系統陣痛，不是結構性問題

百度的支持者會指出，Apollo Go 已經累計完成超過 2,000 萬次服務，而這是第一次大規模系統故障。從統計學角度來看，這仍然是極低的故障率。百度的第六代 Robotaxi RT6 [成本已降至 3 萬美元以下](https://cnevpost.com/2024/05/15/baidu-apollo-launches-6th-gen-robotaxi/)，遠低於 Waymo 早期動輒 20 萬美元的單車成本，這讓大規模商業化變得可行。Apollo Go 甚至在武漢率先實現了[單車運營盈利](https://carnewschina.com/2025/11/13/baidus-apollo-go-robotaxi-leads-global-autonomous-driving-with-17m-orders-targets-profit-this-year/)。

投資市場的反應也相當冷靜。事件發生後，百度（BIDU）在美股[盤後僅微跌 2.7%](https://coincentral.com/baidu-bidu-stock-wuhan-robotaxi-outage-safety-debate-apollo-go/)，隔日甚至小幅反彈。市場顯然將此視為短期波動，而非根本性風險。

### 悲觀派：Cruise 的教訓還不夠深刻嗎？

但反對的聲音同樣有力。市場顧問陳立騰在[接受南華早報採訪](https://www.scmp.com/tech/article/3348654/baidus-robotaxi-breakdown-wuhan-strands-riders-raises-safety-concerns)時指出，這起事件凸顯了營運商在應急響應能力上的嚴重不足，可能促使政府加速收緊監管和營運標準。

更尖銳的批評來自對 Cruise 前車之鑑的類比。通用在 Cruise 上燒掉超過 100 億美元，最終[因為一系列安全事故而全面退出](https://www.cnbc.com/2024/12/10/gm-halts-funding-of-robotaxi-development-by-cruise.html)。Yahoo Finance 的分析指出，Cruise 的失敗根本原因是「擴張太快導致嚴重問題」。百度現在正在走一條驚人相似的路——瘋狂擴張規模、追逐訂單增長，而安全基礎設施的建設跟不上部署的速度。

FreightWaves 的一篇深度分析做了一個殘酷的對比：[自動駕駛卡車公司 Aurora 在商業部署前累積了超過 300 萬英里的安全駕駛測試和 10,000 次有人監督的運輸任務](https://www.freightwaves.com/news/why-robotaxis-keep-failing-while-av-trucks-take-the-slow-road-to-safety)，而 Robotaxi 公司則利用寬鬆的監管在城市中快速部署——「矽谷的顛覆優先心態」vs.「運輸業的安全優先文化」。

### 技術路線之爭：端到端是解藥嗎？

武漢事件也重新點燃了自動駕駛兩大技術路線的論戰。

百度和 Waymo 代表的「規則 AI 派」，依賴高精地圖、數十個感測器和預編程規則來驅動車輛。優勢是確定性——只要場景被定義過，系統表現可預測。但武漢和舊金山的事故證明了致命弱點：一旦遇到系統未預見的情況（網路故障、停電、暴雨），整個車隊可能同時失效。

特斯拉、小鵬和地平線代表的「端到端派」，通過端到端神經網路和海量真實駕駛數據訓練 AI，讓車輛「像人一樣思考」。舊金山停電後，馬斯克第一時間在 X 平台嘲諷 Waymo：「特斯拉 Robotaxi 未受舊金山停電影響。」地平線 CEO 余凱也加入論戰：「很明顯，特斯拉是 AI based，Waymo 還是依賴人工規則和基礎設施。」MotorTrend 在 2026 年 1 月的評測中也將 [Tesla FSD v14 評為市場上最佳的駕駛輔助系統](https://www.notateslaapp.com/software-updates/version/2026.2.9.3/release-notes)。

但端到端也不是萬靈丹。純神經網路系統的「黑盒」特性，意味著你永遠無法完全預測它在極端情況下會做什麼。Tesla FSD 自 2025 年 6 月上線以來也發生了 [14 起事故](https://www.damfirm.com/waymo-accident-statistics.html)。真正的答案，可能不在二選一，而在融合——用端到端模型處理感知和預測，用高精地圖提供安全兜底，實現「算法自主學習 + 地圖安全冗餘」的雙軌架構。

### 我的看法

以我觀察這個產業的經驗，武漢事件最讓我在意的不是系統為什麼故障——任何複雜系統都會故障，這不奇怪。真正讓我在意的是故障之後發生了什麼：SOS 按鈕沒有用、客服不知道狀況、承諾的工作人員沒出現、百度超過 24 小時沒有公開聲明。這代表的不是技術失敗，是組織失敗——一家把「規模」和「訂單增長」放在第一優先的公司，根本沒有為「如果一百輛車同時壞掉怎麼辦」做過認真的準備。

---

## 產業衝擊

### 第一層：百度和中國 Robotaxi 賽道的信任危機

最直接的影響者是百度自己。Apollo Go 正處於從「燒錢換規模」到「證明能賺錢」的關鍵轉折點，[計劃 2026 年實現整體盈利](https://carnewschina.com/2025/11/13/baidus-apollo-go-robotaxi-leads-global-autonomous-driving-with-17m-orders-targets-profit-this-year/)。同時，百度正在積極拓展國際市場——與 Uber、Lyft 簽訂合作，進軍南韓、中東和歐洲。武漢事件不會致命，但它給了百度的國際擴張計畫一個很不好的開場。歐洲的監管機構已經比美國和中國更為嚴格，這類事件會成為反對引入中國 Robotaxi 的有力彈藥。

對競爭對手來說，這既是警訊也是機會。小鵬、文遠知行、小馬智行如果能在安全記錄上拉開差距，就能在消費者信任上贏得先機。但更可能的情況是，整個中國 Robotaxi 產業都會被牽連——一輛百度的車出了事，消費者不會區分品牌，他們會說「無人車不安全」。

### 第二層：商業模式的安全成本重估

武漢事件暴露了一個被所有 Robotaxi 公司刻意忽略的成本項目：安全冗餘。

目前的商業模式邏輯很清晰：去掉人類駕駛員 → 降低成本 → 用低價搶市佔率 → 靠規模實現盈利。百度的 RT6 單車成本不到 3 萬美元，蘿蔔快跑在武漢的定價比一線城市低 30%，比人類網約車更便宜。

但這個模型的前提是「不需要人」。武漢事件證明這個前提是錯的——至少在現階段。你需要雲端安全員即時監控車輛狀態，你需要區域安全員在系統失效時趕到現場，你需要一套像航空業一樣成熟的應急響應體系。這些成本加上去之後，Robotaxi 的單車經濟模型會變得很不一樣。

航空業是最好的類比。飛機的自動駕駛（自動巡航）技術早在 1960 年代就已經成熟，但直到今天，每一架商業航班上仍然有兩名飛行員和一套完整的失效備援系統。這不是因為技術不夠好，而是因為當你承載人命時，「夠好」的標準本身就不一樣。

### 第三層：開發者和技術人才的挑戰

對自動駕駛的工程師來說，武漢事件指向一個尷尬的現實：業界花了太多資源在「讓車跑起來」，太少資源在「讓車安全地停下來」。

失效安全（fail-safe）機制的設計——當系統故障時如何安全靠邊停車、如何通知乘客和交通管理中心、如何啟動備援操控——這些「不性感」的工程問題，在簡報和融資中永遠排在新功能和性能提升後面。但武漢告訴我們，這些才是決定 Robotaxi 能不能從「新奇體驗」升級為「城市基礎設施」的關鍵。

### 第四層：網路安全的噩夢情境

如果說武漢事件是一次「意外」的系統故障就能造成百車癱瘓，那一次「蓄意」的攻擊會怎樣？

[Upstream Security 的 2026 年全球汽車網路安全報告](https://www.prnewswire.com/il/news-releases/ransomware-attacks-on-automotive-and-smart-mobility-more-than-doubled-in-2025-according-to-new-research-by-upstream-security-302691468.html)顯示，針對汽車和智慧移動產業的勒索軟體攻擊在 2025 年翻了一倍以上。[卡巴斯基的 2026 年報告](https://ics-cert.kaspersky.com/publications/blog/2026/02/19/risks-for-the-automotive-industry-in-2026/)更直接警告：自動駕駛車輛的大規模實際運營正在「擴大攻擊面，加速攻擊者的能力」，產生「具有巨大衝擊潛力的大規模網路風險」。

研究人員已經證實，自動駕駛汽車的感知系統極其脆弱——[光達可以被虛假信號欺騙，攝影機可以被特製圖案誤導，V2V 通訊可能被截獲篡改，OTA 更新通道可能被注入惡意程式碼](https://arxiv.org/html/2412.15348v1)。2024 年就有研究團隊通過篡改 OTA 更新，成功讓測試車的 AI 系統降低了「避讓行人」的優先級。

想像一下：一個攻擊者同時劫持數百輛 Robotaxi，讓它們集體堵死城市主幹道、包圍重要設施、阻斷應急通道。武漢事件是一次「意外的預演」——它證明了當一個中央系統出問題時，整個車隊可以在幾分鐘內同時失效。如果這是一次有組織的攻擊，後果將遠比幾個乘客被困高架橋嚴重得多。

---

## 未來展望

### 短期（3-6 個月）：監管收緊和安全投資加碼

武漢事件幾乎確定會加速中國自動駕駛安全標準的立法進程。工信部已經完成的[強制性安全國標草案](https://www.electrive.com/2026/02/26/china-introduces-new-regulations-for-autonomous-driving/)可能會提前推動實施，而不是等到 2027 年。我預期百度會在未來幾週內發布一份「安全升級計畫」，承諾增加雲端安全員配置、完善應急響應機制、建立失效安全的標準作業流程。其他 Robotaxi 企業也會跟進類似的安全承諾，因為誰都不想成為下一個「趴窩」的主角。

短期內，我們可能也會看到保險和責任歸屬的討論浮上檯面。當 Robotaxi 造成事故或故障，責任在車企、還是在平台營運商、還是在地方政府？目前這個灰色地帶需要被釐清。

### 中期（6-18 個月）：技術路線分化加速

**情境一：融合路線崛起。** 最可能的發展是，「純高精地圖 + 規則」和「純端到端」的極端路線都會被修正。未來的 Robotaxi 架構會是混合式的——端到端神經網路負責處理動態場景的感知和決策，高精地圖和規則系統作為安全層提供冗餘保障。百度和 Waymo 會加大端到端的投資，而特斯拉和小鵬可能會開始更認真地對待地圖數據的價值。

**情境二：市場洗牌。** 安全標準的提高會拉升營運成本，缺乏資金和技術深度的二三線玩家可能會被淘汰。中國 Robotaxi 的「五虎爭霸」可能在 18 個月內變成三強鼎立。不是每一家都能同時承擔「規模擴張」和「安全投資」的雙重壓力。

**情境三：國際化放緩。** 百度在南韓、阿聯酋和歐洲的擴張計畫可能會遇到更多阻力。歐盟對自動駕駛的態度本就比美國和中國謹慎，武漢事件會成為歐洲監管機構延遲審批的理由。

### 長期推演：Robotaxi 會成功，但不是以現在這種方式

從 3-5 年的尺度來看，我依然相信 Robotaxi 會成為城市交通的重要組成部分。但它的成功路徑，不會是「先衝規模，再補安全」的矽谷模式，而更可能像航空業——先建立一套極其嚴格的安全標準和監管框架，然後在框架內逐步擴展。

這意味著 Robotaxi 的全面普及時間表可能會比市場預期慢 2-3 年。那些估值模型裡「2030 年全面替代人類網約車」的假設，可能過於樂觀。但當它最終到來時，會比現在更安全、更可靠，也更值得信任。

### 給讀者的建議

**如果你是開發者：** 自動駕駛的下一個招聘熱點不是感知或規劃算法，而是安全工程——失效安全設計、分散式系統韌性、即時監控和異常檢測。如果你正在考慮進入這個領域，安全和可靠性工程是值得深耕的方向。

**如果你是創業者或產品經理：** Robotaxi 的基礎設施層還有大量未被滿足的需求——車隊健康監控系統、乘客應急通訊方案、自動駕駛車輛的保險科技（InsurTech）、監管合規工具。這些「不性感」的基礎設施，可能比再做一家 Robotaxi 公司更有機會。

**如果你是一般消費者：** 短期內不必恐慌，但搭乘 Robotaxi 時請確認自己知道如何手動開門、如何撥打 110 或 119。在自動駕駛的安全基礎設施真正成熟之前，保留一點「不完全信任機器」的警覺性，是明智的。

武漢二環線上那些閃著雙閃燈的「殭屍車」，是一面鏡子。它映照出的不是技術的失敗，而是一個產業的優先順序失調——當所有人都在追逐下一個百萬訂單時，沒有人在問：如果下一次不是一百輛車，而是一萬輛呢？

---

## 延伸閱讀

- [Apollo Go's robotaxi fleet suffers mass paralysis — CarNewsChina](https://carnewschina.com/2026/04/01/apollo-gos-robotaxi-fleet-suffers-mass-paralysis-stranding-passengers-on-elevated-highways/)：事件發生後最完整的英文報導之一，包含乘客親歷和時間線還原
- [Baidu's robotaxi breakdown raises safety concerns — South China Morning Post](https://www.scmp.com/tech/article/3348654/baidus-robotaxi-breakdown-wuhan-strands-riders-raises-safety-concerns)：南華早報的深度報導，包含專家分析和百度未回應的細節
- [Passengers stranded after robotaxi outage — NBC News](https://www.nbcnews.com/world/asia/passengers-stranded-moving-traffic-robotaxi-outage-china-wuhan-rcna266192)：國際主流媒體的報導視角，對中國 Robotaxi 產業的國際觀感有影響力
- [Why robotaxis keep failing while AV trucks take the slow road — FreightWaves](https://www.freightwaves.com/news/why-robotaxis-keep-failing-while-av-trucks-take-the-slow-road-to-safety)：對 Robotaxi vs 自動駕駛卡車安全文化差異的深度對比分析
- [GM exits robotaxi market, shuts down Cruise — CNBC](https://www.cnbc.com/2024/12/10/gm-halts-funding-of-robotaxi-development-by-cruise.html)：Cruise 的失敗史，是理解「擴張太快」後果的最佳案例
- [China introduces mandatory safety standards for autonomous driving — Electrive](https://www.electrive.com/2026/02/26/china-introduces-new-regulations-for-autonomous-driving/)：中國首份強制性自動駕駛安全標準的詳細解析
- [Ransomware attacks on automotive doubled in 2025 — Upstream Security](https://www.prnewswire.com/il/news-releases/ransomware-attacks-on-automotive-and-smart-mobility-more-than-doubled-in-2025-according-to-new-research-by-upstream-security-302691468.html)：自動駕駛車輛網路安全威脅的最新數據
- [Waymo recalls software after school bus failures — NPR](https://www.npr.org/2025/12/06/nx-s1-5635614/waymo-school-buses-recall)：Waymo 校車違規事件的完整報導，是理解「修了又壞」困境的好案例
