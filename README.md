# Dashboard Design

## Objective
Design an interactive dashboard for business stakeholders that surfaces 
sales, profit, and growth signals at a glance, and supports drill-down into state, category, and customer-level detail.

## Tool
Power BI Desktop (free)

## Dataset
Indian e-commerce Sales & Financial dataset (sourced from Kaggle) — 
order-level records across states, product categories, sub-categories, customers, and payment modes.

## KPIs Selected
| KPI | Value | Why it's here |
|---|---|---|
| Total Amount | ₹438K | Headline revenue figure |
| Total Profit | ₹37K | Profitability, not just top-line |
| Total Quantity | 5,615 | Volume signal, pairs with revenue |
| Average Profit | 24.64 | Per-order profitability health check |

Growth is represented dynamically through the **Profit by Month** trend line rather than a single static card, 
so stakeholders can see month-over-month movement directly.

## Dashboard Features
- **KPI cards** with icon accents for totals/summary
- **Slicers**: Quarter (Qtr 1–4) button slicer + State dropdown, both filter every visual
- **Time-series analysis**: Profit by Month bar chart
- **Category & payment breakdowns**: donut charts for category mix and payment mode split
- **Geographic comparison**: horizontal bar chart ranking all states by revenue
- **Consistent color theme**: navy/purple base with a single orange accent
- **Customer & sub-category views**: top customers by amount, profit by sub-category

## Key Insights
- Madhya Pradesh (₹7.38K) and Maharashtra (₹6.96K) lead revenue by state
- Clothing dominates category mix at 63% of quantity sold
- COD (44%) and UPI (21%) together cover two-thirds of payment volume
- **Rajasthan is currently unprofitable** (-₹0.32K) despite positive revenue — flagged for investigation
- Profit turned negative in **May, July, August, September, and December** — a recurring dip worth a seasonal review
- Printers (₹8.6K) and Bookcases (₹6.5K) are the strongest sub-categories by profit

## Outcome
This project reinforced how a small set of well-chosen KPIs, paired with interactivity and a disciplined color theme, 
turns raw transactional data into a dashboard business stakeholders can actually act on.


5. **Making a dashboard interactive**: Adding slicers/filters, cross-filtering between visuals, drill-through pages, bookmarks/buttons for navigation, and tooltips.
6. **Handling large datasets**: Use Import mode with proper data modeling (star schema), aggregate/summarize where possible, use DirectQuery for very large sources, remove unused columns, and optimize DAX measures.
7. **Chart types for trend analysis**: Line charts and column/bar charts for time-series; area charts when showing cumulative volume; combo charts when comparing two related trends (e.g., sales vs. profit) on one visual.
