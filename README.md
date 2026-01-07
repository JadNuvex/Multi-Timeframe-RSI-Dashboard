# Multi-Timeframe-RSI-Dashboard
A technical analysis tool for TradingView that monitors RSI momentum across 15 timeframes simultaneously using a color-coded heatmap grid. Built in Pine Script v6.

## Features
* **15-Timeframe Coverage:** Instantly view momentum from ultra-scalp (1m) to long-term (M) horizons.
* **Persistence Logic:** Uses a custom algorithm to track if momentum is holding above or below the 50-midline, helping to filter out false reversals.
* **Clean UI:** A horizontal table layout that stays out of the way of your price action analysis.
* **Pine Script v6:** Built using the latest TradingView standards for optimal performance and data handling.

## How the Logic Works
Unlike a standard RSI that only shows a single value, this dashboard uses a persistence-based color system:
* **Dark Red/Green:** Extreme overbought () or oversold ().
* **Bright Red/Green:** Strong momentum trend (Price has hit an extreme more recently than it has crossed the 50-midline).
* **Gray:** Neutral momentum.

## Implementation Details
The script utilizes `request.security` and `array` structures to efficiently manage multi-symbol data without lagging the chart interface. It is designed for traders who prioritize **robust risk management** and need to confirm trend alignment across multiple timeframes before entry.

## Installation
1. Copy the code from `Multi-Timeframe RSI Dashboard`.
2. Open the **Pine Editor** in TradingView.
3. Paste the code and click **Add to Chart**.
