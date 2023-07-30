# energyforecasting
Power Usage Forecasting
**Project Overview**
This project aims to forecast daily power usage based on historical power usage data and weather data. The forecasting model can help predict future power usage and inform energy planning and resource allocation decisions.

**Data**
The data used in this project include:

Power usage data (power_usage_2016_to_2020.csv): This file contains hourly power usage data from 2016 to 2020. The columns include StartDate (the start date and hour of the power usage), Value (kWh) (the amount of power used in kilowatt hours), day_of_week (the day of the week, where Monday is 0 and Sunday is 6), and notes (categorization of the day as either 'weekday' or 'weekend').

Weather data (weather_2016_2020_daily.csv): This file contains daily weather data from 2016 to 2020. The columns include date, day of the week, maximum/average/minimum temperature, dew point, humidity, wind speed, pressure, and precipitation.

The power usage data and weather data are merged on the date to create a combined dataset for modeling.

**Methodology**
The project follows these steps:

Data Preprocessing: This includes converting date columns to datetime format, aggregating the hourly power usage data to daily data, and merging the power and weather datasets.

Exploratory Data Analysis (EDA): This involves generating plots to understand the distribution of data and the relationships between variables, and computing correlation coefficients.

Feature Engineering: New features are created, such as lag features, which represent the value of a variable at a previous time step.

Time Series Decomposition: The time series is decomposed into trend, seasonality, and residual components to understand the underlying patterns in the data.

Model Building and Evaluation: An XGBoost model is trained on the training data and evaluated on the test data. The model's performance is measured using root mean squared error (RMSE).

**Results**
The XGBoost model achieves a RMSE of approximately 13.54 on the test set. This means that on average, the model's predictions are about 13.54 kWh off from the actual values.

**Next Steps**
Potential next steps for this project include trying different models, tuning the model parameters, creating additional features and monitoring and updating the model over time.
