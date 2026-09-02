# Medical Insurance Cost Analysis

## Overview

Healthcare analytics project using **Python, SQL, Tableau, and Linear Regression** to identify the factors associated with higher medical insurance charges.

## Tools

Python | Pandas | SQL | SQLite | Tableau | Scikit-learn | Git

## Data Cleaning

- Checked missing values and data types
- Removed 1 duplicate record
- Validated numerical and categorical fields
- Saved a cleaned dataset with **1,337 records**

## SQL Findings

- Smokers averaged **$32,050** in charges vs **$8,441** for non-smokers
- Members over 50 averaged **$18,085**, the highest age group
- Obese members averaged **$15,572**, the highest BMI category
- Southeast had the highest regional average at **$14,735**
- Obese smokers over 50 were the highest-cost group at about **$47,369**

## Tableau Dashboard

The dashboard compares average medical charges by:

- Smoking status
- Age group
- BMI category

![Medical Insurance Dashboard](images/medical_insurance_dashboard.png)

## Predictive Model

Linear Regression was used to predict medical insurance charges.

**Test Results**
- MAE: **$4,069**
- RMSE: **$5,940**
- R²: **0.80**

## Key Takeaway

Smoking, age, and BMI were the strongest cost-related factors in the dataset. The project demonstrates an end-to-end healthcare analytics workflow from data cleaning and SQL analysis to visualization and predictive modeling.
