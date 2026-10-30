# 作品與筆記

我是 Tommy，做技術產品規劃，也自己寫程式。近期的作品包含學習工具、AI 功能和自動化。這裡整理可以公開的程式與開發取捨。

[LinkedIn](https://www.linkedin.com/in/chia-en/) · [English](README.md)

## 近期實作

### [社群任務平台](cases/quest-platform/README.zh-TW.md)

從參與者提交證明，到後台審核、積分與例外處理。案例包含回應遺失後的重試、附件權限，以及在新環境檢查交付包的過程。

### [現貨交易介面](cases/spot-interface/README.zh-TW.md)

供產品審查的 React Native 示範版，包含本機訂單狀態與錢包切換。案例說明舊狀態覆蓋的問題，以及分開記錄的 iOS、Android 驗證。所有交易均為模擬。

這兩份是匿名案例。實作、客戶素材和交付檔維持私有。

## 公開作品

### [TOEFL Vocab](https://github.com/asdc163/toefl-vocab)

離線單字學習 App，搭配間隔複習。Gemini 負責選配的解釋與內容生成；詞庫和複習流程不需要模型金鑰。我把這兩部分分開，讓學習的主要任務不被供應商狀態綁住。

[模型串接與錯誤處理](docs/ai-capability-evidence.zh-TW.md#toefl-vocab)

### [PM Signal Lab](https://github.com/asdc163/pm-signal-lab)

把產品筆記整理成可討論的決策。[AI 發布審查練習](https://github.com/asdc163/pm-signal-lab/tree/main/playbooks/ai-launch-review)有一個具體問題：回答擅自批准退款，是否應該擋下試行？來源規則、範例回覆和評分標準都能直接讀，也可以對決定提出異議。這是一份虛構練習。

### [OpenClaw Dashboard](https://github.com/altoslab447/openclaw-dashboard)

在本機集中查看 agent 工作區的任務、排程、設定與日誌。我保留唯讀界線，查看狀態不會順便取得執行動作的入口。

其他程式：[CareLens](https://github.com/asdc163/carelens)，包含 Claude 圖片輸入與無 key mock 的原型；[ethers-v6-codemod](https://github.com/asdc163/ethers-v6-codemod)，以 AST 處理 JavaScript 遷移的工具。

## 商用案例

- [Telegram 社群 Bot](https://github.com/asdc163/telegram-community-bot-case-study)：群內參與、群主私訊管理與投遞恢復。
- [VPN 訂閱系統](https://github.com/asdc163/vpn-subscription-case-study)：付款核對、續費，以及客戶端使用資格。

公開的是工程案例。商用原始碼、客戶身分和營運資料保留私有；各案例另外列出交付狀態與驗證紀錄。

## 筆記

- [JSON 格式正確，內容仍然可能錯](notes/structured-output.zh-TW.md)
- [產品取捨](docs/tpm-review-guide.zh-TW.md)
- [AI 實作筆記](docs/ai-capability-evidence.zh-TW.md)

[開發方式](docs/how-i-build.md) · [公開原則](docs/publication-policy.md)
