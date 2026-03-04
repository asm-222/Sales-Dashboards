# 📊 Sales & Order Analysis

An end-to-end **Excel Data Analysis Project** that transforms raw sales data into actionable business insights using Power Query, Data Modeling, and Power Pivot.

---

## 📊 Dashboard Preview

### 📌 Dashboard Screenshot
![Dashboard](https://github.com/asm-222/Sales-Dashboards/blob/main/pic/Dashboard1.PNG)

### 🎥 Dashboard Demo
<h2 align="center">Dashboard Demo</h2>

<p align="center">
  <img src="https://raw.githubusercontent.com/asm-222/Sales-Dashboards/main/pic/Dash.gif" width="90%">
</p>

---

## 🚀 Project Overview

The **Sales & Order Analysis** project demonstrates a complete data analytics workflow inside Microsoft Excel:

- 🧹 Data Cleaning & Transformation using **Power Query**
- 🏗 Data Modeling & Normalization
- 📊 Data Analysis with **Power Pivot**
- 📈 Interactive Dashboard with Pivot Tables, Charts & Slicers

The goal of this project is to analyze sales performance, customer behavior, and regional trends to support data-driven business decisions.

---

## 🔗 Data Source

The dataset was sourced from a public Google Sheets file:

📎 Sales Dataset:  
https://docs.google.com/spreadsheets/d/1_YDa6Lbh9d_-C3LKvSDyqld_sKqWTHEi/edit?gid=371685605#gid=371685605

---

## 🛠 Tools & Technologies

- Microsoft Excel
  - Power Query (Data Cleaning & Transformation)
  - Data Model (Relationships & Normalization)
  - Power Pivot
  - DAX Measures
  - Pivot Tables & Pivot Charts
  - Slicers & Timeline

---

## 🧹 Data Preparation Process

### 1️⃣ Data Cleaning (Power Query)
- Removed duplicates
- Handled missing values
- Standardized date & currency formats
- Created calculated columns
- Fixed inconsistent text formatting

### 2️⃣ Data Modeling
- Normalized data into:
  - Fact Table: Sales Transactions
  - Dimension Tables: Customers, Products, Dates, Regions
- Built relationships inside Data Model
- Imported structured model into Power Pivot

### 3️⃣ Analysis & Dashboard Creation
- Created KPI Measures using DAX
- Built Pivot Tables for insights
- Designed interactive dashboard with:
  - KPI Cards
  - Sales Trend Chart
  - Top Products Chart
  - Regional Analysis
  - Customer Segmentation
  - Dynamic Filters (Slicers & Timeline)

---



## 📈 Key Insights (Sample Insights)

- 💰 Total Revenue: $2.5M+
- 📦 Total Orders: 15K+
- 📊 Average Order Value: $160+
- 🏆 Top Category: Electronics (45% of revenue)
- 🌎 Best Performing Region: West Region
- 🔁 Repeat customers generate majority of revenue
- 📅 Q4 shows highest sales peak

*(Values are placeholders and may vary depending on refresh.)*

---

## 📊 Example DAX Measures

```DAX
Total Sales = SUM(Sales[TotalAmount])

Total Orders = DISTINCTCOUNT(Sales[OrderID])

Average Order Value = 
DIVIDE([Total Sales], [Total Orders])

YoY Growth = 
VAR CurrentYear = [Total Sales]
VAR PreviousYear = 
    CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))
RETURN
DIVIDE(CurrentYear - PreviousYear, PreviousYear)
