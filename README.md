# Lab 4: Churn Risk Advisor — From Notebook to Product

## Project Overview

This project is part of **Introduction to Applied AI — Lab 4**. It converts a machine learning customer churn prediction model into a web application using **Streamlit**.

The application predicts the probability that a telecom customer may leave the service and provides a risk category to help prioritize customer retention efforts.

## Objectives

- Load and use a previously trained machine learning model.
- Build a web application using Streamlit.
- Predict customer churn probability from customer details.
- Categorize customers into Low, Watch, and High risk bands.
- Compare predictions under different customer scenarios.
- Upload a CSV file to score multiple customers.
- Download the results of batch predictions.
- Present model information and limitations.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Joblib
- Streamlit
- Git and GitHub

## Repository Structure

```text
churn-risk-advisor/
│
├── app.py
├── churn_model.joblib
├── model_meta.json
├── sample_customers.csv
├── requirements.txt
├── README.md
└── .gitignore
```

## Application Features

### 1. Customer Profile

Users can enter customer details such as tenure, contract type, monthly charges, internet service, payment method, and other service options.

### 2. Churn Probability

The application uses the trained model to estimate a customer's churn probability.

### 3. Risk Classification

Customers are classified into risk bands based on the selected contact threshold:

- **High:** Probability is at or above the contact threshold.
- **Watch:** Probability is below the threshold but at least half of it.
- **Low:** Probability is below half of the threshold.

### 4. What-If Analysis

Users can explore how the model's prediction changes when selected customer features are changed, such as contract type or payment method.

These comparisons show model associations and do not establish that changing a feature will cause a customer to stay.

### 5. Batch Customer Scoring

Users can upload a CSV file containing the required customer columns. The application calculates churn probabilities and allows the scored data to be downloaded as a CSV file.

### 6. Model Information

The About tab displays available model metadata and explains important limitations.

## Dataset

The project uses the IBM Telco Customer Churn dataset from the earlier coursework notebook.

The dataset contains telecom customer information, service details, billing information, and churn outcomes.

## Installation and Setup

### Prerequisites

- Python 3.11 recommended
- Git
- A GitHub account

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/churn-risk-advisor.git
cd churn-risk-advisor
```

Replace `YOUR-USERNAME` with your GitHub username.

### Step 2: Create a Virtual Environment

On Windows:

```bat
python -m venv .venv
.venv\Scripts\activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

Make sure `requirements.txt` pins the same scikit-learn version used to save the trained model.

### Step 4: Run the Application

```bash
streamlit run app.py
```

Open the local URL shown in the terminal, usually:

`http://localhost:8501`

## Required Files

- `app.py` — Streamlit application.
- `churn_model.joblib` — Trained machine learning model.
- `model_meta.json` — Model metadata, feature columns, and threshold information.
- `sample_customers.csv` — Sample customer records for batch scoring.
- `requirements.txt` — Python dependencies.

## Model Evaluation

Model evaluation results should be reported using the actual values from the previous coursework notebook and `model_meta.json`.

- Cross-validation AUC mean: **[Insert actual value]**
- Cross-validation AUC standard deviation: **[Insert actual value]**
- Test AUC: **[Insert actual value]**
- Selected contact threshold: **[Insert actual value]**

Do not use example or estimated metrics in place of your actual results.

## Limitations

- The model was developed using a US telecom customer dataset.
- Its performance has not necessarily been validated on customers in Pakistan or other markets.
- Predictions are estimates, not guarantees.
- Feature associations do not prove causation.
- The application is intended to support customer retention prioritization, not to make high-impact decisions automatically.

## Learning Outcomes

Through this lab, I practiced deploying a machine learning model in a user-facing application, preparing input features consistently, implementing individual and batch predictions, exploring what-if scenarios, and organizing a project for GitHub.

## Author

**Maaz Imtiaz**

BS Electronics — Final Year Student

## Academic Context

Introduction to Applied AI — Lab 4: From Notebook to Product, and Presentation 1.

## License

This repository was created for educational and academic purposes.
