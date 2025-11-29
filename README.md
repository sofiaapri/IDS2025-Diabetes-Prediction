# IDS2025-Diabetes-Prediction
Predicting and Analysing Diabetes Risk Using Patient Health Data

### Dataset (14.37 MB): 
100 000 synthetic patient records. Each record includes demographic, lifestyle, medical, and clinical features that are common predictors of diabetes [1] 

### Goal 1:
Explore how demographic, lifestyle, and clinical indicators relate to diabetes risk and stage, and identify patient clusters that represent distinct risk profiles (low, medium, high). Clustering is performed without label columns (diagnosed_diabetes, diabetes_stage) and without using the dataset’s precomputed diabetes_risk_score; these are only used afterwards to interpret the clusters.

### Goal 2: 
Build and evaluate models to predict diabetes diagnosis and stage based on patient data. Modeling excludes diabetes_risk_score as an input feature to avoid data leakage. For stage-prediction, Gestational diabetes will be treated separately since it represents a distinct clinical case compared to other diabetes types.

### Goal 3: 
Identify the most influential predictors of diabetes, derive a simple interpretable risk score (low, medium, high) and compare it against the dataset’s provided diabetes_risk_score baseline.

### Links:
[1] https://www.kaggle.com/datasets/mohankrishnathalla/diabetes-health-indicators-dataset