# 📊 Retail Store Sales Analysis — Advanced Excel Mini Project

> **Platform:** Agileology (EdTech & Upskilling Platform)
> **Submitted By:** Vathada Swaroop Kumar
> **Duration:** Mar 15, 2026 – Mar 18, 2026
> **Tool Used:** Microsoft Excel (Advanced)

---

## 📌 Project Overview

This project was completed as part of the Advanced Excel Mini Project
assigned by Agileology. It involves end-to-end data analysis of a
Retail Store Sales dataset containing 12,575 records using Microsoft
Excel — covering data cleaning, advanced formulas, pivot tables,
advanced charts and an interactive KPI dashboard.

---

## 📁 Repository Files

| File | Description |
|------|-------------|
| `retail_store_sales.xlsx` | Complete project workbook with all 7 sheets |
| `Raw_retail_Store_sales_data.xlsx` | Original raw dataset (12,575 records, 11 columns) |
| `Adv_Excel_Project_Documentation.pdf` | Full project documentation (7 pages) |
| `Adv_Excel_Case_Scenario.pdf` | Instructor case scenario and requirements |

---

## 🗂️ Dataset Description

| Detail | Info |
|--------|------|
| Total Records | 12,575 rows |
| Total Columns | 11 (original) → 15 (after cleaning) |
| Date Range | January 2022 — January 2025 |
| Unique Customers | 25 |
| Categories | 8 (Butchers, Beverages, Food, Furniture, Patisserie, Milk Products, Electric Household Essentials, Computers & Electric Accessories) |
| Payment Methods | Cash, Credit Card, Digital Wallet |
| Locations | Online, In-store |

---

## 📂 Workbook Sheet Structure

| Sheet | Purpose |
|-------|---------|
| `Raw_Data` | Original untouched dataset — never modified |
| `Cleaned_Data` | Cleaned data with 15 columns including 4 helper columns |
| `Data_Analysis` | All formulas, functions and array calculations |
| `Pivot_Summary` | 4 Pivot Tables, calculated field, 3 pivot charts, slicers and timeline |
| `Advanced_Charts` | Combo Chart, Sparklines and Waterfall Chart |
| `Dashboard` | Interactive KPI Dashboard with linked charts and slicers |
| `Documentation` | Full project documentation sheet inside workbook |

---

## 🧹 Data Cleaning Steps

| Step | Action | Records Fixed |
|------|--------|--------------|
| 1 | Protected Raw_Data — copied to Cleaned_Data sheet | — |
| 2 | Converted to Excel Table named SalesData (Ctrl+T) | — |
| 3 | Checked duplicates — zero duplicates found | 0 |
| 4 | Fixed blank cells in Discount Applied → FALSE | 4,199 |
| 5 | Fixed blank cells in Item → "Unknown" | 1,213 |
| 6 | Fixed blank cells in Price Per Unit → 0 | 609 |
| 7 | Fixed blank cells in Quantity & Total Spent → 0 | 604 |
| 8 | Added helper column: Month (=TEXT formula) | 12,575 |
| 9 | Added helper column: Year (=YEAR formula) | 12,575 |
| 10 | Added helper column: Month-Year combined label | 12,575 |
| 11 | Added Sales Tier using Nested IF (High/Medium/Low) | 12,575 |

---

## 🔢 Advanced Formulas & Functions Used

| Formula / Function | Category | Purpose |
|--------------------|----------|---------|
| `=SUM(SalesData[Total Spent])` | Aggregate | Total revenue — Result: $1,552,071 |
| `=AVERAGE(SalesData[Total Spent])` | Aggregate | Average order value — Result: $129.65 |
| `=COUNTA(SalesData[Transaction ID])` | Aggregate | Total transactions — Result: 12,575 |
| `=COUNTA(UNIQUE(SalesData[Customer ID]))` | Dynamic Array | Unique customers — Result: 25 |
| `=COUNTIF(SalesData[Discount Applied],TRUE)` | Conditional | Discounted orders — Result: 4,219 |
| `=SUMIF(SalesData[Category],"Butchers",SalesData[Total Spent])` | Conditional | Sales per category |
| `=COUNTIF(SalesData[Category],"Beverages")` | Conditional | Orders per category |
| `=SUMIFS(SalesData[Total Spent],SalesData[Location],"Online",SalesData[Year],2024)` | Multi-condition | Online sales 2024 — Result: $265,246.50 |
| `=XLOOKUP(B51,SalesData[Transaction ID],SalesData[Total Spent],"Not Found")` | Lookup | Transaction lookup by ID |
| `=UNIQUE(SalesData[Category])` | Dynamic Array | All unique categories |
| `=SORT(UNIQUE(SalesData[Category]))` | Dynamic Array | Sorted unique categories |
| `=FILTER(SalesData[Item],SalesData[Total Spent]>500)` | Dynamic Array | High value transactions |
| `=LARGE(SalesData[Total Spent],{1,2,3,4,5})` | Dynamic Array | Top 5 sales values |
| `=IF([@[Total Spent]]>500,"High",IF([@[Total Spent]]>200,"Medium","Low"))` | Logical | Sales tier classification |
| `=TEXT([@[Transaction Date]],"MMMM")` | Date/Text | Extract month name |
| `=YEAR([@[Transaction Date]])` | Date/Text | Extract year number |
| `=TEXT([@[Transaction Date]],"MMM-YYYY")` | Date/Text | Month-Year label |

---

## 📊 Pivot Tables & Charts

| Pivot Table | Rows | Values | Filter | Chart |
|-------------|------|--------|--------|-------|
| PT1 — Sales by Category | Category | SUM of Total Spent + Avg Sale Value (Calculated Field) | Year | Clustered Column |
| PT2 — Monthly Sales Trend | Month-Year | SUM of Total Spent | Category | Line Chart |
| PT3 — Payment Method | Payment Method | SUM of Total Spent | Location | Pie Chart |
| PT4 — Online vs In-Store | Location | COUNT of Transaction ID | Year | Column Chart |

**Interactive Features:**
- 3 Slicers — Category, Location, Payment Method (connected to all 4 Pivot Tables)
- 1 Transaction Date Timeline (connected to all 4 Pivot Tables)

---

## 📈 Advanced Charts

| Chart | Data Used | Purpose |
|-------|-----------|---------|
| Combo Chart | Category vs Total Sales + Order Count | Compare sales value and order volume on dual axes |
| Sparklines | Monthly Total Spent values | Mini trend lines showing monthly patterns inline |
| Waterfall Chart | Month-Year vs Total Spent | Visualize monthly revenue gains and losses |

---

## 🧮 Data Analysis Tools

| Tool | How Used |
|------|---------|
| Goal Seek | Determined what Total Spent value is needed to reach $200,000 target revenue |
| Scenario Manager | Built 3 scenarios — Low Sales ($50), Base Sales ($200), High Sales ($500) |

---

## 📉 Key Findings & Insights

| # | Finding | Result |
|---|---------|--------|
| 1 | **Total Revenue** | $1,552,071 across 3 years (2022–2025) |
| 2 | **Highest Selling Category** | Butchers — $208,118 |
| 3 | **Lowest Selling Category** | Milk Products — $180,112 |
| 4 | **Top Payment Method** | Cash — $537,710 |
| 5 | **Online vs In-Store** | Online (6,354) slightly exceeded In-Store (6,221) |
| 6 | **Peak Month** | January 2022 — $52,911.50 |
| 7 | **Avg Order Value** | $129.65 per transaction |
| 8 | **Discounted Orders** | 4,219 (33.5% of all orders) |
| 9 | **Discounted Beverages Sales** | $67,696 |
| 10 | **Credit Card Online Sales** | $260,851 |

---

## 🎯 Skills Demonstrated

- ✅ Data Cleaning & Transformation
- ✅ Advanced Formulas (SUMIFS, XLOOKUP, Dynamic Arrays, Nested IF)
- ✅ Pivot Tables with Calculated Fields
- ✅ Interactive Slicers & Timeline
- ✅ Advanced Charts (Combo, Sparklines, Waterfall)
- ✅ KPI Dashboard Design
- ✅ What-If Analysis (Goal Seek, Scenario Manager)
- ✅ Data Documentation

---

## 👤 Author
**Vathada Swaroop Kumar**

- LinkedIn: [Swaroop Kumar Vathada](https://www.linkedin.com/in/swaroopkumarvathada)

  Platform: Agileology (EdTech & Upskilling Platform)
  Advanced Excel Mini Project — Retail Store Sales Analysis
