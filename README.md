# Geospatial-Analysis-and-Temperature-Prediction

Dataset: https://drive.google.com/drive/folders/1J0abkMosgloUCfJXA3qGYE4NpNq7wNVw?usp=sharing

#### Abstract
The aim of the project is to analyse the dataset to find the evidence of global warming, find seasonal trends in temperature of Indian states, plotting these observations on the map and develop a Time Series Model to predict the temperature of few major cities of India. A time series model involves working on time based data, to derive hidden insights for predictions and informed decision making. These models generally run on serially correlated data. In this project, I have used state of the art libraries and well established time series techniques to predict temperature.The different datasets used for analysis contains temperature data from years 1750-2015.

With pre-processing of data some strong insights were prominent, 
Here are some of the observations:

![image](https://user-images.githubusercontent.com/49190511/117656674-41bcf980-b1b6-11eb-9df4-c7d9173fe8dd.png)
###### In this chart we can notice the increase in temperature from 1960s, thus manifesting global warming.




![image](https://user-images.githubusercontent.com/49190511/117657339-14248000-b1b7-11eb-996f-6f8d15b7cb52.png)
###### Increase in average temperature of India is evident.




![image](https://user-images.githubusercontent.com/49190511/117657754-914ff500-b1b7-11eb-832d-401688b2a7e9.png)
###### Plotting the average temperature of different states of India on the world map using opencage. The latitudes & longitudes of each state were scrapped from opencagedata.com 




![image](https://user-images.githubusercontent.com/49190511/117658220-1dfab300-b1b8-11eb-8efe-e14c4cc71ecd.png)
###### Creating the heatmap of each state to observe the seasonal trend of India.



Next step is to test the stationarity of the data for the time series model. A stationary process has the property that the mean, variance and autocorrelation structure do not change over time.

There are two test performed on the data to test it's stationarity . 
1) Visualizing the line plot 
2) Dickey Fuller test

On the basis of the result of Dickey Fuller test, first order differencing of the data is performed. The updated data is passed through the Moving Average & ARIMA models. 
The data is passed within a window of 7 steps to the MA model resulting in MSE of 1.20

Then acf, pacf plots were analysed to get the q and p values. These values are passed into the ARIMA model resulting a MSE of 1.46.
The values passed as p,d,q to the ARIMA model are p=5,d=0,q=9

Here, p is partial autocorrelation factor 
      q is autocorrelation factor
      and, d is the differencing factor 
