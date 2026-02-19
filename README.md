# Advanced SQL Data Analytics (SSMS)

This project is an **end-to-end advanced data analytics solution** built using SQL Server and SSMS.  
It covers everything from database initialization and data loading to exploratory data analysis (EDA), advanced analytics, and business reporting using dimensional warehouse tables.

---

## 📂 Project Overview

The solution is organized as a collection of SQL scripts that you can run step by step to:

- Create and initialize the `DataWarehouseAnalytics` database.
- Load dimension and fact tables from CSV files into a `gold` schema.
- Perform exploratory data analysis (EDA) on customers, products, and sales.
- Analyze key measures, time-based trends, cumulative performance, and segmentation.
- Generate ready-to-use reports for customers and products.

The project is ideal for learning and demonstrating practical SQL analytics skills in a data warehouse style model.

---

## 🏗️ Database Design

The database follows a simple star-schema style layout under the `gold` schema:

- `gold.dimCustomers` – Customer attributes (ID, name, country, demographics, etc.)
- `gold.dimProducts` – Product attributes (category, subcategory, product line, cost, etc.)
- `gold.factSales` – Transactional sales facts (dates, quantities, prices, revenue, customer/product keys)

This structure supports powerful analytical queries for BI and reporting scenarios.

---

## 📑 Script Structure

All SQL files are numbered to reflect the logical execution order.

1. **`00_init_database.sql`**  
   - Creates (or recreates) the `DataWarehouseAnalytics` database.  
   - Creates the `gold` schema and core tables (`dimCustomers`, `dimProducts`, `factSales`).  
   - Loads data from CSV files into the tables using `BULK INSERT`.

2. **Exploratory Data Analysis (EDA)**  
   - `01_database_exploration.sql` – Inspect database objects, row counts, and basic sanity checks.  
   - `02_dimensions_exploration.sql` – Explore customer and product dimensions (countries, categories, demographics).  
   - `03_date_range_exploration.sql` – Explore date coverage, min/max dates, and gaps in sales data.  
   - `04_measures_exploration.sql` – Compute key business metrics (total sales, quantity, orders, customers, products).

3. **Advanced Analytics**  
   - `05_magnitude_analysis.sql` – Magnitude and distribution analysis by country, gender, category, customer, etc.  
   - `06_ranking_analysis.sql` – Ranking queries (Top/Bottom N customers, products, countries by revenue or quantity).  
   - `07_change_over_time_analysis.sql` – Time-series trends using year/month/date aggregations.  
   - `08_cumulative_analysis.sql` – Running totals and moving averages using window functions.  
   - `09_performance_analysis.sql` – Performance vs. targets or previous periods (growth, decline, trend indicators).  
   - `10_data_segmentation.sql` – Segmentation of customers/products into groups or tiers based on behavior/metrics.  
   - `11_part_to_whole_analysis.sql` – Part-to-whole insights (e.g., contribution of top segments to total sales).

4. **Reporting**  
   - `12_report_customers.sql` – Customer-focused report combining key KPIs, revenue, and behavior.  
   - `13_report_products.sql` – Product-focused report summarizing performance by product, category, and subcategory.

---

## 🚀 Getting Started

### Prerequisites

- Microsoft SQL Server (Developer/Express/Standard/Enterprise)
- SQL Server Management Studio (SSMS)
- Access to the CSV data files referenced in `00_init_database.sql`  
  (update the file paths in the script to match your local environment)

### Setup Steps

1. Open SSMS and connect to your SQL Server instance.
2. Open `00_init_database.sql`.
3. Update the `BULK INSERT` file paths to point to your CSV folder.
4. Run the script to create and load the `DataWarehouseAnalytics` database.
5. Execute the remaining scripts in numeric order to explore and analyze the data:
   - `01_...sql` → `02_...sql` → … → `13_...sql`.

---

## 🔍 Key Analytics Covered

- **Database Exploration** – Structure, row counts, and sanity checks.  
- **Dimensions Exploration** – Countries, segments, categories, and demographics.  
- **Date & Time Analysis** – Ranges, seasonality, trends over months/years.  
- **Measures & KPIs** – Total sales, quantity, orders, customers, products.  
- **Magnitude & Distribution** – How metrics spread across segments and regions.  
- **Ranking** – Top/Bottom N customers, products, and countries.  
- **Change Over Time** – Growth or decline across periods.  
- **Cumulative Metrics** – Running totals and moving averages using window functions.  
- **Performance Analysis** – Relative performance comparisons.  
- **Segmentation & Part-to-Whole** – Grouping entities and understanding contributions.  
- **Reporting** – Customer and product views ready for BI dashboards.

---

## 🎯 Learning Outcomes

By going through this project you will:

- Practice writing **clean, production-style SQL** in SSMS.
- Understand how to structure **EDA and advanced analytics** using only SQL.
- Learn to use **aggregations, joins, window functions, ranking, and date functions** effectively.
- See how to turn raw transactional data into **insightful reports and business views**.

---

## 📌 Future Enhancements

Possible extensions for this project:

- Add stored procedures or views for frequently used reports.
- Integrate with a visualization tool (Power BI, Tableau) on top of `DataWarehouseAnalytics`.
- Implement role-based security or row-level security for sensitive data.
- Automate data refresh and scheduling with SQL Agent jobs.

---

## 📄 License

This project is released under the MIT License.  
Feel free to use, modify, and extend it for learning or analytics use cases.

---
