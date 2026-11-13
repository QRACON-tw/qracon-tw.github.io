# QRACON 官方網站入口

此 repository 是 QRACON 組織的 GitHub Pages 根網址：<https://qracon-tw.github.io/>。

首頁列出目前年度 `2026`；點選後會經由 `/2026/` 前往 QRACON 2026 官網：<https://2026-qracon.entangletech.tw/>。

GitHub Pages workflow 會在入口 repository 的 `main` 更新、收到年度官網的 `repository_dispatch`，或手動執行時部署 `site/`。目前 2026 repository 的 `main` 有新 commit 時，會透過 `.github/workflows/notify-website-deploy.yml` 發送 `annual-site-updated` 事件。

要啟用跨 repository 事件，請在 `QRACON-tw/2026` 設定名為 `PAGES_DISPATCH_TOKEN` 的 Actions repository secret。此 fine-grained personal access token 僅需授權 `QRACON-tw/qracon-tw.github.io`，並開啟 repository `Contents: write` 權限。若未設定或 token 權限不足，2026 repo 的通知 workflow 會明確失敗；可在入口 repo 手動執行部署 workflow。
