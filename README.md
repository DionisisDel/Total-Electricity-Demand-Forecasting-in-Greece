# Total-Electricity-Demand-Forecasting-in-Greece

In this project, we forecast the total electricity demand in Greece for 5 years using ARIMA time series models. Specifically, we use historical demand data from 2006 to 2022 to predict the demand for the years 2023, 2024, 2025, 2026, and 2027. To perform the data analysis and visualization, the R programming language was used along with its respective libraries.

The first thing examined was whether the time series is stationary. For this purpose, the ACF and PACF functions were calculated, which revealed that the time series is not stationary. This claim was confirmed by the corresponding ADF and KPSS tests that were conducted.

To achieve stationarity, second-order differencing was required.

Subsequently, the auto.arima command was used to find the best ARIMA model based on MSE and AICc criteria. However, after testing, it was found that there is a better model according to these criteria than the one suggested by auto.arima. The table below shows some of the models that were tested.
![ARIMA models](https://github.com/DionisisDel/Total-Electricity-Demand-Forecasting-in-Greece/assets/105522901/b4d6cada-b2c1-4386-b6c7-33e24d0f45d6)

Ultimately, the ARIMA(1,2,1) model was selected. After examining whether the residuals of the model constitute white noise, the model was then used to make predictions.

## Comments

* From the graphical representation of the data, notable is the electricity demand value in the year 2008, where it reached a historical maximum of approximately 56 TWh. However, in 2009, there was a significant decrease due to reduced industrial loads and network-level consumption, attributed to the economic crisis that occurred during that period.
* In the graphical representation showing the forecasted values, one might expect an increase in electricity demand rather than the slight decrease observed. This is primarily due to the significant increase in electricity prices over the last two years, which has led consumers to reduce their usage. Additionally, the European Union's policies addressing the climate crisis and environmental protection have sensitized citizens to make smarter use of electricity, thereby reducing consumption.




Copyright © – All rights reserved Dionisios Delaportas, 2024

The above analysis was conducted as part of my thesis titled "Forecasting Electricity Demand Using Time Series Methods," of which I am the sole author. Copying, storing, and distributing this work, in whole or in part, for commercial purposes is prohibited. Reprinting, storing, and distributing for non-profit, educational, or research purposes is permitted provided the source is acknowledged and this notice is preserved.
The link to the entire thesis is available here: https://nemertes.library.upatras.gr/items/6e51ffcb-997a-4e20-a4b0-2a9aa0a2b7fb
