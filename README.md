# Kickstarter Status Prediction

## What is Kickstarter?
Kickstarter is a platform for crowdfunding creative projects, including everything from films, music, and art to technology, design, and food. The basic idea is that creators can pitch their project to the public and set a fundraising goal, and backers can pledge money to help make the project a reality. In return, backers typically receive rewards such as exclusive access, limited edition products, or even a chance to collaborate with the creator.

## Goal
This project aims to anticipate the success or failure of a Kickstarter campaign and to assist campaign owners in better planning their campaign by offering trends and analyses based on historical data from Kickstarter projects.

## Dataset
The dataset was taken from Kaggle. It contains approximately 374,860 Kickstarter project data up until 2018. There are 12 features and one target variable that determines whether a project was successful.. This target variable has 5 possible options, “failed”, “canceled”, “live”, “suspended”, and “successful”. The description of the features are listed below:

|feature|desc.|
|-------|-----|
|ID | ID is unique for each project.|
|Name | name of the Kickstarter project|
|Category | the listed category of the project like Documentary|
|Sub_Category | Sub Category under Category like Film,Music which comes under Documentary.|
|Currency | currency used to support the project|
|Deadline | deadline for crowdfunding |
|Goal | the fundraising goal or the amount of money needed to complete the project|
|Launched | the data the project launched|
|Pledged | amount pledged by backers|
|Backers | number of people that invested in the project |
|Country | source country of the project|
|usd_pledged | amount pledged by backers in USD|
|usd_goal_real | the amount of money needed to complete the project in USD|
|State | the variable to be predicted|

## Implementation
The following machine learning models were employed to predict the status of a Kickstarer project.
- Random Forest
- Naive Bayes
- Complement Naive Bayes
- Gausian Naive Bayes
- Decision Trees
- Support Vector Machines
- XGBoost
- Ensemble methods

## Results
After hyperparameter tuning using grid/random search, these are the results that were obtained.
### Random Forest 
|class|numerical|textual|
|-----|---------|-------|
|0|precision:0.93 - recall:0.89|precision:0.69 - recall:0.70|
|1|precision:0.90 - recall:0.93|precision:0.72 - recall:0.71|
|overall accuracy|0.91|0.71|

### Decision Tree
|class|numerical|textual|
|-----|---------|-------|
|0|precision:0.93 - recall:0.89|precision:0.57 - recall:0.73|
|1|precision:0.90 - recall:0.93|precision:0.67 - recall:0.53|
|overall accuracy|0.91|0.61|

### Support Vector Machine
|class|numerical|textual|
|-----|---------|-------|
|0|precision:0.84 - recall:0.78|precision:0.65 - recall:0.69|
|1|precision:0.81 - recall:0.86|precision:0.70 - recall:0.66|
|overall accuracy|0.82|0.77|

### XGBoost
|class|numerical|textual|
|-----|---------|-------|
|0|precision:0.91 - recall:0.90|precision:0.67 - recall:0.72|
|1|precision:0.91 - recall:0.92|precision:0.72 - recall:0.66|
|overall accuracy|0.92|0.69|

## Conclusion
The success rate of the projects is most closely associated with the `backers_count` which represents the number of people supporting or backing the project.



