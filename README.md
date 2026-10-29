
# 📦 Invoice Intelligence System

An AI-powered Vendor Invoice Intelligence Portal built with Python, Streamlit, and Machine Learning to estimate freight costs and identify vendor invoices that may require manual approval.


🚀 **[Live Demo](https://invoiceintelligencesystem-vcyspjeusfxypvawvuwyvc.streamlit.app/)** 

## 📑 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Machine Learning Models & Performance](#-Machine-Learning-Models--Performance)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
  - [Clone the Repository](#1-clone-the-repository)
  - [Create a Virtual Environment](#2-create-a-virtual-environment)
  - [Install Dependencies](#3-install-dependencies)
  - [Run the Application](#4-run-the-application)
- [How to Use](#-how-to-use)
- [Business Value](#-business-value)
- [Author](#-author)



## 📌 Overview

Invoice processing involves validating costs, reviewing freight charges, and identifying unusual transactions. This project combines two machine learning prediction modules in a single interactive web application to support invoice review and cost estimation.

## ✨ Features

- **Freight Cost Prediction:** Estimate freight costs based on invoice dollar value.
- **Invoice Risk Flagging:** Predict whether an invoice should be flagged for manual approval using invoice quantity, invoice value, freight cost, total item quantity, and total item value.
- **Interactive Web Interface:** Select a prediction module and enter input values through Streamlit forms.


## 🤖 Machine Learning Models & Performance

The Invoice Intelligence System integrates two machine learning modules: **Freight Cost Prediction** and **Invoice Manual-Approval Flagging**.

### 1. Freight Cost Prediction

**Objective:** Predict freight costs using invoice-related input features.

**Algorithms Evaluated:**
- Linear Regression
- Decision Tree Regression
- Random Forest Regression

#### Model Performance Comparison

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 24.11 | 124.72 | 96.99% |
| Decision Tree Regression | 32.97 | 150.31 | 95.63% |
| Random Forest Regression | 26.13 | 134.79 | 96.48% |

**Best Model: Linear Regression**

Linear Regression was selected as the final freight cost prediction model because it achieved the highest R² score (96.99%) and the lowest MAE (24.11) and RMSE (124.72) among the three evaluated models.

**Evaluation Metrics:**
- **MAE (Mean Absolute Error):** Measures the average absolute difference between actual and predicted freight costs.
- **RMSE (Root Mean Squared Error):** Measures prediction error while penalizing larger errors more heavily.
- **R² Score:** Measures how much of the variation in freight costs is explained by the model.

**Saved Model:** `predict_freight_model.pkl`

### 2. Invoice Manual-Approval Flagging

**Objective:** Classify invoices into two categories to help identify invoices that may require manual review.

**Algorithm:** Random Forest Classifier

#### Overall Model Performance

| Metric | Score |
|---|---:|
| Accuracy | 89% |
| Weighted Precision | 90% |
| Weighted Recall | 89% |
| Weighted F1-Score | 88% |

#### Class-wise Performance

| Metric | Class 0 | Class 1 |
|---|---:|---:|
| Precision | 0.86 | 0.96 |
| Recall | 0.98 | 0.71 |
| F1-Score | 0.92 | 0.81 |
| Support | 725 | 384 |

The Random Forest Classifier achieved **89% accuracy** on the evaluation dataset.

Class 1 achieved **96% precision** and **71% recall**. This means the model performs well when identifying predicted Class 1 cases, but it misses some actual Class 1 cases. If Class 1 represents invoices requiring manual approval, improving recall could help reduce missed reviews.

**Saved Model:** `predict_flag_model.pkl`

### 📊 Model Selection Summary

| Prediction Task | Selected Model | Key Result |
|---|---|---|
| Freight Cost Prediction | Linear Regression | R²: 96.99% |
| Invoice Manual-Approval Flagging | Random Forest Classifier | Accuracy: 89% |

Both models support data-driven invoice processing by estimating freight costs and helping prioritize invoices for review.

**Note:** These metrics reflect the reported evaluation results. Actual performance may vary on new or unseen data.


## 🛠️ Tech Stack

- Python
- Pandas and NumPy
- Scikit-learn
- Streamlit
- Plotly
- Joblib

## 📁 Project Structure

```text
Invoice_Intelligence_System/
├── app.py
├── requirements.txt
├── predict_flag_invoice.pkl
├── predict_freight_model.pkl
├── scaler.pkl
└── inference/
    ├── predict_freight.py
    └── predict_invoice_flag.py
```

The `inference/` folder contains the prediction modules used by the application.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/dhanashrikatkar99/Invoice_Intelligence_System.git
cd Invoice_Intelligence_System
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the application

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal.

## 💻 How to Use

1. Launch the application.
2. Choose a prediction module from the sidebar.
3. Enter the requested invoice details.
4. Submit the form to generate a prediction.
5. Review the estimated freight cost or invoice approval flag.

   Freight Cost Prediction screenshot
   <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/83060ceb-b1aa-4b6c-896d-ff3593da2305" />

   Invoice Manual Approval Flag screenshot
   <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0711da64-127a-480d-9345-5ff0a74cdcb9" />


   

## 💼 Business Value

- Supports freight cost estimation and budgeting.
- Helps prioritize invoices for manual review.
- Can reduce repetitive review effort through data-driven screening.
- Makes machine learning predictions accessible through a simple interface.



## 👩‍💻 Author

**Dhanashri Katkar**

GitHub: [dhanashrikatkar99](https://github.com/dhanashrikatkar99)

