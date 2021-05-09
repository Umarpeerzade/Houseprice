# Data Science House Price Predection: Project Overview 
* Create a model to pridict Sales Price of House from given label Data.
* Optimized Linear, Lasso, and Random Forest Regressors using GridsearchCV to reach the best model. 

## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn
## Data Visulation
After importing Data We will perform some Data Analysis and Data Visulation
like
* Bar Graph
* line Graph
*
 ![alt text](https://github.com/Umarpeerzade/Houseprice/blob/main/LinePLot.PNG)
* Heatmap to Check Relation 
* 
  ![alt text](https://github.com/Umarpeerzade/Houseprice/blob/main/heatmap.PNG)
* Scatter Plot (to check Relation between Features)
* 
![alt text](https://github.com/Umarpeerzade/Houseprice/blob/main/Scatterplot.PNG)
* Boxplot,Count Plot
* 
![alt text](https://github.com/Umarpeerzade/Houseprice/blob/main/countplot.PNG)

## Data Cleaning
*	Checking Null Values
*	Remove Null value feature having more than 40% of Data Null
*	Fill Null values By Mean/median/mode for test as well as train Data 
*	Check Outlier of Sales Price and Remove outlier
*	for that we will use Boxplot
*	
![alt text](https://github.com/Umarpeerzade/Houseprice/blob/main/boxplot.PNG)
*	Check distribution Plot whether is normalized or not
*	
![alt text](https://github.com/Umarpeerzade/Houseprice/blob/main/distr_plot.PNG)
*	To normalize Salesprice convert it to Log(salesprice)
*	after Taking log we get below Distribution plot which is near to normal distribution
![alt text](https://github.com/Umarpeerzade/Houseprice/blob/main/aftrlog.PNG)
*	Remove Unwanted features
*	Remove Dummy Variables
*	Seperate Target variable from Train data

## Model Building 

First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 20%. 

also Transform Train Data into normalize form using preprossing

I tried three different models and evaluated them using Mean Absolute Error. I chose MAE because it is relatively easy to interpret and outliers aren’t particularly bad in for this type of model.   

I tried three different models:
*	**Multiple Linear Regression** – Baseline for the model
*	**Lasso Regression** – Because of the sparse data from the many categorical variables, I thought a normalized regression like lasso would be effective.
*	**Random Forest** – Again, with the sparsity associated with the data, I thought that this would be a good fit. 

## Model performance
The Random Forest model far outperformed the other approaches on the test and validation sets. 
*	**Linear Regression**: R2 = 0.80 ,RMSE=0.068
*	**Ridge Regression**: RMSE=0.80 , RMSE=0.14
* **PCA+ Linear Regression**: R2=0.82, RMSE=0.063


