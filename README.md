# 📊 ShopSphere — E-Commerce Sales & Customer Analytics

An interactive Power BI analytics project built to analyze e-commerce sales performance, profitability, customer contribution, product performance, regional performance, and time-based trends.

---

## 📌 Project Overview

ShopSphere Sales & Customer Analytics transforms raw e-commerce transaction data into an interactive four-page Power BI dashboard.

The project focuses on answering key business questions such as:

- How are overall sales and profit performing?
- Which products and categories generate the most sales?
- Which customers contribute the most sales and profit?
- Which regions and states perform better?
- How do sales and profit change over time?
- What is the overall profitability of the business?

---

## 🛠️ Tools & Technologies

- Power BI Desktop
- Power Query
- DAX
- Microsoft Excel
- Data Modeling
- Star Schema / Dimensional Modeling
- Interactive Data Visualization

---

## 🗂️ Data Model

The project uses a fact-and-dimension architecture.

### Fact Table

**FactSales**

Contains transactional information including:

- Order ID
- Order Date
- Customer ID
- Product ID
- Location Key
- Sales Amount
- Profit
- Quantity
- Cost
- Discount Percentage
- Unit Price

### Dimension Tables

**DimCustomer**
- Customer ID
- Customer Name
- Gender
- Age
- City
- State
- Region

**DimProduct**
- Product ID
- Product Name
- Brand
- Category
- Sub-Category
- Cost

**DimLocation**
- Location Key
- City
- State
- Region

**DimDate**
- Date
- Year
- Month
- Quarter
- Year Month
- Day
- Day Name

---

## 🔗 Data Model

```text
DimCustomer ──────┐
                  │
DimProduct ───────┤
                  │
DimLocation ──────┤─── FactSales
                  │
DimDate ──────────┘
