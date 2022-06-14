# Rainfall prediction: Random forest vs Logistic Regression
Here I made point predictions of Rainfall in Australia and tested accuracy of Logistic Regression vs Random Forest Classifier


## Introduction

In this project, I studied how to build a useful and accurate model to predict rainfall, an important factor in agriculture, in major cities in Australia. I used the data set from Kaggle which provides 10-year rainfall information in the location we are aiming to make predictions. 

The two major algorithms used in this project are Random Forest Classifier and Logistic Regression. 

Along with that, interpretability is also one of the major goals in this project as the target clients would be farmers who do not have much technical knowledge and require simpler explanations of the models as well the finding results. Therefore, I built a visualization dashboard using Tableau to better understand the model prediction. 

Repo content:
1. Python notebook source code - Rainfall Prediction.ipynb
2. Input data - weatherAUS.csv  
You may also find this dataset by this link https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package  
4. Output data - Australia_forecast.csv
5. Dashboard - Rain_forecast.twbx


## Problem Statement

![something](https://imageresizer.static9.net.au/XyOKqmK3wHiqtHn8kZrUZ_N120Q=/1200x628/smart/https%3A%2F%2Fprod.static9.net.au%2Ffs%2F5e95d05e-ce2c-4ac7-8066-ef40c53d82a7)

In agriculture, one of the major factors that would affect the season outcome is weather conditions. Farmers make decisions based on daily weather changes, involving factors such as: fertilizing, crop growth and irrigation. 

Crops are sensitive to moisture, light, and temperature. Firstly, with historical and prediction information, it is easier to track crop growth and decide when and how much to irrigate. Secondly, fertilizer timing and delivery, which can ensure the effectivity by fitting process to specific weather conditions. For example, it is a well know agricultural fact that nitrogen fertilizers are the most efficient to be applied before rainfall if it is not going to be too intense. However, treatment of plants to protect against weeds is not efficient to be applied before the rain as applied treatment tools are going to be washed away from a field. Finally, under some extreme weather conditions, the field will not be suitable for farmers to work on.

As a result, the weather forecast has long been a focus for agriculture. Weather condition prediction is essential for precision agriculture and the ultimate goal of weather prediction is to optimize the growth efficiency of individual crops. Among the weather conditions, rainfall is one of the most important factors which is related to each of the three examples above since it directly influences the moisture level as well as field workability.

Climate changes are a major factor affecting agriculture in Australia as variety of climates are present in the country due to its geographical size and placement. The main issue attributed to importance is presence of frequent droughts. As major part of Australian continent is a desert and according to Wikipedia “more than 80% of the country has an annual rainfall of less than 600 mm”. 

Consequently, rainfall forecasts are an essential tool for agricultural entrepreneurs in those regions as their business processes are highly dependent on that factor.

Although the data set is limited to Australia, the model can always be expanded to other regions in which rainfall predictions would benefit in any mean.  

## Data

The data adopted for the model is 10 years’ daily weather observations from major areas in Australia.   
Features include:  
1. Date, the date of observation; 
2. Location, the common name of the location of the weather station;  
3. MinTemp, the minimum temperature in degrees Celsius; 
4. MaxTemp, the maximum temperature in degrees celsius;  
5. Rainfall, the amount of rainfall recorded for the day in mm;  
6. Evaporation, the so-called Class A pan evaporation in the 24 hours to 9 am, etc.  
7. The target variable is a binary variable RainTomorrow, which indicates whether rainfall appears tomorrow.   

![something](https://github.com/BananZza1998/Snaps_1/blob/main/Data_snap.png?raw=true)   


The complementary data used to visualize the model is the latitude and longitude of each unique area in the dataset, which is obtained from the open API geographical data source positionstack.com   

Data cleaning process includes conversion of dates into the appropriate format, replacing empty values with average values and dropping columns with more than 10% of missing data for each location. Additionally, I convert all categorical variables from their string values to integer indices.   

After cleaning the data, what is left is 48 major cities/areas in Australia adding up to 140k entries for the main data set.    

(Check the code for model setup and data processing)    

## Setup

Both models are well-known in the weather forecast sectors. The coefficients in logistic regression are easy to interpret after log and odds transformation. For the random forest model, the intuition is weighted votes of different trees, and decision trees are able to interpret too.
Considering each location separately, it is predicted for each day whether it will rain or not tomorrow. Regarding in/out of sample split, I set data before 2016 as the in-sample set, and 2017 data as the out-of-sample set. Train-test split is 80 to 20 percent respectively. The prediction accuracy for both models is roughly similar, which is greater than 75% in the lowest-accurate city and generally greater than 85% on the whole test set.


## Outcome

### Visual

I visualized the model prediction in Tableau, which is easier to comprehend for the general audience.  
Users would be able to choose the date to view the forecast and click on the triangle button to play the animation.  
Also, visualization allows to check prediction accuracy at different levels: location and date. (.twbx file in the repo)

![Dashboard](https://github.com/BananZza1998/Snaps_1/blob/main/Dashboard.png?raw=true)   


### Model comparison

Regarding model comparison, I consider Random Forest Classifier to be slightly better due to stable output for the whole dataset. Despite both models provide similar accuracy, the Logistic Regression appears to have null prediction scores for several locations.


![Performance](https://github.com/BananZza1998/Snaps_1/blob/main/Performance.png?raw=true)   










