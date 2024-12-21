# PHASE 3 PROJECT.

# CUSTOMER CHURN PREDICTION FOR SYRIATEL: LEVERAGING PREDICTIVE ANALYTICS TO RETAIN CUSTOMERS.

# OVERVIEW.
Customer churn is a significant challenge in the telecommunications industry, where companies like SyriaTel face financial losses from customers who discontinue their services. This project aims to build a binary classification model that predicts whether a customer is likely to churn. The insights derived from this model will help SyriaTel proactively identify at-risk customers and implement targeted retention strategies, reducing churn rates and improving long-term revenue.

## BUSINESS UNDERSTANDING.
### Objective:
SyriaTel, a telecommunications company, is facing significant revenue losses due to customer churn. Retaining existing customers is more cost-effective than acquiring new ones. The goal of this project is to build a binary classification model to predict whether a customer will churn. This will enable SyriaTel to:
1.	Identify at-risk customers early.
2.	Design targeted retention strategies, such as personalized offers or discounts.
3.	Improve customer satisfaction and loyalty.
4.	Minimize revenue losses caused by customer attrition.
Key Business Questions:
1.	What are the main factors contributing to customer churn?
2.	How can these factors be used to design effective customer retention strategies?
3.	How accurately can the model predict customer churn, enabling timely interventions?


## DATA UNDERSTANDING.
### Dataset Overview:
The dataset, sourced from Kaggle, contains historical information on SyriaTel customers, covering demographics, usage patterns, account details, and support interactions. Key components include:
1.	Target Variable:
*	Churn: Binary indicator of whether a customer has churned (1) or not (0).
2.	Predictor Variables / Features:
* Customer Demographics: Attributes like age and gender.
* Service Usage Metrics: Data usage, call durations, and interaction frequency.
* Account Information: Contract type, tenure, billing details, and payment methods.
* Customer Support Interactions: Frequency and type of customer service engagements.
### Initial Observations:
* Potential class imbalance: There may be significantly fewer churn cases than non-churn cases.
* Mix of numerical and categorical features requiring preprocessing.
* Missing values and outliers may exist, requiring appropriate handling( exploration and potential preprocessing)
### Key Questions for Analysis:
* Are there strong correlations between customer behaviors (e.g., low tenure, high call drops) and churn?
* Do demographic or account-related features differentiate churners from non-churners?
* How influential are customer support interactions in churn prediction? 

## DATA PREPARATION.
### Objective:
To ensure the dataset is clean, transformed, and ready for modeling by addressing quality issues and engineering relevant features to ensure compatibility with the chosen models and improve prediction accuracy.
### 1.	Data Cleaning:
*	Handle missing numerical values with 0 imputation.
*	Fill missing categorical values with Unknown.
*	Remove duplicate records to avoid bias.
### 2.	Outlier Treatment:
*	Detect outliers using box plots or interquartile range (IQR).
*	Cap extreme outliers or adjust to reasonable limits as needed.
### 3.	Feature Transformation:
*	Standardize/Scale numerical features (e.g., tenure, monthly charges) for models sensitive to scale like logistic regression.
*	Encode categorical variables using one-hot encoding or label encoding.
### 4.	Feature Engineering:
*	Create derived features like "average call duration per day or average monthly spend or interaction frequency per week."
*	Transform non-linear relationships for compatibility with logistic regression.
### 5.	Class Imbalance Handling:
*	Apply SMOTE (Synthetic Minority Oversampling Technique) or adjust class weights for balanced model evaluation.
### 6.	Data Splitting:
*	Split the dataset into training (80%) and test (20%) subsets to evaluate model performance on unseen data.


## MODELING.
### Objective: Develop and compare machine learning models to predict customer churn, starting with a base model and progressing to more advanced techniques.
### 1.	Model Selection:
*	Base Model: Logistic Regression for simplicity and interpretability.
*	Advanced Models: 
*	Decision Tree for capturing non-linear relationships.
*	Random Forest for enhanced accuracy and robustness.
### 2.	Model Training:
o	Train each model on the training dataset.
o	Apply cross-validation to optimize hyperparameters and avoid overfitting.
### 3.	Hyperparameter Tuning:
*	Logistic Regression: Adjust regularization parameters (L1, L2 penalties).
*	Decision Tree: Optimize max depth, min samples per leaf, and splitting criteria.
*	Random Forest: Tune the number of trees and max features.
### 4.	Evaluation Metrics:
*	Primary Metric: Accuracy to measure overall performance.
*	Complementary Metrics: Precision, recall, F1-score, and ROC-AUC for a more comprehensive evaluation, especially in the case of class imbalance.

## EVALUATION.
### Objective: Assess model performance and ensure it meets business requirements.
### 1.	Evaluate Test Set Performance:
*	Measure accuracy, precision, recall, F1-score, and ROC-AUC on the test set.
*	Compare test performance with cross-validation results to check for overfitting or underfitting.
### 2.	Feature Importance Analysis:
*	For Logistic Regression, interpret feature coefficients to understand their impact on churn.
*	For Decision Tree and Random Forest, extract feature importance scores to identify key predictors.
### 3.	Model Comparison:
*	Compare Logistic Regression, Decision Tree, and Random Forest results to select the best-performing model based on evaluation metrics and business priorities.
### 4.	Business Impact Analysis:
*	Translate model predictions into actionable insights, such as identifying high-risk customers for retention campaigns.
*	Estimate potential cost savings or revenue improvements from reduced churn.
### 5.	Final Model Deployment:
*	Deploy the best-performing model in a production environment.
*	Set up monitoring to track model performance over time and retrain as necessary.



