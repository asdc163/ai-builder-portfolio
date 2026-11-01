# 產品畫面

這裡保留真實介面截圖。商用畫面已裁切或以不透明遮罩去識別，日期與示範範圍隨圖保留。

[作品集](../README.zh-TW.md) · [網站素材使用方式](WEBSITE-HANDOFF.md)

## PM Signal Lab

以本機工作表及自編練習，整理能被追問的產品決策。

工作表設計、來源審查與產品決策練習。 回覆流暢還不夠，缺乏依據的決策需要明確審查。

<a href="pm-signal-lab/source-review-desktop.png"><img src="pm-signal-lab/source-review-desktop.png" width="820" alt="PM Signal Lab 工作表：虛構客服審查與可展開的來源紀錄"></a>

桌面工作表，使用虛構示範筆記。2026 年 8 月 16 日歷史本機截圖。 · Chrome desktop · 2026-08-16

<a href="pm-signal-lab/first-run-desktop.png"><img src="pm-signal-lab/first-run-desktop.png" width="820" alt="桌面首次開啟工作表"></a>

歷史本機畫面，訪談明確標示為虛構示範；UI 像素未修改。 · Chrome desktop · 2026-08-16

<a href="pm-signal-lab/first-run-mobile.png"><img src="pm-signal-lab/first-run-mobile.png" width="320" alt="窄屏首次開啟工作表"></a>

同一首次開啟狀態的歷史響應畫面；UI 像素未修改。 · Chrome mobile viewport · 2026-08-16

公開來源，保留桌面與窄屏工作表的歷史畫面。 截圖不代表新一輪正式部署、真人研究或成長成效。

[作品詳情](https://github.com/asdc163/pm-signal-lab)

## 托福單字隨身學

以離線單字學習為核心，Gemini 擴充為選配。

學習流程、字典資料與選配 Gemini 功能。 核心字典與複習工作不依賴模型金鑰。

<a href="toefl-vocab/word-detail.png"><img src="toefl-vocab/word-detail.png" width="320" alt="字義、字根與詞性家族"></a>

由公開來源在本機補拍的無金鑰字典流程；裁取彈窗上半部，未執行 Gemini。 · Chrome desktop · 2026-11-01

<a href="toefl-vocab/quiz-question.png"><img src="toefl-vocab/quiz-question.png" width="320" alt="單字練習題"></a>

本機補拍，使用預設示範進度；不含學習者紀錄或模型回覆。 · Chrome desktop · 2026-11-01

公開來源；本機補拍字典與練習彈窗。 本次補拍不證明模型品質、學習成效或部署可用性。

[作品詳情](https://github.com/asdc163/toefl-vocab)

## 節點服務手機介面

讓接手團隊能嵌入的原生元件；驗收宿主與正式整合入口分開。

產品流程、React Native 實作與宿主整合。 確認時重新檢查報價快照；正式服務與導覽由宿主負責。

<a href="node-interface/ios-network.png"><img src="node-interface/ios-network.png" width="320" alt="節點搜尋與網路卡片"></a>

歷史 iOS 元件畫面；已移除節點識別碼與數值。 · iOS Simulator · 2026-10-31

<a href="node-interface/android-network.png"><img src="node-interface/android-network.png" width="320" alt="Android 節點網路版面"></a>

同一元件的獨立 Android 截圖；已移除識別碼與數值。 · Android Emulator · 2026-10-30

私人前端交付，保留模擬器與 Emulator 的歷史檢查紀錄。 不宣稱已完成實體裝置、真實錢包、正式服務或商店上架驗證。

[作品詳情](https://github.com/asdc163/ai-builder-portfolio/tree/main/cases/node-interface)

## 現貨交易介面

可獨立審查的原生前端示範，訂單狀態在本機運作。

委託介面、錢包狀態與原生工程交付。 Session 轉換使用 reducer 當下狀態；原生介面與示範控制器分開。

<a href="spot-interface/ios-order-entry.png"><img src="spot-interface/ios-order-entry.png" width="320" alt="示範下單介面"></a>

原生純前端示範；裁去品牌標頭，移除報價、餘額及客製資產名稱。 · iOS Simulator · 2026-10-30

<a href="spot-interface/ios-order-result.png"><img src="spot-interface/ios-order-result.png" width="820" alt="本機委託建立結果"></a>

本機模擬委託，不是真實交易；已移除訂單數值、時間、餘額及客製資產名稱。 · iOS Simulator · 2026-10-30

<a href="spot-interface/android-large-text.png"><img src="spot-interface/android-large-text.png" width="320" alt="窄屏與放大字級"></a>

歷史最終版的針對性響應檢查畫面；已移除財務數值，滑桿百分比為固定操作標籤。 · Android Emulator · 2026-10-30

由早期 Expo 審查版遷移至 Community CLI 的前端交付。 沒有真實資產或交易；分平台檢查對應具名版本與選定測試，不當成最終版本單次全套通過。

[作品詳情](https://github.com/asdc163/ai-builder-portfolio/tree/main/cases/spot-interface)

## 社群任務平台

參與者送件與營運審核，包含重試與補件。

參與者與管理端流程、補件恢復及交接。 重試不能重複發點；附件必須有明確的存取邊界。

<a href="quest-platform/submission-waiting.png"><img src="quest-platform/submission-waiting.png" width="820" alt="送件後等待審核"></a>

本機前端審查的實際任務彈窗；裁去品牌、帳戶情境與背景資料。 · Chrome mobile viewport · 2026-10-30

<a href="quest-platform/submission-needs-changes.png"><img src="quest-platform/submission-needs-changes.png" width="320" alt="退件原因與補件入口"></a>

同一任務收到補件要求的狀態；已裁去背景並遮蔽審核時間。 · Chrome mobile viewport · 2026-10-30

私人實作交付；公開匿名案例及歷史本機審查畫面。 不宣稱公開託管、接收方部署、真實錢包或外部服務已完成驗證。

[作品詳情](https://github.com/asdc163/ai-builder-portfolio/tree/main/cases/quest-platform)

## VPN 訂閱系統

訂閱結帳、付款對帳與客戶端權限狀態。

續費流程、付款狀態邊界、客戶端恢復與工程交接審查。 從付款頁返回不等於結算完成；未完成訂單需要清楚的恢復入口。

<a href="vpn-subscription/membership-renewal.png"><img src="vpn-subscription/membership-renewal.png" width="320" alt="續費方案選擇"></a>

歷史工程審查畫面；已移除售價與付款路徑，畫面不代表實際網路可用性。 · iOS Simulator · 2026-10-15

<a href="vpn-subscription/payment-return-pending.png"><img src="vpn-subscription/payment-return-pending.png" width="820" alt="付款返回後的未完成訂單"></a>

歷史審查中的未完成訂單狀態；已移除金額與時間，不代表真實資金結算。 · iOS Simulator · 2026-10-15

匿名商用工程案例，附歷史 iOS 審查畫面片段。 不宣稱真實資金、實體裝置、目標網路或消費者正式發布已驗證。

[作品詳情](https://github.com/asdc163/vpn-subscription-case-study)

## Telegram 社群營運機器人

社群參與、群主私訊管理，以及投遞結果不明時的恢復。

參與規則、角色檢查、投遞行為與商用交接審查。 敏感操作重新核對群主身分，並保留投遞結果不明的狀態。

<a href="telegram-community-bot/historical-command-inventory.png"><img src="telegram-community-bot/historical-command-inventory.png" width="820" alt="早期營運功能選單"></a>

群主專用私訊管理改版前的歷史片段，僅說明功能範圍，不代表現行權限流程；已裁去品牌與對話情境。 · Telegram client · 2026-10-13

匿名商用案例；畫面僅公開較早的營運選單片段。 歷史圖早於群主專用私訊管理改版，不能當成現行操作證據。

[作品詳情](https://github.com/asdc163/telegram-community-bot-case-study)

## CareLens 照護原型

圖片輸入的照護原型，具備無金鑰 mock 與預設示範資料。

原型流程、圖片 API 邊界，以及模型與 mock 的明確區分。 以 schema 解析模型回覆，並把 mock 結果與辨識準確度分開。

<a href="carelens/prototype-landing.png"><img src="carelens/prototype-landing.png" width="820" alt="照護原型首頁"></a>

既有公開原型圖，內容為虛構示範；拍攝日期不詳，未驗證 OCR 或醫療效能，UI 像素未修改。 · Repository screenshot · None

<a href="carelens/prototype-dashboard.png"><img src="carelens/prototype-dashboard.png" width="320" alt="原型家庭照護總覽"></a>

既有原型截圖，裁取主要內容區；已移除示範姓名、email 與數值，不作為醫療或模型效能證據。 · Repository screenshot · None

公開原型；使用既有 repository 截圖，拍攝日期不詳。 模型行為、OCR 準確度、醫療正確性與部署可用性均未驗證。

[作品詳情](https://github.com/asdc163/carelens)

## OpenClaw Dashboard

在本機檢視代理工作區，同時保留唯讀邊界的看板。

唯讀營運介面、解析邊界與公開交接文件。 檢視工作區不應同時取得執行代理操作的路徑。

<a href="openclaw-dashboard/synthetic-workspace.png"><img src="openclaw-dashboard/synthetic-workspace.png" width="820" alt="唯讀看板與空白示範工作區"></a>

在隔離、明示虛構的工作區補拍；沒有真實代理、私人設定或營運日誌，UI 像素未修改。 · Chrome desktop · 2026-11-01

公開來源；本機補拍示範工作區。 不宣稱具備託管控制平台、登入保護或真實代理效能。

[作品詳情](https://github.com/altoslab447/openclaw-dashboard)

## ethers-v6-codemod

以 AST 進行 JavaScript 程式遷移的工具。

公開遷移工具實作與文件。 先比對語法，再變更程式表達式。

公開來源；命令列工具，沒有產品 UI。 不為它捏造 App 畫面；本輪作品集更新未重跑工具。

[作品詳情](https://github.com/asdc163/ethers-v6-codemod)
