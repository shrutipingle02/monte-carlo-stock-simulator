# Monte Carlo Stock Price Simulator

A Python project that uses the Monte Carlo method to forecast stock price movements based on historical volatility.

## What it does
- Pulls real stock data using `yfinance`
- Calculates daily volatility from historical log returns
- Runs 100,000+ simulations to forecast future price ranges
- Outputs expected price and 95%/98% confidence intervals
- Includes a reusable `MonteCarlo` class for testing multiple tickers

## Results
Forecasted GOOG's price 2 days ahead: **$335.78** expected, with a 95% confidence range of **$323.25–$348.40**. Actual live price landed at **$335.76** — right in range.

## Tech Stack
Python, NumPy, Pandas, yfinance, Matplotlib, Jupyter Notebook
