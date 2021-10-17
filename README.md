# Credit Risk Analysis with Supervised Machine Learning

## I. Overview

### Background

For this project, I am applying machine learning techniques to help Jill to solve a real-world challenge: credit card risk. I need to employ different techniques to train and evaluate models with unbalanced classes: `imbalanced-learn` and `scikit-learn` libraries to build and evaluate models using resampling. 

I used credit card credit dataset from LendingClub (a peer-to-peer lending services company). Then followed the steps below:

1.	First, I used `RandomOverSampler` and `SMOTE` algorithms to oversample the data
2.	I used `ClusterCentroids` algrithem to undersample the data. 
3.	I used a combinatorial approach of over- and undersampling using the `SMOTEENN` algorithm.
4.	I used `BalancedRandomForestClassifier` and `EasyEnsembleClassifier` to predict credit risk.
5.	Provide recommendation on whether they should be used to predict credit risk

### Purpose

The purposes of the project are:
1.	Use Resampling Models to Predict Credit Risk
2.	Use the SMOTEENN Algorithm to Predict Credit Risk
3.	Use Ensemble Classifiers to Predict Credit Risk
4.	Provide written report on the Credit Risk Analysis

## II. Results

### RandomOverSampler

![01](https://user-images.githubusercontent.com/84211948/137615316-907eaadd-6a58-4537-ac71-870190d2acb1.png)

- The balanced accuracy score is 65%.
- For high-risk, the precision score is 1%, recall score is 63%. Only 1% of predicted high-risk are true high-risk and 63% high-risk cases are correctly identified by this model with a F1 score of 2%. 
- For low-risk, the precision score is 100%, recall score is 67%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 67% low-risk are correctly identified with a F1 score of 80%.


### SMOTE 

![02](https://user-images.githubusercontent.com/84211948/137615321-03af0675-c3d4-4a97-831f-c2dad0583fd2.png)

- The balanced accuracy score is 65%.
- For high-risk, the precision score is 1%, recall score is 64%. Only 1% of predicted high-risk are true high-risk and 64% high-risk cases are correctly identified by this model with a F1 score of 2%. 
- For low-risk, the precision score is 100%, recall score is 66%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 66% low-risk are correctly identified with a F1 score of 79%.

### ClusterCentroids

![3](https://user-images.githubusercontent.com/84211948/137615327-da3f350c-4c6f-4433-ae1b-754c6ea2bf92.png)

- The balanced accuracy score is 53%.
- For high-risk, the precision score is 1%, recall score is 61%. Only 1% of predicted high-risk are true high-risk and 61% high-risk cases are correctly identified by this model with a F1 score of 1%. 
- For low-risk, the precision score is 100%, recall score is 45%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 45% low-risk are correctly identified with a F1 score of 62%.

### SMITEENN

![4](https://user-images.githubusercontent.com/84211948/137615333-98a23cd8-e840-4b0c-b2e1-ba33c0e65561.png)

- The balanced accuracy score is 64%.
- For high-risk, the precision score is 1%, recall score is 70%. Only 1% of predicted high-risk are true high-risk and 70% high-risk cases are correctly identified by this model with a F1 score of 2%. 
- For low-risk, the precision score is 100%, recall score is 57%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 57% low-risk are correctly identified with a F1 score of 73%.

### BalancedRandomForestClassifier

![5](https://user-images.githubusercontent.com/84211948/137615341-f408d043-1f15-43f0-995b-9e537410085c.png)

- The balanced accuracy score is 79%.
- For high-risk, the precision score is 4%, recall score is 67%. 4% of predicted high-risk are true high-risk and 67% high-risk cases are correctly identified by this model with a F1 score of 7%. 
- For low-risk, the precision score is 100%, recall score is 91%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 91% low-risk are correctly identified with a F1 score of 95%.

### EasyEnsembleClassifier

![6](https://user-images.githubusercontent.com/84211948/137615350-b01390a7-5183-4db5-ba66-95a7a082eba0.png)

- The balanced accuracy score is 93%.
- For high-risk, the precision score is 7%, recall score is 91%. 7% of predicted high-risk are true high-risk and 91% high-risk cases are correctly identified by this model with a F1 score of 14%. 
- For low-risk, the precision score is 100%, recall score is 94%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 94% low-risk are correctly identified with a F1 score of 97%.

## III. Summary

In summary, `ClusterCentroids` has the lowest accuracy score, precision score, recall score and the F1 score. On the other hand, `EasyEnsembleClassifier` has the highest accuracy score, precision score, recall score and F1 score. 

### Recommendation

Due to the small population of high-risk, the precision scores of high-risk are extremely low for each model, and low-risk precision scores are almost 100% for all of the models. For credit risk analysis, it very important to catch the high-risk profiles. In this case, the recall score of high-risk is more essential, it indicates how many high-risk profiles can be identified among all real high-risk profiles. Therefore, `EasyEnsembleClassifier` has the best performance to catch high-risk profiles, it determined 92% of real high-risk profiles. At the same time, all of the models also falsely determined a large number of high-risk those are actually low-risk profiles (low precision scores of low-risk), so that many applicants will be falsely rejected.

In conclusion, if the bank just aims to catch as many high-risk as possible, `EasyEnsembleClassifier` would be the best choice. However, if the bank aims to accurately determine both low- and high-risk profiles, they should move on to models other than the above six.



