# Annual Return & Retirement Calculators

**Languages:** [English](README.md) · [中文](README.zh-TW.md)

Static HTML tools for compound growth, IRR, and retirement planning. No build step — open any `.html` file in a browser or use GitHub Pages.

**Live (GitHub Pages):** <https://boson316.github.io/niu/>

---

## Quick start

| Page | Description |
|------|-------------|
| [index.html](index.html) | Version hub — pick a calculator |
| [annual_return_calculator_v6.html](annual_return_calculator_v6.html) | **Recommended** — app-style UI: compound calculator, multi-stage plan and retirement planner in one, with charts, yearly tables, installable PWA |
| [annual_return_calculator_v4.html](annual_return_calculator_v4.html) | Previous — CAGR / IRR, multi-stage, solve for FV / rate / principal / time / payment |
| [annual_return_calculator_v5.html](annual_return_calculator_v5.html) | Previous — retirement planner: 4% rule, Taipei housing presets, years-to-FIRE with ETF assumptions |
| [annual_return_calculator_en_v1.html](annual_return_calculator_en_v1.html) | English UI (v1-style) |

Legacy versions (`annual_return_calculator.html`, `v3`) remain for reference.

### Local preview

```bash
# From this folder
npx serve .
# Open http://localhost:3000/
```

Or double-click any HTML file.

---

## Features

### v6 — Compound & retirement app

- Bottom tab bar on mobile, live result card (no Calculate button), floating result pill, dark mode, thousands-separator inputs with 萬 hints
- Compound tab: solve for FV / rate / payment / principal / time; switching modes keeps the last answer
- Multi-stage tab: contribute or withdraw per stage, frequency, yearly step-up, one-off lump sums; overall IRR from actual cash flows
- Retirement tab: adjustable withdrawal rate + house goal, **inflation-adjusted** targets, other retirement income, post-retirement drawdown simulation, ±2% return scenarios
- Interactive growth charts and year-by-year tables; shareable links; installable/offline PWA (`manifest.webmanifest`, `sw.js`)
- Math changes vs v4/v5: rates are **effective annual** by default (nominal ÷ 12 overstated returns), IRR search covers −99% to 1000%, begin/end-of-period timing, depletion detection

### v4 — Annual return calculator

- Future value, IRR, required principal, time, or periodic payment
- Multiple stages (previous stage FV rolls into next principal)
- v5 can open v4 with query parameters for fine-tuning

### v5 — Retirement planner

- **4% rule:** monthly living expense × 300 = living-expense portfolio target
- **Housing:** one-time Taipei purchase goal (presets from recent transaction data)
- **Total target** = living fund + house
- Solve: years to retire, monthly savings needed, or required starting principal
- Mobile: numeric keyboard (`inputmode`), fixed bottom **Calculate** bar

---

## Disclaimer

Educational estimates only — **not** investment, tax, or financial advice. The 4% rule and assumed ETF returns (e.g. 10%) are not guaranteed. Housing presets are approximate; verify with actual listings and registered transaction prices.

---

## Deploy to GitHub Pages (`boson316/niu`)

1. Push this folder to `main` at repo root (or `/docs` if you configure Pages that way).
2. **Settings → Pages →** Deploy from branch `main`, folder `/ (root)`.
3. URLs: `https://boson316.github.io/niu/<filename>.html`

---

## License

MIT (or specify your license if different).
