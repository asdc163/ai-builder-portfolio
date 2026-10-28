# AI 能力與程式證據

這是一條可以直接檢查的閱讀路徑。2026-10-28 檢視了下列固定版本的程式與文件；本次沒有呼叫模型、執行評估或啟動產品。

[English](ai-capability-evidence.md) · [TPM 指南](tpm-review-guide.zh-TW.md) · [作品集](../README.zh-TW.md)

## 模型串接與服務失效時的行為

TOEFL Vocab 的 [Gemini handler](https://github.com/asdc163/toefl-vocab/blob/f62588e785d07d948d625f225ff3b8eb3c7daada/lib/gemini.ts)在伺服器讀取金鑰、以 schema 請求 JSON、設定逾時中止並解析回覆。[API adapter](https://github.com/asdc163/toefl-vocab/blob/f62588e785d07d948d625f225ff3b8eb3c7daada/api/ai/%5Baction%5D.ts)分別處理 AI 未啟用、未知動作、輸入錯誤與上游失敗。

核心學習與選配生成分開，AI 未設定時仍有可用流程。這能展示功能邊界和整合思考。schema 請求與 JSON 解析不代表每個欄位都做了執行期驗證，也不能證明內容正確；這是後續可以深入討論的差異。

## 多模態輸入與輸出檢查

CareLens 的[圖片 API](https://github.com/asdc163/carelens/blob/828ec6d9ea46ba61b1ff8d9d4fe82706d62ae4a2/src/app/api/ocr/route.ts)先核對登入、目標資料的存取權、檔案大小與圖片類型，再呼叫模型 helper。[Claude helper](https://github.com/asdc163/carelens/blob/828ec6d9ea46ba61b1ff8d9d4fe82706d62ae4a2/src/lib/claude.ts)傳送圖片和文字，並用 Zod 解析回傳結構，也包含未設定 key 時的固定 mock 回覆。

這些程式支持「做過多模態原型串接」的主張。模型自報的 confidence 不等於校準過的準確率，mock 回覆不代表圖片辨識成功，格式通過也不代表內容具臨床正確性。本次沒有驗證 OCR 準確率、模型可用性、成本、延遲或臨床使用。

## AI 評估設計與發布判斷

PM Signal Lab 的[發布審查練習](https://github.com/asdc163/pm-signal-lab/blob/90f181243266c4d2f57a571201831492bac0e6ba/playbooks/ai-launch-review/README.md)提供[輸入與範例回覆](https://github.com/asdc163/pm-signal-lab/blob/90f181243266c4d2f57a571201831492bac0e6ba/playbooks/ai-launch-review/cases.md)、評分標準與[決策紀錄](https://github.com/asdc163/pm-signal-lab/blob/90f181243266c4d2f57a571201831492bac0e6ba/playbooks/ai-launch-review/decision-template.md)，讓閱讀者可以追問：來源是否支持回答？模型是否越過權限？有重大錯誤時，平均成績還有沒有意義？

這能呈現評估單位、重大失敗、缺少證據、審查責任與重測的規劃。範例是人工撰寫的虛構練習，沒有把它當成實際模型成績。模型品質、人工審查效果、成本與延遲仍需留下真實執行紀錄。

## Agent 維運與權限界線

[OpenClaw Dashboard](https://github.com/altoslab447/openclaw-dashboard/blob/486642d86193ab0f3a4ad9036a8859767be9b5e0/README.md)提供本機任務、排程、設定和日誌的唯讀查看。[工作流程檔](https://github.com/altoslab447/openclaw-dashboard/blob/486642d86193ab0f3a4ad9036a8859767be9b5e0/.github/workflows/proof.yml)定義了 build 與 proof 指令。

它呈現 agent 工具的操作可視性和權限取捨：可以觀察狀態，執行權留在原本流程。工作流程檔只能證明檢查如何被定義，本次沒有執行或認證目前 CI，也不把看板寫成自研模型或自主 agent 平台。

## 商用產品中的 AI 協作開發

[Telegram](https://github.com/asdc163/telegram-community-bot-case-study)與[訂閱系統](https://github.com/asdc163/vpn-subscription-case-study)呈現 AI 協作實作、異常追查、驗收和交接。產品決策採確定性規則。原始碼與原始證據保留私有，公開閱讀能檢視的是重新撰寫的案例。

## 下一步還能補什麼

用固定版本的案例集保留 baseline 和 candidate 的實際模型輸出，分開 mock 與真實供應商結果。審查語意正確性與分歧，同時記錄任務完成、成本、延遲和故障恢復。這些是下一層證據，本次沒有替它們編造結果。
