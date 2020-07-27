
# Module 3 Final Project: Customer Churn with Telco Data Set


For this project I will be predicting Customer Churn using the Telco Customer Churn Data Set. This data set is available through Kaggle and also in this repo. 

https://www.kaggle.com/blastchar/telco-customer-churn

Churn is defined as the percentage of customers who's business you lost during a set period of time. It can be calculated by dividing the amount of customers lost by the total number of customers you had at the beginning of this time frame.

If you were trying to calculate churn for this data set, the churn percentage can be said to be 26.6% for this time frame. As no dates are available in this data set, we cannot say what time frame this churn rate occured over.

<img src='/figures/churn_yes_no.png' />

<b>The goal of this project is to identify the most predictive features that lead customers to churn and provide business recommendations for how to reduce the number of customers who churn. <b>

I will be using the OSEMN approach in this project, which follows the process outlined below:

* Obtain the data
* Scrub the data to remove outliers and prepare it for modeling
* Explore data with visualizations to look for predictive behaviour
* Model data using Machine Learning methods and tune models to maximize predictive power
* Interpret findings and present to stakeholders

# Evaluation Metrics- Recall and F Beta Score

Given the many model evaulation metrics available to us, I wanted to make sure that I was tuning my model in an appropriate way for this business case. For this reason, I decided to focus on Recall and the F Beta Score.

Recall is an evaluation metric that can be calculated the total number of true positives divided by the number of true positives plus the number of false negatives. Because of the way that this metric is calculated, it rewards tuning models that do not result in False Negatives. For this business case, the model predicting that a customer will not churn and then the customer ends up leaving would be a far more expensive mistake for the business stakeholders than the opposite.

I also included the F Beta Score as an evaluation metric for the model. The F Beta Score is related to the F-1 score in that it measures the harmonic mean between precision and recall in the model. However, the F Beta score includes a paramter called beta that allows the score to be weighted towards precision or recall. Since I am trying to target the recall metric, I have tuned the F Beta score to be more sensitve to the recall score. 

# Model Results

I ran 4 different models (Logistic Regresion, Random Forest, Support Vector Machine, and Gradient Boosted Random Forest) and recorded the results of each model run below. 

<img src='/figures/model_results.png' />

<img src='/figures/model_viz.png' />

<b>After plotting the evaluation metrics for the models that I ran for this project, I have concluded that the Random Forest Model was the most effective model for predicting churn in this data set. It was able to predict churn using customer data up to 80% effectively

While there were other models that had higher Train/Test Recall Scores (the Support Vector Machines) they were worse at predicting one of the classes in the data set. Also, the Gradient Boosted model performed about as well as the Random Forest model, but it was harder and more computationally and time consuming than the Random Forest Model

# Findings and Conclusion

Across all models the most important predictors for customer churn ended up being Tenure (how long the customer had been at the company), Contract (whether the customer was under a 1 or 2 year contract), and if they are signed up Fiber Optic Internet Service. 

1) <b>The longer the customer has been with the company the less likely they will be to churn
    <img src='/figures/tenure_viz.png' />
  
2. <b>If the customer is under a long term (1 or 2 year) contract, they are less likely to churn
    <img src='/figures/churn_viz1.png' />
    <img src='/figures/churn_viz2.png' />
  
3. <b>If the customer is signed up for Fiber Optic Internet, they are more likely to churn
    <img src='/figures/fiber_viz1.png' />
    <img src='/figures/fiber_viz2.png' />
    <img src='/figures/fiber_viz3.png' />
    <img src='/figures/fiber_viz4.png' />
    <img src='/figures/fiber_viz5.png' />
    
  
# Business Recommendations

<b>Given this data by a company looking for an insight into why their customers keep churning, I would make the following recommendations. 

1) Invest in a Customer Success department built on keeping your customers in their first year of business happy

    - This is where the most churn is occuring so focus your staff on plugging this leak first
    
2) Train your sales team to focus on signing new customers to 1 or 2 year contracts. Offer incentives or roll other services into a bundle that a customer can only get when they sign up for a 1 or 2 year contract.

3) Bundle technical support into the fiber optic internet service tier. There is clearly a disconnect between what should be a faster, more reliable internet service and what is right now a service that is driving away customers. 
