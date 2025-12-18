# SyriaTel Customer Churn Prediction

## Project Overview
SyriaTel is experiencing revenue loss due to customer churn. Acquiring new customers is significantly more expensive than retaining existing ones, yet SyriaTel has not been leveraging its rich customer usage and service data to proactively predict churn.

This project applies **predictive analytics and machine learning** to identify customers at high risk of churning, uncover the key drivers of churn, and recommend data-driven retention strategies.

The analysis follows the full **data science lifecycle**, from business understanding to actionable recommendations.

---

## Business Problem
Customer churn directly impacts SyriaTel’s revenue and long-term sustainability. The goal is to build a **binary classification model** that predicts whether a customer is likely to churn, enabling early intervention and targeted retention efforts.

---

## Objectives
- Build a binary classification model to predict customer churn  
- Identify key factors strongly associated with churn  
- Compare multiple classification models and select the most effective one  
- Evaluate model generalization on unseen data  
- Support data-driven decision-making to reduce customer attrition  

---

## Data Source
- Dataset: **Telecom Customer Churn Dataset**
- Source: Kaggle  
  https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset

The dataset contains **3,333 customers** with **21 features**, including usage behavior, service plans, billing charges, and customer service interactions.

---

## Data Science Workflow

### 1. Data Understanding
- Inspected dataset structure, data types, and target distribution
- Verified absence of missing values and duplicates
- Identified numerical and categorical features
- Confirmed class imbalance in churn vs non-churn customers

---

### 2. Exploratory Data Analysis (EDA)
- Analyzed churn distribution
- Examined usage patterns and customer service interactions
- Identified early indicators of churn such as:
  - High customer service call frequency
  - Higher total charges
  - Subscription to international plans

---

### 3. Data Preparation & Feature Engineering
- Standardized column naming
- Engineered aggregate features:
  - `total_minutes`
  - `total_charges`
  - `total_calls`
- Dropped redundant and low-impact features
- Built a preprocessing pipeline with:
  - Standard scaling for numerical features
  - One-hot encoding for categorical variables

---

### 4. Modeling
The following models were trained and evaluated:

- **Logistic Regression** (baseline, class-balanced)
- **Decision Tree Classifier**
- **Random Forest Classifier**

Handling of class imbalance included:
- Class weighting
- SMOTE (Synthetic Minority Oversampling Technique)

---

### 5. Model Evaluation
Models were evaluated using:
- Recall (Churn)
- Precision (Churn)
- F1-score
- ROC-AUC
- Confusion matrices

**Key Insight:**  
Accuracy alone was not sufficient due to class imbalance; recall and ROC-AUC were prioritized.

---

### 6. Model Selection
The **Random Forest model** demonstrated the strongest overall performance:
- High ROC-AUC (~0.90)
- Strong precision for churn predictions
- Reliable generalization to unseen data

This model was selected as the final recommendation for deployment.

---

## Key Findings
- Customer churn is driven by **multiple interacting factors**, not a single variable
- High customer service call volume is a strong churn signal
- Customers on international plans exhibit higher churn risk
- Usage intensity and total charges act as early warning indicators
- Ensemble models outperform linear and rule-based approaches

---

## Recommendations
- Deploy the Random Forest churn prediction model for proactive retention
- Monitor churn drivers as early warning signals
- Integrate churn risk scores into CRM workflows
- Target retention resources toward high-risk, high-value customers
- Continuously retrain and monitor model performance

---

## Repository Structure
