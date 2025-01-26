# Forecasting-Time-Series
This study explores time series models to forecast U.S. residential energy consumption (BTU) from 2011-2019. The data shows strong seasonality with consumption spikes in winter and summer months due to heating and cooling needs, without a constant trend indicating external factor dependencies.

Multiple forecasting approaches were tested. **Holt Winter's Method**, using Triple Exponential Smoothing, achieved 5.82% MAPE and 99.17 RMSE, struggling with April and June predictions. **LOESS Decomposition with log transformation** performed better at 4.05% MAPE and 88.79 RMSE, though June and December proved challenging.

**SARIMA models** showed the best results. The initial SARIMA(11,1,1)(1,1,1)[12] achieved 3.43% MAPE, with difficulties in March and November. The final optimized model SARIMA(1,0,0)(2,1,0)[12], using auto-selected parameters via pmdarima, delivered the best performance overall.

In order of accuracy: SARIMA(1,0,0)(2,1,0)[12] performed best, followed by SARIMA(11,1,1)(1,1,1)[12], LOESS Decomposition, and Holt Winter's Method. The strong performance likely stems from the dataset's clear annual seasonal patterns rather than model superiority.
