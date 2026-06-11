# India CPI Inflation Forecasting
### End-to-End Macro-Econometric Pipeline | RBI Monthly Data (Oct 2017 – Jun 2025)

## Overview
Forecasts India's headline CPI year-on-year % change using a 
four-layer variable selection pipeline and SARIMAX/VAR modelling 
on RBI macroeconomic data.

**Key result:** VAR model achieved MAE of X pp on 12-month 
walk-forward out-of-sample evaluation, outperforming 
SARIMAX(2,0,2)×(1,1,0,12).

**Dominant finding:** Inflation inertia via food price levels 
(CPI_FOOD) is the strongest short-run predictor of headline CPI, 
consistent with food's ~45% weight in India's CPI basket.

## Methodology
- Data: RBI Database on Indian Economy (DBIE)
- Stationarity: ADF + KPSS with Perron (1989) structural break adjustment
- Causality: Toda-Yamamoto (1995) Granger on levels
- Cointegration: Engle-Granger (1987) pairwise screening
- Model: SARIMAX(2,0,2)×(1,1,0,12) vs VAR benchmark
- Evaluation: Walk-forward OOS + Diebold-Mariano (1995) test

## Key References
- RBI DEPR (Singh et al., 2024)
- IEG WP-461 (Ghosh & Ghosh, 2023)
- IMF WP 17/33 (Benes et al., 2017)
- Toda & Yamamoto (1995, Journal of Econometrics)
- Engle & Granger (1987, Econometrica)

## Data
Data sourced from RBI DBIE (https://dbie.rbi.org.in).
Download the monthly macroeconomic indicators file and 
place it in the `data/` folder before running the notebook.

## Planned Extensions
- Interactive Streamlit forecast dashboard
- Live RBI data integration

## Requirements
See `requirements.txt`. Run `pip install -r requirements.txt`.
