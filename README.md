# 📊 Sales & Customer Insights Dashboard

> A Power BI project analyzing sales performance, customer behavior, and regional trends using real-world structured data.

---

## 🗂️ Project Overview

This project simulates a business intelligence solution for a retail company. It covers the full data analytics pipeline — from raw data preparation in Excel to interactive dashboard design in Power BI.

**Tools Used:** Power BI · Excel · SQL · Power Query · DAX

---

## 📁 Files

| File | Description |
|------|-------------|
| `Sales_Dashboard_Data.xlsx` | Dataset with 200 orders across 5 sheets |
| `PowerBI_Dashboard_Mockup.html` | Interactive dashboard mockup (open in browser) |

---

## 📋 Dataset Structure

The Excel file contains **5 sheets**:

| Sheet | Content |
|-------|---------|
| `Sales_Data` | 200 orders — product, customer, region, revenue, profit |
| `Monthly_Summary` | Revenue & profit aggregated by month |
| `Category_Analysis` | Performance breakdown by product category |
| `Region_Analysis` | Sales metrics by region |
| `KPI_Dashboard` | Key metrics summary |

---

## 📈 Dashboard Features

- **KPI Cards** — Total Revenue, Total Profit, Total Orders, Avg Order Value
- **Line Chart** — Monthly revenue & profit trend (Jan–Dec 2024)
- **Donut Chart** — Revenue distribution by product category
- **Bar Chart** — Revenue comparison across 5 regions
- **Top Products Table** — Top 5 products ranked by revenue
- **Profit Margin Gauge** — Visual indicator of overall profitability

---

## 💡 Key Insights

- 📦 **Electronics** is the top-performing category at **38%** of total revenue
- 🌍 **North region** leads in sales with **158K SAR**
- 💻 **Laptop** is the best-selling product with **98.4K SAR** revenue
- 📅 Revenue shows a consistent **upward trend** throughout 2024
- 💰 Overall **profit margin: 30.4%**

---

## 🔧 How to Reproduce in Power BI

1. Open **Power BI Desktop**
2. Click **Get Data → Excel** and import `Sales_Dashboard_Data.xlsx`
3. Load all 5 sheets
4. Use `Sales_Data` as the main fact table
5. Build relationships on: `Month`, `Category`, `Region` columns
6. Create the following visuals:
   - **Card** visuals for KPIs
   - **Line Chart** using `Monthly_Summary`
   - **Donut Chart** using `Category_Analysis`
   - **Bar Chart** using `Region_Analysis`
   - **Table** for top products
7. Add **Slicers** for Region and Category filtering

---

## 📐 DAX Measures

```dax
Total Revenue = SUM(Sales_Data[Revenue])

Total Profit = SUM(Sales_Data[Profit])

Profit Margin % = DIVIDE([Total Profit], [Total Revenue], 0)

Avg Order Value = DIVIDE([Total Revenue], DISTINCTCOUNT(Sales_Data[Order_ID]), 0)

Revenue Growth % = 
DIVIDE(
    [Total Revenue] - CALCULATE([Total Revenue], PREVIOUSYEAR('Date'[Date])),
    CALCULATE([Total Revenue], PREVIOUSYEAR('Date'[Date])),
    0
)
```

---

## 👩‍💻 Author

**Aryam Mohammed Almohammedi**  
Management Information Systems · Taibah University  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/aryam-mis)

---

> 📌 *This is a personal project built independently to apply and showcase skills in Power BI, Excel, and business intelligence.*
