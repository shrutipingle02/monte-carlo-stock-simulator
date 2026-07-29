# Monte Carlo Stock Price Simulator

## Overview
This project applies the Monte Carlo method to simulate and forecast short-term stock price movements based on historical volatility. It provides a probabilistic view of potential future prices, expressed as an expected value and a confidence interval, rather than a single deterministic prediction.

## What is Monte Carlo?
The Monte Carlo method is a statistical technique that allows for the simulation of a wide range of possible outcomes in a process that cannot easily be predicted due to the intervention of random variables. It is widely used in finance, engineering, and science to model the probability of different outcomes in a process that cannot easily be predicted due to the complexity of the variables involved.

## Visualization
Visualization plays a crucial role in this project, enabling the interpretation of simulated stock price trajectories over time. Through graphical representation, users can visually assess the range of potential future stock prices, which is facilitated by plotting the outcomes of 100,000 Monte Carlo simulations.

## Live Testing
The project includes a live testing component, where the Monte Carlo simulation was applied to predict the future stock price of Google. For this demonstration, data from 2024 to present was used to forecast GOOG's stock price two trading days ahead.

### Methodology
1. **Data Collection** — Historical daily closing prices for GOOG were retrieved via the Yahoo Finance API, covering the period from 2024 to present.
2. **Return Calculation** — Daily logarithmic returns were computed from the closing price series to normalize price changes and better capture compounding behavior.
3. **Volatility Estimation** — The standard deviation of daily log returns was used as a proxy for the stock's historical volatility.
4. **Simulation** — Using a random walk driven by the estimated volatility, 100,000 independent price paths were simulated forward from the most recent closing price.
5. **Statistical Inference** — The simulated price distribution at the forecast horizon was used to compute the expected price (mean) and a 95% confidence interval (2.5th–97.5th percentile).

### Backtesting Results
The expected price for 2 days later is: $335.78

The 95% confidence interval for the price 2 days later is: ($323.25, $348.40)

The 98% confidence interval for the price 2 days later is: ($319.89, $351.56)

The actual GOOG price shortly after the forecast was: $335.76

## Tech Stack
Python · NumPy · Pandas · yfinance · Matplotlib · Jupyter Notebook
