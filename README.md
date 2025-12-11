# 🩺 Breast Cancer Diagnosis Prediction  
### Using K-Nearest Neighbors (KNN) and K-Means Clustering  
---

## 🎯 Objective
The goal of this assignment is to classify breast cancer tumors into two categories:

- **Malignant (M)**
- **Benign (B)**

This is achieved using a **supervised algorithm (KNN)** and an **unsupervised algorithm (K-Means Clustering)**.

---

## 📂 Dataset Description
The dataset contains several numerical features describing tumor cell characteristics, along with a `diagnosis` label indicating whether the tumor is malignant or benign.

---

## 🧹 Data Preprocessing Steps

### ✔ 1. Label Encoding
The categorical diagnosis column is encoded as:
- `M → 1`
- `B → 0`

### ✔ 2. Removing Unnecessary Columns
The following columns are dropped to clean the dataset:
- `id`
- `Unnamed: 32` (empty column)

### ✔ 3. Feature Scaling (Min–Max Normalization)
All feature columns (except the encoded `diagnosis`) are scaled into the **0–1 range** using Min-Max Normalization:

\[
X_{scaled} = \frac{X - X_{min}}{X_{max} - X_{min}}
\]

This ensures that all features contribute equally to the model.

---

## 🔀 Train–Test Split
The dataset is split into:
- **80% Training Data**
- **20% Testing Data**

This ensures proper evaluation of the KNN model.

---

## 🔵 K-Means Clustering (Unsupervised)
- K-Means is applied with **k = 2**, because there are two natural groups:
  - Malignant  
  - Benign  

- The clustering helps to observe:
  - How naturally the dataset separates
  - Whether malignant and benign tumors form distinguishable clusters

This does **not** use the diagnosis labels during training — only feature values.

---

## 🟢 K-Nearest Neighbors (Supervised Classification)
The KNN classifier is trained using:
- **k = 5**

Reason:
- Small datasets perform well with lower k values  
- k=5 balances bias and variance

The model predicts whether a tumor is **malignant (1)** or **benign (0)** on the test set.

---

## 📈 Evaluation Metrics

The performance of the KNN model is measured using:

### ✔ Accuracy
Proportion of total correct predictions.

### ✔ Precision
How many predicted malignant tumors were actually malignant.

### ✔ Recall
How many actual malignant tumors were correctly identified.

### ✔ F1-Score
Harmonic mean of precision and recall — useful for imbalanced datasets.

---

## 🧪 Summary of the Workflow

1. Encode diagnosis values (M→1, B→0)  
2. Drop unnecessary columns  
3. Normalize the dataset using Min-Max scaling  
4. Split dataset (80% train / 20% test)  
5. Apply K-Means clustering (k=2)  
6. Train KNN classifier (k=5)  
7. Evaluate using accuracy, precision, recall, F1-score  

---

## ✅ Final Notes
This assignment demonstrates both:

- **Unsupervised Learning** (K-Means)  
- **Supervised Learning** (KNN Classification)

It provides a complete workflow for medical diagnostic prediction using machine learning techniques.

---

## 📘 End of Report
