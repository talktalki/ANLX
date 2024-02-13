# Stock Price Prediction Using Time Series Forecasting

## Project Overview
- Background: In late January 2021, GameStop (GME), a video game retailer, became the center of a financial phenomenon known as a 'short squeeze.' This occurred when a surge of retail investors, coordinating through social media platforms like Reddit's r/wallstreetbets, began buying up GameStop's stock. This drove up the stock price dramatically, which in turn inflicted heavy losses on hedge funds and other investors who had bet against the stock by short-selling it. The event drew widespread media attention, sparked controversy over stock market practices, and led to hearings in the U.S. Congress.
- Objective: In this project, I build a stock price prediction model (LSTM) incorporating both **historical stock market data and social media sentiment** to predict daily closing prices between June 2021 and August 2021, a total of 90 days.
The LSTM network is specifically designed to capture long-term dependencies and has proven to be effective in time series forecasting tasks. I then evaluate its accuracy on the GameStop short squeeze, and analyze potential improvements based on the event.

## Dataset
- Historical Stock Price: Yahoo Finance (accessed programmatically via yfinance in Python)
  - January 4th, 2021 - August 31st, 2021
- Reddit Sentiment: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/TUMIPC (rGME_dataset_features.csv)
  - January 4th, 2021 - December 31st, 2021

## Part 1: Model Building
1. Time-series forecasting: This model will focus on historical stock price data, employing neural network architectures like LSTMs to capture sequential patterns and long-term dependencies.
2. Sentiment analysis: Uses sentiment scores captured in the rGME_dataset_features.csv dataset
3. Model fusion: This model will combine the predictions from both the time-series forecasting and sentiment analysis to perform the final predictions.

## Part 2: Model Training & Evaluation
The LSTM model is built using deep learning framework PyTorch. Model is trained on the training dataset, which is the time period Jan 2021 to May 2021.
Hyperparameter tuning is done on the number of hidden layers, the number of neurons per layer, and the learning rate. 
Once the model is trained, its performance is evaluated on the testing dataset, which is the time period June 2021 to September 2021. Metrics used to assess the model's accuracy are mean squared error (MSE), root mean squared error (RMSE), and mean absolute error (MAE). 
I visualize the predicted stock prices alongside the actual prices to gain insights into the model's performance.

## Part 3: Model Adaptation
The model's predictions did not change significantly even after adding simulated spikes in social media sentiment. This indicates that the current model may not be effectively capturing the impact of extreme sentiment on stock prices. Some potential modifications and feature engineering approaches that could improve its performance are:
- Incorporating features related to stock market volatility, trading volume, and historical price movements. These features can provide context and help the model better understand the relationship between sentiment and stock prices.

## Part 4: Concusion and Future Directions
The GameStop short squeeze had a profound impact on the effectiveness of traditional forecasting models and highlighted the potential value of incorporating social media sentiment data in financial analysis. Here's an analysis of these aspects along with a discussion on the ethics of social media mining:

## Packages Used
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
