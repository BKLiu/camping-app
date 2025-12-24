露營小助手 (Camping Assistant) 🏕️

一個專為露友設計的輕量級 Web App，整合了營地行程管理、多人即時分帳與地圖導航連動功能。無需下載，透過瀏覽器即可與夥伴即時協作。

✨ 主要特色

📊 全能總覽儀表板：即時統計總支出、人均費用、營位費，並視覺化顯示各露友的支出貢獻。

🌐 多人即時同步：整合 Firebase Firestore，產生專屬行程 ID，讓夥伴透過雲端即時參與編輯。

💰 智能分帳系統：自動計算「誰該給誰多少錢」的最短還款路徑，內建防呆提示與成員人數檢查。

⛺ 行程細節紀錄：支援儲存營位費、夜衝費及營地備註，一鍵跳轉 Google Maps 導航。

📱 響應式設計：針對手機操作優化，支援鍵盤 Enter 快速輸入，即使在小螢幕也能完美顯示。

🛠️ 版本更新歷史 (Version History)

v1.0.4 (最新版本)

修正： 處理 auth/custom-token-mismatch 錯誤。當環境憑證不匹配時，自動回退至「匿名登入」，確保連線穩定。

優化： 強化身分驗證邏輯，增加錯誤監聽與使用者提示。

v1.0.3

功能： 為所有輸入框加上 Enter 鍵監聽。在支出項目按 Enter 跳轉金額，在其他框按 Enter 直接執行動作。

修正： 解決多人連線彈窗在手機版（小螢幕）上的跑版問題，優化 ID 輸入框與按鈕的寬度比例。

v1.0.2

功能： 在成員管理頁面新增「清空本地快取資料」按鈕，方便重新開啟新行程。

優化： 強化分帳邏輯，加入除以零檢查與金額必須大於 0 的防呆機制。

修正： 確保動態更新清單後，Lucide 圖示能正確重新渲染。

v1.0.1

修正： 解決 GitHub Pages 部署後出現 ReferenceError 的問題（將函式顯式綁定至 window 物件）。

優化： 修正模組化腳本（module scope）導致 HTML onclick 失效的問題。

優化： 預留 Firebase Config 配置區塊並增加 API 填寫狀態偵測。

v1.0.0

初始發佈： 包含儀表板、成員管理、分帳計算與本機 localStorage 儲存功能。

🚀 部署教學 (Deployment Guide)

1. 取得 Firebase 配置

前往 Firebase Console 建立新專案。

啟用 Firestore Database（建議使用測試模式）。

啟用 Authentication 中的「匿名 (Anonymous)」登入方法。

在「專案設定」中新增網頁應用程式，複製 firebaseConfig 內容。

2. 更新程式碼

開啟 camping_app.html。

找到 const firebaseConfig = { ... } 區塊（約在檔案中後段）。

貼上您的專案 API Key 與 ID。

3. 上傳至 GitHub

將檔案重新命名為 index.html。

上傳至 GitHub Repository。

前往 Settings > Pages，將來源設為 main 分支後儲存。

在 Firebase 的 Authentication > Settings > Authorized domains 中加入您的 GitHub 網址（例如：username.github.io）。

📖 使用提示

儲存目的地：在「行程」分頁輸入完按 Enter 即可儲存並產生導航連結。

快速連線：點擊右上角燈號即可開啟多人模式，將 ID 分享給朋友後，大家的手機會即時同步。

分帳提醒：若還沒加成員就想分帳，系統會自動跳轉引導您先新增夥伴。

📄 授權協議

本專案採用 MIT License 授權。

🌲 由露營愛好者為夥伴們開發。祝您露營愉快！🔥
