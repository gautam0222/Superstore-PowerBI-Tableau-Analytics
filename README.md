# 📊 Superstore Sales Analytics Dashboard

### Power BI + Tableau Data Visualization Project

An **end-to-end Business Intelligence and Data Visualization project**
built using **Power BI and Tableau** to analyze retail sales
performance, profitability, and customer behavior using the **Superstore
dataset**.

This project demonstrates a complete **data analytics workflow used in
real-world BI environments**, including:

-   Data Cleaning & Transformation
-   Data Modeling
-   DAX Measures
-   Interactive Dashboards
-   Business Insights & Storytelling

------------------------------------------------------------------------

# 🚀 Project Overview

Retail companies generate large amounts of transactional data, but raw
data alone does not support strategic decision-making.

This project converts **9,994 retail order records** into a fully
interactive analytics system using modern BI tools.

The solution consists of two primary dashboards:

1️⃣ **Exploratory Data Visualization using Tableau**\
2️⃣ **Interactive Business Intelligence Dashboard using Power BI**

These dashboards allow users to explore:

-   Regional sales performance
-   Product category profitability
-   Seasonal sales trends
-   Customer segment behavior
-   Product-level revenue contribution

------------------------------------------------------------------------

# 📂 Dataset

Dataset Used: **Superstore Sales Dataset**

Source: Kaggle\
https://www.kaggle.com/datasets/vivek468/superstore-dataset-final

Dataset Characteristics:

  Attribute     Details
  ------------- ---------------------
  Rows          9,994 records
  Columns       15 attributes
  Time Period   2014 -- 2017
  Industry      Retail / E-commerce

Key dataset fields:

-   Order Date
-   Ship Date
-   Region
-   State
-   Category
-   Sub-Category
-   Product Name
-   Sales
-   Quantity
-   Discount
-   Profit
-   Customer Segment

------------------------------------------------------------------------

# 🛠 Tools & Technologies

### Business Intelligence

-   Power BI Desktop
-   Tableau Public

### Data Processing

-   Power Query
-   DAX (Data Analysis Expressions)

### Visualization Techniques

-   KPI Cards
-   Interactive Filters
-   Drill-down Hierarchies
-   Geographic Maps
-   Time Series Analysis
-   Conditional Formatting

------------------------------------------------------------------------

# ⚙️ Data Preparation

Data cleaning and preparation were performed using **Power BI Power
Query Editor**.

### Cleaning Steps

-   Removed blank rows
-   Removed duplicate records
-   Removed error values
-   Verified column data types
-   Standardized field formats

### Feature Engineering

Two calculated columns were created.

**Profit Status**

    if [Profit] > 0 then "Profitable" else "Loss"

Used to classify transactions based on profitability.

**Shipping Duration**

    Ship Days = Ship_Date - Order_Date

Used to evaluate logistics performance.

------------------------------------------------------------------------

# 📐 Data Modeling

A **Date Dimension Table** was created using DAX.

    Date = CALENDARAUTO()

Relationship:

    Date[Date] → Superstore[Order_Date]

This enables **time intelligence calculations such as YoY analysis**.

------------------------------------------------------------------------

# 📊 DAX Measures

### Total Sales

    Total Sales = SUM('Superstore'[Sales])

### Total Profit

    Total Profit = SUM('Superstore'[Profit])

### Total Quantity

    Total Quantity = SUM('Superstore'[Quantity])

### Profit Margin

    Profit Margin % =
    DIVIDE([Total Profit],[Total Sales],0) * 100

### Average Discount

    Avg Discount = AVERAGE('Superstore'[Discount])

### Year-over-Year Sales Growth

    YoY Growth =
    DIVIDE(
        [Total Sales] -
        CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date])),
        CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date])),
    0)

------------------------------------------------------------------------

# 📊 Tableau Dashboard

The Tableau dashboard focuses on **exploratory analysis**.

Visualizations include:

-   Sales by Category
-   Monthly Sales Trend with Forecast
-   Profit by Sub-Category

### Dynamic Parameter

A parameter allows switching between:

-   Sales
-   Profit
-   Quantity

This improves dashboard interactivity.

------------------------------------------------------------------------

# 📈 Power BI Dashboard

The Power BI dashboard is designed as a **fully interactive executive
analytics dashboard**.

### Key Features

-   KPI Performance Cards
-   Interactive Filters (Slicers)
-   Drill-down Hierarchies
-   Geographic Sales Map
-   Product Ranking Table
-   Sales Trend Analysis

### Dashboard Visuals

  Visualization    Purpose
  ---------------- -----------------------------
  KPI Cards        Overall performance metrics
  Bar Chart        Sales by category
  Horizontal Bar   Profit by sub-category
  Map              Regional sales distribution
  Table            Top products by sales
  Line Chart       Monthly sales trends

------------------------------------------------------------------------

# 📊 Key Insights

-   West region contributes the highest share of revenue
-   Technology category generates the highest profit
-   Furniture category shows the lowest margins
-   Consumer segment drives the majority of orders
-   Holiday season (Nov--Dec) produces peak sales

------------------------------------------------------------------------

# 💡 Business Recommendations

1.  Reduce excessive discounting in low-margin product categories.
2.  Expand technology product offerings in underperforming regions.
3.  Increase inventory before holiday sales periods.
4.  Improve targeted marketing for corporate customers.

------------------------------------------------------------------------

# 📁 Repository Structure

    superstore-sales-analytics
    │
    ├── dataset
    │   └── superstore_dataset.xlsx
    │
    ├── powerbi-dashboard
    │   └── dashboard.pbix
    │
    ├── tableau-dashboard
    │   └── tableau_link.txt
    │
    ├── documentation
    │   └── project_guide.docx
    │
    ├── report
    │   └── insight_report.pdf
    │
    └── README.md

------------------------------------------------------------------------

# 🎯 Learning Outcomes

This project demonstrates:

-   Business Intelligence skills
-   Data cleaning and transformation
-   Data modeling
-   DAX calculations
-   Dashboard design
-   Data storytelling

------------------------------------------------------------------------

# 👨‍💻 Author

**Gautam Sukhani**

AI Intern \| Data Analytics Enthusiast \| Developer

Skills: - Power BI - Tableau - Python - AI Agents - Data Analytics
