# credit-risk-classification

# Overview of the Analysis
- In this project, I used various techniques to train and evaluate a model based on loan risk. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify borrowers' creditworthiness.
- The purpose of the model was to predict borrowers' loan status and whether they are accurately predicted as healthy or high-risk. 
- The dataset contains key attributes to assist in forming and training the model:
  - loan_size, interest_rate,	borrower_income, debt_to_income,	num_of_accounts, derogatory_marks,	total_debt,	loan_status
  
# Model Building & Prediction
- I created a data frame using the original data and separated y and X by the "loan_status" column and all remaining attribute columns. I then split the data into training and testing sets and created a Logistic Regression Model with the original data.
- Next, I made predictions for testing data and calculated the model's accuracy using testing data: the accuracy result was 0.992.
- I then evaluated the model's performance by generating a confusion matrix and a classification report. Please see the detailed analysis and findings below.

# Findings and Analysis 
- Data context: A value of 0 in the "loan_status" column means that the loan is healthy, and a value of 1 indicates that the loan has a high risk of default.
- Based on the results generated from the Logistic Regression model:
  - The confusion matrix snapshot:

    <img width="426" alt="image" src="https://github.com/Tianyueli/credit-risk-classification/assets/42381263/467df348-6197-4c55-9d9f-ddec67381349"> 
  - The likelihood of this model getting the loan being healthy result correctly (aka. Precision for loan_status = 0) is 99.8%: 18655 / (18655 + 36)
  - The likelihood of this model getting the loan being high-risk result correctly (aka. Precision for loan_status = 1) is 84.1%: 583 / (110 + 583)
  - The possibility of getting the loan being healthy result correctly within the total number of loans being healthy (True positives and false negatives) (aka. Recall for loan_status = 0) is 99.4%: (18655 / (18655 + 110)
  - The possibility of getting the loan being high-risk result correctly within the total number of loans being unhealthy (True negatives and false positives) (aka. Recall for loan_status = 1) is 94.2%: 583 / (36 + 583)
  - Overall, the model's accuracy in predicting the creditworthiness of borrowers based on loan status is 99.2%: (18655 + 583) / (18655 + 583 + 36 + 110).

    <img width="625" alt="image" src="https://github.com/Tianyueli/credit-risk-classification/assets/42381263/01749a57-8431-41e2-9747-06eb22102b31">

# Summary
- In conclusion, this logistic regression model obtained a high accuracy of 99.2% when predicting the creditworthiness of borrowers based on the health of their loan status.
- Summarized view, please see classification report below:

    <img width="407" alt="image" src="https://github.com/Tianyueli/credit-risk-classification/assets/42381263/40d1c642-635d-458e-9d89-0fe989a93786">
    
- Furthermore, here's a brief  evaluation of different models taken into consideration based on their performance:
    
    * Which one seems to perform best? How do you know it performs best?
      - If time allows, I would also build a Random Forest model to compare the accuracy and evaluate whether one model might further enhance the accuracy of prediction. However, since the current logistic model arrived at 99% accuracy, this appears to be an effective and useful model based on the data provided.
    * Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s or predict the `0`'s? )
      - The model's performance depends on the problem we are trying to solve. For the current analysis, I'm trying to identify creditworthiness to narrow down the list of borrowers. Therefore, status_loan = 0 (aka. healthy loan status) is the primary target I aim to predict. On the other hand, if a different project evaluates the effectiveness of a new pharmaceutical drug, where 0 is the negative result, and 1 is a health improvement, then it might be more beneficial to aim the analysis on the prediction of 1.


# References

- Modules Imported:
  - import numpy as np
    import pandas as pd
    from pathlib import Path
    from sklearn.metrics import confusion_matrix, classification_report

- The data for this dataset was generated by edX Boot Camps LLC and is intended for educational purposes only.
