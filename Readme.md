[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/3TS0mELD)

# Machine Learning Task 1

## Breast Cancer — Binary Classification

Binary classification task using the **Breast Cancer Wisconsin Dataset** from scikit-learn.


## Objective

In this task, we build and compare 3 **binary classification** models to predict whether a tumor is:

- **0 — Malignant (Cancerous)**
- **1 — Benign (Non-cancerous)**

The binary classification models:

- Logistic Regression
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)

We focus on this task at **model training, evaluation, and comparison**.

⚠️ Feature scaling NOT used in this task.

---

## Dataset

We used the **Breast Cancer Wisconsin Dataset**, that available directly in `scikit-learn`

| Property       | Value                     |
|----------------|---------------------------|
| Samples        | 569                       |
| Features       | 30 numerical              |
| Target         | Binary (0 = Malignant, 1 = Benign) |
| Missing Values | None                      |

### Dataset Overview

- 569 samples
- 30 numerical features
- Binary target variable
- No missing values

Each feature represents a measurement extracted from a digitized image of a breast mass (e.g., radius, texture, area, smoothness, concavity, symmetry, etc.).

---

## Dataset Loading

Use the following code to load the dataset:

```python
from sklearn.datasets import load_breast_cancer

data = load_breast_cancer()
X = data.data
y = data.target
```

---

## The Main Tasks:

### 1. Train-Test Split

Split the dataset using:

- `test_size = 0.2`
- `random_state = 42`
- `stratify = y`

### 2. Model Training

Train the following models:

- Logistic Regression
- SVM
- KNN

Used default parameters unless clearly justified.

### 3. Model Evaluation

For each model, compute:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

### 4. Model Comparison

Create a comparison table summarizing the evaluation metrics for all models.

Then write a short conclusion answering:

- Which model performed best?
- In a medical context, which metric is most important and why?

---

## Project Structure

Your project must follow this structure:

```
breast-cancer-binary-classification/
├── modeling.ipynb
└── README.md
```

## Results Summary

| Model               | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression | 0.9561   | 0.9466    | 0.9861 | 0.9659   |
| SVM                 | 0.9298   | 0.9210    | 0.9722 | 0.9459   |
| KNN                 | 0.9122   | 0.9428    | 0.9166 | 0.9295   |


## Conclusion

**Logistic Regression** is the best-performing model across all metrics.

In a medical context, **Recall** is the most important metric because missing a malignant tumor (false negative) carries far greater risk than a false alarm. Logistic Regression achieves the highest recall at **98.61%**.

## Requirements

```
scikit-learn
numpy
pandas
matplotlib
seaborn
```
