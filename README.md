# Give_me_some_credit
📌 **Project Overview**

This project analyzes the "Give Me Some Credit" dataset
"https://www.kaggle.com/datasets/brycecf/give-me-some-credit-dataset",

a financial dataset used to assess credit risk. The goal is to build insights and tools that help predict whether an individual will experience financial 

distress within the next two years.

Banks use credit scoring models like this one to make informed decisions about lending. By analyzing financial behaviors and demographic indicators, we can 
better understand patterns of default risk.



🧾 **Dataset Description**
Each record represents an individual consumer and includes features related to their credit usage, payment history, income, and demographics       

SeriousDlqin2yrs: Target variable. 1 = default in 2 years, 0 = no default

RevolvingUtilizationOfUnsecuredLines: Ratio of used credit to total credit available

Age: Age of the individual

NumberOfTime30-59DaysPastDueNotWorse: Past due payments (30-59 days)

DebtRatio: Total monthly debt / gross monthly income

MonthlyIncome: Monthly income of the individual

NumberOfOpenCreditLinesAndLoans: Number of open credit lines and loans

NumberOfTimes90DaysLate: Number of times payment was over 90 days late

NumberRealEstateLoansOrLines: Number of real estate loans/lines

NumberOfTime60-89DaysPastDueNotWorse: Past due payments (60-89 days)

NumberOfDependents: Number of dependents the individual has

🔍 **Objectives**

Clean and prepare the dataset using BigQuery SQL:
using some function to clean the data 
**1-COALESCE(MonthlyIncome, median_income_by_age_group) AS MonthlyIncome**

I used this function to replace the MonthelyIncome **NULL** values by median income by age group.

**2-ROW_NUMBER() OVER (PARTITION BY>>>>>>>>>>>>**

I used this function remove duplicate.

**3-Handle Invalid or Outlier Values**
 Negative or zero ages:
Explore relationships between features and default risk

Visualize insights using dashboards

Optionally build a predictive model for default classification

🛠 **Tools Used**

Google BigQuery (SQL-based analysis & feature engineering)

Tableau for dashboards

📊 **Key Insights**

Default rates are higher among younger consumers (under 30)

High DebtRatio and RevolvingUtilizationOfUnsecuredLines correlate with financial distress

Income and payment history are critical predictors of risk


