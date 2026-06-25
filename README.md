# 📉 Telecom Customer Churn Analysis

An end-to-end exploratory data analysis (EDA) on a telecom company's customer dataset to identify churn patterns, uncover business-level defects, and recommend actionable retention strategies.

---

## 📌 Problem Statement

Customer churn is one of the most costly problems in the telecom industry. This project analyses a real-world telecom dataset to answer:
- **Who is churning?** (demographics, tenure, contract type)
- **Why are they churning?** (services, payment methods, engagement)
- **What can the company do to retain them?**

---

## 📂 Repository Structure

```
telecom-churn-analysis/
│
├── Telecom Churn Analysis.ipynb           # Main analysis notebook
├── Customer Churn.csv                     # Dataset
├── Telecom_Churn_Analysis_Summary.pdf     # One-page executive summary report
└── README.md
```

---

## 📊 Dataset Overview

| Feature | Description |
|---|---|
| `customerID` | Unique customer identifier |
| `gender` | Male / Female |
| `SeniorCitizen` | Whether the customer is a senior citizen |
| `tenure` | Months the customer has been with the company |
| `Contract` | Month-to-month / One year / Two year |
| `PaymentMethod` | Electronic check, mailed check, bank transfer, credit card |
| `TotalCharges` | Total amount charged to the customer |
| `Churn` | Whether the customer churned (Yes / No) — **target variable** |

> Dataset source: (https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

---

## 🔍 Analysis Performed

### 1. Data Cleaning
- Fixed `TotalCharges` column (whitespace → 0, cast to float)
- Verified zero null values and no duplicate customer IDs
- Encoded `SeniorCitizen` from binary (0/1) to readable Yes/No labels

### 2. Churn Distribution
- **26.54%** of customers have churned — a significant business problem
- Visualised using countplot and pie chart

### 3. Demographic Analysis
- **Gender**: No significant difference in churn between males and females
- **Senior Citizens**: Churn at a disproportionately higher rate than non-seniors

### 4. Tenure Analysis
- Customers in their **first 1–2 months** churn in very large numbers
- Long-tenure customers show strong retention — loyalty builds over time

### 5. Contract Type
- **Month-to-month** contracts have the highest churn rate
- Customers on 1-year or 2-year contracts are far more likely to stay

### 6. Services Analysis (9 features)
Analysed: `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`

- Customers **without** OnlineSecurity, TechSupport, and OnlineBackup churn significantly more
- These services act as "stickiness" features — low adoption is a retention risk

### 7. Payment Method
- **Electronic Check** users have the highest churn rate among all payment methods
- Automated payment methods (bank transfer, credit card) correlate with lower churn

---

## 💡 Key Findings

| Finding | Impact |
|---|---|
| 26.54% overall churn rate | High — industry average is ~15–25% |
| Month-to-month contract users churn most | Contract flexibility = low commitment |
| Churn spikes in months 1–2 | Onboarding failure point |
| Senior citizens churn more | Underserved demographic |
| E-Check users churn most | Payment friction / financial stress signal |
| Low add-on adoption → higher churn | Services aren't being cross-sold |

---

## ✅ Recommendations

1. **Incentivise longer contracts** — Discounts and perks for annual/2-year plan upgrades
2. **Build a 30-day onboarding programme** — Structured check-ins to anchor new customers early
3. **Bundle sticky services by default** — Include OnlineSecurity and TechSupport in standard plans
4. **Target Electronic Check users** — Offer bill credits to migrate them to auto-pay
5. **Create a Senior Citizen plan** — Simplified pricing, dedicated support, proactive outreach
6. **Build a churn prediction model** — Score customers monthly and intervene before they leave

---

## 🛠️ Tools & Libraries

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-lightgrey?logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualisation-teal)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Plotting-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/your-username/telecom-churn-analysis.git
cd telecom-churn-analysis

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn

# 3. Launch the notebook
jupyter notebook Telecom_Churn_Analysis.ipynb
```

---
**Amarendra Andia** — Metallurgical & Materials Engineering Student, NIT Jamshedpur
