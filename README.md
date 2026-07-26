# AIMLDataAssignment2
In this application, you will explore a dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. Your goal is to understand what factors make a car more or less expensive. As a result of your analysis, you should provide clear recommendations to your client -- a used car dealership -- as to what consumers value in a used car.


## Findings
The null values for the columns condition, cylinders , VIN , drive, size , type and paint_color is more than 30% of the total values in the respective columns.
The column id is for identification and can be dropped from the dataset as this feature does not impact the price of the used car.
Column model has 29649 categories which is very high cardinality for any one hot encoder.
VIN number column has a lot of null values and will not add much to the car price and can be dropped from the dataset.
Size column has about 71.77% of null values and will impact the ability of the model to predict the price efficiently. The column can be dropped from the data set.
The columns/features (condition, cylinders, drive,type) that are important and has 20% more than null values need to marked as unknown or any categorical value in the dataset.
Other columns which have less than 5% of data missing can be handled appropriately.
Histogram plot for the distribution of target price taking all the rows is more skewed to the left and also have outliers. PLot with price values filtered between 500 to100k  is more stable.
There are 32895 rows with price value equals to 0.
Duplicate VIN number records counts is 40280.
Odometer column has values equal to 0 and some values equal to 10,000,000 miles which does not look right.
Group by condition median plot shows us that the price is better for newer condition cars.
Group by Type median shows that the if the type is pickup and truck then the median prices are more when compared to other types.
Group by drive median plot indicates higher prices for 4wd than the other fwd or rwd cars.
Group by fuel type median plot indicates highest price for diesel cars followed by electric, gas and hybrid.
Scatter plots of price and odometer , price and age shows a steep decline as the number of years and mileage increases. the heap map also confirms the negative relationship between price and age , price and odometer.

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
Analyzed more than 350k used car listings and used the Ridge and lasso models to fit the data. The R2 score was slightly better for Ridge which indicates a better model.
The top 10 features that affected the price of the car both negatively and postively were determined.
As the age of the car goes by the value of the car decreased by  988$ per year. 
For every 10k miles driven the value of the car decrease by 694$.
The car in new condition sells for $7003 more than the median value in the data set followed by good, excellent and fair. 
Higher the number of cylinders, higher the price of the used cars.
Title status salvage sells for lower proce when compared to other title status.
Tesla, Ram, Porsche and similar luxury brands sell for more price than the other economy brands like chrysler, fiat, hyundai and saturn.
Pick up trucks , coup sells at higher price than the sedans and mini vans.
4wd and rwd have higher prices than the fwd.
White, black , orange and yello shows slightly higher median prices than the green and purple cars.




Link to the [notebook](https://github.com/amairj4u/ALMLDataAssignment2/blob/main/prompt_II.ipynb)
