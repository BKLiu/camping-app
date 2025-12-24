# **露營分帳小助手：GitHub 發佈指南**

這份指南將引導你將 camping\_app.html 發佈到 GitHub 並開啟 **GitHub Pages** 功能，讓你的露營夥伴可以透過網址直接使用。

## **準備工作**

1. 擁有一個 [GitHub 帳號](https://github.com/)。
2. 將你的程式碼檔案重新命名為 **index.html**。
   3. *理由：GitHub Pages 預設會尋找名為 index.html 的檔案作為網站首頁。*

## **方法一：透過瀏覽器上傳（最簡單，推薦）**

如果你不想安裝任何軟體，這是最快的方式：

### **1. 建立新的存放庫 (Repository)**

* 登入 GitHub 後，點擊右上角的 **「+」**，選擇 **「New repository」**。
* **Repository name**: 輸入專案名稱（例如：camping-app）。
* **Public/Private**: 選擇 **Public**（若要使用免費版的 GitHub Pages，必須設為公開）。
* 點擊底部的 **Create repository**。

### **2. 上傳檔案**

* 在新頁面中，找到「uploading an existing file」的連結。
* 將你的 **index.html** 檔案拖曳進去。
* 在下方的 Commit 訊息欄位輸入：「Initial commit」。
* 點擊 **Commit changes**。

### **3. 開啟網站功能 (GitHub Pages)**

* 點擊該專案頁面上方的 **Settings**（設定）。
* 在左側選單找到 **Pages** 標籤。
* 在 **Build and deployment** 下方的 Branch 選擇 **「main」**，資料夾選擇 **「/(root)」**。
* 點擊 **Save**。

### **4. 取得網址**

* 等待約 1-3 分鐘，重新整理 Pages 頁面。
* 你會看到上方出現一行字：Your site is live at https://\<你的帳號\>.github.io/camping-app/。
* 點擊該連結，你的 App 就正式上線了！

## **方法二：使用 Git 指令（專業開發者推薦）**

如果你電腦有安裝 Git，可以使用以下指令：

\# 1. 進入你的專案資料夾  
\# 2. 初始化 Git  
git init

\# 3. 加入檔案（確保檔案已命名為 index.html）  
git add index.html

\# 4. 提交  
git commit -m "First release"

\# 5. 建立主分支  
git branch -M main

\# 6. 連接到遠端 GitHub 專案（請替換為你的專案網址）  
git remote add origin [https://github.com/你的帳號/camping-app.git](https://github.com/你的帳號/camping-app.git)

\# 7. 推送上傳  
git push -u origin main

*上傳後，仍需執行上述「方法一」中的 **步驟 3** 來啟用 Pages 功能。*

## **常見問題 (FAQ)**

### **Q1: 我修改了程式碼，要怎麼更新網站？**

* **網頁版**：進入 GitHub 專案頁面，點擊 index.html 分頁中的「編輯 (鉛筆圖示)」或直接再次上傳新版本覆蓋即可。
* **網址會變嗎？** 不會，網址會永遠固定。

### **Q2: 為什麼我打開網址是空白的或 404？**

* 檢查檔案名稱是否拼錯，必須是小寫的 index.html。
* GitHub Pages 部署需要一點時間，請稍等幾分鐘。

### **Q3: 資料會不見嗎？**

* 不會。這個 App 使用的是瀏覽器的 localStorage 技術，資料儲存在使用者的手機/電腦中，上傳到 GitHub 只是提供程式下載。
