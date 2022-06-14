# Rainfall Random forest vs Logistic Regression
Here I made point predictions of Rainfall in Australia and tested accuracy of Logistic Regression vs Random Forest Classifier


## Introduction

In this project, I studied how to build a useful and accurate model to predict rainfall, an important factor in agriculture, in major cities in Australia. I used the data set from Kaggle which provides 10-year rainfall information in the location we are aiming to make predictions. 

The two major algorithms used in this project are Random Forest Classifier and Logistic Regression. 

Along with that, interpretability is also one of the major goals in this project as the target clients would be farmers who do not have much technical knowledge and require simpler explanations of the models as well the finding results. Therefore, I built a visualization dashboard using Tableau as one of the deliverables to better understand the model prediction. Finally, we analyzed the model results and made recommendations on model selection in predicting rainfall for agriculture.


Repo content:
1. Python notebook source code - Rainfall Prediction.ipynb
2. Input data - weatherAUS.csv  
You may also find this dataset by this link https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package  
4. Output data - Australia_forecast.csv
5. Dashboard - Rain_forecast.twbx


## Problem Statement

In agriculture, one of the major factors that would affect the season outcome is weather conditions. Farmers make decisions based on daily weather changes, involving factors such as: fertilizing, crop growth and irrigation. 

Crops are sensitive to moisture, light, and temperature. Firstly, with historical and prediction information, it is easier to track crop growth and decide when and how much to irrigate. Secondly, fertilizer timing and delivery, which can ensure the effectivity by fitting process to specific weather conditions. For example, it is a well know agricultural fact that nitrogen fertilizers are the most efficient to be applied before rainfall if it is not going to be too intense. However, treatment of plants to protect against weeds is not efficient to be applied before the rain as applied treatment tools are going to be washed away from a field. Finally, under some extreme weather conditions, the field will not be suitable for farmers to work on.

As a result, the weather forecast has long been a focus for agriculture. Weather condition prediction is essential for precision agriculture and the ultimate goal of weather prediction is to optimize the growth efficiency of individual crops. Among the weather conditions, rainfall is one of the most important factors which is related to each of the three examples above since it directly influences the moisture level as well as field workability.

Climate changes are a major factor affecting agriculture in Australia as variety of climates are present in the country due to its geographical size and placement. The main issue attributed to importance is presence of frequent droughts. As major part of Australian continent is a desert and according to Wikipedia “more than 80% of the country has an annual rainfall of less than 600 mm”. 

Consequently, rainfall forecasts are an essential tool for agricultural entrepreneurs in those regions as their business processes are highly dependent on that factor.

Although the data set is limited to Australia, the model can always be expanded to other regions in which rainfall predictions would benefit in any mean.

