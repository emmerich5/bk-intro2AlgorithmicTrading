# CHAPTER 01 - HISTORY

* Blocking trade (1970): Algos used mainstream for trades > $1 million, or when > 10,000 shares.
* Pair trading (1980)

# CHAPTER 02 - ALL ABOUT TRADING ALGORITHMS YOU EVER WANTED TO KNOW

* Algos efficiency varies depending on the trading stock and time.
* The SEC required by 2011 a minimum of $25K for a trading account.
* Trading time is 9:30am to 4pm Eastern time. Some traders work only half a day.
* This book will focus on the American equity market traded on NASDAQ, and the NY Stock Exchange.
* Assets such as futures, commodities, options, and foreign exchange are different, with some basic similarities.

# CHAPTER 03 - ALGOS DEFINED AND EXPLAINED

* The parameters utilized in an algo are critical. Wrong parameters will lose trades. Seldom will these parameters be adaptive (ML)
* Real time data feed of a trade consist of:
   * Stock ticker symbol
   * timestamp
   * number of shares
   * trade price
* Every time new data arrives, it triggers an action.
* Every time a trade is executed, it must be protected by a Stop Loss Order.

# CHAPTER 06 - CURRENTLY POPULAR ALGOS

* Tier-1 Algos do trades for long term duration. No immediate return.
* High Frequency trading minimize the time of trading for immediate profit. Small points earned sum in millions a year.
* Individual traders use Algos for immediate returns.
* Front run is the act of being discovered.

## Sniffer Algos
* Search predictability in competitors and takes advantage of this by front running it.

## VWAP - Volume Weighted Average Price
* Oldest, most utilized, and most modified by Tier-1
* Utilizes real time and historic volume data as criterion
* It slices large orders over a set period of time or trading session with respect to the stock's liquidity.
* Utilized on longer duration orders.
* Trader specifies the number of discrete time intervals (waves)
* Trading volume is higher in the first part of the trading session to minimize adverse impact on price.

### PROs:
* Slicing up large orders in smaller ones minimize the risk.
* It makes the order size invisible to other participants.
* Because of waves strategy is difficult to be identified by market competitors.

## TWAP – Time Weighted Average Price
* Divides the order kind of evenly over a number of discrete time intervals (waves)
* Often used with fuzzy time intervals to avoid Sniffers

## POV – Percentage of Volume
* Goal is to participate in volume trading, but with only fractions of the volume percentage.
* Staying under the radar is critical on this algo.

## Other Algos
Most Algos will try to hide the trading strategy from competitors:
* ‘Black Lance’ – Search for Liquidity
* The Peg – Stay Parallel with the Market
* Iceberg – Large Order Hiding
* Recursive Algos: call themselves until a condition is met.
* Serial Algos: Execute a set series sequentially with logic that provides branching.
* Parallel Algos: Execute multiple instructions simultaneously.
* Iterative Algos: Utilize parameterizable values to make decisions with repetetive constructions (if/then, do/while, for/next)

## Pair Trading Strategy
* Certain stocks usually in the same sector/industry have strong correlation in their price movement.
* Departure from the pattern of correlation is temporal, reverting back to the correlation over time.
* When correlated pairs move in opposite directions:
  * Short (Sell) the out-performing stock
  * Long (Buy) the under-performing stock
* Algo watches their movement, and when a deviation crosses a preset limit, the trade goes into effect.
* Algo works over extended period of time (weeks)
* CONs: risk of liquidity crisis in one stock blocks the close of trade.

# CHAPTER 07 - A PERSPECTIVE VIEW FROM A TIER 1 COMPANY (UBS)
* Assembling a team of highly qualified experts. There are three areas to draw from – the traders, the quantitative analysts and the technology developers – and it is essential to create a balance between these three groups.
  * Traders will be more experienced in the end-users’ behaviour and what they would like to see in terms of functionality.
  * Successful systems will not be one that runs the most mathematically sophisticated modelling process but is nigh on impossible to be used by the average trader.
* Sophistication in trading and modelling means that there is now far more input from quantitative analysts.
* Each new generation of algorithm trading tools, however, is
not built from scratch. It is about finding the limitations of existing systems and then making the necessary improvements so it is often a case of moving sideways in order to go forwards.

# CHAPTER 08 - HOW TO USE ALGOS FOR INDIVIDUAL TRADERS
* ALPHA ALGO = primary goal is profit per trade.
* Liquidity: 2,500 shares traded at the same time represent 1 or 2 small orders of Tier-1, which they see individual traders as noise in the system.
* Avoid: stock trades with love volumes < 500,000 shares per session.
* Parameterization: Loopback of 5 session is often normal and varies according to the stock activity. Parameterization should be made daily. For high volume stocks > 15 million loopback increases to 10 trading sessions.
* Algo must constantly backtest at least 6 out of 10 profitable.
* When parameterization is used +/- 5% the Algo should reach at least 7 out of 10 trades profitable (however neither top traders achieve this)


# CHAPTER 09 - HOW TO OPTIMIZE INDIVIDUAL TRADER ALGOS
## Choosing Stocks
* Volume > 1 million shares per session
* Trade price > $35

## Optimization
* Use basis points per trade per second (per cent profit per second):
   * Example: $1 on $100 share in 30 seconds is better than the same in 60 seconds. $1 on $50 is better than both.
 * The longer your money is exposed to the market the longer the time that it is at risk.
 * The longer your money is tied up to a trade the longer the time you cannot use it on another trade.
 * If a trade is producing a predefined return as measured by total basis points per second for the trade, the position is hold. As soon as the basis points return wanes past a set threshold, the protective stop is cancel, and the trade is put as sell market order.
 * Parameters used often include SMA, LMA, and EMA.
 * Optimal Algo is 8 profitable trades out of 10, with 2 stopped out by a stop loss Algo.
 * Profitable trades average between 25 and 40 basis points net of commission.

# Chapter 10
* Master Algo deploying dozens of specialized
algos matched to the personality profiles of individual stocks with real-time backtesting and parameter setting.
