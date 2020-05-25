## Introduction

Forecasting of future data is very valuable in the Energy sector where information about future consumption and generation trends can help plan the operation of plants. This analysis compares different kinds of models for time series forecasting to determine which model works the best

## Data

The data has been sourced from Kaggle: https://www.kaggle.com/robikscube/hourly-energy-consumption 
It contains power consumption readings for various electricity companies in MegaWatts (MW). The Dayton dataset has been used for this analysis. However, a master dataset containing data from all the power companies has been used at the end for an experimental model. 

<img src="https://github.com/Eashani/Timeseries-Analysis-Energy-Data-/blob/master/pic1dayton.png" alt="Sample data_dayton" width="300" height="300">

## Data Exploration

The data starts from approximatelty 2005 to 2018 and has been recorded per hour.
<img src="https://github.com/Eashani/Timeseries-Analysis-Energy-Data-/blob/master/dayton_hourly.png" alt="Sample data_dayton" width="700" height="300">

## Analysis

The 4 models used have been FBProphet, XGBoost, Recurrent neural networks (RNN) and Long Short Term Memory (LSTM) (a variation of RNN)
The data has been normalized prior to usage. The FBProphet, RNN and LSTM models can work with the timestamp data as is but XGBoost requires the timestamp to be broken down into individual components. All of these models have been run on the Dayton dataset. However, an experimental XGBoost model using the whole dataset has also been tested to check if it works.

## Results

Root mean squared error (RMSE) was used as the error metric. The neural network models had the lowest RMSE and were the best

<img src="https://github.com/Eashani/Timeseries-Analysis-Energy-Data-/blob/master/rmse.png" alt="Sample data_dayton" width="400" height="300">

Looking at the plots for predicted vs observed data (Blue: predicted, Red: observed),

### FBprophet 
<img src="https://github.com/Eashani/Timeseries-Analysis-Energy-Data-/blob/master/prophet.png" alt="fbprophet" width="700" height="300">

### XGBoost 
<img src="https://github.com/Eashani/Timeseries-Analysis-Energy-Data-/blob/master/xgboost.png" alt="xgboost" width="700" height="300">
<img src="https://github.com/Eashani/Timeseries-Analysis-Energy-Data-/blob/master/xgboost2.png" alt="xgboost2" width="700" height="300">

### RNN 
<img src="https://github.com/Eashani/Timeseries-Analysis-Energy-Data-/blob/master/rnn.png" alt="rnn" width="700" height="300">

### LSTM

<img src="https://github.com/Eashani/Timeseries-Analysis-Energy-Data-/blob/master/lstm.png" alt="lstm" width="700" height="300">
