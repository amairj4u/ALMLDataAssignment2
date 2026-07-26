# AIMLDataAssignment2
In this application, you will explore a dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. Your goal is to understand what factors make a car more or less expensive. As a result of your analysis, you should provide clear recommendations to your client -- a used car dealership -- as to what consumers value in a used car.


## Findings
1. The null values for the columns condition, cylinders , VIN , drive, size , type and paint_color is more than 30% of the total values in the respective columns.
2. The column id is for identification and can be dropped from the dataset as this feature does not impact the price of the used car.
3. Column model has 29649 categories which is very high cardinality for any one hot encoder.
4. VIN number column has a lot of null values and will not add much to the car price and can be dropped from the dataset.
5. Size column has about 71.77% of null values and will impact the ability of the model to predict the price efficiently. The column can be dropped from the data set.
6. The columns/features (condition, cylinders, drive,type) that are important and has 20% more than null values need to marked as unknown or any categorical value in the dataset.
7. Other columns which have less than 5% of data missing can be handled appropriately.
8. Histogram plot for the distribution of target price taking all the rows is more skewed to the left and also have outliers. PLot with price values filtered between 500 to100k  is more stable.
9. There are 32895 rows with price value equals to 0.
10. Duplicate VIN number records counts is 40280.
11. Odometer column has values equal to 0 and some values equal to 10,000,000 miles which does not look right.
12. Group by condition median plot shows us that the price is better for newer condition cars.
13. Group by Type median shows that the if the type is pickup and truck then the median prices are more when compared to other types.
14. Group by drive median plot indicates higher prices for 4wd than the other fwd or rwd cars.
15. Group by fuel type median plot indicates highest price for diesel cars followed by electric, gas and hybrid.
16. Scatter plots of price and odometer , price and age shows a steep decline as the number of years and mileage increases. the heap map also confirms the negative relationship between price and age , price and odometer.
17. Ridge alpha = 2.68 , R2 = 0.735 RMSE = 7370 MAE = 5119 non zero feat : 190
18. Lasso alpha = 1.00 , R2 = 0.734 RMSE = 7373 MAE = 5115 non zero feat : 162
19. Comparing the 2 regression models Ridge regression looks to be a better model. It is taking into account all the features after pre processing.
20. Two of the numerical features namely age and odometer has the one of the biggest negative impact on the price of the car. Age has a -7972 and Odometer has -3992.
21. Other major factors economy manufacturer cars like fiat, mitsubishi, kia and hyundai.
22. Branded/high end cars have a positive impact on the price of the car.
23. The number of cylinders for the engine also has a positive impact on the prices of the car.
24. Clean title car also has a positive impact on the price.
25. Electric vehicles has a negative impact on the price of the car.
26. Using the linear regression model the coefficients for age returned is -988. It means that for every year the price of the car is reduced by 988.
27. The coefficient for the Odometer is -694 for every 10k miles. This means that for every 10k miles the value of the car is reduced by 694.
28. The car in new condition sells for 7003 more than the median value in the data set.
29. Analyzed more than 350k used car listings and used the Ridge and lasso models to fit the data. The R2 score was slightly better for Ridge which indicates a better model.
30. The top 10 features that affected the price of the car both negatively and postively were determined.
31. As the age of the car goes by the value of the car decreased by  988 per year. 
32. For every 10k miles driven the value of the car decrease by 694.
33. The car in new condition sells for 7003 more than the median value in the data set followed by good, excellent and fair. 
34. Higher the number of cylinders, higher the price of the used cars.
35. Title status salvage sells for lower proce when compared to other title status.
36. Tesla, Ram, Porsche and similar luxury brands sell for more price than the other economy brands like chrysler, fiat, hyundai and saturn.
37. Pick up trucks , coup sells at higher price than the sedans and mini vans.
38. 4wd and rwd have higher prices than the fwd.
39. White, black , orange and yello shows slightly higher median prices than the green and purple cars.



Link to the [notebook](https://github.com/amairj4u/ALMLDataAssignment2/blob/main/prompt_II.ipynb)
