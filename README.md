# Truebeacon-Quant Research Project

## Overview
This repository contains the code and documentation for the pairs trading strategy developed as part of the TrueBeacon intern assignment. The project aims to build and optimize a medium-frequency trading strategy based on the volatility spread between Nifty and Bank Nifty indices.

## Project Structure
'data.parquet': The dataset containing minute-level implied volatilities (IVs) of Bank Nifty and Nifty, along with Time To Expiry (TTE) for the series.
'pairs_trading_strategy.py': The main Python file containing the implementation of the pairs trading strategy.
'requirements.txt': List of required Python packages.

## Assumptions
1. The dataset may contain missing values, and these are handled by Pandas 'isnan' function.
2. The trading horizon for the strategy ranges from 30 minutes to 5 days.

## Implementation
### Base Model: Z-Score
The base model follows a z-score-based approach. The z-score of the spread between Bank Nifty IV and Nifty IV is calculated and used to identify divergence from the historical mean. Trades are executed based on the z-score thresholds.

### Modified Model: Moving Average(MA)
The moving average model is a time series model that accounts for very short-run autocorrelation.



