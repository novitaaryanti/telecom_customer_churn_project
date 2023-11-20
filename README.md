# Telecom Customer Churn Project
Machine learning implementation in R for binary classification.



## A. Background
The Telecom Customer Churn Project is a basic implementation of binary classification using machine learning models in R. The goal is to do binary classification to predict the churn of the telecom company. This prediction is useful to see the percentage of customers to discontinue using telecom services. If the customer is labelled as churn, then the customer is likely to stop using the service.



## B. Objectives
This project is the implementation of training and predicting binary classes using Random Forest and Regularized Logistic Regression.



## C. Dataset
The dataset used for this dataset is obtained from the UC Irvine Machine Learning Repository named __[Iranian Churn Dataset](https://archive.ics.uci.edu/dataset/563/iranian+churn+dataset)__. 
- **Call  Failure**: number of call failures
- **Complains**: binary categorical where 0 = no complaint and 1 = complaint
- **Subscription  Length**: total months of subscription
- **Charge  Amount** = ordinal attribute in range 0 to 9 where 0 = lowest amount and 9 = highest amount
- **Seconds of Use** = total seconds of calls
- **Frequency of use** = total number of of calls 
- **Frequency of SMS** = total number of text messages
- **Distinct Called Numbers** = total number of distinct phone calls
- **Age Group** = ordinal attribute in range 1 to 5 where 1 = younger age and 5 = older age
- **Tariff Plan** = binary categorical where 1 = pay as you go and 2 = contractual
- **Status** = binary categorical where 1 = active and 2 = non-active
- **Age** = actual age of the customer
- **Customer Value** = calculated value of customer
- **Churn** = binary categorical where 1 = churn and 0 = non-churn



## D. Model Evaluation
The model used for this project is Random Forest and Regularized Logistic Regression. By doing 5-fold cross-validation, the best parameters for those models are:
1. Random Forest
   - mtry = 2
2. Regularized Logistic Regression
   - cost = 0.5
   - loss = L1
   - epsilon = 0.001

The ROC from the models using those best parameters and the balanced accuracy from the prediction performance: 
| Metrics           	| Random Forest 	| Regularized Logistic Regression 	|
|-------------------	|---------------	|---------------------------------	|
| ROC               	| 0.9583140     	| 0.9135615                       	|
| Balanced Accuracy 	| 0.8343        	| 0.72263                         	|

It appears that Random Forest performs better than Regularized Logistic Regression.



## E. Conclusion
From the result, it is found that Random Forest gives better performance compared to Regularized Logistic Regression based on the ROC = 0.9583140 and balanced accuracy = 0.8343. The best parameter for the Random Forest model on this dataset based on the ROC is using 2 features to consider at each split point (mtry).

## F. Further Work
This project can still be improved for better results by doing hyperparameter tuning or using other models. This project can also be made into a simple program or application so that other users can perform the prediction in a more friendly interface.
