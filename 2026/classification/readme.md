# Machine Learning: Classification Methods

**BMI 511 — Spring 2026**  
**Instructor:** Pratik Dutta, Ph.D. | Department of Biomedical Informatics, Stony Brook University

---

## Lecture Materials

| Material | Description |
|----------|-------------|
| [ML_Classification_Lecture.pptx](./ML_Classification_Lecture.pptx) | Lecture slides (~30–35 min presentation) covering classification fundamentals, 5 core algorithms, evaluation metrics, and hands-on lab plan |

## Google Colab Notebooks

| # | Notebook | Topics | Open in Colab | Time |
|---|----------|--------|---------------|------|
| 1 | [Breast Cancer Classification](./NB1_Breast_Cancer_Classification.ipynb) | Logistic Regression, Decision Tree, Random Forest; train/test split, confusion matrix, feature importance | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/duttaprat/BMI_511/blob/main/2026/classification/NB1_Breast_Cancer_Classification.ipynb) | ~25 min |
| 2 | [Diabetes Prediction & Model Comparison](./NB2_Diabetes_Model_Comparison.ipynb) | All 5 classifiers head-to-head; ROC curves, cross-validation, GridSearchCV hyperparameter tuning | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/duttaprat/BMI_511/blob/main/2026/classification/NB2_Diabetes_Model_Comparison.ipynb) | ~35 min |
| 3 | [Gene Expression Cancer Classification](./NB3_Gene_Expression_Classification.ipynb) | High-dimensional data (p >> n), PCA, sklearn Pipelines, feature selection (ANOVA, MI), gene signature extraction | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/duttaprat/BMI_511/blob/main/2026/classification/NB3_Gene_Expression_Classification.ipynb) | ~30 min |
| 4 | [Decision Trees, CART & Random Forest](./NB4_DecisionTrees_CART_RandomForest.ipynb) | CART algorithm deep dive; Gini vs Entropy; pruning strategies; bagging; individual trees vs ensemble; learning curves | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/duttaprat/BMI_511/blob/main/2026/classification/NB4_DecisionTrees_CART_RandomForest.ipynb) | ~30 min |

## Suggested Teaching Flow (2.5 hours)

```
[0:00–0:35]   Lecture slides (presentation)
[0:35–1:00]   Notebook 1 — Breast Cancer Classification (intro)
[1:00–1:35]   Notebook 2 — Diabetes Prediction (model comparison)
[1:35–1:45]   Break
[1:45–2:15]   Notebook 4 — Decision Trees & CART deep dive
[2:15–2:30]   Notebook 3 — Gene Expression (advanced, if time permits) + wrap-up
```

## Algorithms Covered

- **Logistic Regression** — linear, probabilistic, clinical risk scores
- **Decision Tree (CART)** — interpretable rules, Gini/Entropy splitting
- **Random Forest** — ensemble of CART trees, bagging, feature importance
- **Support Vector Machine (SVM)** — kernel methods, high-dimensional data
- **K-Nearest Neighbors (KNN)** — instance-based, distance metrics

## Requirements

All notebooks run in Google Colab with no additional setup. Standard libraries used:
- `scikit-learn`, `numpy`, `pandas`, `matplotlib`, `seaborn`
