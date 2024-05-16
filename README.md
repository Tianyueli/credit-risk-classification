# credit-risk-classification

# Overview of the Analysis
- This project, I used various techniques to train and evaluate a model based on loan risk. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
- The purpose of the model was to predict the loan status of borrowers and whether they are acurractely predicted as healthy or high-risk. 
- The dataset contains key attributes to assist forming and training of the model:
  - loan_size, interest_rate,	borrower_income, debt_to_income,	num_of_accounts, derogatory_marks,	total_debt,	loan_status
  
# Model building & Prediction
- I created a dataframe using the original data and separated y and X by "loan_status" column and all remaining attribute columns. I then splitted the data into training and testing sets and created a Logistic Regression Model with the original data.
- Next I made predictions for testing data and calculated for the accuracy of model using testing data: accuracy result 0.992.
- I then evaluated the model’s performance by generating a confusion matrix and a classification report. Please see detailed analysis and findings below.

# Findings and Analysis 
- Data context: a value of 0 in the “loan_status” column means that the loan is healthy, and a value of 1 means that the loan has a high risk of defaulting.
- Based on the the results generated from the Logistic Regression model:
  - The confusion matrix snapshot:

    <img width="426" alt="image" src="https://github.com/Tianyueli/credit-risk-classification/assets/42381263/467df348-6197-4c55-9d9f-ddec67381349"> 
  - The likelihood of this model getting the loan being healthy result correctly (aka. Precision for loan_status = 0) is 99.8%: 18655 / (18655 + 36)
  - The likelihood of this modelgetting the loan being high-risk result correctly (aka. Precision for loan_status = 1) is 84.1%: 583 / (110 + 583)
  - The possibility of getting the loan being healthy result correctly within total number of loans actually being healthy (True positives and false negatives) (aka. Recall for loan_status = 0) is 99.4%: (18655 / (18655 + 110)
  - The possibility of getting the loan being high-risk result correctly within total number of loans actually being unhealthy (True negatives and false positivies) (aka. Recall for loan_status = 1) is 94.2%: 583 / (36 + 583)
  - Overall, the accuracy of the model of predicting status of creditworthiness of borrowers based on loan status is 99.2%: (18655 + 583) / (18655 + 583 + 36 + 110).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.


# Summary
- In conclusion, this logistic regression model obtained a high accuracy of 99.2% when predicting the creditworthiness of borrowers based on the health of their loan status.
- Summarized view please see classification report below:

    <img width="407" alt="image" src="https://github.com/Tianyueli/credit-risk-classification/assets/42381263/40d1c642-635d-458e-9d89-0fe989a93786">


    ## Summary
    
    Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
    
    * Which one seems to perform best? How do you know it performs best?
    * Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

    If you do not recommend any of the models, please justify your reasoning.



# References

- Modules Imported:
  - import numpy as np
    import pandas as pd
    from pathlib import Path
    from sklearn.metrics import confusion_matrix, classification_report

- Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.
