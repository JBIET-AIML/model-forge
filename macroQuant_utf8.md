# 🏆 Hackathon Problem Statement

## **MacroQuant 2026: Forecasting & Trading Gold and Silver**

---

## 📌 Background

Gold and silver are globally traded precious metals that serve as:

* Inflation hedges
* Safe-haven assets during market stress
* Industrial commodities linked to economic growth

Unlike isolated asset forecasting problems, precious metals are deeply connected to global macroeconomic forces such as:

* Interest rates
* Inflation expectations
* Currency movements
* Equity market performance
* Volatility regimes
* Liquidity conditions

For example, gold prices often respond strongly to changes in U.S. real interest rates and movements in the US Dollar Index, while silver is additionally influenced by industrial demand and copper price dynamics.

This hackathon simulates a real-world quantitative macro trading environment where forecasting accuracy must translate into profitable trading performance.

---

# 🎯 Core Objective

Participants must build an **end-to-end quantitative system** that:

### A. Forecasts Future Returns

Predict short-term and medium-term returns for:

* Gold Futures
* Silver Futures

Across three horizons:

* 1-day ahead return
* 30-day ahead return
* 6-month ahead return

---

### B. Converts Forecasts into Trading Decisions

Generate daily trading signals:

| Signal | Action       |
| ------ | ------------ |
| +1     | Long (Buy)   |
| 0      | Hold         |
| -1     | Short (Sell) |

The goal is not only to minimize prediction error, but to **maximize risk-adjusted returns**.

---

# 📊 Dataset Description

## This dataset is a comprehensive macro-financial time series collection designed for:

- Multi-horizon forecasting of gold and silver
- Systematic trading strategy development
- Macro-driven asset pricing research
- Cross-country macro sensitivity analysis

## The dataset integrates:

- Global precious metals futures
- Currency markets
- Equity indices
- Volatility indices
- Commodity markets
- U.S. macroeconomic drivers
- Indian macroeconomic indicators

## Data Frequency

* Daily for market variables
* Monthly/Quarterly for macro variables
* All macro series can be forward-filled to business-day frequency during modeling

All data begins from January 1, 2005 and extends to the most recent available date.


### MacroQuanta Economic Data

Downloaded using `pandas_datareader`. Downloaded using *yfinance*.

Includes:

#### 🇺🇸 United States

* 10-Year Real Yield (DFII10)
* 10-Year Treasury Yield (DGS10)
* 2-Year Treasury Yield (DGS2)
* 10-Year Breakeven Inflation (T10YIE)
* 5-Year Breakeven Inflation (T5YIE)
* CPI (CPIAUCSL)
* M2 Money Supply (M2SL)
* Industrial Production (INDPRO)

#### 🇮🇳 India

* CPI (INDCPIALLMINMEI)
* Policy Rate
* 10Y Government Bond Yield
* 3M Treasury Bill Rate
* M3 Money Supply
* GDP per Capita
* Bank NPL Ratio

---

## 3️⃣ Folder Structure

```
data1/
│
├── global_data/
│   ├── Gold_Futures.csv
│   ├── Silver_Futures.csv
│   ├── DXY.csv
│   ├── SP500.csv
│   ├── VIX.csv
│   ├── Copper.csv
│   ├── Oil.csv
│   ├── US_Real_Yield_10Y.csv
│   └── ...
│
└── india_data/
    ├── Gold_India_ETF.csv
    ├── Silver_India_ETF.csv
    ├── USDINR.csv
    ├── NIFTY50.csv
    ├── India_CPI_All.csv
    └── ...
```

Each file contains:

| Column       | Description          |
| ------------ | -------------------- |
| Date         | Business date        |
| Value Column | Price or macro value |

---

---

# 🧠 Challenge Components

## 1️⃣ Multi-Horizon Forecasting

Build time-series models to predict/forecast: Gold & Silver returns

- 1-Day Return = log(Pₜ₊₁ / Pₜ)
- 30-Day Return = cumulative log return over next 30 trading days
- 6-Month Return = cumulative log return over next 126 trading days

Participants may use:

* Linear models
* Tree-based models
* Deep learning
* Ensemble methods

Time-series rigor is mandatory (no data leakage).

---

## 2️⃣ Systematic Trading Strategy

Participants must convert predictions into:

* Daily position signals
* Portfolio allocation decisions
* Risk-managed trading strategies

Constraints:

* Initial capital: $100,000
* Transaction cost: 0.05% per trade
* Daily rebalancing
* No look-ahead bias

---

# 🗂 Data Split (Time-Series Safe)

| Period    | Usage      |
| --------- | ---------- |
| 2005–2018 | Training   |
| 2019–2021 | Validation |
| 2022–2025 | Test       |

Random shuffling is strictly prohibited.

---

# 📏 Evaluation Metrics

## 📌 Forecasting Evaluation (45%)

Primary:

* RMSE (Root Mean Squared Error)

Secondary:

* MAE
* R²
* Directional Accuracy

Multi-horizon performance will be averaged.

---

## 📌 Trading Evaluation (55%)

Primary:

* Sharpe Ratio (risk-adjusted return)

Secondary:

* CAGR
* Maximum Drawdown
* Sortino Ratio
* Hit Ratio

---

# 🏆 Scoring Breakdown

| Component                | Weight |
| ------------------------ | ------ |
| Forecast RMSE (Test)     | 30%    |
| Multi-Horizon Robustness | 15%    |
| Sharpe Ratio (Test)      | 30%    |
| Drawdown Control         | 10%    |
| Validation Methodology   | 10%    |
| Model Explainability     | 5%     |

---

# ⚙ Rules & Constraints

* No future data usage
* No external data unless explicitly allowed
* Code must be reproducible
* All preprocessing steps must be documented
* Trading strategy must incorporate transaction costs

---

# 💡 What Judges Are Looking For

* Economically grounded feature engineering
* Robust walk-forward validation
* Overfitting control
* Risk-aware portfolio construction
* Explainable modeling approach
* Stable performance across regimes

---

# 🚀 Deliverables

Participants must submit:

1. Forecast predictions (test set)
2. Daily trading signals
3. Backtest performance metrics
4. Technical report (max 10 pages)
5. Source code
6. Protype (if possible)

---