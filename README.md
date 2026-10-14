# Lockheed Martin | Interactive Financial & Geopolitical Analysis

**A browser-based, interactive recreation of the analytical content of my Power BI research project.**

[**Open the interactive dashboard**](https://3lessing.github.io/LMT_Geopolitical_Analysis/) · [**Research report (PDF)**](LMT_Research_Report.pdf)

**Author:** Blessing Nwotite  
**Data coverage:** Lockheed Martin FY2021–FY2025 financial statements; LMT, SPY and ITA daily prices through September 11, 2026; 10 selected geopolitical events during 2021–2025.

## Overview

This project evaluates Lockheed Martin's financial performance, backlog growth, cash generation, and historical stock-price reactions to selected geopolitical events. It compares LMT with the S&P 500 ETF (SPY) and the iShares U.S. Aerospace & Defense ETF (ITA) across 1-, 5-, 10-, and 20-session event windows.

The website is **not an embedded Power BI report**. It is a standalone reconstruction with a redesigned layout, built with native HTML/CSS/JavaScript and locally bundled Plotly.js. Its charts are real, data-backed interactive charts—not images.

## What you can interact with

- **Executive Overview:** select years, click segment-revenue bars and backlog bars, and jump to event-window analysis.
- **Financial Performance:** change focus years, click financial table rows and chart points, hover for exact data, and explore profitability and revenue growth.
- **Event Analysis:** switch 1/5/10/20 trading sessions, compare ITA or SPY, and click individual geopolitical-event bars or table rows to inspect returns.
- **Reaction Persistence:** view event outperformance across four windows, click columns and heatmap cells, and compare event-level benchmark-adjusted returns.
- **Operating Performance:** filter by financial year and business segment; inspect revenue, backlog and segment margins.
- **Market Performance:** change date ranges, toggle LMT/SPY/ITA, hover the charts, zoom and pan the plotted data, and see the returns recalculate.
- **Cash Flow Analysis:** change fiscal years and compare operating cash flow, investing and financing flows, dividends, buybacks, and free cash flow.
- **Methodology & Limitations:** review formulas, data conventions and research caveats.
- **Sources & Event Register:** filter and open selected geopolitical events; inspect links to data origins.

## Key findings

- Lockheed Martin's reported revenue increased from **$67.0B in FY2021** to **$75.0B in FY2025**, while its operating margin declined from **13.6%** to **10.3%**.
- FY2025 reported backlog was **$193.6B** and free cash flow was approximately **$6.9B**.
- LMT outperformed ITA on a price-return basis across **8 of 10 events within 5 trading sessions**, compared with **4 of 10 within 20 trading sessions**. The sample is deliberately selected and **does not establish causality or a repeatable trading strategy**.

## Run locally

1. Download this repository or clone it.
2. Open **`index.html`** in a browser. Internet access and a Power BI account are not required because Plotly is bundled locally.
3. Choose pages from the left navigation and use filters and charts to explore.

## Publish with GitHub Pages

1. Upload `index.html`, `styles.css`, `app.js`, `data.js`, `plotly.min.js`, `LMT_Research_Report.pdf`, and this `README.md` to the **root** of the public repository.
2. From **Settings → Pages**, select **Deploy from a branch**, then `main` and `/(root)`.
3. Save and wait for GitHub Pages to finish publishing.
4. Refresh `https://3lessing.github.io/LMT_Geopolitical_Analysis/` (Ctrl+Shift+R if an older version is cached).

No build tools, API keys or online JavaScript frameworks are required. Previous `page-*.webp` screenshot files are not used by this new version.

## Data, methodologies and limitations

- Annual financials: [Lockheed Martin full-year FY2021 release](https://news.lockheedmartin.com/2022-01-25-Lockheed-Martin-Reports-Fourth-Quarter-and-Full-Year-2021-Financial-Results), [FY2023 release](https://news.lockheedmartin.com/2024-01-23-Lockheed-Martin-Reports-Fourth-Quarter-and-Full-Year-2023-Financial-Results), and [FY2025 release](https://news.lockheedmartin.com/2026-01-29-Lockheed-Martin-Reports-Fourth-Quarter-and-Full-Year-2025-Financial-Results), with comparative-year figures.
- Daily price histories: Nasdaq-sourced LMT, SPY and ITA close-price observations retained in the Power BI project dataset, including a documented SPY April 20, 2026 correction.
- Selected historical events: public UN, NATO and related historical sources included in the Sources & Event Register.
- Event price return = end-window close / baseline close − 1. Relative return = LMT price return − benchmark price return.
- Prices and returns **exclude dividends**. Historical adjustment conventions have not been exhaustively independently confirmed.
- The 10 events are not a randomized or exhaustive sample, timing is based on assigned public dates, and co-occurring news may drive prices. The dashboard makes **no causal claims** and is not investment advice.
- Before redistributing historical market data publicly, confirm that the applicable source license permits republication.

## Technical notes

The web dashboard uses locally bundled **Plotly.js 3.3.1** (MIT-licensed) for interactive charts. Data is stored in `data.js` and analyzed in-browser using ordinary JavaScript. The app sends no requests to external financial APIs and does not refresh automatically.

© 2026 Blessing Nwotite · Independent portfolio research.
