# Lockheed Martin | Financial Performance & Geopolitical Event Analysis

**A nine-page interactive website based on my original Power BI report**, exploring Lockheed Martin financial performance (FY2021–FY2025) and market-price responses to ten selected geopolitical events.

### [Open the interactive website](https://3lessing.github.io/LMT_Geopolitical_Analysis/)

The site preserves the original nine-page arrangement, colors and research copy. All analytical chart regions are rebuilt as live SVG/HTML elements at page load, using the source data; page images are retained only as visual/background references. Browser-side functionality adds filtering without requiring a Microsoft or Power BI account. This is a custom recreation, not a Power BI embed.

## Research question

Does geopolitical tension translate into sustained outperformance for defense stocks?

### Key findings

- Across ten selected geopolitical events, LMT outperformed defense ETF **ITA in 8 of 10 events (80%)** over the first five trading sessions; median relative outperformance was **+2.45 percentage points**.
- At 20 trading sessions, that dropped to **4 of 10 (40%)** and median relative performance fell to **−1.93 percentage points**.
- LMT revenue grew from approximately **$67.0B in FY2021 to $75.0B in FY2025**, while its reported operating margin declined from **13.6% to 10.3%**.
- Results are exploratory and should not be interpreted as evidence of causality or an actionable investment strategy.

## What is interactive?

1. Navigate all **nine original report pages** using the Pages sidebar.
2. On **Event Analysis**, change the event window between **1, 5, 10 and 20 trading sessions** using the header selector or the selector positioned over the original slicer. Event returns, benchmark comparison bars, median returns, and the share beating ITA are recomputed from event-level observations.
3. Click an **event name or benchmark bar** to cross-highlight the selected event and recalculate metrics for that event. Use the event selector to make the selection from anywhere.
4. Click **years** and **operating segments** on financial/operating/cash-flow pages to filter and explore the original annual figures.
5. On **Market Performance**, change the **start/end dates**, show or hide **LMT, SPY and ITA**, hover for dated close values, or **drag across the plot to zoom**. The site rebases indexed performance to 100 using each series' first available trading close in the selected period.
6. Use **Reset selections** to clear filters on your current page and return to the original default values.

The narrative descriptions and methodology pages remain read-only. All main analytical charts are live SVG rather than static screenshots. Some views cross-highlight selections instead of performing the identical cross-filter propagation of Power BI; native `.pbix` execution is not supported by GitHub Pages.

## Included files

- `index.html` — website application and interactive charts/selection logic.
- `data.js` — annual financial, segment and cash-flow observations, event-study observations and daily closing prices, built from project source data.
- `page-1.webp` through `page-9.webp` — exported original report pages used for visually faithful presentation.
- `LMT_Original_Report.pdf` — original report PDF, accessible through the website.
- `README.md` — research summary and site instructions.

## Methodology and limitations

Price returns are calculated from the recorded trading closes and **exclude dividends**. Trading sessions are counted from the assigned post-event trading session. Relative returns compare LMT's event-window price return with SPY and ITA for the same window, in percentage points. Ten selected events cannot establish a general relationship or isolate confounding information. Source histories and adjustments have the limitations described in the report. A corrected SPY close on April 20, 2026 is reflected in the website's price series.

Underlying information is sourced from Lockheed Martin earnings releases, Nasdaq price observations (with identified corrections and verification), and event references identified in the original report. Data publication may be subject to the original providers' licensing and redistribution requirements.

## Verification checklist

Before sharing on LinkedIn, open the **GitHub Pages website** rather than the GitHub repository's Code tab. The following should work:

- **Event Analysis:** select **5 sessions**; the share beating ITA changes from **70% at 10 sessions** to **80% at 5 sessions**, while the table and colored comparison bars redraw. Hover a bar for its exact value.
- **Event Analysis:** click *Fall of Kabul* in the event table; the share and median now reflect only that event. Click the row again to clear selection.
- **Financial Performance:** click the 2024 row; the selected year becomes highlighted across the financial charts, then click 2025.
- **Market Performance:** uncheck SPY; the SPY line disappears. Adjust the date range; the indexed series start at 100 within the new selected window.
- **Reset selections** clears all active filters.

Use a private/incognito browser window to check whether deployment is accessible without logging into GitHub. Depending on browser caching, you may need a hard refresh after the next commit. If the live link still shows screenshot-only visuals, check whether the updated `index.html` was committed in the root of the deployed `main` branch.

## Deployment

This is a static GitHub Pages project. Put all files in the **root** of the public repository `3lessing/LMT_Geopolitical_Analysis`. Under **Settings → Pages**, choose **Deploy from a branch**, `main`, and `/(root)`. GitHub will serve `index.html`. No npm install, paid hosting, database, Microsoft sign-in or credentials are needed to view the public site.

**Portfolio project by Blessing Nwotite.** Not financial or investment advice.
