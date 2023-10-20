# Pairs_Tradind_and_CoIntegration_Strategy

Stocks pair Selected:  Cipla - Lumin

Hedge ratio = 0.924
P value = 0.014936

Annualized Sharpe Ratio 
July 2020-July 2021: 0.61
July 2021-July 2022: 0.70
July 2022-July 2023: 1.32

CAGR = 15.60%
Maximum Drawdown = 36.66%
Frequency of trades placed = 216 days
Cumulative Returns = Rs.53,593.91(53.59 %)

Pairs Trading

When it comes to pairs trading methods, a pair of equities usually takes a market-neutral stance. This indicates that the approach is unaffected by the direction of the larger market, whether it is rising or falling. Instead, the idea of mean reversion is the foundation of pairs trading. It becomes relevant when two securities with a strong positive correlation veer off the beaten track. The fundamental premise is that they'll eventually return to their previous pattern.
A price spread between the two equities is created during this deviation, providing a chance for profit. A trader can open a long position on a stock that is predicted to rise and a short position on one that is expected to fall. Profitable trades are produced when the pair behaves as predicted.
The trader can limit their losses even in situations where the pair deviates from expectations. This occurs as a result of gains on one security more than offsetting losses on another. Thus, pairs trading offers a way to reduce prospective losses and is used as a type of hedging.





Importing Stock Price dataset
A three-year retrospective analysis, starting in July 2017 and ending in July 2020, is conducted in the context of putting this approach into action. Finding stock pairs with a high positive correlation is the main goal. We have chosen to concentrate on the individual stocks that make up the Pharma index since we will be paying closer attention to stocks that are part of the pharmaceutical industry.


Identifying stock pairs
Cointegration
The most common test for Pairs Trading is the cointegration test. Cointegration is a statistical property of two or more time-series variables which indicates if a linear combination of the variables is stationary.
Let us understand the statement above. In this case, The two-time series variables are the log of stocks A and B prices. A Linear combination of these variables can be a linear equation defining the spread.
The spread can be computed using the formula:
Spread = log(a) – n * log(b)
Here, 'a' and 'b' represent the prices of stocks A and B, respectively. For each purchase of stock A, you've simultaneously sold 'n' shares of stock B. If both 'a' and 'b' increase in such a way that the spread value diminishes, it can lead to a financial loss. This occurs because stock A is experiencing slower growth compared to stock B, and you have a short position on stock B.
So if we start with ‘n’, which is called the hedge ratio, so that spread = 0, the property of stationary implies that the expected value of spread will remain as 0. Any deviation from this expected value is a case for statistical abnormality, hence a case for pairs trading!

Finding stock pairs with cointegrated time series:

The pairs of stocks having a cointegration are those with a p-value less than the threshold of 0.05. P-value can be considered as a measure of the strength of cointegration between the two series. A lower p-value indicates a stronger cointegration.
Testing Data
The strategy will use a 3-year testing period from June 2020 to June 2023. The spread between the prices of the two stocks will be used to determine points of entry and exit for the pair trade.
Z-Score
A Z-score is a numerical measurement that describes a value's relationship to the mean of a group of values. The Z-score is measured in terms of standard deviations from the mean. Z-scores also make it possible to adapt values from data sets having very different ranges to make scores that are comparable. Essentially, z-scores can shrink a large range of values into a much smaller range, which is easier to handle.
Trading Strategy
After generating the graph of the z-score, we need to set our entry and exit points on which our positions or holdings depend.
Very first, we have deduced the mean of the z-score, which is  0.553471.
By doing random data sampling for the threshold values of entry points, we have come up with the following values, which generate maximum profits.
The values that we have taken are:(We have plotted these values in the graph provided with the code.)

Entry points: lower threshold value: 1.2
                      (When the z-score goes below this, we will be taking a LONG position i.e we’ll buy Cipla and sell Lupin)
                     upper threshold value:1.6
                       (When the z-score goes above this, we will be taking a SHORT position i.e we’ll sell Cipla and buy Lupin)

Risk Management Measures

Exit points: When these points are crossed, we’ll pause trading or don't hold any position to stop loss.
Lower exit point: 0.9
Upper exit point: 2.0

Trading Signals Generated and Position Sizing
From this, we have extracted the positions of both stocks, which are indicated in the following manner: 1 indicates to buy that stock
                             -1 indicates selling that stock
                             0 indicates we are not holding any positions on that particular day


Portfolio Performance
PnL Calculation
We have obtained a profit of over Rs. 53,593.91. 
The explanation of this calculation follows below :
Through the positions acquired previously,
We calculate the total assets corresponding to CIPLA and the total assets corresponding to LUPIN
Summing this up, we get our profit
Portfolio Returns

Annualized Sharpe Ratio 
July 2020-July 2021: 0.61
July 2021-July 2022: 0.70
July 2022-July 2023: 1.32

CAGR = 15.60%
Maximum Drawdown = 36.60%
Frequency of trades placed = 216 days
Cumulative Returns = Rs. 53,593.91(53.59%)

CAGR :
Compound annual growth rate (CAGR) is a way to measure how an investment or business has grown over a specific period of time. It takes into account the effect of compounding, which means that the growth builds upon itself.


Maximum Drawdown:
Maximum drawdown (MDD) is a measure of an asset's largest price drop from a peak to a trough. Maximum drawdown is considered to be an indicator of downside risk, with large MDDs suggesting that down movements could be volatile.

Sharpe Ratio :
The Sharpe ratio compares the return on investment with its risk. It's a mathematical expression of the insight that excess returns over a period of time may signify more volatality and risk rather than investing skill.
