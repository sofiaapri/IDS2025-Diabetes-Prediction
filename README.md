# IDS2025-Diabetes-Prediction
Predicting and Analysing Diabetes Risk Using Patient Health Data

## Dataset (14.37 MB): 
100 000 synthetic patient records. Each record includes demographic, lifestyle, medical, and clinical features that are common predictors of diabetes [1] 

## Motivation
Diabetes is a major and growing public health burden, yet it often develops silently for many years before diagnosis. In many real-world settings, detailed laboratory tests are expensive, unavailable, or only carried out once the disease is already suspected. Understanding how simple demographic, lifestyle and routine clinical measures relate to diabetes can help identify higher-risk individuals earlier and support prevention. By analysing this synthetic population without using diagnostic laboratory markers, we examine how far everyday clinical and lifestyle information can indicate diabetes risk and which factors contribute most to it.

## Goal 1:
Explore how demographic, lifestyle and non-laboratory clinical indicators relate to diabetes, and identify patient clusters that represent broad metabolic risk profiles (lower, intermediate, higher). Clustering is performed on upstream features only, excluding diagnostic lab markers and the dataset’s diabetes_risk_score;

## Goal 2: 
Build and evaluate predictive models for diabetes outcomes, focusing primarily on diabetes diagnosis as a binary target. All models exclude diagnostic lab variables and diabetes_risk_score to avoid data leakage.

## Goal 3: 
Identify the most influential predictors for diagnosed_diabetes, and use them to construct a simple, interpretable point-based risk score with low, medium and high risk groups. Compare this 5-variable score to the dataset’s original diabetes_risk_score in terms of diabetes prevalence across risk groups.

## Results
Results

- Diabetes is associated with older age, higher BMI, blood pressure and lipids, lower physical activity, and family history of diabetes.

- K-means clustering yields three metabolic profiles (lower, intermediate, higher risk) with modest but consistent differences in diabetes prevalence.

- The best prediction model is a tuned Random Forest (macro-F1 ≈ 0.60, ROC-AUC ≈ 0.66) using only non-laboratory features.

- Top predictors include family history, age, physical activity, BMI, blood pressure and lipid profile, aligning with known risk factors.

- A simple 5-variable point-based risk score shows a clear low/medium/high gradient in diabetes prevalence.

- The risk score performs competitively with the dataset’s composite diabetes_risk_score (similar ROC-AUC), despite most likely using fewer and simpler inputs.

## To replicate our analysis:
1. Clone the repository.

2. Run Goal 1 notebook: exploratory analysis and clustering.
  Open the EDA.ipynb and run all cells. This notebook loads the provided synthetic diabetes dataset, removes diagnostic lab variables  and rare outcome categories, performs    exploratory analysis, and fits the K-means clustering model to obtain the three metabolic risk profiles.

3. Run Goal 2–3 notebook: predictive modelling and risk score.
  Open the notebook Modelling.ipynb and run all cells. This notebook applies the same preprocessing pipeline, trains and evaluates the supervised models for     diagnosed_diabetes and diabetes_stage, extracts feature importances and correlations, and constructs and evaluates the 5-variable point-based risk score.

## Links:
[1] https://www.kaggle.com/datasets/mohankrishnathalla/diabetes-health-indicators-dataset
