# QRACON 官方網站入口

此 repository 是 QRACON 組織的 GitHub Pages 根網址：<https://qracon-tw.github.io/>。

目前會從 [`QRACON-tw/2026`](https://github.com/QRACON-tw/2026) 的 `main` 分支抓取最新網站原始碼，建置後發布到 Pages。每日 16:17（臺灣時間）自動更新，也可在 GitHub Actions 手動執行 `Deploy latest 2026 to GitHub Pages`。

建置時會將 Astro 的 `site` 暫時覆寫為根網址，讓 canonical URL 與 sitemap 指向 GitHub Pages；不會修改 2026 官網 repository。發布到此根網址的頁面路徑是 `/`，目前不使用 `/2026` 前綴。
