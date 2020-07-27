
# Module 3 Final Project: Customer Churn with Telco Data Set


For this project I will be predicting Customer Churn using the Telco Customer Churn Data Set. This data set is available through Kaggle and also in this repo. 

https://www.kaggle.com/blastchar/telco-customer-churn

Churn is defined as the percentage of customers who's business you lost during a set period of time. It can be calculated by dividing the amount of customers lost by the total number of customers you had at the beginning of this time frame.

If you were trying to calculate churn for this data set, the churn percentage can be said to be 26.6% for this time frame. As no dates are available in this data set, we cannot say what time frame this churn rate occured over.

<img href='/figures/churn_yes_no.png' >

<b>The goal of this project is to identify the most predictive features that lead customers to churn and provide business recommendations for how to reduce the number of customers who churn. <b>

I will be using the OSEMN approach in this project, which follows the process outlined below:

* Obtain the data
* Scrub the data to remove outliers and prepare it for modeling
* Explore data with visualizations to look for predictive behaviour
* Model data using Machine Learning methods and tune models to maximize predictive power
* Interpret findings and present to stakeholders

# Evaluation Metrics- Recall and F Beta Score

I ran 4 different models (Logistic Regresion, Random Forest, Support Vector Machine, and Gradient Boosted Random Forest) and recorded the results of each model run below. 


<b>After plotting the evaluation metrics for the models that I ran for this project, I have concluded that the Random Forest Model was the most effective model for predicting churn in this data set. It was able to predict churn using customer data up to 80% effectively

While there were other models that had higher Train/Test Recall Scores (the Support Vector Machines) they were worse at predicting one of the classes in the data set. Also, the Gradient Boosted model performed about as well as the Random Forest model, but it was harder and more computationally and time consuming than the Random Forest Model

# Findings and Conclusion

Across all models the most important predictors for customer churn ended up being Tenure (how long the customer had been at the company), Contract (whether the customer was under a 1 or 2 year contract), and if they are signed up Fiber Optic Internet Service. 

1) <b>The longer the customer has been with the company the less likely they will be to churn
  
2. <b>If the customer is under a long term (1 or 2 year) contract, they are less likely to churn
  
3. <b>If the customer is signed up for Fiber Optic Internet, they are more likely to churn
  
# Business Recommendations

<b>Given this data by a company looking for an insight into why their customers keep churning, I would make the following recommendations. 

1) Invest in a Customer Success department built on keeping your customers in their first year of business happy

    - This is where the most churn is occuring so focus your staff on plugging this leak first
    
2) Train your sales team to focus on signing new customers to 1 or 2 year contracts. Offer incentives or roll other services into a bundle that a customer can only get when they sign up for a 1 or 2 year contract.

3) Bundle technical support into the fiber optic internet service tier. There is clearly a disconnect between what should be a faster, more reliable internet service and what is right now a service that is driving away customers. 
