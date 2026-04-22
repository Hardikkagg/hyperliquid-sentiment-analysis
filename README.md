# Hyperliquid Trader Behavior Analysis

##  Overview
This project analyzes how Bitcoin market sentiment (Fear/Greed) influences trader behavior and performance on Hyperliquid.

The goal is to uncover patterns that can help inform smarter trading strategies.

---

##  Methodology

- Loaded and cleaned two datasets:
  - Bitcoin Fear/Greed Index
  - Hyperliquid historical trading data
- Converted timestamps to daily level and merged datasets on date
- Created key metrics:
  - Profit & Loss (PnL)
  - Win rate
  - Position size (used as proxy for risk)
  - Trade frequency
- Segmented traders based on:
  - Position size (High vs Low)
  - Trading frequency (Frequent vs Infrequent)
  - Consistency (Win rate > 50%)

> Note: Leverage data was not available, so position size (USD) was used as a proxy for risk-taking behavior.

---

##  Key Insights

1. **Performance varies with sentiment**  
   Traders achieve higher average PnL and win rates during Greed periods, while Neutral periods show the weakest performance.

2. **Risk-taking increases during Greed**  
   Traders take larger position sizes during Greed periods, indicating a strong risk-on behavior.

3. **Consistent traders outperform**  
   Traders with higher win rates maintain stable performance across all sentiment conditions, while inconsistent traders are more affected during Fear periods.

---

##  Strategy Recommendations

1. **Sentiment-Based Risk Adjustment**  
   Increase position size moderately during Greed periods to capitalize on higher returns, while reducing exposure during Fear periods to manage downside risk.

2. **Trader Filtering Strategy**  
   Only consistent traders should actively trade during volatile market conditions, while inconsistent traders should reduce activity during Fear periods.

---

##  Output

The analysis includes the following visualizations:

- Performance by Sentiment (PnL, Win Rate, Loss)
- Average Position Size by Sentiment
- Consistent vs Inconsistent Trader Performance

All charts are saved in the `charts/` folder.

---

##  How to Run

1. Clone the repository:
```bash
git clone https://github.com/your-username/hyperliquid-sentiment-analysis.git
