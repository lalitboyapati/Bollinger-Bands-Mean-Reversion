# Bollinger Bands Mean Reversion Strategy

This project implements and backtests a **mean reversion strategy** using Bollinger Bands on the SPY ETF (2015–2025).

## 📈 Strategy Overview
- **Indicator**: Bollinger Bands (20-day SMA ± 2σ)
- **Rules**:
  - Buy when price falls below the lower band (expect reversion upward)
  - Short when price rises above the upper band (expect reversion downward)
  - Exit when price crosses back over the middle SMA
- **Costs**: 2 bps per side
- **Asset**: SPY

## ⚙️ Parameters
- Window: 20 trading days
- Multiplier: k = 2.0
- Period: 2015-01-28 → 2025-09-15

## 📊 Results
- Final Equity: \$83,940 (starting from \$100,000)
- CAGR: –1.58% per year
- Sharpe Ratio: –0.04
- Max Drawdown: –45.9%
- Number of Trades: 100
- Win Rate: 64%
- Avg Trade: –0.12%

## 🚀 Next Steps
This baseline strategy **lost money overall**, despite a 64% win rate. Improvements could include:
- Adding filters (RSI, volume, volatility regimes)
- Position sizing techniques
- Risk management rules (stop-loss, take-profit)

## 🛠️ Setup
Clone repo and install dependencies:
```bash
git clone https://github.com/<your-username>/bollinger-mean-reversion.git
cd bollinger-mean-reversion
pip install -r requirements.txt
