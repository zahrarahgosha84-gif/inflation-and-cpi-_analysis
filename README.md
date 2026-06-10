# US Inflation Dynamics & Monetary Policy

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![ARIMA-GARCH](https://img.shields.io/badge/Model-ARIMA--GARCH-orange)]()

## Overview

This project explores the relationship between **US inflation** and monetary policy (Federal Funds Rate). Using a two‑phase analytical approach – **Exploratory Data Analysis (EDA)** followed by **advanced time‑series modeling** – we built a hybrid **ARIMA‑GARCH** model that forecasts both inflation trends and market volatility. The final model achieves an **RMSE of 0.409**, demonstrating high predictive accuracy.

## Key Findings

- Inflation exhibits cyclical patterns and significant regime shifts over decades.
- The Federal Funds Rate generally follows inflation trends, confirming its role as a primary monetary policy tool.
- The correlation between inflation and interest rates is positive (~0.71) but **not static** – it varies with economic regimes (e.g., 1970s vs. 2010s).
- ARIMA residuals show **volatility clustering**, indicating heteroskedasticity and justifying the need for a GARCH component.

## Methodology

### 1. Exploratory Data Analysis (EDA)

- **Time‑series plots** of inflation vs. Federal Funds Rate.
- **Lag correlation** to identify lead‑lag relationships.
- **Correlation heatmap** (coefficient ~0.71).
- **Rolling correlation** to capture regime‑dependent dynamics.

### 2. Time‑Series Modeling (ARIMA)

- Model trained to capture the underlying trend of inflation.
- Initial 12‑month forecast based on historical averages.
- Residual analysis revealed **volatility clustering** → GARCH needed.

### 3. Hybrid ARIMA‑GARCH Model

- **ARIMA** models the conditional mean (trend).
- **GARCH** models the time‑varying conditional variance (volatility/risk).
- Produces robust forecasts that account for both trend and uncertainty.

## Results

- **Final Forecast**: ARIMA‑GARCH provides reliable inflation predictions for economic decision‑making.
- **Performance Metric**: RMSE = **0.409**
- **Volatility prediction** tracks conditional variance, quantifying forecast risk over time.

## Technologies Used

- **Python** – core language
- **Pandas** – data manipulation
- **Statsmodels** – ARIMA modeling
- **Arch library** – GARCH modeling
- **Matplotlib / Seaborn** – visualizations

## Getting Started

### Prerequisites

```bash
pip install pandas statsmodels arch matplotlib seaborn
## Repository Structure
├── data/               # Raw and processed datasets
├── notebooks/          # EDA and modeling notebooks
├── outputs/            # Plots and forecast results
├── README.md           # This file
└── requirements.txt    # Python dependencies
