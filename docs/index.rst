.. FamaFrench documentation master file, created by
   sphinx-quickstart on Fri Sep  1 13:16:33 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

India's Smart Beta
======================================

`Compiled by Prof. Jim Kyung-Soo Liew and Ravpritpal (Ravi) Kohli (MS in Finance Johns Hopkins University)`



.. raw:: html


	<div class = "intrinsic container">
		<iframe align = "left" width="100%" height="650" frameborder="0" scrolling="auto" src="_static/cum_rets_facs.html"></iframe>
	</div>



Summary
--------

Fama and French (1992, 1993) [#]_ introduced pioneering research that has made factor investing pervasive.
Their HML (high book-to-market stocks minus low book-to-market stocks) and SMB (small capitalization stocks minus big
or large capitalization stocks) has become staples in the business school classroom education.

Approximately a decade later, Liew and Vassalou (2000) [#]_ extended Fama-French's SMB and HML by linking them to real
economy variables, namely future real GDP (gross domestic product) growth. These results have helped investors better
understand the importance of risks and returns available in both the domestic (United States markets) and the
developed international markets.

However, emerging market research into Fama-French factors has been limited and suspect at best. In this work,
we work we attempt to provide more transparency into the emerging market Fama-French factor world by understanding
the subtle nuances within these markets. Our first market that we examine is the Indian Stock Market.


The Factors
------------

We document the returns of the Fama-French factor mimicking portfolio from March 31, 1996 – September 29, 2017. The factors, namely High Book–to-Market  `minus` Low Book-to-Market (HML), Small Market Equity
`minus` Big Market Equity (SMB), Winners `minus` Losers (WML) and Market Risk Premium (MRP), have positive average annualized returns of 5.45%, 12.18%, 5.71% and 6.81% respectively. Moreover, WML shows a
negative correlation with HML and SMB, however, has a negligible correlation with MRP (See Appendix for descriptive statistics).
The Fama/French factor replicating portfolios, both long and short, outperformed the excess returns to Market, which is given by :math:`MRP` where :math:`MRP = R_{m} - R_{f}` and
:math:`R_{f}` is the yield on 91 days Indian T-bill  in this period. HML, however, has underperformed the :math:`MRP`


.. raw:: html

	<iframe align = "left" width="100%" height="600" frameborder="0" scrolling="auto" src="_static/FamaFrenchFacs.html"></iframe>





However, due to unavailability of stocks required to be short sold and high liquidity risk eventually leading to high transaction cost and more market impact, we find that implementing these factors in India
to be extremely difficult. We document these results in the following section :ref:`shrt-avl` and :ref:`liqtcost`. We discuss and propose alternative solutions of long-only portfolios.


Long Only Portfolios
---------------------

In Figure above (top), the aggregate performance of long-only equally weighted (EW) (See Appendix for long only value weighted) portfolios based on Value (High B/M), Size (Small Cap), and Momentum(Winner)
has been nothing but impressive. It has outperformed the market (Nifty 50), which is used as a market proxy as it is indicative of the broader market, significantly. The portfolio of High B/M, Small Cap
and Winners has grown by 61x, 132x and 105x, respectively over the past 21.5 years (from March 31, 1996 – September 29, 2017) whereas Nifty 50 has grown by 9.9x in the same period.
To learn more about methodology check our :ref:`method-india` section.

The annualized returns for these long-only value weighted (VW) portfolios based on Value, Size, Momentum and Nifty 50 index are 18.7%, 27.37%, 21.27% and 13.54%, respectively (See Appendix for yearly returns).
This illustrates the outperformance of the long only factor portfolios compared with the market proxy.


These back-tested portfolios are free of **Survivorship Bias** and **Look Ahead Bias**, about which you can learn more about in :ref:`survivors` and :ref:`lookahead`.


The Indian Market
------------------


.. raw:: html

	<iframe align = "left" width="100%" height="600" frameborder="0" scrolling="auto" src="_static/T-bill3.html"></iframe>




The Indian Stock market has 21 stock exchanges, Bombay Stock Exchange (`BSE <http://www.bseindia.com/>`_) and National
Stock Exchange (`NSE <https://www.nseindia.com>`_) being the most prominent out of them offering high liquidity for investment.
Currently as of September 2017 the Market Capitalization for 5,828 companies listed on BSE is approximately US$ 1.94 Trillion [#]_.
Whereas the Market Capitalization for 1,681 companies listed in NSE is approximately US$ 1.7 Trillion as of March 2017.

Our universe, the Nifty 500 index accounts for approximately  95.2% of the free float market capitalization of the stocks listed on NSE as on March 31, 2017. [#]_

It is also interesting to note that the BSE Sensex, which consists of 30 Largest stocks in BSE,  has provided an aggregate of **97%** returns in this period and in the `Figure 2` above that
the Risk Free (:math:`R_{f}`) rate in India has been steadily declining, currently at an annualized yield of 5.8% `(See figure above).`










.. toctree::
   :maxdepth: 2
   :caption: Contents:

   Fama
   method
   crnt_posititions
   shrt_sllng_ind
   liquidity
   

































.. rubric:: Footnotes

.. [#] `"The Cross-Section of Expected Stock Returns" (1992) by Eugene F. Fama and Kenneth R. French <http://onlinelibrary.wiley.com/doi/10.1111/j.1540-6261.1992.tb04398.x/abstract>`_

.. [#] `"Can Book-to-Market, Size, and Momentum be Risk Factors That Predict Economic Growth?" (2000) by Jim Kyung-Soo Liew and Maria Vassalou <http://www.sciencedirect.com/science/article/pii/S0304405X00000568>`_

.. [#] http://www.bseindia.com/markets/Equity/EQReports/Historical_EquitySegment.aspx?expandable=7

.. [#] https://www.nseindia.com/products/content/equities/indices/nifty_500.htm
