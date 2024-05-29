# Project Name
> Prediction of Demand for Shared Bikes

## Table of Contents
Step 1: Reading and Understanding the Data
    - Data Cleaning
    - Standardization of data for better interpretation
    - Visualizing the data
    - Univariate and Bivariate analysis
 Step 2 Preparing the Data for Modeling
    - introducing dummy variables to categorical values
    - Splitting into train and test set
    - Rescaling the features
Step 3 Training the Model
    - Calculating Variable Inflation factor for all variables.
    - Dropping columns one by one. Find the R2 value
Step 4 Residual Analysis
- Model building Using RFE(Recursive Feature Elimination)
Step-5 Predictions and Evaluation on the test set



<!-- You can include any other section that is pertinent to your problem -->

## General Information
- Provide general information about your project here.
    Prediction of Demand for Shared Bikes. Building Linear regression model to predict the bike demand.

- What is the business probem that your project is trying to solve?

Problem Statement:
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

A US bike-Sharing provider BoomBikes has recently suffered revenue dips due to pandemic situation. The Company is finding very difficult in to sustain in the current market scenaro. Thay have planned to prepare themselves to cater to the people's needs once the situation gets better..So they want to understand the factors affecting the demand for these shared bikes in the American market.

The company wants to know

Which variables are significant in predicting the demand for shared bikes.
How well those variables describe the bike demand

- What is the dataset that is being used?

day.csv contains
instant: record index
	- dteday : date
	- season : season (1:spring, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2018, 1:2019)
	- mnth : month ( 1 to 12)
	- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : temperature in Celsius
	- atemp: feeling temperature in Celsius
	- hum: humidity
	- windspeed: wind speed
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
The equation for the best fit line is
Total Bike Demand = 0.2318 + 0.4657 x temp + 0.2355 x yr -0.1562 x windspeed -0.0836 x season_spring + 0.0398 x season_summer + 0.0758 x season_winter - 0.0529 x weekday_Monday -0.0282 x weekday_Tuesday - 0.0759 x weathersit_Cloudy -0.2811 x weathersit_Light-Rain
Temp is having higher positive coefficient, so temperature is major influencing factor on the increase of bike demand.
Similarly year is having next highest coefficent. season summer and winter also influencing the increase of bike demand.
When there is Rain and cloudy and windspeed reduces the bike demand due to negative coefficents.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
Python 3.0 libraries
Numpy, pandas, statsmodel for building linear regression model.
sklearn for RFE feature selection, model_selection for train test split, metrics for r2_score.

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- Upgrad
- Based on the tutorial of Simple linear regression and Multiple linear regression.

## Contact
Created by [@settumurugan] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->