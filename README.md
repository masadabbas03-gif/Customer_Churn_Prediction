

📞 Customer Churn Prediction using Machine Learning

This project focuses on predicting customer churn for a subscription-based service (like telecom, banking, or SaaS). Using historical customer data, multiple machine learning models identify customers who are likely to leave, enabling businesses to take proactive retention measures.

📌 Project Overview

Customer churn is a critical business metric. This project aims to build classification models to predict churn based on customer demographics, account information, and usage patterns.

📊 Dataset

· Source: CustomerChurn.csv (Telco Customer Churn Dataset)
· Instances: 7,043 customers
· Features: 20 columns including:
  · Demographics: gender, SeniorCitizen, Partner, Dependents
  · Services: PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies
  · Account Info: tenure, Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges
· Target Variable: Churn (Yes/No)

🛠️ Technologies Used

· Python 3.x
· Pandas, NumPy
· Matplotlib, Seaborn
· Scikit-learn
· Imbalanced-learn (SMOTE)
· XGBoost
· Pickle

🧠 Machine Learning Workflow

1. Data Loading & Exploration

· Loaded the dataset using Pandas
· Checked shape, data types, and missing values
· Dropped customerID column

2. Data Preprocessing

· Handled missing values in TotalCharges column
· Exploratory Data Analysis (EDA) with histograms, box plots, correlation heatmap, and count plots
· Label Encoding for categorical variables using LabelEncoder
· Saved encoders as encoders.pkl

3. Handling Class Imbalance

· Identified class imbalance (Churn: 1869, No Churn: 5174)
· Applied SMOTE to balance the classes

4. Model Building

· Split data into training and testing sets (80-20 split)
· Trained three models with default hyperparameters:
  · Decision Tree Classifier
  · Random Forest Classifier
  · XGBoost Classifier

5. Model Evaluation

· Used 5-fold cross-validation on SMOTE data
· Random Forest performed best with 84% accuracy
· Final evaluation on test data:

Metric Value
Accuracy 78%
Precision (Churn) 0.58
Recall (Churn) 0.59
F1-Score (Churn) 0.58

6. Model Saving

· Saved the trained model as customer_churn_model.pkl
· Saved encoders as encoders.pkl

7. Prediction System

· Built a prediction system using saved model and encoders
· Sample prediction:
  · Input: Customer with low tenure, month-to-month contract, electronic check
  · Output: No churn (78% probability)

📁 Project Structure

```
Customer_Churn_Prediction/
│
├── NoteBook/
│   └── Customer_Churn_Prediction.ipynb   # Main notebook
├── CustomerChurn.csv                       # Dataset
├── encoders.pkl                            # Saved label encoders
├── customer_churn_model.pkl                 # Trained model
├── README.md                                # Project documentation
└── requirements.txt                         # Dependencies

🚀 How to Run

1. Clone the repository
2. Install dependencies: pip install -r requirements.txt
3. Run the Jupyter Notebook

🔮 Future Work

· Hyperparameter tuning using GridSearchCV
· Try CatBoost or LightGBM
· Deploy as Streamlit web app
· SHAP/LIME for model interpretability

🤝 Connect

Gmail: masadabbas03@gmail.com
