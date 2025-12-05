# Diabetes Prediction Model

##  Project Overview
This project implements a neural network model for predicting diabetes diagnosis based on demographic, lifestyle, and medical history data. The model is built using TensorFlow/Keras and includes comprehensive data preprocessing, handling of imbalanced data, and evaluation metrics.

##  Dataset
The dataset contains 700,000 training samples with 26 features, including:

### Numerical Features:
- Age
- Alcohol consumption per week
- Physical activity minutes per week
- Diet score
- Sleep hours per day
- Screen time hours per day
- BMI
- Waist-to-hip ratio
- Blood pressure measurements (systolic, diastolic)
- Heart rate
- Cholesterol levels (total, HDL, LDL)
- Triglycerides

### Categorical Features:
- Gender
- Ethnicity
- Education level
- Income level
- Smoking status
- Employment status

### Medical History Indicators:
- Family history of diabetes
- Hypertension history
- Cardiovascular history

### Target Variable:
- Diagnosed diabetes (binary: 0 = No, 1 = Yes)

##  Data Preprocessing

### 1. Feature Scaling
- Numerical features are standardized using StandardScaler
- Categorical features are encoded using LabelEncoder

### 2. Handling Class Imbalance
- SMOTE (Synthetic Minority Over-sampling Technique) is applied to balance the training data

### 3. Train-Test Split
- Training data: 700,000 samples
- Test data: Separate file for predictions

##  Model Architecture
The neural network consists of the following layers:

1. **Input Layer**: 25 features
2. **Dense Layer 1**: 64 units, ReLU activation
3. **Dense Layer 2**: 32 units, ReLU activation
4. **Dense Layer 3**: 16 units, ReLU activation
5. **Dense Layer 4**: 8 units, ReLU activation
6. **Output Layer**: 1 unit, Sigmoid activation

**Total Parameters**: 4,353

##  Training Configuration
- **Optimizer**: Adam
- **Loss Function**: Binary Crossentropy
- **Metrics**: Accuracy, Mean Absolute Error
- **Batch Size**: 32
- **Epochs**: 10
- **Validation Split**: 20%

##  Performance Metrics
On the training set (after SMOTE balancing):
- **Accuracy**: 60.84%
- **Mean Absolute Error**: 0.3916
- **F1 Score**: 0.6821
