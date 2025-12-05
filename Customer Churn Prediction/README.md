# Customer Churn Prediction Model

A deep learning model for predicting customer churn in telecom services using neural networks. This project demonstrates end-to-end machine learning workflow from data preprocessing to model deployment.

##  Project Overview

This project builds a binary classification model to predict whether a customer will churn (leave the service) or not. The model uses a neural network architecture implemented with TensorFlow/Keras and achieves approximately 79% accuracy on the test set.

##  Dataset

The dataset (`ccp.csv`) contains customer information from a telecom company with 7,043 entries and 21 features including:

### Features:
- **Demographic info**: Gender, SeniorCitizen, Partner, Dependents
- **Account information**: tenure, Contract, PaperlessBilling, PaymentMethod
- **Services subscribed**: PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies
- **Charges**: MonthlyCharges, TotalCharges

### Target Variable:
- **Churn**: Whether the customer left the service (Yes/No)

##  Model Architecture

The neural network model has the following architecture:
Input Layer (19 features)
↓
Dense Layer (32 neurons, ReLU activation)
↓
Dense Layer (16 neurons, ReLU activation)
↓
Dense Layer (8 neurons, ReLU activation)
↓
Output Layer (1 neuron, Sigmoid activation)