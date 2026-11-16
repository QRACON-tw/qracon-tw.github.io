# QRACON 官方網站入口

此 repository 管理 QRACON 組織 GitHub Pages 根網站及共用自訂網域：<https://2026-qracon.entangletech.tw/>。

根網址 `/` 會查詢 QRACON-tw 的公開 repositories，找出最新且已啟用 GitHub Pages 的四位數年度 repo，再直接前往對應路徑（例如 `/2026/`），不另外提供年度選擇頁。各年度網站會在自己的導覽列提供其他年度的入口；年度頁面由各年度 repository 的 GitHub Pages 專案網站直接提供，使用同一個自訂網域。

GitHub Pages 根網站 workflow 會在此 repository 的 `main` 更新或手動執行時部署 `site/`。年度網站則由各自 repository 的 Pages 設定及部署 workflow 自行更新；年度 repo 不需要通知 token。

DNS 請將自訂網域 CNAME 指向 `QRACON-tw.github.io`，由此 repository 的 Pages 網域設定統一管理。年度專案網站會沿用組織的自訂網域，並使用各自的 repo 路徑。
