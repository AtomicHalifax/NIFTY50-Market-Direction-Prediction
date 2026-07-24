# NIFTY50 Market Direction Prediction

> 📈 An end-to-end Machine Learning pipeline for predicting the next-day direction of the NIFTY 50 Index using historical market data, global financial indicators, and technical analysis.


<p align="center">

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?style=for-the-badge&logo=scikitlearn)
![XGBoost](https://img.shields.io/badge/XGBoost-Boosting-red?style=for-the-badge)
![LightGBM](https://img.shields.io/badge/LightGBM-Gradient%20Boosting-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-success?style=for-the-badge)

</p>

---

## 🚀 Overview

Predicting financial markets is a challenging time-series classification problem due to market volatility, non-linearity, and continuously changing economic conditions.

This project develops a complete **Machine Learning pipeline** to predict the **next-day direction of the NIFTY 50 Index** by combining domestic market data, global financial indices, currency exchange rates, commodity prices, and engineered technical indicators.

Rather than focusing solely on model performance, this repository emphasizes **reproducible experimentation**, **systematic feature engineering**, and **engineering best practices** throughout the complete ML lifecycle.

---

# End-to-End Workflow

<img width="1536" height="1024" alt="Workflow" src="https://github.com/user-attachments/assets/590316a2-1fd7-4ed6-a204-0efdc0321dbf" />


The project follows a structured machine learning workflow beginning with historical market data collection and progressing through preprocessing, feature engineering, chronological data splitting, model development, hyperparameter tuning, feature refinement, and final evaluation.

This modular workflow ensures reproducibility while minimizing data leakage in a financial time-series environment.

---

# Project Architecture

<img width="1376" height="768" alt="image" src="https://github.com/user-attachments/assets/217c43ee-a598-429b-ab05-b5fc799629cb" />

The architecture integrates multiple financial markets into a unified prediction pipeline.

### Data Sources

- NIFTY 50
- India VIX
- S&P 500
- NASDAQ Composite
- Dow Jones Industrial Average
- USD/INR Exchange Rate
- Crude Oil Futures

These datasets are synchronized chronologically before feature engineering and model training.

---

# Key Features

- 📊 End-to-end machine learning workflow
- 📈 Multi-market financial data integration
- ⚙️ Technical indicator feature engineering
- 📅 Chronological train-validation-test splitting
- 🤖 Comparative evaluation across multiple ML algorithms
- 🎯 Hyperparameter tuning and feature refinement
- 📚 Complete project documentation for reproducibility

---

# Machine Learning Pipeline

<p align="center">
<img width="1376" height="768" alt="image" src="https://github.com/user-attachments/assets/04e1bdde-84d1-4cdf-9caa-1c52f1e9f302" />


The pipeline was designed following a modular architecture where each stage can be independently reproduced, validated, and improved.

Major stages include:

1. Data Collection
2. Data Cleaning
3. Feature Engineering
4. Time-Series Splitting
5. Model Development
6. Hyperparameter Optimization
7. Feature Selection
8. Performance Evaluation

---

# Data Collection

<p align="center">
<img width="1376" height="768" alt="image" src="https://github.com/user-attachments/assets/f70032bc-24d2-48f8-823b-9bc7f4bff7dd" />

Historical market data was collected using the **Yahoo Finance API (yfinance)**.

## Dataset Summary

| Property | Value |
|-----------|-------|
| Data Source | Yahoo Finance |
| Market | NIFTY 50 |
| Auxiliary Markets | VIX, S&P 500, NASDAQ, Dow Jones, USD/INR, Crude Oil |
| Frequency | Daily |
| Period | 2008 – 2026 |
| Prediction Task | Binary Classification |

The collected datasets were aligned by trading date before preprocessing and feature generation.

---

# Feature Engineering

<p align="center">
<img width="1376" height="768" alt="image" src="https://github.com/user-attachments/assets/9f92e72a-5753-4416-9aa1-4f53a8f6ccef" />


Raw market prices alone rarely capture the complete dynamics of financial markets.

To improve predictive capability, several technical indicators were engineered to represent trend, momentum, and volatility.

## Trend Indicators

- Simple Moving Average (SMA)
- Exponential Moving Average (EMA)

## Momentum Indicators

- Relative Strength Index (RSI)
- MACD
- Rate of Change (ROC)

## Volatility Indicators

- Bollinger Bands
- Average True Range (ATR)
- Rolling Volatility

These engineered features significantly enriched the information available to the learning algorithms.

---
