# Geographic Distribution of VA Expenditures — FY 2024

**Live dashboard:** https://kevinrcartercodes.github.io/VA_Test/

> **Built by Kevin Carter.** This is a sample of what Claude can build in ~10 minutes — going from a raw government XLS file to a fully interactive, accessible, and publicly hosted dashboard. This is **not an official VA product** and is not affiliated with or endorsed by the U.S. Department of Veterans Affairs.

An interactive, single-page dashboard visualizing how the U.S. Department of Veterans Affairs distributed **$295.5 billion** in expenditures across all 50 states, DC, Puerto Rico, and Guam during Fiscal Year 2024.

## What's in the Dashboard

| Section | What it shows |
|---|---|
| **FY 2024 at a Glance** | KPI cards for total, direct ($154.5B), and indirect ($141.0B) expenditures |
| **Key Insights** | Callout cards highlighting spending concentration, risks (Medical Care at 88% of indirect, PACT Act growth pressure), and opportunities (education investment models) |
| **How VA Dollars Are Spent** | Donut charts + proportional treemap breaking down direct vs. indirect benefit categories |
| **State-Level Analysis** | Interactive tabs with 8 charts (top-20 bars, stacked comparisons, ratio analysis, category breakdowns) plus a sortable/searchable data table of all 53 jurisdictions |
| **Risks & Opportunities** | Strategic observations: rural access gaps, construction spending disparities, loan guaranty underutilization |

## Data Source

[GDX FY 2024](https://www.va.gov/vetdata/expenditures.asp) — Geographic Distribution of VA Expenditures, prepared by the National Center for Veterans Analysis and Statistics (September 2025). All figures are in thousands of dollars ($000s).

## Tech

- Single self-contained `index.html` — no build step, no backend
- [Chart.js 4.4](https://www.chartjs.org/) via CDN for all visualizations
- VA Design System color tokens and typography (Source Sans / Bitter)
- Section 508 accessible: skip nav, focus styles, ARIA labels on all charts, keyboard-navigable tabs

## Running Locally

```bash
open index.html
```

That's it. All data is embedded inline; no server or internet connection required (aside from the CDN fonts/Chart.js — those will fail gracefully offline).

## Notes

- FY 2024 is the first year Memorial Benefits and DIC/Survivors Pension appear as separate categories in GDX
- State expenditures are attributed by Veteran residence (for individual programs) or place of performance (for construction)
- This data may not reconcile directly with other VA financial reports due to differing inclusion criteria
