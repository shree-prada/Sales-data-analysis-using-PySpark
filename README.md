# Sales-data-analysis-using-PySpark

The dataset is a sample sales data containing information about orders and products sold. It has 53,130 records and various columns. 
The code does the following steps:

1.	Reads the 'sales_data_sample_csv' table into a Spark DataFrame.
2.	Prints the schema of the DataFrame using the dtypes method.
3.	Selects the columns 'QUANTITYORDERED', 'PRICEEACH', 'ORDERLINENUMBER', and 'SALES' from the DataFrame and displays the results using the display method.
4.	Creates a VectorAssembler object with input columns 'QUANTITYORDERED' and 'PRICEEACH' and output column 'features'.
5.	Transforms the DataFrame by adding the 'features' column using the VectorAssembler object created in step 4 and selects the 'features' and 'total_sales' columns only.
6.	Splits the transformed DataFrame into a training set (90%) and a test set (10%) using the randomSplit method.
7.	Displays the test set using the display method.
8.	Creates a LinearRegression object with input features column 'features' and label column 'total_sales', and fits the model using the training set.
9.	Prints the coefficients and intercept of the linear regression model.
10.	Calculates and prints the root mean squared error (RMSE) and R-squared (R2) of the model on the training set.
11.	Predicts the total_sales values of the test set using the trained linear regression model and displays the predictions, actual total_sales values, and input features using the display method.
12.	Calculates and prints the R2 of the predictions using the RegressionEvaluator object.
13.	Predicts the total_sales values of the test set using a DecisionTreeRegressor model and calculates and prints the RMSE of the predictions.
14.	Displays the predictions using the show method.
15.	Predicts the total_sales values of the test set using a GBTRegressor model and displays the predictions, actual total_sales values, and input features of the first 5 records using the show method.


