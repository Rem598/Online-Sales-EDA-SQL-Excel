# 📊 Online Sales Performance Analysis (SQL & Excel)

## 📋 Project Summary

This project involves a comprehensive **Exploratory Data Analysis (EDA)** of a simulated global online sales dataset. The primary goal was to transform raw transactional metrics into clear, actionable business insights regarding **product performance, regional dominance, and sales trends over time.**

**Tools Used:** **SQL** (Querying & Aggregation), **Microsoft Excel** (Visualization & Dashboarding)

---
## 🗃️ Dataset Overview

The dataset covers a year of transactions and includes key metrics like:
* **Transaction ID**
* **Date** (for time-series analysis)
* **Product Category & Name**
* **Units Sold & Unit Price** (used to calculate Total Revenue)
* **Region & Payment Method**

[Dataset Source: Kaggle Dataset](https://www.kaggle.com/datasets/shreyanshverma27/online-sales-dataset-popular-marketplace-data)

---
## 🔧 Key Analysis Methodology

1.  **Data Cleaning:** Handled missing values and standardized date/text formats.
2.  **SQL Aggregation:** Wrote complex queries to aggregate sales data by region, month, and product category.
3.  **Visualization:** Created informative charts and pivot tables in Excel to show trends.
4.  **Insight Generation:** Derived actionable takeaways for marketing and inventory teams.

---
## 🧠 SQL Highlights

These queries formed the foundation for the business insights.


```sql
## Total Sales by Region
SELECT Region, SUM(Total_Revenue) AS Total_Sales
FROM sales_data
GROUP BY Region
ORDER BY Total_Sales DESC;

## Top 10 products

SELECT Product_Name, SUM(Total_Revenue) AS Revenue
FROM sales_data
GROUP BY Product_Name
ORDER BY Revenue DESC
LIMIT 10;

## Sales Trends Over Time (Monthly)

SELECT DATE_FORMAT(Date, '%Y-%m') AS Month, SUM(Total_Revenue) AS Monthly_Sales
FROM sales_data
GROUP BY Month
ORDER BY Month;
```
📊 Key Visualizations
The images below summarize the core findings from the analysis.

Total Sales by Region ![Sales by Region](Total-sales-by-region.jpg)

Revenue by Product Category
Revenue Over Time
Revenue by Payment Method

💡 Actionable Insights
Based on the analysis, here are the key findings:

- Regional Focus: North America is the dominant region for revenue, suggesting marketing budgets should be allocated to capitalize on this lead.

- Product Strategy: Electronics massively outperform all other product categories; further analysis on inventory and pricing for this category is recommended.

- Seasonal Trends: April is the clear peak month for sales, indicating a potential seasonal event or marketing campaign success that should be replicated.

- Payment Gateway: The vast majority of purchases are made via Credit Card, confirming the reliability of existing payment infrastructure.
