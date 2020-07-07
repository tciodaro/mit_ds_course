# IBM Project Charter

## Business understanding

IBM is a centenary worldwilde tech company with over 350000 employes. For the past 10 years IBM has been shifting its busines model from selling machines to provide more high values IT related services as Cloud, Quantum computing, Blockchain, Cognitive, etc.

## Final Goal

In oder to prevent valuable employees to leave the enterprise (reduce good employee atrition level), IBM RH in partnership with the AI research team are working on a sollution to predict wether the employee has the desire of leaving the company based on several caracteristics of his internal and external caracteristics. The managment team expect to use the results to proactively take action to maintain a sustainable good employee attrition level.


## Scope

The dataset was build requesting wheter the employee would be willing to leave the the company with no wage increase.

* ** Problem** : Binary Classification
* ** Algorithm** : Supervised Training
* ** DataSet** : CSV file with each employee data (kaggle)
* ** Target Variable** : Positive Attrition (the employee would accept) or Negative attrition (the employee would stay at IBM)

## Metrics

* Qualitative goal: Estimate if an employee would be willing to leave the company for a similar wage based on its caracteristics
* Benchmarking: Positive attition Recall (TP/FP+TP) as the main goal is to practively take action to prevent good employee to leave, it is more important to correctly map the unsatisfied employee than wrongly classify a true satisfied employee.

## Planning 

* Sprint 1: Business understanding and data preparation.
* Sprint 2: Data Analysis and features construction.
* Srpint 3: Classifier Modelling and results evaluation.
* Sprint 4: Model results report

## Arquitecture

* Data

    * CSV File
    * Data report [here](../DataReport/DataReport.md "Data report")
    
* Model 

    * Binary Classifier to predicit if an employee would leave the company for a similar wage
    * Linear Model: Logistic regression
    * Non Linear: Random forest, SVM and KNN
    * The dataset will be divided in 80% training and 20% testing
    * The model will be evaluated considering only the test data
    * The model and analysis can be study [here](../Model/Model.md "Modeling report")
    
* Deliverable

    * Presentation with the results
    * Excel Dataset with the test predicted attrition

## Team 

    * Consultoria:
		* Project lead (Octavio)
		* PO (Octa)
		* Data scientist(s) (Tata)
		* Account manager (Tavinho)
	* Retail Co:
		* Data administrator (IBM)
		* Business contact 
        
