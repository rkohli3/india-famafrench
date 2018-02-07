.. _shrt-avl:

Short Selling in India
========================

NSE Regulations and SLBS
---------------------------


According to `NSE <https://www.nseindia.com/products/content/equities/slbs/slbs.html>`_ `Short Selling means selling of a stock that
the seller does not own at the time of trade. Short selling can be done by borrowing the stock through Clearing Corporation/Clearing
House of a stock exchange which is registered as Approved Intermediaries (AI's). Short selling can be done by retail as well as
institutional investors. The Securities Lending and Borrowing mechanism allows short sellers to borrow securities for making delivery.`

Short Selling intraday is not limited by restrictions, provided the investor covers (buys) his/her position the same day, i.e. Intraday Trading.


The National Securities Clearing Corporation Ltd. as an Approved Intermediary launched the Securities Lending  & Borrowing Scheme (SLBS)
on April 21, 2008. This scheme is facilitated on an automated screen based platform where the order matching is on price time priority and
where the participant needs to quote the lending fee per share on the order matching platform. [#]_

According to the SLBS `website <https://www.nseindia.com/products/content/equities/slbs/features_slbs.htm>`_,

- The Tenure of borrowing and lending is available up to a period of 12 months

- Placing an early recall for the securities lent is provided as a facility

- Making an early repayment as a facility is provided to the borrower.



The Hypothetical Portfolio
----------------------------

To test the feasibility of implementing both long and short factor portfolios,
we create a hypothetical portfolio on September 29, 2017 for the sorting done on
March 31, 2017, consisting of Value Weighted factor portfolios based on Size,
Value and Momentum by allocating ₹ 25 MM in the ratio of 4:4:2, respectively.

This process is initially carried on all the long positions for Size, Value and
Momentum and then for short positions.


.. figure:: _static/hypothetical.png
  :scale: 50%
  :align: center

  `The Table above shows the Hypothetical Portfolio of Long only Factors with
  capital of Rupees 25 Million in the ratio of 4:4:2 to Value, Size and Momentum
  respectively.`


The net positions consist of 409 stocks that need to be short sold and 448
stocks that need to be bought as of September 29, 2017.

There were 868 stocks trading on the last sorting date ie March 31, 2017 and
857 stocks on the most recent rebalancing date and date of hypothetical
portfolio creation ie September 29, 2017 from the universe of stocks that
have ever been a part of Nifty 500 Index. Rest have either been merged,
suspended, or delisted. Due to the missing data, the 30th percentile for 868
stocks, which is 260th item, does not match our number of stocks for upper and
bottom HML. The case of missing data is also applicable for SMB.


The NSE SLBS website updates the securities available for borrowing/lending at
4:15 pm IST every trading day. The list of Trading Holidays
can also be found `here <https://www.nseindia.com/products/content/equities/slbs/mrkt_timing_holidays.htm>`_

The following table shows the :ref:`shrt_avl_tbl` on a particular day.
Although, the NSE website updates this table every trading day at
4:15pm IST, we update the table once every week on Friday at 9:00am EST


You can also ``Download`` the `table <https://www.nseindia.com/content/slbs/slb_elg_sec.csv>`_ showing the short availabilities. The link
redirects you to the NSE website for an automatic download.



.. toctree::
   :maxdepth: 2
   :caption: Contents:

   shrt_avail










.. rubric:: Footnotes

.. [#] `Features of SLBS <https://www.nseindia.com/products/content/equities/slbs/features_slbs.htm>`_
