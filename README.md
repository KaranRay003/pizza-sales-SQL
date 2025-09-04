# 📊 Pizza Sales SQL Analysis

## 📌 Project Overview  
This project focuses on analyzing **pizza sales data** using SQL. The dataset contains details about pizza orders, including sales, customers, and product information. The goal is to write and execute SQL queries to answer specific business questions and generate insights into sales performance.  

After extracting `pizza_sales.zip`, you will find the dataset required for SQL queries.  

## 🗄️ Dataset Information  
The dataset includes transactional sales records such as:  
- **Order ID** – Unique identifier for each order  
- **Pizza type & size** – Different product variations  
- **Quantity** – Number of pizzas ordered  
- **Price** – Unit price of pizzas  
- **Order date & time** – Timestamp of each order  

*(The exact schema may vary depending on the extracted files.)*

## 🎯 Objectives  
The project answers business questions such as:  
- Total revenue generated  
- Best-selling pizzas (by quantity & revenue)  
- Average order value  
- Sales trends by day, week, or month  
- Customer buying patterns  

These queries are listed in **`Questions.txt`**.  

## 🛠️ Tools & Technologies  
- **SQL** – For writing and executing queries  
- **SQLite / MySQL / PostgreSQL** – Compatible database engines  
- **Any SQL Client** (DBeaver, MySQL Workbench, SQLite Studio, etc.)  

## 🚀 How to Use  
1. Extract the dataset:  
   ```bash
   unzip pizza_sales.zip
Import the dataset into your SQL database (e.g., MySQL, PostgreSQL, or SQLite).

Open Questions.txt – it contains all the query prompts.

Write SQL queries to answer each question.

Analyze the results and interpret insights.

📈 Expected Outcomes
By completing this project, you will:

Gain hands-on SQL query writing experience

Learn how to clean and query real-world sales data

Extract meaningful insights for business decision-making

📝 Example Queries
sql
Copy code
-- 1. Total Revenue
SELECT SUM(quantity * price) AS total_revenue
FROM pizza_sales;

-- 2. Best Selling Pizza (by quantity)
SELECT pizza_name, SUM(quantity) AS total_sold
FROM pizza_sales
GROUP BY pizza_name
ORDER BY total_sold DESC
LIMIT 1;

-- 3. Monthly Sales Trend
SELECT strftime('%Y-%m', order_date) AS month, SUM(quantity * price) AS revenue
FROM pizza_sales
GROUP BY month
ORDER BY month;# pizza-sales-SQL
