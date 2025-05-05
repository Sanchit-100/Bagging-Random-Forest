# Decision Tree Classifier from Scratch

This project implements a **Decision Tree Classifier** from scratch in Python without using `sklearn.tree`. It also includes enhancements like **Bagging** and **Random Forests** to improve classification accuracy and robustness. Only `numpy` and `pandas` are used.

---

## Features

### ✅ Decision Tree Classifier
- **Binary Splitting** based on thresholds to minimize **Gini Impurity**
- **Recursive Tree Construction** with customizable:
  - Maximum depth (`max_depth`)
  - Minimum samples per leaf (`samplesPerLeaf`)
- **Prediction Support** for individual and batch samples
- **Visualization** of tree structure via `print_tree()`

### ✅ Bagging Classifier
- Trains multiple trees on bootstrap samples
- Computes **Out-Of-Bag (OOB) Error** for unbiased performance estimation

### ✅ Random Forest Classifier
- Extension of Bagging with **feature randomness**
- At each split, considers only a random subset of features (`max_features`)
- Computes **OOB error**

---

## Dataset

The training dataset simulates a marketing scenario:

| Age | Income | Student | Credit Rating | Buy Computer |
|-----|--------|---------|---------------|--------------|
| 25  | High   | No      | Fair          | No           |
| 30  | High   | No      | Excellent     | No           |
| 35  | Medium | No      | Fair          | Yes          |
| 40  | Low    | No      | Fair          | Yes          |
| 45  | Low    | Yes     | Fair          | Yes          |
| 50  | Low    | Yes     | Excellent     | No           |
| 55  | Medium | Yes     | Excellent     | Yes          |
| 60  | High   | No      | Fair          | No           |

**Target**: Predict whether a person will buy a computer.

### Encodings

- Income: `{Low: 0, Medium: 1, High: 2}`
- Student: `{No: 0, Yes: 1}`
- Credit Rating: `{Fair: 0, Excellent: 1}`

---
