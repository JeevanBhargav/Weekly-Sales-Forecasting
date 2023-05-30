# Weekly-Sales-Forecasting
# Description:
In this project, we aim to forecast weekly sales based on a dataset that includes information such as date, weekly sales, holiday, temperature, fuel price, CPI (consumer price index), and unemployment. Various predictive analysis methods are applied to generate sales forecasts.
# These are the steps that were followed to conduct the prescriptive analysis:

## Naïve Forecast:
Utilized the previous week's sales value as the forecast for the current week.
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/0d8d3503-eacf-4d4c-b139-54f7db8438b1)
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/0ea331b3-9669-4202-b1f1-64adcf8e4a59)

## Moving Average (N=3):
Calculated the average of the previous three weeks' sales and used it as the forecast for the current week.
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/53debf89-9769-4020-9f13-a7974c53708e)
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/99590630-f65c-4bf7-b988-98b29d0e9be3)

## Weighted Average:
Assigned weights 𝛼!"# = 0.5, 𝛼!"$ = 0.3, 𝛼!"% = 0.2 to the sales of the previous three weeks.
Computed the weighted sum of the sales to obtain the forecast for the current week.
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/9c6ced71-f6be-4f1f-a95e-6e5515c254e6)
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/d5112138-7f30-4797-8e94-321f1a8c987c)

## Exponential Smoothing:
Employed the exponential smoothing method with a smoothing constant of 0.5.
Generated the forecast by adding a percentage of the forecast error (previous forecast minus previous sales) to the previous forecast.
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/a460d7a7-2ae0-4cce-897d-65ac59f61e71)

## Linear Regression:
Conducted linear regression analysis considering all predictor variables (holiday, temperature, fuel price, CPI, unemployment).
### Generated the coefficients of the intercept and factors influencing demand using Regression in Data Analysis Add-on.
![Screenshot 2023-05-30 082545](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/7e5ce238-b7ce-4b98-bf79-25c902f05350)
![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/3589def5-50e9-4920-a376-c6abd103f400)


![image](https://github.com/JeevanBhargav/Weekly-Sales-Forecasting/assets/130612387/f894e186-cbf2-4cd2-b15f-ad24bf597f57)


### Utilized the formula: intercept + sumprod(factor coeff * factor actual values) to forecast sales based on the regression model.



# Conclusion:
Through the application of various forecasting methods, we have generated sales forecasts for the weekly sales dataset. The Naïve Forecast, Moving Average, Weighted Average, and Exponential Smoothing methods provide simple yet effective ways to predict sales based on historical data. Additionally, the linear regression analysis incorporating predictor variables offers a more comprehensive approach to forecasting. By considering factors such as holidays, temperature, fuel price, CPI, and unemployment, the linear regression model provides insights into the impact of these variables on sales. The combination of these forecasting methods provides a range of approaches to predict weekly sales, allowing for informed decision-making and planning.





