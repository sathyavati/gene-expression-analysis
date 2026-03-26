# 🧬Gene Expression Analysis and Disease Relationship

## 📌 Project Overview

This project explores how gene expression data and clinical features can be used to predict:

🧪 Disease Status

💊 Treatment Response

Using machine learning, we aim to uncover biological patterns and support data-driven healthcare decisions.


## 🧠 What is Gene Expression?

Gene expression refers to how actively a gene produces its functional products (like proteins).
Variations in gene expression can indicate disease presence, progression, and severity.
## 🎯 Problem Statement

Can we predict disease status and treatment response using gene expression data and clinical features?
## 💡 Why This Problem Matters

🔬 Molecular Insights

Understanding how gene expression influences disease development

🔗 Integration of Factors

Combining:

* Gene data

* Clinical data (Age, Gender)

* Lifestyle factors (Smoking)

🧬 Personalized Medicine

* Early diagnosis

* Biomarker discovery

* Better treatment strategies
## ⚠️ Challenges

1. Biological Variability

Gene expression varies across patients → noisy data

2. High Dimensionality

Real-world datasets contain thousands of genes

3. Class Imbalance

Some disease classes have very few samples

4. Accuracy vs Interpretability

Balancing:

* High accuracy

* Medical explainability
## 📂 Dataset

📍 Source: Kaggle (by ylmzasel)

👥 Samples: 1000 patients

Features:

  * Gene Expression:

       * Gene_X_Expression

       * Gene_Y_Expression

  * Clinical:

       * Age

       * Gender

       * Smoking Status

  * Targets:

       * DiseaseStatus

       * TreatmentResponse
## ⚙️ Methodology

🔹 1. Data Preprocessing
* Removed leakage features:
   * PatientID
   * SmokingStatus
   * TreatmentResponse
   * Missing value handling
   * Label Encoding
   * Feature Scaling

🔹 2. Feature Selection
* ANOVA (SelectKBest)
* LASSO (conceptual from research)

🔹 3. Dimensionality Reduction
* PCA (Principal Component Analysis)
* Reduced features → retained 99.1% variance

🔹 4. Handling Imbalance
* Applied SMOTE
* Balanced class distribution for better learning

🔹 5. Model Training
* Logistic Regression
* Random Forest
* Support Vector Machine (SVM)

✔ Hyperparameter tuning using GridSearchCV

✔ Cross-validation using Stratified K-Fold
## 📊 Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
## 📈 Results

| Model               | Accuracy    | F1 Score  | AUC       |
| ------------------- | ----------- | --------- | --------- |
| Logistic Regression | 0.69        | 0.78      | 0.83      |
| Random Forest       | ⭐ **0.945** | **0.956** | **0.999** |
| SVM                 | 0.62        | 0.73      | 0.84      |

👉 Best Model: Random Forest
## 🔍 Key Insights

* Gene expression is a strong predictor of disease
* Most important features:
   * Age
   * Gene_X_Expression
   * Gene_Y_Expression
* PCA successfully reduced dimensionality
* SMOTE improved minority class detection
## 🚫 Limitations

* Dataset has only 2 gene features
* Severe class imbalance
* TreatmentResponse prediction not possible:
    * Only one class present in diseased subset
## 🔮 Future Work

* Use large-scale genomic datasets
* Apply deep learning (ANN, CNN)
* Use SHAP/LIME for explainability
* Deploy as a healthcare prediction tool
