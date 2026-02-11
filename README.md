# Telco-customer-churn-EDA
This Colab notebook demonstrates an end-to-end machine learning workflow for Telecom Customer Churn prediction, including data cleaning, exploratory analysis, model training, evaluation, and churn prediction using the Telco dataset.
Project Overview
Customer churn is a critical problem for telecom companies, as retaining existing customers is more cost-effective than acquiring new ones.
This project builds an end-to-end machine learning pipeline to predict whether a customer will churn based on demographic, service usage, and billing information.

The repository follows MLOps best practices, including:
Data exploration & preprocessing
Model training and evaluation
Reproducible pipeline structure
Clear performance reporting

Dataset
Source: Telco Customer Churn dataset
Target variable: Churn
1 → Customer churned
0 → Customer retained

Data Exploration

Exploratory Data Analysis (EDA) is performed in notebooks/01_data_exploration.ipynb.

🧠Model Training
Train / Validation Split
The dataset is split using a stratified train-validation split
Split ratio:
80% Training
20% Validation

Stratification ensures that the churn/non-churn class distribution is preserved in both sets.

Steps include:
Feature scaling
Model initialization
Training on the training dataset
Saving the trained model artifact



Metrics Reported
The following metrics are used to evaluate the model:
Accuracy
Precision
Recall
F1-score
ROC-AUC Score

These metrics are chosen to properly evaluate churn prediction, where class imbalance is common.

Best Result

Best performing model achieved:
Accuracy: ~80%
ROC-AUC Score: ~0.84
F1-score (Churn class): Strong balance between precision and recall

This indicates that the model effectively distinguishes churned customers from retained ones.

🚀 How to Run the Project
Run on Google Colab
Open the notebook directly:
notebooks/01_data_exploration.ipynb

Future Improvements
Hyperparameter tuning
Experiment tracking with MLflow
CI/CD pipeline integration
Model deployment using Docker and FastAPI

End Results (Numerical Performance)

After training and evaluating the churn prediction model on the validation dataset, the following results were obtained:

Evaluation Metrics (Validation Set)
Metric	  Value
Accuracy	0.80 (80%)
Precision	0.79
Recall	  0.76
F1-Score	0.77
ROC-AUC 	0.84

Best Result Summary

The model achieves an accuracy of 80%, which shows strong prediction performance.
A ROC-AUC score of 0.84 indicates the model can distinguish between churned and non-churned customers.
The F1-score of 0.77 confirms balance between precision and recall, which is crucial for churn prediction where false negatives are not cost-effective.
