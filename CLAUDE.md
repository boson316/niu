# CLAUDE.md — boson316/niu

## 工作流程（Claude 請遵守）

這是 repo 擁有者的明確指示，優先於「在指定分支開發、完成後開 PR」的預設流程。

**小修改：直接推到 `main`**（不開 PR、不另開分支）
- 改文字、連結、數字、小樣式、文件等低風險修改。

**這些修改：先開 PR，再由 Claude 幫忙合併**
- 大改版（版面、整體樣式、新增或移除功能）
- 改計算公式或計算邏輯（改完要附驗算結果：FV 與封閉公式一致、各反推模式能回推原輸入）
- 新增計算機版本（例如 v7）
- 流程：在工作分支 commit → 開 PR → 附上截圖與重點說明給使用者看 → 使用者說可以（例如「合併」「OK」）後由 Claude 合併。使用者沒同意前不要合併。
- 不確定算大還是小時，當成大改，走 PR。

**兩種都要做的事**
- 推之前先檢查：能跑的測試要跑；有改畫面就用 Playwright 截圖檢查（桌機、手機、深色模式），並把截圖給使用者看。
- 不要 force push、不要改寫 `main` 的歷史。
- commit 訊息用英文、寫清楚改了什麼；回覆使用者一律用**繁體中文**。
- 進 `main` 後 GitHub Pages 約 1–3 分鐘會更新，回報時附上線上網址。

## 專案重點

- 純前端 HTML 計算機，部署在 GitHub Pages：<https://boson316.github.io/niu/>，不需 build。
- **目前主力是 `annual_return_calculator_v6.html`**（單檔 App：複利計算 `#calc`／多階段 `#multi`／退休規劃 `#retire`，PWA）。v1–v5 保留不動，只做必要的連結修正。
- v6 支援中英文：`?lang=en|zh`（會記住選擇；沒指定時看瀏覽器語言）。介面固定文字的英文在 `STATIC_EN` 對照表，程式產生的文字用 `T('中文', 'English')`。**新增或修改任何文字時，中英文都要一起改**；英文版金額單位用 TWD／K／M。
- PWA 檔案：`manifest.webmanifest`、`sw.js`、`icon*.png`、`icon.svg`。改動 v6 後把 `sw.js` 的 `CACHE` 版本號 +1。
- 計算慣例：報酬率預設為**有效年化**（月報酬 = (1+r)^(1/12) − 1）；退休規劃含通膨調整。改公式後要驗證：FV 與封閉公式一致、各反推模式能回推原輸入（瀏覽器 console 有 `window.NiuCalc` 可測）。
- 配色：沉穩的藍（`--accent: #3b5fc4`），避免高飽和漸層。
- 改版本或功能時同步更新 `index.html`（版本總覽）與 `README.md`／`README.zh-TW.md`；作品集（boson316/portfolio）裡的計算機介紹也可能需要更新。
