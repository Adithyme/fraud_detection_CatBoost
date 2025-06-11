Fraud Detection System for Online Transactions

📌 Project Objective

To develop an accurate and explainable machine learning model that detects fraudulent credit card transactions using anonymized features (V1 to V28) and standard variables like 'Amount' and 'Time'.

📊 Dataset

Source: Kaggle - Credit Card Fraud Detection dataset : Link:-https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Total records: 284,807

Fraud cases: 492 (highly imbalanced)

Features:

Time, Amount: Transaction details

V1 to V28: PCA-transformed features for confidentiality

Class: 0 (Non-Fraud), 1 (Fraud)

**🧹 Data Preprocessing**

Checked for null values: Found minimal nulls in the last few columns

Removed nulls using dropna() method

Scaled Amount and Time using StandardScaler

Applied SMOTE to handle class imbalance:

Before: [0: 49062, 1: 130]

After: [0: 49062, 1: 49062]

Retained all features since PCA-transformed data already encodes relevant information

Scaled non-PCA features (Amount, Time) to ensure consistency

**🧠 Machine Learning Models**

**1. XGBoost Classifier**

Achieved high precision and recall for both classes

ROC AUC Score: 0.9771

**2. CatBoost Classifier (Tuned)**

Strong recall and accuracy

ROC AUC Score: 0.9850

## 📈 Evaluation Metrics

| Metric       | XGBoost | CatBoost |
|--------------|---------|----------|
| Precision    | 0.88    | 0.74     |
| Recall       | 0.90    | 0.94     |
| F1-Score     | 0.89    | 0.83     |
| ROC AUC      | 0.9771  | 0.9850   |

> **Conclusion**: CatBoost is slightly better in recall (which is crucial for fraud detection), while XGBoost provides higher precision.


**🧠 Explainability**

Used SHAP for global and local interpretation

Key influential features: V14, V21, V1, V4, V6

**🚀 Future Enhancements**

Bayesian Hyperparameter Optimization

Model deployment using Streamlit or Gradio

Add LIME for local explanation

Use real-time data stream simulation

**🧾 Requirements**

pandas
numpy
scikit-learn
xgboost
catboost
shap
matplotlib
seaborn
imbalanced-learn

**🏁 How to Run**

Clone this repository

Open the notebook in Google Colab or Jupyter

Run all cells sequentially

Modify parameters or try other models as needed

**🙌 Acknowledgements**

Credit Card Fraud Detection dataset by Worldline and ULB (on Kaggle)

**📬 Contact**

Adithya CH: adithyach36@gmail.com LinkedIn: [http://www.linkedin.com/in/adithya-c-h-589345291]

"Fraud detection is not just about catching the fraudsters — it's about building trust and transparency in the system."
