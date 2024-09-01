# 網頁切版直播班 Vite 範例

## Node.js 版本

* 專案的 Node.js 版本需為 v16 以上
* 查看 Node.js 版本指令：`node -v`

## 指令列表

* `npm install`：初次下載該範例專案後，需要使用 `npm install` 來安裝套件
* `npm run dev`：執行開發模式
  
  若沒有自動開啟瀏覽器，可在瀏覽器搜尋欄手動輸入
  
  ```txt
  http://localhost:5173/<repository name>/pages/index.html
  ```

* `npm run build`：執行編譯模式（不會開啟瀏覽器）
* `npm run deploy`：自動化部署

## 資料夾結構

* assets：靜態資源放置處
  * images：圖片放置處
  * scss：SCSS 樣式放置處
* layout：ejs 模板放置處
* pages：頁面放置處
* `main.js`：JavaScript 程式碼可寫在該檔案內

### 注意事項

* 已將 pages 資料夾內的 `index.html` 預設為首頁，建議不要任意修改 `index.html` 的檔案名稱
* `.gitignore` 檔案是用來忽略掉不該上傳到 GitHub 的檔案（例如：node_modules），請不要移除 `.gitignore`

## 開發模式的監聽

vite 專案執行開發模式 `npm run dev` 後即會自動監聽，不需要使用 Live Sass Compiler 的 `watch SCSS` 功能

## 部署 gh-pages 流程說明

### Windows 版本

* 在 GitHub 建立一個新的 Repository

* 部署前請務必先將原始碼上傳到 GitHub Repository，也就是初始化 GitHub，因此通常第一步驟會在專案終端機輸入以下指令

  ```bash
  git init # 若已完成初始化就可以不用輸入
  git add .
  git commit -m 'first commit'
  git branch -M main
  git remote add origin [GitHub Repositories Url]
  git push -u origin main # 僅限第一次輸入，往後只需要輸入 git push
  ```

* 初始化完畢後，執行 `npm run deploy` 指令進行自動化部署
