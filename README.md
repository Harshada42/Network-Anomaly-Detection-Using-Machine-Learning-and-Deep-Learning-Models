# Network-Anomaly-Detection-Using-Machine-Learning-and-Deep-Learning-Models
This project focuses on detecting network anomalies and potential intrusions using a combination of Machine Learning (ML) and Deep Learning (DL) techniques.
By leveraging the NSL-KDD dataset, the system classifies normal and attack traffic to improve network security monitoring and intrusion prevention.

Objective
Build a reliable anomaly detection framework for network traffic.
Compare the performance of ML algorithms (Random Forest, Logistic Regression, Isolation Forest) and DL models (Autoencoder).
Develop a hybrid model that combines the strengths of supervised and unsupervised learning.
Provide explainability through feature importance and SHAP (SHapley Additive exPlanations) analysis.

About Dataset
Dataset Used: NSL-KDD Dataset
Features: 41 network traffic attributes
Target Classes: Normal vs. various attack categories (DoS, Probe, R2L, U2R)

Models Implemented
Logistic Regression : Simple baseline for linear separation of classes
Random Forest : Ensemble model for robust classification
Isolation Forest : Detects anomalies without labeled data
Autoencoder : Learns normal patterns to reconstruct and identify anomalies
Hybrid model (Isolation Forest + Logistic Regression : Combines unsupervised detection with supervised classification

Evaluation Metrics:
Accuracy
Precision
Recall
F1-Score
Confusion Matrix
ROC Curve
Feature Importance & SHAP Interpretability

