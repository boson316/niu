# 年化報酬率與退休規劃計算機

**Languages:** [English](README.md) · [中文](README.zh-TW.md)

複利、IRR、退休概算的純 HTML 工具。無需 build，瀏覽器直接開啟，或透過 GitHub Pages 部署。

**線上版：** <https://boson316.github.io/niu/>

---

## 快速開始

| 頁面 | 說明 |
|------|------|
| [index.html](index.html) | 版本總覽 — 選擇計算機 |
| [annual_return_calculator_v4.html](annual_return_calculator_v4.html) | **建議使用** — 年化報酬／IRR、多階段、可反推本利和／報酬率／本金／時間／定額 |
| [annual_return_calculator_v5.html](annual_return_calculator_v5.html) | 退休規劃 — 4% 法則、台北市房價預設、ETF 假設下幾年能退休 |
| [annual_return_calculator_en_v1.html](annual_return_calculator_en_v1.html) | 英文介面（v1 風格） |

舊版（`annual_return_calculator.html`、`v3`）仍保留供對照。

### 本機預覽

```bash
# 在此資料夾
npx serve .
# 開啟 http://localhost:3000/
```

或直接雙擊任一 HTML 檔。

---

## 功能摘要

### v4 — 年化報酬率計算機

- 算最終金額、IRR、所需本金、所需時間、定期定額
- 多階段：上一階段最終金額可帶入下一階段本金
- v5 可帶參數開啟 v4 細調

### v5 — 退休規劃計算機

- **4% 法則：** 月生活開銷 × 300 = 生活費所需本金
- **買房：** 台北市一次性購屋目標（依近期實價登錄概算預設）
- **退休總目標** = 生活費本金 + 房價
- 反推：幾年能退休、每月要存多少、現在要有多少本金
- 手機：數字鍵盤、底部固定「計算」按鈕

---

## 免責聲明

僅供教育與概算，**不構成**投資、稅務或理財建議。4% 法則與 ETF 假設報酬（如 10%）皆非保證。房價預設為參考值，請以實際物件與實價登錄為準。

---

## 部署至 GitHub Pages（`boson316/niu`）

1. 將此資料夾 push 至 `main`（repo 根目錄）。
2. **Settings → Pages →** Branch `main`，資料夾 `/ (root)`。
3. 網址：`https://boson316.github.io/niu/<檔名>.html`

---

## 授權

MIT（若你使用其他授權請自行修改）。
