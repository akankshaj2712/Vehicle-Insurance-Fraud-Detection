# 🕵️ Fraud Detection Analysis Report
🔍 **Objective**

This project focuses on detecting fraudulent vehicle insurance claims using machine learning. Insurance fraud leads to billions in losses annually—early detection helps mitigate these risks.

**Goals:**

Identify key factors influencing fraud.

Develop predictive models to classify claims as fraudulent or genuine.

📊 **Dataset Overview**

The dataset includes:

Demographics (e.g., Age, Sex, MaritalStatus)

Vehicle & Policy Info (VehicleCategory, VehiclePrice, PolicyAnnualPremium)

Claim Characteristics (ClaimAmount, AccidentArea, DayOfWeek, Month)

Target Variable: FraudFound_P (1 = Fraudulent, 0 = Genuine)

🧪 **Methodology**

**Exploratory Data Analysis (EDA):**

Visualizations and statistical summaries to understand feature distributions and class imbalance.

**Data Preprocessing:**

Handled missing values and categorical encoding

Applied feature scaling using StandardScaler

Used SMOTE to balance class distribution

**Model Comparison:**

Logistic Regression

Random Forest

XGBoost

Neural Network (Autoencoder)

Voting Classifier (XGBoost + Logistic Regression)

✅ **Results**

| Model                   | Recall (Fraud) | Accuracy | F1-Score |
| ----------------------- | -------------- | -------- | -------- |
| Logistic Regression     | 81%            | 54%      | 18%      |
| Random Forest           | 89%            | 57%      | 19%      |
| XGBoost                 | 90%            | 59%      | 20%      |
| **Neural Network (AE)** | **95%**        | 55%      | **20%**  |
| Voting Classifier       | 92%            | 56%      | 19%      |


Neural Network with Autoencoder was selected as the final model due to 95% recall, crucial for minimizing false negatives in fraud detection.

📈 **Key Takeaways**

Recall was prioritized as the main evaluation metric due to the high cost of false negatives.

Feature engineering and SMOTE significantly improved minority class detection.

Ensemble and deep learning models provided the best balance between recall and interpretability.
