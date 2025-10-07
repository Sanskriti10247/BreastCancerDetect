# 🩺 Breast Cancer Detection using Machine Learning

This is a **college group project** for our Machine Learning course.  
The goal of this project is to build an interpretable and accurate machine learning model to detect **breast cancer (Malignant vs. Benign)** using diagnostic data.

---

## 📖 Project Overview

- **Dataset**: Breast Cancer Wisconsin (Diagnostic) Dataset from Kaggle  
  → [Link](https://www.kaggle.com/datasets/shantanugarg274/breast-cancer-prediction-dataset?select=breast_cancer_updated.csv)  
  → 5,015 rows × 32 features  

- **Problem Statement**:  
  Early and accurate diagnosis of breast cancer is critical for improving survival rates. While ML models can achieve high accuracy, their "black box" nature hinders clinical adoption. Doctors need interpretable models they can trust.  
  Our project focuses on **both predictive performance and interpretability** using SHAP values and feature importance.  

- **Models Implemented**:
  - Logistic Regression → interpretable baseline  
  - Random Forest → ensemble method, strong recall (0.99)  
  - XGBoost → boosting, best trade-off between accuracy & recall  

- **Explainability**:
  - Feature importance (impurity-based & permutation)
  - SHAP analysis (bar, beeswarm, waterfall plots)  
  - Key predictors: `compactness_mean`, `symmetry_mean`, `compactness_worst`

---
## 🚀 Open the Notebook (no setup needed)

You can run the notebook directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lf69jXtTER39634vmyOwnUJL-vjRr65h)

Click the badge above, and it will open the notebook in Colab — no installation or setup required.  

---

## 📊 Results

| Model              | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---------------------|----------|-----------|--------|----------|---------|
| Logistic Regression | 0.929    | 0.938     | 0.949  | 0.944    | 0.922   |
| Random Forest       | 0.965    | 0.961     | 0.984  | 0.973    | 0.991   |
| XGBoost             | 0.969    | 0.970     | 0.981  | 0.976    | 0.992   |

✅ **XGBoost emerged as the best model**, balancing high recall (critical in medicine) with strong accuracy.  
✅ Random Forest offered robustness + interpretability.  
✅ Logistic Regression provided a transparent baseline.

---

## 👥 Team Details

**Team Name**: *Model Mavericks*  

- Kabeer, 24BCS10119 (Team Leader)  
- Sanskriti, 24BCS10247  
- Shrival Kumar, 24BCS10254  
- Tejas Kumat, 24BCS10299  
- Nishant Bhaleem, 24BCS10314  

---

## 📂 Project Structure
```
BreastCancerDetect/
│
├── data/ # Dataset (CSV)
├── notebooks/ # Colab notebook
│ └── ML_Project.ipynb
├── ProjectReport/ # Detailed project report
│ └── Project_Report.pdf
└── README.md # Documentation
```

We aimed to build a model that’s not only accurate but also interpretable, so medical professionals can trust its predictions. We used techniques like SHAP analysis to explain which features influence predictions.  

---
## ⚙️ Methodology  

1. **Data Exploration**  
   - Checked for missing values and duplicates.  
   - Examined class balance between malignant and benign cases.  

2. **Baseline Model**  
   - Started with **Logistic Regression** for interpretability.  
   - Used **recall** as the primary metric, since false negatives are riskier than false positives.  

3. **Advanced Models**  
   - **Random Forest**: captured non-linear relationships, ensemble learning.  
   - **XGBoost**: boosting to reduce bias, strong accuracy on tabular data.  

4. **Explainability**  
   - **Feature Importance**: impurity-based & permutation.  
   - **SHAP Analysis**: bar, beeswarm, and waterfall plots to show how features influence predictions.  

 **Key Findings**:  
- **Recall**: Random Forest and XGBoost both achieved ~0.98–0.99 recall → nearly all malignant cases detected.  
- **Interpretability**: Logistic Regression coefficients and SHAP values gave transparent insights.  
- **Top Predictors**: `compactness_mean`, `symmetry_mean`, `compactness_worst`, and perimeter-related features consistently emerged as most important.

## 🔍 Explainability with SHAP  

- **Bar Plot**: `compactness_mean` and `symmetry_mean` had the strongest influence.  
- **Beeswarm Plot**: Showed how low/high feature values pushed predictions toward malignant or benign.  
- **Waterfall Plot**: Gave instance-level explanations — why a specific tumor was classified as malignant.  

This ensures the model is **not just accurate, but also trustworthy**.  

---

## 📑 Full Report

See the detailed methodology, results, analysis, and discussion here:  
**[Project_Report.pdf](ProjectReport/Project_Report.pdf)**

## Thank You !! 🎉

Thank you for taking the time to review our project.  
We hope our work contributes to the understanding of how **AI can support early breast cancer detection** and inspire future developments in interpretable medical AI.  
