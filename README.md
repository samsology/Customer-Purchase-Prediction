# TECH CRUSH Data Science 2026

## Team Dynamo (Group 14)

### Retail / Marketing: Customer Purchase Prediction

---

## 📌 Project Overview

Retail and e-commerce businesses continuously seek to increase conversion rates and maximize marketing ROI. Understanding **which customers are likely to complete a purchase** enables more efficient ad spend allocation, targeted campaigns, and personalized offers.

This project develops a **classification model** that predicts whether an online shopper will complete a purchase based on browsing behavior and demographic information.

The project was completed as part of the **Tech Crush Data Science 2026 Capstone Program** by **Team Dynamo**.

---

## 🎯 Business Problem

An e-commerce company wants to predict whether a customer session will result in a purchase.

### Objectives:

1. Perform **Exploratory Data Analysis (EDA)** to uncover behavioral patterns.
2. Preprocess and prepare data for modeling.
3. Build and compare classification models.
4. Optimize the best-performing model.
5. Provide business-driven recommendations.

---

## 📂 Dataset

**Source:** Kaggle – Online Shoppers Purchasing Intention Dataset
[https://www.kaggle.com/datasets/imakash3011/online-shoppers-purchasing-intention-dataset](https://www.kaggle.com/datasets/imakash3011/online-shoppers-purchasing-intention-dataset)

### Dataset Description

The dataset contains user session-level data including:

* Administrative page visits
* Informational page visits
* Product-related page visits
* Bounce rates
* Exit rates
* Page values
* Month
* Operating system
* Browser
* Region
* Traffic type
* Visitor type
* Weekend indicator
* Target variable: `Revenue` (Purchase / No Purchase)

---

## 🧠 Project Workflow

### 1️⃣ Business Understanding

* Defined problem scope.
* Identified key business KPIs (conversion rate, precision, recall).
* Established performance evaluation strategy.

---

### 2️⃣ Data Understanding

* Examined dataset structure and feature types.
* Checked for missing values and data consistency.
* Identified categorical vs numerical variables.
* Evaluated class distribution.

Observation:

* Dataset is slightly imbalanced (fewer purchase cases).

---

## 🔎 3️⃣ Exploratory Data Analysis (EDA)

### Univariate Analysis

* Distribution of numerical features.
* Frequency distribution of categorical variables.
* Purchase rate across months and visitor types.

### Bivariate Analysis

* Purchase behavior vs:

  * Page value
  * Product-related duration
  * Bounce rate
  * Visitor type
  * Weekend sessions

### Correlation & Multicollinearity

* Correlation heatmap to detect strong linear relationships.
* Identified key predictive features.

---

### 📊 Key Behavioral Findings

1. **Higher page value strongly correlates with purchase completion.**
2. Increased **product-related page duration** increases likelihood of conversion.
3. High **bounce rate and exit rate** negatively affect purchase probability.
4. Returning visitors show higher conversion likelihood.
5. Some seasonal/month-based variation exists.

These findings align with practical e-commerce behavior patterns.

---

## 🧹 4️⃣ Data Preprocessing

### Steps Performed:

* Label encoding for categorical variables.
* One-hot encoding where necessary.
* Train-test split.
* Feature scaling (where required).
* Handling class imbalance considerations.
* Multicollinearity checks.

---

## 🤖 5️⃣ Model Building & Evaluation

Three classification models were built and compared:

1. Logistic Regression
2. Decision Tree
3. Random Forest

Evaluation metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC

---

## 📈 Model Performance Summary

| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| ------------------- | -------- | --------- | ------ | -------- | ------- |
| Logistic Regression | 0.8517   | 0.5172    | 0.7880 | 0.6245   | 0.9104  |
| Decision Tree       | 0.8570   | 0.5307    | 0.7461 | 0.6202   | 0.8692  |
| Random Forest       | 0.8853   | 0.6058    | 0.7644 | 0.6759   | 0.9293  |

---

## 🏆 Best Model: Random Forest

Random Forest outperformed other models across:

* Highest Accuracy (88.53%)
* Highest F1-Score
* Highest ROC-AUC (0.9293)
* Better precision-recall balance

---

## 🔧 Model Optimization

Hyperparameter tuning was applied to improve performance.

### Optimized Random Forest Performance:

* Accuracy: **0.8882**
* Precision: **0.6172**
* Recall: **0.7513**
* F1-Score: **0.6777**
* ROC-AUC: **0.9306**

The optimized model achieved improved balance and slightly better predictive strength.

---

## 📊 Interpretation & Business Insight

### EDA Interpretation

* Conversion likelihood increases with deeper browsing engagement.
* Page value is a strong indicator of intent.
* Returning users are more valuable prospects.

### Model Interpretation

* Random Forest captures nonlinear interactions better than Logistic Regression.
* High ROC-AUC indicates strong discriminative ability.
* Precision-recall tradeoff was optimized to improve marketing decision-making.

### Optimization Insight

Threshold tuning improved precision without severely compromising recall, making it more suitable for targeted marketing campaigns.

---

## 💼 Business Recommendations

1. **Target High Page-Value Sessions**

   * Trigger personalized offers for high page-value users.

2. **Retarget Returning Visitors**

   * Allocate higher budget to returning user campaigns.

3. **Reduce Bounce Rate**

   * Improve landing page design.
   * Optimize user interface and loading speed.

4. **Dynamic Budget Allocation**

   * Use model predictions to allocate ad spend dynamically.

5. **Real-Time Purchase Probability Scoring**

   * Integrate model into production to score sessions in real time.

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

## 📁 Project Structure

```
├── Working_file(version_4).ipynb
├── README.md
├── dataset (external – Kaggle)
└── presentation slides
```

---

## 👥 Team Roles & Timeline

| Project Section             | Member(s) In-Charge | Deadline         |
| --------------------------- | ------------------- | ---------------- |
| Business Understanding      | All Team Members    | 20th – 22nd Feb  |
| Data Understanding          | All Team Members    | 20th – 22nd Feb  |
| EDA                         | Oliver / Ampadu     | 23rd – 26th Feb  |
| Data Preprocessing          | Damilola / Akinwale | 27th – 28th Feb  |
| Modelling                   | Feranmi / Afeez     | 1st – 2nd March  |
| Evaluation                  | Mahmud / Oluwafunmi | 2nd – 3rd March  |
| Interpretation              | Samuel / Stephen    | 3rd – 5th March  |
| Recommendation / Conclusion | Samuel              | 6th March        |
| README / Medium             | —                   | 7th March        |
| Presentation Slide          | —                   | 8th March        |
| Review                      | All Team Members    | 9th – 12th March |

---

## 🚀 How to Run the Project

### 1️⃣ Clone Repository

```bash
git clone <repository_link>
cd <project_folder>
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

Or manually install:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 3️⃣ Run Notebook

Open Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```
Working_file(version_4).ipynb
```

Run all cells sequentially.

---

## 🔮 Future Improvements

* Implement Gradient Boosting (XGBoost, LightGBM).
* Address class imbalance using SMOTE.
* Deploy as REST API using Flask/FastAPI.
* Build dashboard for marketing team.
* Implement real-time inference pipeline.

---

## 📌 Conclusion

This project demonstrates how data-driven modeling can significantly enhance marketing efficiency in e-commerce.

The optimized Random Forest model provides strong predictive power and practical business utility. By leveraging behavioral patterns and machine learning, businesses can:

* Increase conversion rates
* Reduce wasted ad spend
* Improve personalization
* Drive revenue growth

Team Dynamo successfully delivered a structured, end-to-end machine learning solution aligned with real-world business objectives.

---

**Tech Crush Data Science 2026 — Team Dynamo**
