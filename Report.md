# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis:
   -The purpose of this analysis was to classify the difference between loans with a healthy status (0) and unhealthy status (1) 

* Explain what financial information the data was on, and what you needed to predict:
   -The financial info that was used to categories the difference included the size of the loan from the borrower.
   -The interest rate applied to that loan
   -The income of the borrower 
   -How the person's income compared to their current debt
   -The number of accounts a borrower has
   -Any derogatory marks on loans that the borrower holds
   -Finally, the total debt held by the borrower

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
  -In the initial data sets we had the following split of healthy loans vs unhealthy loans (denoted as 0 or 1):
    - 75,036 (97%)
    - 2,500 (3%)

* Describe the stages of the machine learning process you went through as part of this analysis.
  - We will feed the data into a function that will train our model to make predictions from the current dataset. It will use this info to later make predictions about the health of the loan. 
  - We will then fit the training data into different models to see what predictions our machine learing models will make
  - Once the data is fit to the model, we will then assess the accuracy in a few different ways to see if the predicted values from the machine match with actual results.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method):
  - We will run a few different logistic regression models. Once with the raw data and once with a resampling method that will adjust for the lower count unhealthy loans.
  - The logistic regression model will classify which financial info is more closely associated with healthy loans and which ones are associated with unhealthy loans.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  -Model 1 is a logistic regression model that is only using the raw data to make predictions:

    -The model had an accuracy of .992/1
    -It had an average recall score of .94
    -The precision was reported as .99




* Machine Learning Model 2:
  -Model 2 is a logistic regression model that used the oversampled data to make predictions

    -The model had an accuracy of .992/1
    -It had an average recall score of .99
    -The precision reported was .99

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
  -Both models seem to preform at a high level, with model 2 preforming slightly better. However, if you are concerned that we might be missing more information on higher risk borrowers, the oversampling method might be best given that the raw data shows only 3% of total borrowers who have unhealthy loans.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s?)
  -Yes, but there could be downsides to not knowing either direction. If we are not doing a good job predicting the risky loans, obviously this can expose a lender to risk. However, if we are only focusing on predicting 1's we may be missing out on potential clients and revenue. 

If you do not recommend any of the models, please justify your reasoning.
