
# 📉 Sales Analysis
---

## 📌 Project Overview

This SQL project analyses a global dataset of tech layoffs, focusing on patterns across company size, funding, geography, and time. Using MySQL, the project involved full data cleaning and exploration to surface key trends in layoffs across the industry.

---

## 🎯 Business Objective

### **Business Request & User Stories**

The business request for this data analyst project was an executive sales report for sales managers. Based on the request that was made from the business, the following user stories were defined to fulfill delivery and ensure that acceptance criteria were maintained throughout the project.

| # | As a (role) | I want (request / demand) | So that I (user value) | Acceptance Criteria |  |
| --- | --- | --- | --- | --- | --- |
| 1 | Sales Manager | To get a dashboard overview of internet sales | Can follow better which customers and products sells the best | A Power BI dashboard which updates data once a day |  |
| 2 | Sales Representative | A detailed overview of Internet Sales per Customers | Can follow up my customers that buys the most and who we can sell more to | A Power BI dashboard which allows me to filter data for each customer |  |
| 3 | Sales Representative | A detailed overview of Internet Sales per Products | Can follow up my Products that sells the most | A Power BI dashboard which allows me to filter data for each Product |  |
| 4 | Sales Manager | A dashboard overview of internet sales | Follow sales over time against budget | A Power BI dashboard with graphs and KPIs comparing against budget |  |

# Data Cleansing & Transformation (SQL)

---

## 🧹 Data Cleaning Process

Performed in `world_layoffs_data_cleaning.sql`, including:
- ✅ Deduplication using `ROW_NUMBER() OVER (...)` with full record partitioning
- ✅ Standardization: trimmed whitespace, unified country names, normalized industry labels
- ✅ Date conversion and datatype updates
- ✅ Null handling: used self-joins to backfill industry data based on company/location
- ✅ Removed blank or empty rows (e.g. rows with no layoff data)

Staging tables were used throughout to preserve original data and enable rollback if needed.

---

## 🔍 Exploratory Analysis Highlights

Key queries in `world_layoffs_exploratory_data_analysis.sql` included:

- **Total layoffs by company, year, and country**
- **Top 5 companies by layoffs each year**
- **Rolling monthly and yearly layoff trends using window functions**
- **Stage-based and industry-based analysis of impact severity**
- **Identifying locations most affected by layoffs per year**

These results would support interactive dashboards or trend reports for decision-makers.

---

## 🛠 Tools & Skills Demonstrated

- **SQL (MySQL)**: joins, CTEs, window functions, `ROW_NUMBER()`, `DENSE_RANK()`, date conversion
- **Data Cleaning**: deduplication, field standardization, NULL handling, type casting
- **Exploratory Analysis**: grouping, aggregation, time-based trends, ranking
- **Data Storytelling**: converting raw data into questions executives care about

---

## 📂 Files Included

| File | Description |
|------|-------------|
| `world_layoffs_data_cleaning.sql` | Cleans raw layoff data, removes duplicates, fixes formatting, prepares staging table |
| `world_layoffs_exploratory_data_analysis.sql` | Analyses layoff patterns by company, country, year, and other segments |

---

## 💡 Query to Identify Most Impacted Locations Each Year

# Sales Management Dashboard

The finished sales management dashboard with one page with works as a dashboard and overview, with two other pages focused on combining tables for necessary details and visualizations to show sales over time, per customers and per products.

![](https://analyzewithaliportfolio.wordpress.com/wp-content/uploads/2021/02/dashboard-2.png?w=825)


https://app.powerbi.com/reportEmbed?reportId=5d1cd891-a9f9-428e-bbb4-3b27b36b7070&autoAuth=true&ctid=957886e1-6d0b-44df-8768-a3ab1550488b
