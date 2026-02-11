

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

