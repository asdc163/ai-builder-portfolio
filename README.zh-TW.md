# Tommy 的產品作品

Technical Product Manager · AI Builder

我做學習工具、自動化與選配 AI 功能。這裡整理產品決策如何落到實作、驗收及交接。

[AI 實作](docs/ai-capability-evidence.zh-TW.md) · [產品畫面](media/README.zh-TW.md) · [LinkedIn](https://www.linkedin.com/in/chia-en/) · [English](README.md)

<a href="media/toefl-vocab/word-detail.png"><img src="media/toefl-vocab/word-detail.png" width="185" height="251" alt="TOEFL Vocab：無金鑰的字義與詞性家族流程"></a> <a href="media/node-interface/android-network.png"><img src="media/node-interface/android-network.png" width="208" height="251" alt="節點網路：歷史 Android 元件，識別碼與數值已移除"></a>

畫面分別是 TOEFL 的無金鑰字典流程，以及歷史 Android 節點元件。[圖庫](media/README.zh-TW.md)保留日期、平台及去識別說明。

## 公開程式與 AI 評估

**[TOEFL Vocab](https://github.com/asdc163/toefl-vocab)** 的查字與間隔複習不依賴模型金鑰，Gemini 用來擴充學習素材。[實作筆記](docs/ai-capability-evidence.zh-TW.md#toefl-vocab)說明模型整合與錯誤處理。

**[PM Signal Lab](https://github.com/asdc163/pm-signal-lab)** 把來源觀察連到產品決策。[AI 上線審查練習](https://github.com/asdc163/pm-signal-lab/tree/main/playbooks/ai-launch-review)附有政策、自編回覆與評分規則；其中一筆無依據的退款核准，足以暫停虛構的試點。

## 近期實作

| 案例 | 介面背後的決定 |
| --- | --- |
| [節點服務手機介面](cases/node-interface/README.zh-TW.md) | 把可嵌入的 React Native 模組與驗收宿主分開，並在確認前重新檢查報價。 |
| [社群任務平台](cases/quest-platform/README.zh-TW.md) | 保留送件與補件狀態、限制附件存取，並避免重試時重複發點。 |
| [現貨交易介面](cases/spot-interface/README.zh-TW.md) | 修正錢包切換時的舊狀態競態，交付 iOS、Android 原生工程；交易均為模擬。 |

以上為匿名工程案例，各自交代我的工作、交付範圍與驗證界線。商用原始碼和客戶資料維持私有。

## 商用系統

- [Telegram 社群營運機器人](https://github.com/asdc163/telegram-community-bot-case-study)：社群參與、群主私訊管理，以及投遞結果不明時的恢復。
- [VPN 訂閱系統](https://github.com/asdc163/vpn-subscription-case-study)：結帳、付款對帳、續費與客戶端權限。

## 筆記

- [JSON 格式正確，內容仍然可能錯](notes/structured-output.zh-TW.md)
- [產品取捨](docs/tpm-review-guide.zh-TW.md)

其他程式：[OpenClaw Dashboard](https://github.com/altoslab447/openclaw-dashboard)，本機唯讀代理工作區看板；[CareLens](https://github.com/asdc163/carelens)，具備無金鑰 mock 的圖片輸入原型；[ethers-v6-codemod](https://github.com/asdc163/ethers-v6-codemod)，AST 程式遷移工具。

[開發方式](docs/how-i-build.md) · [公開政策](docs/publication-policy.md) · [網站素材](media/WEBSITE-HANDOFF.md)
