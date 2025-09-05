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
RNNs and LSTMs capture sequential dependencies, unlike feedforward networks. LSTMs can remember long-term patterns, which is crucial for stock forecasting.

## 2. Why is sequence framing (input windows) important in time series forecasting?
Sequence framing converts past stock prices into supervised learning format (past n steps → next step), allowing the model to learn historical trends.

## 3. How does feature scaling impact training of RNN/LSTM models?
Scaling ensures all features are in the same range, preventing dominance of large values. It stabilizes training and speeds up convergence.

## 4. Compare SimpleRNN and LSTM in terms of handling long-term dependencies.
SimpleRNN works for short-term sequences but struggles with vanishing gradients. LSTMs retain information over longer sequences using gates.

## 5. What regression metrics (e.g., MAE, RMSE) are appropriate for stock price prediction, and why?
MAE gives average prediction error, while RMSE penalizes large errors more. Both are better suited than accuracy for continuous stock values.

## 6. How can you assess if your model is overfitting?
If training loss keeps dropping but validation/test loss rises, the model is overfitting by memorizing instead of generalizing.

## 7. How might you extend the model to improve performance (e.g., more features, deeper network)?
Improvements include adding more stock indicators, deeper LSTM layers, dropout, or tuning hyperparameters like epochs and batch size.

## 8. Why is it important to shuffle (or not shuffle) sequential data during training?
Stock data should not be fully shuffled, since order matters. Maintaining sequence order ensures temporal relationships are preserved.

## 9. How can you visualize model prediction vs actual values to interpret performance?
Plot actual vs predicted prices over time to visually check if the model follows market trends and identify mismatches.

## 10. What real-world challenges arise when using RNNs for stock price prediction?
Markets are noisy and influenced by external events. Models risk overfitting and often fail to generalize well to unseen data.
