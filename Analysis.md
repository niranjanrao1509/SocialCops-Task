The technique used to perform analysis-
● Cleaning the data ,which had many issues from naming errors to missing values to
limited or high degree Skeweness
● Removing the outliers, from removing abnormal prices due to incorrect data to illogical
data values, using standard outlier filtering processes and visualising to confirm
● Analysis of Seasonality in the Prices and removing it to understand general trend in the
price movements
● Comparing Prices (MSP,RAW and Deseasonalized) to observe APMC, as well as
commodity pricing trends and come up with standard solutions to fix any anomalies if
exist
● Finally, observing Price fluctuations across years


Seasonality Type Detection
● Procedure -
○ Use seasonal_decompose
○ Use it’s residuals and eventually their Auto-Correlation-Function values to detect
Type of Seasonality (Multiplicative or Additive)
○ Collect unique pairs of APMC and Commodity to get all the records for that pair and
uses seasonal_decompose and acf to detect type
○ Check for Seasonality by plotting Auto-correlation grams

Deseasonalize Prices based on detected Seasonality Type
Procedure-
● Seasonal_decompose to get the seasonal component of the time-series
data for a particular pair of APMC,Commodity
● Removing the seasonal component from the price for all the pairs
● Plotting the result from the seasonal_decompose to confirm if there is a
seasonality component, which did exist
● Plotting the Raw(modal_price) and Deseasonalized Price to observe smoothening of
the line, indicating removal of Seasonality and Stationarity in Time-Series
