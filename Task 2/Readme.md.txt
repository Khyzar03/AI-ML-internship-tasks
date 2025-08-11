Task 2: Predict Future Stock Prices (Short-Term)

Objective:
Use historical stock data to predict the next day's closing price.

Dataset Used
Source: Yahoo Finance (yfinance Python library)
Ticker: AAPL (Apple Inc.)

Features:

Open: Opening price of the day
High: Highest price during the day
Low: Lowest price during the day
Volume: Number of shares traded
Close: Closing price of the day (target variable)



Algorithm Used: Linear Regression (from sklearn.linear_model
Training: Model trained on past daily stock prices with 80% training and 20% testing split.

Important Findings and Results
Although the model has limits for extremely volatile fluctuations, it was able to reflect the overall trend of Apple's closing price.

Next-Day Closing Price Prediction: Based on the most recent data available, the model predicted a closing price for the following day that was fairly close to the real trend (the precise figure changes based on the run date).

Observation: Although linear regression offers a solid foundation, more sophisticated models like Random Forests, Gradient Boosting, or LSTM neural networks can increase the accuracy of stock price predictions.

Visualization: The model performs well during stable times but poorly during abrupt spikes or declines, according to scatter plots and line charts that compare actual and projected values.