# Market Risk Engine
Regulatory-grade market risk measurement and validation system for a multi-asset portfolio, implementing three VaR methodologies, Expected Shortfall (Basel III/IV), GARCH volatility modeling, regulatory backtesting, and historical stress testing.

## Project Status
🚧 In progress

## Methodology
1. Portfolio construction with log returns across equity, fixed income, and commodities
2. Parametric VaR using variance-covariance method (95%, 99% confidence)
3. Historical Simulation VaR — no distributional assumption
4. Monte Carlo VaR with Cholesky decomposition for correlated draws
5. Expected Shortfall at 97.5% (Basel III/IV standard) across all three methods
6. GARCH(1,1) dynamic volatility modeling replacing constant-vol assumption
7. Regulatory backtesting — Kupiec POF, Christoffersen Independence, Basel Traffic Light
8. Historical stress testing — 2008 GFC, COVID-19 March 2020, 2022 Rate Shock

## Tech Stack
Python · pandas · NumPy · SciPy · arch · yfinance · matplotlib · seaborn

## Setup
```bash
git clone https://github.com/rushabha-raool/market-risk-engine.git
cd market-risk-engine
python -m venv .venv
source .venv/bin/activate  # Mac/Linux
pip install -r requirements.txt
```

## Notebooks
- `01_portfolio_construction.ipynb` — Data pull, log returns, return distribution analysis
- `02_parametric_var.ipynb` — Variance-covariance VaR with fat tail diagnostics
- `03_historical_simulation_var.ipynb` — Empirical distribution VaR, methodology comparison
- `04_monte_carlo_var.ipynb` — Simulated VaR with correlated random draws
- `05_expected_shortfall.ipynb` — CVaR across all methods, Basel III regulatory context
- `06_garch_volatility.ipynb` — Dynamic conditional volatility, GARCH vs constant-vol VaR
- `07_backtesting_framework.ipynb` — Kupiec, Christoffersen, Basel Traffic Light classification
- `08_stress_testing.ipynb` — Named scenario shocks, correlation breakdown analysis


## Author
Rushabha Raool · [LinkedIn.com/in/rushabha-raool]