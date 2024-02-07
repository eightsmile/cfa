## Trading

### Algorithm Trading

- Schedule Algorithm: 
  - appropriate for orders **do not have expectations for adverse price movement** during the trade horizon. 
  - have greater risk tolerance for **longer execution time periods** 
  - and are more concerned with **minimizing market impact.** 
  - are often appropriate when the **order size is relatively small** (e.g., no more than 5%–10% of expected volume), the **security is relatively liquid**
- Trade in Open Mkt
  - can be quickly traded, avoid the impact of information leakage and alpha decays



Schedule Algorithm

-  POV algorithms incorporate real-time volume by following (or chasing) volumes, they may not complete the order within the time period specified.
- TWAP algorithms, which send the same number of shares and the same percentage of the order to be traded in each time period, will help ensure the specified number of shares are executed within the specified time period.

Dark Pool:

- **trading venue, transactions and quantities is always reported**, however, there is **no pre-trade transparency such as limit price** that reflect intention to trade, which gives you as a trading party advantage of information not being leaked to the market.
- Dark pools provide **anonymity** because no pre-trade transparency exists. Exchanges are known as lit markets (as opposed to dark markets) because they provide pre-trade transparency—namely, limit orders that reflect trader intentions for trade side (buy or sell), price, and size. However, with a dark pool, there is less certainty of execution as compared to an exchange

### Performance Attribution or Appraisal 

- **Performance Appraisal** draws conclusions regarding the quality of a portfolio manager’s investment decisions. 评判 PM 怎么样
- **Performance attribution** should help explain how performance was achieved by breaking apart the return or risk into different explanatory components.

### Performance Allocation Method 

- **Returns-based attribution method** is most appropriate when the underlying portfolio holdings are not readily available with sufficient frequency at the required level of detail (e.g., hedge funds).  缺holding数据时，直接拿factor 和 return 跑回归，easy
- **Transactions-based attribution method** is most effective for active stock selection portfolios because it captures both the holdings and the transactions (purchases/sales) completed within the defined period, which would allow the entire excess return to be quantified and explained.
- **Holdings-based attribution method** is most appropriate for investment strategies **with little turnover (e.g., passive strategies)** because it only references the beginning-of-period and end-of-period holdings and ignores individual transactions. In this case, because the identified portfolio is a very active strategy, the holdings-based method would not be the most appropriate method*.*

### Benchmark

- **Manager universe** is a broad group of managers with similar investment disciplines. Although not a benchmark, per se**, a manager universe allows investors to make comparisons with the performance of other managers following similar investment disciplines.** 可以选各种形式的 style 对比
- **Factor-model-based benchmarks** are constructed by regressing the portfolio’s return against the factors believed to influence returns. 用于比回归
- **Absolute return benchmark** is a minimum target return that the manager is expected to beat. It will not determine how the manager performed relative to other managers. 比绝对值是否满足minimum，不比别的portfolio