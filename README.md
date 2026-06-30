# 📡 Telecom Customer Churn Prediction
### An End-to-End Data Analytics & Machine Learning Project
 
![Python](https://img.shields.io/badge/Python-3.11-blue?style=flat&logo=python)
![Power BI](https://img.shields.io/badge/PowerBI-Dashboard-yellow?style=flat&logo=powerbi)
![ML](https://img.shields.io/badge/ML-XGBoost%20%7C%20LightGBM-green?style=flat)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange?style=flat)
 
---
 
## 📌 Problem Statement
 
XYZ Telecom is experiencing a **26.5% annual customer churn rate**, resulting in significant revenue loss every quarter. The Customer Success and Revenue Analytics teams require a data-driven early-warning system that:
 
- Identifies **high-risk customers 60–90 days before churn** occurs
- Segments customers by **behavioral and demographic risk profiles**
- Enables **targeted retention campaigns** by the marketing team
- Provides explainable predictions that business stakeholders can act on
**Goal:** Reduce customer churn by 8–10% within two quarters through predictive intervention, using machine learning and an interactive Power BI dashboard.
 
---
## 📁 Project Structure
 
```
telecom-churn-prediction/
│
├── data/
│   ├── raw/                  ← Original unmodified dataset (not pushed to Git)
│   ├── processed/            ← Cleaned & feature-engineered data
│   └── predictions/          ← Model output scores for Power BI
│
├── notebooks/
│   ├── 01_data_profiling.ipynb       ← Initial data understanding
│   ├── 02_eda.ipynb                  ← Exploratory Data Analysis
│   ├── 03_feature_engineering.ipynb  ← New feature creation
│   ├── 04_modeling.ipynb             ← Model building & evaluation
│   └── 05_explainability.ipynb       ← SHAP analysis
│
├── src/
│   ├── preprocess.py         ← Data cleaning functions
│   ├── features.py           ← Feature engineering pipeline
│   └── model.py              ← Model training & evaluation
│
├── powerbi/
│   └── churn_dashboard.pbix  ← Final Power BI dashboard
│
├── reports/
│   └── business_summary.pdf  ← Non-technical stakeholder report
│
├── requirements.txt
├── .gitignore
└── README.md
```
 
---
 
## 📊 Dataset
 
| Property | Detail |
|---|---|
| **Source** | IBM Telco Customer Churn — Kaggle |
| **Rows** | 7,043 customers |
| **Columns** | 21 features |
| **Churn Rate** | 26.54% |
| **Domain** | Telecommunications |
 
### Key Features
 
| Feature | Description |
|---|---|
| `customerID` | Unique customer identifier |
| `tenure` | Number of months with the company |
| `MonthlyCharges` | Current monthly bill amount |
| `TotalCharges` | Total amount charged to date |
| `Contract` | Contract type (Month-to-month, One year, Two year) |
| `PaymentMethod` | How the customer pays |
| `InternetService` | Type of internet service |
| `TechSupport` | Whether customer has tech support |
| `Churn` | Target variable — Yes / No |
 
---
 
## 🔧 Tech Stack
 
### Data & Engineering
- **Python 3.11** — Core language
- **Pandas & NumPy** — Data manipulation
- **SQL / SQLite** — Data storage and querying
- **Jupyter Notebook** — Analysis environment
### Machine Learning
- **Scikit-learn** — Preprocessing, baseline models
- **XGBoost / LightGBM** — Production-grade gradient boosting
- **Imbalanced-learn** — SMOTE for handling class imbalance
- **SHAP** — Model explainability
### Visualization & Reporting
- **Matplotlib / Seaborn / Plotly** — EDA charts
- **Power BI Desktop** — Stakeholder dashboard
### DevOps & Workflow
- **Git & GitHub** — Version control
- **MLflow** — Experiment tracking
---
 
## 🗺️ Project Workflow
 
```
Business Problem Definition
        ↓
Data Acquisition (Kaggle)
        ↓
Data Profiling & Quality Check  ← notebook 01
        ↓
Exploratory Data Analysis       ← notebook 02
        ↓
Feature Engineering             ← notebook 03
        ↓
Model Building & Evaluation     ← notebook 04
        ↓
SHAP Explainability             ← notebook 05
        ↓
Power BI Dashboard
        ↓
Business Recommendation Report
```
 ## 📈 Power BI Dashboard Pages
 
| Page | Content |
|---|---|
| **Executive Summary** | Churn rate KPIs, revenue at risk, trend lines |
| **Churn Risk Segmentation** | CLV vs churn probability scatter, treemap by segment |
| **Behavioral Deep Dive** | Usage patterns, support tickets, payment failures |
| **Model Predictions** | Top 500 high-risk customers with churn scores |
| **Retention Tracking** | Campaign ROI, intervention success rate |
---

## ⚠️ Real-World Challenges Addressed
 
**Class Imbalance** — Only 26.5% of customers churn. Handled using SMOTE oversampling and evaluated using AUC-ROC and F1-score instead of raw accuracy.
 
**Hidden Data Quality Issues** — `TotalCharges` column stored as string type despite being numerical, containing 11 hidden null values missed by standard checks.
 
**Feature Engineering** — Raw columns alone are insufficient. New features created include usage trends, support ticket frequency, and price sensitivity scores.
 
**Temporal Validation** — Data split by time (not randomly) to simulate real production model validation.
 
**Business Explainability** — SHAP values used to explain every prediction in plain business language, not just model scores.

---
 
## 🚀 How to Run This Project
 
### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/telecom-churn-prediction.git
cd telecom-churn-prediction
```
### 2. Create virtual environment
```bash
python -m venv venv
venv\Scripts\activate       # Windows
source venv/bin/activate    # Mac/Linux
```
 
