# CLAUDE.md — boson316/niu

## 工作流程（Claude 請遵守）

- **改完直接推到 `main`，不要開 PR、不要另開分支。** 這是 repo 擁有者的明確指示，優先於「在指定分支開發」的預設流程。
- 推之前先做檢查：跑得動的測試要跑；有改畫面就用 Playwright 截圖檢查（桌機、手機、深色模式），並把截圖給使用者看。
- 不要 force push、不要改寫 `main` 的歷史。
- commit 訊息用英文、寫清楚改了什麼；回覆使用者一律用**繁體中文**。
- 推到 `main` 後 GitHub Pages 約 1–3 分鐘會更新，回報時附上線上網址。

## 專案重點

- 純前端 HTML 計算機，部署在 GitHub Pages：<https://boson316.github.io/niu/>，不需 build。
- **目前主力是 `annual_return_calculator_v6.html`**（單檔 App：複利計算 `#calc`／多階段 `#multi`／退休規劃 `#retire`，PWA）。v1–v5 保留不動，只做必要的連結修正。
- PWA 檔案：`manifest.webmanifest`、`sw.js`、`icon*.png`、`icon.svg`。改動 v6 後把 `sw.js` 的 `CACHE` 版本號 +1。
- 計算慣例：報酬率預設為**有效年化**（月報酬 = (1+r)^(1/12) − 1）；退休規劃含通膨調整。改公式後要驗證：FV 與封閉公式一致、各反推模式能回推原輸入（瀏覽器 console 有 `window.NiuCalc` 可測）。
- 配色：沉穩的藍（`--accent: #3b5fc4`），避免高飽和漸層。
- 改版本或功能時同步更新 `index.html`（版本總覽）與 `README.md`／`README.zh-TW.md`；作品集（boson316/portfolio）裡的計算機介紹也可能需要更新。
