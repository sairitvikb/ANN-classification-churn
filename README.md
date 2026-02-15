# ANN-Classification-Churn

Customer churn prediction using an **Artificial Neural Network (ANN)** trained on bank-customer data, with a **Streamlit web app** for interactive predictions.

---
## ✨ What this project does
- Trains an ANN model to predict whether a customer will **churn (exit)** or **stay**
- Saves the trained model (`model.h5`) plus preprocessing artifacts (encoders + scaler)
- Provides a Streamlit UI (`app.py`) where you enter customer details and get:
  - **Churn probability**
  - Final label: **Likely to churn / Not likely to churn**

---
## 🧠 Model & Features
The app uses these input features:
- CreditScore
- Geography (One-Hot Encoded)
- Gender (Label Encoded)
- Age
- Tenure
- Balance
- NumOfProducts
- HasCrCard
- IsActiveMember
- EstimatedSalary

Prediction output:
- `Churn Probability` (float)
- Threshold: `> 0.5` → likely churn

---
## 📁 Project Structure
```bash
ANN-Classification-Churn/
│── app.py                         # Streamlit app
│── Churn_Modelling.csv             # Dataset
│── experiments.ipynb               # Training/experiments notebook
│── prediction.ipynb                # Testing predictions notebook
│── model.h5                        # Trained ANN model
│── label_encoder_gender.pk1        # LabelEncoder for gender
│── one_hot_encoder_geo.pk1         # OneHotEncoder for geography
│── scaler.pk1                      # StandardScaler for numeric features
│── requirements.txt                # Dependencies
│── runtime.txt                     # Runtime (useful for deployment)
└── README.md
