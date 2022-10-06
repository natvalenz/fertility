# Fertility and Women's Labor Supply

## Research question
Are KNN, logistic regression, decision trees and random forest good models for predicting whether someone will want more kids based on their age, ethinicity, work hours, and gender of their 1st child?

## Source
https://vincentarelbundock.github.io/Rdatasets/doc/AER/Fertility.html

## Dataset
Cross-section data from the 1980 US Census on married women aged 21–35 with two or more childre
A data frame containing 254,654 (and 30,000, respectively) observations on 8 variables.
### Variables
- morekids factor. Does the mother have more than 2 children?
- gender1 factor indicating gender of first child.
- gender2 factor indicating gender of second child.
- age age of mother at census.
- afam factor. Is the mother African-American?
- hispanic factor. Is the mother Hispanic?
- other factor. Is the mother's ethnicity neither African-American nor Hispanic, nor Caucasian? (see below)
- work number of weeks in which the mother worked in 1979.

## Compare
### Overfitting? Which model is better for classification for the dataset and why?

#### Decision tree classifier and a random forest classifier
There does not appear to be overfitting in any of the models. The accuracy score for training and test sets is similar. Decision tree is a simpler model. Also, decision tree takes up less resources. The accuracy scores for both models are similar. Decision tree appears to be the better model. Although normalization of the data and hyper parameter tuning was applied the metrics are not promising. The highest accuracy score achieved was of 63%.

#### KNN Classifier
There does not appear to be overfitting and the model is performing slightly worse than Random Forest and Decision Trees.

#### Logistic Regression
The model does not appear to be overfitting and 60% accuracy isn't terrible, but the Pseudo R^2 is very low.
Looking more closely at the data in work hours you can see an imbalance there is a high number of individuals who work 0 hours. Are these stay-at-home moms and should this be included as a separate variable?
