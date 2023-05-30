# Weekly-Sales-Forecasting
# Introduction:
In this project, we have analyzed a weekly sales dataset to forecast future sales. The dataset contains several columns, including date, weekly sales, holiday indicator, temperature, fuel price, CPI (consumer price index), and unemployment rate. Our objective was to develop accurate sales forecasts using various time series forecasting methods (predictive analysis) and evaluate their goodness of fit. 
The dataset that includes information such as:
Date: The date of the sales record
Weekly Sales: The sales amount for the corresponding week
Holiday: A binary variable indicating whether the week includes a holiday (1 for holiday, 0 otherwise)
Temperature: The temperature during the week
Fuel Price: The fuel price during the week
CPI: Consumer Price Index, providing a measure for inflation
Unemployment: The percentage of unemployment. 
# Data Analysis and Preprocessing
Before proceeding with the forecasting, we conducted data analysis and preprocessing steps. This included examining the dataset for missing values, outliers, and inconsistencies. We ensured that the data was properly formatted and suitable for analysis. Additionally, we explored the relationships between variables through visualizations and statistical analysis to gain insights into their potential impact on sales.

# Forecasting Methods
To forecast weekly sales, we employed the following methods:

## Naïve Forecast:
Utilized the previous week's sales value as the forecast for the current week.
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/0d8d3503-eacf-4d4c-b139-54f7db8438b1)
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/0ea331b3-9669-4202-b1f1-64adcf8e4a59)

## Moving Average (N=3):
Calculated the average of the previous three weeks' sales and used it as the forecast for the current week.
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/53debf89-9769-4020-9f13-a7974c53708e)
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/99590630-f65c-4bf7-b988-98b29d0e9be3)

## Weighted Average:
Assigned weights 𝛼1 = 0.5, 𝛼2 = 0.3, 𝛼3 = 0.2 to the sales of the previous three weeks.
Computed the weighted sum of the sales to obtain the forecast for the current week.
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/9c6ced71-f6be-4f1f-a95e-6e5515c254e6)
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/d5112138-7f30-4797-8e94-321f1a8c987c)

## Exponential Smoothing:
Employed the exponential smoothing method with a smoothing constant of 0.5.
Generated the forecast by adding a percentage of the forecast error (previous forecast minus previous sales) to the previous forecast.
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/a460d7a7-2ae0-4cce-897d-65ac59f61e71)

## Linear Regression:
Conducted linear regression analysis considering all predictor variables (holiday, temperature, fuel price, CPI, unemployment).
Generated the coefficients of the intercept and factors influencing demand using Regression in Data Analysis Add-on.
![Screenshot 2023-05-30 082545](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/7e5ce238-b7ce-4b98-bf79-25c902f05350)
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/3589def5-50e9-4920-a376-c6abd103f400)

Utilized the formula: intercept + sumprod(factor coeff * factor actual values) to forecast sales based on the regression model.
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/9dd41a5d-c5f2-486f-93ed-de2e1a8ce03e)

![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/f894e186-cbf2-4cd2-b15f-ad24bf597f57)
# Goodness of Fit Evaluation:
In addition to generating sales forecasts using different time series methods, we have also evaluated the goodness of fit for each method by calculating Mean Absolute Error (MAE), Mean Squared Error (MSE), and Mean Absolute Percentage Error (MAPE).

The formulas used for these metrics are as follows:
#### Mean Absolute Error (MAE) or (MAD):
MAE = Sum(abs(Actual - Forecast)) / n
#### Mean Squared Error (MSE):
MSE = Sum((Actual - Forecast)^2) / (n - 1)
#### Mean Absolute Percentage Error (MAPE):
MAPE = Sum(abs(Actual - Forecast) * 100 / Actual) / n
Where:
Actual represents the actual sales values.
Forecast represents the forecasted sales values.
n represents the number of data points or weeks in the dataset.
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/842e69c0-d76a-4982-a127-32a6bcd4b3e0)

In MAD/MAE: The forecasting method with the lowest MAD value indicates the best goodness of fit. In this case, the Naïve method has the lowest MAD value, indicating a better fit compared to other methods.

In MSE: Similarly, the forecasting method with the lowest MSE value is considered to have the best goodness of fit. In this case, the Regression method has the lowest MSE value, suggesting a better fit.

In MAPE: The forecasting method with the lowest MAPE value signifies the best relative accuracy in terms of percentage errors. Lower MAPE values indicate a smaller average percentage difference between the actual and forecasted values. Here, the Naïve method has the lowest MAPE value, indicating a better fit.


# Conclusion:
This project focused on forecasting weekly sales using various time series methods. We explored the Naïve Forecast, Moving Average, Weighted Average, Exponential Smoothing, and Linear Regression techniques. The combination of these forecasting methods provides a range of approaches to predict weekly sales, allowing for informed decision-making and planning.

By evaluating the goodness of fit using metrics such as MAD, MSE, and MAPE, we identified accurate and reliable forecasting method for the dataset at hand. These forecasts can assist businesses in making informed decisions, optimizing inventory, and planning for future sales.




