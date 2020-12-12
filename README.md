# stock-analysis
Challenge 2: VBA

## Overview of Project

The analysis was developed to help the user determine the total daily volume and return for a set of stocks in a selected year. Daily volume is the total number of shares traded during a day; it calculates how actively a stock is traded. The yearly return is the percentage difference in price from the beginning  to the end of the year; showing the investor if the shares gained or lost value with time. 

In the output table, Steve will be able to evaluate which stocks had greater returns to help his parents make informed decisions about where to invest based on historical data.

## Results
### Stock Performance Analysis
![ScreenShot](https://github.com/liviamiyabara/stock-analysis-challenge/blob/main/Resources/All%20Stocks%20(2017%20%26%202018).png)

Overall, 2017 was a good year for most of the companies in the analysis except for TERP, which was the only share that lost value in that year, -7.2% return. The stocks with the highest returns were DQ (199.4%) and SEDG (184.5%).

In 2018, the scenario is quite the opposite from previous year; most companies lost their stock value, only RUN and ENPH had positive returns (84.0% and 81.9% respectively). DQ and JKS had the worst performance based on the tickers in the list with -62.6% and -60.5% return respectively.   

The analysis indicates that just considering the historical stock information might not be the best method to determine which stocks someone should invest. For Steve’s parents that invested everything in DQ shares, 2018 was not a profitable year.

### Code Execution Time
![ScreenShot](https://github.com/liviamiyabara/stock-analysis-challenge/blob/main/Resources/Code%20running%20time.png)

The new refactored macro decreased the running time from 8.20 to 0.07 seconds, improving it by 99%. The main driver for the optimization was using the tickerIndex variable in a loop that accessed the correct index, in our case each ticker, across the four different arrays: 

*	tickerVolumes: sum of the total number of shares traded 
*	tickerStartingPrices: starting price of the stock
*	tickerEndingPrices: ending price of the stock
*	tickers: ticker name

Below is the detailed code for the loop, only one Index was applied to 4 arrays:
![ScreenShot](https://github.com/liviamiyabara/stock-analysis-challenge/blob/main/Resources/Loop%20tickerIndex.png)

## Summary
Summary: In a summary statement, address the following questions.
#### a) What are the advantages or disadvantages of refactoring code?
#### b) How do these pros and cons apply to refactoring the original VBA script?

Besides decreasing the code execution time and using less memory, refactoring can simplify the code by making it more efficient. It can reduce the number of repetitive tasks and avoid manual changes making it more reliable. Refactoring helps the user to read, understand, modify and even enhance the code even further.

The disadvantages of refactoring would be the time and resources consumed on something that was already delivering what you needed. It can also lead to new bugs or mistakes that can take time to be solved depending on the complexity. 

For this challenge, the refactored macro can be beneficial in the future if the user wants to process a larger amount of data (e.g. all stocks traded), but for the specific analysis done for only 12 stocks it might not be worth to spend time improving the code since the process time was not an issue. The difference to run the macros was just seconds, so the waiting time was not perceptible to the user. It would be a different situation if the analysis contained thousands of stocks, then the code execution time would be relevant. 
