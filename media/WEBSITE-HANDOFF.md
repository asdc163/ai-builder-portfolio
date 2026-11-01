# 個人網站素材使用方式

作品資料集中在 [portfolio.json](../portfolio.json)。圖片、圖說和公開案例放在同一份 repository，之後可以直接複製到網站的內容目錄。

## 先接這兩類內容

- `projects`：中英文名稱、摘要、使用者工作、我的貢獻、關鍵取捨、AI 範圍、交付狀態、技術與證據限制。
- `assets`：相對路徑、原生尺寸、中英文替代文字與圖說、拍攝日期、平台、處理方式及檔案雜湊。

把 `portfolio.json` 與整個 `media/` 放在相同內容根目錄。`assets[].path` 都從這個根目錄解析；在網站產生圖片 URL 時，加上網站的內容路徑即可。不要把 GitHub 的檔案瀏覽頁當成圖片 URL。

每個專案的 `imageIds` 對應 `assets[].id`。`coverImageId` 只選可作為封面的圖；值為 `null` 時，不要自動拿第一張圖補上。

## 圖片與文字一起使用

先用 `summary` 說清楚產品，再用 `contribution` 與 `decision` 說明我的工作。呈現 AI 能力時讀取 `aiScope`，避免把確定性自動化寫成模型功能。完整說明仍連回 `caseUrl`。

網站圖片使用 `alt` 與可見的 `caption`，並帶入 `width`、`height`，避免載入時跳動。保留原圖比例；功能表單、彈窗與響應測試圖不適合一律裁成橫幅。

只有需要縮圖時才另產生衍生檔。衍生圖的輸入必須是這裡已去識別的公開圖片；保留原 PNG，讓詳細頁能開啟原尺寸。公開圖的中繼資料已移除，遮罩已寫入實際像素，沒有藏在 CSS、SVG 或透明圖層後方。

## 保留這些區分

- `captureDate: null` 表示拍攝日期不詳。`updatedOn` 是資料整理日期，不能當成拍攝或產品發布日期。
- `projectDates: null` 表示未提供專案起訖時間；不要由截圖日期推算開發週期。
- `historical-only` 是歷史畫面。Telegram 選單早於目前的群主私訊管理，不能拿來示範現行權限流程。
- 窄屏瀏覽器截圖、iOS Simulator、Android Emulator 與實體裝置是不同證據。
- TOEFL 圖是無金鑰流程；OpenClaw 是虛構空白工作區；CareLens 是未驗證醫療或模型效能的原型。
- `not-applicable` 的命令列工具沒有產品 UI，不需要製作假 App 畫面。

這些素材用於 Tommy 的個人作品集。它們不包含私人產品的原始碼、授權或交付包，也不授予他人重製私人產品的權利。各公開程式庫的程式授權仍以原 repository 為準。
