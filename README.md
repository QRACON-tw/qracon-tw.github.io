# QRACON 官方網站入口

此 repository 是 QRACON 組織的 GitHub Pages 根網址：<https://qracon-tw.github.io/>。

首頁列出 `2026` 與 `2025` 年度官網入口。`/2026/` 會前往 QRACON 2026 官網：<https://2026-qracon.entangletech.tw/>；`/2025/` 對應至 `QRACON-tw/2025` 的 GitHub Pages 專案網站。

GitHub Pages workflow 會在入口 repository 的 `main` 更新、收到年度官網的 `repository_dispatch`，或手動執行時部署 `site/`。`QRACON-tw/2025` 的 GitHub Pages 直接從 `main` 根目錄發布，因此該 repo 的新 commit 會更新 `/2025/` 專案網站。`QRACON-tw/2025` 與 `QRACON-tw/2026` 都有 `.github/workflows/notify-website-deploy.yml`，可在 `main` 有新 commit 時通知入口 repository 重新部署。

要啟用跨 repository 事件，請分別在 `QRACON-tw/2025` 與 `QRACON-tw/2026` 設定名為 `PAGES_DISPATCH_TOKEN` 的 Actions repository secret。此 fine-grained personal access token 僅需授權 `QRACON-tw/qracon-tw.github.io`，並開啟 repository `Contents: write` 權限。`2025` repo 目前尚未設定此 secret；未設定或 token 權限不足時，通知 workflow 會明確失敗。入口 repository 仍可手動執行部署 workflow。
