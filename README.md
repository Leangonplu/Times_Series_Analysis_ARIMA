# Times_Series_Analysis_ARIMA

Application for Univariate Time Series with ARIMA: Algorithmic Trading Model for $/£ Exchange Rates (Dataset: YahooFinancials)

This project focuses on building an algorithmic trading model for analyzing and forecasting $/£ exchange rates using the ARIMA (Autoregressive Integrated Moving Average) model. ARIMA is a statistical model commonly used for time series analysis and forecasting. It combines autoregressive, moving average, and integration components to capture trends, seasonality, and autocorrelation in sequential data.

## Dataset
The dataset used in this project is obtained from YahooFinancials and covers a 3-year period from January 1, 2017, to December 31, 2020. It consists of daily exchange rate data for $/£, including the opening rate (OHLC), maximum and minimum intraday rates, and closing rate. The data is stored as a Pandas dataframe for further analysis and modeling.

## Data Preprocessing
To prepare the data for analysis, we create a new series by calculating the differences between consecutive closing rates. This series represents the one-day return. However, it's important to note that the return cannot be calculated for the first trading day of the dataset, so the corresponding cell will contain NaN (not available). Additionally, the return series is obtained by applying the differencing process to the closing price series to ensure stationarity.

## Data Analysis
We perform various analyses on the data to gain insights into its characteristics:

- Stationarity: We conduct the Augmented Dickey-Fuller test to determine if the series is stationary.
- Distribution: We examine the normality of the series using autocorrelation plots and the Jaque-Bera test.
- Autocorrelation: We check for autocorrelation in the residuals.

## Algorithmic Trading Model

The objective of the model is to generate buy and sell signals based on the detected patterns in the exchange rate data:

a) If the real exchange rate is higher than expected, indicating overvaluation, it is a sell signal.
b) Conversely, if the exchange rate is lower than expected, indicating undervaluation, it is a buy signal.

The model utilizes the ARIMA framework to analyze the time series, detect patterns, and generate trading signals based on the identified patterns.

By leveraging the power of ARIMA and analyzing the $/£ exchange rates, this application aims to provide valuable insights for algorithmic trading strategies in the foreign exchange market.
