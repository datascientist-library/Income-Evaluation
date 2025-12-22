
---

# 💰 Income Evaluation & Prediction (<=50K / >50K)

## 📌 Project Overview

This capstone project focuses on **income evaluation across different countries** using demographic, educational, and occupational data.
The objective is to **build a machine learning model** that predicts whether an individual's income exceeds **50K per year**, while also identifying the **key factors contributing to higher income levels**.

Such a model can help organizations, policymakers, and analysts better understand income distribution and socio-economic patterns.

---

## 🎯 Problem Statement

Given a set of personal and professional attributes, predict whether a person’s income falls into one of the following categories:

* **0** → Income ≤ 50K
* **1** → Income > 50K

This is treated as a **binary classification problem**.

---

## 📂 Dataset Information

* **Total Rows:** 32,561
* **Total Columns:** 15
* **Target Variable:** Income threshold (<=50K, >50K)

### 🔑 Feature Description

| No. | Feature Name     | Description                        |
| --- | ---------------- | ---------------------------------- |
| 1   | Age              | Age of the individual              |
| 2   | Work-class       | Employment / profession category   |
| 3   | Final_census     | Census population indicator        |
| 4   | Education        | Highest education qualification    |
| 5   | Education_num    | Years spent in education           |
| 6   | Marital Status   | Marital status of the individual   |
| 7   | Occupation       | Type of occupation                 |
| 8   | Relationship     | Relationship or dependency status  |
| 9   | Race             | Ethnicity                          |
| 10  | Gender           | Gender of the individual           |
| 11  | Capital-gain     | Profit from sale of capital assets |
| 12  | Capital-loss     | Loss from sale of capital assets   |
| 13  | Hours/week       | Working hours per week             |
| 14  | Country          | Country of residence               |
| 15  | Income threshold | Target column (<=50K / >50K)       |

---

## 🧹 Data Cleaning & Preprocessing

During data exploration and preprocessing, the following steps were performed:

* Identified **24 duplicate records** and removed them.
* Dropped **unnecessary columns** with excessive missing values.
* Handled missing values:

  * `capital-gain` and `capital-loss` contained missing values represented as `0`
  * `work-class`, `occupation`, and `country` contained missing values represented as `?`
* Encoded target labels:

  * `<=50K` → **0**
  * `>50K` → **1**
* Addressed **class imbalance**:

  * Income ≤ 50K → 24,720 records
  * Income > 50K → 7,841 records
  * Applied **SMOTE (Synthetic Minority Oversampling Technique)** to balance the dataset

---

## 📊 Exploratory Data Analysis (EDA)

Key insights derived from data visualization and categorical analysis:

### 🔍 Key Observations

1. **Gender Impact**

   * Males have a significantly higher proportion in the **>50K income group**
   * Females are predominantly concentrated in the **≤50K income group**

2. **Marital Status**

   * Individuals with **married-civ-spouse** status are more likely to earn >50K
   * Never-married, divorced, and separated individuals mostly fall under ≤50K

3. **Education Level**

   * Higher education levels (Bachelors, Masters, Doctorate) strongly correlate with income >50K
   * Lower education levels are mostly associated with income ≤50K

4. **Occupation**

   * High-paying roles: *Exec-managerial, Prof-specialty, Tech-support*
   * Lower-paying roles: *Handlers-cleaners, Machine-op-inspct, Other-service*

### 📌 Conclusion from EDA

Income level is strongly influenced by:

* Gender
* Marital status
* Education
* Occupation

Individuals who are **male, married, highly educated, and working in professional or managerial roles** are more likely to earn above 50K.

---

## 🤖 Machine Learning Models Trained

The following models were trained and evaluated:

| Model                     | Accuracy | Precision | Recall   | F1-Score |
| ------------------------- | -------- | --------- | -------- | -------- |
| Logistic Regression       | 0.80     | 0.55      | 0.85     | 0.67     |
| Decision Tree             | 0.80     | 0.58      | 0.65     | 0.61     |
| Random Forest             | 0.84     | 0.67      | 0.70     | 0.68     |
| Gradient Boosting         | 0.83     | 0.61      | 0.83     | 0.71     |
| XGBoost                   | **0.85** | **0.67**  | **0.77** | **0.72** |
| Support Vector Classifier | 0.81     | 0.57      | 0.86     | 0.69     |

---

## 🏆 Model Selection & Optimization

* **XGBoost** delivered the best baseline performance with **85% accuracy**
* Applied:

  * Hyperparameter tuning
  * Cross-validation
* Final optimized model achieved:

  * ✅ **87% accuracy**
  * Strong balance between precision and recall

This makes the model reliable for predicting income thresholds.

---

## 📈 Final Results

* Successfully built a **robust income prediction model**
* Identified **key socio-economic factors** affecting income
* Final model performs well even on imbalanced data

---

## 🛠️ Tech Stack

* **Programming Language:** Python
* **Libraries:** NumPy, Pandas, Matplotlib, Seaborn
* **ML Libraries:** Scikit-learn, XGBoost, Imbalanced-learn (SMOTE)

---

## 👤 Author

**Mihir Patil**
MSc Data Science Aspirant | Data Enthusiast

---

If you want, I can also:

* ✨ Make this **more concise**
* 🧑‍💼 Rewrite it in a **recruiter-focused style**
* 📦 Add a **project folder structure** section
* 📊 Add **sample visualizations section**

Just tell me 👍
