java c
~PS.II~
PROBLEM SET 2   
Fall 2024
Department of Economics
[Due online 11/29]
LOW-FREQUENCY DATA
1. A minimum variance stock portfolio bundles stocks so that the re-sulting portfolio variance is as low as possible. Optimal weights in this portfolio are given by:
where   Σ   is the covariance matrix of returns for a sample of n stocks. Optimal weights can be positive (long), negative (short), or zero (stock isn’t part of the minimum variance portfolio).
One may additionally impose that the minimum variance portfolio is zero beta, so that it’s as little exposed to market risk as possible. This involves adding the constraint w0β = 0 to the problem above. The resulting optimal-weight vector is:

1. Derive   
2. You will now assemble a zero-β   minimum variance portfolio using data. You’ll obtain optimal portfolio weights based on a random sample of stocks during 2000-2009, evaluate the portfolio performance in-sample, and then evaluate the portfolio’s performance out-of-sample during 2010-2023. This is a very simple and rough exercise - you won’t reshuffle weights, rebalance, or tilt the portfolio to capture specific factors.
You are going to download all the data you need from WRDS. First you need to create a profile in your computer that allows you to submit queries using R, Python etc. If you use R like me, please follow these instructions (for Mac and Windows):
https://wrds-www.wharton.upenn.edu/pages/support/programming-wrds/programming-r/r-from-your-computer/.
You can find similar instructions for other software here:
https://wrds-www.wharton.upenn.edu/pages/support/programming-wrds/.
In the .../week1/code/ folder, you’ll find the R script. wrds_zeroBeta_portfolio.R. The top of the script. contains the WRDS key (change the "user=" term with your WRDS username).

You need to run this chunk every time your WRDS session expires (you’ll get an error in R). You’ll only be able to connect to WRDS and download data if you have created the .pgpass file (for Mac or the equivalent for your OS) as described in the link above. Th代 写Department of Economics PROBLEM SET 2 Fall 2024Python
代做程序编程语言e script. is annotated. It will draw a random sample of 400 stocks from the US stock market to assemble the portfolio. The data being queried from WRDS come from CRSP. You can find out more information about it on the WRDS website.
3. Run the whole code. It ends with computations of Sharpe ra-tios for the portfolio during 2000-2009 and SPY (to represent the SP 500). After you run the entire code, run saveRDS(portfolio_returns, "~/PATH/yourlastname_yourfirstname.rds") which will save your dataset contain-ing the stock codes, monthly returns, the portfolio monthly and cumulative return, and market monthly and cumulative returns. You’ll upload this data to a link to be provided later. If you export this file incorrectly you won’t receive points for this question.
4. Report the portfolio and market Sharpe ratios calculated at the end of the code. Your portfolio performance may be better or worse than that of the market. The 2000-2009 period purposefully picks a bear market. Because the zero beta portfolio is uncorrelated with the market, it should perform. relatively well when the market is down. But since we’re not targeting any return level in the optimization problem, after discounting the risk-free rate (which was 4.46% during the period) there may be no excess return. After reporting the Sharpe ratios discuss the portfolio performance taking into account these factors.
5. The code has the part "Out-of-sample evaluation" missing. Write up the necessary code and present the portfolio and market Sharpe ratios for the post-2009 period. This will tell you how well the portfolio would’ve done. The code you’ll write will look similar to the one for the in-sample exercise. Some stocks will be discontinued. You should not rebalance the portfolio or re-calculate the optimal weights. The risk-free rate during the period is 2.38%. Report the Sharpe ratios and discuss the possible reasons for the under/over performance of the portfolio out-of-sample relative to the in-sample performance you previously computed.







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
