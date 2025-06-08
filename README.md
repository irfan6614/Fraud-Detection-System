Fraud Detection System
About the Project
This project helps detect **fraudulent credit card transactions** using machine learning.  
We use a **Random Forest** model and handle imbalanced data with **SMOTE**.  
You can test the model using a **simple command-line interface (CLI)**.
fraud-detection/
├── creditcard.csv # The dataset (from Kaggle)
├── train_model.py # Code to train and save the model
├── fraud_model.pkl # The saved trained model
├── model_columns.pkl # List of input features used in the model
├── fraud_cli.py # Script to test new transactions using CLI
└── README.md # This file

---
Requirements:

Install the necessary Python libraries by running:

```bash
pip install pandas scikit-learn imbalanced-learn joblib
Dataset Used:
Download the dataset from Kaggle and place the creditcard.csv file in the project folder.
How to Run the Project
1.	Train the Model
        python train_model.py
This will:
•	Load the dataset
•	Balance the classes using SMOTE
•	Train a Random Forest model
•	Save the model and feature list
2.	Test with CLI (Command Line)
        python fraud_cli.py
The program will ask you to enter 30 values (features) like V1, V2, ..., Amount. After you enter all the values, it will tell you whether the transaction is Fraudulent or Not Fraudulent.
---- Fraud Detection System ----
Please enter values for 30 features:
V1: -1.23
V2: 2.45
...
Amount: 149.62

Prediction: Not Fraudulent
Model Info:
•  Model: Random Forest Classifier
•  Imbalanced data is handled using SMOTE
•  The model is trained using 80% of the data, tested on 20%
Sample Model Performance:
Precision: 0.93
Recall:    0.79
F1-score:  0.85
Key Points
•	Most transactions are not fraud, so we use SMOTE to balance the data.
•	The model works well and catches most fraud cases.
•	Simple and easy to test via the command line.

