# Blocker Fraud Company project

This project contains the solution for this business case: https://bit.ly/34V6Wpw

The business case uses dataset from this kaggle webpage: https://www.kaggle.com/ntnu-testimon/paysim1

To not clog the notebook, it has the been divided in 4 parts:

## Part1:
in this part I sampled the data to reduce computational cost and completed the analysis until Exploratory Data Analysis (EDA) and feature engineering. Note the interest choice to cap the outliers and use logarithmic transformation on the continuous data.
## Part2:
Realizing that fraud only happens with transfer types Transfer and Cash_out, I eliminated every sample containing other types of transfer and repeated the steps of part 1 to see what changes with data sampled this way. 
## Part3:
This part is focused on selecting the best Machine Learning model. I tried several models and undersampling techniques. Surprisingly undersample didnt show a significant increase in accuracy. The best model was random forest with data unbalanced. After selecting the best model I tuned it with random search techniques. Note that I don't have computational resource to conduct this part without sampling this dataset.
## Part4:
Finally with the final model chosen and tuned, I used it on the full dataset. The model had the following performance:

**Final result:**
* Balanced Accuracy: 0.998765
* F1Score: 0.998764
* KappaScore: 0.998762

Resulting in the following **business performance:**

* With client's total amount of transactions of \\$229,409,295,522.24, the company's total profit is $555,956,368.86.
* This means the fraud company's relative profit for each \\$100 of transaction from client is \\$0.24

## Some mistakes and future improvements:
* I mistakengly mixed portuguese and english in this project. At this point the project is too long and I and too busy to change this, I hope the reader doesnt mind.
* Although I was very careful to not make data likage mistakes, a more correct form of conducting this project would be to isolate a test dataset from the very start.

# The Business Challenge
The Blocker Fraud Company: 
* Financial transactions' fraud detection specialized company. 
* The Blocker Fraud service ensures fraudulent transactions block.

Business Model: 
* service's performance monetization.

Expansion Strategy in Brazil:
* The company receives 25% of each transaction value truly detected as fraud.
* The company gives back 5% of each transaction value detected as fraud, however the transaction is legitimate.
* The company gives back 100% of the value for the customer in each transaction detected as legitimate, however the transaction is actually a fraud.

Goal:

* Create a model with high accuracy and precision with respect to transactions' fraud detection.

The following questions must be answered:

* What is the model's precision and accuracy?
* What is the model's reliability with respect to transactions' classification as legitimate or fraudulent?
* What is the company's forecasted revenue if the model classifies 100% of the transactions?
* What is the company's forecasted loss in case of model's failure?What is the Blocker Fraud Company forecasted profit using the model?
