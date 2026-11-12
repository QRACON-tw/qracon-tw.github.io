# QRACON 官方網站入口

此 repository 是 QRACON 組織的 GitHub Pages 根網址：<https://qracon-tw.github.io/>。

部署 workflow 會查詢 `QRACON-tw` 組織的公開 repositories，選出名稱符合四位數 `20XX` 的最高年度 repository，並從該 repository 的預設分支抓取網站原始碼，建置後發布到 Pages。每日 16:17（臺灣時間）自動更新，也可在 GitHub Actions 手動執行 `Deploy latest annual website to GitHub Pages`。如果找不到符合條件且有預設分支的公開年度 repository，workflow 會停止並在執行紀錄說明原因。

建置時會將 Astro 的 `site` 暫時覆寫為根網址，讓 canonical URL 與 sitemap 指向 GitHub Pages；不會修改年度官網 repository。發布到此根網址的頁面路徑是 `/`，網址不加年度前綴。
