# Day 2 – Recurrent Neural Networks (RNN)
## Objective

Build and train a Recurrent Neural Network (SimpleRNN or LSTM) to predict stock prices using the Tesla stock dataset. Evaluate performance using regression metrics and visualize predictions.

## Tasks

Load the Tesla stock price dataset.

Preprocess the data (scaling, supervised sequence framing, train-test split).

Build and train an RNN (SimpleRNN/LSTM) to predict the next-day opening price.

Evaluate using regression metrics (MAE, RMSE).

Visualize predictions vs actual values.


## Core Concept Questions & Answers

## 1. What is the benefit of using RNNs (or LSTMs) over traditional feedforward networks for time-series data?
Traditional feedforward networks treat inputs independently and fail to capture temporal relationships. RNNs, and especially LSTMs, are designed to handle sequential dependencies by retaining past information. This memory aspect makes them powerful for time-series forecasting tasks like stock prices, where future values depend heavily on historical patterns.

## 2. Why is sequence framing (input windows) important in time series forecasting?
Sequence framing restructures time-series data into supervised learning format, where previous values (windows) are used to predict the next step. Without this, models cannot learn temporal relationships. By providing historical context, sequence framing ensures that the network captures meaningful trends, making predictions more reliable and accurate.

## 3. How does feature scaling impact training of RNN/LSTM models?
Feature scaling normalizes all inputs into a consistent range, typically between 0 and 1. This prevents features with large magnitudes from dominating the learning process. Scaled inputs stabilize training, improve gradient flow, and speed up convergence, ultimately enabling RNNs and LSTMs to learn patterns more effectively and accurately.

## 4. Compare SimpleRNN and LSTM in terms of handling long-term dependencies.
SimpleRNNs can capture short-term dependencies but struggle with long-term sequences due to vanishing gradients. LSTMs overcome this limitation through gated mechanisms that regulate information flow, allowing them to retain important patterns for longer periods. This makes LSTMs more effective in tasks like stock price forecasting, where past context matters significantly.

## 5. What regression metrics (e.g., MAE, RMSE) are appropriate for stock price prediction, and why?
For stock prediction, metrics like MAE and RMSE are more meaningful than accuracy since outputs are continuous values. MAE provides the average prediction error, offering interpretability. RMSE penalizes larger errors more, making it sensitive to big deviations. Both help evaluate how close predictions are to actual stock values.

## 6. How can you assess if your model is overfitting?
Overfitting occurs when the model memorizes training data instead of generalizing. A clear sign is low training loss but high validation or test loss. Monitoring learning curves helps identify overfitting, as the gap between training and validation performance widens, indicating the model is not performing well on unseen data.

## 7. How might you extend the model to improve performance (e.g., more features, deeper network)?
Model performance can be improved by introducing additional features like trading volume, moving averages, or market indicators. Architecturally, deeper LSTM layers or hybrid models can capture more complex relationships. Regularization methods such as dropout, along with hyperparameter tuning, further enhance the ability to generalize and avoid overfitting.

## 8. Why is it important to shuffle (or not shuffle) sequential data during training?
For sequential data like stock prices, shuffling can break temporal order, leading to meaningless training. Since the sequence matters, data should be framed into windows while maintaining order. However, within batches, careful handling may be applied to balance training efficiency and preservation of time-based dependencies.

## 9. How can you visualize model prediction vs actual values to interpret performance?
Visualizing predictions against actual stock prices helps assess how well the model tracks real market movements. Line plots are often used, showing true values and predictions over time. This provides intuitive insights into trends, errors, and whether the model consistently follows upward or downward stock price movements.

## 10. What real-world challenges arise when using RNNs for stock price prediction?
Stock price prediction faces challenges due to market volatility, news impact, and unpredictable events. RNNs may overfit to historical data and fail to adapt to sudden changes. Additionally, financial data is noisy and non-stationary, making it difficult for even sophisticated models to generalize and deliver consistent accuracy.
