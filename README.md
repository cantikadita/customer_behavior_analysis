# customer_behavior_analysis
data analytics project showcasing customer behavior analysis using python, sql, and power BI
# Customer Shopping Behavior Analysis

## 📋 Overview

This project provides an end-to-end data analytics solution to analyze customer purchasing patterns and demographics. By integrating **Python** for data engineering, **SQL** for deep-dive querying, and **Power BI** for visualization, this project identifies high-value customer segments and optimizes marketing strategies based on shopping habits.

## 📊 Dataset

* **Source:** Customer Shopping Behavior Dataset (Kaggle).
* **Size:** 3,900 rows and 18 initial columns.
* **Key Features:** Customer ID, Age, Gender, Item Purchased, Category, Purchase Amount (USD), Location, Size, Color, Season, Review Rating, Subscription Status, and Shipping Type.

## 🛠 Tools & Technologies

* **Python:** Data cleaning and Exploratory Data Analysis (EDA).
* *Libraries:* `pandas`, `sqlalchemy`, `psycopg2`, `pymysql`.


* **SQL (PostgreSQL / MySQL / SQL Server):** Advanced business logic and customer segmentation.
* **Power BI:** Interactive dashboarding and DAX (Data Analysis Expressions).
* **Gamma AI:** Professional presentation deck generation.

## 🚀 Project Steps

### 1. Data Cleaning & EDA (Python)

Performed automated data profiling and cleaning to ensure high data quality:

* **Handling Missing Values:** Imputed missing "Review Ratings" using the median rating of the specific product category.
* **Feature Engineering:** * Created `age_group` (Young Adult, Adult, Middle-aged, Senior).
* Mapped purchase frequencies to numeric `purchase_frequency_days`.


* **Optimization:** Removed redundant columns like `promo_code_used` after verifying it was identical to `discount_applied`.
* **Standardization:** Converted all column headers to snake_case for database compatibility.

### 2. Database Integration (SQL)

Loaded the refined data into a relational database and executed complex queries to extract business insights:

* **Customer Segmentation:** Used CTEs to categorize users as 'New', 'Returning', or 'Loyal' based on purchase history.
* **KPI Extraction:** Calculated revenue by gender, subscription status, and age group.
* **Advanced Logic:** Ranked top 3 products within each category using `ROW_NUMBER()` window functions.

### 3. Data Visualization (Power BI)

Developed an interactive dashboard to visualize the SQL-derived insights:

* **Sales Performance:** Tracking total revenue and average spend across categories.
* **Demographic Breakdown:** Analyzing the influence of age and gender on shopping frequency.
* **Logistics Analysis:** Comparing shipping types (Standard vs. Express) against purchase amounts.

### 4. Professional Reporting

* **Presentation:** Generated a stakeholder-ready slide deck using **Gamma AI** to summarize key findings and strategic recommendations.

## 📈 Dashboard Preview

## 💡 Results & Insights

* **Demographic Leaders:** Male customers contributed significantly more to total revenue compared to female customers.
* **Loyalty & Revenue:** Customers categorized as "Loyal" (over 10 previous purchases) represent a critical segment for retention marketing.
* **Shipping Influence:** Standard and Express shipping types show comparable average purchase amounts, suggesting shipping speed isn't a primary barrier for high-value orders.
* **Age Contribution:** Revenue is highest among the "Middle-Aged" and "Young Adult" segments.

## ⚙️ How to Run

1. **Environment Setup:**
```bash
pip install pandas sqlalchemy psycopg2-binary pymysql pyodbc

```


2. **Run Cleaning Script:** Execute `Customer_Shopping_Behavior_Analysis.ipynb` to clean the data and export it to your database.
3. **Database Configuration:** Update the connection string in the Python script with your local `username` and `password`.
4. **SQL Queries:** Run `customer_behavior.sql` in your preferred SQL editor to view advanced metrics.
5. **Dashboard:** Open the `.pbix` file in Power BI Desktop to interact with the visualizations.

