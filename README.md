# QRACON 官方網站入口

此 repository 管理 QRACON 組織 GitHub Pages 根網站及共用自訂網域：<https://2026-qracon.entangletech.tw/>。

首頁列出年度官網入口。`/2025/` 與 `/2026/` 都由各年度 repository 的 GitHub Pages 專案網站直接提供，使用同一個自訂網域，不會轉址到其他網域。

GitHub Pages 根網站 workflow 會在此 repository 的 `main` 更新或手動執行時部署 `site/`。年度網站則由各自 repository 的 Pages 設定及部署 workflow 自行更新；年度 repo 不需要通知 token。

DNS 請將自訂網域 CNAME 指向 `QRACON-tw.github.io`，由此 repository 的 Pages 網域設定統一管理。年度專案網站會沿用組織的自訂網域，並使用各自的 repo 路徑。
