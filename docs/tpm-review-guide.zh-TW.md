# 產品取捨

整理幾個作品裡的決定。它們都發生在使用者流程和技術實作交會的地方。

[English](tpm-review-guide.md) · [作品](../README.zh-TW.md)

## 複習不依賴生成成功

[TOEFL Vocab](https://github.com/asdc163/toefl-vocab)的詞庫和間隔複習不需要 AI。生成解釋可以增加內容，但接上供應商以後，不應讓整個學習任務都依賴一次模型呼叫成功。

代價是介面要說清楚更多狀態：沒有啟用、等待逾時，以及上游錯誤。[API handler](ai-capability-evidence.zh-TW.md#toefl-vocab)分開處理這幾種情況。接下來要回答的是，生成內容帶來的學習幫助，能否抵過錯誤、等待和成本。這需要使用者與模型評估。

## 參與和管理分開

[Telegram Bot](https://github.com/asdc163/telegram-community-bot-case-study)讓一般成員留在原群參與，群主透過私訊設定。群主可能在選單開啟後換人，所以每次敏感操作重新檢查身分，也是產品行為的一部分。

群主多了一次前往私訊的切換，換來的是成員不必理解管理介面就能參與。[案例的交付筆記](https://github.com/asdc163/telegram-community-bot-case-study/blob/main/docs/delivery-decisions.md)另外交代依賴與驗收問題。

## 付款出錯，要留恢復路徑

[訂閱系統](https://github.com/asdc163/vpn-subscription-case-study)需要處理少付、晚到和到期前續費。帳本保留實收金額，介面則讓人看懂下一步該做什麼。

地址額度用完會阻擋新訂單，但已存在的訂單仍要繼續核款。把這兩種可用性分開，才不會連已經開啟的付款路徑都一起藏起來。[交付筆記](https://github.com/asdc163/vpn-subscription-case-study/blob/main/docs/delivery-decisions.md)保留後續要完成的依賴。

## 模型可以替誰做承諾

[PM Signal Lab 的虛構練習](https://github.com/asdc163/pm-signal-lab/tree/main/playbooks/ai-launch-review)讓助手草擬客服回覆，沒有批准退款的權限。真正要確認的是，回覆到了客戶以前，審查者能不能發現這個越權承諾。

練習指出錯誤、暫停試行，再要求用實際輸出重測。人工審查本身也需要證據；在流程圖裡放一個步驟，還不能知道它的效果。

## 讓營運人員重試，也不重複加分

[社群任務平台](../cases/quest-platform/README.zh-TW.md)的積分調整若已生效、回應卻遺失，營運人員會不知道該不該再按一次。相同請求重送時應讀回既有結果，權限、帳本與稽核則放在同一條決策路徑。

案例也交代被退回的提交怎麼補件、重新進入審核。定義錯誤狀態之外，還要把下一步做出來。

## 切換錢包時，保留剛成交的訂單

[現貨介面](../cases/spot-interface/README.zh-TW.md)雖然是示範版，本機資料仍需一致。舊 session 快照可能覆蓋剛成交的訂單，因此一般錢包轉換改成依 reducer 的當前狀態計算，不在一般導覽中替換整份 session。

原生版面檢查與狀態模型回歸各自回答不同問題。案例分開記錄兩者，也保留模擬交易和真實交易服務的界線。

這些內容說明實作取捨與待驗證問題，不當作客戶研究或商業成效。商用驗證細節列在個別案例。
