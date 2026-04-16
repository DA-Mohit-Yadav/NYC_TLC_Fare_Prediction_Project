# New York City Taxi and Limousine Commission Fare Prediction

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" alt="Python Badge">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-green?style=for-the-badge&logo=pandas" alt="Pandas Badge">
  <img src="https://img.shields.io/badge/Scikit%20Learn-Machine%20Learning-orange?style=for-the-badge&logo=scikitlearn" alt="Scikit Learn Badge">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" alt="Status Badge">
</p>

## Overview
This project builds a machine learning model to predict taxi fare amounts using **New York City Taxi and Limousine Commission (TLC)** trip data. It covers the complete data science workflow, including domain understanding, data cleaning, exploratory data analysis (EDA), feature engineering, statistical testing, and ensemble modeling.

The primary objective is to estimate the correct fare for a taxi ride and use these predictions to identify potential **overcharging, meter issues, or data anomalies**.

---

## Problem Statement
Taxi fares depend on factors like distance, duration, pricing type, and timing. However, real-world data often contains inconsistencies. This project aims to build a robust regression model to predict fares and flag records where the actual fare deviates significantly from the expected value.

### Business Use Case
* **Fare Estimation:** Provide users with accurate upfront costs.
* **Fraud Detection:** Identify overcharging or "long-hauling."
* **Data Quality:** Monitor the integrity of TLC trip records.
* **Pricing Analysis:** Understand patterns in pricing across different times and categories.

---

## Dataset Summary
The dataset consists of trip-level records from the NYC TLC.

| Item | Value |
| :--- | :--- |
| **Total Rows** | 22,699 |
| **Total Columns** | 18 |
| **Time Coverage** | 2017 |
| **Data Type** | Trip-level records |

### Key Features
* **Temporal:** `tpep_pickup_datetime`, `tpep_dropoff_datetime`
* **Trip Details:** `passenger_count`, `trip_distance`, `RatecodeID`
* **Target:** `fare_amount` (Tip amount is excluded to prevent data leakage)

---

## Project Workflow

### 1. Data Cleaning & Preprocessing
To ensure model reliability, the following steps were taken:
* Standardized datetime formats and categorical types.
* Removed negative/zero fares and unrealistic trip distances.
* Filtered out disputed payments and extreme outliers (e.g., \$999.99 fares).
* Handled unrealistic trip durations.

### 2. Exploratory Data Analysis (EDA)
* **Distance vs. Fare:** Strong positive correlation.
* **Duration:** Significant impact, though secondary to distance.
* **Distribution:** Fare amounts are right-skewed.
* **Categorical:** Passenger count has a negligible effect on the total fare.

### 3. Statistical Analysis
Validated patterns using:
* **T-tests**
* **ANOVA**
* **Tukey HSD Test** (to verify significant differences between pricing groups).

### 4. Feature Engineering
New features created to capture hidden patterns:
* `ride_duration`: Total time elapsed.
* `time_period`: Categorized as Rush Hour, Mid-day, Night, etc.
* `is_weekend` / `is_holiday`: Boolean indicators.
* `speed`: Average trip speed to detect traffic impact.

---

## Model Architecture

### Preprocessing Pipeline
Built using **Scikit-learn**, the pipeline includes:
* **RobustScaler:** For `trip_distance` and `ride_duration` (handles outliers).
* **StandardScaler:** For `passenger_count`.
* **OneHotEncoder:** For categorical variables.

### The Model: Stacking Regressor
A stacked ensemble was used to capture both linear and non-linear relationships:
* **Base Models:** Linear Regression & Decision Tree Regressor.
* **Meta-Model:** Ridge Regression.

### Performance
| Metric | Value |
| :--- | :--- |
| **Cross-validation $R^2$** | 0.9765 |
| **Test $R^2$** | 0.9526 |

---

## Fraud Detection Logic
The system identifies fraud by calculating the residual between the predicted and actual fare:
> **$\text{Anomaly Flag} = |\text{Actual Fare} - \text{Predicted Fare}| > \text{Threshold}$**

Large discrepancies may indicate meter tampering, inefficient routing, or manual entry errors.

---

## Tech Stack
* **Languages:** Python
* **Data Ops:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn, Statsmodels
* **Utilities:** Holidays, Pickle

---




## Contact Me

[![GitHub](https://img.shields.io/badge/GitHub-DA--Mohit--Yadav-181717?style=for-the-badge&logo=github)](https://github.com/DA-Mohit-Yadav)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mohit%20Yadav-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/mohit-yadav-0394b224a/)

[![Email](https://img.shields.io/badge/Email-mohitkaninwal12%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mohitkaninwal12@gmail.com)
