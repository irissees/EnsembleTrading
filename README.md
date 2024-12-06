# Ensemble Trading with Robinhood API

## Overview
This module leverages advanced machine learning models—**XGBoost**, **LightGBM**, and **CatBoost**—to predict overnight changes in stock prices within the stock market using the Robinhood API. It is particularly suited for smaller trading accounts aiming to generate income while adhering to the **Pattern Day Trader Rule**.

## Key Features
- **Stock Data Retrieval**: Automatically fetches daily stock data for the past five years using the **Robinhood API**.
- **Feature Engineering**: Incorporates:
  - **Time2Vec** for encoding month and day.
  - Open, High, Low, Close (**OHLC**) prices.
  - Volume
  - Stock symbol
- **Prediction Target**: Predicts the **percent change** between today's close and tomorrow's open price.
- **Evaluation Metric**: Optimizes for \( R^2 \), ensuring minimized variance in predictions.

## How It Works
1. **Input**: A list of stock symbols.
2. **Data Processing**: Fetches historical stock data and prepares features.
3. **Model Training**: Trains ensemble models on the data to predict overnight price changes.
4. **Output**: Predictions for the percent change between today’s close and tomorrow’s open.

## Installation
Ensure you have Python installed, then set up the required dependencies by running:

```bash
pip install -r requirements.txt
```
## Benefits
- **Optimized for Overnight Trading**: Focuses on predicting short-term changes, ideal for traders with smaller accounts.
- **Pattern Day Trader Rule Compliance**: Avoids frequent intraday trades while maintaining income potential.
- **Ensemble Learning**: Combines the power of multiple state-of-the-art models for better accuracy.
- **Data-Driven Strategy**: Based on studies showing that a significant portion of stock price movements occurs **overnight** rather than during intraday trading hours, making this approach particularly effective.
![Untitled](https://github.com/user-attachments/assets/adde4227-4f4c-48a6-88c2-6addd7f72d89)


## Requirements
- A list of stock symbols you want to analyze.
- Access to **Robinhood Account** for stock data retrieval.

## Insert Username/Password here:
```python
account = r.login(username='',password='') #Fill in Email/Password
```
## Change stock symbols here:
```python
tickerList = ['AAPL', 'TSLA', 'GOOGL']
```
### Run rest of the blocks to train models and make predictions
