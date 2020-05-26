<h1> Data Science Project Overview: Flight Delay Analysis </h1>

<b> The goal of the project is to predict the delay times of particular flights. </b>

<ul>
<li>The dataset has 3 files named airlines, airports and flights. All are in the csv format. 
The focus for this project has mainly been on the flights.csv file. 
The dataset had almost 5 million rows of data and was quite dirty and hance the first step was data wrangling.</li>
<li> After preprocessing the data, three models were applied viz; Multiple Linear Regression, Random Forest and XGBOOST.</li>
<li>Finally the model accuracies were determined and the delay times for flights were caluclated</li>
</ul>

<h1> Code and Resources Used </h1> 
<b>Python Version:</b> 3.7.4<br>
<b>Packages:</b> Pandas, NumPy, Seaborn, Matplotlib, Sci-Kit Learn, Statsmodels<br>
<b>References:</b> <a href="https://github.com/mon2barot/Universe/blob/master/references/flight%20delay%20references"> Click here</a><br>
<b>Dataset:</b> <a href = "https://www.kaggle.com/usdot/flight-delays?select=airports.csv" >FlightDelays.csv</a>

<h1> Project Walkthrough </h1>

### Data Wrangling
<br>
1) Time was in hh:mm format which made it difficult for processing.
Hene time has been has been converted into minutes. 
<i>[Link to reference used for Time conversion](https://bit.ly/2TCxWp1)</i>
<br>
2) Some variables were not in correct format, hence data type conversion had to be done. 
For example, the variable WHEELS_ON which had values for the time a plane had it's wheels on was of type object. 
Therefore it was converted to float.  
<br>
3) Finally missing values were imputed and categorical variables were handled by creatging dummy variables. 
<br>
<br>
<i>Data cleaning is done in a separte Jupyter Notebook.</i>
<br>

### Model Building

The following three models have been applied - 
<br>

<b>1) Multiple Linear Regression: </b>
<br> The <i>sklearn</i> package has been used to import <i>LinearRegression</i>.
<br> The <i>intercept_</i> and <i>coef_</i> method has been used to calculated the regression equation.
<br>

![alt text](https://github.com/mon2barot/Universe/blob/master/images/FDMLR1.JPG "Multiple Linear Regression")


<b>2) Radndom Forest: </b>
<br> The <i>RandomForestRegressor</i> has been imported from the <i>ensemble</i> learning method of the sklearn library.
<br>

![alt text](https://github.com/mon2barot/Universe/blob/master/images/FDRF1.JPG "Random Forest")

<b> 3) Extra Gradient Boosting: </b>
<br> The <i>xgboost</i> library has been imported and the dataset has been converted into Dmatrix for faster processing. 
<br> Finally, the <i>XGBRegressor class is called and several of its hyper-parameters are set.
 <br>
  
  ![alt text](https://github.com/mon2barot/Universe/blob/master/images/FDXGB1.JPG "XGBoost")
 
  <br>
   <ul>
   <li>The fitting of every model is done via the <i>fit()</i> function on the training set .</li>
   <li>Predictions for every model have been done via the <i>predict()</i> function on the test set and the entire dataset as well.</li>
 </ul>
 ### Model Evaluation 
 
 
Every model has been evaluated by determining its R squared and RMSE values. 

1) For MLR the R squared value is 100%, which indicates overfitting. The RMSE value is 0. Hence it is not a good model. 

2) For Random Forest the R squared value is almost 100% and RMSE is a low value of 2.56. However, model indicates overfitting. 

3) For XGBoost the R square value is 70% and the RMSE value is 22.2 which is good. Hence this is a good model.

### Conclusion

XGBoost is the best model for predicting the flight delays. Take a look at the predictions in the image below.<br>
<br>

[!alt text](https://github.com/mon2barot/Universe/blob/master/images/FDXGB2.JPG "XGBoost Prediction")
<br>

From the predictions it can be understood that Alaska Airlines flight from SEA to ANC will be delayed 9 by minutes. It can also be interpreted that American Airlines flight from LAX to PBI will be 3 minutes early.

Hence, information regarding flight delays or early arrivals can be utilized to make decisions. For example the decisions regarding exit gate numbers can be made for a smoother customer experience. Furthermore, even parking spaces can adjusted such that other scheduled flights are not delayed.  
