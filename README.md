# Data Wrangling for Loyalty Analysis

## Overview

This project focuses on cleaning, transforming, and feature engineering a **loyalty rewards dataset**. The goal is to create a dataset that is consistent, analysis-ready, and suitable for statistical modeling or machine learning.  

The dataset contains user engagement metrics, demographic details, timestamps, and categorical tags, originally with missing values, inconsistent formatting, and numeric inconsistencies.

---

## Dataset

**Files included:**

- `RewardsData.csv` – Original dataset with raw user records.  
- `RewardsData_Wrangled.csv` – Cleaned, transformed, and feature-engineered dataset.  
- `untitled.ipynb` – Jupyter Notebook containing all steps: data cleaning, transformations, and feature engineering.  

**Columns in the dataset:**

- **Identifiers & Demographics:** `User ID`, `Birthdate`, `City`, `State`, `Zip`  
- **Engagement Metrics:** `Available Points`, `Total Points Earned`, `Points Spent`  
- **Timestamps:** `Joined On`, `Last Seen`  
- **Categorical Labels:** `Tags`  

---

## Data Wrangling Steps

1. **Numeric Cleaning**
   - Corrected inconsistencies in points (`Available Points` = `Total Earned – Points Spent`)  
   - Removed negative or illogical values  

2. **Categorical Cleaning**
   - Normalized `City` and `State`  
   - Replaced missing/garbage values with `"unknown"`  
   - Standardized `Tags` and split multi-labels into lists  

3. **Datetime Cleaning**
   - Converted `Birthdate`, `Joined On`, `Last Seen` to datetime format  
   - Filled missing values  

4. **Numeric Transformations**
   - Applied log, square root, and z-score standardization for skewed columns  

5. **Feature Engineering**
   - Derived `Age`, `Tenure_Days`, `Days_Since_Last_Seen`, `Points_Spent_Ratio`  
   - Processed tags for segmentation and analysis  

---

## Benefits

- **Analysis-Ready:** Ready for behavioral analysis, segmentation, and visualization.  
- **Model-Ready:** Suitable for predictive modeling, including churn prediction and engagement scoring.  
- **Operational Use:** Supports loyalty program insights, customer retention studies, and marketing decisions.  

---

## Usage

1. Clone this repository:
```bash
git clone https://github.com/Nabeelgitz/Data-wrangling-for-loyalty-analysis-data-set.git
