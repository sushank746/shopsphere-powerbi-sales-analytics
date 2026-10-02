# ShopSphere — E-Commerce Sales & Customer Analytics

## 1. Project Overview

ShopSphere is an interactive Power BI analytics project designed to analyze e-commerce sales performance, profitability, customer contribution, product performance, regional performance, and time-based trends.

The project transforms raw transactional data into a structured analytical data model and presents the results through an interactive four-page Power BI dashboard.

---

## 2. Business Problem

E-commerce businesses generate large volumes of transactional data, but raw data alone does not provide an easy way to understand business performance.

This project addresses questions such as:

- How much revenue is being generated?
- How profitable is the business?
- Which products and categories generate the most sales?
- Which customers contribute the most revenue and profit?
- Which regions and states perform best?
- How do sales and profit change over time?
- What are the key business KPIs?

---

## 3. Project Objectives

The main objectives were:

1. Clean and transform raw transactional data.
2. Build a structured dimensional data model.
3. Create reusable DAX measures.
4. Analyze sales, profit, customers, products and geography.
5. Identify trends and high-performing segments.
6. Build an interactive executive-level dashboard.
7. Present business insights in a clear and understandable format.

---

## 4. Tools & Technologies

- Microsoft Power BI
- Power Query
- DAX
- Data Modeling
- Data Visualization
- Microsoft Excel

---

## 5. Data Model

The project uses a dimensional modeling approach consisting of one fact table and multiple dimension tables.

### Fact Table

**FactSales**

Contains transactional-level information including:

- Order ID
- Order Date
- Product ID
- Customer ID
- Location Key
- Sales Amount
- Profit
- Quantity
- Discount
- Cost
- Unit Price

### Dimension Tables

#### DimCustomer

Contains customer-level information:

- Customer ID
- Customer Name
- Gender
- Age
- City
- State
- Region

#### DimProduct

Contains product information:

- Product ID
- Product Name
- Brand
- Category
- Sub-Category
- Cost

#### DimLocation

Contains geographic information:

- Location Key
- City
- State
- Region

#### DimDate

A dedicated date dimension used for time-based analysis.

It contains:

- Date
- Year
- Month
- Month Number
- Quarter
- Year Month
- Day
- Day Name

---

## 6. Data Model Relationships

The model follows a one-to-many dimensional structure:

DimCustomer → FactSales

DimProduct → FactSales

DimLocation → FactSales

DimDate → FactSales

All relationships are active and use single-direction filtering from dimensions to the fact table.

---

## 7. DAX Measures

### Total Sales

```DAX
Total Sales =
SUM(FactSales[SalesAmount])
