# Module 20 Report 

---

## Overview of the Analysis

The purpose of this challenge was to test to see if we could predict who has a good loan status and who has a high-risk loan  
status based off of other data relating to it. The labels were `0` for good loan status and `1` for high-risk loan status.  
A `value_counts` of the labels showed 75,036 for group 0 and 2,500 for group 1. To start the analysis, we had to split the  
training and testing data using the `train_test_split` function from sklearn. This defaults to a 75% training group and 25%  
testing group. We then used the `LogisticRegression` funciton to initiate, fit, and then predict the model. Finally, to see 
our predictions we calculated the `balance_accuracy` score, generated a `confusion_matrix` of the model, and printed the  
`classification_report` for the model. After these predictions and results, the next part was to complete the same steps with  
the `RandomOverSampler` module from imbalanced-learn to see if/how our predictions would differ. 

---

## Results

* Machine Learning Model 1:
  
  * The balanced accuracy score was a 0.9520
  * The accuracy for the classification report was a 0.99
  * The precision for `0` was a 1.00
  * The recall for `0` was a 0.99
  * The precision for `1` was a 0.85
  * The recall for `1` was a 0.91  



* Machine Learning Model 2:  

  * The balance accuracy score was a 0.9937
  * The accuracy for the classification report was a 0.99
  * The precision for `0` was a 1.00
  * The recall for `0` was a 0.99
  * The precision for `1` was a 0.84
  * The recall for `1` was a 0.99

---

## Summary

Between the 2 models, the second one with the `RandomOverSampler` seemed to be more precise in its predictions overall for  
group `1` and group `0`. While both models have predicted the `0's` almost 100%, the `1's` predictions were not quite that  
high. It is more important to be able to predict the `1's` because those are the loans that are at a high risk of default.  
A loan that has defaulted damages your credit-score and makes it very hard for you to buy a car or a house or get a credit  
card in the future. A loan that is at high-risk of defaulting hasn't defaulted yet, but are close. If we could predict who is  
high-risk, we could help those people from not defaulting and ruining their credit or future ability to purchase big things.  
While the second model was more precise in predicting the recall, the prediction for the precision was at a 84% which I would  
not feel comfortable using that method with such high stakes at hand. 
