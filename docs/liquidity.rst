.. _liqtcost:

Liquidity Risk and Transaction Cost
====================================

To execute trading of portfolio, constituents of which are Small Cap stocks, requires understanding of the Liquidity Risk and Transaction Cost associated with each
constituents of the portfolio. Investors should not underestimate the indirect costs associated with liquidity and the the Bid/Ask Spread. In times of low liquidity,
many investors rely on the dealers, or market markers for the provision of liquidity. [#]_ Bondarenko (2001), decomposes the Bid/Ask Spread into two components, Adverse Selection
& Imperfect Competition, in which he argues that market makers post prices that are steeper than efficient prices, which then becomes the source of their profit.




`Bid/Ask <http://www.nasdaq.com/investing/glossary/b/bid-asked-spread>`_ Spread is the difference between the highest price (`Ask <http://www.nasdaq.com/investing/glossary/a/ask>`_) and investor is willing to sell its securities and the lowest price (`Bid <http://www.nasdaq.com/investing/glossary/b/bid-price>`_) at which the
investor is willing to buy its securities. One of the determinants for this Spread is the Volume of shares traded. Intuitively, it makes sense. Consider an example
when the market has less number of shares of a Security "A". This Security A is considered illiquid, which implies, lesser people trading the security at a particular
point in time. Because it is more difficult for the market maker to convert this Security A to cash, the broker needs to compensated more, thus adding to the Bid/Ask
Spread and Transaction Cost.

It is thus safe to say that market efficiency and quality could be estimated by means of how narrow the Bid/Ask Spreads are. There has
been no dearth of literature on measuring the efficiency and quality of markets through the Bid/Ask Spreads. In fact overreaction and under reaction in markets, both of which are
market inefficiencies, have often widened the Spreads in markets. [#]_ This implies that using Bid/Ask Spreads to is indeed a theoretically correct and practically sane method of
measuring market efficiencies.


Let's go back to the example of Security A. Let's say that the current Bid price is $5 and the current Ask price is $5.05, the the Bid/Ask Spread of Security A is  approximately
0.9% of the current Ask price. The implication of this spread is that the investor loses 0.9% (1%) of the value of Security A as soon as he/she buys (short sells) the Security.


For the purpose of implementation and choosing the constituents of our portfolio
from a liquid and an efficient market, we study the behavior of bid/ask spread
as a percentage of average mid-price intraday of present 500 constituents of
Nifty 500 with respect to turnover and market capitalization.
We conclude that the smaller the stocks, the more the transaction cost.
Similarly, we find a linear relationship between the turnover of the stock and
the average bid/ask spread.

.. raw:: html

  <iframe align = "center" width="1050" height="610" frameborder="0" scrolling="auto" src="_static/Total_BidAsk.html"></iframe>


`In the Figure above, we notice that the average Bid/Ask Spread as a percentage of the Mid-Price (average intraday) of NIFTY500 constituents is a decreasing function of Volume, implying
that higher trading volume comes with tighter spreads and better quality in Market Microstructure.`





.. raw:: html

  <iframe align = "center" width="1050" height="610" frameborder="0" scrolling="auto" src="_static/TopBidAsk.html"></iframe>


  <iframe align = "center" width="1050" height="610" frameborder="0" scrolling="auto" src="_static/BottomBidAsk.html"></iframe>


`The figures above indicate the bid/ask spread percentage for the Smallest 100
stocks and the Largest 100 stocks from the Index of 500 stocks.`
We noticed a high disparity between the bid/ask spread of Largest 100 and
Smallest 100 stocks in the Nifty 500 index. We also studied the bid/ask spread
percentage from October 13, 2017 to November 13, 2017 and found that for Top 100
and Bottom 100 Stocks, the bid/ask spread percentage did not move much for this
period, which had neither any inclusion nor exclusion of stocks to the index.

Due to unavailability of intraday data for stocks other than those in Nifty
500 Index, we could not conduct the same test for stocks outside of Nifty 500 Index.
However, as discussed above, to be considered for the index, the constituent has
to be in the top 800 rank based on the average daily turnover and average full
market capitalization. Moreover, given that the constituents of Nifty 500
(500 out of more than 1600 stocks) represent 95.2% of market capitalization of
National Stock Exchange, it is safe to assume that the stocks that are not a
part of the index may have a higher bid/ask spread percentage on an average and
may also be less liquid because of their size and low trading activities.


Another important determinant of Bid/Ask Spread is volatility. Many studies
(Chordia, Roll, and Subhramanyam, 2000, 2001, 2002) [#]_ find that higher
liquidity is generally associated with lower volatility and Transaction
Cost [#]_. This makes sense intuitively, as volatility usually increases during
a rapid decline or advancement of market, in which case market makers step in to take advantage of - and profit
from - the change. As the price of a security advance increasingly, more
investors are willing to pay a higher price for the security enabling the market
maker to charge a higher (premium)
than efficient price on the security.










.. rubric:: Footnotes

.. [#] Bondarenko, Oleg (2001). `Competing Market Makers, Liquidity Provision and Bid-Ask Spread <https://papers.ssrn.com/sol3/papers.cfm?abstract_id=253894>`_ , `Journal of Financial Markets`, 4, 269-308
.. [#] Allen B. Atkins and Edward A. Dyl (1990),  `Price Reversals, Bid-Ask Spreads, and Market Efficiency <https://www.jstor.org/stable/2331015>`_, `The Journal of Financial and Quantitative Analysis`, 25(4), 535-547
.. [#] Chordia, Tarun, Roll, Richard and Subrahmanyam, Avanidhar, (2002), `Order imbalance, liquidity, and market returns <https://EconPapers.repec.org/RePEc:eee:jfinec:v:65:y:2002:i:1:p:111-130>`_ , `Journal of Financial Economics`, **65**, issue 1, p. 111-130.
.. [#] Li, J., & Wu, C. (2006). `Daily Return Volatility, Bid-Ask Spreads and Information Flow: Analyzing the Information Content of Volume <http://www.jstor.org/stable/10.1086/505249?seq=1#page_scan_tab_contents>`_, `Journal of Business`, 79(5), 2697-2739 doi:10.1086/505249
