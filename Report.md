<div style="font-family:Georgia;background-color:black; padding:30px; font-size:17px">

#  Loan Default Project Report

In today’s world, obtaining loans from financial institutions has become a very common phenomenon. Every day many people apply for loans, for a variety of purposes. But not all the applicants are reliable, and not everyone can be approved. Every year, there are cases where people do not repay the bulk of the loan amount to the Financial Institutions which results in huge financial loss. The risk associated with making a decision on a loan approval is immense. Hence, the idea of this challenge is to use the financial data provided and use machine learning techniques on this data to extract important information and predict if a customer would be able to repay the loan or not. In other words, the goal is to predict if the customer would be a defaulter or not.<br>

 ## Dataset
 The Dataset contained 6 features and 58 entries.
> * **Customer ID:** This feature indicates the Id of each customer.
> * **Annual income:** The self-reported annual income provided by the customer during registration. 
> * **Credit score:** This is  a prediction of your credit behavior, such as how likely you are to pay a loan back on time, based on information from your credit reports.
> * **Employment length:** This feature indicates employment length in years and months.
> * **Debt-to-income-ratio:** Asuuming this is a ratio calculated using the customers’s total debt, divided by the customers’s self-reported income.
> * **Loan default:**  binary indicator of whether the customer defaulted. **0 means Not- Defaulted** & **1 means Defaulted**
  
 ## Data Cleaning
  The data cleaning was executed in the following way:
  > * Checked for the data type and information of each column
  > * Checked for duplicates in the dataset
  > * Checked for percentage of null values in the dataset: 
  
    Annual income:1.72%; 
  
    Employment length:1.72%; 
  
    Debt-to-income ratio:1.72%; 
  
    Loan default:1.72%
  
  > * Described a function to:
  
     i. Drop the Customer ID column
     ii. Filled in missing values in the Age column and Employment lenght using .fillna().mode()
     iii. Filled in missing values in the Debt-to-income ratio and Loan Default column using .fillna.median()
  
  ## Exploratory Data Analysis
  > * Decided the Target Variable which is - Loan Default and visualized the distribution of Loan Defaulters with 29.3% of the customers defaulted their loans.
  > * The customers with Annual Incme greater than $60,000, were less likely to default their loans.
  > * More than 25% of the customers earned less than $45,000 Annually.
  > * Customers with a credit score higher than 650 were less likely to default on their loans.
  > * More than 29% of the customers had a credit score lower than 650.
  > * Visualized the Employent lenght distribution and found that 27.58% of the customers have been at their current job for 1 year or less.
  > * Customers who have been at their current job for less than 2 years were most likely to default on their loans.
  > * All the customers with 6 months of employment defaulted on their loans.
  
  ## Data Preprocessing
  The features had kind of a normal distribution with little to no skewness but was highly unbalanced.
  #### Correlation Analysis
  Correlation analysis was used to analyse the degree to which the variables were related to each other, where the relationship could be either positive or negative.
  #### Balancing the Dataset
  There was class imbalance, using SMOTE, which is an oversampling technique to generate synthetic samples of the minority class to balance the class distribution.
  ## Modelling
  
  #### Model function for the raw dataset (Unscaled Data)
  Usually, some algorithms require standardized or transformed data to achieve better results. I tested different techniques to see how well the models perform on data.

First, I tested the performance on the "raw" data, by using them in the original format.
  > * **Logistic Regression Model**: The logistic regression model correctly predicted 83.34% of the loans to be Defaulted or Not Defaulted.Auc-Roc score =88.46%
  > * **Decision Tree Classifier Model**: This model correctly predicted 88.89% of the loans to be defaulted or not defaulted. Auc-Roc Score = 92.31%
  > * **Random Forest Classifier Model**: The Random Forest Classifier model correctly predicted 94.45% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 96.15%
  > * **AdaBoost Classifier Model**: The Ada Boost Classifier model correctly predicted 88.89% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 92.31%
  > * **Gradient Boost Classifier Model**:The Gradient Boost Classifier model correctly predicted 94.45% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 96.15%
  > * **XG Boost Model**:The XGBoost Classifier model correctly predicted 88.89% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 92.31%
  > * **LGBM Model**: The LGBM model correctly predicted 88.89% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 92.31%
  > * **CatBoost Model**: The CatBoost Classifier model correctly predicted 94.45% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 96.15%
  #### Model function for the Scaled Data 
  This was done to see if there would be any improvements in the performance of each of the models.
  > * **Logistic Regression Model**: The Scaled Logistic Regression model correctly predicted 100% of the loans to be Defaulted or Not Defaulted. Auc-Roc score =100%
  > * **Decision Tree Classifier Model**: This model correctly predicted 100% of the loans to be defaulted or not defaulted. Auc-Roc Score = 100%
  > * **Random Forest Classifier Model**: The Random Forest Classifier model correctly predicted 94.45% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 96.15%
  > * **AdaBoost Classifier Model**: The Ada Boost Classifier model correctly predicted 100% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 100%
  > * **Gradient Boost Classifier Model**:The Gradient Boost Classifier model correctly predicted 94.45% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 96.15%
  > * **XG Boost Model**:The XGBoost Classifier model correctly predicted 88.89% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 92.31%
  > * **LGBM Model**: The LGBM model correctly predicted 88.89% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 92.31%
  > * **CatBoost Model**: The CatBoost Classifier model correctly predicted 94.45% of the loans to be Defaulted or Not Defaulted. Auc-Roc score = 96.15%
  
### Stacking some of the Classifier models to achieve better performance
  
  
  
  
  
  
</div>

