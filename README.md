
# Module 20 Challenge (Credit Risk Classification)

![image](https://user-images.githubusercontent.com/116117065/228039501-c624c93e-8921-4528-8091-72eb1eefbbb8.png)


## Table of Contents:

1. Overview of the Analysis

2. Model Results

3. Summary


## 1. Overview of the Analysis

* Lenders operate on the fundamental assumption that the borrowers they lend money or assets to will repay their debts. However, there is always a risk associated with lending, as some borrowers may default on their loans or fail to return the assets, leading to financial losses for the lenders. To mitigate this risk, lenders use various techniques to assess the creditworthiness of borrowers. In this analysis, we will use Machine Learning to examine a dataset of a peer-to-peer lending service company's past lending activities to construct a model that can identify the probability of borrowers defaulting on their loans.

* The y_prediction is the variable being predicted in this analysis. To begin, I gather data from the loan_status column and store it in the y_variable. By utilizing the value_counts method, I can determine the number of good and bad loans present in the dataset. This information is then utilized to create the test data for both training and prediction purposes.

* Employing a machine learning model, my objective is to find the difference between healthy (low-risk) and non-healthy (high-risk) loans. To accomplish this we have made two models and using methods of LogisticRegression and resampling methods. Logistic Regression Algorithm is the ideal tool, as it is frequently employed to estimate the probability of a target variable in classification problems.


     <img src="https://user-images.githubusercontent.com/116117065/228032346-3d5c921f-3af9-4ead-b942-a8a0655b2f65.png"  width="650" height="300">

 
     ![image](https://user-images.githubusercontent.com/116117065/228034138-17dcced3-f6bf-46dd-83be-11382ef04ae1.png)

The model shows the number of healthy loans are higher than the non-healthy or high risk loans. The balanced accuracy score is 95% and its because the of data being imbalanced. According to the report we can also see the model scored 85% or above on all of the metrics. however, the model predicted the healthy loans 100% of the time and predicted the non-healthy loands 85% of the time. 

According to the confusion matrix there are 18,765 loan status from which the model predicted 18,663 as healthy correctly and 102 incorrectly. Likewise, out of 619 loan status it predicted the 563 as non-healthy correclty and 56 incorrectly. 

I have used the **RandomOverSampler** module to generate a better accuracy score from the data.

The following are results for value_count:


   ![image](https://user-images.githubusercontent.com/116117065/228035545-0737503e-3cb9-4148-89b2-7079588b5185.png)

   ![image](https://user-images.githubusercontent.com/116117065/228038069-8ac71058-a893-46f4-8c29-aace9adb33a8.png)

---------------------------------------------------------------------------------------------------------------------------------------------------------------

## 2. Results

* Machine Learning Model 1 (LogisticRegression):

     * balanced_accuracy_score = 0.9520479254722232
     * precision 0=1.00, 1=0.85
     * recall 0=0.99, 1=0.91
     
   ![image](https://user-images.githubusercontent.com/116117065/228047920-e979828f-c9fd-4a77-b2e2-e888e64cfc44.png)
   
   
   ![image](https://user-images.githubusercontent.com/116117065/228037332-a9b372d0-0210-4656-9864-99da2e598a2c.png)
   
  
    

* Machine Learning Model 2 (RandomOverSampler):

     * balanced_accuracy_score = 0.9936781215845847
     * precision 0=0.99, 1=0.99
     * recall 0=0.99, 1=0.99
  
  
  ![image](https://user-images.githubusercontent.com/116117065/228036907-9745e958-cde7-40a1-a960-06d909da7c3f.png)
  
  ![image](https://user-images.githubusercontent.com/116117065/228037014-479fcd2a-f006-438d-9282-509634060965.png)

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 3. Summary

Based on my analysis, the RandomOverSampler model appears to be the most effective, as it identifies a greater number of individuals who may be
at risk of defaulting on loans due to their credit risk.

The Logistic Regression model trained with OverSampled data outperformed the model trained with Imbalanced data, primarily due to the balanced nature of the data. Consequently, the model achieved a higher accuracy score and recall rate, indicating that it would make significantly fewer mistakes when categorizing non-healthy loans.

I would recommend the RandomOverSampler model for the better accuracy score and the ability to detect mistakes. 

