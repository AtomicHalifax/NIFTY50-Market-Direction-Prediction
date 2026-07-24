# Why This Project?

## Why NIFTY 50?

NIFTY 50 represents the performance of India's largest companies
across multiple sectors.

It provides a broad representation of the Indian equity market.

---

## Why Predict Direction Instead of Price?

Exact price prediction is highly sensitive to market noise.

Instead, this project focuses on binary classification:

1 → Next day market increase

0 → Next day market decrease

This makes the problem more stable and realistic.

---

## Why Yahoo Finance?

Yahoo Finance provides:

- Historical OHLCV data
- Global market indices
- Free accessibility
- Long historical coverage

---

## Why These Features?

### Domestic Indicators

Used because Indian markets are affected by:

- Local economic conditions
- Domestic investor sentiment
- Market momentum


### Global Indicators

Included because modern markets are interconnected.

Examples:

NASDAQ → Global technology sentiment

S&P500 → US market direction

USD/INR → Currency movement

Crude Oil → Energy and inflation impact


---

## Why Technical Indicators?

Raw prices alone do not represent market behaviour.

Indicators capture:

- Momentum
- Trend
- Volatility

Examples:

RSI → Overbought/Oversold conditions

MACD → Trend momentum

Bollinger Bands → Volatility


---

## Why Time Series Split?

Random splitting creates data leakage.

Financial markets are chronological.

The model must always learn from:

Past → Future

Never:

Future → Past


---

## Why These Models?

### Logistic Regression

Used as a baseline model.

Provides:

- Interpretability
- Simple benchmark


### Decision Tree

Used to capture nonlinear relationships.


### XGBoost

Chosen because:

- Handles complex patterns
- Strong performance on tabular data


### LightGBM

Chosen because:

- Faster training
- Efficient with large feature sets


---

## Why ROC-AUC?

Accuracy alone is not enough.

ROC-AUC measures how well the model separates:

Positive movement vs Negative movement.

---

## Why Feature Importance?

Understanding important variables helps:

- Interpret model behaviour
- Remove unnecessary features
- Improve future versions
