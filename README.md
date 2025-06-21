# Multivariate-LSTM
A multivariate LSTM (Long Short-Term Memory) model for predicting the next day's closing stock price of Google. Unlike traditional univariate time series models, this approach incorporates multiple features ("Open", "High", "Low", "Close", "Volume") to capture more complex market dynamics.

Objective:
- To build a deep learning model capable of learning patterns from 30 days of past stock data.
- Predict the next day’s "Close price" using all available features.
- Evaluate model accuracy using consistent metrics (RMSE, MAE).

Features Used:
- Open price
- High price
- Low price
- Close price (target)
- Volume

Methodology
1. Data Preprocessing:
   - Normalization using "MinMaxScaler"
   - Sequence creation using a sliding window (30-day lookback)

2. Model Architecture:
   - LSTM with 64 hidden units
   - Dropout (0.2) for regularization
   - Dense output layer for predicting a single value (next day's Close)

3. Training:
   - Loss function: Mean Squared Error
   - Optimizer: Adam
   - EarlyStopping to avoid overfitting
  
Results:
- RMSE: 3.78
- MAE: 2.84

These results indicate strong model performance, with low average error considering Google’s stock price range (typically 150–180). The LSTM model successfully captured temporal dependencies using all input features.

Visualization:
The notebook also includes a plot comparing predicted vs actual closing prices on the test set, giving a visual sense of prediction quality.

Conclusion:
Multivariate LSTM outperforms traditional models (ARIMA, univariate XGBoost) by leveraging multiple signals from the stock data. This approach demonstrates the potential of deep learning in financial forecasting.
