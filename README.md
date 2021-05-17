# Credit Risk Analysis

## Project Overview
The purpose of this project is to employ different techniques to train and evaluate models with unbalanced classes. With the [credit dataset](https://github.com/Mishkanian/Credit_Risk_Analysis/blob/main/LoanStats_2019Q1.csv.zip) from LendingClub, several different algorithms are used to predict credit risk. The performance of these different models are evaluated and recommendations are suggested based on the results.

## Software
- Python 3.7
- SciPy 1.6.2
- Scikit-learn 0.24.1
- imbalanced-learn 0.80

## Results

Below are the resampling models have been used in this project.

### Oversampling: Native Random Oversampling
- Balanced Accurracy Score: 0.674

### Oversampling: SMOTE
Synthetic Minority Oversampling Technique (SMOTE) is an oversampling approach to deal with unbalanced datasets.
- Balanced Accurracy Score: 0.662

### Undersampling: Random Undersampling
In random undersampling, instances are randomly selected from the majority class and removed until the size of the majority class is reduced (typically to the size of the minority class).
- Balanced Accurracy Score: 0.662

### Combination Sampling: SMOTEENN
SMOTEENN is combination of SMOTE and Edited Nearest Neighbor (ENN) algorithms. This involves a two step process:
  1. Oversample the minority class with SMOTE.
  2. Clean the resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong to two different classes, that data point is dropped.
- Balanced Accurracy Score: 0.644
 
### Balanced Random Forest Classifier
- Balanced Accurracy Score: 0.788

### Easy Ensemble AdaBoost Classifier
- Balanced Accurracy Score: 0.931

## Summary

[PROJECT IN PROGRESS]

**Author: Michael Mishkanian**  
For all questions and inquiries, please contact me on [LinkedIn](https://www.linkedin.com/in/michaelmishkanian/).
