# Task 7: Sales Data Analysis with SQLite and Python

## 📌 Objective
The goal of this task is to perform basic data analysis using Python and a SQLite database. We created a database, inserted sample sales data, ran SQL queries to analyze total quantity and revenue per product, and visualized the results using matplotlib.

---

## 🛠️ Tools Used
- Python
- SQLite (via `sqlite3`)
- pandas
- matplotlib

---

## 🧮 Data Structure

The SQLite table `sales` contains the following columns:
- `product` (TEXT): Name of the product
- `quantity` (INTEGER): Number of items sold
- `price` (INTEGER): Price per unit

Sample Data:

| product   | quantity | price  |
|-----------|----------|--------|
| Laptop    | 2        | 60000  |
| Phone     | 5        | 20000  |
| Headphone | 10       | 1500   |
| Tablet    | 3        | 25000  |
| Mouse     | 7        | 700    |

---

## 🧾 SQL Query Used

```sql
SELECT 
  product,
  SUM(quantity) AS total_quantity,
  SUM(quantity * price) AS total_revenue
FROM sales
GROUP BY product;
