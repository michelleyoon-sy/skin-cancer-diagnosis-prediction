# skin-cancer-diagnosis-prediction

This project focuses on predicting skin cancer status (Benign vs. Malignant) using statistical learning and machine learning methods. Developed as part of the *STATS 101C: Introduction to Statistical Models and Data Mining* course at UCLA, our team achieved 4th Place in the Kaggle competition with a final predictive accuracy of 0.60750. 

## Overview

Early detection of skin cancer is vital for improving survival rates, yet clinical data often contains complex patterns and significant missingness. This project utilizes a medical dataset, consisting of 50,000 training and 20,000 testing observations, to identify key predictors and build a robust classification model. Our approach prioritizes statistical rigor, effective imputation of medical data, and the balance between model complexity and interpretability.

https://www.kaggle.com/competitions/predicting-skin-cancer-status

## Key Challenges

* High Missingness: Approximately 7.84% of the training data was missing, a common issue in medical records. 
* Feature Selection: Identifying clinically relevant variables from 50 predictors across demographic, lifestyle, and clinical categories. 

## Key Features

* Data Imputation:
Implemented a specialized strategy for medical data by treating missing categorical values as a distinct "Data Not Available" category, which preserved information and significantly boosted accuracy to our highest score. 
* Regularized Modeling (Elastic Net):
Developed a Generalized Linear Model (GLM) with Ridge and Lasso regularization ($\alpha=0.5$). This allowed us to control coefficient magnitudes and mitigate overfitting while retaining clinically relevant predictors.

## Tech Stack

| Category | Tools / Methods |
|---|---|
| Programming | R, R Markdown |
| Data Analysis | EDA, Missing Data Imputation (MissForest, MICE, Hot Deck) |
| Statistical Modeling | Logistic Regression, LDA/QDA, ANOVA, Chi-Squared Test |
| Machine Learning | Random Forest, Elastic Net, LASSO, KNN, Naive Bayes |

## Models Evaluated

| Model | Imputation Method | Best Accuracy |
| --- | --- | --- |
| **GLM (Elastic Net)** | **Mean + "Missing" Cat** | **0.60750** |
| Logistic Regression | MissForest | 0.60415 |
| LDA | MissForest | 0.60360 |
| LASSO | MissForest | 0.60040 |
| Random Forest | - | 0.59630 |

## Results & Discussion

Our final model demonstrated that while complex models like Random Forest are powerful, a well-tuned Regularized Logistic Regression offered superior performance and interpretability for this medical dataset. The success of treating "missing" values as information suggests that data missingness in medical contexts is often not random (MNAR) and contains underlying diagnostic signals. 

## Collaboration

Developed collaboratively by Vidusha Adira, Maggie Cheung, Aashima Khanna, and Allison Seteono.

While we all contributed to EDA and model development, I primarily focused on the model developmen with a particular emphasis on implementing the Regularized GLM and Random Forest.

## Presentation & Paper

* [Final Paper (PDF)](./skin_cancer_diagnosis_prediction_final_paper.pdf)
* [Final Presentation (PDF)](./skin_cancer_diagnosis_prediction_final_presentation.pdf)
