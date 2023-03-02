# Deciding on which model to use in a ML problem:

## We will understand how to train different models, how to optimize and compare the models to decide on which model to use for out analysis.

A survey was conducted on 1525 voters with 9 variables. Building a model, to predict which party a voter will vote for on the basis of the given information, to create an exit poll that will help in predicting overall win and seats covered by a particular party.

### This analysis is for learning purposes only. We will look at how different Machine Learning models can be appied on such data and understand the model evaluation techniques.

## Steps involved:
Descriptive statistics and null value condition checks were done on the data.

Performing Univariate, Bivariate and exploratory data analysis with checks on Outliers.

### Data Preparation:
#### We need to encode our string variables as we can only have numerical data which can be fed to a ML model.
There are various encoding techniques we can use to achieve this such as one hot encoding and label encoding.

#### Data Scaling was performed to bring all the variables on a similar dimension so that the distance based algorithms will not be affected by variables with larger dimensions.

### Model Building:

Various models were built to check the performance of each model. The models build were on Logistic Regression, LDA (linear discriminant analysis), K-Nearest Neighbors Model, Naïve Bayes Model, support vector machine (SVM), bagging(Random Forest) and boosting algorithms(XGBoost, ADA Boost, etc)

### Model optimization:

Bagging and boosting algorithms perform differently based on hyperparameter settings.
It is not possible for us to check how model(s) perform on each combination of hyperparameters. An automated methodology is required to achieve this.
GridSearchCV and Param grid techniques were used to achieve this.

Best parameters were found using these techniques and model performance was checked after training the models with best parameters obtained.

### Model Performance:
Model performacne was checked on various metrics such as:
Checking the performance of Predictions on Train and Test sets using Accuracy, Confusion Matrix, Plot ROC curve and get ROC_AUC score for each model.

#### Please check the jupyter notebook to understand how each of the models performed on each of the above mentioned metrics. However, below is a high level inference about this excercise.

### Inference:

Looking at the performance metrics, all the models are doing decently good
The models on support vector machine, XGBoost and Adaboost seem to be performing slightly better with accuracy scores around 81-83%

The logistic regression, LDA and KNN models are also performing good with accuracy scores around of 82%, 82% and 80% respectively

Naive Bayes and Random Forest Classifier are having accuracy scores around 75 percent respectively. While other models seem to be doing better with the accuracy scores above 80 percent

In all of the models, we can see that the recallsfor Labor are on higher when compared to the recall for conservative.
Recall for conservative is very low for the models on Random Forest and Naive Bayes, while other models give decent numbers
