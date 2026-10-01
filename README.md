# Multi-asset-risk-engine
Multi-Asset Market Risk Engine calculating Student's t-VaR/ES with Kupiec POF Backtesting validation.

# Multi-Asset Market Risk Engine & Validation Framework

An industry market risk simulation built to quantify and statistically validate tail risk for a multi-asset portfolio under non-normal distribution regimes.

## Portfolio Configuration
* **Assets**: NVIDIA, Goldman Sachs, Bitcoin
* **Time Horizon**: 3 Years (Roughly 751 active trading days)
* **Risk Parameters**: 95% Confidence Interval, 1-Day Holding Period

## Core Methodology & Analytical Insights
* **Fat-Tail Modeling**: Replaced traditional Gaussian parameters with a **Student's t-distribution**, dynamically fitting the data to reveal extreme leptokurtosis with a **Degrees of Freedom metric of 5.52**.
* **Risk Metrics**: 
  - **95% Daily VaR**: 2.79% (\$27,850.93 baseline exposure on a \$1M book)
  - **Parametric Student's t-Expected Shortfall (ES)**: 4.07% (\$40,665.91 average conditional tail loss)
* **Validation**: Implemented a **Kupiec Proportion of Failures (POF)** backtest. The model generated **31 exceptions** against an expected 37. The resulting **Likelihood Ratio of  1.2754** easily fell below the **3.8415 Chi-Square critical threshold**, mathematically validating the model's structural integrity.

## Language and Libraries
* Python, Jupyter Lab, NumPy, Pandas, SciPy, yFinance
