# Amazon Sales Analysis Dashboard

## Overview
This project analyzes Amazon sales data to provide insights into order trends, product distribution, courier status, and regional sales performance. The analysis is performed using **Python**, **Pandas**, **Matplotlib**, and **Seaborn**.

The dataset initially contained 128,976 records and 21 columns, including order details, product category, size, courier status, quantity, amount, and shipping information.

---

## Dataset Information

- **Rows:** 128,976  
- **Columns:** 21 (after cleaning, 19)  
- **Key Columns:**
  - `Order ID`: Unique identifier for each order
  - `Date`: Order date
  - `Status`: Order status (Shipped, Cancelled, etc.)
  - `Category`: Product category (T-shirt, Shirt, Blazzer, etc.)
  - `Size`: Product size (S, M, L, XL, etc.)
  - `Quantity`: Number of units purchased
  - `Amount`: Order amount in INR
  - `ship-city`, `ship-state`, `ship-country`: Shipping location
  - `B2B`: Indicates if the buyer is a business

**Data Cleaning & Preprocessing:**
- Removed empty columns (`New`, `PendingS`)  
- Dropped rows with null values  
- Converted `Date` to datetime type  
- Converted `ship-postal-code` to integer  
- Renamed `Qty` column to `Quantity`  
- Final dataset after cleaning: 37,514 rows × 19 columns  

---

## Exploratory Data Analysis (EDA)

### Product Size Distribution
- Count plot of product sizes using a **Viridis palette**
- **Insight:** M-size is the most frequently purchased, followed by L and XL.
- Annotated bar labels are included in the notebook.

### Total Quantity by Size
- Bar chart of total quantity sold per size
- **Insight:** Most sold size is **M**, followed by **L** and **XL**.

### Courier Status Distribution
- Count plot showing courier status for each order, split by order status
- **Insight:** Most orders are successfully shipped; a few are still in transit or cancelled.

### Category Distribution
- Histogram of product categories
- **Insight:** T-shirts have the highest purchase volume.

### B2B vs Retail Buyers
- Pie chart showing proportion of B2B vs Retail buyers
- **Insight:** 99.2% of buyers are retailers, 0.8% are B2B buyers.

### Product Availability by Size
- Scatter plot of Category vs Size
- **Insight:** Shows distribution of available sizes per product category.

### Regional Distribution of Orders
- Count plot of states showing order volumes
- **Insight:** Maharashtra has the largest number of orders.
- Top 10 states plotted with horizontal bar chart using Viridis palette

---

## Dataset Summary Statistics

### Numerical Columns
| Column   | Count | Mean   | Min  | Max  |
|----------|-------|--------|------|------|
| Quantity | 37,514 | 0.87  | 0    | 5    |
| Amount   | 37,514 | 646.55 | 0    | 5495 |

### Categorical Columns
- **Most frequent order status:** Shipped - Delivered to Buyer  
- **Most frequent product category:** T-shirt  
- **Most frequent size:** M  
- **Most common city/state:** Bengaluru / Maharashtra  

---

## Conclusion
- Amazon primarily serves **retail buyers** with very few B2B orders.  
- **Maharashtra** leads in order volume among states.  
- **T-shirts** are the highest selling category, and **M-size** is the most preferred.  
- Most orders are fulfilled via **Amazon** and delivered successfully.  

This analysis provides actionable insights for inventory planning, regional marketing, and supply chain optimization.

---

## Technologies Used
- Python 3.x  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  

---

### Notes
- All plots and visualizations can be found and executed in the Jupyter Notebook file (`.ipynb`).  
- Viridis color palette is used throughout for consistency in categorical plots.
