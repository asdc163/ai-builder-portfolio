# Tommy | Technical Product Manager & AI Builder

我的主軸是技術產品規劃與開發：從使用者問題收斂第一版，再處理產品流程、模型整合、品質評估與工程交接。這份作品集把產品取捨和能檢查的 AI 技術證據放在一起。

[AI 能力與程式證據](docs/ai-capability-evidence.zh-TW.md) · [TPM 閱讀指南](docs/tpm-review-guide.zh-TW.md) · [English](README.md)

## 先看可以檢查的證據

- **模型串接：** TOEFL Vocab 有伺服器端 Gemini handler、JSON 回覆格式請求、逾時與上游錯誤處理，核心學習流程不依賴 AI。CareLens 則探索圖片轉結構化資料，使用 Claude 和執行期 schema 檢查。
- **AI 評估設計：** PM Signal Lab 提供來源規則、失敗案例、評分標準與發布決策範本。範例回覆是人工撰寫的練習材料。
- **技術交付：** 商用案例呈現付款狀態、即時角色授權、結果不明的投遞，以及移交責任的處理方式。實際程式與營運資料保留私有。

[能力證據頁](docs/ai-capability-evidence.zh-TW.md)把每個主張連到固定版本的公開檔案，也標示證據能支持到哪裡。

## 精選作品

| 作品 | 適合檢查什麼 | 狀態與範圍 |
| --- | --- | --- |
| [PM Signal Lab](https://github.com/asdc163/pm-signal-lab) | AI 評估案例、重大失敗判斷、來源對照與 PM skills。 | 公開練習與瀏覽器工作表，不當作模型實測成績。 |
| [TOEFL Vocab](https://github.com/asdc163/toefl-vocab) | Gemini 串接、結構化回覆請求、上游錯誤與離線學習核心。 | 公開程式；本次未重測供應商或學習成效。 |
| [CareLens](https://github.com/asdc163/carelens) | 圖片上傳、權限查核、Claude 請求與 Zod 解析。 | 多模態原型，有未設定 key 時的 mock 路徑，不宣稱臨床可靠性。 |
| [Telegram 社群 Bot](https://github.com/asdc163/telegram-community-bot-case-study) | 角色界線、持久化投遞、異常處理與擁有權交接。 | 匿名商用案例，程式與營運資料不公開。 |
| [VPN 訂閱系統](https://github.com/asdc163/vpn-subscription-case-study) | 訂閱帳務、客戶端協調、跨系統依賴及發布驗收。 | 匿名工程交付案例，正式營運另需證據。 |
| [OpenClaw Dashboard](https://github.com/altoslab447/openclaw-dashboard) | agent 工作區的本機可視性，以及唯讀操作界線。 | 位於我維護的另一個帳號，不執行 agent 動作。 |

## 技術產品經理的閱讀角度

[TPM 閱讀指南](docs/tpm-review-guide.zh-TW.md)把作品連到使用者問題、第一版範圍、技術取捨、驗收問題與交接界線。面談時可以挑一個問題深入談，例如「同一筆付款重播怎麼辦」或「Bot 發送結果不明時是否應該重送」。

我用 AI 協作開發，也依工作需求實作模型功能。Telegram 與 VPN 的產品邏輯採確定性規則，AI 的角色是協助工程工作。

## 聯絡與合作

技術職務交流可以從能力證據頁開始，再選一個案例討論。產品想法或操作問題可透過[公開專案詢問](https://github.com/asdc163/ai-builder-portfolio/issues/new?template=project-inquiry.yml)描述可公開的部分；憑證、客戶資料、預算與商業文件請勿放入 issue。

[開發方式](docs/how-i-build.md) · [公開原則](docs/publication-policy.md)

本次於 2026-10-28 對照公開程式版本與既有私有案例紀錄整理，沒有重新呼叫模型、啟動商用服務或執行各產品。
