# 🧬 Explainable Machine Learning for Cancer Prediction Using RNA Sequencing Data

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python) 
![XGBoost](https://img.shields.io/badge/XGBoost-Gradient%20Boosting-orange) 
![PLOS ONE](https://img.shields.io/badge/PLOS%20ONE-Paper-lightgrey) 
![Status](https://img.shields.io/badge/Status-Completed-success)

This repository presents an **explainable machine learning model** for predicting cancer using **high-dimensional RNA sequencing data**. The study leverages **feature selection** and **XGBoost classification** to distinguish cancer patients from non-cancer patients while highlighting the **most influential genes** driving predictions.  

---

## 📌 Dataset Overview

The dataset originates from **The Cancer Genome Atlas (TCGA)**, accessed via the **Genomic Data Commons (GDC)**.

- **Number of features:** 18,741 genes (e.g., `ARHGEF10L`, `HIF3A`, etc.)  
- **Feature values:** Continuous numeric gene expression values (e.g., 5.2482, 4.0013, 2.9374, …)  
- **Target variable:** `sample_type_id`  
  - `0.0` → Non-cancer patient  
  - `1.0` → Cancer patient  
- **Purpose:** Predict cancer presence based on RNA expression profiles.  

> The combination of high-dimensional continuous features with a **binary target** makes this dataset ideal for **explainable machine learning**, enabling the identification of key genes associated with cancer.

---

## 🧪 Project Overview

The workflow of this study includes:

1. **Data preprocessing:** Cleaning and preparation of RNA sequencing data.  
2. **Feature selection:** Identifying the most relevant genes using **Mutual Information (MI)**.  
3. **Classification:** Training an **XGBoost** model for cancer prediction.  
4. **Evaluation:** Validating model performance using cross-validation and classification metrics.  
5. **Explainability:** Highlighting the most influential genes to provide biological insights.  

---

## 📈 Model Performance

### Validation Metrics

| Metric | Cancer (1) | Non-Cancer (0) |
|--------|------------|----------------|
| Precision | 0.99 | 1.00 |
| Recall    | 1.00 | 0.83 |
| F1-Score  | 0.99 | 0.91 |

- **Overall Accuracy:** 0.99  
- **Macro F1 Score:** 0.95  

### Cross-Validation (5-fold)

| Fold | Accuracy |
|------|----------|
| 1 | 1.000 |
| 2 | 0.985 |
| 3 | 1.000 |
| 4 | 0.985 |
| 5 | 0.985 |

- **Average Accuracy:** 0.991  

> The results demonstrate excellent predictive performance, especially for correctly identifying cancer patients.

---

## 📊 Feature Importance

The **top 15 genes** contributing most to cancer prediction, based on **XGBoost feature importance**, are:

| Rank | Gene Symbol | Importance Score |
|------|------------|----------------|
| 1    | ANGPTL6    | 0.2219         |
| 2    | CLEC4G     | 0.1967         |
| 3    | GABRD      | 0.0716         |
| 4    | COLEC10    | 0.0674         |
| 5    | CD34       | 0.0505         |
| 6    | OLFML2A    | 0.0285         |
| 7    | CLEC4M     | 0.0281         |
| 8    | SMARCA4    | 0.0252         |
| 9    | CCNE1      | 0.0247         |
| 10   | ECM1       | 0.0236         |
| 11   | CD200      | 0.0227         |
| 12   | GPR21      | 0.0215         |
| 13   | AZI1       | 0.0205         |
| 14   | ATN1       | 0.0196         |
| 15   | NOTCH3     | 0.0177         |

> These genes are the most influential features in the XGBoost model for predicting cancer. Highlighting them improves **explainability** and gives insight into potential **biological relevance** of gene expression patterns.

#### Suggested Visualization
![Feature Importance](Results/FeatureImportance.png)
This provides a clear, visual summary of the genes most critical for model predictions.
🧠 Key Takeaways

High predictive accuracy: The model identifies cancer patients with near-perfect accuracy.

Explainable insights: Top-ranked genes reveal the features driving predictions, providing biological interpretability.

Robust model: Consistent cross-validation results demonstrate generalizability.
🛠 Tools & Technologies

Python – data processing and analysis

XGBoost – gradient boosting classifier

Scikit-Learn – feature selection and model evaluation

Pandas & NumPy – handling high-dimensional gene expression data
🤝 Contribution

This repository is for results and methodology sharing only.
For questions, discussions, or collaboration inquiries, please open an issue.
