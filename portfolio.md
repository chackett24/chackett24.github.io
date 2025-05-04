---
layout: default
title: MIT Lincoln Laboratory
---

# Passive Portfolio / Index Creation

## Project Overview

In this project, the goal was to construct an index fund that closely tracks a specified market index. The aim was to use optimization techniques to create a portfolio of stocks that mirrors the performance of a pre-specified stock market index, such as the **S&P 100**, **Dow Jones Industrial Average**, or **NASDAQ 100**.

---

## Methodology

### 1. **Index Selection & Data Collection**
For this project, I selected the **S&P 100** index, which includes 100 large-cap stocks from the S&P 500. The following steps were followed:

- **Historical Data:** I gathered **weekly return data** for the S&P 100 from the past **three years**.
- **Time Partitioning:** The data was split into two portions:
  - **In-sample (70%)**: Used for model calibration and parameter estimation.
  - **Out-of-sample (30%)**: Used for performance testing of the constructed index fund.

### 2. **Portfolio Construction Techniques**
To construct the index fund, I applied three key methods based on optimizing the tracking performance of the portfolio:

#### a. **Maximizing Correlation with the Original Fund**
The portfolio was constructed by selecting a **set number of assets** (e.g., 25 stocks) whose returns maximized the **correlation** with the original market index (e.g., S&P 100). The goal was to select a subset of stocks that closely mirrored the overall performance of the index.

#### b. **Matching Index Characteristics**
This method aimed to ensure the constructed portfolio shared similar **characteristics** with the original index, such as **market capitalization exposure (e.g., small-cap vs. large-cap)** and **sector distribution (e.g., tech, retail, aerospace)**. The optimization problem sought to minimize the difference between the characteristic profile of the tracking portfolio and the benchmark.


#### c. **Weighting by Returns to Match Original Index**
This method focused on **keeping the portfolio weights as close as possible to the original index**, weighted by the returns of each stock. The goal was to find the optimal weights such that the constructed portfolio's returns were as similar as possible to the returns of the original market index.

### 3. **Rolling-Time Window Approach for Out-of-Sample Testing**
To evaluate the performance of the constructed index fund, I used a **rolling-time window approach**:

- **Window Size:** The out-of-sample data was divided into **four quarters** (quarterly rebalance).
- **Rolling Windows:** The in-sample data was shifted over time, recalibrating the model and constructing a new portfolio at each step.
- **Rebalancing:** The portfolio was rebalanced at the start of each quarter based on the updated in-sample data.

### 4. **Model Testing**
I compared the performance of the constructed index fund against the actual S&P 100 index, using key performance metrics:

- **Compound Annual Growth Rate (CAGR)**
- **Max Drawdown**
- **Sharpe Ratio**
- **Volatility**

---

## Results

### Portfolio Performance Comparison
The following metrics were used to evaluate the performance of the constructed portfolio and the S&P 100 index:

- **CAGR (Compound Annual Growth Rate)**
- **Max Drawdown**
- **Volatility**
- **Sharpe Ratio** (Risk-Adjusted Return)

#### Results Summary:
- The **Maximizing Correlation** method provided a good fit in terms of mirroring the performance of the original index.
- The **Optimizing Proportions of Attributes** approach resulted in a more stable portfolio but didn’t track the index as closely during certain market movements.
- The **Weighting by Returns** technique produced a portfolio with a return profile that closely mimicked the original index but with slightly higher volatility.

