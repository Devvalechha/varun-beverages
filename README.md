# Budget vs Actual Financial Analysis Varun Beverages Ltd.

This is an FP&A-style financial model I built in Excel using 5 years of Varun Beverages' historical financials (2021-2025), forecasting 3 years forward (2026-2028). The goal wasn't just to project numbers — it was to actually understand what's driving the company's growth (volume or price), how that flows through to profitability, and how sensitive the forecast is to a couple of key assumptions. 

Data is sourced from publicly available financial statements, but the assumptions and forecasting logic are my own.

---

## What This Model Covers

*   **Historical:** Revenue, Volume, and Realization trend analysis (2021-2025)
*   **Price vs Volume Variance:** Decomposition breaking down why revenue moved
*   **Driver-based 3-year forecast:** Revenue, COGS, Employee Cost, Other Opex, EBITDA
*   **EBITDA Ratios:** Margin, Revenue Growth, EBITDA Growth, and Operating Leverage ratios
*   **Balance Sheet Metrics:** Return on Equity and Debt to Equity for historical years
*   **Sensitivity Analysis:** A 2-variable EBITDA sensitivity table (Volume Growth vs COGS %)
*   **Executive Summary:** With key takeaways

---

## Sheet Structure

| Sheet | What's in it |
| :--- | :--- |
| **Executive Summary** | Key findings and takeaways start here |
| **Dashboard** | Charts, ratio table, and the sensitivity heatmap |
| **Ratio Analysis** | Revenue/EBITDA growth, margins, ROE, D/E |
| **Assumptions** | The drivers feeding the 3-year forecast |
| **Calculations** | The actual forecast engine Sections A, B, and C |
| **Raw Data** | Cleaned P&L base the model runs off |
| **Data Sheet** | Full raw financial data (source, not for direct reading) |

---

## Key Findings

*   **Revenue** grew from ₹8,823 Cr (2021) to ₹21,685 Cr (2025) roughly 2.5x, a ~25% CAGR.
*   **Almost all of that growth** came from volume, not price. Sales volume nearly doubled (569 → 1,213 million cases) while realization per case only moved about 15% over the same period.
*   **Net profit** grew even faster than revenue (4.4x vs 2.5x), which means margins expanded along the way, not just the topline.
*   **EBITDA margin** has settled at around 23% in the most recent years, which lines up with the forecast assumption, so the historical base and the forward-looking model are consistent.
*   **Best case vs worst case** in the sensitivity table shows almost a 2x swing in EBITDA just from Volume Growth and COGS% moving a few points. Profitability here is genuinely sensitive to both levers.

---

## Auditing My Own Model

Before finalizing this, I went back through every formula and found a few real issues:

*   **Understated Other Operating Expenses:** The historical P&L was only pulling 3 of 7 actual expense line items — Raw Material, Employee Cost, and one small "Other Expenses" line — while Power & Fuel, Other Manufacturing Expenses, and Selling & Admin (one of the largest cost lines in the business) were never linked in. This alone was overstating historical EBITDA margin by around 20 percentage points — the sheet was showing ~44% margin when the real number is closer to 23%. Traced it back to the source data and fixed the formulas to pull every relevant expense line.
*   **Broken chart references:** A couple of series on the dashboard charts were pointing to deleted cells (`#REF!` errors), most likely left over from an earlier version of the sheet. Re-linked them to the correct ranges.
*   **A variance formula copy-paste error:** One cell in the Price Variance calculation was multiplying by price instead of volume, breaking the usual variance formula pattern used everywhere else in that section. Fixed to match the correct logic.

> I'm keeping this section in on purpose. Catching your own mistakes is part of the job, not something to hide.

---

## Note on Balance Sheet Ratios

ROE and Debt to Equity are calculated for historical years but left blank for the forecast years this model only projects the P&L forward, not a full Balance Sheet, so there's no forecasted Equity or Borrowings figure to calculate those ratios from. Rather than fill those cells with a rough guess, I left them out.

---

## Disclaimer

Built for learning and portfolio purposes. Not investment advice, and shouldn't be treated as an official analysis of Varun Beverages Ltd.

---

## Connect

Open to feedback feel free to raise an issue, or reach out on [LinkedIn](https://www.linkedin.com/in/dev-valechha-48467928a/).
