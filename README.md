# Master_thesis_Saksham_2026
Handling Holiday Effect
This repository contains the code and experiments used in my master’s thesis.  
The main goal is to improve forecasting around holidays by comparing standard baselines with feature-engineered (FE) regressors that spread holiday effects over a multi-day window.

The work is implemented primarily as a single Jupyter notebook and produces figures and diagnostics used in the thesis.

## What this repository includes

- Two domains:
  - Tourism time series (daily)
  - Retail time series (daily)
- Models and baselines:
  - SARIMAX / SARIMA-style baselines
  - Prophet baselines (linear and logistic variants)
  - TBATS baseline
- Feature engineering variants (examples used in the notebook):
  - Windowed holiday templates (median, Gaussian, trapezoid)
  - One-hot holiday indicators
  - Days-interaction style regressors (holiday timing / weekday interactions)
- Evaluation:
  - Rolling-origin forecasting (out-of-sample)
  - Window-based scoring around holiday centers: ±K days
  - K values used: {1, 2, 3, 5, 7}

## Repository structure

- saksham-master-thesis.ipynb
  - Main notebook containing:
    - Data loading and preprocessing
    - Holiday calendar construction and center-date logic (consecutive holidays merged)
    - Model training and evaluation
    - Figures and appendix diagnostics
- figures/ (created by the notebook)
  - Saved plots used for analysis and thesis figures (if you keep the default paths)
- Outputs saved by cells (examples)
  - acf_pacf_tourism.png
  - Additional diagnostics and per-window comparison plots (depending on which cells you run)

## Requirements

Recommended:
- Python 3.10+ (works with 3.9+ in many cases)
- Jupyter Notebook or JupyterLab

Key packages used:
- pandas, numpy
- matplotlib
- scikit-learn
- statsmodels
- holidays
- prophet
- tbats 
