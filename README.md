# Machine Learning Enhanced Mean-Reversion Strategy 📈🤖

An algorithmic trading project combining Stochastic Calculus (Ornstein-Uhlenbeck) and Supervised Machine Learning (XGBoost) to trade cointegrated assets pairs.

## 🚀 Project Overview

This project implements a systematic **Pairs Trading strategy**. It identifies statistical arbitrage opportunities using a mean-reversion model and filters these signals using a Machine Learning classifier to improve the risk-adjusted returns.

**Key Features:**
* **Quantitative Modeling:** Spread modeling using the **Ornstein-Uhlenbeck (OU)** stochastic process.
* **Signal Generation:** Z-score based entry/exit points.
* **ML Filtering:** An **XGBoost** classifier filters trade signals based on market regime features (Volatility, RSI, Momentum).
* **Risk Management:** Dynamic Volatility Targeting and Value-at-Risk (VaR) monitoring.

## 🛠️ Tech Stack

* **Python 3**
* **Data Analysis:** Pandas, NumPy
* **Finance:** Yfinance (Data collection), Statsmodels (Cointegration tests, ADF)
* **Machine Learning:** Scikit-Learn, XGBoost
* **Visualization:** Matplotlib, Seaborn

## 📊 Methodology

1.  **Pair Selection:** Automatic selection of correlated assets (e.g., KO vs PEP) using Cointegration tests (Engle-Granger).
2.  **Baseline Model:** Calculating the spread $X_t = \log(A) - \beta \log(B)$ and its Z-score.
3.  **ML Layer:** Determining if a mean-reversion signal is valid or a "bull trap" using XGBoost (AUC achieved: 0.83).
4.  **Execution:** Applying Volatility Targeting to size positions dynamically.

## 📈 Results

* **Strategy AUC:** 0.835 (Ability to predict profitable mean-reversions).
* **Accuracy:** ~73% on filtered high-conviction trades.
* **Risk Control:** The strategy adapts leverage to maintain a target volatility of 10%.

## 👨‍💻 Author

**Nolan Lebeau** - *Engineering Student, Major in Financial Engineering @ESILV*
[LinkedIn Profile](https://www.linkedin.com/in/nolan-lebeau/)
