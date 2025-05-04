
# 🧠 Employee Attrition Risk Prediction

This project identifies employees who are at risk of leaving the company using three machine learning models:
- **Logistic Regression**
- **Decision Tree**
- **Random Forest**

The analysis is designed to support HR decision-making by flagging high-risk individuals for proactive retention actions.

---

## 📂 Dataset Overview
The dataset includes:
- 91 current employees
- 33 former employees

**Features used:**
- `Age`
- `Tenure in the company`
- `Salary`
- `Department`

*Note: The entire dataset was used for modeling (no train/test split), as the goal was to evaluate risk for each existing employee.*

---

## 🔍 Modeling Summary

| Model              | Highlights                                                                 |
|-------------------|----------------------------------------------------------------------------|
| Logistic Regression | Short tenure and low salary strongly associated with risk. Some departments increase risk. |
| Decision Tree      | Tenure is the primary split. Salary and age follow.                        |
| Random Forest      | Tenure > 40% importance. Salary and age are key secondary factors.         |

---

## 📊 Key Insights

- **Short Tenure** is the strongest predictor of attrition across all models.
- **Low Salary** is a strong secondary predictor and potential sign of dissatisfaction.
- **Younger Age** mildly increases risk, especially when combined with short tenure and low pay.
- **Department** has some effect (e.g., Department 3 & 4 increase risk in LR).

---

## 🧑‍💼 Risk Profiles

### ✅ Stable Employee:
- Long tenure
- Higher salary
- Often 40+ years old
- Departments 1 or 2

### ⚠️ At-Risk Employee:
- 0–5 years tenure
- Below-average salary
- Aged 20–35
- Departments 3 or 4

---

## 🏷️ Risk Classification Criteria

| Condition                                    | Risk Level       |
|---------------------------------------------|------------------|
| Flagged by all 3 models                     | Very High Risk   |
| RF + (Tree or LR)                           | High Risk        |
| Only Random Forest                          | Medium-High Risk |
| Tree + LR (without RF)                      | Medium Risk      |
| Only one model (Tree or LR)                 | Low Risk         |
| Not flagged by any model                    | Stable           |

---

## 📁 Files in this Repository

| File | Description |
|------|-------------|
| `logistic_regression.ipynb` | Logistic Regression analysis and predictions |
| `decision_tree.ipynb`       | Decision Tree analysis and risk scoring     |
| `random_forest.ipynb`       | Random Forest analysis and variable importance |
| `Attrition_Risk_Report.pdf` | Final report with business insights         |
