# 💳 Credit Card Default Prediction

A complete end-to-end machine learning pipeline for predicting credit card payment defaults, built as part of a practical skills assignment. The project covers exploratory data analysis, data preparation, model training, evaluation, and interpretability using SHAP.

---

## 📁 Repository Structure

```
├── Credit_Card.csv                  # Dataset (see details below)
└── README.md                        # This file
```

---

## 📊 Dataset — `Credit_Card.csv`

### Overview

| Property | Value |
|---|---|
| **Filename** | `Credit_Card.csv` |
| **Records** | 34,788 |
| **Features** | 30 |
| **Target variable** | `default.payment.next.month` |
| **Time period** | April – September 2005 |
| **Domain** | Credit risk / Financial services |

The dataset contains demographic, credit limit, billing, and payment history information for credit card clients. The target variable indicates whether a client **defaulted** on their payment in the following month (`1 = Default`, `0 = No Default`). 

---

### Column Descriptions

| # | Column | Type | Description |
|---|--------|------|-------------|
| 1 | `ID` | int | Unique client identifier |
| 2 | `LIMIT_BAL` | float | Credit limit in New Taiwan dollars. Contains missing values |
| 3 | `SEX` | float | Gender (1 = Male, 2 = Female). Contains missing values |
| 4 | `EDUCATION` | float | Education level (1 = Graduate school, 2 = University, 3 = High school, 4–6 = Other). Contains missing values |
| 5 | `MARRIAGE` | float | Marital status (1 = Married, 2 = Single, 3 = Other). Contains missing values |
| 6 | `AGE` | float | Client age in years (range: 21–79). Contains missing values |
| 7 | `PAY_0` | int | Repayment status — September (-2 = No consumption, -1 = Paid in full, 0 = Minimum paid, 1–8 = Months delayed) |
| 8 | `PAY_2` | int | Repayment status — August |
| 9 | `PAY_3` | int | Repayment status — July |
| 10 | `PAY_4` | int | Repayment status — June |
| 11 | `PAY_5` | int | Repayment status — May |
| 12 | `PAY_6` | int | Repayment status — April |
| 13 | `BILL_AMT1` | float | Statement bill amount — September (NT dollars) |
| 14 | `BILL_AMT2` | float | Statement bill amount — August |
| 15 | `BILL_AMT3` | float | Statement bill amount — July |
| 16 | `BILL_AMT4` | float | Statement bill amount — June |
| 17 | `BILL_AMT5` | float | Statement bill amount — May |
| 18 | `BILL_AMT6` | float | Statement bill amount — April |
| 19 | `PAY_AMT1` | float | Payment amount made — September (NT dollars). Contains missing values |
| 20 | `PAY_AMT2` | float | Payment amount made — August. Contains missing values |
| 21 | `PAY_AMT3` | float | Payment amount made — July |
| 22 | `PAY_AMT4` | float | Payment amount made — June |
| 23 | `PAY_AMT5` | float | Payment amount made — May |
| 24 | `PAY_AMT6` | float | Payment amount made — April |
| 25 | `default.payment.next.month` | int | **Target variable** — 1 = Defaulted, 0 = Did not default |
| 26 | `risk_leak` | float | Continuous risk score derived from payment behaviour (range: -0.39 to 1.40) |
| 27 | `BILL_AMT_SUM` | float | Total cumulative bill amount across all six months (NT dollars) |
| 28 | `LIMIT_BAL_LOG` | float | Natural logarithm of `LIMIT_BAL` — normalises the skewed credit limit distribution |
| 29 | `CITY` | str | Anonymised city label associated with the client's account (50 unique values: City_1 to City_50) |
| 30 | `RISK_RATING` | int | Categorical risk classification (1 = Low, 2 = Medium, 3 = High) |

---

## 📄 License

This project is intended for **educational purposes** as part of a practical machine learning assignment.
