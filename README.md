# Credit Risk Analysis

## Project Overview
The purpose of this project is to employ different techniques to train and evaluate models with unbalanced classes. With the [credit dataset](https://github.com/Mishkanian/Credit_Risk_Analysis/blob/main/LoanStats_2019Q1.csv.zip) from LendingClub, several different algorithms are used to predict credit risk. The performance of these different models are compared and recommendations are suggested based on the results.

## Software
- Python 3.7
- SciPy 1.6.2
- Scikit-learn 0.24.1
- imbalanced-learn 0.80

## Results

Below are the resampling models have been used in this project and their individual results.

### Oversampling: Native Random Oversampling
In [random oversampling](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.RandomOverSampler.html), instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced.
- Balanced Accurracy Score: 0.674
- High-Risk Precision: 0.01
- High-Risk Recall: 0.74

![random_over](https://github.com/Mishkanian/Credit_Risk_Analysis/blob/main/README_images/random_oversample.png)

### Oversampling: SMOTE
Synthetic Minority Oversampling Technique ([SMOTE](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html)) is an oversampling approach to deal with unbalanced datasets.
- Balanced Accurracy Score: 0.662
- High-Risk Precision: 0.01
- High-Risk Recall: 0.63

![smote](https://github.com/Mishkanian/Credit_Risk_Analysis/blob/main/README_images/smote.png)

### Undersampling: Random Undersampling
In [random undersampling](https://imbalanced-learn.org/stable/references/generated/imblearn.under_sampling.RandomUnderSampler.html), instances are randomly selected from the majority class and removed until the size of the majority class is reduced (typically to the size of the minority class).
- Balanced Accurracy Score: 0.662
- High-Risk Precision: 0.01
- High-Risk Recall: 0.63

![random_under](https://github.com/Mishkanian/Credit_Risk_Analysis/blob/main/README_images/random_under.png)

### Combination Sampling: SMOTEENN
[SMOTEENN](https://imbalanced-learn.org/stable/references/generated/imblearn.combine.SMOTEENN.html) is combination of SMOTE and Edited Nearest Neighbor (ENN) algorithms. This involves a two step process:
  1. Oversample the minority class with SMOTE.
  2. Clean the resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong to two different classes, that data point is dropped.
- Balanced Accurracy Score: 0.644
- High-Risk Precision: 0.01
- High-Risk Recall: 0.72

![smoteenn](https://github.com/Mishkanian/Credit_Risk_Analysis/blob/main/README_images/smoteenn.png)

### Balanced Random Forest Classifier
A [Balanced Random Forest](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.BalancedRandomForestClassifier.html) is an ensemble method that randomly under-samples to achieve balance.
- Balanced Accurracy Score: 0.788
- High-Risk Precision: 0.03
- High-Risk Recall: 0.70

![balanced_forest](https://github.com/Mishkanian/Credit_Risk_Analysis/blob/main/README_images/balanced_random_forest.png)

### Easy Ensemble AdaBoost Classifier
Bag of balanced boosted learners also known as [EasyEnsemble](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.EasyEnsembleClassifier.html). The balancing is achieved by random under-sampling.
- Balanced Accurracy Score: 0.931
- High-Risk Precision: 0.09
- High-Risk Recall: 0.92

![adaboost](https://github.com/Mishkanian/Credit_Risk_Analysis/blob/main/README_images/adaboost.png)

## Summary

[Easy Ensemble AdaBoost Classifier](https://imbalanced-learn.org/stable/references/generated/imblearn.combine.SMOTEENN.html) has the highest Balanced Accuracy Score out of all of the techniques employed in this project. EasyEnsemble also has the highest precision, recall, and F1 scores as proven by the imbalanced classification reports printed for each model.

If one of the models in this project must be used to predict credit risk, it is recommended to use **Easy Ensemble AdaBoost Classifier.**  However, if given the option, it is not suggested to use any of these models. Although the EasyEnsemble model performed the best in this group, its precision for high-risk data points is still only 0.09. This indicates that very few of positive predictions are true (False Positives). Further research and development is required to create a more robust model that can predict credit risk.


**Author: Michael Mishkanian**  
For all questions and inquiries, please contact me on [LinkedIn](https://www.linkedin.com/in/michaelmishkanian/).
