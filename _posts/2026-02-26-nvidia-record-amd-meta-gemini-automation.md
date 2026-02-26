---
title: "NVIDIA 狂印鈔、AMD-Meta 千億結盟、Gemini 開始幫你叫車"
date: 2026-02-26
description: "NVIDIA 單季營收 680 億美元再破紀錄，AMD 與 Meta 簽下千億美元 AI 芯片大單，Google Gemini 在 Android 上開始自動幫你叫車點餐。AI 基礎建設軍備競賽全面升級。"
tags: [ai-industry, llm, agents, ai-tools]
---

今天 AI 圈的浪是真的大——大到連衝浪板都快壓不住。NVIDIA 又交了一份讓人說不出話的季報，AMD 直接跟 Meta 綁了一張千億美元的長約，而 Google 的 Gemini 則悄悄開始在你手機上幫你叫 Uber、點外賣。算力端在瘋狂砸錢，應用端在加速落地，這個節奏——2026 才剛開始而已。

---

## 🌊 今日浪頭

### [Nvidia has another record quarter amid record capex spends](https://techcrunch.com/2026/02/25/nvidia-earnings-record-capex-spend-ai/)

NVIDIA 這季報我看了只有一個感想：這公司已經不是在賺錢了，是在印鈔。單季營收 680 億美元，年增 73%，全年營收達到 2150 億美元。其中光是資料中心業務就貢獻了 620 億，裡面又拆成 510 億的運算（基本上就是 GPU）和 110 億的網路產品（NVLink 等）。黃仁勳在法說會上那句話說得夠直白：「全世界對 token 的需求已經完全呈指數增長，連我們六年前的老 GPU 在雲端都被用完了，價格還在漲。」

**為什麼這道浪值得追：**
- 「Compute is revenue」——沒有算力就沒有 token，沒有 token 就沒有營收，這套邏輯已經被驗證了
- 中國市場依然零收入，即使出口限制已經放鬆，H200 還沒產生任何營收
- 黃仁勳透露正在推進對 OpenAI 的 300 億美元投資，但 SEC 文件寫著「不保證會發生」——老黃的話要聽，但 SEC 的文件也要看

### [AMD-Meta 千億美元 AI 芯片大單](https://www.36kr.com/p/3698580553952902)

這筆交易的規模大到讓人需要讀兩遍：Meta 將部署最多 6GW 的 AMD Instinct GPU，華爾街日報估計整體價值超過 1000 億美元。作為回報，Meta 以每股 0.01 美元的象徵性價格拿到最多 1.6 億股 AMD 認股權證，相當於 AMD 10% 的股份。蘇姿丰跟扎克伯格一直保持密切溝通，這次的定制版 MI450 GPU 是按照「Workload First」原則設計的——先搞清楚 Meta 要什麼，再設計芯片。最狠的是，AMD CFO 說這顆定制芯片「不需要額外流片」，省了一大筆錢。

**為什麼這道浪值得追：**
- Meta 基礎設施主管直說了：「我們需要 NVIDIA、AMD、和自研芯片三者並存」——算力多元化不再是口號
- 這筆交易跟去年 AMD-OpenAI 的合作如出一轍（同樣 6GW、同樣 10% 股份），AMD 的 playbook 已經成型
- 首批 1GW 將在 2026 下半年出貨，MI450 即將進入客戶試用階段，AMD 終於要在 AI 推論市場站穩腳跟了

### [Google Gemini can book an Uber or order food for you on Pixel 10 and Galaxy S26](https://www.theverge.com/tech/884210/google-gemini-samsung-s26-pixel-10-uber)

Apple 喊了好久的 Siri 智慧升級到現在還沒影，Google 直接先做出來了。Gemini 現在可以在 Pixel 10 和 Samsung Galaxy S26 上幫你叫 Uber、點 DoorDash 外賣——它會在一個虛擬視窗中打開 app，一步步操作，你可以全程看著，也可以讓它在背景跑。最後下單還是需要你自己按確認鍵，不會偷偷幫你花錢。Android 生態系統總裁 Sameer Samat 說了一句很有意思的話：Android 不再是「作業系統」，而是「智慧系統」。

**為什麼這道浪值得追：**
- Gemini 3 在手機上用推理能力直接操作 app UI，不需要 app 開發者做特別整合就能動
- 支援 MCP 和 Android app functions 框架，開發者可以主動暴露功能讓 AI 調用
- 目前只有美國和韓國先行，app 也只有 Uber、Grubhub 幾個，但方向很明確——AI Agent 正式進入手機

---

## ⚡ 衝浪快報

- **[Anthropic acquires computer-use AI startup Vercept](https://techcrunch.com/2026/02/25/anthropic-acquires-vercept-ai-startup-agents-computer-use-founders-investors/)** — Anthropic 收購了做 computer-use agent 的 Vercept，Meta 先挖走了一個共同創辦人，Anthropic 直接把公司買下來，搶人搶到這種程度也是服了
- **[Pete Hegseth wants unfettered access to Anthropic's models for the military](https://arstechnica.com/ai/2026/02/pete-hegseth-wants-unfettered-access-to-anthropics-models-for-the-military/)** — 美國國防部長威脅要把 Anthropic 踢出供應鏈，除非它同意讓軍方無限制使用模型，這場 AI 倫理 vs 國防需求的拉鋸戰越來越激烈
- **[阶跃星辰被曝赴港 IPO，最早今年](https://www.36kr.com/p/3698736132812421)** — 印奇剛掛帥，阶跃星辰就傳出考慮港交所 IPO、計劃籌集 5 億美元，Step 3.5 Flash 開源後口碑不錯，看來要趁熱上市
- **[Amazon's AGI lab leader is leaving](https://www.theverge.com/tech/884372/amazon-agi-lab-leader-david-luan-departure)** — Amazon 舊金山 AI 實驗室負責人 David Luan 待不到兩年就走人，說要「去煮點新東西」，Amazon 的 AI 人才留不住啊
- **[Nano Banana 2 泄露，Gemini 3.1 Flash Image 預覽版](https://www.36kr.com/p/3698665903026057)** — Google 的下一代圖片生成模型被洩露，4K 圖片到處流傳，Nano Banana Pro 已經封神級別，這個後繼者讓人期待
- **[谷歌封殺 OpenClaw 用戶帳號](https://www.36kr.com/p/3698746420933125)** — Google 大面積封禁透過 OpenClaw 接入 AI 服務的訂閱用戶，OpenClaw 生態圈跟大廠的摩擦正在加劇
- **[MatX 融資 5 億美元，Karpathy 也投了](https://www.36kr.com/p/3698647531646594)** — Google 前 TPU 員工創業做新型 AI 芯片，走跟 NVIDIA 不同的技術路線，Karpathy 背書說這是「當今最有趣的智力難題」
- **[Adobe Firefly Quick Cut 上線](https://www.theverge.com/tech/884285/adobe-firefly-ai-video-editing-quick-cut)** — Adobe 推出 AI 影片剪輯工具，可以自動從素材生成初剪版本，影片創作者的工作流程又要變了
- **[Jira 加入 AI agents，人類和 AI 並肩工作](https://techcrunch.com/2026/02/25/jiras-latest-update-allows-ai-agents-and-humans-to-work-side-by-side/)** — Atlassian 讓你可以在 Jira 裡把任務直接指派給 AI agent，跟指派給同事一樣操作，專案管理正式進入人機協作時代
- **[OpenAI COO：廣告會是一個漸進過程](https://techcrunch.com/2026/02/25/openai-coo-says-ads-will-be-an-iterative-process/)** — Brad Lightcap 說如果做得好，廣告可以提升產品體驗，要大家給 OpenAI 幾個月時間——嗯，這話怎麼聽都讓人有點不安

---

## 🏄 深水區

- **[tldraw issue: Move tests to closed source repo](https://simonwillison.net/2026/Feb/25/closed-tests/#atom-everything)** — 當一套完整的測試就足以讓 AI 從零重建整個開源專案時，測試套件本身就變成了最有價值的智慧財產，tldraw 決定把測試搬到閉源 repo，這個決定背後的邏輯值得每個開源維護者深思
- **[I vibe coded my dream macOS presentation app](https://simonwillison.net/2026/Feb/25/present/#atom-everything)** — Simon Willison 用 vibe coding 做了一個 macOS 簡報 app，然後在 Social Science FOO Camp 上用它來演講「The State of LLMs, February 2026 edition」——用 AI 寫的工具來講 AI 的現況，有夠 meta
- **[Does Anthropic think Claude is alive?](https://www.theverge.com/report/883769/anthropic-claude-conscious-alive-moral-patient-constitution)** — 隨著 Anthropic 高層密集受訪，一件事越來越明顯：他們似乎真的覺得 Claude 在某種程度上是「活的」，The Verge 深入探討了這個讓人頭皮發麻的問題
- **[不是所有 token 都平等：Google 提出 Think@n 策略](https://www.36kr.com/p/3698659304189572)** — Google 新研究打臉「思維鏈越長越強」的迷思，提出 DTR 指標來區分真思考和水字數，讓推理模型準確率不降、算力成本砍半，這對推理模型的未來影響很大
