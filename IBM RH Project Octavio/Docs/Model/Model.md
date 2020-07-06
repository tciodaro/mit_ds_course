# Modelling report

## Data analysis and transformations

The redundant and non informative variables were removed from the data.

The classifier categorical variables were transformed in to binary columns.

Due to the high correlation beetween two variables (Joblevel and MonthlyIncome), It wasa decided to remove the JobLevel from thhe analysis as the result were sligly better without it.

Due to distribution nature of some variables, they were passed in to a log transformation ('MonthlyIncome','YearsSinceLastPromotion','TotalWorkingYears','NumCompaniesWorked').

Apart from the categorical variables and the log transformed ones, the rest were normalized using the Yeo Jhonson method.


## Test and Train

it was used 80% of the data sample for training and 20% for testing

## Model choice

4 diferent models were used in order to chose the one with better results.

    * Logistic regresion (linear)
    *SVM (non linear)
    *KNN (non linear)
    *Random forest (non linear)
    
As the Logistic regression was the model which best performed based on the AUC parameter (0.865), from this point, all the anlalysis were build considering only the Logistic regression.

## Metrics evaluation and results

Quick recap:

The data set is a bit unbalanced considering that around 84% of the employee confirmed a negative attrition. So, the main goal is to create an classifier that could score a negative attrition recall than  better than 50%:

The results:

The model was able to perform an 47% recall score, not reaching our main goal. However it performed very well on the other metrics so, overall the classifier is better than just a 50% guess.











