# Credit Card Fraud Detection using Machine Learning

## Overview
This project focuses on detecting fraudulent credit card transactions using machine learning techniques. The dataset contains 10,000 synthetic transactions designed to simulate real-world credit card activity. The goal is to build a model capable of distinguishing between legitimate and fraudulent transactions based on transaction behavior and risk-related features.

Fraud detection is a critical problem in financial systems, and one of the main challenges is the **class imbalance** between normal and fraudulent transactions. This project explores different techniques to handle imbalanced data and evaluate model performance effectively.

---

## Dataset Description
The dataset includes **10,000 transactions** and **10 features** related to transaction behavior.

### Features
- **transaction_id** – Unique identifier for each transaction  
- **amount** – Transaction amount  
- **transaction_hour** – Hour of the transaction (0–23)  
- **merchant_category** – Category of the merchant  
- **foreign_transaction** – Indicates if the transaction is international (0/1)  
- **location_mismatch** – Whether the transaction location differs from billing location (0/1)  
- **device_trust_score** – Trust score of the device used (0–100)  
- **velocity_last_24h** – Number of transactions made in the last 24 hours  
- **cardholder_age** – Age of the cardholder  
- **is_fraud** – Target variable (0 = Normal, 1 = Fraud)

The dataset is **highly imbalanced**, where fraudulent transactions represent only a small portion of the data.

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Understanding dataset structure
- Statistical summary of features
- Visualization of class distribution
- Identifying class imbalance

### 2. Data Preprocessing
- Removing unnecessary columns
- Encoding categorical features
- Splitting data into training and testing sets

### 3. Handling Class Imbalance
Since fraud cases are rare, **SMOTE (Synthetic Minority Over-sampling Technique)** was applied to balance the training dataset and improve model learning.

### 4. Model Training
A **Random Forest Classifier** was trained on the balanced dataset to detect fraudulent transactions.

### 5. Model Evaluation
The model was evaluated using metrics suitable for imbalanced classification problems:

- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

---

## Results
The trained model successfully identifies fraudulent transactions while balancing the trade-off between **precision** and **recall**. In fraud detection systems, recall is often prioritized to ensure that as many fraudulent transactions as possible are detected, even if it leads to some false positives.

---

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)

---

## Key Insights
- Fraud detection datasets are typically **highly imbalanced**.
- Handling imbalance using techniques like **SMOTE** improves model performance.
- Evaluating models using **precision, recall, and ROC-AUC** provides better insight than accuracy alone.

---

## Conclusion
This project demonstrates how machine learning can be applied to detect fraudulent credit card transactions. It highlights the importance of handling class imbalance, performing proper data analysis, and selecting appropriate evaluation metrics for real-world financial applications.

---
