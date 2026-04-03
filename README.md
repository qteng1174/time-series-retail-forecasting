# Time-Series Analysis and Forecasting of Monthly U.S. Retail Sales

## Overview
This project analyzes and forecasts monthly U.S. retail sales using classical time-series methods. The goal is to compare models from different categories and identify the model with the best predictive performance.

## Dataset
- **Source:** Federal Reserve Economic Data (FRED)
- **Series ID:** MRTSSM44000USN
- **Coverage:** January 1992 – October 2025
- **Frequency:** Monthly
- **Sample Size:** 406 observations
- **Unit:** Millions of U.S. dollars

## Project Objective
Retail sales reflect consumer spending and overall economic activity. Because the series shows both trend and strong seasonality, this project evaluates several forecasting methods to determine which model best captures the data and produces accurate out-of-sample forecasts.

## Methods
The following models were compared:
- Seasonal Naive (baseline)
- ETS (Error, Trend, Seasonal)
- SARIMA
- Regression with ARMA errors

## Exploratory Analysis
The project examined the original series, Box-Cox transformation, first-order differencing, and seasonal differencing. The analysis showed strong seasonality and changing variance, and differencing was used to help achieve stationarity.

## Model Evaluation
Models were evaluated using:
- RMSE
- MAE
- MAPE
- Residual diagnostics
- Ljung-Box tests

## Key Results
- The baseline Seasonal Naive model captured yearly seasonality but underestimated the upward trend.
- SARIMA improved substantially over the baseline.
- ETS achieved the best forecast accuracy on the test set.
- The final comparison showed that ETS had the strongest alignment with the observed 2023–2025 data.

## Main Finding
ETS provided the best predictive performance overall, with a test-set MAPE of about 1.34% and RMSE of about 10,019.5, outperforming the other models in forecast accuracy.

## Files
- `Final version.Rmd` — source analysis and code
- `Final-version-copy.html` — rendered report
- `Final.pptx` — presentation slides
- `MRTSSM44000USN.csv` — dataset

## Tools
- R
- R Markdown
- forecast package
- ggplot2

## Future Improvements
A potential next step is to study the structural break caused by COVID-19 more explicitly by comparing models trained on pre-COVID and post-COVID periods separately.

## Author
Yunelle Teng
