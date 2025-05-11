# Streamlit Customer Churn Prediction 🚀

A machine learning project to predict customer churn using Scikit-learn and deploy it via Streamlit. This end-to-end pipeline includes data preprocessing, model training, and a Streamlit-powered interactive prediction interface.

---

## 🗂️ Project Structure

├── experiments.ipynb # Data exploration, preprocessing, training

├── prediction.ipynb # Predict churn using trained model

├── Churn_Modelling.csv # Source dataset

├── scaler.pk1 # Trained StandardScaler

├── label_encoder_gender.pk1 # LabelEncoder for Gender

├── onehot_encoder_geo.pk1 # OneHotEncoder for Geography'

├── trained_model.pkl # Final ML model

├── columns.pk1 # Feature column order used for scaling

├── app.py # Streamlit app (coming soon)

├── README.md # GitHub documentation

└── requirements.txt # Python dependencies


---

## 📊 Dataset Overview

- **Source**: Kaggle - [Churn Modelling Dataset](https://www.kaggle.com/datasets/shubhendra7/customer-churn-modelling)
- **Rows**: 10,000 customers
- **Target**: `Exited` — whether the customer churned (1) or stayed (0)

Key Features:
- `CreditScore`, `Geography`, `Gender`, `Age`, `Balance`, `Tenure`, `IsActiveMember`, `EstimatedSalary`, etc.

---

## ⚙️ Model Workflow

1. **Data Preprocessing**
   - Dropped non-informative columns (`RowNumber`, `CustomerId`, `Surname`)
   - Label encoded `Gender`
   - One-hot encoded `Geography`
   - Standardized numerical features

2. **Training**
   - Used models like Logistic Regression, Random Forest, etc.
   - Performance evaluated using accuracy, confusion matrix, and classification report
   - Final model and preprocessing pipeline saved with `pickle`

3. **Prediction**
   - New input is processed using saved encoders & scaler
   - Prediction made via trained model
   - Ready for deployment via Streamlit

---

## 💻 Streamlit App (Coming Soon)

A lightweight web interface to make live predictions.

```bash
# To run the app (after adding app.py)
streamlit run app.py
Input_data = {
    'CreditScore': 600,
    'Geography': 'Germany',
    'Gender': 'Male',
    'Age': 40,
    'Tenure': 3,
    'Balance': 60000,
    'NumOfProducts': 2,
    'HasCrCard': 1,
    'IsActiveMember': 1,
    'EstimatedSalary': 50000
}
📈 Model Performance
Metric	Score
Accuracy	~86%
Precision	High
Recall	Balanced
Confusion Matrix	Included in notebook

🛠️ Tech Stack
Python 3.12

Pandas, NumPy

Scikit-learn

Pickle

Jupyter Notebook

Streamlit

📌 To Do
 Model training & evaluation

 Save preprocessing pipeline

 Build app.py with Streamlit UI

 Add Streamlit deployment link

 Add Dockerfile (optional)
