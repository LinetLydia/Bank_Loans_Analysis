# **Credit Risk Analysis using Machine Learning and SQL**

## **1. Project Overview**
This project focuses on analyzing credit risk and predicting loan defaults using a dataset of 45,000 loan applicants.  
The dataset contains demographic, financial, and credit-related attributes that help assess the likelihood of loan repayment.

The goal is to:
- Identify key factors influencing loan default.
- Build a predictive model for loan repayment probability.
- Provide actionable insights for better credit risk management.

---

## **2. Dataset Description**
The dataset contains **45,000 records** with the following key features:

| Category | Feature | Description |
|-----------|----------|-------------|
| **Personal Information** | `person_age` | Age of the applicant |
| | `person_gender` | Gender (male/female) |
| | `person_education` | Education level (High School, Bachelor, etc.) |
| | `person_income` | Annual income (USD) |
| | `person_emp_exp` | Employment experience (years) |
| | `person_home_ownership` | Home ownership type (RENT, OWN, MORTGAGE) |
| **Loan Details** | `loan_amnt` | Loan amount requested |
| | `loan_intent` | Purpose of the loan |
| | `loan_int_rate` | Interest rate (%) |
| | `loan_percent_income` | Ratio of loan amount to income |
| **Credit History** | `cb_person_cred_hist_length` | Credit history length (years) |
| | `credit_score` | Applicant’s credit score |
| | `previous_loan_defaults_on_file` | Previous loan defaults (Yes/No) |
| **Target Variable** | `loan_status` | 1 = Repaid, 0 = Defaulted |

---

## **3. Steps in the Project**
### **Step 1: Business Understanding**
Define the goal — to assess credit risk and predict potential loan defaults to help lenders make data-driven decisions.

### **Step 2: Data Understanding**
- Loaded and explored the dataset.
- Examined structure, data types, and distributions.
- Verified data completeness and quality.

### **Step 3: Data Preparation**
- Imported the dataset into SQLite.
- Checked table schema using `PRAGMA table_info()`.
- Verified column names and data types for SQL analysis.

### **Step 4: Exploratory Data Analysis (EDA)**
Performed SQL-based and visual analysis to uncover patterns:
- Default rate by loan purpose.
- Repayment rate by credit score category.
- Effect of previous defaults on repayment.
- Impact of income group and home ownership.

### **Step 5: Visualization of Insights**
Visualized findings using Seaborn and Matplotlib for:
- Loan status distribution.
- Default rates across loan types, credit scores, and income levels.

### **Step 6: Model Building**
- Trained a **Random Forest Classifier** to predict loan repayment.
- Achieved an accuracy of **93%**.
- Evaluated performance using **Precision, Recall, F1-Score**, and **Confusion Matrix**.

### **Step 7: Model Optimization**
- Used **GridSearchCV** for hyperparameter tuning.
- Applied **5-fold Cross-Validation** for robustness.
- Final model achieved improved and consistent performance across folds.

---

## **4. Key Findings**
- **77.78%** of applicants defaulted on their loans, while only **22.22%** repaid successfully.
- **Venture** and **Education** loans had the highest default rates.
- Applicants with **previous loan defaults** had a **0% repayment rate**.
- Higher **income** and better **credit scores** slightly improved repayment odds, though anomalies exist.
- **Previous defaults**, **loan_percent_income**, and **loan_int_rate** were the top predictors of loan performance.

---

## **5. Technologies Used**
- **Python:** Data analysis and model development  
- **SQLite:** SQL-based data querying  
- **Pandas & NumPy:** Data handling and transformation  
- **Matplotlib & Seaborn:** Visualization  
- **Scikit-learn:** Model training and evaluation  

---

## **6. Conclusion**
The project successfully demonstrates how machine learning and SQL analytics can be combined to assess credit risk.  
The final model achieves high accuracy and identifies critical risk factors such as previous defaults and income-to-loan ratio, helping lenders make more informed credit decisions.

---

## **7. Future Work**
- Incorporate additional behavioral data (e.g., payment history).
- Test ensemble models (XGBoost, LightGBM).
- Implement model explainability (SHAP/LIME).
- Build an interactive dashboard for real-time credit risk scoring.

