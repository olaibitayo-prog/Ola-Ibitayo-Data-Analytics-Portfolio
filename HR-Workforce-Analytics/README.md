# HR Workforce Analytics Dashboard

## Project Overview

This project analyzes workforce data to identify employee trends, improve retention strategies, and support data-driven human resource decision-making.

The goal is to demonstrate how organizations can use analytics to understand workforce performance, employee engagement, and organizational health.

---

## Business Problem

Organizations collect large amounts of employee data across departments, roles, performance reviews, and retention records.

Without effective analytics, HR leaders may struggle to understand:

- Employee turnover risks
- Workforce performance trends
- Hiring effectiveness
- Department-level challenges
- Employee engagement patterns

This project transforms HR data into actionable insights.

---

## Business Questions

This analysis answers:

1. What factors contribute to employee turnover?
2. Which departments experience the highest attrition?
3. How does employee satisfaction relate to retention?
4. Are salary, tenure, or workload influencing resignations?
5. Which workforce areas need management attention?

---

## Dataset

The dataset includes:

- Employee information
- Departments
- Job roles
- Salary data
- Performance ratings
- Satisfaction scores
- Tenure
- Attrition status

---

## Key Performance Indicators (KPIs)

Metrics analyzed:

- Employee Count
- Attrition Rate
- Retention Rate
- Average Tenure
- Employee Satisfaction
- Performance Rating
- Department Turnover Rate

---

## Data Cleaning Process

Issues addressed:

- Missing employee information
- Duplicate employee records
- Incorrect data types
- Inconsistent department names
- Missing performance values

Cleaning steps:

- Removed duplicates
- Standardized categories
- Corrected formatting
- Prepared reporting tables

---

## SQL Analysis

SQL was used to analyze:

- Employee retention
- Department trends
- Workforce demographics
- Performance metrics


Example:

Employee turnover by department:

```sql
SELECT
    department,
    COUNT(*) AS employees_left
FROM employees
WHERE attrition = 'Yes'
GROUP BY department
ORDER BY employees_left DESC;
