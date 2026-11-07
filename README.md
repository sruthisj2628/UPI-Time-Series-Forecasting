# UPI Transaction Volume Forecasting Using Time Series Analysis

## Project Overview
This project analyzes historical monthly Unified Payments Interface (UPI) transaction data in India and forecasts future transaction volumes using Time Series Analysis techniques.

The project uses Moving Average and ARIMA models to identify trends, study historical transaction patterns, and predict future UPI transaction volumes.

## Objectives
- Analyze historical UPI transaction trends.
- Visualize monthly transaction volume and value.
- Apply Moving Average techniques.
- Check time series stationarity using the Augmented Dickey-Fuller (ADF) test.
- Develop and evaluate ARIMA forecasting models.
- Forecast UPI transaction volume for the next six months.

## Dataset
- **File:** `upi_monthly.csv`
- **Frequency:** Monthly
- **Period:** April 2016 – August 2026
- **Observations:** 125
- **Target variable:** `VolumeMn` (transaction volume in millions)

## Technologies Used
- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Scikit-learn

## Methodology
1. Data loading and preprocessing.
2. Exploratory Data Analysis (EDA).
3. Trend visualization.
4. Moving Average analysis (3-month, 6-month and 12-month).
5. Stationarity testing using ADF.
6. ACF and PACF analysis.
7. ARIMA model development.
8. Model evaluation using MAE, RMSE and MAPE.
9. Residual diagnostics.
10. Six-month forecasting.

## Model Performance

| Model | MAE | RMSE | MAPE |
|---|---:|---:|---:|
| ARIMA(3,2,1) | 4849.78 | 6163.63 | 22.77% |
| ARIMA(1,1,1) | 3870.25 | 4626.43 | 18.33% |
| ARIMA(2,1,1) | 1921.79 | 2395.08 | 9.17% |

ARIMA(2,1,1) achieved the lowest forecasting errors among the three evaluated models.

## Six-Month Forecast
The selected model forecasts UPI transaction volume from September 2026 to February 2027.

| Month | Forecasted Volume (Millions) |
|---|---:|
| September 2026 | 25134.47 |
| October 2026 | 25683.20 |
| November 2026 | 26208.00 |
| December 2026 | 26727.42 |
| January 2027 | 27247.93 |
| February 2027 | 27771.74 |

## Key Findings
- UPI transaction volume shows a strong increasing trend.
- The original time series is non-stationary.
- Differencing was applied to achieve stationarity.
- ARIMA(2,1,1) performed best among the tested configurations.
- The forecast indicates continued growth in UPI transaction volume.

## Project Structure
```text
UPI-Time-Series-Forecasting/
├── Dataset/
│   └── upi_monthly.csv
├── Python_Analysis/
│   └── UPI_Transaction_Trend_Analysis_and_Forecasting_Using_Moving_Average_and_ARIMA.ipynb
├── Report/
│   └── UPI Transaction Volume Forecasting Using Time Series Analysis.pdf
└── README.md
```

## Limitations
- Forecasts are based on historical monthly data.
- External factors affecting UPI adoption are not included.
- Model performance is based on the selected train-test split.
- The selected model is the best among the configurations evaluated, not necessarily the optimal ARIMA model.

## Conclusion
This project demonstrates the application of Time Series Analysis for understanding and forecasting UPI transaction volume. Moving Average and ARIMA techniques were used to analyze historical patterns and estimate future transaction trends.

## Author
**Sruthi S J**  
B.Tech Computer Science and Engineering
