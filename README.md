# Task 7: Basic Sales Summary with SQLite and Python

This project demonstrates how to:
- Connect Python to an SQLite database
- Run basic SQL queries to summarize sales (total quantity, revenue)
- Load results into pandas DataFrame
- Print results and visualize using matplotlib

## Files
- sales_data.db → SQLite database with sample sales table
- task7_sales_summary.py → Python script that connects to DB, runs queries, and plots results
- sales_chart.png → Bar chart of revenue by product

## SQL Query Used
```sql
SELECT product, 
       SUM(quantity) AS total_qty, 
       SUM(quantity * price) AS revenue
FROM sales 
GROUP BY product;

