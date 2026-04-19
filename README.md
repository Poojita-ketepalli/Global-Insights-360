# Business Insights 360 — Power BI Dashboard

## Project Overview

AtliQ Hardware is a fast-growing consumer electronics company selling products across brick-and-mortar stores and e-commerce platforms globally. As the business expanded, leadership relied on Excel-based reports that were slow, error-prone, and unable to support data-driven decisions at scale.

This project delivers a **multi-view Power BI dashboard** that gives stakeholders across Finance, Sales, Marketing, Supply Chain, and Executive leadership a single source of truth — enabling faster, smarter decisions.

---

## Live Dashboard

[View Live Dashboard](https://app.powerbi.com/groups/me/reports/9d8c07f6-ed46-40e9-a782-2d0894482502/03487d221010611c00ba?experience=power-bi) ← replace with your Power BI Service link

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Power BI Desktop | Dashboard development and DAX measures |
| DAX Studio | Performance optimization |
| Power Query | Data transformation and modelling |
| SQL | Data extraction from MySQL database |
| Excel / CSV | Secondary data source |

---

## Data Sources

- **MySQL Database** — transactional sales, finance, and supply chain data
- **Excel / CSV Files** — targets, market share, and supplementary data

Data was connected, cleaned, and transformed using Power Query before being modelled into a star schema inside Power BI.

---

## Dashboard Pages

### 1. Home Page
A navigation hub with buttons linking to each functional view. Designed for quick access across departments.

### 2. Finance View
Tracks Profit & Loss performance across markets, products, and customers.

**Key visuals:**
- P&L statement matrix based on selected year
- Stacked area chart showing Net Sales trend over time
- KPI cards for Net Sales, Gross Margin %, and Net Profit %
- Slicers for Year, Quarter, Region, Segment, and Customer

### 3. Sales View
Analyses customer and product performance to identify top contributors and underperformers.

**Key visuals:**
- Customer performance matrix — Net Sales vs Gross Margin %
- Product performance scatter chart
- Donut charts for regional sales mix
- Bar chart showing top/bottom customers by revenue

### 4. Marketing View
Evaluates product and segment performance to support marketing strategy.

**Key visuals:**
- Segment/product performance matrix with GM% and Net Profit %
- Waterfall chart showing Net Profit contribution by division
- Scatter charts for product-level performance analysis
- Pie chart for product category distribution

### 5. Supply Chain View
Monitors forecast accuracy, inventory risk, and supplier performance.

**Key visuals:**
- KPI cards for Forecast Accuracy %, Net Error, and Absolute Error
- Line and column combo chart — Forecast Accuracy vs Last Year trend
- Scatter chart for customer-level risk analysis
- Detailed accuracy table by product/segment

### 6. Executive View
A single-page summary for senior leadership with the most critical business metrics.

**Key visuals:**
- KPI cards — Net Sales, Gross Margin %, Net Profit %, Forecast Accuracy %
- Revenue contribution by channel (Retailer vs Direct vs Distributor)
- Ribbon chart — Top 5 customers and products by revenue share
- Line and column combo — Revenue and GM% trend over time
- Market share analysis — AtliQ vs competitors by region

## Data Model

Star schema design with:
- **Fact tables**: fact_sales_monthly, fact_forecast_monthly, fact_actual_estimates, post_invoice_deductions, manufacturing_cost, freight_cost, Operational Expenses, marketshare, Target
- **Dimension tables**: dim_customer, dim_product, dim_market, dim_date

---

## Performance Optimization

Used **DAX Studio** to:
- Identify slow-running measures using Server Timings
- Reduce unnecessary calculated columns
- Achieved 5% improvement in report load time
- Reduced data-related processing overhead by 20%

---

## Key Business Insights

- **Finance**: Identified markets with below-target Gross Margin % requiring cost review
- **Sales**: Top 5 customers contribute disproportionate share of revenue — retention priority
- **Marketing**: Certain product segments show high sales volume but negative net profit
- **Supply Chain**: Forecast accuracy gaps flagged for specific high-volume SKUs
- **Executive**: AtliQ's market share growth tracked against key competitors by region

---




**Skills demonstrated:**
- Multi-source data connection (MySQL + Excel)
- Star schema data modelling in Power BI
- Advanced DAX — CALCULATE, time intelligence, dynamic measures
- Cross-functional dashboard design for 5 business departments
- Performance tuning with DAX Studio


## Business & Finance Terms Learnt

Working on this project introduced key business and finance concepts used in real analytics roles. These terms appear across the dashboard and are essential for any data analyst working in a business or finance domain.

---

### Finance & P&L Terms

| Term | Full Form | Definition |
|---|---|---|
| P&L | Profit & Loss | A financial statement showing revenue, costs, and profit over a period. |
| Net Sales | — | Total revenue after deducting returns, allowances, and discounts. The top line of a P&L. |
| Gross Margin | GM | Net Sales minus Cost of Goods Sold (COGS). Shows how much profit is made before operating expenses. |
| GM % | Gross Margin % | Gross Margin divided by Net Sales × 100. A key profitability ratio — higher is better. |
| COGS | Cost of Goods Sold | Direct costs of producing the goods sold — raw materials, manufacturing, freight. |
| Net Profit | — | Revenue minus ALL expenses including COGS, operating costs, and taxes. The bottom line. |
| Net Profit % | NP % | Net Profit divided by Net Sales × 100. Shows overall profitability after all costs. |
| Operational Expense | OpEx | Day-to-day running costs — salaries, marketing, rent, utilities. Not directly tied to production. |
| Pre-invoice Deduction | — | Discounts agreed before the invoice is raised — typically volume-based or channel discounts. |
| Post-invoice Deduction | — | Deductions applied after invoicing — rebates, promotional allowances, returns. |
| Net Invoice Sales | — | Sales value after pre-invoice deductions are applied. |

---

### Time Intelligence Terms

| Term | Full Form | Definition |
|---|---|---|
| YTD | Year to Date | Cumulative value from the start of the current financial year to today. Used to track progress mid-year. |
| YTG | Year to Go | Remaining portion of the year — from today to the end of the financial year. |
| LY | Last Year | The same period in the previous financial year. Used for year-over-year (YoY) comparison. |
| BM | Benchmark | A reference point to compare performance against — could be last year, target, or industry average. |
| QTD | Quarter to Date | Cumulative value from the start of the current quarter to today. |
| MTD | Month to Date | Cumulative value from the start of the current month to today. |

---

### Sales & Market Terms

| Term | Full Form | Definition |
|---|---|---|
| NS | Net Sales | Total revenue after all deductions. Primary top-line metric. |
| GS | Gross Sales | Total revenue before any deductions. Rarely used as a final KPI. |
| Market Share % | — | A company's sales as a percentage of total industry sales in a market. AtliQ's share vs competitors. |
| Channel | — | The route through which products reach customers — Retailer, Direct, or Distributor. |
| Retailer | — | Third-party stores that sell AtliQ products to end consumers (e.g. Croma, Amazon). |
| Distributor | — | Intermediaries who buy in bulk from AtliQ and sell to smaller retailers. |
| Direct | — | AtliQ's own stores or website — selling directly to consumers without a middleman. |
| Region | — | Geographic grouping of markets — APAC, EU, NA, LATAM etc. |
| Segment | — | Customer classification — Notebook, Desktop, Peripherals, Networking, Storage, Accessories. |

---

### Supply Chain Terms

| Term | Full Form | Definition |
|---|---|---|
| Forecast Accuracy % | FA % | How closely actual sales matched the forecast. Higher % = better planning. Calculated as 1 - (Absolute Error / Forecast Quantity). |
| Net Error | — | Forecast Quantity minus Actual Sales. Positive = overforecast, Negative = underforecast. |
| Absolute Error | ABS Error | The absolute value of Net Error — always positive. Used to measure error magnitude regardless of direction. |
| Excess Inventory | EI | Stock held above what was needed — ties up working capital and increases storage cost. |
| Out of Stock | OOS | When actual demand exceeds available inventory — leads to lost sales. |
| Risk | — | In supply chain context: EI Risk (too much stock) vs OOS Risk (too little stock). |






