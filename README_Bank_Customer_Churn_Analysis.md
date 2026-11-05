# Bank Customer Churn Analysis

## 1. Project Overview
This project analyzes customer churn in a bank dataset and identifies customer characteristics associated with leaving the bank.

The analysis uses Python, Pandas, Matplotlib, and Seaborn. The cleaned dataset contains 10,000 customer records and 12 columns.

## 2. Objective
The main objective is to understand:
- How many customers stayed and how many churned.
- Which customer groups have higher churn rates.
- Whether age, credit score, balance, salary, tenure, product usage, geography, gender, card ownership, and activity are related to churn.
- Which variables show stronger relationships with the churn target.
- How customer characteristics can support churn-reduction decisions.

## 3. Dataset
**File:** `Bank_Churn_Cleaned_Dataset.csv`

### Main columns
| Column | Description |
|---|---|
| CustomerID | Unique customer identifier |
| CreditScore | Customer credit score |
| Geography | Customer country/region |
| Gender | Customer gender |
| Age | Customer age |
| Tenure | Number of years with the bank |
| Balance | Account balance |
| NumOfProducts | Number of bank products used |
| HasCrCard | Whether the customer has a credit card |
| IsActiveMember | Whether the customer is an active member |
| EstimatedSalary | Estimated customer salary |
| Exited | Churn target: 1 = churned, 0 = stayed |

## 4. Derived Features
### Churn
A readable `Churn` column is created:
- `Stayed` → Exited = 0
- `Churned` → Exited = 1

### AgeGroup
Age is grouped into:
- 18–25
- 26–35
- 36–45
- 46–55
- 56–65
- 65+

### HasBalance
Customers are divided into:
- `Balance > 0`
- `Zero Balance`

## 5. Analysis Workflow
1. Load the CSV dataset.
2. Inspect the shape and missing values.
3. Calculate the overall churn rate.
4. Create a readable churn label.
5. Perform categorical churn analysis.
6. Analyze age distribution and age-group churn.
7. Compare numerical variables using boxplots.
8. Compare churn for zero and non-zero balances.
9. Analyze Geography × Gender churn rates.
10. Generate a correlation heatmap.
11. Study the relationship between Age and CreditScore.
12. Save visualization charts for reporting.

## 6. Visualizations

### 01 — Churn Distribution
Shows the proportion and count of customers who stayed versus churned.

### 02 — Churn Rate by Categorical Variables
Compares churn percentages across:
- Geography
- Gender
- Number of products
- Credit-card ownership
- Active-member status

### 03 — Age Analysis
Shows the age distribution for churned/stayed customers and the churn percentage for each age group.

### 04 — Numeric Boxplots
Compares churned and stayed customers for:
- CreditScore
- Balance
- EstimatedSalary
- Tenure

Boxplots help identify differences in central tendency and spread between churn groups.

### 05 — Balance and Churn
Compares churn rates for customers with zero balance and customers with a non-zero balance.

### 06 — Geography × Gender Heatmap
Displays churn percentages for combinations of geography and gender.

### 07 — Correlation Heatmap
Shows correlations among numerical and encoded categorical variables. It helps identify variables that have stronger positive or negative relationships with `Exited`.

### 08 — Age vs Credit Score
A scatter plot showing the relationship between age and credit score, separated by churn status.

## 7. Important Interpretation
The visualizations should be used to identify patterns rather than to claim that one variable directly causes churn.

In general, customer churn analysis can help a bank:
- Identify high-risk customer segments.
- Prioritize retention campaigns.
- Understand customer engagement.
- Review product usage patterns.
- Design targeted offers and support.
- Monitor changes in churn over time.

## 8. Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab / Jupyter Notebook
- CSV dataset

## 9. Required Libraries
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

## 10. How to Run
1. Open the notebook in Google Colab or Jupyter Notebook.
2. Upload `Bank_Churn_Cleaned_Dataset.csv`.
3. Update the CSV path if required.
4. Run the cells from top to bottom.
5. The visualization section generates the charts.
6. The generated chart images can be used in reports or presentations.

## 11. Project Output
The project produces eight major visualization groups:
1. Churn distribution
2. Categorical churn rates
3. Age analysis
4. Numeric boxplots
5. Balance-based churn
6. Geography × Gender heatmap
7. Correlation heatmap
8. Age vs Credit Score scatter plot

A separate PDF containing only these visualization graphs is provided with this project.

## 12. Conclusion
This project provides an exploratory view of bank customer churn. By combining categorical analysis, numerical comparisons, distribution plots, heatmaps, and correlation analysis, the bank can better understand which customer segments require attention.

The analysis is exploratory and should be combined with statistical testing and/or a predictive machine-learning model before making automated business decisions.
