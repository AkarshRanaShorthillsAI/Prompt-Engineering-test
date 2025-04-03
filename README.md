# Prompt-Engineering-test
# NSE Nifty 50 Stock Analysis Script

## Overview
This Python script fetches live stock data from the NSE Nifty 50 API, processes it, and provides various stock analysis insights. It identifies:

- Top 5 gainers and losers based on percentage change.
- Stocks trading 30% below their 52-week high.
- Stocks trading 20% above their 52-week low.
- Top 5 stocks with the highest returns in the last 30 days.

Additionally, the script visualizes the gainers and losers using a bar chart.

## Requirements
Ensure you have the following dependencies installed before running the script:

```sh
pip install requests pandas matplotlib beautifulsoup4
```

## How It Works
1. **Fetch Data**: Retrieves live stock data from the NSE Nifty 50 API.
2. **Process Data**: Extracts relevant stock information.
3. **Analysis**:
   - Identifies top 5 gainers and losers based on percentage change.
   - Finds stocks trading 30% below their 52-week high.
   - Identifies stocks trading 20% above their 52-week low.
   - Retrieves the top 5 stocks with the highest returns in the last 30 days.
4. **Visualization**: Plots a bar chart of the top 5 gainers and losers.

## Usage
Run the script using Python:

```sh
python script.py
```

## Functions

### `fetch_nse_data()`
Fetches live stock data from the NSE Nifty 50 API.

### `process_data(nse_data)`
Processes the fetched NSE data and selects relevant columns.

### `find_gainers_losers(df)`
Finds the top 5 gainers and losers based on percentage change.

### `below_52_week_high(df)`
Identifies stocks trading 30% below their 52-week high.

### `above_52_week_low(df)`
Identifies stocks trading 20% above their 52-week low.

### `highest_returns_30d(df)`
Finds the top 5 stocks with the highest returns in the last 30 days.

### `plot_gainers_losers(gainers, losers)`
Plots a bar chart of the top 5 gainers and losers of the day.

## Example Output
Upon execution, the script prints analysis results and displays a visualization.

```
Top 5 Gainers:
   symbol  lastPrice  pChange
0  ABC     100.50    5.67
1  XYZ     150.30    4.89
...

Top 5 Losers:
   symbol  lastPrice  pChange
0  LMN     200.10   -3.45
1  DEF     175.25   -2.78
...
```



