#  Diabetes Health Indicators – Machine Learning Project

A supervised machine learning project focused on **early detection of diabetes** using real-world clinical data.  
This project compares multiple classification models to identify the most accurate and reliable approach for medical diagnosis.

---

##  Project Overview

Diabetes mellitus is a chronic disease that often goes undetected in its early stages, leading to severe complications such as heart disease, kidney failure, and vision loss.  
The goal of this project is to **build and evaluate machine learning models** that can predict whether a patient has diabetes based on routine health indicators.

The project emphasizes **high recall and F1-score**, which are critical in healthcare to minimize missed diagnoses.

---

##  Objectives

- Clean and preprocess real-world medical data
- Handle missing values and duplicates
- Compare multiple supervised ML models
- Evaluate models using **Accuracy, Precision, Recall, F1-Score, ROC-AUC**
- Select the best-performing model for diabetes prediction

---

##  Dataset Description

- **Dataset:** `diabetes_dataset_2.csv`
- **Type:** Clinical health data
- **Initial Features:** 31
- **Final Features:** 28 (after cleaning and feature selection)

### Key Challenges Addressed:
- Missing values in clinical measurements (BMI, insulin, glucose)
- Duplicate patient records
- Inconsistent categorical formatting
- Target leakage (`diabetes_stage` column removed)

---

##  Data Preprocessing Pipeline

1. **Removed duplicate records**
2. **Dropped irrelevant & leakage-prone features**
3. **Handled missing values**
   - Numerical → Median Imputation
   - Categorical → Most Frequent (Mode)
4. **Cleaned categorical text**
5. **One-Hot Encoding for categorical variables**
6. **Standard Scaling for numerical features**
7. **Converted boolean features to integers**

---

## Machine Learning Models Used

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest (Bagging)
- Gradient Boosting

---

##  Model Evaluation Metrics

Each model was evaluated using:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC Curve & AUC
- Confusion Matrix

---

## Results Summary

| Model              | F1-Score |
|-------------------|----------|
| Logistic Regression | ~0.88 |
| KNN               | ~0.82 |
| Decision Tree     | ~0.92 |
| Gradient Boosting | ~0.92 |
| **Random Forest** | **0.9225 (Best)** |

**Best Model:** **Random Forest (Bagging)**  
It achieved the highest F1-score, offering an excellent balance between precision and recall.

---

##  Visualizations Included

- ROC Curves for all models
- Correlation Heatmap
- Confusion Matrices

### Key Insights:
- **HbA1c** and **Postprandial Glucose** are the strongest predictors
- Physical activity shows a negative correlation with diabetes
- Ensemble models outperform simpler classifiers

---

## Conclusion

This project demonstrates that **tree-based ensemble models**, particularly **Random Forest**, are highly effective for medical diagnosis tasks.  
With strong ROC-AUC (>0.94) and F1-score performance, the final model provides a reliable framework for early diabetes detection.

---

##  Project Structure

```bash
├── ML.ipynb
├── diabetes_dataset_2.csv
├── ML final project report.pdf
├── README.md
