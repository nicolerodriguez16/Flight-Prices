# Milestone:  Exploratory Data Analysis(EDA)

Milestone 4 required the Flight Prices dataset to undergo feature engineering and modeling.  Through this process, the main steps my program made was converting all categorical features into numeric values through StringIndexer and Encoding, features that were indexed included “segmentsCabinCode", "startingAirport", "destinationAirport", "travelDuration”, and encoded “segmentsCabinCodeIndex", "startingAirportIndex", "destinationAirportIndex", "travelDurationIndex","isBasicEconomy_binary", "isRefundable_binary", "isNonStop_binary”.


As well as making ‘isBasicEconomy’, ‘isRefundable’, and ‘isNonStop’ binary and to create new numeric columns to be added to the Vector Assembler



 Through Vector Assembler all features were merged and saved to a parquet file sent to the trusted folder.  The file was then retrieved to be used in the modeling portion of the milestone.  The modeling process began by splitting the data into 70% training and 30% testing sets, setting the label as “totalFare” on linear regression estimator and evaluator to retrieve RMSE, R2, RME to identify the accuracy of the model.  With the hyperparameter grid made, the CrossValidator was added calling our features saved previously, the evaluator, the grid with hyperparameters and the 3-fold cross validation our data will undergo. The model was trained and the bestModel was called to predict the test set and the Average Metric: “[119.3626682511643]”, showing the performance over the three folds, Root Mean Squared Error: “119.36465702019076”  showing the square root of the mean squared error showing how far the predictions are from the actual outcomes and R-Squared: “0.5151452061893984” , presenting how well the model performs and predicts totalFare.  


 After conducting the model and receiving feedback, I was suggested on changing the parameter grid with some variations in regularization and elastic net. Adjusting my code to reflect:
“params = ParamGridBuilder() \
.addGrid(linear_reg.fitIntercept, [True, False]) \
.addGrid(linear_reg.regParam, [0.001, 0.01, 0.1, 1, 10]) \
.addGrid(linear_reg.elasticNetParam, [0, 0.25, 0.5, 0.75, 1]) \
.build()”
However, it’s results were not reflecting the ideal outcomes of a lower root mean squared error and a higher R squared. 


Issues Faced: 
When working on Milestone 4, a few challenges that I went through included using the wrong feature engineering methods on certain columns when converting to numeric, YARN running out of RAM, adding my leadTime incorrectly resulting in NULL values and it’s inability to be used in the linear regression model, and more that resulted in numerous moments where I had to restart and reevaluate my plan.
