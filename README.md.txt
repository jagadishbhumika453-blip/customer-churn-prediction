# Customer Churn Prediction using Machine Learning

## Project Overview

This project focuses on predicting whether a customer is likely to churn or continue using a service.

The project uses the Telco Customer Churn dataset from Kaggle. Machine Learning classification algorithms are applied to analyze customer information and predict customer churn.

The complete Machine Learning workflow is implemented in a Kaggle Notebook, including data exploration, data cleaning, exploratory data analysis, preprocessing, model training, evaluation, model comparison, and prediction.

---

## Problem Statement

Customer churn is an important problem for service-based companies. Losing customers can affect revenue and business growth.

The objective of this project is to develop a Machine Learning model that can predict whether a customer is likely to leave the service based on customer information such as:

- Tenure
- Contract type
- Internet service
- Payment method
- Monthly charges
- Total charges
- Customer services
- Demographic information

The prediction can help businesses identify customers who are at risk of leaving and take suitable retention actions.

---

## Dataset

The dataset used in this project is the **Telco Customer Churn Dataset** available on Kaggle.

### Dataset Source

Kaggle:
https://www.kaggle.com/datasets/palashfendarkar/wa-fnusec-telcocustomerchurn

### Dataset Size

- Rows: 7043
- Columns: 21

### Target Variable

`Churn`

The target variable contains two classes:

- `Yes` – Customer has churned
- `No` – Customer has not churned

---

## Features

The dataset contains the following features:

| Feature | Description |
|---|---|
| customerID | Unique customer identifier |
| gender | Customer gender |
| SeniorCitizen | Whether the customer is a senior citizen |
| Partner | Whether the customer has a partner |
| Dependents | Whether the customer has dependents |
| tenure | Number of months the customer has stayed |
| PhoneService | Whether phone service is subscribed |
| MultipleLines | Multiple phone lines status |
| InternetService | Type of internet service |
| OnlineSecurity | Online security subscription |
| OnlineBackup | Online backup subscription |
| DeviceProtection | Device protection subscription |
| TechSupport | Technical support subscription |
| StreamingTV | Streaming TV subscription |
| StreamingMovies | Streaming movies subscription |
| Contract | Customer contract type |
| PaperlessBilling | Paperless billing status |
| PaymentMethod | Payment method |
| MonthlyCharges | Monthly customer charges |
| TotalCharges | Total customer charges |
| Churn | Customer churn status |

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Kaggle

---

## Machine Learning Workflow

The following workflow was followed:

1. Dataset loading
2. Dataset exploration
3. Data cleaning
4. Missing value handling
5. Duplicate record checking
6. Exploratory Data Analysis
7. Feature engineering
8. Categorical variable encoding
9. Train-test split
10. Feature scaling
11. Model training
12. Model evaluation
13. Model comparison
14. Best model selection
15. Feature importance analysis
16. Customer churn prediction

---

## Data Cleaning

The dataset was checked for missing values, blank values, and duplicate records.

The `TotalCharges` column contained blank values. These blank values were converted into missing values and replaced using the median of the column.

The `customerID` column was removed because it is only an identifier and does not provide useful information for predicting churn.

Duplicate records were also checked and removed if present.

---

## Exploratory Data Analysis

Several visualizations were created to understand customer churn patterns.

### Churn Distribution

The distribution of churned and non-churned customers was analyzed.

### Contract Type vs Churn

Customers with month-to-month contracts showed a higher tendency to churn compared with customers having longer-term contracts.

### Tenure vs Churn

Customers with shorter tenure were generally more likely to churn.

### Internet Service vs Churn

Churn behavior varied across different internet service types.

### Payment Method vs Churn

Different payment methods showed different levels of customer churn.

### Monthly Charges vs Churn

Customers with higher monthly charges generally showed higher churn tendencies.

### Senior Citizen vs Churn

Churn behavior differed between senior and non-senior customers.

---

## Data Preprocessing

The following preprocessing techniques were applied:

### Target Encoding

The `Churn` column was converted into numerical values:

- `No` → 0
- `Yes` → 1

### Categorical Encoding

Categorical variables were converted into numerical values using one-hot encoding.

```python
pd.get_dummies(X, drop_first=True)