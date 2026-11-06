# 🚴 Bike Sales Analysis – Power BI Dashboard

An interactive Power BI report that analyses bike sales performance across products, categories, regions, customers and time. It covers revenue, profit, orders, returns and target tracking, with time-intelligence measures such as YTD, QTD, MTD and rolling revenue.

![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Measures-blue)

---

## 📖 Project Overview

This project analyses sales data for a bike retailer and turns it into an interactive dashboard covering:

- Performance against revenue targets
- Sales and profit by product category, model and colour
- Returns by product and country
- Sales trends by year, quarter, month and weekday vs. weekend

## 🗂 Data Model

| Table | Type | Description |
|---|---|---|
| `SalesRecord` | Fact | Order-level sales transactions |
| `Returns` | Fact | Returned items and quantities |
| `Products` | Dimension | Product name, model, colour |
| `ProductSubcategories` | Dimension | Product subcategories |
| `ProductCategories` | Dimension | Product categories |
| `Customers` | Dimension | Customer details, including gender |
| `Territories` | Dimension | Sales territories and countries |
| `Calendar` | Dimension | Date table with Year, Quarter, Month, `IsWeekend?` |
| `Measure Table` | Measures | All DAX measures |

## 🧮 Key Measures (DAX)

- **Sales:** `Revenue`, `Expenses`, `Profit`, `QuantitySold`, `Bike Sold`, `Red Color Qty Sold`
- **Orders:** `Total Orders`, `All Orders`, `Weekday Orders`, `Weekend Orders`, `Total Bulk Orders`, `Total Regular Order`
- **Returns:** `Total Returns`, `All Returns`, `Bike Returns`, `Return Rate %`, `Bike Return Rate`, `% of All Orders`, `% Of All Returns`
- **Time intelligence:** `Target Revenue`, `YTD Revenue`, `QTD Revenue`, `MTD Revenue`, `Previous Month Revenue`, `10 Days Rolling Revenue`

---

## 🖼 Dashboard Preview

### 1. Overview KPIs
Revenue, expenses, profit, orders and weekday/weekend split.

![Overview KPIs](screenshots/01-overview-kpis.png)

### 2. Returns Analysis
Returns by product, category and country, with return rate KPIs.

![Returns Analysis](screenshots/02-returns-analysis.png)

### 3. Time Intelligence
Revenue vs. target with YTD, QTD, MTD and rolling revenue.

![Time Intelligence](screenshots/03-time-intelligence.png)

### 4. Revenue vs. Target Revenue by Month

![Target Revenue by Month](screenshots/04-target-revenue-by-month.png)

### 5. Quantity Sold by Year

![Quantity Sold by Year](screenshots/05-quantity-sold-by-year.png)

### 6. YTD and QTD Revenue vs. Target

![YTD and QTD vs Target](screenshots/06-ytd-qtd-vs-target.png)

### 7. Map Visual – Revenue and Return Rate by Country

![Map Visual](screenshots/07-map-visual.png)

### 8. Total Orders vs. Total Returns by Category

![Orders vs Returns](screenshots/08-orders-vs-returns.png)

### 9. Total Orders by Model Name and Category

![Orders by Model and Category](screenshots/09-orders-by-model-category.png)

### 10. Weekday vs. Weekend Orders by Category

![Weekday vs Weekend Orders](screenshots/10-weekday-vs-weekend-orders.png)

### 11. Revenue and Profit by Category

![Revenue and Profit by Category](screenshots/11-revenue-and-profit-by-category.png)

### 12. Profit and Bikes Sold by Year and Quarter

![Profit and Bikes Sold by Quarter](screenshots/12-profit-and-bikes-sold-by-quarter.png)

### 13. Bikes Sold by Year and Quarter

![Bikes Sold by Quarter](screenshots/13-bikes-sold-by-quarter.png)

### 14. Bikes Sold and Red Colour Quantity Sold

![Bikes Sold and Red Color](screenshots/14-bikes-sold-and-red-color.png)

### 15. Bikes Sold by Model Name

![Bikes Sold by Model](screenshots/15-bikes-sold-by-model.png)

### 16. Orders by Gender and Quantity Sold by Product Colour

![Gender and Colour](screenshots/16-gender-and-color.png)

---

## 📁 Repository Structure

```
├── BikeSalesAnalysis.pbix
├── screenshots/
│   ├── 01-overview-kpis.png
│   ├── 02-returns-analysis.png
│   ├── 03-time-intelligence.png
│   ├── 04-target-revenue-by-month.png
│   ├── 05-quantity-sold-by-year.png
│   ├── 06-ytd-qtd-vs-target.png
│   ├── 07-map-visual.png
│   ├── 08-orders-vs-returns.png
│   ├── 09-orders-by-model-category.png
│   ├── 10-weekday-vs-weekend-orders.png
│   ├── 11-revenue-and-profit-by-category.png
│   ├── 12-profit-and-bikes-sold-by-quarter.png
│   ├── 13-bikes-sold-by-quarter.png
│   ├── 14-bikes-sold-and-red-color.png
│   ├── 15-bikes-sold-by-model.png
│   └── 16-gender-and-color.png
└── README.md
```

## 🛠 Tools Used

- Power BI Desktop
- DAX
- Data modelling (star schema)









