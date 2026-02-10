# 🏦 Loan Data Cleaning Pipeline using Pandas

## 📌 Project Overview

Machine Learning is not required for every dataset — but **data cleaning is always required**.

This project demonstrates how to build a **professional data cleaning pipeline using Pandas** on a Loan Approval Prediction dataset.

The goal of this project is to:

* Understand the dataset
* Identify and handle missing values
* Fix incorrect data types
* Standardize text columns
* Handle outliers
* Build a reusable cleaning pipeline function

T

## 📊 Dataset Description

The dataset contains **614 rows and 13 columns**.

### Features:

| Column Name       | Description               |
| ----------------- | ------------------------- |
| Loan_ID           | Unique Loan ID            |
| Gender            | Male / Female             |
| Married           | Yes / No                  |
| Dependents        | Number of dependents      |
| Education         | Graduate / Not Graduate   |
| Self_Employed     | Yes / No                  |
| ApplicantIncome   | Applicant income          |
| CoapplicantIncome | Co-applicant income       |
| LoanAmount        | Loan amount               |
| Loan_Amount_Term  | Loan term (in months)     |
| Credit_History    | Credit history (0 or 1)   |
| Property_Area     | Urban / Rural / Semiurban |
| Loan_Status       | Loan Approved (Y/N)       |

---

## 🧹 Data Cleaning Steps Performed

### ✅ 1. Data Understanding

* Checked dataset shape
* Used `.info()` to inspect data types
* Used `.describe()` to review summary statistics

---

### ✅ 2. Missing Values Handling

* Categorical columns → filled using **Mode**
* Numerical columns → filled using **Median**

Why?

* Mode works best for categorical majority values.
* Median is robust to outliers.

---

### ✅ 3. Fixed Special Column (Dependents)

* Converted `"3+"` → `3`
* Converted column to numeric type

---

### ✅ 4. Text Standardization

* Removed extra spaces
* Converted text to lowercase

Example:

```
" Male " → "male"
```

---

### ✅ 5. Data Type Optimization

* Converted categorical columns to `category` dtype
* Improved memory efficiency

---

### ✅ 6. Outlier Handling

Outliers were capped at the **99th percentile** for:

* `LoanAmount`
* `ApplicantIncome`

This prevents extreme values from affecting analysis.

---

### ✅ 7. Removed Unnecessary Column

* `Loan_ID` was dropped because it does not help in modeling.

---

## 🔁 Reusable Cleaning Function

The project includes a reusable function:

```python
def clean_loan_data(df):
    ...
```

You can reuse this function for:

* Model training
* EDA
* Deployment workflows

---

## ▶️ How to Run in Google Colab

1. Open Google Colab
2. Upload `loan_prediction.csv`
3. Run notebook cells step-by-step
4. Final cleaned dataset will be saved as:

```
cleaned_loan_data.csv
```

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Google Colab

---

## 🎯 Learning Outcomes

After completing this project, you will understand:

* How to inspect a dataset properly
* How to handle missing values professionally
* How to clean categorical data
* How to handle outliers
* How to build a reusable data cleaning pipeline
* Best practices (no inplace operations, safe copying, structured workflow)

---

## 🚀 Future Improvements

This project can be extended to:

* Feature Engineering
* Data Encoding
* Data Scaling
* Building a Machine Learning Model
* Creating a Scikit-learn Pipeline
* Deploying the model

---

## 📌 Author

**Hafiz Muhammad Adnan Taj**

---

## ⭐ Final Note

Data cleaning is one of the most important skills in Data Science.

Before building models, always make sure:

> “Garbage In = Garbage Out”

Clean data leads to better analysis, better models, and better decisions.

---

Happy Learning 🚀
