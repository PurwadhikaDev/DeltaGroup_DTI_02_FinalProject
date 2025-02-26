# DeltaGroup_DTI_02_FinalProject

# Telco Customer Churn Prediction

## Project Overview
Telecommunication companies face challenges in retaining their subscribed customers. In this project, we build a Machine Learning model to predict customer churn based on demographic data, customer account information, and service usage.
According to Harvard Business Review, acquiring a new customer can be 10-25 times more expensive than retaining an existing one. Therefore, this project aims to reduce churn rates through a data-driven strategy.

## Dataset
The dataset used in this project is Telco Customer Churn, which contains information on:

Customer services booked :
- PhoneService — Whether the customer has a phone service (Yes, No)
- MultipleLines — Whether the customer has multiple lines (Yes, No, No phone service)
- InternetService — Customer’s internet service provider (DSL, Fiber optic, No)
- OnlineSecurity — Whether the customer has online security (Yes, No, No internet service)
- OnlineBackup — Whether the customer has online backup (Yes, No, No internet service)
- DeviceProtection — Whether the customer has device protection (Yes, No, No internet service)
- TechSupport — Whether the customer has tech support (Yes, No, No internet service)
- StreamingTV — Whether the customer has streaming TV (Yes, No, No internet service)
- StreamingMovies — Whether the customer has streaming movies (Yes, No, No internet service)

Customer account information :
- Tenure — Number of months the customer has stayed with the company
- Contract — The contract term of the customer (Month-to-month, One year, Two year)
- PaperlessBilling — Whether the customer has paperless billing (Yes, No)
- PaymentMethod — The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))
- MonthlyCharges — The amount charged to the customer monthly
- TotalCharges — The total amount charged to the customer

Customers demographic info :
- customerID — Customer ID
- Gender — Whether the customer is a male or a female
- SeniorCitizen — Whether the customer is a senior citizen or not (1, 0)
- Partner — Whether the customer has a partner or not (Yes, No)
- Dependents — Whether the customer has dependents or not (Yes, No)
- 
Target :
*   0: Customer won't churn
*   1: Churn will churn

## Business Understanding
The business objectives of this project are:
- Identify customer churn patterns based on given data.
- Analyze the factors that contribute to churn .
- Determine the best Machine Learning model for churn prediction.
- Reduce False Negatives in churn prediction to retain more customers.
- Help the marketing team create more effective customer retention strategies.

### Stakeholder:
With the available churn data, the marketing team aims to accurately identify churn patterns to optimize retention costs and develop targeted strategies for different customer segments to enhance customer retention.. additionally, this data will be further used by sales, customer service, and product team for product development and improving customer experience.

## Machine Learning Approach
The modeling process involves:
1. Data Exploration & Preprocessing: Data cleaning, handling missing values, encoding categorical variables.
2. Handling Class Imbalance: Using Borderline SMOTE oversampling to balance the dataset.
3. Benchmarking Models: Testing various algorithms like Logistic Regression, Random Forest, XGBoost, etc.
4. Model Evaluation: Using appropriate metrics for churn prediction.
