# Stock Price Forecasting and Anomaly Detection with VAE and Transformer

This project implements a pipeline for **stock price anomaly detection** using a Variational Autoencoder (VAE) and **future price forecasting** using an Enhanced Transformer model inspired by the paper "Attention is All You Need". Additionally, a simple **trading strategy** is built based on the model's predictions and detected anomalies.

---

## Overview

This repository focuses on detecting anomalies in stock price time series data using a Variational Autoencoder (VAE) and leveraging an Enhanced Transformer model for multi-step future price forecasting. The pipeline also includes:
- Feature engineering with technical indicators like **Moving Averages (MA)** and **Relative Strength Index (RSI)**.
- A simple rule-based **trading strategy** for actionable insights based on detected anomalies and price predictions.
- Full end-to-end documentation available in a **Google Colab Notebook**.

---

## Features

- **Technical Feature Engineering**:
  - Compute **7-day Moving Average (MA7)**, **21-day Moving Average (MA21)**, and **RSI (14)**.
- **Anomaly Detection**:
  - Use a **Variational Autoencoder (VAE)** with LSTM encoder-decoder architecture.
  - Dynamically compute anomaly thresholds using reconstruction error percentiles.
  - Visualize anomalies on stock price time series.
- **Future Price Forecasting**:
  - Enhanced **Transformer model** with:
    - Multi-head attention layers.
    - Positional encoding for temporal data.
    - Capability for multi-step forecasting.
- **Trading Strategy**:
  - Generates **Buy**, **Sell**, or **Hold** signals based on price predictions and recent anomalies.
  - Risk mitigation features (e.g., stop-loss recommendations).
- **Interactive SHAP Explanations**:
  - Use **SHAP** to explain anomalies and identify which features contribute most to high reconstruction errors.

---

## TODO:
Currently the models do not generalise well to stocks that see extreme increases / drops in price in a short period. 
