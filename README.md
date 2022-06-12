
**Brief Description**

I work with the housing in California (1990) dataset and try to evaluate three models that can help predict housing prices. 
The dataset is also available for download here (see "housing.csv").

**Versions of packages used:**

Pandas version: 1.4.2,

Numpy version: 1.21.5,

Matplotlib version: 3.5.1,

Sklearn version: 1.0.2

**Methodology:**

The three models I have used are linear regression, decision trees and random forests. I transform the training set using the sklearn pipeline, 
then run LinearRegressor(), RandomForestRegressor() and DecisionTreeRegressor(). After computing the root mean squared error (RMSE) for each and running
10-fold cross-validation, I settle on the Random Forest Regressor. Then I run GridSearchCV to obtain max_features = 8 and n_estimators = 8. Code in line 595 gives
an idea of the importance of individual features in determining median house value, and we can drop certain unimportant features. Finally, I test my final_model 
against the test data and compute the RMSE score.
