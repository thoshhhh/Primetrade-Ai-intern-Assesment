# Trader Performance vs Market Sentiment  
## Data Science / Analytics Intern – Round-0 Assignment  
**Primetrade.ai**

---

## 📌 Project Overview

This project analyzes how **market sentiment (Fear vs Greed)** influences **trader behavior and performance** on the Hyperliquid platform.

The goal is to uncover **behavioral patterns**, **performance differences**, and **actionable trading rules** that can inform smarter, sentiment-aware trading strategies.

---

## 📂 Datasets Used

### 1️⃣ Bitcoin Market Sentiment (Fear & Greed Index)

- Columns:
  - `timestamp`
  - `value`
  - `classification` (Fear / Greed)
  - `date`
- Granularity: Daily

### 2️⃣ Historical Trader Data (Hyperliquid)

Key columns used:
- `account`
- `coin`
- `execution price`
- `size usd`
- `side`
- `timestamp`
- `closed pnl`
- `date`

> ⚠️ Note: The dataset does **not** include an explicit leverage column.

---

## 🧹 Part A — Data Preparation

### ✔ Steps Performed

- Loaded both datasets
- Checked:
  - number of rows & columns
  - missing values
  - duplicate rows
- Normalized column names
- Converted timestamps to `datetime`
- Aligned both datasets at **daily level**
- Merged trader data with sentiment data using `date`

### ✔ Feature Engineering

Created the following metrics:

- **daily_pnl** – total PnL per trader per day  
- **win_rate** – percentage of profitable trades  
- **avg_trade_size_usd** – average USD exposure per trade  
- **trades** – number of trades per day  
- **long_ratio** – proportion of long (buy) trades  

> Since leverage was not available, **average trade size (USD)** was used as a **proxy for effective leverage**.

---

## 📊 Part B — Analysis

### 🔍 Key Questions Answered

- Does trader performance differ between **Fear** and **Greed** days?
- Do traders change behavior based on market sentiment?
- Which trader segments perform better or worse across regimes?

---

## 👥 Trader Segmentation

The following segments were analyzed:

1. **High vs Low Leverage (Proxy) Traders**
   - Based on average trade size (USD)

2. **Frequent vs Infrequent Traders**
   - Based on daily trade count

3. **Consistent vs Inconsistent Traders**
   - Based on volatility of daily PnL

---

## 📈 Visualizations Included

- Boxplot: Daily PnL — Fear vs Greed
- Tables comparing:
  - Performance metrics
  - Behavioral metrics
  - Segment-wise performance

Each insight is supported by **tables and/or charts**.

---

## 🧠 Key Insights (Summary)

- Traders achieve **higher PnL and win rates during Greed days**
- **Fear days lead to reduced trade size and defensive behavior**
- **Consistent traders outperform across both market regimes**
- **High exposure traders suffer disproportionate losses during Fear**

---

## 🎯 Part C — Actionable Strategies

Two sentiment-aware trading rules were proposed:

- Risk suppression for high-exposure traders during Fear
- Selective aggression during Greed for consistent traders only

(See `ADVISE.md` for full details)

---

## ⭐ Bonus Work

### ✔ Predictive Model
- Logistic Regression
- Predicts profitable vs unprofitable trader-days
- Features used:
  - sentiment
  - trade size
  - trade frequency
  - directional bias

### ✔ Trader Clustering
- KMeans clustering
- Identifies behavioral archetypes such as:
  - Conservative traders
  - Aggressive traders
  - Directional traders

---

## ▶️ How to Run

1. Open `Prime_Trade_Ai.ipynb`
2. Ensure the datasets are in the same directory
3. Run all cells from top to bottom

No additional configuration required.

---

## ✅ Conclusion

This notebook provides a **reproducible, sentiment-aware analysis of trader behavior**, supported by data, visual evidence, and actionable insights.  
All mandatory tasks and bonus analyses are completed.

---
