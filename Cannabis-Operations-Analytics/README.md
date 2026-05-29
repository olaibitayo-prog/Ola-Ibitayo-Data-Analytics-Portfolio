# Cannabis Operations Analytics Dashboard

## Project Overview

This project analyzes cannabis production and operational data to evaluate business performance, identify inefficiencies, and support data-driven decision making.

The analysis focuses on production output, quality control, inventory management, and revenue performance.

---

## Business Problem

Cannabis producers manage large amounts of operational data across cultivation, production, inventory, and sales.

Without effective analytics, leadership may struggle to identify:

- Production inefficiencies
- Quality issues
- Revenue opportunities
- Inventory challenges

This project demonstrates how analytics can improve operational visibility.

---

## Business Questions

This analysis answers:

1. Which cannabis strains generate the highest revenue?
2. Which strains produce the highest yield?
3. Are quality control defects affecting profitability?
4. Which cultivation rooms perform best?
5. What products should production prioritize?

---

## Dataset

The dataset includes:

- Batch information
- Cannabis strains
- Production rooms
- Yield metrics
- Quality control results
- Inventory data
- Sales performance

---

## Data Cleaning Process

Data quality issues identified:

- Missing values
- Duplicate records
- Incorrect formatting
- Inconsistent categories
- Invalid operational values

Cleaning steps:

- Standardized fields
- Validated production metrics
- Removed duplicates
- Prepared analysis tables

---

## SQL Analysis

SQL techniques used:

- SELECT statements
- Filtering
- GROUP BY
- Aggregations
- Joins
- KPI calculations

Example business analysis:

Which strains generate the highest revenue?

```sql
SELECT
    strain,
    SUM(revenue) AS total_revenue
FROM production
GROUP BY strain
ORDER BY total_revenue DESC;
