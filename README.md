# PCT-PREDICTION
This repository contains a machine learning-based Clinical Decision Support  model designed to predict whether procalcitonin (PCT) levels exceed 0.5 ng/mL using commonly available laboratory tests.
This repository contains a machine learning-based Clinical Decision Support (CDS) system designed to predict whether procalcitonin (PCT) levels exceed 0.5 ng/mL using commonly available laboratory tests. The model utilizes complete blood count (CBC) parameters, C-reactive protein (CRP), and creatinine (Cr) levels to provide a binary prediction of PCT levels, enabling clinicians to optimize testing and antibiotic stewardship.
# Procalcitonin Prediction using XGBoost (Google Colab)
This project focuses on predicting **Procalcitonin (PCT) levels** using the **XGBoost** machine learning model. Procalcitonin is a biomarker used to diagnose bacterial infections and sepsis. The model predicts whether the Procalcitonin level is **≥ 0.5** (binary classification) based on various laboratory test results.
The code is designed to run in **Google Colab**, making it easy to use without requiring local setup.
## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Google Colab Setup](#google-colab-setup)
4. [Usage](#usage)
5. [File Descriptions](#file-descriptions)
6. [Outputs](#outputs)
7. [License](#license)
---
## Project Overview
The goal of this project is to build a machine learning model that predicts whether a patient's Procalcitonin level is **≥ 0.5** based on a set of laboratory test results. The model is trained using the **XGBoost** algorithm, and hyperparameter tuning is performed using **RandomizedSearchCV**. The project includes:
- Data preprocessing and feature selection.
- Hyperparameter tuning for the XGBoost model.
- Model evaluation using accuracy, confusion matrix, ROC-AUC, and classification report.
- SHAP (SHapley Additive exPlanations) for model interpretability.
- Prediction on new patient data.
---
## Features
- **Input Data**: The dataset includes laboratory test results such as WBC, CRP, Creatinine, and more.
- **Target Variable**: Binary classification of Procalcitonin levels (`< 0.5` or `≥ 0.5`).
- **Model**: XGBoost with hyperparameter tuning.
- **Evaluation Metrics**:
  - Accuracy
  - Confusion Matrix (TP, TN, FP, FN)
  - ROC-AUC Curve
  - Sensitivity and Specificity
  - Positive Predictive Value (PPV) and Negative Predictive Value (NPV)
- **Interpretability**: SHAP summary and dependence plots for feature importance.
---
## Google Colab Setup
To run this project in Google Colab, follow these steps:
1. **Open Google Colab**:
   - Go to [Google Colab](https://colab.research.google.com/).
   - Click on `File` → `New Notebook` to create a new Colab notebook.
2. **Upload the Code**:
   - Copy the code from the repository and paste it into a Colab notebook cell.
   - Alternatively, you can upload the `.ipynb` file directly to Colab.
3. **Upload Dataset and New Patient Data**:
   - When prompted by the script, upload the following files:
     - **Train/Test Dataset**: The dataset containing laboratory test results and Procalcitonin levels.
     - **New Patient Data**: The dataset containing laboratory test results for new patients.
4.  **Run the Script**:
   - Execute each cell in the Colab notebook sequentially.
   - The script will:
     - Preprocess the data.
     - Train the XGBoost model with hyperparameter tuning.
     - Evaluate the model using various metrics.
     - Generate visualizations (confusion matrix, ROC curve, feature importance, SHAP plots).
     - Predict Procalcitonin levels for new patients and save the results to an Excel file.
       
  5.  **Download the Results**:
   - After running the script, download the following files:
     - `new_patient_predictions.xlsx`: Contains predictions for new patients.
     - `summary_statistics.xlsx`: Contains summary statistics of the dataset.
---
## Outputs
1. **Model Evaluation**:
   - Accuracy, Confusion Matrix, Classification Report.
   - ROC-AUC Curve, Sensitivity, Specificity, PPV, NPV.
2. **Visualizations**:
   - Confusion Matrix with TP, TN, FP, FN values.
   - Feature Importance Plot.
   - SHAP Summary Plot and Dependence Plots.
3. **Predictions**:
   - Predictions for new patients saved in `new_patient_predictions.xlsx`.
4. **Summary Statistics**:
   - Summary statistics of the dataset saved in `summary_statistics.xlsx`.
---

