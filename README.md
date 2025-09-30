Fraud Detection Case Study
Problem Statement

A bank aims to build a real-time fraud detection system that identifies fraudulent transactions while minimizing false positives. The dataset is highly imbalanced with only ~5% fraud cases, making it challenging to achieve high recall.

Dataset

500 rows, 6 columns

Features: Amount, Location, MerchantCategory, CardHolderAge, Time

Target: IsFraud (imbalanced, 25–30 fraud cases)

Approach

Data Preprocessing

Handled missing values (median for numeric, most frequent for categorical)

Standardized numeric features, one-hot encoded categorical features

Dropped irrelevant identifiers (TransactionID)

Handling Imbalance

Applied SMOTE oversampling

Used class-weighted models

Model Development

Benchmarked multiple models: Logistic Regression, Random Forest, Gradient Boosting, SVM, KNN, Decision Tree

Hyperparameter tuning using GridSearchCV with ROC-AUC scoring

Evaluation

Metrics: Precision, Recall, ROC-AUC, Confusion Matrix

Threshold tuning with precision-recall curve to improve fraud detection recall

Results

Models achieved strong ROC-AUC but recall remained limited due to dataset imbalance

Adjusted thresholds improved fraud detection rates at the cost of more false positives

Random Forest and Gradient Boosting performed better than Logistic Regression on ROC-AUC

Conclusion

The project demonstrates a complete ML workflow for imbalanced fraud detection: preprocessing, resampling, model training, hyperparameter tuning, and threshold adjustment.
With more data and advanced feature engineering, performance could be further improved.

Future Work

Explore anomaly detection methods (Isolation Forest, One-Class SVM)

Use boosting methods such as XGBoost or LightGBM with class imbalance handling

Feature engineering: transaction frequency, ratios, time-based patterns

Cost-sensitive learning to directly optimize for recall
