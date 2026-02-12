SyriaTel Customer Churn Prediction
## Business Understanding
Stakeholder: SyriaTel Customer Retention Team

The Problem: SyriaTel faces an annual customer churn rate of approximately 15%, resulting in significant revenue loss. Since acquiring new customers is more expensive than retaining existing ones, the goal is to predict which customers are likely to leave.

Objective: Develop a classification model to identify high-risk customers, allowing the Retention Team to intervene proactively and mitigate revenue loss.

## Data Overview
The dataset includes customer usage patterns, service calls, and plan details.

Target Variable: churn (True/False)

Key Features: Customer service calls, total day minutes, and international plan status.

## Methodology
This project followed an iterative modeling process:

Preprocessing: Handled categorical encoding for plans and scaled numerical features.

Feature Engineering: Combined individual charges into a total_charge feature to capture overall customer spending.

Modeling: Evaluated Logistic Regression, Decision Trees, and Random Forest models.

Optimization: Used GridSearchCV to tune hyperparameters, focusing on Recall to ensure we catch as many churners as possible.

## Evaluation
Our final model (Random Forest) achieved a Recall of 75%+, meaning we correctly identify the vast majority of customers who are actually planning to leave.

Top Predictor: Customer Service Calls was the strongest indicator of churn. Customers who call support more than 3 times are significantly more likely to leave.

## Business Recommendations
Service Recovery: Implement a mandatory follow-up for any customer reaching 3+ service calls.

Loyalty Incentives: Offer targeted discounts to high-spending customers (Top 10% of total_charge) who are flagged by the model.

Plan Review: Investigate why users on the International Plan have a higher churn rate—consider adjusting pricing or perks.