Diabetes Detection ML Project:
This project applies machine learning techniques to predict diabetes in female patients using the Pima Indians Diabetes Dataset. The aim is to build a clinically useful diagnostic model, with a strong emphasis on maximizing recall and F1-score to ensure effective detection of diabetic individuals.

Objective:
To develop a predictive model that can assist in clinical laboratory settings for identifying diabetes in female patients, utilizing physiological and medical features. The model prioritizes sensitivity (recall) and balanced performance to support medical decision-making.

Dataset
Source: Kaggle - Pima Indians Diabetes Database

Population: Female patients aged 21 years and older, of Pima Indian heritage

Target Variable: Outcome

1 = Diabetic

0 = Non-diabetic

Features Used:
Pregnancies

Glucose (most important feature)

Blood Pressure

Skin Thickness

Insulin

Body Mass Index (BMI)

Diabetes Pedigree Function

Age

Methodology
Data Cleaning: Zero values were replaced with NaN in specific columns (Glucose, Blood Pressure, Skin Thickness, BMI, Insulin) and imputed with column means.

Feature Scaling: Standardized features using StandardScaler.

Class Balancing: Applied SMOTE (Synthetic Minority Over-sampling Technique) to address class imbalance.

Model Training: Used RandomForestClassifier with hyperparameter tuning via GridSearchCV.

Threshold Tuning: Adjusted classification threshold based on ROC curve to improve recall.

Evaluation Metrics:

Confusion Matrix

Recall and F1-score (especially for class 1 - diabetics)

ROC AUC Score

Results
Recall (Diabetic Class - 1): 76%

F1-score (Diabetic Class - 1): 71%

ROC AUC Score: 0.82

Key Finding: Glucose was identified as the most important predictive feature, aligning with clinical understanding of diabetes.

Visualizations
Bar plot showing feature importance based on the trained Random Forest model

Box plot visualizing glucose distribution by diabetes outcome


File Structure

diabetes-detection-ml/
├── diabetes_dataset.csv                 # Original dataset
├── diabetes_model_pipeline.ipynb        # Colab Notebook with full pipeline
├── README.md                            # Project documentation

Future Work:
Integration of other models such as LightGBM or XGBoost

Implementation of ensemble methods

Use of SHAP or LIME for advanced model interpretability

Deployment of the model as a clinical diagnostic application using Streamlit or Flask

