# ⚡ Electricity Demand Forecasting Using Time Series Models

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/GIVEN-CHINYAMA/electricity-demand-forecasting/blob/main/electricity_demand_forecasting.ipynb)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-black?style=flat-square&logo=github)](https://github.com/GIVEN-CHINYAMA/electricity-demand-forecasting)
![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=flat-square&logo=tensorflow)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)

> **Author:** Given Chinyama
> **Institution:** Kwame Nkrumah University
> **Date:** May 2026

---

## 👆 Click "Open in Colab" Above to View the Full Notebook

GitHub cannot render large notebooks with embedded visualisations.
Click the **Open in Colab** button above to view the complete project
with all code, outputs, and 23 professional charts.

---

## Results Summary

| Model | RMSE (MW) | MAE (MW) | MAPE | R² |
|-------|-----------|----------|------|----|
| ARIMA(3,1,3) | 2,453.98 | 1,885.90 | 11.89% | -0.82 |
| SARIMA(2,1,0)(2,0,0,7) | 2,014.40 | 1,529.17 | 9.84% | -0.22 |
| Prophet | — | — | 7.49% | — |
| **LSTM** | **736.10** | **571.54** | **3.86%** | **0.84** |

**LSTM achieved 96.1% forecast accuracy — best model on all metrics.**

---

## Project Overview

Forecasting daily electricity demand using 5,057 observations from
the AEP grid (2004-2018). Four models are built, trained, evaluated,
and compared across 11 stages in a complete end-to-end pipeline.

---

## What This Project Covers

| Stage | Description |
|-------|-------------|
| Stage 1 | Environment setup |
| Stage 2 | Data collection (AEP Kaggle dataset) |
| Stage 3 | Preprocessing and EDA (7 plots) |
| Stage 4 | Feature engineering (13 features) |
| Stage 5 | Stationarity testing and decomposition |
| Stage 6 | ARIMA model |
| Stage 7 | SARIMA model |
| Stage 8 | Prophet model |
| Stage 9 | LSTM neural network |
| Stage 10 | Model comparison |
| Stage 11 | 30-day future forecast |

---

## Technologies Used

| Tool | Purpose |
|------|---------|
| Python 3.10+ | Core language |
| TensorFlow / Keras | LSTM model |
| Statsmodels | ARIMA / SARIMA |
| Prophet (Meta) | Seasonal forecasting |
| pmdarima | auto_arima order selection |
| pandas / numpy | Data manipulation |
| matplotlib / seaborn | Visualisation |
| Google Colab | Cloud execution |

---

## Key Findings

1. **LSTM outperformed all 3 other models** on every metric
2. SARIMA improved ARIMA by **17%** by capturing weekly seasonality
3. Strong dual seasonality confirmed — summer and winter demand peaks
4. Weekday demand is consistently **800+ MW higher** than weekends
5. The ADF test confirmed the series is already stationary (p=0.000)

---

## How to Run

Click the **Open in Colab** button at the top of this page.

Or run locally:
```bash
git clone https://github.com/GIVEN-CHINYAMA/electricity-demand-forecasting.git
pip install pandas numpy matplotlib seaborn statsmodels pmdarima prophet tensorflow
jupyter notebook electricity_demand_forecasting.ipynb
```

---

## Dataset

**AEP Hourly Energy Consumption** from Kaggle
- Source: [kaggle.com/datasets/robikscube/hourly-energy-consumption](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption)
- 121,000+ hourly records resampled to 5,057 daily observations
- Coverage: 2004 to 2018

---

*If you found this useful, please star the repository!*
