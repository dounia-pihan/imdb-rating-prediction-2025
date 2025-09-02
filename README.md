# 🎬 IMDb Rating Prediction with ML - 2025 (*academic project*)

![Python](https://urldefense.com/v3/__https://img.shields.io/badge/Python-3.9-blue__;!!JmtQ7uFmLckTLA!8odC85lDCGVE5j5w1jYIwb6b32ysxAWrXCnhusoUod_dnwIhNnL3NLdK46ORFBZ1R-bvwR6p4iER3_qffrduAxHwkAM$)  
![scikit-learn](https://urldefense.com/v3/__https://img.shields.io/badge/scikit--learn-1.3-orange__;!!JmtQ7uFmLckTLA!8odC85lDCGVE5j5w1jYIwb6b32ysxAWrXCnhusoUod_dnwIhNnL3NLdK46ORFBZ1R-bvwR6p4iER3_qffrdud4U9bSw$)  
![Pandas](https://urldefense.com/v3/__https://img.shields.io/badge/Pandas-Data*20Analysis-lightblue__;JQ!!JmtQ7uFmLckTLA!8odC85lDCGVE5j5w1jYIwb6b32ysxAWrXCnhusoUod_dnwIhNnL3NLdK46ORFBZ1R-bvwR6p4iER3_qffrduuT1xeoQ$)  
![Matplotlib](https://urldefense.com/v3/__https://img.shields.io/badge/Matplotlib-Visualization-yellow__;!!JmtQ7uFmLckTLA!8odC85lDCGVE5j5w1jYIwb6b32ysxAWrXCnhusoUod_dnwIhNnL3NLdK46ORFBZ1R-bvwR6p4iER3_qffrduQXJtbAc$)  
![RandomForest](https://urldefense.com/v3/__https://img.shields.io/badge/Model-RandomForest-green__;!!JmtQ7uFmLckTLA!8odC85lDCGVE5j5w1jYIwb6b32ysxAWrXCnhusoUod_dnwIhNnL3NLdK46ORFBZ1R-bvwR6p4iER3_qffrdu6q7p9xo$)  

---

## Project Description  

This project applies supervised Machine Learning techniques to predict IMDb ratings.  
The workflow includes:  
- A full preprocessing pipeline (handling missing values + OneHot encoding).  
- Comparison between **Linear Regression** and **Random Forest Regressor**.  
- Model evaluation using a train/test split and cross-validation.  
- External validation on a second dataset of movies to test generalization.  

---

## Objective 

The goal of this project is to develop a **supervised Machine Learning model** capable of predicting a movie’s IMDb rating based on its features (genre, runtime, release year, etc.).  

This work aims to:  
- Assess the performance of different regression models.  
- Highlight dataset limitations (bias from the IMDb Top 1000).  
- Test the model’s ability to generalize on an external dataset.  

---

## Methodology  
1. **Data Preprocessing**  
   - Imputation of missing values (median for numeric, most frequent for categorical).  
   - OneHot encoding for categorical features.  
2. **Model Training**  
   - Linear Regression (baseline).  
   - Random Forest Regressor (main model).  
3. **Evaluation**  
   - Metrics: R² and RMSE.  
   - Cross-validation (KFold=5).  
   - Visualization: Predicted vs Actual scatter plots.  
4. **External Validation**  
   - Tested the pipeline on `all_movies_dataset.csv`.  
   - Showed limited generalization due to dataset differences.  

---

## Results  
- **Linear Regression** → Low performance (R² close to 0).  
- **Random Forest** → Strong performance on IMDb Top 1000 (R² ≈ 0.8).  
- **External validation** → Negative R² (poor predictions on unseen dataset).  

This highlights a selection bias: training only on the Top 1000 (already well-rated movies) makes the model good at predicting “good” films, but weak on a more diverse dataset.  

---
