
# 📦 Invoice Intelligence System

An AI-powered Vendor Invoice Intelligence Portal built with Python, Streamlit, and Machine Learning to estimate freight costs and identify vendor invoices that may require manual approval.


🚀 **[Live Demo](https://invoiceintelligencesystem-vcyspjeusfxypvawvuwyvc.streamlit.app/)** 

## 📑 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
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

