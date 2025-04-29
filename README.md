# U.S. Nuclear Production Time Series Analysis and Forecasting

- [Introduction](#introduction)
- [How to Use](#how-to-use)
- [Methods](#methods)
- [Results ](#results)

## Introduction
This project aims to forecast nuclear energy production using time series analysis. The goal is to develop a predictive model that can forecast future nuclear energy production based on historical data. The ARIMA model (AutoRegressive Integrated Moving Average) is used to analyze and predict trends, and its performance is evaluated using RMSE (Root Mean Squared Error).

## How to Use
1. Download the .ipynb file.
2. Download the "Primary energy production by source" dataset from [U.S. Energy Information Administation's website](https://www.eia.gov/totalenergy/data/annual/index.php)
3. Ensure that the .ipynb file and the .xlsx file are in the same folder, or that you have made the necessary changes to the file path in the code.
4. Ensure you have the libraries pandas, seaborn, matplotlib, statsmodels, pmdarima, and sklearn installed on your machine. (NOTE: pmdarima may require you to downgrade your version of numpy to anything less than version 2.0)
6. Run the notebook!

## Methods
The data were first loaded and preprocessed, ensuring proper data types and indexing. Then preliminary visualizations were created. Next, time series analysis using rolling mean and standard deviation was conducted. 

![Nuclear Production Rolling](images/nuclear%20rolling%20mean.png)

This was followed by ADF and autocorrelation testing as well as trend decomposition. Then, the data were split into train and test sets and time series forecasting was done using ARIMA. 

![Nuclear Production TestTrain](images/nuclear%20train%20test.png)

The ARIMA model was finally evaluated using RMSE.

## Results

The U.S.'s nuclear electric energy production was shown to have increased greatly from 1973 to about 2000, when it then leveled off and remained stable up until the present day. 

![Nuclear Production Line Plot](images/nuclear%20line%20plot.png)

The data was shown to be stationary, autocorrelated, and non-seasonal. 

![Nuclear Production Trend Decomp](images/nuclear%20trend%20decomposition.png)

The ARIMA(3,1,5)(0,0,0)[0] model was able to effectively forecast nuclear energy production with a low RMSE of 0.04, indicating good prediction accuracy. 

![Nuclear Production TestTrainPred](images/nuclear%20train%20test%20pred.png)
