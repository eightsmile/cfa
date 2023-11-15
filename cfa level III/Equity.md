# Equity

## Overview

### Income associated with an Equity Portfolio

1. Dividend Income
2. Securities Lending Income: lend to short seller
   - dividends on loaned stock are compensated by the borrower
   - Reinvestment return of cash collateral are received
3. Dividend Capture 
   - buy a stock before ex-dividend date
   - hold it throng the ex-dividend date
   - sell that stock after ex date
4. Writing Options 
   - Covered call: long stock + write a call
   - Cash-coverd put: sell a put + buy bond, at same strike price

### Fees

1. Management Fees 与业绩无关，只与 AUM 相关
2. Performance Fees (incentive fee): high water mark
3. Administration Fees, which is part of the management fees
4. Marketing and Distribution fees
5. Trading Costs 
    1. explicit cost: broker commission, stock exchange fee, taxes, etc  , directly visible
    2. implicit cost: bid-ask spread, price impact from transaction 由于买卖量大导致价格被推高或拉低 造成的成本 Delay cost (slippage costs) 由于延迟下单导致的cost

### Shareholder Engagement 股东主义

Shareholder engagement refers to investors and managers interacting with companies in ways to potentially favourably impact the stock price.

Pros: (1) improve efficiency (2) get internal information about that firm (3) for active and large investors, so benefits all shareholders, and (4) good for non-financial interests such as ESG.

Cons: (1) time consuming and costly, (2) aim to increase stock price, so focus on short-term goals, not long-term goals, (3) acquisition of material non-public info, so may have risks of insider trading (4) conflict of interest between large and small stakeholders.

---

## Passive Equity Investment

Tracking Error T.E. (active risks $\sigma_A$), (active return $R_A$)

$\sigma_A = s.d. (R_A) = \sqrt{\frac{\sum (RA - \bar{RA})^2}{n-1}}$ 

As $\bar{RA} = 0$

$\sigma_A = \sqrt{\frac{\sum RA^2}{n-1}}= \sqrt{\frac{\sum (R_p- R_{benchmark})^2}{n-1}}$

So, portfolio 偏离 Benchmark, 则 T.E 提升

### Indexes as a Basis for Investment

- **Rules-Based**: follow the rules of weighting scheme, rebalancing frequency, etc

- **Transparent**

- **Investable** 如 HS300为市值最大的300只，那么300th可能会变化，此时 passive invest to replicate the index 会导致300th经常更换而带来transaction cost

    - Buffering 缓冲区: establishing ranges around breakpoints that define whether a stock belongs in one index or another.

        左右两边取一个范围 构建更宽的边界，达到更大的边界才会纳入或剔除。

    - Packeting: splitting stock positions into multiple parts 

- Determine the Market Exposure (based on IPS)
    - Market Segment (domestic or international, developed or emerging  or frontier, etc)
    - Capitalisation (size factor): market size, large-cap, mid-cap, etc
    - Growth versus Value (style factor): choose exposure to growth stock (high PE high PB) or value stock (low PE PB)
    - Other risk factors

### Stock Construction

- #### **Stock Inclusion**

    1. Exhaustive 穷举选取一定范围内所有的stock
    2. Selective Approach 选取特定的stock

- #### **Weighting Methods**

    1. Market-Cap Weighting (**S&P500**) (偏向large cap stock)

        1. Liquidity-weighted 这种方法会 heavily weighted Large-cap stocks, as they are higher liquid

        2. Free-Float weighting 考虑在流通的 stock 的总市值（限售的 stock 被剔除了）

        3. Mean-variance efficient: x-axis is s.d.; y-axis is return 画出CML curve

            Offer the highest return for a given level of risks

    2. Price Weighting (**Dow Jones, Nikkei 225**) （偏向高价股 high price stocks）

        - 股数相同，都为 k 股，所以为 price weighted

        - $w_i = \frac{MV_j}{\sum MV_i} = \frac{P_j \times K}{\sum P_i \times K} = \frac{P_j}{\sum P_i}$

        - 高价股权重会更高，对 index 影响更大。growth stock 往往 price 更高，所以 growth stock 在 index 中权重更大
        - 拆股 split 等影响 price，会影响 price weighting。但 拆股不会影响 market cap，所以不影响 market-cap weighting。
        - Rebalance weights 因为拆股会带来价格减半，但是实际上 index 不应受到影响，所以要调整 被拆 stock 的 weight 使得拆股前后 index 数值一致，然后反推 weights。所以 price weighting 会调整 weights

    3. Equal Weighting （偏向小盘股 small cap stocks）

        $w = \frac{1}{n}$

        $Index = \frac{\sum^N_1 P_i}{N}$

        - Least concentrated 不会受市值影响
        - Slow changing sector exposures, less reconstitution 因为无偏好，所以不会因为 index 内股票代表性不足而重构，所以 重构较少
        - Affected by price change, so small stocks (, which are highly volatile) would make the index highly fluctuated. 小市值股票会带来 index 波动
        - Require **regular rebalancing**. I.E. 如果 Price Increase，那么在 index 中 MV 上升，所以 weights 上升。要保证 equal weight 就需要 卖出该 stock。所以经常需要 rebalance。且 高抛低吸 contrarian
        - Limited Investment Capacity （1）因为小盘股多，流动性不好（2）需要老 rebalance 所以 trading cost 高

    4. Fundamental Weighting （上证50）(偏向 低价股 low price stock）（虽然叫 fundamental 但是实际上上 通过市场上的错误定价 而选择特定的 tilt 挣钱

        weight stocks by fundamental factors

        1. Contrarian 
        2. value tilt 偏向价值股 ，price 低，所以 dividend ratio $D/P$ 高，基本面越好

    - P.S.:
        1. If Tax-Exempt, then equal-weighted 的 trading cost 的和 capital gain 的税被免了，所以 equal-weighted might get **superior return**
        2. Market-cap weighted & Fundamentally weighted
            - Shared characteristics: low cost, rules-based, transparency
            - Different: market-cap-weight is based on EMH 在 CML 上。但 fundamentally weights exploit inefficiencies in market pricing.
    
- #### **Rebalancing and Reconstitution** 

    - **Rebalance**: reweighs
    - **Reconstitution**: add or remove new stocks
    - **Rebalance and Reconstitution create turnover and transaction costs **这俩都会带来 transaction cost 成本提升
        - turnover for **developed country's stocks** & **large-cap** index are infrequent so less cost
        - benchmark using **stock selection** rather than **exhaustive inclusion** makes high turnover.

- #### Concentration

    - Effective # Number of Stocks 真正在市场上能影响股票价格 的 #，所以
        - the greater the efficient #, the more diversified
        - the lower the efficient #, the more concentrated
        - Effective # <=> $1 / HHI = \frac{1}{\sum w^2}$
        - if equal weighted, $w = 1/n$, then HHI is lowest, and effective # is highest. Thus, Equal Weighting would generating greatest diversification, lowest concentration.


![Screenshot 2023-11-15 at 21.35.44](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-15%20at%2021.35.44.png)

### Passive Investment Strategy (Smart Beta)

![Screenshot 2023-11-15 at 21.40.43](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-15%20at%2021.40.43.png)

因为是 passive strategy ，所以目的是与 benchmark 收益一致。

但是 实际操作上 要 face transaction cost, bid-ask spread etc。

所以 T.C. (transaction cost) 会导致portfolio 收益降低。

那么为了保证 port return 与 benchmark return 一样，就需要做一部分的 active management。如多投好的factor，挣positive active return；或者少投差的factor，挣positive active return

只需要一点点的盘子，做 active 来 cover transaction cost，所以主要还是 passive，smart beta 部分只有一点点

#### Factors

- Growth factor
- Value
- Size
- Yield
- Momentum
- Quality
- Volatility

#### Three Strategies

1. Reutrn Oriented Strategy 为了挣钱 

   - Divident Yield Strategy
   - Momentum Strategy
   - Fundamentally Weighted Strategy (value > Growth)

2. Risk-Oriented Strategy 为了降低组合的风险

   - Volatility Weighting $w = 1/\sigma_i$
   - Minimum Variance Investing

   Pros: lower risks

   Cons: use historical data may not indicate future

3. Diverisifcation-oriented Strategy

#### Pros and Cons of Smart Beta

- **Pros**: 
  1. pure exposure to specific segments
  2. less costly T.C. than active management
  3. can have factor rotation that incorporate investors' view
- **Cons**:
  1. concentrate risk exposure
  2. have tracking error
  3. T.C. or management fee is less than active management but greater than passive cap-weighted investing 

### Pooled Investment

(1) open-end mutual fund

(2) ETFs

#### 对比 mutual fund & ETFs

![Screenshot 2023-11-15 at 22.17.16](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-15%20at%2022.17.16.png)

#### ETFs v.s. Mutual Funds

- ETFs' redemption 拿钱换股，所以其他人 包括 NAV不会被影响，所以 redemption is more cheap and efficient, but Mutual Funds 会拿钱换stock
- ETF s higher transaction costs from commission and bid-ask spread. 因为可以在二级交易 and might be illiquid in some secondary market

###  Derivatives

- Completion Overlays: 用于建仓
- Rebalancing Overlays: 用于调仓
- Currency Overlays: 用于调整 FX risks

- **Pros**:
  1. Quick, efficient, cheap
  2. liquid
  3. Easy to leverage
- **Cons**:
  1. need **roll over**
  2. position limit
  3. mgiht not be qualified to be traded in exchange. 可能无法在 交易所交易. OTC might be exposed to counterparty risk
  4. basis risks can increase trading error 当 future/forward 的 selling date != expire date 可能会有 tracking error