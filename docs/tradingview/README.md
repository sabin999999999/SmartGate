# TradingView Strategy: AI-Inspired Trading Bot

This directory contains a Pine Script strategy that you can copy into TradingView to experiment with an "AI-inspired" momentum and trend-following bot.

## Files

- `AI_Inspired_Trading_Bot.pine` – the full Pine Script (version 5) strategy file.

## How to Use on TradingView

1. Open [TradingView](https://www.tradingview.com/) and launch the **Pine Editor** tab at the bottom of the chart.
2. Copy the entire contents of [`AI_Inspired_Trading_Bot.pine`](AI_Inspired_Trading_Bot.pine) and paste it into the editor.
3. Click **Add to chart**. TradingView will compile the script and overlay the strategy on your active symbol.
4. Adjust input parameters in the script settings to match your preferred time frame and risk appetite.
5. Review the **Strategy Tester** tab to inspect performance metrics.

## Strategy Overview

The script combines multiple indicators to build a composite score:

- Exponential Moving Averages (trend strength)
- Relative Strength Index (momentum)
- MACD crossover confirmation
- Volume spikes relative to a moving average
- Bollinger Bands to estimate price position within a volatility envelope

When the composite score crosses above a bullish threshold (default: 65) and other confirmations align, a long position is opened. Likewise, a low score (default: 35) with bearish confirmation triggers a short entry. Each trade applies configurable stop-loss, take-profit, and optional trailing stop exits.

> **Important:** This strategy is for educational purposes only. Always forward-test and paper trade before risking real capital.
