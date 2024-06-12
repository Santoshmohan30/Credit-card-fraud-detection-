Report
Credit Card Fraud Detection 
1. Introduction
Credit card fraud is a significant issue in the financial industry, leading to substantial monetary losses. This project aims to build a predictive model using logistic regression to identify fraudulent transactions based on a dataset of credit card transactions.

2. Data Description
The dataset contains transactions made by credit cards in September 2013 by European cardholders. It presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, with the positive class (frauds) accounting for 0.172% of all transactions.

3. Data Preprocessing
Loading the dataset: The dataset was loaded into a Pandas DataFrame.
Inspecting the dataset: The first and last five rows were displayed to understand the structure.
Dataset information: The info() method was used to get an overview of the dataset, including data types and non-null counts.
Missing values: We checked for missing values in each column, but found none.
Class distribution: The distribution of the 'Class' column was inspected, revealing a highly imbalanced dataset with significantly more normal transactions than fraudulent ones.
4. Data Analysis
Separating the data: The data was split into two subsets: legit (normal transactions) and fraud (fraudulent transactions).
Statistical analysis: Descriptive statistics were computed for the 'Amount' column in both subsets.
Comparison of transactions: The mean values of all features were compared between the normal and fraudulent transactions.
5. Under-Sampling
To address the class imbalance, under-sampling was performed:

A subset of the normal transactions (legit_sample) was randomly selected to match the number of fraudulent transactions (492).
The under-sampled normal transactions were concatenated with the fraudulent transactions to form a new dataset.
6. Model Building
Feature and target separation: The features (X) and target (Y) were separated.
Data splitting: The dataset was split into training and testing sets using an 80-20 split with stratified sampling to maintain the class distribution.
Model training: A logistic regression model was trained on the training data.
7. Model Evaluation
Accuracy on training data: The model achieved an accuracy of X% on the training data.
Accuracy on test data: The model achieved an accuracy of Y% on the test data.
8. Conclusion
The logistic regression model showed promising results in detecting fraudulent transactions. However, given the imbalanced nature of the dataset, further techniques such as over-sampling, SMOTE, or using more complex models (e.g., Random Forest, XGBoost) could be explored to potentially improve performance.
