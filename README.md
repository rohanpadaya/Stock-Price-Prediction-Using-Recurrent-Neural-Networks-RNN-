# Stock Price Prediction Using Recurrent Neural Networks (RNN)

## Overview

This project aims to predict stock prices for two major companies, Apple and Samsung, using various Recurrent Neural Network (RNN) architectures. The goal is to explore and compare different RNN models, including Vanilla RNN, Enhanced RNN (with Dropout and Batch Normalization), Long Short-Term Memory (LSTM), and Gated Recurrent Unit (GRU) networks to determine the most effective model for financial time series forecasting.

## Dataset

The datasets used in this project contain historical stock prices of Apple (AAPL) and Samsung (005930.KS). The data was obtained from Yahoo Finance and includes variables such as opening price, closing price, adjusted closing price, highest and lowest price of the day, and trading volume.

- **Apple Dataset**: Historical stock data from 20th November 2018 to 17th November 2023.
- **Samsung Dataset**: Historical stock data from 20th November 2018 to 20th November 2023.

[Link to Yahoo Finance](https://finance.yahoo.com/)

## Project Files

- **AAPL.csv**: Contains the historical stock data for Apple.
- **005930.KS.csv**: Contains the historical stock data for Samsung.
- **RNNA3.ipynb**: Jupyter Notebook containing the implementation of various RNN architectures.
- **RNN_Assignment_3_Report.pdf**: Detailed report discussing the methodologies, results, and conclusions of the project.

## Methodology

1. **Data Visualization**: Initial exploration and visualization of stock price trends over time.
2. **Data Pre-Processing**: 
   - Synchronization of datasets to align on common dates.
   - Scaling and normalization of data using MinMax Scaler.
   - Structuring data into sequences for RNN input.
3. **Modeling**:
   - **Vanilla RNN**: Baseline model with 2651 trainable parameters.
   - **Enhanced RNN**: Added Dropout and Batch Normalization layers to prevent overfitting and stabilize training.
   - **LSTM**: Utilized to address the vanishing gradient problem and capture long-term dependencies.
   - **GRU**: Simplified version of LSTM, designed to be computationally efficient while handling temporal dependencies.
4. **Experimental Analysis**: Extensive evaluation of each model using Mean Squared Error (MSE) as the primary metric.

## Results

- **Apple Dataset**:
  - Vanilla RNN: MSE = 0.0004
  - Enhanced RNN: MSE = 0.0005
  - LSTM: MSE = 0.0633
  - GRU: MSE = 0.0525

- **Samsung Dataset**:
  - Vanilla RNN: MSE = 0.0003
  - Enhanced RNN: MSE = 0.0008
  - LSTM: MSE = 0.0012
  - GRU: MSE = 0.0004

The results indicate that the Vanilla RNN model outperformed other models, highlighting the importance of selecting the appropriate model based on data characteristics.

## Conclusion

The Vanilla RNN model was found to be the most effective for this specific financial time series data, outperforming more complex models like LSTM and GRU in terms of accuracy (MSE). This project demonstrates the potential of simpler models when appropriately tuned for the task at hand.

## How to Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/stock-price-prediction-rnn.git
