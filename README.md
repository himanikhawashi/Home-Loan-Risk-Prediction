# Home Loan Risk Prediction using Machine Learning

## Overview
This project focuses on predicting the risk associated with home loan applications using applicant demographic, financial, and credit-related data. The objective is to help financial institutions identify eligible applicants while minimizing loan default risk through data-driven decision-making.

## Dataset
The project involves multiple datasets related to loan applications and credit history, including:
- Application train data
- Bureau data
- Credit card balance data
- Other financial and credit-related records

These datasets were merged into a single analytical dataset for model development.

## Problem Statement
Loan defaults pose a significant financial risk to lending institutions. This project aims to build a reliable loan risk prediction model that classifies applicants based on their likelihood of loan approval and default risk.

## Approach
- Data cleaning and preprocessing
- Handling missing values and outliers
- Merging multiple datasets using appropriate join strategies
- Feature engineering and encoding of categorical variables
- Exploratory Data Analysis (EDA)
- Handling class imbalance using SMOTE
- Model training, comparison, and hyperparameter tuning
- Model evaluation using classification metrics

## Models Used
- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost Classifier

## Model Recommendation
**Recommended Model:** Tuned XGBoost Classifier

XGBoost was selected due to its superior performance on imbalanced data, ability to capture complex feature relationships, and improved accuracy and AUC after hyperparameter tuning.

## Challenges & Solutions

### Data Quality Challenges
- **Missing Values:** Imputed using mean (continuous variables) and mode (categorical variables). Rows with more than 60% missing data were removed.
- **Categorical Variables:** Converted into numerical format using one-hot encoding.
- **Class Imbalance:** Addressed using SMOTE to generate synthetic samples for the minority class (eligible loan customers).

### Multiple Dataset Integration
- Integrated several large datasets while ensuring no loss of critical information.
- Applied **inner joins** and **left joins** carefully to preserve relevant features and maintain data integrity.

### Model Selection & Performance
- Despite SMOTE, recall for the minority class remained challenging.
- Hyperparameter tuning using **GridSearchCV** was performed to reduce underfitting and overfitting.
- XGBoost demonstrated the best balance between performance and robustness.

## Exploratory Data Analysis (EDA)
- Used visualizations such as correlation heatmaps, box plots, and pair plots to analyze relationships and detect outliers.
- Performed statistical analysis (mean, median, mode, standard deviation) to understand feature distributions.
- Conducted categorical feature analysis using bar plots and chi-square tests.
- Evaluated feature importance to identify key drivers of loan eligibility.

## Model Interpretability
- Leveraged XGBoost feature importance to identify influential factors such as credit score and applicant income.
- Improved transparency to support explainable and trustworthy lending decisions.

## Model Deployment
- Serialized the trained model using **Pickle** for easy deployment and reuse.

## Conclusion
This project successfully addressed challenges related to data quality, multi-source data integration, class imbalance, and model interpretability. By applying SMOTE, extensive feature engineering, and a tuned XGBoost model, a robust home loan risk prediction system was developed to support accurate and data-driven loan approval decisions.


## Tools & Technologies
- Python
- Pandas, NumPy
- scikit-learn
- XGBoost
- imbalanced-learn (SMOTE)
- Matplotlib, Seaborn
