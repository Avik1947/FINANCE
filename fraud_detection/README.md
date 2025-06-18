# 🕵️‍♂️ Fraud Detection with Machine Learning

## 🔍 Problem
Credit fraud costs billions annually. The challenge? Fraud is rare, dynamic, and hides in noise. Traditional rule-based systems fail when fraud adapts. This project tackles real-world **highly imbalanced** fraud detection with ML — blending precision, automation, and anomaly intuition.

## ⚙️ Solution
We engineered a **ML pipeline** optimized for rare event classification, built with:

- 📊 **Preprocessing** for signal clarity  
- 🧠 **Model experimentation** across baseline and advanced classifiers  
- ⚠️ **Anomaly-detection** via IQR method  
---

## 🧠 Why These Decisions?

### 1. EDA-Driven Feature Understanding
We studied transaction patterns to isolate features with outlier potential (e.g.PCA variables). Used:

- Correlation heatmaps  
- Class imbalance visualization  
- Log-transformation on skewed features  

→ Goal: convert raw data into behavior fingerprints.

---

### 2. Anomaly-Aware Class Handling
**Fraud ≈ 0.17%** of data. So accuracy is **useless**.

We prioritized:

- `precision`, `recall`, `f1-score` over accuracy  
- PR-AUC (Precision-Recall curve) over ROC  
- Used **stratified train-test splits**  

→ Goal: maximize true positives, minimize false alarms.

---

### 3. Model Experiments

Tested multiple models with focus on **generalizability**:
→ We selected models based on **PR-AUC & F1** rather than raw accuracy.

---

### 4. Cross-Validation + Tuning

- Used `StratifiedKFold` to preserve fraud distribution across folds   
→ Goal: consistent fraud detection, even in unseen scenarios.

### 5. Undersampling + training
- Undersampled our data to get a balanced class subset
- Goal: Increase Recall.

---

## 🚀 Results

- **Recall**: 0.9 (SVC)  
- **f1-score**: 0.11
- **Precision**: 0.06  

---
