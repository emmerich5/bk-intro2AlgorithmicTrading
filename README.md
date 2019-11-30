# BOOK - AN INTRODUCTION TO ALGORITHMIC TRADING V2 (2011)

## Preface Part I

* Algorithmic is mainstream.
* Tier-1 corporations have a massive advantage and resources.
* Advantages: cost reduction (at least 6:1 ratio in savings per transaction), higher probability of success, and speed.
* By 2009, at least 50% of trading transactions where automated.
* Part I is focused on Tier-1 companies (Chapter 1 - 10)
* Part II is for individual trading with Leshik-Cralle ALPHA algorithm for manual trading.

## Preface Part II - THE LESHIK-CRALLE TRADING METHODS (Algorithms For Individual Traders)
* trade = thick
* Most stocks are unlikely to move very far in < 150ms
* Metrics should include:
  * Volatility
  * Volume
  * Price levels
* Trading is like predicting how the weather will be in three days, but calculated in minutes (3min)
* A trade consist of:
  * date
  * time of trade
  * volume (how many shares traded)
  * price at which changed hands
* A thick series is asynchronous.
* A time series aggregates trades into a time interval (min,seconds,etc)
* An algo should be able to recognize trade triggers:
  * peaks
  * troughs (valleys or negative peaks)
* Trade triggers should be  recognized between 3 to 7 ticks of the turn, which gives a high probability the trade price hasn't moved too much from thr trigger point.
* Long algos (Buying) are easier to implement because there are several selection of stocks.
* Sell algos are difficult to optimize because you can sell only what you bought.
* An algo should have a "Capital Protection Stop"

# ERRATA
* Missing CD which includes Excel formulas, and data.