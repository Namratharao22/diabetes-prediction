# Diabetes Prediction using Machine Learning

This project aims to predict the likelihood of a person having diabetes based on various clinical features such as age, gender, blood glucose level, BMI, hypertension, and smoking history using machine learning algorithms.

## Project Overview

The goal of this project is to build and evaluate predictive models for diabetes diagnosis using two machine learning algorithms:

1. **Support Vector Machine (SVM)**
2. **Decision Tree Classifier**

The dataset used is the **Diabetes Prediction Dataset**, which includes several clinical features and a target variable indicating whether a person has diabetes or not.

## Features

The dataset contains the following features:

- **gender**: Gender of the patient (Male/Female)
- **age**: Age of the patient
- **hypertension**: Whether the patient has hypertension (0 = No, 1 = Yes)
- **heart_disease**: Whether the patient has heart disease (0 = No, 1 = Yes)
- **smoking_history**: Smoking history (never, No Info, current, former, ever)
- **bmi**: Body Mass Index of the patient
- **HbA1c_level**: Hemoglobin A1c level of the patient
- **blood_glucose_level**: Blood glucose level of the patient
- **diabetes**: Target variable indicating if the person has diabetes (0 = No, 1 = Yes)

## Data Preprocessing

The dataset underwent several preprocessing steps:

1. **Gender Encoding**: The 'gender' feature was converted to a binary representation (0 = Female, 1 = Male).
2. **Smoking History Encoding**: The 'smoking_history' feature was converted to numeric values.
3. **Missing Values Handling**: Rows and columns with excessive missing values were removed.
4. **Feature Scaling**: Features were standardized using `StandardScaler` to ensure they are on the same scale for model training.

## Model Building

### Support Vector Machine (SVM)

- Hyperparameter tuning was performed using `GridSearchCV` with a focus on recall as the evaluation metric.
- The best parameters were:
  - **C**: 1
  - **Gamma**: scale
  - **Kernel**: linear

### Decision Tree Classifier

- Hyperparameter tuning was also performed for the Decision Tree classifier.
- The best parameters were:
  - **Criterion**: gini
  - **Max Depth**: 3
  - **Min Samples Split**: 4
  - **Min Samples Leaf**: 3

## Evaluation Metrics

- **Accuracy**: The proportion of correctly predicted instances (both positives and negatives).
- **Precision**: The proportion of true positives out of all predicted positives.
- **Recall**: The proportion of true positives out of all actual positives.
- **F1 Score**: A balanced score that combines precision and recall.
- **Confusion Matrix**: Used to evaluate the performance of the models.

### Results:

- **Decision Tree**:  
  - Accuracy: 97.23%  
  - Precision: 1.0000  
  - Recall: 0.6813  
  - F1 Score: 0.8104  

- **SVM**:  
  - Accuracy: 96.20%  
  - Precision: 0.9000  
  - Recall: 0.8260  
  - F1 Score: 0.8620  

## Conclusion

Both models (SVM and Decision Tree) demonstrated good performance in predicting diabetes, with Decision Tree showing slightly higher accuracy and precision. However, SVM performed better in terms of recall and F1 score, making it a better choice when prioritizing fewer missed diagnoses (false negatives).

