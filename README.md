# Credit Risk Classification

This assignment was to use classification techniques to evaluate the loan risk of people. 0 being a healthy loan  
and 1 being a high-risk loan. To do this, we used a dataset of historical lending activities to train and  
evaluate a model based on its loan risk. We created two models and analyzed which, if any, worked better at their  
predictions. Then write a report on your findings.  

---

## About

This assigment is split into three sections. Part's 1 and 2 are creating two different models to predict and  
evaluate the loan status of people and part 3 is to write up a report on your findings. For the models, use  
the `lending_data.csv` to read in the data and train/test on. 
  * `0` loan status means the loan is healthy.
  * `1` loan status means the loan is at a high-risk of defaulting.
Train, test, and split the data before initializing, fitting, and predicting. After all those steps are done,
evaluate the balanced accracy score, the confusion matrix, and the classification report for each model. Finally,
write up a classification report on your findings and analyze which, if any, model is best to use.

---

## Getting Started  

  1. Create a new repository for this project called `credit-risk-classification`.
  2. Clone the new repository to your computer.
  3. Inside your `credit-risk-classification` repository, create a folder titled "Credit_Risk."
  4. Inside the "Credit_Risk" folder, add the `credit_risk_classification.ipynb` and `lending_data.csv` files.
  5. Use the [Starter_Code](https://github.com/Kaileycar/credit-risk-classification/files/12707034/Starter_Code.zip) to get the files.
  6. Add a `report.md` to analyze your findings.

---

## Usage

### Model 1: Original Data
  * Split the data into training and testing steps.
      * Create the labels (`y`) from the "loan_status" column.
      * Create the features (`X`) from the remaining columnns.
  * Use the function `train_test_split` to split up the data.

  * Create a Logistic Regression model with the original data.
      * Fit the model by using the training data (`X_train` and `y_train`).
      * Save the predictions for the testing data labels by using the testing features data (`X_test`) and the fitted model.
      * Evaluate the model's performance by doing the following:
          * Calculating the `balanced_accuracy` score by using the `y_test` and `predictions`.
          * Caluclate the `confusion_matrix` by using the `y_test` and `predictions`.
          * Caluculate the `classification_report` by using the `y_test` and `predictions`.

  * Answer the following question: **How well does the logistic regression model predict both the 0 (healthy loan) and
                                     1 (high-risk loan) labels?**

### Model 2: RandomOverSampled Data  
  * Instantiate the `random oversampler` model from imbalanced-learn.
  * Fit the original training data to the random_oversampler model.

  * Create a Logistic Regression model.
      * Fit the model with the resampled data (`X_resampled` and  `y_resampled`).
      * Save the predictions to a variable. Use the testing data (`X_test`) and the fitted model.
      * Evaluate the model's performance by doing the following:  
          * Calculating the `balanced_accuracy` score by using the `y_test` and `predictions`.  
          * Caluclate the `confusion_matrix` by using the `y_test` and `predictions`.  
          * Caluculate the `classification_report` by using the `y_test` and `predictions`.

  * Answer the  following question: **How well does the logistic regression model, fit with oversampled data, predict both
                                    the 0 (healthy loan) and 1 (high-risk loan) labels?**

### Report: Credit Risk Analysis  
  Write a brief report that includes a summary and analysis of the performance of the machine learning models.  
  Structure your report by using the report template that `Starter_Code` includes, ensuring that it contains the following:  
    * **An overview of the analysis:** Explain the purpose of this analysis.  
    * **The results:** Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine  
      learning model.  
    * **A summary:** Summarize the results from the machine learning model. Include your justification for recommending the model  
      for use by the company. If you don’t recommend the model, justify your reasoning.  

---

## Links: 

  * [Balanced Accuracy](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.balanced_accuracy_score.html)
  * [Random OverSampler](https://imbalanced-learn.org/stable/over_sampling.html)
