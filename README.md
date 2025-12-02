# 💳 Credit Card Behaviour Score Prediction
### Finance Club | IIT Roorkee
**Risk Assessment & Default Prediction using Advanced Classification Techniques**

---

### 📌 Project Overview
[cite_start]This project focuses on minimizing financial losses for lending institutions by predicting the likelihood of customer credit card defaults[cite: 66, 85]. [cite_start]Using a dataset of **25,000+ records**, we engineered a robust machine learning pipeline to identify key drivers of default and generate a 14-day rolling inventory plan[cite: 147].

The solution addresses the challenge of **class imbalance** and optimizes for **Recall** to ensure high-risk customers are accurately identified.

### ⚙️ Technical Architecture

#### 1. Data Processing & Engineering
* [cite_start]**Data Cleaning:** Handled missing values (Age) and resolved categorical inconsistencies in Education/Marriage columns[cite: 151, 420].
* [cite_start]**Outlier Management:** Applied **Winsorization (1%)** instead of IQR clipping to preserve valuable financial variability in bill/payment amounts[cite: 967].
* **Feature Engineering:**
    * [cite_start]`Credit_Utilization_Ratio`: Ratio of average bill to credit limit[cite: 457].
    * [cite_start]`Max_Delinquency_Streak`: Longest consecutive overdue period[cite: 462].
    * [cite_start]`AVG_Bill_Amt`: Smoothed spending behavior metric[cite: 452].
* [cite_start]**Feature Selection:** Dropped statistically insignificant features (`BILL_AMT_MAY`, `BILL_AMT_APR`) based on p-value testing[cite: 1099].

#### 2. Advanced Modeling Strategy
* [cite_start]**Class Imbalance Handling:** Applied **SMOTE (Synthetic Minority Over-sampling Technique)** on training data to balance the Non-Default vs. Default ratio[cite: 1190].
* [cite_start]**Hyperparameter Tuning:** Utilized **Optuna** for Bayesian optimization of model parameters[cite: 1243].
* [cite_start]**Models Evaluated:** Logistic Regression, Random Forest, XGBoost, and LightGBM[cite: 1242].

---

### 📊 Key Results & Performance

**Champion Model: LightGBM**
[cite_start]Selected for its superior balance of speed, precision, and recall, making it ideal for real-time risk assessment[cite: 1412].

| Metric | LightGBM (Best) | XGBoost | Random Forest | Logistic Reg |
| :--- | :--- | :--- | :--- | :--- |
| **F2 Score** | **0.8094** | 0.8123 | 0.8124 | 0.7439 |
| **Recall** | **0.8105** | 0.8157 | 0.8129 | 0.6000 |
| **Accuracy** | **0.8105** | 0.8157 | 0.8129 | 0.7383 |
| **AUC Score** | **0.75** | 0.75 | 0.76 | 0.74 |

> *Note: We prioritized the **F2 Score** and **Recall** to minimize False Negatives (missed defaulters), which carry the highest financial risk.*

---

### 💡 Business Insights
* [cite_start]**Demographics:** Young individuals (ages 23-44) show a higher risk of default compared to older demographics[cite: 477].
* [cite_start]**Education:** University graduates exhibited the highest count of defaults, necessitating stratified risk analysis[cite: 530].
* [cite_start]**Payment Behavior:** Strong correlation observed between immediate past payment history (e.g., Sept/Aug) and default probability[cite: 926].

---

### 🛠️ Tech Stack
* [cite_start]**Language:** Python 3.11 🐍 [cite: 70]
* **Libraries:** Pandas, NumPy, Scikit-learn, Imbalanced-learn (SMOTE).
* **Boosting:** XGBoost, LightGBM.
* **Optimization:** Optuna.
* [cite_start]**Environment:** Google Colab (GPU accelerated)[cite: 77].

---

### 👨‍💻 Author
**Alumolu Rakesh Reddy**
* **ID:** 22117017
* **Department:** Mechanical Engineering, IIT Roorkee
* **Project:** Finance Club Open Project

> *Submitted as part of the Credit Card Behaviour Score Prediction project under the guidance of the Finance Club, IIT Roorkee.*
