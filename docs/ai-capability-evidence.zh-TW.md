# AI 實作筆記

模型相關的程式可以直接讀。以下是我會先看的幾個位置。

[English](ai-capability-evidence.md) · [作品](../README.zh-TW.md)

## TOEFL Vocab

[Gemini helper](https://github.com/asdc163/toefl-vocab/blob/f62588e785d07d948d625f225ff3b8eb3c7daada/lib/gemini.ts)負責伺服器端請求、JSON schema、逾時和回覆解析。[API route](https://github.com/asdc163/toefl-vocab/blob/f62588e785d07d948d625f225ff3b8eb3c7daada/api/ai/%5Baction%5D.ts)分開處理 AI 未啟用、輸入不符與供應商錯誤。

我把生成做成選配，沒設定模型金鑰也能使用詞庫和複習。schema 請求與 JSON 解析處理的是整合格式，單字內容正不正確仍要另外檢查。

## CareLens

[圖片 API](https://github.com/asdc163/carelens/blob/828ec6d9ea46ba61b1ff8d9d4fe82706d62ae4a2/src/app/api/ocr/route.ts)先檢查登入、目標資料存取權、檔案大小與圖片類型。[Claude helper](https://github.com/asdc163/carelens/blob/828ec6d9ea46ba61b1ff8d9d4fe82706d62ae4a2/src/lib/claude.ts)送出圖片與文字，再用 Zod 解析回覆。沒設定 key 時，走的是固定 mock。

這是多模態原型。confidence 是模型產生的欄位，臨床正確性未經驗證。[JSON 格式正確，內容仍然可能錯](../notes/structured-output.zh-TW.md)說明了結構檢查與內容檢查的差別。

## PM Signal Lab

[發布審查練習](https://github.com/asdc163/pm-signal-lab/tree/90f181243266c4d2f57a571201831492bac0e6ba/playbooks/ai-launch-review)包含虛構規則、人工撰寫的回覆與評分標準。一則回答超出了助手權限，因此範例決定暫停試行，再安排下一輪評估。

這裡呈現評估設計。範例分數來自練習，不是某個模型的實測成績。

## Agent 工具

[OpenClaw Dashboard](https://github.com/altoslab447/openclaw-dashboard/blob/486642d86193ab0f3a4ad9036a8859767be9b5e0/README.md)在本機顯示工作區狀態，不執行 agent 動作。repo 另有 [build 與 proof 指令](https://github.com/altoslab447/openclaw-dashboard/blob/486642d86193ab0f3a4ad9036a8859767be9b5e0/.github/workflows/proof.yml)。

程式版本於 2026-10-28 檢視。本次沒有執行模型、產品或 CI；品質、成本、延遲與使用成效需要個別留下紀錄。
