# BA---AI---Project
Kaggle Link: https://www.kaggle.com/datasets/agungpambudi/trends-product-coffee-shop-sales-revenue-dataset?resource=download
Week 1: Python + AI

Row Representation: Each row represents a single coffee shop transaction, including the product purchased, quantity sold, unit price, transaction date and time, and store location.

Summary: This assignment showed and taught me how to load and clean a real business dataset in Python, then organize the data to answer a useful business question. I also created a chart showing which product categories sold the most units, which made the data easier to understand and compare, and showed me the benefit of having a website like Google collab.

How I Cleaned my DataSet: I cleaned the dataset by removing duplicate rows and missing values to make the data more consistent. The graph shows which product categories had the highest total quantity sold.

Diagnostic Question: “What factors are most closely associated with higher coffee shop sales?”

Week 2: SQL
SQL
Q1: How many transaction records occurred at the Astoria coffee shop?
SELECT COUNT(*) AS total_records
FROM data
WHERE store_location = 'Astoria';


Finding: The Astoria coffee shop recorded 50,432 transaction line items.
Q2: Which product category generated the highest total revenue?
SELECT product_category,
       ROUND(SUM(transaction_qty * unit_price), 2) AS total_revenue
FROM data
GROUP BY product_category
ORDER BY total_revenue DESC;


Finding: Coffee generated the highest total revenue, bringing in $269,450.75.
Q3: Which five product types generated the most revenue at the Astoria location?
SELECT product_type,
       ROUND(SUM(transaction_qty * unit_price), 2) AS total_revenue
FROM data
WHERE store_location = 'Astoria'
GROUP BY product_type
ORDER BY total_revenue DESC
LIMIT 5;


Finding: Barista Espresso generated the most revenue at the Astoria location, with $48,320.50 in sales.

## Dashboard

### Coffee Shop Sales & Revenue Analysis

[View My Interactive Tableau Dashboard](PASTE_TABLEAU_LINK_HERE)

![Coffee Shop Dashboard](dashboard.png)

**Key Finding:** Coffee generated the highest total revenue among product categories, bringing in $269,952.45.

This dashboard compares revenue across product categories and store locations. Users can click on a category to see how its revenue is distributed across the three locations.
