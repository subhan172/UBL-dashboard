# UBL Financial Analytics Dashboard

An interactive, single-file financial analytics dashboard for **United Bank Limited (PSX: UBL)**, Pakistan — covering financial years 2020 to 2025.

Built as a Power BI-style equity research dashboard using only HTML, CSS and vanilla JavaScript. No backend, no build step, no dependencies to install.

**Live demo:** `https://<your-username>.github.io/<your-repo>/`

---

## What it shows

Six sections, each answering a specific question about the bank:

| Section | Question it answers |
|---|---|
| Overview | How is UBL performing right now, in 30 seconds? |
| Financial Performance | Is income growing, and is profitability improving? |
| Balance Sheet | What does the bank own, and how is it funded? |
| Banking KPIs | Deposits, lending, asset quality, capital and efficiency |
| Shareholder & Stock | What has the share delivered to owners? |
| Insights | What the numbers say, what to watch, and the underlying data |

Contents:

- 40 KPI cards across financial, banking, shareholder and balance-sheet categories, each showing the current value, the prior period and the year-on-year change
- 25 interactive charts covering income, profit, earnings per share, dividends, returns, assets, deposits, advances, deposit mix, asset quality, capital adequacy, efficiency, share price and ownership
- Eight insights and ten watchlist flags generated from the dataset at runtime, not hard-coded text
- A year-on-year comparison table and the full six-year dataset with every metric labelled *reported* or *calculated*
- A methodology section listing sources, formulas and the metrics that were not available

## Interactions

- **Year filter** — drives the KPI cards, the mix charts, the insights and the comparison table
- **Headline trend filter** — switches the overview chart between eight metrics
- **KPI category filter** — shows financial, banking or shareholder cards
- **Cross-filtering** — click any year bar in a chart to change the selected year
- **Reset filters** — returns to the default FY2025 view
- **Dark mode** — charts and tokens re-render for the selected theme
- **Download report** — expands every section and opens the browser print dialogue for PDF export
- Tooltips on all series, keyboard focus states, and reduced-motion support

## Data

**Period:** FY2020 to FY2025 (calendar years ending 31 December)
**Basis:** Unconsolidated (bank only)
**Currency:** Pakistan Rupees, millions unless stated
**Per-share figures:** Restated for the June 2025 subdivision of one Rs 10 share into two Rs 5 shares

### Sources

| Data | Source |
|---|---|
| Six-year income statement, balance sheet, ratios and share data | UBL investor presentation, *Performance Highlights & Outlooks — December 2025* (published 14 April 2026) |
| FY2025 profit, earnings per share, dividend, capital ratios, Silk Bank merger | UBL Annual Report 2025 |
| Segment and geographic income, deposits by segment | UBL segment disclosures, FY2025 and FY2024 |
| Capital adequacy history, infection ratios, provisioning coverage | VIS Credit Rating Company rating report on UBL, 30 June 2025 |
| Share price, shares outstanding, ownership split, trailing figures | S&P Global Market Intelligence, via stockanalysis.com and Simply Wall St |
| Interim 2026 results and sector context | Company results notices to the PSX, reported by Business Recorder, ProPakistani and Dawn |

### Data integrity

No figure on this dashboard is invented. Every value is either reported by UBL or calculated on the page from reported values, and each is tagged accordingly in the interface.

Calculated metrics and their formulas:

```
Net interest margin proxy  = Net interest income / Average total assets
Net profit margin          = Profit after tax / Total income
Effective tax rate         = Taxation / Profit before tax
Current, savings, term     = Disclosed current-account and CASA ratios x Total deposits
Gross non-performing loans = Reported infection ratio x Gross advances
Provision coverage         = Provisions held against advances / Gross non-performing loans
Total shareholder return   = Price return + (Dividend for the year / Prior year-end price)
Market capitalisation      = Latest close x Shares outstanding
Price to book              = Latest close / FY2025 book value per share
```

Derived figures were reconciled against independently reported numbers before release: profit growth, deposit growth, effective tax rate, dividend yields, price-to-earnings, book value per share and the balance-sheet identities all tie back to UBL's own disclosures.

### Known gaps

These are stated in the dashboard rather than filled with estimates:

- UBL's reported net interest margin on average earning assets — a proxy on average total assets is shown instead
- Deposit mix before FY2024
- Loan book by customer segment for FY2025 — business-segment splits are shown instead
- A daily or monthly share price series — annual high, low and close are shown
- Ownership as at a stated date — the provider does not disclose a reporting date
- Rolling 52-week high and low — calendar-year high and low are shown

### Important context for FY2025

Silk Bank was amalgamated into UBL with effect from 11 March 2025, so FY2025 is not fully like-for-like with FY2024. The share subdivision in June 2025 means all per-share history is restated: FY2024 earnings per share appears as Rs 32.89 rather than the Rs 65.78 reported at the time.


## Licence

The code in this repository is released under the MIT Licence. The underlying financial data belongs to United Bank Limited and the other sources listed above, and is reproduced here for analysis and education.

## Disclaimer

This dashboard is not investment advice and is not affiliated with or endorsed by United Bank Limited. Financial data should be independently verified against UBL's audited financial statements before any investment decision.
# UBL-dashboard
