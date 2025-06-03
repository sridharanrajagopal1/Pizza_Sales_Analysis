## 🎯 Objectives
- Clean and prepare raw data in Excel
- Generate KPIs using SQL queries
- Create an interactive dashboard in Power BI
- Derive actionable insights from pizza sales

## 🧹 Excel Data Cleaning
Steps performed in `cleaned_pizza_sales.xlsx`:
- Converted `order_date` and `order_time` to standard datetime formats
- Removed duplicates and null rows
- Standardized values in `pizza_category`, `pizza_name`, and `pizza_size`
- Added calculated column: `total_price = quantity * unit_price`

## 📊 Key KPIs (SQL Queries)

> SQL queries are available in `SQL_Queries/pizza_kpis.sql`
Example KPIs:
```sql
-- Total Revenue
SELECT SUM(total_price) AS total_revenue FROM pizza_sales;
-- Average Order Value
SELECT SUM(total_price) / COUNT(DISTINCT order_id) AS avg_order_value FROM pizza_sales;
-- Total Pizzas Sold
SELECT SUM(quantity) AS total_pizzas_sold FROM pizza_sales;
-- Best Selling Pizza
SELECT pizza_name, SUM(quantity) AS total_sold
FROM pizza_sales
GROUP BY pizza_name
ORDER BY total_sold DESC
LIMIT 1;

📈 Power BI Dashboard
The Power BI dashboard includes:
✅ Total Revenue, Orders, and Pizzas Sold
📉 Daily and Monthly Trends
🍕 Best & Worst Selling Pizzas
📊 Sales by Category and Size
🧭 Interactive filters and visuals

🧰 Tools Used
Excel: Data cleaning and preprocessing
PostgreSQL: KPI calculations and queries
Power BI: Visualization and reporting
Git/GitHub: Version control and project hosting

🚀 How to Use
Clone or download this repository.
Open the Excel file and review cleaned data.
Run SQL queries in your PostgreSQL environment.
Open the .pbix file in Power BI Desktop to explore the dashboard.

📬 Contact
Name: Sridharan R
LinkedIn:www.linkedin.com/in/sridharan-rajagopal
📧 sridharanmettur@gmail.com

⭐ If you like this project, consider giving it a star!
Let me know if you'd like this customized with your name, LinkedIn, or to include a real dataset and dashboard files.
