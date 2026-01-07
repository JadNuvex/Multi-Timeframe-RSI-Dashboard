# Multi-Timeframe-RSI-Dashboard
A technical analysis tool for TradingView that monitors RSI momentum across 15 timeframes simultaneously using a color-coded heatmap grid. Built in Pine Script v6.

Monitoring 15 different timeframes manually requires constant chart switching or a cluttered workspace, making it nearly impossible to spot trend alignment in real-time.
<img width="1372" height="125" alt="image" src="https://github.com/user-attachments/assets/867002bc-cdba-4bce-b699-cc5c995f24e1" />
<img width="1457" height="150" alt="image" src="https://github.com/user-attachments/assets/1194f479-9d75-44e7-825c-6b0314444293" />
<img width="1164" height="146" alt="image" src="https://github.com/user-attachments/assets/2d74df29-aaee-4c88-bd7d-a6efb77e1649" />


This MTF Momentum Monitor condenses those 15 charts into a single, high-density dashboard. This allows you to verify instantly if a short-term move is an isolated event or a high-probability entry aligned with the long-term trend.
<img width="685" height="52" alt="image" src="https://github.com/user-attachments/assets/13dd5acb-b929-48fe-933b-f0cbaf19d76f" />

## Features
* **15-Timeframe Coverage:** Instantly view momentum from ultra-scalp (1m) to long-term (M) horizons.
* **Persistence Logic:** Uses a custom algorithm to track if momentum is holding above or below the 50-midline, helping to filter out false reversals.
* **Clean UI:** A horizontal table layout that stays out of the way of your price action analysis.
* **Pine Script v6:** Built using the latest TradingView standards for optimal performance and data handling.

## How the Logic Works
The dashboard filters market noise and confirms trend strength by categorizing price action into three logical states across 15 timeframes:

* **State 1: Setup (Dark Colors)**
    * **Trigger:** RSI hits extreme levels ( or ).
    * **Context:** Identifies "High-Alert" zones where a reversal or a major momentum breakout is imminent.


* **State 2: Execution (Bright Colors)**
    * **Trigger:** RSI leaves the extreme zone but persists on its respective side of the 50-midline.
    * **Context:** Confirms the active trend is holding. This allows for "riding the trend" and prevents premature exits.


* **State 3: Reset (Gray)**
    * **Trigger:** RSI crosses back over the 50-midline.
    * **Context:** Signals that momentum has been neutralized; the current trade setup is no longer valid.


  ### **Implementation Details**
    * **Multi-Timeframe Engine:** Utilizes `request.security` to pull data from 15 distinct intervals (1m to Monthly) into a single chart context.
    * **Optimized Performance:** Uses `array` structures to handle data processing efficiently, ensuring the dashboard doesn't lag the TradingView interface.
    * **Persistence Algorithm:** Employs a custom logic function to track the "time since last extreme," distinguishing between a trend-less chop and a strong momentum push.
    * **UI Architecture:** Built using the `table` namespace in Pine Script v6, featuring a horizontal grid layout for a low-profile, non-intrusive workspace.

## Installation
1. Copy the code from `Multi-Timeframe RSI Dashboard`.
2. Open the **Pine Editor** in TradingView.
3. Paste the code and click **Add to Chart**.
