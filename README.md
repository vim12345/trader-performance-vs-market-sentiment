# Trader Performance vs Market Sentiment

## Overview
This project analyzes how Bitcoin market sentiment (Fear vs Greed) influences trader behavior and performance on Hyperliquid.  
The objective is to identify behavioral patterns and derive actionable, sentiment-aware trading strategies.

This analysis was completed as part of the **Primetrade.ai – Data Science Intern (Round-0) Assignment**.

---

## Datasets

### 1. Bitcoin Fear & Greed Index
**File:** `fear_greed_index.csv`  

**Columns:**
- `timestamp`
- `value`
- `classification` (Fear / Greed)
- `date`

---

### 2. Hyperliquid Historical Trader Data
**File:** `historical_data.csv`  

**Columns:**
- `Account`
- `Coin`
- `Execution Price`
- `Size Tokens`
- `Size USD`
- `Side`
- `Timestamp IST`
- `Start Position`
- `Direction`
- `Closed PnL`
- `Transaction Hash`
- `Order ID`
- `Crossed`
- `Fee`
- `Trade ID`
- `Timestamp`

---

## Project Structure

```text
.
├── Trader_Performance_vs_Market_Sentiment.ipynb
├── historical_data.csv
├── fear_greed_index.csv
└── README.md

## Setup Instructions
### 1. Create a virtual environment

  python -m venv venv
  venv\Scripts\activate          

### 2. Install dependencies
   pip install pandas numpy matplotlib seaborn


### How to Run

1. Ensure the following files are present in the project root:

* historical_data.csv

* fear_greed_index.csv

### Start Jupyter Notebook:

   Trader_Performance_vs_Market_Sentiment.ipynb

# Methodology
### Data Preparation

* Loaded both datasets and inspected dimensions

* Checked for missing values and duplicates

* Dropped rows without Closed PnL

* Converted timestamps and aligned data at daily granularity

### Feature Engineering

* Daily PnL per trader

* Number of trades per day

* Average trade size (USD)

* Long/Short ratio

* Trader consistency using PnL volatility

### Analysis

* Compared trader performance across Fear vs Greed regimes

* Studied behavioral changes in trade frequency and position size

* Segmented traders by frequency and consistency

### Key Insights

* Trader performance differs significantly between Fear and Greed regimes.

* Trade frequency and position size increase during Greed periods.

* Traders with lower PnL volatility perform more consistently during Fear regimes.

* High-volatility traders experience larger upside and drawdowns during Greed periods.

### Strategy Recommendations

* During Fear regimes, prioritize traders with low PnL volatility.

* Greed regimes may benefit frequent traders, but require stricter risk controls.

* Reduce exposure to high-volatility traders during sentiment regime shifts.

### Reproducibility

* All analysis steps are fully documented in the notebook

* No external APIs or proprietary data sources are used

* Results can be reproduced by rerunning the notebook



