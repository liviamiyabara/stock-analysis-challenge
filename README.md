# stock-analysis
Challenge 2: VBA

## Overview of Project

The analysis was developed to help the user determine the total daily volume and return for a set of stocks in a selected year. Daily volume is the total number of shares traded during a day; it calculates how actively a stock is traded. The yearly return is the percentage difference in price from the beginning  to the end of the year; showing the investor if the shares gained or lost value with time. 

In the output table, Steve will be able to evaluate which stocks had greater returns to help his parents make informed decisions about where to invest based on historical data.

## Results
#### Stock Performance Analysis
![ScreenShot](https://github.com/liviamiyabara/stock-analysis-challenge/blob/main/Resources/All%20Stocks%20(2017%20%26%202018).png)

Overall, 2017 was a good year for most of the companies in the analysis except for TERP, which was the only share that lost value in that year, -7.2% return. The stocks with the highest returns were DQ (199.4%) and SEDG (184.5%).

In 2018, the scenario is quite the opposite from previous year; most companies lost their stock value, only RUN and ENPH had positive returns (84.0% and 81.9% respectively). DQ and JKS had the worst performance based on the tickers in the list with -62.6% and -60.5% return respectively.   

The analysis indicates that just considering the historical stock information might not be the best method to determine which stocks someone should invest. For Steve’s parents that invested everything in DQ shares, 2018 was not a profitable year.

#### Code Execution Time
![ScreenShot](https://github.com/liviamiyabara/stock-analysis-challenge/blob/main/Resources/Code%20running%20time.png)

The new refactored macro decreased the running time from 8.20 to 0.07 seconds, improving it by 99%. The main driver for the optimization was the tickerIndex variable that access the correct index across the four different arrays: 

*	tickerVolumes: holds the sum of the total number of shares traded during a day for a given ticker
*	tickerStartingPrices: stores the starting price of a specific ticker
*	tickerEndingPrices: stores the ending price of a specific ticker
*	tickers: stores the specific ticker name

Below is the detailed code for the loop, only one Index was applied to 4 arrays:
![ScreenShot](https://github.com/liviamiyabara/stock-analysis-challenge/blob/main/Resources/Loop%20tickerIndex.png)

## Summary
Summary: In a summary statement, address the following questions.
#### a) What are the advantages or disadvantages of refactoring code?

#### b) How do these pros and cons apply to refactoring the original VBA script?
