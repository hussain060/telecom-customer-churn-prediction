# Telecom Customer Churn Prediction Using Machine Learning

## Project Overview

This project focuses on predicting customer churn for a telecommunications company using machine learning.

The project includes data cleaning, exploratory data analysis (EDA), categorical feature encoding, feature scaling, train-test splitting, model training, model evaluation, and feature importance analysis.

Two machine learning classification models were implemented and compared:

Logistic Regression
Random Forest Classifier

The models were evaluated using Accuracy, Precision, Recall, F1-Score, and ROC-AUC.


## Dataset

The project uses the Telco Customer Churn dataset.

The original dataset contains:

- 7,043 customer records
- 21 columns
- Customer demographic information
- Services used by customers
- Contract details
- Billing information
- Churn status

During data cleaning, 11 records with missing `TotalCharges` values were removed, leaving 7,032 records for modelling.

### Target Variable

`Churn`

- `0` = Customer stayed
- `1` = Customer churned


## Exploratory Data Analysis

EDA was performed to understand the relationship between customer characteristics and churn.

The analysis included:

- Churn distribution
- Contract type vs churn
- Tenure vs churn
- Monthly charges vs churn
- Payment method vs churn
- Gender vs churn
- Senior citizen status vs churn
- Internet service vs churn
- Total charges vs churn

Some noticeable patterns in the dataset included higher churn rates among month-to-month contract customers, customers with shorter tenure, and customers with higher monthly charges.

These observations describe associations in the dataset and do not imply causation.

---

## Data Preprocessing

The following preprocessing steps were performed:

1. Converted `TotalCharges` from object to numeric format.
2. Handled missing values in `TotalCharges`.
3. Converted the target variable `Churn` from `Yes/No` to `1/0`.
4. Removed `customerID` because it is an identifier rather than a predictive feature.
5. Converted categorical features into numerical features using one-hot encoding.
6. Split the data into training and testing sets using an 80/20 split.
7. Applied feature scaling for Logistic Regression.

After preprocessing, the dataset contained 36 model features.

---

## Machine Learning Models

### Logistic Regression

Logistic Regression was used as a classification baseline for predicting whether a customer would churn.

### Random Forest

Random Forest was used as a tree-based classification model and was also used to analyze feature importance.

---

## Model Results

Both models were evaluated on the same test dataset.

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.8038 | 0.6476 | 0.5749 | 0.6091 | 0.8357 |
| Random Forest | 0.7875 | 0.6221 | 0.5107 | 0.5609 | 0.8171 |

In this experiment, Logistic Regression achieved higher scores across the reported evaluation metrics on the test dataset.

---

## Feature Importance

Random Forest feature importance was used to identify features that contributed most to the model's predictions.

Important features included:

- TotalCharges
- MonthlyCharges
- tenure
- InternetService
- PaymentMethod
- Contract
- PaperlessBilling
- OnlineSecurity
- Partner

Feature importance indicates how useful features were to the model's predictions. It does not establish that a feature directly causes customer churn.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Project Workflow

Data Collection  
↓  
Data Cleaning  
↓  
Exploratory Data Analysis  
↓  
Feature Preparation  
↓  
Categorical Encoding  
↓  
Train-Test Split  
↓  
Feature Scaling  
↓  
Model Training  
↓  
Model Evaluation  
↓  
Model Comparison  
↓  
Feature Importance Analysis

---

## Key Learning Outcomes

Through this project, I worked with:

- Real-world customer churn data
- Data cleaning and preprocessing
- Exploratory Data Analysis
- Categorical feature encoding
- Train-test splitting
- Feature scaling
- Classification algorithms
- Model evaluation metrics
- Model comparison
- Feature importance analysis

---

## Future Improvements

Possible future improvements include:

- Hyperparameter tuning
- Cross-validation
- Handling class imbalance using appropriate techniques
- Trying additional classification models
- Deploying the model as a web application

---

## Project Structure

```text
telecom-customer-churn-prediction/
│
├── Customer_Churn_Prediction.ipynb
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── README.md
├── .gitignore
└── screenshots/

## Author

Hussain Bohra
GitHub: https://github.com/hussain060