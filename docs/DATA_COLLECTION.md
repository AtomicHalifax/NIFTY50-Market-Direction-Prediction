# Data Collection 🗂️

This document explains the data collection process used for the NIFTY50 Market Direction Prediction project.

The objective was to collect historical market data from multiple financial instruments and create a unified dataset for machine learning-based market direction prediction.

The data collection pipeline followed:

Financial Data Sources
↓
Historical Data Download
↓
Data Cleaning
↓
Data Alignment
↓
Return Calculation
↓
Final Dataset Creation

---

# Data Source 📊

## Why Yahoo Finance?

Yahoo Finance was selected as the primary data source because it provides:

- Historical OHLCV market data
- Multiple global financial instruments
- Long-term historical availability
- Easy accessibility through Python using `yfinance`

The data was collected programmatically to ensure:

- Reproducibility
- Consistency
- Easy future updates

---

# Data Collection Library 🐍

The `yfinance` Python library was used to collect historical market data.

Example workflow:

```python
import yfinance as yf

data = yf.download(
    ticker,
    start=start_date,
    end=end_date
)


Market Instruments Collected 🌎

To capture both domestic and global market influences, multiple financial indicators were collected.

Indian Market Data 🇮🇳
NIFTY 50 Index

Ticker:

^NSEI

Features collected:

Open
High
Low
Close
Volume

Purpose:

Represents the overall movement of the Indian equity market.

Global Market Indicators 🌐

Global markets were included because international movements can influence Indian markets.

S&P 500

Purpose:

Represents broad US market performance.

Collected:

Open
High
Low
Close
Volume
NASDAQ

Purpose:

Captures global technology sector performance and investor sentiment.

Collected:

Open
High
Low
Close
Volume
Dow Jones

Purpose:

Represents large-cap US market movements.

Collected:

Open
High
Low
Close
Volume
Other Financial Indicators 📈
Volatility Index (VIX)

Purpose:

Measures market uncertainty and investor fear.

Collected:

Open
High
Low
Close
USD/INR Exchange Rate

Purpose:

Currency movement can influence foreign investment and Indian markets.

Collected:

Open
High
Low
Close
Crude Oil

Purpose:

Energy prices influence inflation, economic conditions, and market sentiment.

Collected:

Open
High
Low
Close
Volume
Historical Period ⏳

The dataset covers:

Start Date:
2008-03-04

End Date:
2026-07-21

The long historical period was selected to include:

Different market cycles
Bull and bear markets
Economic changes
High volatility periods
Data Cleaning 🧹

After downloading, the data was processed before model development.

Steps performed:

Missing Value Handling

Financial markets may have missing values due to:

Different trading holidays
Market closures
Different operating calendars

Missing values were handled to maintain consistency across datasets.

Data Alignment

Since different markets operate in different time zones, all datasets were aligned using trading dates.

This ensured that each row represented comparable market information.

Feature Organization

The final dataset combined:

NIFTY 50 data
Global market indicators
Currency data
Commodity data

into a single dataframe.

Return Calculation 📉

Daily returns were calculated for major market indicators.

Formula:

Return = (Current Price - Previous Price) / Previous Price

Returns were added because:

They normalize price movements
Allow comparison between different markets
Capture daily momentum

Generated features:

NIFTY_Return
SP500_Return
NASDAQ_Return
DOW_Return
USDINR_Return
CRUDE_Return
VIX_Return
Final Dataset 📋

After data collection and preprocessing:

Dataset Shape:

4347 rows × 41 columns

The dataset contained:

Original market features
Daily return features
Engineered technical indicators (added later)
Data Leakage Prevention 🔒

Financial data requires careful handling because future information can easily leak into training.

To prevent leakage:

Data was sorted chronologically
Future values were not used during training
Time-based train/validation/test splitting was applied
Data Collection Outcome ✅

The final dataset provided a foundation for:

Exploratory data analysis
Feature engineering
Machine learning model training
Model evaluation

The collected data represents a combination of:

Indian Market Factors
          +
Global Market Signals
          +
Currency & Commodity Effects
          +
Technical Indicators
          ↓
Machine Learning Prediction Pipeline
