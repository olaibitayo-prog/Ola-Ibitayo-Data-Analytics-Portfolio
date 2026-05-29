# Sales Business Analytics Dashboard

## Project Overview

This project analyzes sales performance data to identify revenue trends, customer behavior, and business opportunities.

The goal is to demonstrate how organizations can use analytics to improve sales strategy and operational decision-making.

---

## Business Problem

Sales organizations collect large amounts of data from transactions, customers, and sales activities.

Without effective reporting, leadership may struggle to understand:

- Revenue performance
- Product profitability
- Customer trends
- Sales efficiency

---

## Business Questions

This project answers:

1. Which products generate the highest revenue?
2. Which sales channels perform best?
3. What factors influence profitability?
4. How do sales trends change over time?
5. Where are opportunities for improvement?

---

## Dataset

The dataset contains:

- Transactions
- Products
- Customers
- Sales representatives
- Revenue
- Discounts
- Profit

---

## Key Performance Indicators

Metrics analyzed:

- Total Revenue
- Total Profit
- Profit Margin
- Average Order Value
- Sales Growth
- Product Performance

---

## Data Cleaning

Issues handled:

- Missing values
- Duplicate transactions
- Incorrect formatting
- Data type errors
- Inconsistent categories

---

## SQL Analysis

SQL used for:

- Revenue analysis
- Customer segmentation
- Product ranking
- Trend analysis


Example:

```sql
SELECT
    product_category,
    SUM(revenue) AS total_revenue
FROM sales
GROUP BY product_category
ORDER BY total_revenue DESC;
