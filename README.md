# credit-risk-classification

# Overview 
- This project, I used various techniques to train and evaluate a model based on loan risk. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
  
# Model building & Prediction
- I created a dataframe using the original data and separated y and X by "loan_status" column and all remaining attribute columns. I then splitted the data into training and testing sets and created a Logistic Regression Model with the original data. 
- Next I made predictions for testing data and calculated for the accuracy of model using testing data: accuracy result 0.992.
- I then evaluated the model’s performance by generating a confusion matrix and a classification report. Please see detailed analysis and findings below.

# Findings and Analysis 
- Based on the the results generated from the confusion matrix:
  - The likelihood of this model getting the loan being healthy result correctly (loan_status = 0) is 99.8%: 18655 / (18655 + 36)
  <img width="426" alt="image" src="https://github.com/Tianyueli/credit-risk-classification/assets/42381263/467df348-6197-4c55-9d9f-ddec67381349">
  - The likelihood of this modelgetting the loan being unhealthy result correctly (loan_status = 1) is 84.1%: 583 / (110 + 583)
  - The possibility of getting the loan being healthy result correctly within total number of loans actually being healthy (True positives and false negatives) (aka. recall for loan_status = 0) is 99.4%: (18655 / (18655 + 110)
  - The possibility of getting the loan being unhealthy result correctly within total number of loans actually being unhealthy (True negatives and false positivies) (aka. recall for loan_status = 1) is 94.2%: 583 / (36 + 583)
  - Overall, the accuracy of the model of predicting status of creditworthiness of borrowers based on loan status is 99.2%: (18655 + 583) / (18655 + 583 + 36 + 110).
  

  <img width="404" alt="image" src="https://github.com/Tianyueli/credit-risk-classification/assets/42381263/34feda4d-cf15-4797-8634-937e7d2aaa00">

- How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?
- A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
- Write a Credit Risk Analysis Report

# Data Reference


# References

- Modules Imported:
  - import numpy as np
    import pandas as pd
    from pathlib import Path
    from sklearn.metrics import confusion_matrix, classification_report

- Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.
