# stock-transformer

A transformer-based model that predicts stock returns using historical price data. The model uses a Transformer architecture to learn patterns from OHLCV data and predict next day returns.

## Features

- Downloads historical stock data from Yahoo Finance for 100+ major stocks
- Feature engineering including returns, volatility, volume changes, and cyclical time encodings
- Transformer architecture with configurable layers, heads, and dimensions
- Temporal data splitting (train/validation/test) to prevent data leakage
- Per ticker standardization using training set statistics
- Early stopping and learning rate scheduling during training

## Usage

The notebook demonstrates:
1. Data download and preprocessing
2. Model training with early stopping
3. Evaluation on test set
4. Inference for specific tickers

## Model Architecture

- Input: 64-day windows of 7 engineered features
- Transformer encoder with configurable dimensions
- Output: Predicted next day return (regression) or direction (classification)
