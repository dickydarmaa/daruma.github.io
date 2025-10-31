
# 🌧️ Flood Prediction System – Bandar Lampung

**Predicting flood events using meteorological data and machine learning.**  
A **Data Science project** that applies the **Random Forest Classifier** to predict flood occurrences in **Bandar Lampung (2010–2020)** based on key meteorological indicators.

![Correlation Matrix](./korelasi.png)
![Feature Importance](./featureImportance.png)

---

## 📘 Project Overview

This project focuses on developing a **Flood Prediction Model for Bandar Lampung** using data science and machine learning techniques.  
The goal is to identify key meteorological factors influencing flood events and to build a model that supports **early warning systems** for local disaster mitigation.

The project follows the **CRISP-DM-inspired data science workflow**, covering:
1. Data understanding  
2. Preprocessing & feature engineering  
3. Modeling using Random Forest  
4. Evaluation (Accuracy, Recall, Precision, AUC-ROC)  
5. Visualization and deployment via interactive dashboard

---

## 🧠 Key Insights

| Factor | Correlation with Flood |
|--------|------------------------|
| **Weekly Rainfall** | **1.00 (Strongest Predictor)** |
| **Daily Rainfall** | 0.76 |
| **Humidity** | 0.74 |
| **Air Temperature** | 0.63 |

> High rainfall accumulation, elevated humidity, and higher air temperatures strongly correlate with flood events.

---

## ⚙️ Model Development

### 🧩 Data Source
- Dataset: [Kaggle – Dataset Kejadian Banjir dan Variabel Pendukung](https://www.kaggle.com/datasets/ramadhannurpambudi/dataset-kejadian-banjir-dan-variabel-pendukung)
- Location: Bandar Lampung, Indonesia  
- Period: 2010–2020  
- Total Records: 50 samples  

### 🔍 Features
| Category | Variables |
|-----------|------------|
| Meteorological | Air Temperature, Humidity, Surface Wind, Monsoon Direction, Daily Rainfall, Weekly Rainfall |
| Temporal | Year, Month, Day |
| Target | Flood Occurred (1=Yes, 0=No) |

### 🧼 Preprocessing Steps
- Checked for missing and duplicate values  
- Standardized numeric formats  
- Normalized data to 0–1 range  
- Converted `Tanggal` to temporal features (`Year`, `Month`, `Day`)

---

## 🤖 Model Specification

| Component | Description |
|------------|-------------|
| **Algorithm** | Random Forest Classifier |
| **Estimators** | 50 trees |
| **Weights** | Balanced class weights |
| **Validation** | Stratified 5-Fold Cross Validation |
| **Split Ratio** | 70% Train / 30% Test |
| **Libraries** | pandas, numpy, scikit-learn, matplotlib, seaborn |

---

## 📊 Evaluation Results

| Metric | Score |
|--------|--------|
| **Accuracy** | 93.3% |
| **Recall** | 100% |
| **Precision** | 85.7% |
| **AUC-ROC** | 94.4% |
| **OOB Score** | 97% |
| **Mean Cross-Validation Score** | 90% |

> ✅ The model successfully identified **all flood cases (Recall 1.0)** while maintaining **high precision** and **strong generalization**.

---

## 🧩 Feature Importance

| Rank | Feature | Importance Score |
|------|----------|------------------|
| 1 | Total Rainfall (mm) | 0.55 |
| 2 | Humidity (%) | 0.15 |
| 3 | Air Temperature (°C) | 0.13 |
| 4 | Year | 0.05 |
| 5 | Weekly Rainfall | 0.04 |
| 6 | Surface Wind | 0.03 |
| 7 | Month | 0.02 |
| 8 | Monsoon Direction | 0.02 |
| 9 | Day | 0.01 |

> 💡 **Rainfall** dominates as the strongest indicator of flood likelihood.

---

## 🌐 Interactive Dashboard

A responsive dashboard built using **Tailwind CSS** and **Chart.js** to visualize:
- Model metrics (accuracy, recall, precision, AUC)
- Feature importance
- Confusion matrix
- Correlation matrix
- Cross-validation & OOB performance

### 🔗 Demo File:
> [index.html](./index.html)

**Preview:**
![Dashboard Preview](./preview-dashboard.png)

---

## 🏗️ Project Architecture

