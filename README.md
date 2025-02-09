# Loan Approval Prediction

## Project Overview
This project aims to build a **loan approval prediction model** using **machine learning**. The model predicts whether a loan application should be approved or rejected based on financial and demographic data. It has been deployed using **FastAPI** and **Render**.

---

## 1. Problem Definition
### Objective:
The goal of this project is to predict **loan approval** based on various financial and personal attributes of an applicant.

### Why This Matters:
- Helps financial institutions make **data-driven** decisions.
- Reduces **risk** by identifying potentially **risky loan applicants**.
- Speeds up the **loan approval process**.

---

## 2. Data Source and Description
The dataset consists of **4,269 loan applications** with **13 original features**. After preprocessing (e.g., One-Hot Encoding), the final model uses **16 input features**.

### Features:
1. `loan_id`: Unique ID for the loan application.
2. `no_of_dependents`: Number of dependents.
3. `education`: Graduate / Not Graduate.
4. `self_employed`: Yes / No.
5. `income_annum`: Annual income (in currency).
6. `loan_amount`: Loan amount requested.
7. `loan_term`: Duration of the loan (months).
8. `cibil_score`: Credit score of the applicant.
9. `residential_assets_value`: Value of residential assets.
10. `commercial_assets_value`: Value of commercial assets.
11. `luxury_assets_value`: Value of luxury assets.
12. `bank_asset_value`: Total bank assets.
13. `debt_to_income_ratio`: Debt-to-income ratio.
14. `total_assets`: Sum of all assets.
15. `education_Graduate`: One-Hot Encoded feature.
16. `self_employed_Yes`: One-Hot Encoded feature.

---

## 3. Exploratory Data Analysis (EDA)
**Findings from EDA:**
- Income and loan amount **show a correlation**.
- **CIBIL score** has a strong impact on loan approval.
- **Self-employed applicants** have a slightly lower approval rate.

**Visualizations:**
- Distribution of **income** and **loan amounts**.
- Relationship between **CIBIL score** and approval status.
- Feature importance analysis.

---

## 4. Data Preprocessing
### Steps Taken:
✅ **Handling Missing Values**  
✅ **Outlier Detection & Removal**  
✅ **Scaling Numerical Features**  
✅ **One-Hot Encoding for Categorical Features**  

**Final Feature Count:** 16 input features after transformations.

---

## 5. Model Selection & Training
The **Random Forest Classifier** was chosen due to:
- High accuracy.
- Ability to handle both categorical and numerical features.
- Robustness to missing and unscaled data.

**Hyperparameter tuning was performed using GridSearchCV.**  

---

## 6. Model Evaluation
The model was evaluated using:
✅ **Accuracy**  
✅ **Precision, Recall, F1-Score**  
✅ **AUC-ROC Curve**  

---

## 7. Model Interpretation
### Key Insights:
- **CIBIL score** is the most important feature.
- **Income and assets** significantly impact the prediction.
- **Loan term** has a moderate influence.

---

## 8. Deployment
### How the API Works:
- Built using **FastAPI**.
- The model is **served via an API** that accepts JSON requests.
- A **frontend UI** allows users to input loan details.

### How to Run Locally:
1. **Clone the repository**
   ```bash
   git clone https://github.com/kalebb1/Loan-Approval-Prediction
   cd loan-approval-predictor

2. ### Access using a website:

   [visit](https://loan-approval-prediction-tqbe.onrender.com/)

  
