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
├── SImulation.ipynb            # All-in-one script:
│                               #   - Simulates GARCH data with Beta, Student-t, and Gaussian innovations
│                               #   - Performs MLE/QMLE estimation and compares their performance
│                               #   - Conducts multi-step volatility and VaR forecasts
│── Macroeconomic indicators.ipynb  # Applies model to macroeconomic time series
│── RPI.csv                     # UK RPI data used in the empirical section
├── README.md                   # Project overview and reproducibility instructions
└── requirements.txt            # Python packages required for running the code

### Reproducibility

To reproduce the main results from the thesis:

1. **Run simulations and parameter estimation**  
   Open and run `SImulation.ipynb` to:
   - Simulate GARCH(1,1) processes under Beta, Student-t, and Gaussian innovations
   - Estimate model parameters using MLE or QMLE
   - Evaluate estimation accuracy across specifications
   - Conduct h-step-ahead forecast and evaluate prediction accuracy via three loss functions and VaR backtesting

2. **Empirical analysis on macroeconomic data**  
   Open and run `Macroeconomic indicators.ipynb` to:
   - Load UK RPI data from `RPI.csv` and download other indicators data from the [FRED database](https://fred.stlouisfed.org/) using the `pandas_datareader` package  
   - Fit GARCH models with different innovations
   - Forecast future volatility and compute multi-step ahead Value-at-Risk (VaR)
   - Compare empirical performance across innovation types

3. **Data**
   - `RPI.csv` contains the UK Retail Price Index time series, originally obtained from the UK Office for National Statistics. This is one of the macroeconomic indicators analyzed.  
   - Additional time series (e.g., CPI, PPI, FX rates, etc.) are automatically downloaded from the FRED database using Python code within the notebook (`Macroeconomic indicators.ipynb`).
   - Including `RPI.csv` ensures partial offline reproducibility, while the rest of the data requires internet access to fetch via `pandas_datareader`.
