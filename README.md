## 📈 Time Series Econometrics Analysis of CSCO, TMUS, S&P 500, and VIX

This repository contains a comprehensive econometric analysis of time series data for:
- **CSCO** (Cisco Systems)
- **TMUS** (T-Mobile US)
- **^GSPC** (S&P 500 Index)
- **^VIX** (CBOE Volatility Index)

The analysis includes data exploration, statistical testing, VAR modeling, Granger causality, and volatility modeling using GARCH. It also includes weekday effect analysis for the S&P 500.

---

### 📊 Project Overview

The project is divided into several sections:

#### 1. **Data Collection**
- Prices downloaded using `yfinance` from 2016 to 2024.
- Daily closing prices for CSCO, TMUS, S&P 500 (^GSPC), and VIX (^VIX).

#### 2. **Data Visualization**
- Time series plots for each asset.
- Differenced log returns for CSCO, TMUS, and ^GSPC.
- First differences for ^VIX.

#### 3. **Stationarity Tests**
- Augmented Dickey-Fuller (ADF) tests to check for stationarity.

#### 4. **VAR Model**
- Vector AutoRegression applied on the return series.
- Optimal lag selection using criteria like AIC/BIC.
- Impulse Response Functions (IRFs) to analyze shocks.

#### 5. **Granger Causality**
- Matrix showing whether past values of one variable help forecast another.

#### 6. **Volatility Modeling (GARCH)**
- Applied GARCH(1,1) to cryptocurrency returns (e.g., XRP-USD).
- ARCH test on residuals to justify GARCH usage.

#### 7. **Weekday Effect Analysis**
- Analyzed whether returns differ across weekdays for the S&P 500.
- Included t-tests for significance and annual weekday return plots.

---

### 🧠 Technologies Used

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- `statsmodels` for econometric modeling
- `yfinance` for data extraction
- `arch` package for GARCH modeling
- Jupyter Notebook

---

### 📂 File Structure

```
📁 root/
├── share_pr.csv               # Raw stock prices
├── dataset.csv                # Log returns and differences
├── crypto_ret.csv             # XRP returns
├── result_df.csv              # T-test results for weekday effect
├── gspc1.png                  # Bar plot of average weekday returns
├── gspc3.png                  # Yearly weekday effect plot
└── time_series_analysis.ipynb # Main analysis notebook
```

---

### 🧪 How to Run

1. Install the required packages:

```bash
pip install yfinance statsmodels arch matplotlib seaborn
```

2. Launch the Jupyter Notebook:

```bash
jupyter notebook
```

3. Open `time_series_analysis.ipynb` and run the cells in sequence.

---

### 📌 Notes

- The dataset can be modified by changing the tickers in the script.
- The analysis assumes knowledge of time series econometrics, such as stationarity, VAR, IRF, and GARCH modeling.

---
