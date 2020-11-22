-------------------------------------------------------------------------------------------------------
Version 1.0
-------------------------------------------------------------------------------------------------------

>Dependent on tickers.csv to match stocks from top 100 stock data.

We have 2 input files in total:
MCAP_TOP100.xlsx
tickers.csv
(only NSE Top100 data)

>Fetches data that the top 100 stock contains and returns the similar tickers upto 2 matches for nse and 
bse respectively.
>Mismatch in words may produce unusable ticker names for files without close matching symbol names.
>Able to produce square matrix of stock data along with market data (of daily returns).

>All calculations are done on Daily Returns.
>Beta calculation is for stocks from NSE are compared with NSE Market data.(NIFTY100)
>Calculation of Beta for top 100 stocks is done and plotted against the names of the stocks using 10 year data
from 01-08-2010 to 01-08-2020 (1st August)
>Calulation and plotting of Beta from year 2013-2018 vs. 2018-2020 data is done.

Observations:

We observe the Beta values range from 0.249551 (ALKEM.NS) to a top value of 1.651020 (HINDALCO.NS)

The beta values for the ten lowest and highest stocks have the highest variance compared to the stocks lying in
between

-------------------------------------------------------------------------------------------------------
Version 2.0 (Current Version)
-------------------------------------------------------------------------------------------------------

>Now no longer depends on tickers.csv to match stock names and obtain tickers.
>Data of top 100 stocks directly obtained from BSE India and NSE India website can be used for calculation.
That is the only input data required in this version.

We have 2 input files in total:
MCAP_TOP100.xlsx
MCAP_TOP100BSE.csv
(top 100 NSE and top 100 BSE)

>All Operations converted to callable functions to avoid repetition of code and increased runtime.
>Beta values of Both NSE and BSE stocks can be found. With a change in the parameter value of market_price, 
stock_price in the Merge function defined in the notebook corresponding to the top 100 data of NSE and BSE respectively.

>The calculations performed in version 1 are repeated here for BSE Stocks this time.
>Beta values for 10 year data is done (01-08-2010 to 01-08-2020).
>Beta values from 2010-2015 are compared with data from 2015-2020.
>Also group values of size 10 of Beta vs. Average Returns are computed.

Observations:

We observe that beta values range from 0.292113 (NESTLEIND.BO) to a peak value of 1.437835 (IBULHSGFIN.BO)
Also the variance is very high towards the top end of the beta values.

For the comparision of 2010-2015 and 2015-2020 stocks data we notice that few stocks have been delisted and few stocks
have their IPO after the year 2015.

Ex:
RBL Bank Limited (RBLBANK.BO) which had an IPO on Aug 19,2016.

From the scatter plot we get the grouped values of Beta vs Average Return.