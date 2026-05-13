# skin-cancer-diagnosis-prediction

This project focuses on predicting skin cancer status (Benign vs. Malignant) using statistical learning and machine learning methods. Developed as part of the *STATS 101C: Introduction to Statistical Models and Data Mining* course, our team achieved 4th Place in the Kaggle competition with a final predictive accuracy of 0.60750. 

## Overview

Early detection of skin cancer is vital for improving survival rates, yet clinical data often contains complex patterns and significant missingness. This project utilizes a large-scale medical dataset to identify key predictors and build a robust classification model. Our approach prioritizes statistical rigor, effective imputation of medical data, and the balance between model complexity and interpretability. 

### Key Challenges

* 
**High Missingness**: Approximately 7.84% of the training data was missing, a common issue in medical records. 


* 
**Feature Selection**: Identifying clinically relevant variables from 50 predictors across demographic, lifestyle, and clinical categories. 


* 
**Complexity Trade-off**: Navigating the bias-variance tradeoff to prevent overfitting in a high-dimensional feature space. 



## Key Features

* **Advanced Data Imputation**:
Implemented a specialized strategy for medical data by treating missing categorical values as a distinct **"Data Not Available"** category, which preserved information and significantly boosted accuracy to our highest score. 


* **Statistical Feature Engineering**:
Conducted in-depth EDA using density plots, boxplots, and statistical tests (One-Way ANOVA, Chi-Squared) to select the 19 most significant predictors, including age, family history, and immunosuppression status. 


* **Regularized Modeling (Elastic Net)**:
Developed a **Generalized Linear Model (GLM)** with Ridge and Lasso regularization ($\alpha=0.5$). This allowed us to control coefficient magnitudes and mitigate overfitting while retaining clinically relevant predictors. 



## Tech Stack

| Category | Tools |
| --- | --- |
| **Language** | R (R Markdown for full analysis) |
| **Statistical Methods** | GLM (Logistic Regression), LDA/QDA, ANOVA, Chi-Squared Test, Elastic Net |
| **Machine Learning** | Random Forest, LASSO, KNN, Naive Bayes |
| **Data Processing** | MissForest, MICE, Hot Deck Imputation, Exploratory Data Analysis (EDA) |

## Models Evaluated

| Model | Imputation Method | Best Accuracy |
| --- | --- | --- |
| **GLM (Elastic Net)** | **Mean + "Missing" Cat** | **0.60750** |
| Logistic Regression | MissForest | 0.60415 |
| LDA | MissForest | 0.60360 |
| LASSO | MissForest | 0.60040 |
| Random Forest | - | 0.59630 |

## Results & Discussion

Our final model demonstrated that while complex models like Random Forest are powerful, a well-tuned **Regularized Logistic Regression** offered superior performance and interpretability for this medical dataset. The success of treating "missing" values as information suggests that data missingness in medical contexts is often not random (MNAR) and contains underlying diagnostic signals. 

## Collaboration

Developed collaboratively by Vidusha Adira, Maggie Cheung, Aashima Khanna, Allison Seteono, and Michelle Yoon. 

## Presentation & Paper

* [Final Paper (PDF)](https://www.google.com/search?q=link-to-your-paper)
* [Final Presentation (PDF)](https://www.google.com/search?q=link-to-your-presentation)


## Overview

The goal was to create a web-based learning tool that allows readers to explore classical Korean literature through modern data visualization and design.

The original text is used with the approval of the Korean Classics Research Institute, successor to the Minjok Munhwa Promotion Association. The full text is available via the Korean Classics DB or the National Library of Korea Digital Archive.

## Key Features

* Visualization of relationships among characters in *Dogangrok*
* Keyword frequency and LDA topic modeling results represented via word clouds
* Clean, readable web interface for educational use
* Integration of cultural data for modern digital humanities applications

## Tech Stack

| Category      | Tools                      |
| ------------- | -------------------------------------- |
| Frontend      | HTML, CSS, JavaScript                  |
| Visualization | Python (Word Cloud, KoNLPy)            |

## Collaboration

Developed collaboratively with Seonu An.

While we both contributed to design and visualization, I primarily focused on the web interface design and frontend implementation (HTML/CSS).
