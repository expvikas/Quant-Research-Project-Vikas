# Truebeacon-Quant Research Project

## Overview
This repository contains the code and documentation for the pairs trading strategy developed as part of the TrueBeacon intern assignment. The project aims to build and optimize a medium-frequency trading strategy based on the volatility spread between Nifty and Bank Nifty indices.

## Project Structure
**data.parquet**: The dataset containing minute-level implied volatilities (IVs) of Bank Nifty and Nifty, along with Time To Expiry (TTE) for the series.<br>
**trading_strategy.py**: The main Python file containing the implementation of the pairs trading strategy. <br>
**trading_strategy.xlsx**: The Excel file inside the output of the result. <br>
**requirements.txt**: List of required Python packages. <br>
**Full_Data.png**: This image is the output of full-data trading strategies.<br>
**One_day_data.png**: This image outputs a one-day '2021-10-11' trading strategy.


## Assumptions
1. The dataset may contain missing values handled by Pandas 'isnan' function.
2. The trading horizon for the strategy ranges from 30 minutes to 5 days.

## Implementation
### Base Model: Z-Score
The base model follows a z-score-based approach. The z-score of the spread between Bank Nifty IV and Nifty IV is calculated and used to identify divergence from the historical mean. Trades are executed based on the z-score thresholds.

### Modified Model: Moving Average(MA)
A moving average model is a statistical technique commonly used in time series analysis to smooth out fluctuations in data and identify trends over time. It is beneficial for detecting patterns or trends in noisy data sets.

## Performance Values
The performance of both the base and modified models is evaluated based on the following metrics:
### Base Model
1. Absolute P/L: -26.785552670145883
2. Sharpe Ratio: -0.060677269687343514
3. Drawdown: -26.786400988028007
### MA Model
1. Absolute P/L: -26.785552670145883
2. Sharpe Ratio: -0.060677269687343514
3. Drawdown: -26.786400988028007

## Submission
The submission includes the GitHub link to this repository and the complete Python code base.
