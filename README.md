<div align="center">

# 🛡️ FraudLens

### ML-Powered Credit Card Fraud Detection

*Real-time transaction risk scoring with feature-level explanations*

[![Live Demo](https://img.shields.io/badge/🤗%20Hugging%20Face-Live%20Demo-yellow?style=for-the-badge)](https://huggingface.co/spaces/Parth-Saxena/FraudLens)
[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-RandomForest-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

**[🚀 Try the Live Demo](https://huggingface.co/spaces/Parth-Saxena/FraudLens)**

</div>

---

## 📌 Overview

**FraudLens** is an end-to-end machine learning project that detects fraudulent credit card transactions. This repository holds the **original training notebook** — the single source of truth for the model behind the live demo. From raw transaction data → exploratory analysis → trained classifier → deployed interactive app, this repo covers the full pipeline.

> 🔗 This notebook is the exact model deployed at **[FraudLens on Hugging Face Spaces](https://huggingface.co/spaces/Parth-Saxena/FraudLens)** — the live demo is not a separate or restyled model, it's this one, wrapped in an interactive UI.

---

## ✨ What It Does

| | |
|---|---|
| 🎯 | Classifies transactions as **fraudulent** or **legitimate** in real time |
| 📊 | Handles a **highly imbalanced** dataset (~0.17% fraud rate) |
| 🌲 | Trained with a **Random Forest** classifier |
| 🧾 | Live demo returns a **fraud probability score**, risk gauge, and **SHAP-style feature breakdown** |

---

## 📂 Repository Contents

```
📦 FraudLens
 └── 📓 Credit_Card_Fraud_Detection.ipynb   ← original model training notebook (source of truth)
```

---

## 🗃️ Dataset

| Metric | Value |
|---|---|
| **Total transactions** | 284,807 |
| **Fraud cases** | 492 (~0.17%) |
| **Valid transactions** | 284,315 |
| **Features** | `Time`, `Amount`, + 28 PCA-transformed features (`V1`–`V28`) |
| **Target** | `Class` — `0` = legitimate, `1` = fraud |

> Features `V1`–`V28` are anonymized via PCA to protect cardholder confidentiality — they aren't individually human-interpretable, but collectively capture transaction patterns.

---

## 🧠 Approach

```
1. Exploratory Data Analysis
   └── class distribution • fraud vs. valid amount stats • correlation heatmap

2. Preprocessing
   └── feature/target split • 80/20 train-test split

3. Model Training
   └── RandomForestClassifier (scikit-learn)

4. Evaluation
   └── Accuracy • Precision • Recall • F1-score • MCC • Confusion Matrix
```

---

## ⚙️ Getting Started

**1. Install dependencies**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

**2. Run the notebook**

Open `Credit_Card_Fraud_Detection.ipynb` in Jupyter, point the dataset path to your local copy of the CSV, and run all cells to reproduce training and evaluation.

---

## 🚀 Live Demo

<div align="center">

### Try FraudLens without installing anything

[![Open in Spaces](https://img.shields.io/badge/🤗%20Open%20in-Hugging%20Face%20Spaces-blue?style=for-the-badge)](https://huggingface.co/spaces/Parth-Saxena/FraudLens)

</div>

Enter transaction details — amount, merchant category, card info, and more — and get back:

- 🎯 A **fraud probability score** with a color-coded risk gauge
- 🔍 A **SHAP-style feature contribution breakdown** (what pushed the score up or down)
- 📈 **Model confidence** and performance metrics

---

## ⚠️ Disclaimer

This project is built for **educational and portfolio purposes**. It is *not* intended for production fraud detection without further validation, testing, and compliance review.

---

<div align="center">

### 👤 Author

**Parth Saxena**

[![Hugging Face](https://img.shields.io/badge/🤗-Hugging%20Face%20Profile-yellow?style=flat-square)](https://huggingface.co/Parth-Saxena)

</div>
