# Credit Risk Analysis with Supervised Machine Learning

## I. Overview

### Background

For this project, I am applying machine learning techniques to help Jill to solve a real-world challenge: credit card risk. I need to employ different techniques to train and evaluate models with unbalanced classes: `imbalanced-learn` and `scikit-learn` libraries to build and evaluate models using resampling. 

I used credit card credit dataset from LendingClub (a peer-to-peer lending services company). Then followed the steps below:

1.	First, I used `RandomOverSampler` and `SMOTE` algorithms to oversample the data
2.	I used `ClusterCentroids` algrithem to undersample the data. 
3.	I used a combinatorial approach of over- and undersampling using the `SMITEENN` algorithm.
4.	I used `BalancedRandomForestClassifier` and `EasyEnsembleClassifier` to predict credit risk.
5.	Provide recommendation on whether they should be used to predict credit risk

### Purpose

The purposes of the project are:
1.	Use Resampling Models to Predict Credit Risk
2.	Use the SMOTEENN Algorithm to Predict Credit Risk
3.	Use Ensemble Classifiers to Predict Credit Risk
4.	Provide written report on the Credit Risk Analysis
