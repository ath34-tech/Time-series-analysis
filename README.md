# Time Series Analysis (TSA) Exploratory Data Analysis (EDA) and ARIMA Forecasting

This project involves performing exploratory data analysis (EDA) on time series data using Pandas, Matplotlib, and Plotly. The data is fetched using the Yahoo Finance library. The aim is to visualize and understand the underlying patterns, trends, and seasonalities in the data.This demonstrates stock price forecasting using the ARIMA (AutoRegressive Integrated Moving Average) model. It includes fetching stock data, training an ARIMA model, forecasting future prices, and evaluating model performance

## Requirements

Ensure you have the following packages installed:

- `pandas`
- `matplotlib`
- `plotly`
- `yfinance`
- `statsmodels`
- `scikit-learn`
- `pmdarima`

You can install the required packages using pip:

```bash
pip install pandas matplotlib plotly yfinance statsmodels sklearn
```
## Project Structure
**tsa_eda.ipynb:** Jupyter Notebook containing the code for EDA.
**Forecasting.ipynb:** Jupyter Notebook containing the code for Forecasting.
### Data
The time series data is fetched using the Yahoo Finance library and stored directly in a Pandas DataFrame. The data should contain at least a datetime column and one or more columns with numeric values representing the time series.

## Steps Performed
**Fetch Data:**

- Fetch the time series data using the Yahoo Finance library and store it in a Pandas DataFrame.
**Load Data:**

- Parse datetime columns and set them as the index.
**Summary Statistics:**

- Display summary statistics of the data.
- Identify missing values and handle them appropriately.
**Time Series Plots:**

- Plot the raw time series data using Matplotlib and Plotly.
- Visualize trends, seasonal patterns, and any anomalies.
**Resampling and Analysis:**

- Perform resampling to different frequencies (e.g., daily, monthly).
- Analyze the resampled data to observe patterns and trends.
**Rolling Statistics:**

- Calculate and plot rolling mean to observe trends and variability over time.

**Cumulative Moving Average:**

- Calculated and plotted Cumulative Moving Average, helping in observing long-term trend by removing short term fluctuation

**EMA/EWMA:**

- Filters out the noise
- Assists in managing risk by providing a dynamic view of market conditions
- Generates trading signals by comparing the EWMA with the stock's price or other moving averages
- Measures and models the volatility of a stock, which is crucial for risk management and derivative pricing
### Features of ARIMA Forecasting

- **AutoRegressive (AR) Component**: Models the relationship between an observation and several lagged observations. Parameter `p` represents the number of lag observations.
- **Integrated (I) Component**: Deals with differencing to achieve stationarity. Parameter `d` represents the number of times the series is differenced.
- **Moving Average (MA) Component**: Models the relationship between an observation and a residual error from a moving average model applied to lagged observations. Parameter `q` represents the number of lagged forecast errors.
- **Stationarity**: ARIMA models require stationary data. Achieve stationarity through differencing or transformations.
- **AutoARIMA**: Automates parameter selection for ARIMA models.
- **Model Diagnostics**: Analyze residuals and perform tests like the Ljung-Box test to check model fit.
- **Forecasting**: Generate forecasts with confidence intervals for future values.
- **Seasonal ARIMA (SARIMA)**: Extends ARIMA to handle seasonal patterns with additional parameters.

### Usage
To run the analysis, open the Jupyter Notebook tsa_eda.ipynb and execute the cells step-by-step. You can run Forecasting.ipynb and execute all cells.

### Example Plots
- Time Series Plot
- Rolling Mean
- CMA
- EMA/EWMA
### Conclusion
This EDA provides insights into the time series data, helping to identify trends and patterns. These insights are crucial for further modeling and forecasting tasks. Future additions will include advanced smoothing techniques such as Exponential Smoothing (ETS) and exponential weighted Moving Average (EWMA) to enhance the analysis.
