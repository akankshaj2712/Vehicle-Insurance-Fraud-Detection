# Vehicle-Insurance-Fraud-Detection

🔍 Final Observations & Insights — Vehicle Insurance Fraud Detection

 Team Members: Akanksha Jondhale, Viswanath Iruku, Inchara Jayaram Anuradha
 
 Dataset: fraud_oracle.csv
 
 Approach: Supervised Classification using Logistic Regression, Random Forest, Neural Networks with Autoencoders


📌 Problem Overview:

Vehicle insurance fraud, including staged accidents and exaggerated injury claims, is a growing concern impacting insurance companies and policyholders alike. Our goal was to build predictive models that can distinguish between genuine and fraudulent claims using historical data and help insurers take proactive action.

🔧 Preprocessing & Feature Engineering:

•	Handled over 30 categorical and numerical features with significant class imbalance in the target variable FraudFound_P.

•	Applied label encoding, one-hot encoding, and scaling to prepare features for modeling.

•	Created new features like Claim Complexity to capture hidden patterns (e.g., RepNumber / PolicyNumber).

•	Removed multicollinear features using correlation matrix analysis (threshold > 0.9).

•	Balanced the dataset using random oversampling to improve fraud detection performance.


🔍 Key Insights from EDA:

•	Fraud is more frequent in urban areas, with older vehicles, and frequent address changes.

•	Claims without police reports or witnesses are more likely to be fraudulent.

•	Fraudulent claims often involve younger policyholders and lower vehicle value brackets.

•	Heatmaps and clustering plots revealed temporal and regional fraud patterns useful for further operational strategies.


📊 Modeling & Evaluation Results:
We evaluated three key models with resampled data:

✅ Random Forest

•	Accuracy: 96%

•	Precision (Fraud): 98

•	Recall (Fraud): 95%

•	F1 Score: 96%

Observation: This model provided the best overall performance with strong balance between Type I and Type II errors.

✅ Logistic Regression

•	Accuracy: 96%

•	Precision (Fraud): 98%

•	Recall (Fraud): 94%

Observation: Similar to Random Forest, but slightly higher false negative rate. Still a robust and interpretable model.

⚠️ Neural Network (Autoencoder for Anomaly Detection)

•	Accuracy: 90%

•	Precision (Fraud): 7%

•	Recall (Fraud): 6%

Observation: Poor performance in detecting fraud due to subtle anomaly signatures and severe class imbalance. Better suited for unsupervised anomaly cases.

✅ Conclusion:

Our project demonstrates that tree-based ensemble methods like Random Forests are highly effective for fraud detection when paired with thoughtful preprocessing and feature engineering. Balancing the dataset was critical for performance, and interpretability of models like logistic regression can support actionable decisions in real-world settings.
We recommend that insurers integrate such models into their claim pipeline to flag high-risk cases for further manual review, improving efficiency and reducing fraud-related losses.
