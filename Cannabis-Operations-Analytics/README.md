Cannabis Operations Analytics Dashboard
## Project Overview

This project analyzes cannabis cultivation, production, quality control, and sales data to identify operational improvement opportunities and support data-driven decision-making.

Using Excel, SQL, and Power BI, the analysis evaluates strain performance, cultivation room performance, quality outcomes, revenue generation, and product prioritization.

---

## Business Problem

Cannabis producers manage operational data across cultivation rooms, production activities, inventory, quality control, and sales.

Without effective analytics, leadership may struggle to identify:

- High-performing products
- Quality control issues
- Cultivation room performance gaps
- Revenue opportunities
- Products that should be prioritized for production

This project demonstrates how analytics can improve operational visibility and support better business decisions.

---

## Business Questions

1. Which cannabis strains generate the highest revenue?
2. Which strains produce the highest yield?
3. Are quality control defects affecting profitability?
4. Which cultivation rooms perform best?
5. What products should production prioritize?

---

## Dataset

The dataset includes:

- Cannabis strains
- Cultivation rooms
- Yield grams
- Quality control defect flags
- Inventory units
- Units sold
- Revenue
- Sale price
- Environmental metrics including temperature, humidity, and CO2 levels

---

## Data Cleaning Process

Data quality issues reviewed:

- Missing values
- Duplicate records
- Incorrect formatting
- Inconsistent categories
- Invalid operational values

Cleaning steps completed:

- Standardized field names
- Validated numeric fields
- Reviewed duplicate records
- Prepared fields for SQL analysis
- Built clean measures for Power BI reporting

---

## SQL Analysis

SQL was used to validate the dataset and answer key business questions before dashboard development.

### 1. Which cannabis strains generate the highest revenue?

```sql
SELECT
    strain,
    SUM(revenue) AS total_revenue
FROM weedop
GROUP BY strain
ORDER BY total_revenue DESC;
2. Which strains produce the highest yield?
SELECT
    strain,
    AVG(yield_grams) AS avg_yield_grams
FROM weedop
GROUP BY strain
ORDER BY avg_yield_grams DESC;
3. Which strains have the highest quality control defects?
SELECT
    strain,
    SUM(qc_defect_flag) AS total_qc_defects
FROM weedop
GROUP BY strain
ORDER BY total_qc_defects DESC;
4. Which cultivation rooms perform best by yield?
SELECT
    cultivation_room,
    AVG(yield_grams) AS avg_yield_grams
FROM weedop
GROUP BY cultivation_room
ORDER BY avg_yield_grams DESC;
5. What products should production prioritize?
SELECT
    strain,
    SUM(revenue) AS total_revenue,
    SUM(units_sold) AS total_units_sold,
    AVG(yield_grams) AS avg_yield_grams,
    SUM(qc_defect_flag) AS total_qc_defects
FROM weedop
GROUP BY strain
ORDER BY total_revenue DESC, total_units_sold DESC, avg_yield_grams DESC;
