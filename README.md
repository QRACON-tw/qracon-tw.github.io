# QRACON 官方網站與共用網域

此 repository 管理共用自訂網域 <https://qracon.entangletech.tw/>，根路徑 `/` 直接提供最新年度官網；年度路徑（例如 `/2026/`）由各年度 repository 自行部署，因此兩種網址都能瀏覽同一年度內容。

入口 workflow 每 15 分鐘查詢一次 QRACON-tw 公開且已啟用 GitHub Pages 的四位數年度 repository，並將最新年度的網站建置到 `/`。若最新年度的 `main` 有新 commit，下一次排程會重新部署；無需在年度 repository 設定通知 token。判斷新版本的工作與安裝年度 repo 依賴的建置工作分開，Pages 寫入權限只提供給部署工作。根路徑的網站導覽仍可連到年度路徑，各年度網站也會提供其他年度的入口。

此 workflow 也會在入口 repository 的 `main` 更新或手動執行時重新部署。它會從最新年度 repository 安裝鎖定的依賴並以根路徑建置 Astro 網站。

DNS 將自訂網域 CNAME 指向 `QRACON-tw.github.io`，由此 repository 的 Pages 網域設定統一管理。年度專案網站沿用相同網域，使用各自的 repository 路徑。
