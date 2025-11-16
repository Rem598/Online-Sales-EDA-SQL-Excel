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

### Total Sales by Region
```sql
SELECT Region, SUM(Total_Revenue) AS Total_Sales
FROM sales_data
GROUP BY Region
ORDER BY Total_Sales DESC;
