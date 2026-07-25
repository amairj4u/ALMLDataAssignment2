# AIMLDataAssignment2
In this application, you will explore a dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. Your goal is to understand what factors make a car more or less expensive. As a result of your analysis, you should provide clear recommendations to your client -- a used car dealership -- as to what consumers value in a used car.


## Findings
Ridge alpha = 2.68 , R2 = 0.735 RMSE = 7370 MAE = 5119 non zero feat : 190
Lasso alpha = 1.00 , R2 = 0.734 RMSE = 7373 MAE = 5115 non zero feat : 162
Comparing the 2 regression models Ridge regression looks to be a better model. It is taking into account all the features after pre processing.
Two of the numerical features namely age and odometer has the one of the biggest negative impact on the price of the car. Age has a -7972 and Odometer has -3992.
Other major factors economy manufacturer cars like fiat, mitsubishi, kia and hyundai.
Branded/high end cars have a positive impact on the price of the car.
The number of cylinders for the engine also has a positive impact on the prices of the car.
Clean title car also has a positive impact on the price.
Electric vehicles has a negative impact on the price of the car.
Using the linear regression model the coefficients for age returned is -988. It means that for every year the price of the car is reduced by 988$.
The coefficient for the Odometer is -694 for every 10k miles. This means that for every 10k miles the value of the car is reduced by 694$.
The car in new condition sells for $7003 more than the median value in the data set.



Link to the [notebook]()
