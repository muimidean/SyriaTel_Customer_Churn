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

The dataset contains 3,333 customer records with 21 features, including customer usage patterns, service plans, billing information, customer service interactions, and a binary churn indicator.

---

## Data Preparation
Data inspection was performed initially to understand the structure and quality of the dataset. This included checking dataset dimensions, data types, missing values, duplicates, and the distribution of the target variable.

---

## Data Cleaning
The dataset required minimal cleaning as there were no missing values or duplicate records. Column names were standardized for consistency, and unnecessary or redundant variables were removed to improve model performance and interpretability.

---

## Feature Engineering
Feature engineering was performed to enhance predictive power by creating aggregate usage and billing features, including:
- Total minutes used across all call periods
- Total charges across all call periods
- Total number of calls

Redundant call-level variables were dropped after aggregation to reduce multicollinearity and simplify the feature space.

---

## Data Analysis
Exploratory data analysis (EDA) was conducted to understand customer behavior and its relationship with churn. This included:
- Univariate analysis of churn distribution
- Bivariate analysis between churn and customer service calls, usage, and charges
- Identification of behavioral patterns associated with high churn risk

---

## Modeling
Multiple machine learning models were trained and evaluated:
- Logistic Regression (baseline model with class balancing)
- Decision Tree Classifier
- Random Forest Classifier

To address class imbalance, techniques such as class weighting and SMOTE were applied. Model evaluation focused on recall, precision, F1-score, and ROC-AUC rather than accuracy alone.

---

## Findings
The analysis revealed several key insights:

- Customers with a high number of customer service calls are significantly more likely to churn.
- Higher usage intensity and higher total charges are strong early indicators of churn.
- Customers subscribed to international calling plans show a higher churn rate.
- Ensemble models outperform linear and rule-based models in capturing complex churn behavior.

Among all models tested, the **Random Forest classifier** delivered the strongest overall performance, achieving high ROC-AUC and strong precision when identifying churn-risk customers.

---

## Conclusion
This project demonstrates the value of predictive analytics in managing customer churn at SyriaTel. By leveraging historical customer data and applying machine learning techniques, the analysis successfully identifies customers at risk of leaving and uncovers the key drivers of churn.

The Random Forest model proved most effective, highlighting that churn behavior is influenced by multiple interacting factors rather than isolated variables. These findings confirm that SyriaTel can transition from reactive churn management to a proactive, predictive retention strategy.

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
For questions, or further discussion, please contact:

**Dean Muimi Mutie**  
Email: muimidean@gmail.com
