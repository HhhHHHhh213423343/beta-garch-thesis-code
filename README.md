# beta-garch-thesis-code
Code for my MSc thesis on GARCH with Beta innovations

This repository contains all scripts used for:
- Simulation and estimation of GARCH(1,1) models with alternative innovations (Beta, Student-t, Gaussian), with Monte Carlo experiments.
- MLE/QMLE performance comparison: RMSE, SE ratios, Coverage probabilities and interval length.
- h-step-ahead forecasts computation
- Forecasting evaluation: MAE, MSE, QLIKE.
- Multi-step ahead VaR backtesting: Unconditional Coverage (UC) test, Independence (IND) test, Conditional Coverage (CC) test.
- Empirical analysis on macroeconomic series (e.g., CPI, PPI, FX rates, etc.)

## Repository Structure
.
├── Simulation.ipynb            # All-in-one script:
│                               #   - Simulates GARCH data with Beta, Student-t, and Gaussian innovations
│                               #   - Performs MLE/QMLE estimation and compares their performance
│                               #   - Conducts multi-step volatility and VaR forecasts
│── Macroeconomic indicators.ipynb  # Applies model to macroeconomic time series
│
├── README.md                   # Project overview and reproducibility instructions
└── requirements.txt            # Python packages required for running the code
