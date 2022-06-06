# <p align = 'center'>Customer Lifetime Value Prediction</p>

## BUSINESS PROBLEM
An Auto Insurance company in the USA is facing issues in retaining its customers and wants to advertise promotional offers for its loyal customers. They are considering Customer Lifetime Value CLV as a parameter for this purpose. Customer Lifetime Value represents a customer’s value to a company over a period of time. It’s a competitive market for insurance companies, and the insurance premium isn’t the only determining factor in a customer’s decisions. 

CLV is a customer-centric metric, and a powerful base to build upon to retain valuable customers, increase revenue from less valuable customers, and improve the customer experience overall. Using CLV effectively can improve customer acquisition and customer retention, prevent churn, help the company to plan its marketing budget, measure the performance of their ads in more detail, and much more.

## PROJECT OVERVIEW

- The objective of the problem is to accurately predict the Customer Lifetime Value(CLV) of the customer for an Auto Insurance Company
- Performed EDA to understand the relation of target variable CLV with the other features.
- Statistical Analysis techniques like OLS for numerical and Mann–Whitney U and also Kruskal Wallis test for the categorical variables were performed to find the significance of the features with respect to the target.
- Supervised Regression Models like Linear Regression, Ridge Regression, Lasso Regression, DecisionTree Regression, Random Forest Regression and Adaboost Regression.
- Using GridSearchCV with Random Forest Regression gave the best RMSE and R^2 score values

## DATA DESCRIPTION

The dataset represents Customer lifetime value of an Auto Insurance Company in the United States, it includes over 24 features and 9134 records to analyze the lifetime value of Customer.

The dataset was collected from kaggle - https://www.kaggle.com/datasets/ranja7/vehicle-insurance-customer-data

## EXPLORATORY DATA ANALYSIS RESULTS (EDA)

`Univariate`, `Bivariate` and `Multivariate` Analysis were performed to bring out important aspects of data into focus for further analysis. Some of the highlights from EDA are listed below.

### 1. Univariate Analysis
![CLV](/Images/CLV.png "Customer Lifetime Value")
- CLV is heavily right skewed in the data

![location](/Images/location.png "Location")
- Most of the customers are from the suburban region

### 2. Bivariate Analysis
![Bivariate Analysis](/Images/bi.png "Bivariate Analysis of CLV and Monthly Premium")
- CLV and Monthly premium auto have a positive correlation and there is a linear relationship between them.

### 3. Multivariate Analysis
![Heatmap](/Images/Heatmap.png "Heatmap")
- There is a positive correlation between CLV and the monthly premium auto
- There is a slight positive correlation between the total claim amount and CLV.
- Income has a lesser positive correlation with CLV

## SUPERVISED MACHINE LEARNING MODEL

| Model      | R^2 Score | RMSE |
| ----------- | ----------- | ----------- |
| Adaboost Regression |0.89|0.2181 |
| Lasso Regression |  0.19    |0.5992|
| DecisionTree Regression | 0.84 |  0.2668 |
| RandomForest Regression | 0.90 | 0.2047 |
| Linear Regression      | 0.25       |0.5772|
| Ridge Regression   | 0.21        |0.5925|
| RandomForest with GridSearchCV | 0.91 | 0.1956 |

## EVALUATION METRICS

- RMSE and R^2 score were chosen as the metric for the models.

## FINAL MODEL

By comparing RMSE and R^2 score results of models and then we choose the best model as the Random Forest with GridSearchCV, having the best evaluation scores.

## COMCLUSION

1. Overall we can see that No of policies, Monthly Premium auto, Total Claim amount, Months Since Policy Inception, Income, Months Since Last Claim, Number of Open Complaints, Coverage_Extended EmploymentStatus_Employed and Renew Offer Type_Offer2 are the important features in predicting the Customer Lifetime Value (CLV).
2. The customers having more number of policies with high monthly premium will add more value to company.
3. Ironically being an auto insurance company, the type of vehicle or size does not have an impact on the CLV prediction.
4. The insurance agents should start increasing their policy advertisement for the customers who have more no. of policies, which is the major feature in predicting the CLV.
