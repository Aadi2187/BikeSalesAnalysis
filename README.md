# 🚴 Bike Sales Analysis – Power BI Dashboard

An interactive Power BI report that analyses bike sales performance across products, categories, regions, customers and time. It covers revenue, profit, orders, returns and target tracking, with time-intelligence measures such as YTD, QTD, MTD and rolling revenue.

![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Measures-blue)
![Status](https://img.shields.io/badge/status-complete-brightgreen)

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Business Questions Answered](#-business-questions-answered)
- [Data Model](#-data-model)
- [Key Measures (DAX)](#-key-measures-dax)
- [Report Pages](#-report-pages)
- [Dashboard Preview](#-dashboard-preview)
- [How to Use](#-how-to-use)
- [Repository Structure](#-repository-structure)
- [Tools & Skills Demonstrated](#-tools--skills-demonstrated)
- [Author](#-author)

---

## 📖 Project Overview

This project analyses sales data for a bike retailer. The goal is to turn raw transactional data into a clear, interactive dashboard that helps decision-makers understand:

- How the business is performing against its revenue targets
- Which product categories, models and colours drive sales and profit
- Where returns are highest, by product and by country
- How sales behave over time (yearly, quarterly, monthly, weekday vs. weekend)

## ❓ Business Questions Answered

- What are the total **revenue, expenses and profit**?
- How does **actual revenue compare to target revenue** over time?
- Which **categories and models** sell the most?
- What is the **return rate**, and which products or countries have the highest?
- How do **weekday vs. weekend** orders compare?
- How do **bulk orders vs. regular orders** compare?
- Which **countries/territories** generate the most revenue?
- How do sales differ by **customer gender** and **product colour**?

## 🗂 Data Model

The report uses a star-schema style model with one main fact table, lookup tables and a dedicated measures table.

| Table | Type | Description |
|---|---|---|
| `SalesRecord` | Fact | Order-level sales transactions (quantity, territory, product, date) |
| `Returns` | Fact | Returned items and return quantities |
| `Products` | Dimension | Product name, model name, colour and subcategory link |
| `ProductSubcategories` | Dimension | Product subcategories |
| `ProductCategories` | Dimension | Product categories (e.g. Bikes, Accessories) |
| `Customers` | Dimension | Customer details, including gender |
| `Territories` | Dimension | Sales territories and countries |
| `Calendar` | Dimension | Date table with Year, Quarter, Month and `IsWeekend?` flag |
| `Measure Table` | Measures | Holds all DAX measures used in the report |

## 🧮 Key Measures (DAX)

**Sales & Profitability**
- `Revenue`, `Expenses`, `Profit`
- `QuantitySold`, `Bike Sold`, `Red Color Qty Sold`

**Orders**
- `Total Orders`, `All Orders`
- `Weekday Orders`, `Weekend Orders`
- `Total Bulk Orders`, `Total Regular Order`

**Returns**
- `Total Returns`, `All Returns`, `Bike Returns`
- `Return Rate %`, `Bike Return Rate`
- `% of All Orders`, `% Of All Returns`

**Time Intelligence & Targets**
- `Target Revenue`
- `YTD Revenue`, `QTD Revenue`, `MTD Revenue`
- `Previous Month Revenue`
- `10 Days Rolling Revenue`

## 📊 Report Pages

The report contains 17 pages:

| # | Page | Focus |
|---|---|---|
| 1 | Page 1 | Overview KPIs: revenue, expenses, profit, orders, weekday/weekend split |
| 2 | Page 2 | Returns analysis: return rate by product, category and country |
| 3 | Time-Intelligence-1 | Revenue vs. target KPI, YTD/QTD/MTD, rolling revenue |
| 4 | Target Revenue by Month | Revenue vs. target trend by category |
| 5 | Quantity sold by Year | Quantity sold, absolute and 100% stacked by category |
| 6 | YTD Revenue and Target Revenue by Month | YTD and QTD revenue against target |
| 7 | Map Visual | Revenue and return rate by country |
| 8 | Total Order and Total Return | Orders vs. returns by category |
| 9 | Total Order by Model name and Category Name | Orders by model, with category slicer |
| 10 | Total Orders and Weekday Orders by Category name | Weekday vs. total orders |
| 11 | Revenue and Profit by Category Name | Revenue and profit comparison |
| 12 | Profit by Year and Quarter | Profit trend over time |
| 13 | Bike Sold by Year and Quarter | Bikes sold trend |
| 14 | Bike sold and red color | Red-colour bike share of sales |
| 15 | Bike Sold by Model Name | Bikes sold per model |
| 16 | Customer & Colour Analysis | Orders and bulk orders by gender, quantity by colour |
| 17 | Category Ranking | Ribbon chart by category |

**Visual types used:** KPI cards, line, clustered/stacked column, area, ribbon, combo, bar charts, map, matrix/pivot tables and slicers.

## 🖼 Dashboard Preview

![Overview](screenshots/overview.png)
![Returns Analysis](screenshots/returns.png)
![Time Intelligence](screenshots/time-intelligence.png)

## 🚀 How to Use

1. **Clone or download** this repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   ```
2. **Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/)** (free, Windows only).
3. Open `BikeSalesAnalysis.pbix`.
4. Use the page tabs at the bottom to navigate, and the slicers (date, category, colour) to filter the data interactively.

> **Note:** If Power BI shows a data-source error, go to **Home → Transform data → Data source settings** and point the sources to your local data files.

## 📁 Repository Structure

```
├── BikeSalesAnalysis.pbix   # Power BI report file
├── screenshots/             # Dashboard images used in this README
└── README.md
```

## 🛠 Tools & Skills Demonstrated

- **Power BI Desktop**: report design and interactive dashboards
- **Data modelling**: star schema, relationships, dedicated measure table
- **DAX**: time intelligence (YTD, QTD, MTD, rolling averages), ratios, conditional measures
- **Data visualisation**: choosing the right chart for each question, slicers and drill-downs
- **Business analysis**: KPI tracking against targets, returns analysis, regional performance






⭐ If you found this project useful, consider giving it a star!
