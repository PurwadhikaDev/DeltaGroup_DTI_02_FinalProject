# DeltaGroup_DTI_02_FinalProject

# Telco Customer Churn Prediction

Hello everyone!

Welcome to the Telco Customer Churn Analysis project! 🚀 In this project, we dive deep into customer data to identify churn patterns and develop a machine learning model that predicts at-risk customers. These insights help telecom companies optimize retention strategies, reduce churn, and enhance customer loyalty. Join us as we explore how data can keep customers connected! 📊📡

## Related Links
- [Tableau Link](https://public.tableau.com/app/profile/fine.oktafiani/viz/TELCOPREDICTSTORY/Story1?publish=yes)
- [Raw Dataset: Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- [Cleaned Dataset: Telco Customer Churn](https://github.com/PurwadhikaDev/DeltaGroup_DTI_02_FinalProject/blob/main/Cleaned_Dataset%20TelcoCustomerChurn.csv)
- [Predicted Dataset: Telco Customer Churn](https://github.com/PurwadhikaDev/DeltaGroup_DTI_02_FinalProject/blob/main/Predicted_Dataset_TelcoCustomerChurn.csv)
- [Pipeline Best Model(.sav)](https://github.com/PurwadhikaDev/DeltaGroup_DTI_02_FinalProject/blob/main/final_pipeline_DeltaGroup_DTI_02.sav)
- [Workbook.ipynb](https://github.com/PurwadhikaDev/DeltaGroup_DTI_02_FinalProject/blob/main/DeltaGroup_DTI_02_FinalProject_TelcoCustomerChurn.ipynb)

## Project Overview
Telecommunication companies face challenges in retaining their subscribed customers. In this project, we build a Machine Learning model to predict customer churn based on demographic data, customer account information, and service usage. According to Harvard Business Review, acquiring a new customer can be 10-25 times more expensive than retaining an existing one. Therefore, this project aims to reduce churn rates through a data-driven strategy ([Source](https://hbr.org/2014/10/the-value-of-keeping-the-right-customers))

## Business Understanding
The business objectives of this project are:
- Identify customer churn patterns based on given data.
- Analyze the factors that contribute to churn .
- Determine the best Machine Learning model for churn prediction.
- Reduce False Negatives in churn prediction to retain more customers.
- Help the marketing team create more effective customer retention strategies.

### Stakeholder:
With the available churn data, the marketing team aims to accurately identify churn patterns to optimize retention costs and develop targeted strategies for different customer segments to enhance customer retention.. additionally, this data will be further used by sales, customer service, and product team for product development and improving customer experience.

## Analytical Approach
Our approach focuses on analyzing customer data to identify patterns that differentiate churned customers from retained ones. By developing a classification model, we aim to predict churn probability, allowing the company to optimize retention efforts and reduce marketing costs by targeting the right customers efficiently.

## Evaluation Metrics
Since the primary focus is churn reduction, we use F2-score as the main metric, which emphasizes Recall over Precision.
Other metrics used:
 - Accuracy: Measures overall model correctness.
 - Precision: Important if retention intervention costs are high.
 - Recall: Ensures that as many churn customers as possible are detected.
 - F1-score: A balance between Precision & Recall, although in this study, F2-score is prioritized.
 - ROC-AUC score: distinguishing between customers who will churn and those who will stay
 - Average Precision (AP) score: easures the area under the Precision-Recall curve, summarizing model ranking performance. Higher AP (closer to 1) indicates better classification, especially for imbalanced data.

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

### Data Cleaning
- Check Data Types – Ensure each column has the correct data type for analysis.
- Descriptive Statistics – Summarize key metrics to understand raw data distribution.
- Check Unique Values – Identify categorical inconsistencies or anomalies.
- Check Duplicates – Eliminate redundant entries to maintain data integrity.
- Handle Missing Values – Impute or remove missing data for consistency.
- Detect Outliers – Identify and address extreme values affecting model performance.
- Analyze Numerical Distributions – Understand feature distribution for proper scaling.
- Check Multicollinearity – Detect highly correlated features to avoid redundancy.

## Exploratory Data Analysis (EDA)
- Churn ditribution
- Customer Account info with numerical variable
- Customer Account info with categorial variable
- Correlation analysis

## Machine Learning Approach
The modeling process involves:
1. Data Preprocessing: Data cleaning, handling missing values, encoding categorical variables.
2. Handling Class Imbalance: Using Borderline SMOTE oversampling to balance the dataset.
3. Benchmarking Models: Testing various algorithms like Logistic Regression, Random Forest, XGBoost, decision tree, LGBM, K-Nearest Neighbors.
4. Hyperparameter Tuning: use Grid search for finding the best parameters to tune the model.
5. Threshold Analysis: finding the best threshold to get the best F2 score.
6. Model Evaluation: Using appropriate metrics for churn prediction.

## Conclusion
### Conclusion for Business
1. key customer profiles related to churn:
- Gender: Churn rates show minimal differences across genders, ranging from 26-27%.
- Generation: Older customers have a higher churn rate (41.7%) compared to younger customers.
- Marital Status: Customers without a partner are more likely to churn compared to those with a partner.
- Dependents: Customers without family dependents are more likely to churn (31.3%) than those with dependents.

2.  Top factors contribute to churn
- Contract: Shorter contracts are more likely to result in churn. Customer with 'Month-to-month' contract is more likely to churn (42.7%), compared to 'one year contract' (11.3%) and 'two year contract' (2.8%)
- Monthly Charges: low monthly charges are more likely lead to churn. customer who spend monthly charges less than $67.2 are at high churn risk.
- Tenure: Newer customers are at higher risk of churning. Customers with 1-5 month tenure contribute to 40% (744 out of 1866) of total tenure.
- Internet Service: Fiber optic users tend to churn more, contributing around 41.9% of customer churn compared to another internet service.
- paperless Billing: customers with paperless billing tend to churn (33.6 % churn rate)

### Conclusion for Model
1. Best Machine Learning model:
Based on our analysis, the best model for predicting churn is **Logistic Regression with Borderline SMOTE oversampling**, using the following parameters:
- C: 10
- Penalty: I1
- Solver: saga
- Class weight: balanced
- Threshold: 0.43

This model achieves an F2 score of 0.75 and a recall score of 90%, meaning it can effectively predict 90% customers who are likely to churn.

2. Marketing Cost Optimization using the model
- **Without Model:** Out of 7,043 customers, 26.5% (1,866) are projected to churn, requiring acquisition efforts, while the remaining 5,177 customers fall under retention strategies. The total cost incurred without intervention is $424,970, consisting of $373,200 for acquisition and $51,770 for retention.
- **With Model:** With a recall of 90%, the model correctly identifies 1,679 out of 1,866 churners that require targeted retention efforts, while 187 churners are missed and require acquisition. The total cost incurred with the model is $173,120, consisting of $51,770 for retaining non-churners, $83,950 for preventing churn among identified customers, and $37,400 for acquiring new customers to replace those missed by the model.
- **Summary:** By implementing the model, the total cost was significantly reduced from $424,970 to $173,120. This resulted in savings of $251,850, demonstrating the model's effectiveness in optimizing costs.

3. Model Trustworthy:
maintains a balance between recall and F2-score across training and test sets. Specifically, the recall for class 1 is 88.58% (train) vs. 90.10% (test), and the F2-score is 74.59% (train) vs. 75.02% (test). Since the differences are minimal (+1.52% recall and +0.43% F2-score on test data), there is no significant drop in performance. This consistency indicates good generalization, making the model reliable for real-world use.

4. Model Limitation:
  - **Data imbalance in the Churn group.**
  Currently, data imbalance is addressed through data engineering. However, this approach still carries the risk of errors and is not as effective as having a naturally balanced dataset.
  
  - **Features limitation**
  The model predicts customer churn based on the following features: **gender, SeniorCitizen, Partner, Dependents, tenure, PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies, Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges.** If new features are added to the dataset, the model will not be able to account for their impact on churn prediction, requiring retraining data.
  
  - **Features range limitation.**
  The churn prediction model is trained on the following value ranges for each feature:
    - gender = Male, Female
    - senior_citizen = No, Yes
    - partner = No, Yes
    - dependents = No, Yes
    - tenure = 0 - 72 months
    - phone_service = Yes, No
    - multiple_lines = No, Yes, No phone service
    - internet_service = Fiber optic, DSL, No
    - online_security = No, Yes, No internet service
    - online_backup = No, Yes, No internet service
    - device_protection = No, Yes, No internet service
    - tech_support = No, Yes, No internet service
    - streaming_tv = No, Yes, No internet service
    - streaming_movies = No, Yes, No internet service
    - contract = Month-to-month, One year, Two year
    - paperless_billing = Yes, No
    - payment_method = Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic)
    - monthly_charges = 19.85 - 114.70
    - total_charges = 19.65 - 6849.40

If new data contains values outside these ranges, the model may still make predictions, but their accuracy and reliability are uncertain. To ensure accurate predictions, the model should be retrained with updated data that includes the new value ranges


## Recommendation

### Recommendation for Business
Here are the prioritized strategies for business improvement to prevent customer churn:
- **Increase Contract Retention**: Offer a 10-15% discount or free service upgrades for customers who switch from month-to-month to one- or two-year contracts.
- **Bonus for High Spender**: Customers who spend more than the monthly charges average can get additional service bonuses.
- **Improve New Customer Retention**: Implement a personalized onboarding program (emails, tutorials, or dedicated support calls) targeting customers within their first 5 months.
- **Enhance Fiber Optic Service Experience**: Offer a 20% discount on the first 5 months of online security, backup, or tech support for customers with fiber optic service. Conduct customer satisfaction surveys specifically for fiber optic users, identifying key issues related to performance, pricing, or support for improvements.
- **Optimize Paperless Billing Experience**: Introduce payment reminder emails or provide dedicated customer service to call for reminders.

### Recommendation for Model

  - **Balance the dataset**: We can try to use other resampling techniques and collect more real-world data to balance the dataset. This is useful for improving model reliability and reducing bias.
  - **Expand feature set**: If we add new features, we can regularly analyze and add new features, ensuring the model captures all relevant factors influencing churn.
  - **Update model for new data**: Try to re-train the model periodically when we have new features or value ranges to maintain prediction accuracy.
  - **Adjust parameter range**: Currently, we are using the maximum 10 for C parameters. We can try to broaden the range to get better results.
  - **Add more relevant features**: For example, currently, we don't have an 'age' feature, so it's quite difficult to distinguish between senior citizens and non-senior citizens for future data. Adding such features can improve model performance.


### Tableau Dashboard
![image](https://github.com/user-attachments/assets/14d5100b-f6dd-4bc1-80e9-cf7a899ca007)

