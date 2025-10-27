# Bank Loan Default Risk Prediction

This project builds a credit scoring model to predict the likelihood of bank loan default for unsecured lending. Using a dataset of 5,960 applicants, it applies the CRISP-DM framework to perform data cleaning, feature engineering, model training, and interpretability analysis to support data-driven credit decisions.

## Key Features
- Data preprocessing with missing value imputation, outlier handling, and creation of the Loan-to-Value (LTV) ratio feature  
- Model comparison across Logistic Regression, Random Forest, Histogram Gradient Boosting, Decision Tree, and Neural Network  
- Scenario-based modelling:
  - **Goal 1:** Expand approvals while identifying ≥85% of bad customers (HGBT)
  - **Goal 2:** Capture ≥70% of good customers while minimizing default risk (RF)
  - **No Goal:** Balanced accuracy and transparency (DT)
- SHAP-based explainability highlighting key risk drivers such as **Debt-to-Income ratio** and **past delinquencies**

## Results
- Best model: **Histogram Gradient Boosting (Goal 1)** with PR-AUC ≈ 0.90  
- Key predictors: DEBTINC, DELINQ, CLAGE, YOJ  
- Outputs include cleaned data (`cleaned_data_imputed3.csv`) and SHAP beeswarm visualizations

## Tech Stack
Python · pandas · scikit-learn · matplotlib · seaborn · shap  

## Repository Structure
- `Final Code - Risk Default.py` – Main script  
- `data.csv` – Raw dataset  
- `cleaned_data_imputed3.csv` – Processed dataset  
- `shap_beeswarm_*.png` – SHAP visualizations  
- `documentationv2.docx` – Draft report  
- `Final Report.pdf` – Final analysis and recommendations  
