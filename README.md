![Sales-Customer-Support-The-Process](https://github.com/user-attachments/assets/369bf630-f445-4c16-b0c1-aa402d48838d)

# SyriaTel Customer Churn Prediction Project

## Overview

SyriaTel is experiencing revenue loss due to customer churn, where existing customers discontinue using the company’s services. Since acquiring new customers is more costly than retaining current ones, this project applies data science and machine learning techniques to predict customer churn and identify the key factors driving customer attrition. The insights generated aim to support proactive, data-driven customer retention strategies.

---

## Objectives

* Build a binary classification model to predict whether a SyriaTel customer is likely to churn.
* Identify key usage, billing, and service-related factors strongly associated with churn.
* Compare multiple classification models to determine the most effective approach.
* Evaluate model performance using appropriate metrics for imbalanced data.
* Support data-driven decision-making to reduce customer loss and protect revenue.

---

## Data Understanding

The dataset used in this analysis was sourced from Kaggle:
[Telecom Customer Churn Dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset)

The dataset contains **3,333 customer records** with **21 features**, including customer usage patterns, service plans, billing information, customer service interactions, and a binary churn indicator.

---

## Data Preparation

Initial data inspection was conducted to understand the dataset structure and quality. This included:

* Reviewing dataset dimensions and data types
* Checking for missing values and duplicates
* Examining the distribution of the target variable (churn)

---

## Data Cleaning

The dataset required minimal cleaning:

* No missing values or duplicate records were identified
* Column names were standardized for consistency
* Redundant or low-importance variables were removed to improve model performance and interpretability

---

## Feature Engineering

Feature engineering was performed to enhance predictive power by creating aggregate usage and billing features, including:

* **Total minutes** used across all call periods
* **Total charges** across all call periods
* **Total number of calls**

After aggregation, redundant call-period variables were dropped to reduce multicollinearity and simplify the feature space.

---

## Exploratory Data Analysis (EDA)

Exploratory data analysis was conducted to better understand customer behavior and its relationship with churn. Key analyses included:

* Univariate analysis of churn distribution
* Bivariate analysis between churn and customer service calls, usage, and charges
* Identification of behavioral patterns associated with high churn risk

---

## Modeling

Multiple machine learning models were trained and evaluated:

* **Logistic Regression** (baseline model with class balancing)
* **Decision Tree Classifier**
* **Tuned Decision Tree Classifier** (using hyperparameter tuning)
* **Random Forest Classifier**

To address class imbalance, techniques such as **class weighting** and **SMOTE** were applied. Model evaluation focused on **recall**, **precision**, **F1-score**, and **ROC-AUC**, rather than accuracy alone.

---

## Model Comparison and Selection

The models were compared using test set performance, with accuracy used as a high-level comparison metric.

| Model               | Accuracy (%) |
| ------------------- | ------------ |
| Logistic Regression | 76.61        |
| Decision Tree       | 89.36        |
| Tuned Decision Tree | 93.25        |
| Random Forest       | **94.00**    |

The results show a clear performance improvement as model complexity increases. Logistic Regression provided a useful baseline but struggled to capture non-linear relationships. The Decision Tree significantly improved performance, while hyperparameter tuning further enhanced its accuracy.

The **Random Forest model** achieved the highest accuracy and demonstrated superior generalization, confirming that ensemble methods are better suited for capturing complex churn behavior.

---

## Key Findings

* Customers with a high number of **customer service calls** are significantly more likely to churn.
* **Higher usage intensity** and **higher total charges** are strong early indicators of churn.
* Customers subscribed to **international calling plans** show a higher churn rate.
* **Ensemble models** outperform linear and single-tree models when modeling customer churn.

---

## Conclusion

This project demonstrates the value of predictive analytics in managing customer churn at SyriaTel. By leveraging historical customer data and applying machine learning techniques, the analysis successfully identifies customers at risk of leaving and uncovers the key drivers of churn.

The Random Forest model proved most effective, highlighting that churn behavior is influenced by multiple interacting factors rather than isolated variables. These findings support a shift from reactive churn management to a proactive, predictive retention strategy.

---

## Recommendations

* **Adopt Predictive Churn Modeling:** Deploy the Random Forest model to identify high-risk customers early.
* **Monitor Early Warning Signals:** Track customer service call frequency, usage intensity, and total charges as churn indicators.
* **Use Appropriate Evaluation Metrics:** Prioritize recall and ROC-AUC when assessing churn models in imbalanced datasets.
* **Integrate Insights into Business Operations:** Embed churn risk scores into CRM and customer retention workflows.
* **Continuously Improve Models:** Retrain and validate models regularly as customer behavior and service offerings evolve.

---

## Next Steps

* Expand the dataset with newer customer records and additional variables such as promotions or contract types.
* Explore advanced techniques such as gradient boosting and cost-sensitive learning.
* Develop a real-time churn prediction dashboard for business users.

---

## For More Information

For questions or further discussion, please contact:

**Dean Muimi Mutie**
Email: [muimidean@gmail.com](mailto:muimidean@gmail.com)
