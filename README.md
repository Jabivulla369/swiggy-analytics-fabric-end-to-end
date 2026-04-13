# Swiggy Sales & Operations Analytics: End-to-End Microsoft Fabric Ecosystem

## 📌 Project Overview
In the fast-paced food technology sector, data is generated at an immense scale. This project focuses on building a **comprehensive Data Analytics Pipeline** for Swiggy, one of India's leading food delivery platforms. By centralizing raw operational data from multiple sources, this solution provides a "Single Source of Truth" for stakeholders to monitor performance, optimize logistics, and understand consumer behavior.

The project transitions from raw data ingestion to a sophisticated **Power BI Executive Dashboard**, leveraging the modern **Microsoft Fabric** stack.

---

## 🛠️ Technology Stack
* **Platform:** Microsoft Fabric (Unified Analytics)
* **Storage:** Fabric Lakehouse (Delta Parquet)
* **Compute & Logic:** SQL (Data Transformation & Validation)
* **Modeling:** Data Warehouse (Star Schema)
* **Visualization:** Power BI (Semantic Modeling & DAX)

---

## 🚀 The End-to-End Workflow

### 1. Data Ingestion (Lakehouse Layer)
The process begins by ingesting high-volume CSV datasets into the **Fabric Lakehouse**.
* **Datasets:** `fact_orders`, `dim_restaurant`, `dim_dish`, `dim_location`, and `dim_date`.
* **Structure:** Organized raw files into a landing zone to maintain data lineage and enable easy reprocessing.

### 2. Data Transformation & Validation (SQL)
Using SQL, I performed rigorous data engineering to ensure the data was "Analytics-Ready."
* **Cleaning:** Handled missing values in ratings and standardized inconsistent naming conventions across cities and states.
* **Referential Integrity:** Validated that every order in the fact table correctly mapped to a valid restaurant and location.
* **Business Logic:** Derived essential columns for temporal analysis (Year, Month, Quarter) within the `dim_date` table.

### 3. Dimensional Modeling (Star Schema)
To ensure high-performance querying and intuitive reporting, I designed a **Star Schema** in the Fabric Data Warehouse:
* **Fact Table:** `fact_orders` (Price, Rating, Rating Count, Keys).
* **Dimension Tables:** `dim_restaurant`, `dim_dish`, `dim_location`, and `dim_date`.
* *This architecture minimizes redundancy and allows for seamless "slicing and dicing" of data across any business dimension.*

### 4. Semantic Modeling & DAX
I built a Power BI Semantic Model on top of the warehouse, creating custom measures to track key performance indicators:
* **Revenue Metrics:** Total Sales, Average Order Value (AOV).
* **Volume Metrics:** Total Order Count, Total Rating Count.
* **Performance Metrics:** Average Rating per Restaurant/City.

---

## 📊 Business Insights & Impact
The final dashboard provides actionable intelligence across several key areas:

<img width="1063" height="652" alt="swiggy_report" src="https://github.com/user-attachments/assets/847dff4b-4c8a-46fb-961b-c9b5dbcbcc51" />

* **Revenue Drivers:** Discovered that **63.7% of revenue (₹33.77M)** is driven by Veg dishes, highlighting a clear area for menu optimization and targeted marketing.
* **Regional Dominance:** Identified **Karnataka** as the highest-grossing state, followed by Uttar Pradesh and Telangana. This allows operations teams to focus delivery partner recruitment in these high-demand zones.
* **Brand Performance:** Established a ranking system for top brands like **KFC, McDonald’s, and Pizza Hut** based on both revenue and customer satisfaction.
* **Operational Trends:** Mapped a 53M+ total sales trend, identifying Thursday and Sunday as peak days for order volume, crucial for demand forecasting.

---

## 📂 Project Structure
* `Data/`: Contains the dimensional and fact CSV files.
* `SQL_Scripts/`: Queries used for data cleaning and schema creation.
* `Reports/`: PDF export of the Power BI dashboard.
* `Documentation/`: Business requirements and architecture details.

---

## 💡 Professional Summary
This project demonstrates the ability to handle a real-world data lifecycle—moving from messy, fragmented raw files to a polished, executive-level reporting system. It showcases proficiency in **Cloud Data Warehousing**, **SQL Engineering**, and **Data Storytelling**
