# Trading Strategy Advice  
## Sentiment-Aware Rules of Thumb

---

## 🎯 Objective

Translate analytical findings into **practical, actionable trading strategies** based on:

- Market sentiment (Fear / Greed)
- Trader behavior
- Risk exposure patterns

---

## 🚦 Strategy 1: Risk Suppression During Fear

### 📌 Rule of Thumb

> **During Fear days, reduce position size and trading frequency for high-exposure traders.**

---

### 🔍 Rationale

- High exposure (large average trade size) traders experience:
  - Larger drawdowns
  - Higher downside volatility during Fear regimes
- Fear markets amplify losses more than gains

---

### 👥 Target Segment

- High leverage (proxy) traders  
- Frequent traders  

---

### 🛠 Implementation Ideas

- Cap maximum USD exposure per trade
- Limit number of trades per day
- Enforce stricter risk controls during Fear sentiment

---

## 📈 Strategy 2: Selective Aggression During Greed

### 📌 Rule of Thumb

> **During Greed days, allow increased trading activity only for historically consistent traders.**

---

### 🔍 Rationale

- Consistent traders:
  - Capture upside more reliably
  - Maintain controlled volatility
- Inconsistent traders:
  - Show unstable returns even in bullish regimes

---

### 👥 Target Segment

- Consistent (low PnL volatility) traders

---

### 🛠 Implementation Ideas

- Increase position size or trade frequency selectively
- Maintain conservative limits for inconsistent traders
- Use historical consistency as a gating condition

---

## 🧠 Key Takeaway

> **Market sentiment should guide risk allocation, but only traders with proven consistency should be allowed to scale exposure during optimistic regimes.**

---

## ⚠️ Important Note

- Explicit leverage data was not available
- Average trade size (USD) was used as a **proxy for effective leverage**
- This approximation reflects relative risk exposure per trade

---

## ✅ Summary

| Market Sentiment | Recommended Action |
|------------------|-------------------|
| Fear | Reduce exposure, limit trades |
| Greed | Selective scaling for consistent traders |

These rules help balance **risk control** with **opportunity capture**.

---
