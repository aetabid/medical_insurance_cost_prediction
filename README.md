# Medical Insurance Cost Analysis

## Overview

Healthcare analytics project using **Python, SQL, Excel, Tableau, and Linear Regression** to identify the factors associated with higher medical insurance charges.

## Tools

Python | Pandas | SQL | SQLite | Excel | Tableau | Scikit-learn | Git

## Data Cleaning

Using Python (Pandas), I reviewed and prepared the raw dataset for analysis:

- Checked missing values and data types
- Removed duplicate records
- Validated numerical and categorical fields
- Saved a cleaned dataset for downstream SQL, Excel, and modeling work

## SQL Findings

Using SQL (SQLite) to query the cleaned dataset — including `GROUP BY` aggregations and `CASE WHEN` bucketing for age and BMI groups — I identified the following cost patterns:

- Smokers averaged **$32,050** in charges vs **$8,441** for non-smokers
- Members over 50 averaged **$18,085**, the highest age group
- Obese members averaged **$15,572**, the highest BMI category
- Southeast had the highest regional average at **$14,735**
- Obese smokers over 50 were the highest-cost group at about **$47,369**

## Excel Billing Reconciliation Workflow

To demonstrate hands-on billing and reconciliation skills, I built a dedicated Excel workbook (`data/processed/Excel/insurance_billing_reconciliation.xlsx`), using formulas (`IF`, `RANDBETWEEN`), data validation dropdowns, and PivotTables to simulate a real billing reconciliation process on top of the cleaned dataset:

- **Cleaned Data** — the full 1,337-record dataset with added Billed Amount, Paid Amount, Variance, and Status columns, flagging each record as Matched, Underpaid - Review, or Overpaid - Review.
- **Adjustments Log** — a filtered log of the 194 flagged records requiring review, with dropdown-driven Reason Code and Action Taken fields simulating a real exception-tracking workflow.
- **Summary Pivot** — a PivotTable summarizing record counts and dollar variance by status:

| Status | Records | Billed Total | Variance |
|---|---|---|---|
| Matched | 1,143 | $15,262,879.08 | $0 |
| Overpaid - Review | 97 | $1,303,883.46 | -$130,388.35 |
| Underpaid - Review | 97 | $1,187,422.88 | $118,742.29 |

This directly reflects billing specialist duties: reconciling billed vs. paid amounts, flagging and tracking discrepancies, and maintaining clean, audit-ready records.

## Predictive Model

Using Python (Pandas and Scikit-learn), I built a Linear Regression model to predict medical insurance charges from the cleaned dataset. Categorical variables were encoded, and the data was split into training and test sets to evaluate how well the model generalizes to unseen data.

**Test Results**
- MAE: **$4,069**
- RMSE: **$5,940**
- R²: **0.80**

Test performance was consistent with training performance, indicating the model generalizes well rather than overfitting to the training data.

## Key Takeaway

Smoking, age, and BMI were the strongest cost-related factors in the dataset. The project demonstrates an end-to-end healthcare analytics workflow — from Python-based data cleaning and SQL analysis, to Excel-based billing reconciliation, Tableau visualization, and predictive modeling.
