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
1) Multiple Linear Regression: 
<br> The <i>sklearn</i> package has been used to import <i>LinearRegression</i>.
<br> The <i>intercept_</i> and <i>coef_</i> method has been used to calculated the regrssion equation.
<br>

![alt text] (https://github.com/mon2barot/Universe/blob/master/images/FDMLR1.JPG "Multiple Linear Regression")



