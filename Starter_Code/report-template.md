# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

Using supervised machine learning and banking data to predict the outcome, high-risk or healthy loan, of any particular loan. 

Following the prompt, every provided fields, or columns, from the data is fitted into the Logistic Regression model to train the model.

The listed loans, or rolls, are separated into a training portion and a testing portion.  The training portions of the data are the data that was used to fit the model.
The testing portion of the data are used after the training to make prediction by the model in order to determine the precision and accuracy of the machine training model. 

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Logistic Regression:
    * The model had a accuracy score of 99.2%, or (18655+583)/(18655+583+110+36) = (Total True predictions)/(Total Samples).
    * Precision for healthy loans (0) is 1.00.  The model predicted the healthy loans at a very close to 100% rate, actual 99.80% or 18655/(18655+36), with only 36 wrong predictions out of 18691.
    * Precision for high-risk loans (1) is lower at 0.84.  The model precision for high-risk loans are a lot lower, most likely due to the low amount of high-risk loans in the dataset at 84.1% or 583/(583+110). 
        The model made 110 wrong predictions out of 693.  
    * Recall for health loans is 0.99.  The model correctly predicted 18655 healthy loans out of the total 18765 = (18655+110) healthy loans, or 99.4%.
    * Recall for high-risk loans (1) is lower at 0.94.  The model correctly predicted 583 high-risk loans out of the total 619 = (583+36) high-risk loans, or 94.2%.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

The Logistic Regression Model seem to make predictions fairly well, especially if your goal is to determine if the loan is going to be healthy.
However, if your goal is to determine if a loan is going to be high-risk. The model can be slightly risky; it might over predict high-risk loans, when the loan is actually healthy. 
In combination, I will still recommend the model, since the only risk is turning away some healthy loans as high-risk loans.  It still do a good job at not predicting healthy loans, when the loan is actually high-risk.
