# Credit Card Fraud Detection System
Credit card fraud detection using Logistic Regression with EDA and class imbalance analysis

## Overview
This project focuses on detecting fraudulent credit card transactions using machine learning.  
I used **Logistic Regression**, a simple and interpretable classification algorithm, to identify whether a transaction is fraudulent or not.

A key challenge in this project is **class imbalance**, since fraud cases are very rare compared to normal transactions. To address this, I experimented with both unbalanced and balanced data.

---

## Dataset
- Get the dataset I used in this system from:
**Source:** [Kaggle Credit Card Fraud Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- The dataset is anonymized for privacy.
- Features **V1–V28** are PCA-transformed and do not have direct real-world meaning.
- I used only **Time** and **Amount** as input features because they are interpretable.
- **Target variable:**  
  - `Class = 0` → Not Fraud  
  - `Class = 1` → Fraud  

---

## Notebooks in This Repository
This repository contains **two notebooks**:

### 1. Fraud Detection System (Main Notebook)
- Exploratory Data Analysis (EDA)
- Model training on unbalanced data
- Model evaluation
- Final deployed model
- Gradio-based user interface for predictions

### 2. Balanced Data Experiment
- Analysis of class imbalance
- Data balancing using **SMOTE**
- Training Logistic Regression on balanced data
- Performance comparison with the unbalanced model
- Shows how balancing affects accuracy and fraud detection
- SMOTE (Synthetic Minority Oversampling Technique) was used to generate synthetic fraud samples to balance the training data.

---

## Exploratory Data Analysis
- The dataset is **highly imbalanced**, with fraud making up less than 1% of transactions.
- Visualizations used:
  - Bar chart for class distribution
  - Scatter plot (Time vs Amount)
  - Correlation heatmap
- These graphs help understand why fraud detection is a challenging problem.

The dataset contains 17,836 non-fraud transactions and only 81 fraud cases, making fraud less than 0.5% of all transactions.

---

## Model Development
- **Algorithm:** Logistic Regression
- **Train-test split:** Stratified split to preserve class ratios
- Two approaches tested:
  - Training on unbalanced data
  - Training on balanced data using **SMOTE**

This allowed a direct comparison between both approaches.

---

## Results
- The **unbalanced model** achieved very high overall accuracy but struggled with detecting fraud.
- The **balanced model** improved fraud detection but reduced overall accuracy.
- For this project, the unbalanced model was selected as the final system, while the balanced model is included as an experiment to demonstrate understanding of class imbalance.

---

## Deployment
A simple **Gradio-based GUI** was built to simulate real-time fraud detection.  
Users can input transaction details and instantly see whether the transaction is predicted as fraudulent or not.
The interface accepts Time and Amount as inputs and outputs a fraud prediction.

You can try the interactive demo yourself, see **DEMO.md** in this repository for the link.

---

## Technologies Used
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- Imbalanced-learn (SMOTE)  
- Gradio  

---

## Author

Amina, Information Technology university 
