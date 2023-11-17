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

### Portfolio Construction

#### Full Replication

Full replication is preferred for indexes with small numbers of liquid stocks 因为 less liquid stock 会大幅增加交易成本T.C.

- **Pros**: Closely matches the index return, and simple
- **Cons**: Index does not consider trading cost, but build your own portfolio would take T.C.. Those T.C. would bring Tracking Error T.E.
    - whenever the index changes and we have to fully replicate by rebalancing or reconstituting, there would be T.C. and T.E. 当指数变带来重组和调权重的时候，会带来T.E.

![Screenshot 2023-11-16 at 08.28.25](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-16%20at%2008.28.25.png)

如果复制的 stocks 少，则复制的不准确，T.E. 大，如果复制的stocks 多，则 T.C. 大，T.E. 大。That is a tradeoff

#### Stratified Sampling 分组抽样

把 constituent stock 分为 subset，之后从中选取。 Create strata that are mutually exclusive and exhaustive 遍历但不重叠的分组

- Pros: avoid high cost of full replication, easy
- Cons: size of strata might be matter, and high tracking error

#### Optimisation

Using Algorithm to find parameter $w$ weights that can optimise the objective func.

- **Pros**:
    - lower tracking error than stratified sampling 
    - Can account for the covariance / correlation for diversification**Cons**:
- **Cons**
    - Historical data, corr might change
    - Dynamic optimisation would also be costly
    - Might be **mean-variance inefficient** 如果 objective func 不是 mean-var optim。解决 可以先mean-var optim 再走别的 opti

#### Blended Approach

1

### Causes of Tracking Error T.E.

- Number of Constituents
    - Number of constituents 成分股数越多, Tracking Error 越大。因为 illiquidity 大，且 T.C. 来自 rebalance and reconstitution 大
- Fees and Trading Costs
    - Management Fees, Commissions or Bid-ask Spread
    - illqudity
    - Higher Expense Ratio
- Cash Drag 
    - 由于指数不含cash，但是portfolio中往往有cash，且cash 部分没有 return，因此 portfolio 整体的return 会被拉低
- Intra-day Trading
    - index往往是用 Close price 算，但是自己构建 portfolio 是要自己交易的，价格为 intra-day price，与close price 可能不同

In no cost world, Full replication produce lowest T.E., but real world there has be a tradeoff between # of constituents and Cost.

- Control Tracking Error by
    - Minimising the trading cost
    - Netting investor cash inflows and redemptions 以减少 cash drag 的影响
    - Using equalisation tools like derivatives to compensate for cash drag 用 cash 去买 derivative 叫 equitisation，减少 cash drag 的影响

### Sources of Return and Risks

1. Attribution Analysis 见后面reading
2. Security lending 借给 short seller
    - The securities lending income can be an additional return, and then reduce T.C. and T.E.
    - 但是 由于借出了stock，会面临 credit risks, mkt risks, liquidity, etc 所以可能要 collateral 去弥补风险
3. Activism and Engagement 
    - Passive Investment 也可以有 积极的股东主义 去 increase return

---

## Active Equity Investing

(1) Fundamental Approach (2) Quantitative Approach

### Fundamental & Quantitative Approach

#### Fundamental Approach

- **Pitfall in Fundamental Investing** (more subjective 更主观)
    1. Behavioural Biases
    2. Value Trap 不能只因为 P/E 低就买，它PE低可能是因为 该公司要完蛋了，人们都在卖
    3. Growth Trap 不能因为 expected growth 高就买，可能 expected growth 虽然高，但是可能不达预期，或者 timing 不合时宜

#### Quantitative Approach

- Quantitative Approach (more objective 更加客观，由algorithm确定，但是 model building phase依然要主观判断参与)

- Investment Process:

    1. Define the market opportunity

    2. Acquire and Process Data

    3. Back-testing the strategy

        - Information Coefficient (IC) 用 信息系数，factor 与未来return的相关性。 衡量 factor 怎么样
            - Pearson IC: $\rho(S_t, R_{t+1})$ , 是factor score 和下一期return 的相关系数corr。 where $S_t$ is the factor score (expected return), and $R_{t+1}$ is the real return at t+1
                - sensitive to outlier 容易受异常值影响，如在算相关系数的时候有一期的数打错了，那么影响会挺大
            - Spearman IC 计算相关系数 corr between factor score 和 forward return 的排序值.
                - 计算的是排序值，所以outlier的影响会被减少

    4. Evaluating the Strategy 用 out of sample data去评价，因为 algorithm 会学习已有的数据

        - Avoid overfitting (overfitting 也叫做 data mining bias )

    5. Portfolio Construction

        - Model Risks: estimation error

            $\sigma^2_y = \beta^2_1\sigma^2_{x_1} + \beta^2_2\sigma^2_{x_2} + 2\beta_1\beta_2cov_{1,2} + \sigma^2_{\epsilon}$ 

            The error of the error term would contribute to the overall risks of model

        - Periodic Optimisation by algorithm may give different weights, rebalancing create costs

- **Pitfall in Quantitative Investing**
    - Selection Bias:
        - Survivorship bias
        - Look-ahead bias
    - Overfitting (data-mining bias)
    - Constraints
        - Constraints on turnover
        - Lack of availability of borrowing / shorting
        - Transaction cost
        - Quant overcrowding (many quants conduct similar strategy 策略用的多了就失效了)

#### Comparison

![Screenshot 2023-11-16 at 13.26.12](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-16%20at%2013.26.12.png)

Quantitative model consider correlation between factors, so it consider risks at portfolio level.

### Active Strategies

#### Bottom-up

##### Value-Based Approach 价值型，关注未来的 div 收益

- **Relative value**: 投 low multiple (P/E, P/B) 即price 低的 为 value investment
- **Contrarian Investing**: Purchasing or selling securities against prevailing market sentiment.
- **High-quality value**: warren buffet 投 intrinsic value 高的 high quality 龙楼
- **Income Investing**: invest high dividend yields or high div growth rate firm
- **Deep-value investing**: focus on low valuation or firms with financial distress 投 multiple 非常低的，面临退市风险的股票
- **Restrucuring and Distressed debt investing**: invest prior to or during an expected bankruptcy filing
- **Special Situation**: M&A, etc

##### Growth-Based Approach 成长型 关注未来的 增长

- Consistent long-term growth 长期增长 
- Short-term earning momentum 短期增长
- GARP (growth at a reasonable price): e.g. P/E-to-growth ($PEG = \frac{P/E}{g}  $)

#### Top-Down

从宏观分析到行业

1. Country / Geography allocation
2. Industry Sector Rotation
3. Thematic Investment Strategies: Focus on opportunities presented by new technologies, changes in regulations, and economic cycles.
4. Volatility-based Strategies: Volatility trading can be conducted through VIX futures, variance swap, option volatility strategy

#### Factor-Based Strategies

- **Rewarded Factors**: factors have **been shown** to be positively associated with a long-term return premium, such as size, value, momentum
- **Unrewarded Factors**: Factors that **have not been empirically proven** to offer a persistent return premium.

##### Hedged Portfolio Approach (Fama & French)

$R = R_f + \beta_i^{mkt} \times (R_{mkt - R_f}) + \beta_i^{size}\times (R_{small} - R_{big})+ \beta_i^{value}(R_{HighBooktoMarket} - R_{lbm})$

- Construction Process
    1. Rank stocks by factors
    2. Divide the list into quantiles
    3. Long best quantile short worst quantile
    4. Track the performance overtime
- Drawbacks
    1. Middle quantiles is ignored
    2. Cannot capture non-linear relationship between factors and stocks (as there is only rank, which is linear)
    3. It's not a **pure** factor portfolio, as there are many other factors not exposed to a single factor
    4. Portfolio is concentrated.
    5. Assume no short limitations

##### Factor-tilting portfolio

Long only. Will expose to a factor. Controlled level of tracking error 因为只expose to a factor

##### Factor-Mimicking Portfolio (FMP)

Implement a pure factor portfolio 找只暴露一种risk factor 的stocks

##### Factor Timing 因子则时

Equity Style Rotation

#### Activist Strategies 积极的股东主义

taking stakes in companies and pushing for companies to make changes that are expected to enhance the value of the activist’s stake. 通过参股，参与公司运营决策，推动公司战略向为股东好的方向走

Target Companies 大原则是经营不太好的公司，这样才有改进的空间

- Slower revenue & earning growth 增长慢的
- Suffer negative share price momentum
- Have weaker-than-average corporate governance

Tactics

- Seeking board representation
- Writing open letters to management
- Proposing changes
- Proposing financial restructuring
- Reducing extravagant management compensation
- Launching legal proceedings
- Launching a media campaign
- Breaking up a large inefficient conglomerate

Ending

- Growth increase
- 为了提升 ROE ，借钱，发debt，leverage提升
- Price 提升，因为empirically activist strategy 确实会带来好的收益

#### Other Strategies

1. Statistical Arbitrage: mean-reverting, exploit pricing inefficiency
    - Market microstructure-based arbitrage strategies (high frequency)
    - Pairs trading (highly correlated stocks)
2. Event Driven

    - M&A
    - Earnings on Restructuring announcements
    - Share buybacks, special div, etc

    Risks: deal fails, deal duration is long, overestimated

### Style Classification 分辨基金经理的投资风格

- Holding Based Approach 

    人工划分 portfolio 中的个体持仓 stock 应该归属于哪个 style ，然后加总看整个portfolio是什么风格

    - look at the attributes of each individual stock in a portfolio
    - aggregates these attributes to conclude the overall style of the portfolio.

- Return-Based Approach 

    拿 portfolio return 跟 各种指数回归，判断受那个 style index 影响大

    - Regress portfolio return On returns of style index

- Self-identification

    - 根据基金经理 self-described 自己的描述，看是什么style的投资风格

---

## Active Equity Investing

### Active Return

- Overweights outperformed securities 多配好股票
- Underweights underperformed securities 少配差股票

$R_A = \sum \Delta W \times R_i$

#### Sources of Active Returns

We all play with **factors** (not stocks) in this part.

By regression,

(1) for the portfolio: $R_p = \beta_0^p + \beta_1^p F_1 + \beta_2^p F_2 +\epsilon_p$

(2) for the benchmark: $R_B = \beta_0^B + \beta_1^B F_1 + \beta_2^B F_2 +\epsilon_B$

(1) - (2): $R_A = \beta_0^p -\beta_0^B + (\beta_1^p-\beta_1^B) F_1 + (\beta_2^p-\beta_2^B) F_2 +\epsilon_p - \epsilon_B$

The intercepts are approximately equal, so we get the 

$R_A =  \sum(\beta_i^p - \beta_i^B) F_i + \epsilon_p - \epsilon_B$

$R_A =  \sum(\beta_i^p - \beta_i^B) F_i +\alpha+\epsilon$

Let $\epsilon_p - \epsilon_b = \alpha + \epsilon$  把 error 拆解为active return & pure error

According to the above function, we decompose it into three parts.

1. Return from factor weighting:

     $R_A = \sum(\beta_i^p - \beta_i^B) F_i $

2. Return from identifying misplacing, Alpha $\alpha$

    - Sustainable 可持续，取决于基金经理的能力

3. Idiosyncratic Return, $\epsilon$ <- luck

    - Un-sustainable 不可持续，为 Luck

- $\alpha , \epsilon$ 都为regression不能解释的部分。不在 R-squared 中

#### Three Building

1. Factor Weighting 多配好的，少配差的

2. Alpha Skills

    1. CME: **factor timing **根据宏观经济择时配置 factors (配置 rewarded factors)
    2. Unrewarded Factors (thematic exposure) 选择了不常规用的factors

3. Sizing Position 权衡购置单一因子的权重 balance confidence in alpha and factors insights

    如控制 factor weighting 与 alpha skill 的权重，体现 level of confidence of analytics

    - A **factor-orientated manager** 主要从weighting获利的投资者，unexplained part $\alpha , \epsilon$ 都比较小 who spreads their portfolio across many assets is likely to minimise the impact of idiosyncratic risk.

        Systematic manager 不做 factor timing

    - A **stock-picker**, with **higher confidence** 更愿意投资个股，所以$\alpha , \epsilon$,对于个股（看好的stock）position的集中度也比较高 in her analysis of individual securities, is likely to hold more concentrated positions and assume a higher degree of idiosyncratic risk.

        所以discretionary managers are likely to run concentrated portfolio

4. Breadth of Experience (BR) 

    $InformationRatio = \frac{R_A}{\sigma_A}$

    $IR = IC\times TC\times \sqrt{BR}$ , and combine those two 

    $\mathbb{E}(R_A)= IR\times \sigma_A = IC\times TC\times \sqrt{BR}\times \sigma_A $

### Portfolio Construction Approaches

![Screenshot 2023-11-17 at 16.05.21](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-17%20at%2016.05.21.png)

#### Relative Risks

Relative risk is measured w.r.t. the benchmark. There are two measures of the benchmark-relative risks.

1. Active Share: $=\frac{1}{2}\sum |w_p - w_b|$ 主动偏离benchmark投资的份额。 	

    - 要除以 2 因为有主动偏离的部分，需要有其他share 让开匀给 active部分，所以要/2

    - **% of portfolio assets deployed the same as benchmark**

        ​	$=1-active\ share$

        ​	即为 一个 portfolio 中，和 benchmark 表现一致的部分

    - Between (0,1)

    - Sources 来源：(1) 与 benchmark 中成分股不同 (2) weights 不同。P.S. 如果 portfolio 中 stocks 数比 index 少很多，那么active share一定会大，因为如果数少，则 concentration 集中度大

2. Active Risks ( Tracking Error )

    - Source of Risks

        Recall: 

        $R_A =  \sum(\beta_i^p - \beta_i^B) F_i + \epsilon_p - \epsilon_B$	

        $R_A =  \underbrace{\sum(\beta_i^p - \beta_i^B) F_i}_{1} +\underbrace{\alpha}_{2}+\underbrace{\epsilon}_{3}$

        收益被拆成了 3 部分（或者说 2 部分，即 1 和 2+3，同理 风险也将被拆成 2 部分

        $\sigma^2_A = \underbrace{\sigma^2\bigg(\sum (\beta_i^p-\beta_i^b)\times F_i\bigg)}_{factor \ exposure} + \underbrace{\sigma^2_e}_{idiosyncratic \ risks}$

        $\sigma_A = \sqrt{\sigma^2\bigg(\sum (\beta_i^p-\beta_i^b)\times F_i\bigg) + {\sigma^2_{\epsilon}} }$

        	1. 与 factor exposure 相关的
        	1. 和与 个股相关的

    - Active Share v.s. Active Risks

        1. The level of active risk will rise with an increase in factor and idiosyncratic volatility 
        2. High net exposure to a risk factor will lead to a high level of active risk, irrespective of the level of idiosyncratic risk 即 weights diff 会提升 $\sigma_A$ active risks
        3. A portfolio with **neutralised factor exposure** will have active risk attributed entirely to Active Share. 因为 factor neutral 所以 factor exposure risk 为 0，idiosyncratic risks 贡献了所有的 active risks
        4. If # of stocks 小，那么 concentration 小， active weights 小，所以 active share 小，active risks 也小
        5. Correlation 会影响 active risks 但是不影响 active share

![Screenshot 2023-11-17 at 17.01.42](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-17%20at%2017.01.42.png)

- Diversified : active share is low, 
- Concentrated: active share is high
- Factor Bets: active risks is high
- Factor Neutral: active risks is low
