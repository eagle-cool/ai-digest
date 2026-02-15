---
title: "豆包 2.0 數學拿金牌、Blackwell 推論成本砍 10 倍、斯坦福小鎮團隊拿一億美金創業"
date: 2026-02-15
description: "字節跳動豆包大模型 2.0 拿下 IMO 金牌超越 Gemini 3 Pro，NVIDIA Blackwell 讓開源模型推論成本降 10 倍，斯坦福小鎮團隊成立 Simile 獲李飛飛和 Karpathy 投資。"
tags: [llm, agents, ai-industry, mlops]
---

今天的浪很有意思——字節跳動終於把豆包的底層大模型搬出來亮相了，而且一出手就是 IMO 金牌等級的數學能力。另一邊 NVIDIA 秀了一波 Blackwell 的推論經濟學，開源模型跑在上面成本直接砍到十分之一。最讓我眼前一亮的是斯坦福小鎮那幫人居然出來創業了，拿了一億美金要做 AI Agent 的大規模社會模擬——《西部世界》的劇本正在加載中。

---

## 🌊 今日浪頭

### [ByteDance Doubao-Seed-2.0: 豆包大模型 2.0 正式發布](https://seed.bytedance.com/en/blog/seed2-0-%E6%AD%A3%E5%BC%8F%E5%8F%91%E5%B8%83)

字節跳動把豆包的底層引擎換了——Seed 2.0 分成 Pro、Lite、Mini 三個尺寸加一個 Code 專用版，定位是「真實世界複雜任務」的系統性優化。Pro 旗艦版拿下了 IMO、CMO 數學競賽和 ICPC 程式設計競賽的金牌成績，在 Putnam 測試上甚至超過了 Gemini 3 Pro。

我覺得最值得注意的不只是 benchmark 數字，而是它的定價策略——官方說成本比同級競品便宜「大約一個數量級」。在 GPT-5.2 和 Gemini 3 Pro 打得火熱的時候，字節用價格戰直接切入企業市場。多模態方面也很猛：文件理解、長文本推理、影片理解都拿到頂尖分數，在 SuperGPQA 科學知識評測上超過 GPT-5.2。

**為什麼這道浪值得追：**
- IMO/ICPC 金牌等級的數學與推理能力，Putnam 測試超越 Gemini 3 Pro——這不是追趕，是正面對決
- 定價便宜一個數量級，字節明擺著要用價格戰搶企業 AI 市場
- 多模態全面升級：影片理解超越人類水準、長文本推理全面領先，Pro/Lite/Mini 三級部署很實用

### [Inference Providers Cut AI Costs by 10x with Open Source Models on Blackwell](https://blogs.nvidia.com/blog/inference-open-source-models-blackwell-reduce-cost-per-token/)

NVIDIA 這篇不是在秀硬體規格，是在講「推論經濟學」——Baseten、DeepInfra、Fireworks AI、Together AI 四家主要推論服務商用 Blackwell 跑開源模型，每個 token 的成本比 Hopper 世代砍掉最多 10 倍。

具體案例很有說服力：醫療 AI 公司 Sully.ai 把推論成本砍了 90%，回應時間快了 65%，已經幫醫生省回超過 3000 萬分鐘的行政時間。遊戲公司 Latitude 用 DeepInfra 跑 MoE 模型，每百萬 token 從 20 美分降到 5 美分，4 倍成本改善。客服平台 Decagon 透過 Together AI 把每次語音互動成本降了 6 倍，延遲壓到 400 毫秒以下。

關鍵技術是 NVFP4 低精度格式加上 TensorRT-LLM 和 NVIDIA Dynamo 推論框架的組合拳。而且 NVIDIA 已經在預告下一代 Rubin 平台會再帶來 10 倍的效能提升——推論成本的下降速度可能比我們想的還快。

**為什麼這道浪值得追：**
- 開源模型 + Blackwell = 比閉源模型便宜 10 倍的推論成本——這會徹底改變 AI 部署的經濟模型
- 四個真實案例（醫療、遊戲、Agent、客服）證明這不是實驗室數字，是生產環境的實際降幅
- Rubin 平台預告再砍 10 倍——推論成本的 Moore's Law 正在成形

### [Simile: 斯坦福小鎮團隊創業，李飛飛和 Karpathy 都投了](https://www.jiqizhixin.com/articles/2026-02-14-3)

還記得 2023 年那個讓 25 個 AI Agent 在虛擬小鎮裡生活的「斯坦福小鎮」嗎？那篇論文直接把《西部世界》的概念拉進了現實。現在核心團隊出來創業了——新公司叫 Simile，剛完成一億美元融資，投資人陣容很猛：李飛飛和 Karpathy 都在裡面。

Simile 要做的事情聽起來很科幻但其實很實用：用 AI Agent 大規模模擬人類行為。想像一下，你要推出一個新產品，不用做市場調查、不用找焦點團體，直接讓一千個 AI Agent 模擬你的目標用戶群，看他們會怎麼反應。這種「社會模擬即服務」的定位，把 Agent 從「工具」變成了「實驗對象」。

論文作者 Joon Sung Park 在 X 上正式官宣了公司成立。從學術論文到一億美金的公司，這個轉化速度本身就說明了市場對 AI Agent 模擬的胃口有多大。

**為什麼這道浪值得追：**
- 斯坦福小鎮核心團隊 + 李飛飛 + Karpathy 投資——AI Agent 模擬領域的頂配組合
- 一億美元融資規模說明 VC 對 Agent 社會模擬的信心不是一般的強
- 「社會模擬即服務」可能是 AI Agent 最被低估的應用方向——產品測試、政策模擬、城市規劃都用得上

---

## ⚡ 衝浪快報

- **[Google says attackers used 100k+ prompts to try to clone AI chatbot Gemini](https://www.nbcnews.com/tech/security/google-gemini-hit-100000-prompts-cloning-attempt-rcna258657)** — 有人用超過十萬個 prompt 試圖複製 Gemini 的行為模式，AI 模型的「知識產權」保護戰開打了
- **[Ask HN: What explains the recent surge in LLM coding capabilities?](https://news.ycombinator.com/item?id=47019798)** — HN 上的熱議：LLM 寫程式能力最近是不是又跳了一級？很多人覺得這次是真的拐點，不只是 hype
- **[Stoat removes all LLM-generated code following user criticism](https://github.com/orgs/stoatchat/discussions/1022)** — 開源專案 Stoat 在用戶批評後把所有 LLM 生成的 code 全部移除——62 則留言的激烈討論，反映了社群對 AI 生成程式碼品質的信任危機
- **[AI 用 RL 系統突破 300 年亲吻数难题](https://www.jiqizhixin.com/articles/2026-02-14-7)** — 國產 RL 系統在多個維度刷新了 kissing number 的紀錄，AI + 數學的結合又下一城
- **[多模態 Deep Research 終於有了可核驗的評測標準](https://www.jiqizhixin.com/articles/2026-02-14-6)** — MMDeepResearch-Bench 把 Deep Research 的評測從「讀起來不錯」拉到「過程可核驗、證據可追溯」——該有人治治那些只會編的模型了
- **[Agent-evals: Metacognitive scoring for LLM coding agents](https://thinkwright.ai/agent-evals)** — LLM coding agent 的元認知評測框架，不只看輸出對不對，還看推理過程合不合理
- **[AMD Ryzen AI Max+ Strix Halo + ROCm 7.0 效能測試](https://www.phoronix.com/review/amd-rocm-7-strix-halo)** — AMD 在本地 AI 推論的生態系越來越完整了，ROCm 7.0 對 Strix Halo 的支援值得關注
- **[Off Grid: 在手機上離線跑 AI](https://github.com/alichherawalla/off-grid-mobile)** — 開源 app 讓你的手機 GPU 不再閒置，文字生成、圖片辨識全部離線搞定——隱私至上的人會愛這個
- **[Two different tricks for fast LLM inference](https://www.seangoedecke.com/fast-llm-inference/)** — 兩個加速 LLM 推論的實用技巧，寫得簡潔有料
- **[LLM Alignment/Hallucinations Can't Be Fixed – Proof](https://github.com/moketchups/permanently-jailbroken)** — 有人試圖用數學方式證明 LLM 的對齊和幻覺問題「不可修復」——結論很大膽，論證值得看看

---

## 🏄 深水區

- **[騰訊混元 RLVR 訓練崩潰定位：GradLoc 異常梯度定位器](https://www.jiqizhixin.com/articles/2026-02-14-4)** — 如果你在搞大模型的 RLVR 訓練，這篇值得花時間讀：把全局梯度突刺定位到具體的 token 上，從「訓練炸了」變成「知道為什麼炸」，降低 RLVR 研究的工程壁壘
- **[The new AI playbook: why LLM-native beats traditional ML in verticals](https://chrislovejoy.me/llm-native-vs-traditional-ml)** — 垂直領域到底該用傳統 ML 還是直接上 LLM？這篇從第一性原理分析了 LLM-native 方案在哪些場景已經碾壓傳統方法
- **[SnowBall: Iterative Context Processing When It Won't Fit in the LLM Window](https://enji.ai/tech-articles/snowball-iterative-context-processing/)** — 當你的 context 塞不進 LLM 的視窗怎麼辦？SnowBall 的迭代處理方案提供了一個實用的工程解法
- **[AI Bubble Fears Are Creating New Derivatives](https://www.bloomberg.com/news/articles/2026-02-14/ai-bubble-fears-are-creating-new-derivatives-credit-weekly)** — 華爾街開始用衍生品來對沖 AI 泡沫風險了——當金融市場開始做空你的浪，代表這道浪夠大，也代表有人覺得它快要碎了
