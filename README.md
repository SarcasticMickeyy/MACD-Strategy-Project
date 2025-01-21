MACD-Strategy-Project
A Python program that uses historical stock data to simulate trades based on the MACD indicator. It evaluates performance metrics like profit, win rate, and drawdown, providing insights into the effectiveness of the strategy with visualizations of equity growth.
=========================================================================================================================================================================================

Overview

This code analyzes a trading strategy using NVIDIA stock data from 2014 to 2024. It identifies buy signals, tracks trade performance, and calculates various metrics to evaluate the strategy's success.

What Does This Code Do?

Download Data: The code fetches NVIDIA stock price data from Yahoo Finance, including daily prices like open, high, low, close, and trading volume.

Resample Data: It simplifies the data by grouping it into weekly chunks, making it easier to analyze trends over time.

Calculate MACD: The Moving Average Convergence Divergence (MACD) is used to spot when to buy the stock. The MACD Histogram is key here:

If it crosses from negative to positive, it’s a signal to buy.

Simulate Trades: The code pretends to buy and sell the stock based on the MACD signal.

Entry Price: The price at which the trade starts.

Exit Price: The price at which the trade ends.

Stop-Loss (SL): A price below which the trade is automatically closed to limit losses.

Target (TGT): A profit level at which the trade is closed.

Track Performance: It tracks how much money was gained or lost in each trade and calculates overall performance.

Visualize Results: An equity curve (a line graph) shows how the total money grew or shrank as trades were made.

Key Terms

MACD Histogram: A tool that helps identify when the stock’s trend might change.

Stop-Loss (SL): The price limit set to stop further losses.

Target (TGT): The price level where profit is locked in.

Equity Curve: A graph showing how the total profit changes over time.

How It Works Step by Step

1. Download Stock Data

The program uses the yfinance library to fetch NVIDIA stock data from 2014 to 2024. The data includes:

Open Price: The price when the market opens.

Close Price: The price when the market closes.

High Price: The highest price of the day.

Low Price: The lowest price of the day.

Volume: The total number of shares traded.

2. Calculate MACD

The MACD is calculated using specific time periods:

Fast Period (3 days): Captures short-term trends.

Slow Period (21 days): Captures longer-term trends.

Signal Period (9 days): Smooths out noise for clearer signals.

3. Generate Trade Signals

Buy Signal: When the MACD Histogram turns positive after being negative, the code decides to "buy" the stock.

4. Simulate Trades

The program pretends to make trades by:

Using the open price of the next day as the entry price.

Checking if the stop-loss or target level is hit in the next day’s trading range.

5. Calculate Metrics

It calculates:

Total Profit: How much money all trades made in total.

Win Rate: Percentage of trades that made a profit.

Maximum Drawdown: The largest drop in money during the trading period.

Expectancy: Average profit per trade after considering losses.

6. Visualize Results

A line graph shows the cumulative profit for all trades over time, giving a clear picture of how the strategy performed.
