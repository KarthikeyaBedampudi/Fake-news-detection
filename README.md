# 📰 Fake News Detection 

This project implements a machine learning pipeline to classify news headlines as **real** or **fake**, using TF-IDF vectorization and a Passive Aggressive Classifier.

---

## 📌 Overview

Fake news has become a critical issue in the digital age. This project aims to automatically detect deceptive news headlines using basic NLP and supervised machine learning.

---

## 🧾 Dataset

The dataset is a CSV file (`train.csv`) containing labeled news statements.
Each entry includes:

* `Statement`: The news text/headline
* `Label`: Ground truth (`True` or `False`)

---

## 🧠 Model & Workflow

### ✅ Step-by-Step Process

1. **Load and clean the data**

   * Drop missing values
2. **Split data**

   * 80% training, 20% testing
3. **Text preprocessing**

   * Convert text to TF-IDF features
4. **Model training**

   * Passive Aggressive Classifier (good for large, sparse datasets)
5. **Evaluation**

   * Accuracy: `53.2%`
   * Confusion matrix and classification report
6. **User interaction**

   * Input custom headlines for real-time prediction

---

## 📊 Results

| Metric    | Value  |
| --------- | ------ |
| Accuracy  | 53.2%  |
| Precision | \~0.53 |
| F1-score  | \~0.53 |

**Confusion Matrix:**

```
[[422 466]   ← False predictions
 [492 668]]  ← True predictions
```

**Key Insight:**
The model slightly favors predicting headlines as **True** but has room for significant improvement. Data quality or label noise might be affecting results.

---

## 💡 Sample Prediction Output

```
Enter a news headline: Biden signs new climate agreement
Prediction: True

Enter a news headline: Aliens spotted in Central Park
Prediction: False
```

---

## 📦 Requirements

Install with:

```bash
pip install pandas scikit-learn
```

---

## 🚀 Run the Code

```bash
python fake_news_detection.py
```

---
