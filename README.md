# Network Anomaly Detection Using Machine Learning and Deep Learning Models

An intrusion detection and network anomaly detection project using the **NSL-KDD dataset**. This project applies **Machine Learning** and **Deep Learning** techniques to classify normal and malicious network traffic and compare the performance of different detection models.

The goal of this project is to identify abnormal network behavior that may indicate cyber threats such as DoS, Probe, R2L, and U2R attacks.

---

## Project Overview

Network anomaly detection is an important part of cybersecurity monitoring. Traditional security systems may fail to detect unknown or evolving attacks, so anomaly-based intrusion detection systems use data-driven methods to identify suspicious network behavior.

This project builds and compares multiple ML/DL models for intrusion detection using the NSL-KDD dataset. The models are trained on network traffic features and evaluated using accuracy, precision, recall, F1-score, confusion matrix, ROC curve, feature importance, and SHAP explainability.

---

## Objectives

The main objectives of this project are:

- Build an anomaly-based intrusion detection system.
- Classify network traffic as normal or malicious.
- Detect different attack categories such as DoS, Probe, R2L, and U2R.
- Compare supervised, unsupervised, and deep learning models.
- Evaluate model performance using standard classification metrics.
- Improve interpretability using feature importance and SHAP analysis.
- Identify which model performs best for network anomaly detection.

---

## Dataset

The project uses the **NSL-KDD dataset**, a benchmark dataset widely used for intrusion detection research.

### Dataset Files

```text
kdd_train.csv
kdd_test.csv
```

### Dataset Details

- Dataset: NSL-KDD
- Total Features: 41 network traffic attributes
- Target: Normal and attack traffic
- Attack Categories:
  - DoS
  - Probe
  - R2L
  - U2R

The dataset contains different network connection features such as protocol type, service, flag, duration, source bytes, destination bytes, failed login attempts, connection count, and other traffic-based attributes.

---

## Tech Stack

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib
- Seaborn
- SHAP
- Joblib
- Machine Learning
- Deep Learning

---

## Models Implemented

The following models were implemented and compared:

### 1. Logistic Regression

Logistic Regression was used as a baseline supervised learning model. It helps evaluate how well a simple linear classifier can separate normal and attack traffic.

### 2. Random Forest

Random Forest was used as an ensemble-based supervised model. It performs well on structured tabular datasets and helps identify important network traffic features.

### 3. Isolation Forest

Isolation Forest was used as an unsupervised anomaly detection model. It identifies unusual traffic patterns without relying completely on labeled attack data.

### 4. Autoencoder

Autoencoder was used as a deep learning model. It learns compressed representations of normal network behavior and detects anomalies based on reconstruction error.

### 5. Hybrid Model

A hybrid approach was developed by combining **Isolation Forest** and **Logistic Regression**. This combines unsupervised anomaly detection with supervised classification to improve detection capability.

---

## Project Workflow

```text
NSL-KDD Dataset
        |
        v
Data Loading
        |
        v
Data Preprocessing
        |
        v
Feature Encoding and Scaling
        |
        v
Model Training
        |
        v
Model Evaluation
        |
        v
Model Comparison
        |
        v
Feature Importance and SHAP Analysis
```

---

## Methodology

### 1. Data Loading

The NSL-KDD training and testing datasets were loaded using Pandas.

```text
kdd_train.csv
kdd_test.csv
```

---

### 2. Data Preprocessing

Data preprocessing included:

- Checking dataset shape and structure
- Handling categorical features
- Encoding target labels
- Separating input features and target column
- Applying feature scaling where required
- Preparing training and testing sets

---

### 3. Feature Engineering

The dataset contains both numerical and categorical features. Categorical values were encoded so they could be used by machine learning models.

Important feature groups include:

- Basic connection features
- Content-based features
- Traffic-based features
- Host-based features

---

### 4. Model Training

Multiple models were trained to compare their ability to detect anomalies and classify attack traffic.

Models trained:

```text
Logistic Regression
Random Forest
Isolation Forest
Autoencoder
Hybrid Model
```

---

### 5. Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC Curve
- Feature Importance
- SHAP Explainability

---

## Evaluation Metrics

| Metric | Meaning |
|---|---|
| Accuracy | Overall percentage of correct predictions |
| Precision | How many predicted attacks were actually attacks |
| Recall | How many actual attacks were correctly detected |
| F1-score | Balance between precision and recall |
| Confusion Matrix | Shows true positives, true negatives, false positives, and false negatives |
| ROC Curve | Shows classification performance across different thresholds |

---

## Key Result

Among the implemented models, **Random Forest achieved the best performance**, with approximately **93% accuracy**.

Random Forest performed well because:

- It handles high-dimensional tabular data effectively.
- It captures non-linear relationships between features.
- It is robust against noise.
- It provides feature importance for explainability.
- It performs better than simpler linear models on complex attack patterns.

---

## Feature Importance

Feature importance analysis was performed to understand which network traffic attributes contributed most to anomaly detection.

This helps explain why the model classified certain traffic as normal or malicious.

Feature importance is useful in cybersecurity because it helps analysts understand:

- Which network behaviors are suspicious
- Which features influence attack detection
- Which traffic patterns are linked to anomalies
- How the model makes decisions

---

## SHAP Explainability

SHAP analysis was used to improve model interpretability.

SHAP helps explain:

- How each feature contributes to a prediction
- Which features increase attack probability
- Which features reduce attack probability
- How the model behaves on individual predictions

This makes the intrusion detection system more explainable and useful for security analysis.

---

## Repository Structure

```text
Network-Anomaly-Detection-Using-Machine-Learning-and-Deep-Learning-Models/
│
├── README.md
├── MTech Project.ipynb
├── Project.ipynb
├── kdd_train.csv
├── kdd_test.csv
├── model_iforest.joblib
└── model_lr.joblib
```

---

## How to Run the Project

### Prerequisites

Install Python 3.8 or above.

Install the required libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn tensorflow keras shap joblib
```

---

### Steps to Run

1. Clone the repository:

```bash
git clone https://github.com/Harshada42/Network-Anomaly-Detection-Using-Machine-Learning-and-Deep-Learning-Models.git
```

2. Go to the project folder:

```bash
cd Network-Anomaly-Detection-Using-Machine-Learning-and-Deep-Learning-Models
```

3. Open Jupyter Notebook:

```bash
jupyter notebook
```

4. Run the notebook:

```text
MTech Project.ipynb
```

or

```text
Project.ipynb
```

5. Execute the cells step by step to preprocess data, train models, evaluate results, and generate visualizations.

---

## Saved Models

The repository includes saved model files:

```text
model_iforest.joblib
model_lr.joblib
```

These files can be loaded using Joblib for future prediction or testing.

Example:

```python
import joblib

model = joblib.load("model_lr.joblib")
```

---

## Cybersecurity Relevance

This project is relevant to cybersecurity because it demonstrates how AI/ML can support intrusion detection and threat monitoring.

It can help in:

- Detecting abnormal traffic behavior
- Identifying malicious network connections
- Supporting SOC and security monitoring workflows
- Reducing manual analysis of large network logs
- Improving attack classification using machine learning
- Explaining detection decisions using feature importance and SHAP


## Future Enhancements

Possible improvements for this project:

- Add a Streamlit web application for real-time prediction
- Add dashboard visualizations for attack categories
- Add MITRE ATT&CK mapping for detected attack types
- Improve hybrid model performance
- Add real-time packet/log ingestion
- Deploy the model as an API using Flask or FastAPI
- Add Docker support
- Add automated model retraining
- Add alert severity levels such as Low, Medium, and High
- Compare results with newer intrusion detection datasets


