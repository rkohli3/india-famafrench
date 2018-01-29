.. _method-india:

Methodology for India
=======================

Data
-----

The data have been extracted primarily from Centre for Monitoring Indian Economy (`CMIE ProwessDx <https://www.cmie.com/kommon/bin/sr.php?kall=wproducts&tabno=7010&prd=prowessdx&portal_code=030010040005000000000000000000000000000000000>`_). ProwessDx delivers financial performance data
and markets data on Publicly Listed companies in India. Other sources of Data are Bloomberg, Quandl API and Reserve Bank of India.

For each of the methodology below, we rebalance the portfolio every month and deploy a buy and hold strategy for ``currently`` equally weighted portfolio.

One Dimensional sorting
---------------------------

We apply the standard practice for sorting Winners and Losers as mentioned by Jegadeesh and Titman (1993) and popularized by Asness (1994)
where the stocks are ranked based on their cumulative returns for the past eleven months i.e t−12 to t−1, excluding the most recent month as
it is not an indicator of momentum. The top 30% are considered as the Winners and bottom 30% are considered Losers.

For the 1-D portfolios, we simply buy the Winners and short sell the Losers, thus to form Winners `minus` Losers (WML)






The total number of NSE and BSE companies that have survived as of March 2017 are illustrated below. The data accounts for
suspensions and delisting for firms and include companies only.


.. raw:: html




	<iframe align = "left" width="49%" height="400" frameborder="0" scrolling="auto" src="_static/NSE_survivors.html"></iframe>





	<iframe align = "right" width="49%" height="400" frameborder="0" scrolling="auto" src="_static/BSE_Survivors.html"></iframe>













1-Dimensional Sorting
----------------------------

We apply the standard practice for sorting Winners and Losers as mentioned by Jegadeesh and Titman (1993) [#]_ and popularized by Asness (1994) [#]_
where the stocks are ranked based on their cumulative returns for the past eleven months i.e t−12 to t−1, excluding the most recent month as
it is not an indicator of momentum. The top 30% are considered as the Winners and bottom 30% are considered Losers.

For the 1-D portfolios, we simply buy the Winners and short sell the Losers, thus to form Winners `minus` Losers (WML)

.. math::

	\text{WML = Winners stocks - Losers stocks}



Further, to sort one dimensionally for size, we first looked at the distribution of Market Equity for the NSE `sample` stocks over the timespan we covered and decided to chose the
median ME for the sample stocks as the breakpoint, where Small is :math:`< \text{Median}` and Big is :math:`\geq \text{Median}`, thus to form, Small Minus Big(SMB)

.. math::

	\text{SMB = Small stocks - Big stocks}

A similar approach was then used to sort one-dimensionally based on value using the Book-to-Market (BM) ratio. The cutoff points are the sample stocks' 30% 70% and 100% quintiles,
deciles, where High BM stocks are :math:`\geq \text{70th percentile}` and Low BM stocks are :math:`< \text{30th percentile}`, thus to form High Minus Low (HML)

.. math::

	\text{HML = High BM stocks - Low BM stocks}






2-Dimensional Sorting
----------------------

Following the methodology used by Fama-French (1993), we apply the sorting of portfolios based on Value and Size.
The HML and SMB are formed by the intersection of 3 portfolios based on Value and 2 portfolios based on Size.
The figure below shows the sorting of the 4 most recent periods. To check the behavior of the sorting, please visit Appendix.

.. raw:: html

	<iframe align = "left" width="50%" height="350" frameborder="0" scrolling="no" src="_static/sortingsmall2018.html"></iframe>

	<iframe align = "right" width="50%" height="350" frameborder="0" scrolling="no" src="_static/sortingsmall2017.html"></iframe>

	<iframe align = "left" width="50%" height="350" frameborder="0" scrolling="no" src="_static/sortingsmall2016.html"></iframe>

	<iframe align = "right" width="50%" height="350" frameborder="0" scrolling="no" src="_static/sortingsmall2015.html"></iframe>




The breakpoint for 2 portfolios based on Size is the Median ME of the universe of stocks used to form the above portfolios,
where Small is considered stocks having ME :math:`< \text{Median}` and Big is considered stocks having ME :math:`\geq \text{Median}`.
The breakpoint for the 3 portfolios formed on Value are the 30th, 70th and 100th quintiles, deciles of the B/M ratio
of the universe of stocks we cover, where High B/M stocks are :math:`\geq \text{70th percentile}` and Low B/M stocks are :math:`< \text{30th percentile}`.

We have illustrated our findings of the BM ratio and ME ranges from 1995 to 2017 for the universe of our stocks in the study.




.. raw:: html

	<iframe align = "center" width="100%" height="670" frameborder="0" scrolling="auto" src="_static/Sorting_BM.html"></iframe>

	<iframe align = "center" width="100%" height="670" frameborder="0" scrolling="auto" src="_static/Sorting_ME.html"></iframe>





To construct the HML and SMB we take the intersection of the 2 X 3 portfolios and get the 6 portfolios, namely Small Value (SV),
Small Neutral (SN), Small Growth (SG), Big Value (BV), Big Neutral (BN) and Big Growth (BG).


.. figure:: _static/Crossection1.png
	:scale: 50%
	:align: center

	`Figure above shows the cross-section of portfolios based on Size and Value using their respective cut-off points.`


.. math::

	    HML = \frac{1}{2}(SV + BV) - \frac{1}{2}(SG + BG)

.. math::

	    SMB = \frac{1}{3}(SV + SN + SG) - \frac{1}{3}(BV + BN + BG)


Similarly, to construct For WML we take the cross – section of portfolios based on Size and prior 11 month cumulative returns from
:math:`r_{t-12}` to :math:`r_{t-1}`, taking the top 30th percentile as Winners and Bottom 30th percentile as Losers to construct
Momentum portfolios based on Size, namely Small Winners (SW), Small Neutral (SN), Small Losers (SL), Big Winners (BW), Big Neutral (BN) and Big Losers (BL).
WML is the average of Winners minus average of Losers.

.. figure:: _static/Crossection2.png
	:scale: 50%
	:align: center

	`Figure above shows the cross-section of portfolios based on Size and prior 11 month returns using their respective cut-off points.`

.. math::

     WML = \frac{1}{2}(SW + BW) - \frac{1}{2}(SL + BL)

After sorting the portfolios on March 31st, represented by time t, of every year we find the monthly returns for the next 12 months,
represented by :math:`t+1`, :math:`t+2`,..., :math:`t+12`, by deploying a buy – and – hold strategy for a month, thus rebalancing monthly.
Returns are calculated using the formula below

.. math::

	r_t = \frac{P_{t}}{P_{t-1}} - 1

where

.. math::

	P_{t} = \text{Adj Closing Prices at time t}

	P_{t-1} = \text{Adj Closing Prices at time t-1}


`ProwessDx` provides unadjusted closing prices along with adjusting factors. Here, adjusting factors is a multiple that is used to adjust the unadjusted prices
for dividends and stock splits. The :math:`R_{m} - R_{f}` is the Value Weighted Nifty50 Index universe minus 91 – day T-Bill rate provided by the Reserve Bank of India (RBI).
This factor is represented by Market Risk Premium (MRP).

The descriptive statistics of cumulative returns for Fama-French factors as well as long only factor portfolios are provided in the Appendix.












.. rubric:: Footnotes


.. [#] Jegadeesh, N. and Titman, S. (1993), `Returns to buying winners and selling losers: Implications for stock market efficiency`, The Journal of Finance 48(1), 65–91.

.. [#] Asness, Clifford S., 1994, `Variables that explain stock returns`, Ph.D. Dissertation, University of Chicago.
