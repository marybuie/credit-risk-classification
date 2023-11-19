# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

The purpose of this analysis was the develop a machine learning model for credit risk assessment. Credit risk assessment is the process of determining the probability that a borrower will default on a payment. The data in this dataset is fictional and was created for educational purposes, but the columns in the csv were as follows:

loan_size,interest_rate,borrower_income,debt_to_income,num_of_accounts,derogatory_marks,total_debt,loan_status

Information in the csv pertained to loan size, interest rate, borrower income, etc. Though the data was fictional, this is all information that would be necessary in a real credit risk assessment.

Essentially, we were trying to predict which loans were high-risk (high likelihood of defaulting), and which loans were healthy (little to no risk of default). To accomplish this, we analyzed the binary variable 'loan_status.' The 'value_counts' for this variable contain the information we need pertaining to the distribution of healthy and high-risk loans.

Stages of machine learning process:
1. Data prep: I loaded the dataset and explored the basic stats
2. Splitting data: I divdied the dataset into training and testing sets to train the model on one subset and evalute its performance on another.
3. Building a logistic regression model: I used a logistic regression model to predict loan status.
4. Model evaluation: I assesed the model's performance using confusion matrices and classification reports, which provided the values for accuracy, precision, recall, and f1-scores.
5. Resampling: I used random oversampling to enhance the model performance.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
• Balanced Accuracy: 0.9520479254722232, or 95%
• Precision 0: 100%
• Precision 1: 85%
• Recall 0: 99%
• Recall 1: 91%


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
• Balanced Accuracy: 0.9936781215845847, or 99%
• Precision 0: 100%
• Precision 1: 84% 
• Recall 0: 99%
• Recall 1: 99%
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

Both models exhibited strong performance, but the resampled model performed slightly better. The original model achieved an overall accuracy of 99%, with high precision, recall, and F1-score for both the healthy and the high-risk loans. The balanced accuracy was 95.2%. The resampled model was equally as accurate overall. However, and this is crucial for our assessment, the balanced accuracy increased to 99%. Resampling helped address imbalances in the dataset, which in turn allowed us to better capture patterns related to high-risk loans. It's more important to predict the high-risk loans (the 1's) than the healthy ones, since the point of this particular assessment is cost-avoidance (we want to avoid defaults). If we were trying  to predict the healthy loans (the 0's), either model would work.