# Heart Disease Prediction Project

## Overview
This project aims to build a machine learning model to predict whether a person has heart disease or not based on various medical and demographic features.

## Dataset
- **Source**: [Heart Disease Dataset](https://www.kaggle.com/datasets/ritwikb3/heart-disease-cleveland)
- The dataset includes features such as:
  - Age: Patients Age in years (Numeric)
  - Sex: Gender (Male : 1; Female : 0) (Nominal)
  - cp: Type of chest pain experienced by patient. This term categorized into 4 category. 0 typical angina, 1 atypical angina, 2 non- anginal pain, 3 asymptomatic (Nominal)
  - trestbps: patient's level of blood pressure at resting mode in mm/HG (Numerical)
  - chol: Serum cholesterol in mg/dl (Numeric)
  - fbs: Blood sugar levels on fasting > 120 mg/dl represents as 1 in case of true and 0 as false (Nominal)
  - restecg: Result of electrocardiogram while at rest are represented in 3 distinct values 0 : Normal 1: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV) 2: showing probable or definite left ventricular hypertrophyby Estes' criteria (Nominal)
  - thalach: Maximum heart rate achieved (Numeric)
  - exang: Angina induced by exercise 0 depicting NO 1 depicting Yes (Nominal)
  - oldpeak: Exercise induced ST-depression in relative with the state of rest (Numeric)
  - slope: ST segment measured in terms of slope during peak exercise 0: up sloping; 1: flat; 2: down sloping(Nominal)
  - ca: The number of major vessels (0–3)(nominal)
  - thal: A blood disorder called thalassemia 0: NULL 1: normal blood flow 2: fixed defect (no blood flow in some part of the heart) 3: reversible defect (a blood flow is observed but it is not normal(nominal)
  - target: It is the target variable which we have to predict 1 means patient is suffering from heart disease and 0 means patient is normal.

## Project Goals
- Perform exploratory data analysis (EDA) to understand the dataset.
- Train and evaluate multiple machine learning models to predict heart disease.
- Optimize the best-performing model to achieve higher accuracy.

## Project Workflow
1. **Data Preprocessing**:
   - Handle missing values (if any).
   - Normalize or scale numerical features.
   - Encode categorical features.
   
2. **Model Training and Evaluation**:
   - Tested multiple classification models:
     - Logistic Regression
     - Random Forest Classifier
     - K-Nearest Neighbors (KNN)
     - XGBoost
     - CATBoost
   - Performed hyperparameter tuning using `GridSearchCV` and `RandomizedSearchCV`.
   - Best-performing model: Logistic Regression with an accuracy of `88%`.

3. **Performance Metrics**:
   - **Accuracy**: `84%`
   - **Precision**: `82%`
   - **Recall**: `92%`
   - **F1 Score**: `86%`

4. **Feature Engineering**:
   - Thalach & cp were looking highly correlated as per correlation matrix so combined them and dropped thalch cloumn.
   - Slope & oldpeak were looking highly correlated as per correlation matrix so combined them and dropped slope cloumn.
   - Thal & exang were looking highly correlated as per correlation matrix so combined them and dropped thal cloumn.
   - Applied onehot encoding to the categorical features with multiple classes.
