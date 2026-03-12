# Sales Performance & Risk Analysis
### Acme Co. | US Sales Analytics | 2014-2017

---

## Project Overview

An end-to-end analytics project examining four years of sales data for
Acme Co., a multi-region US sales organization. The analysis evaluates
revenue and profit trends, product and channel performance, geographic
distribution, budget variance, and portfolio concentration risk -
resulting in strategic recommendations for leadership.

---

## Business Questions

1. How has revenue and profitability evolved from 2014-2017?
2. Which products and channels drive the largest share of revenue and profit?
3. Are there geographic performance disparities across regions?
4. Did the organization meet its 2017 budget targets?
5. Is revenue exposure concentrated in a small subset of products or customers?

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Python (pandas, numpy) | Data loading, cleaning, enrichment, feature engineering |
| Python (matplotlib, seaborn) | Exploratory analysis and visualization |
| Power BI (DAX, Data Modeling) | Interactive dashboard and KPI calculations |
| Jupyter Notebook (VS Code) | End-to-end analytical workflow |

---

## Dataset

Acme Co. USA Regional Sales Data (2014-2018)

| Table | Description | Rows |
|---|---|---|
| Sales Orders | Core transaction fact table | 64,104 |
| Products | Product name lookup | 30 |
| Customers | Customer name lookup | 175 |
| Regions | Delivery region attributes | 993 |
| State Regions | State-to-macro-region mapping | 48 |
| Budget 2017 | Product-level revenue targets | 30 |

**Analysis scope:** 2014-2017 (61,626 records).
2018 excluded - partial year (January-February only).

**Data Grain:**
Each order contains six product-line records due to multiple
delivery region allocations per order.
```
Grain: OrderNumber + OrderDate + Delivery Region Index
```
---

## Analytical Scope

| Stage | Analysis |
|---|---|
| Data preparation | Loading, grain validation, data quality checks |
| Feature engineering | Revenue, cost, profit, margin |
| Data modeling | Dimension merging - products, customers, regions |
| Performance analysis | Revenue and margin trends |
| Product & channel analysis | Profitability and mix |
| Geographic analysis | Regional and macro-region performance |
| Budget analysis | 2017 variance vs targets |
| Risk analysis | Product and customer concentration |
| Executive summary | Strategic insights and recommendations |

---

## Key Findings

| Dimension | Finding | Risk Level |
|---|---|---|
| Revenue trend | Stable 2014-2016; mild decline in 2017 (-1.5% from peak) | Low |
| Profit margin | 37.3%-37.5% weighted; zero erosion across 4 years | Low |
| Product mix | Product margins show minimal variation across the portfolio | Low |
| Channel mix | Margins are highly consistent across Wholesale, Distributor, and Export channels | Low |
| Regional concentration | 993 regions; top region < 0.2% of revenue | Very Low |
| Macro-region | West leads (30%); Northeast lags (17%) - volume gap only | Low-Medium |
| Budget performance | +17% outperformance in 2017; 28 of 30 products exceeded target | Positive |
| Portfolio concentration | Top 10 products = ~60% revenue; no single-product dependency risk | Moderate |
| Customer concentration | Top 10 customers = 8.84% revenue; highly fragmented | Very Low |

---

## Strategic Recommendations

1. **Prioritise volume growth over margin improvement** - margins are
   structurally stable; any performance improvement must come from volume.
2. **Investigate the Northeast gap** - uniform margins confirm this is
   a market penetration opportunity, not a profitability issue.
3. **Scale top-revenue products** - top 10 products generate ~60% of
   revenue; scaling them proportionally lifts total profit.
4. **Confirm budget periodicity with Finance (quarterly vs annual)**
   before operational reporting - variance figures change materially
   depending on this interpretation.
5. **Investigate 2 underperforming products** - root-cause analysis
   warranted before next planning cycle.
6. **Monitor West macro-region** - 2017 revenue decline in the
   highest-contributing territory warrants attention.

---

## Power BI Report - 5 Pages

| Page | Purpose |
|---|---|
| 1. Executive Overview | Revenue, profit, margin trends and seasonality |
| 2. Product & Channel Performance | Top products, margin distribution, channel mix |
| 3. Regional Performance | Geographic distribution, macro-region analysis, state map |
| 4. Budget vs Actual 2017 | Variance analysis - 28/30 products exceeded target |
| 5. Portfolio Risk & Concentration | Product and customer concentration risk |

---

## Dashboard Preview

### Page 1 — Executive Overview
![Executive Overview](page1_executive_overview.png)

### Page 2 — Product & Channel Performance
![Product & Channel](page2_product_channel.png)

### Page 3 — Regional Performance
![Regional Performance](page3_regional_performance.png)

### Page 4 — Budget vs Actual 2017
![Budget vs Actual](page4_budget_vs_actual.png)

### Page 5 — Portfolio Risk & Concentration
![Portfolio Risk](page5_portfolio_concentration.png)


## Repository Structure
```
sales-performance-risk-analysis/
├── sales_performance_risk_analysis.ipynb
├── regional_sales_dataset.xlsx
├── sales_performance_report.pbix
├── screenshots/
│   ├── page1_executive_overview.png
│   ├── page2_product_channel.png
│   ├── page3_regional_performance.png
│   ├── page4_budget_vs_actual.png
│   └── page5_portfolio_concentration.png
└── README.md
```

---

## How to Run

**Requirements:**
```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

**Open in VS Code:**
- Install the Jupyter extension in VS Code
- Open `sales_performance_risk_analysis.ipynb`
- Update `file_path` in Section 3 to point to your local
  copy of `regional_sales_dataset.xlsx`
- Run all cells top to bottom

**Power BI Report:**
Open `sales_performance_report.pbix` in Power BI Desktop.
Update the data source path to your local dataset if prompted.
```
---

## Author

**Harish Patil**
MBA (Marketing & HR) | Data Analytics

Combining a business management background with hands-on 
data analytics — this project demonstrates end-to-end 
analytical workflow from raw data validation and exploratory 
analysis through to executive reporting in Power BI.

[LinkedIn](linkedin.com/in/harish-patil23) · [GitHub](https://github.com/HarishPatil23)
```

---
