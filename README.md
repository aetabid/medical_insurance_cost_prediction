# Medical Insurance Cost Analysis

## Project Overview

This project analyzes medical insurance cost data to identify the factors associated with higher healthcare charges.

The project began as a regression analysis exercise and was expanded into a complete healthcare analytics workflow using Python, SQL, Tableau, and machine learning.

The analysis focuses on answering practical questions about healthcare costs, validating the quality of the underlying data, identifying high-cost member groups, visualizing key trends, and evaluating how accurately medical charges can be predicted.

---

## Business Questions

The analysis was designed to answer five main questions:

1. How much do medical charges differ between smokers and non-smokers?
2. Which age groups have the highest average medical charges?
3. How does BMI category relate to average medical charges?
4. Which regions have the highest average charges?
5. Which combination of age, BMI, and smoking status identifies the highest-cost member groups?

---

## Tools Used

- Python
- Pandas
- NumPy
- SQL
- SQLite
- Tableau
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Git / GitHub

---

## Dataset

The dataset contains 1,338 medical insurance records with the following fields:

- Age
- Sex
- BMI
- Number of children
- Smoking status
- U.S. region
- Medical insurance charges

The primary outcome analyzed in this project is:

`charges`

---

## Data Quality and Cleaning

Before performing the analysis, I reviewed the dataset for:

- Missing values
- Duplicate records
- Incorrect data types
- Invalid numerical ranges
- Inconsistent categorical values
- Potential outliers

No missing values were identified.

One duplicate record was detected and removed, leaving:

**1,337 cleaned records**

The cleaned dataset was saved separately for use in SQL, Tableau, and predictive modeling.

---

## SQL Analysis

After cleaning the data with Python, I loaded the processed dataset into SQLite and used SQL to answer business and healthcare cost questions.

### Smoking Status

Smokers had average medical charges of approximately:

**$32,050**

compared with:

**$8,441**

for non-smokers.

Smokers therefore had approximately **3.8 times higher average charges** in this dataset.

---

### Age Groups

Average medical charges increased substantially with age.

- Under 30: approximately **$9,201**
- Age 30–50: approximately **$13,254**
- Over 50: approximately **$18,085**

Members over age 50 had the highest average charges.

---

### BMI Categories

BMI was grouped into four categories:

- Underweight: below 18.5
- Normal: 18.5–24.9
- Overweight: 25.0–29.9
- Obese: 30.0+

Average charges were approximately:

- Underweight: **$8,852**
- Normal: **$10,409**
- Overweight: **$10,988**
- Obese: **$15,572**

Members classified as obese had the highest average medical charges.

---

### Regional Differences

Average medical charges by region were approximately:

- Southeast: **$14,735**
- Northeast: **$13,406**
- Northwest: **$12,451**
- Southwest: **$12,347**

The Southeast had the highest average medical charges.

Member counts were relatively similar across regions, reducing the likelihood that the difference was caused simply by a substantially larger regional sample.

---

### Highest-Cost Member Groups

The highest-cost group consisted of members who were:

- Over age 50
- Obese
- Smokers

Their average medical charges were approximately:

**$47,369**

Obese smokers between ages 30 and 50 averaged approximately:

**$41,478**

Obese smokers under age 30 averaged approximately:

**$36,761**

This analysis showed that the combination of smoking status, obesity, and increasing age was associated with the highest medical charges in the dataset.

---

## Tableau Dashboard

A Tableau dashboard was created to make the major healthcare cost trends easy to understand visually.

The dashboard includes:

- Average Medical Charges by Smoking Status
- Average Medical Charges by Age Group
- Average Medical Charges by BMI Category

![Medical Insurance Cost Dashboard](images/medical_insurance_dashboard.png)

The Tableau workbook is also included in this repository:

`Medical_Insurance_Cost_Analysis.twbx`

---

## Predictive Modeling

After completing the descriptive and SQL analysis, I built a Linear Regression model to predict medical insurance charges.

The model included:

- Age
- BMI
- Number of children
- Sex
- Smoking status
- Region

Categorical variables were encoded before model training.

The data was separated into training and testing sets to evaluate performance on unseen records.

---

## Model Performance

### Training Results

- MAE: approximately **$4,208**
- RMSE: approximately **$6,098**
- R²: approximately **0.73**

### Test Results

- MAE: approximately **$4,069**
- RMSE: approximately **$5,940**
- R²: approximately **0.80**

The model explained approximately **80% of the variation in medical insurance charges in the test data**.

Residual analysis was also performed to evaluate prediction errors.

---

## Key Findings

The analysis produced several important findings:

1. **Smoking was one of the strongest cost drivers.**  
   Smokers had average medical charges approximately 3.8 times higher than non-smokers.

2. **Medical charges increased with age.**  
   Members over age 50 had substantially higher average charges than younger groups.

3. **Higher BMI was associated with increased costs.**  
   Members classified as obese had the highest average charges among BMI groups.

4. **The combination of risk factors mattered most.**  
   Older obese smokers represented the highest-cost member segment.

5. **Regional differences existed but were smaller than smoking, age, and BMI differences.**

6. **The regression model performed well on unseen data**, achieving a test R² of approximately 0.80.

---

## Skills Demonstrated

This project demonstrates practical experience with:

- Healthcare data analysis
- Data cleaning and validation
- SQL querying
- KPI and metric analysis
- Segmentation
- Data quality review
- Exploratory data analysis
- Tableau dashboard development
- Healthcare cost analysis
- Statistical modeling
- Regression analysis
- Model evaluation
- Data visualization
- Translating analytical results into business insights
- Git and version control

---

## Project Workflow

The project follows an end-to-end analytics workflow:

**Raw Healthcare Data**

↓

**Python Data Cleaning & Validation**

↓

**Processed Dataset**

↓

**SQL Analysis & Business Questions**

↓

**Tableau Dashboard**

↓

**Predictive Modeling**

↓

**Healthcare Cost Insights**

---

## Purpose

The purpose of this project is to demonstrate how healthcare data can be transformed from raw records into meaningful operational and financial insights.

Rather than focusing only on predictive modeling, the project combines data quality, SQL analysis, visualization, and machine learning to demonstrate a complete junior data analyst workflow.
