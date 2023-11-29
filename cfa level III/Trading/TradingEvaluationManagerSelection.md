# Trading Evaluation & Manager Selection

## Motivations to Trade

- **Profit Seeking**:

    - Trade Urgency 越urgent to trade，受market impact影响越大，TC越高

    - Alpha Decay, Alpha 随着时间过去会越来越小，所以时间过的越久，alpha 超额收益越少
        - Alpha Decay 越大，即很快 alpha就会 decay到0，那么 trade urgency 越大。

- **Risk Management**: 

    1. Remain at targeted risks level
    2. Hedge risks

- **Cash Flow Needs**: 

    - 避免 cash drag
        - Equalisation: invest cash temporarily to futures and ETFs 
        - 用于避免 cash drag。花一部分钱买 equity futures 股指期货 或者 ETFs 挣收益

- **Corporate Actions** 其他事项

    1. Dividends / coupons
    2. Index tracking
    3. Margin or Collateral calls

### Trading Strategies and Strategy Selection

#### Trade Strategy Inputs 影响价格的因素 作为 inputs

- Order Characteristics:
    - Side: 
        - Demand Liquidity Side: 需要买的，与大多数人一致，demand越多，价格推升越多，T.C.(trading cost) 越大
        - Supply Liquidity Side 可以高价卖，提供流动性，T.C.小
    - Size 绝对交易量
    - Relative Size 自己的交易量占整个security 当天交易量的占比 ADV (average daily volume)
- Market Conditions
    - Liquidity Crises
    - Mkt Volatility
- **Market Impacts and Execution Risks**
    - Market Impact 由于越卖越贵导致的价格提升，带来的T.C.提升
    - Execution Risks 建仓时，由于价格波动带来的建仓成本影响
        - 提升 trade urgency 可以在更短时间内建仓，避免时间长，价格波动带来的成本变化
- Security Characteristics
    - 如 海外equity，Individual Security Liquidity
- User-Based Consideration
    - 个人越厌恶风险，trade urgency 越高（越急着做交易）

#### Reference Pirce

- Pre-trade Benchmark 交易前的 benchmark 适用于 Quant Trader 因为需要有数据做跑模型，只能用此前的数据

    - Decision Price 决策价格，如模型预测的价格
    - Previous Close 收盘价
    - Opening Price 不同于收盘价，不会受overnight price fluc影响，不会受 opening auction 开盘集合竞价影响
        - 适合不参与opening auction ，和不受 overnight price change 影响的人
    - Arrival Price 下单时候的市场价格
        - 适合直接下 market order 的人
        - 适合交易紧急 trade urgency 高的人，因为要立刻执行

- Intraday Trade Price

    - VWAP Volume-weighted Average Price 价格加权

        交易量占比作为权重，与交易价格加权

    - TWAP Time-Wighted Average Price 

        等权重的 算数平均价格

- Post-Trade Benchmark

    - Closing Price
        - Pros: minimise tracking error
        - Cons: only known at the end of trading time 

- Price Target Benchmark  自己定制的

### Trade Implementation Choices  交易平台

- Higher-touch Approaches 人工参与的交易平台
    - Principal Trades 由 人工作为做市商 dealer 参与，做市商即意味着会自己有持仓。dealer挣 bid-ask spread
    - Agency Trades 由 broker 挣佣金 commission fees，撮合交易。因为dealer承担更多风险，所以一般 bid-ask spread更大一点
- Low-touch automated execution strategies 低参与的电子化的平台
    - Alternative Trading Systems ATS (Non-exchange trading venues)
    - DMA Direct Market Access
    - Dark Pools 不会披露交易信息，匿名交易，便于机构投资者 做大笔的交易
- Algorithmic Trading
    - Execution Algorithms 用于执行
    - Profit-seeking Algorithms 通过交易挣超额收益的算法

#### Execution Algorithm 电子化 execution trading 的五个交易方法

1. Scheduled (POV, VWAP, TWAP) 适用小订单，不适用大订单，有可能完不成交易如果illiquid

    - POV (percentage of volume) 如 交易量为市场交易量的1%
        - Pros: take advantage of increase liquidity 因为与市场保持一致
        - Cons: Higher Trading Cost 由于自己与市场一致，所以价格会被推高 ，有T.C.
        - Cons: trade may not be complete 无法保障交易达成
    - VWAP 按交易量 （前一天的交易量分时点给做权重）然后按权重分配到此次交易中，对订单拆分
        - 由于empirically，一个trading day 开始和结束时交易多，所以为VWAP curve 是 U shape
        - Pros: 能 compete the trade
        - Cons: 对于 illiquid stock 还是可能完不成交易
        - Cons: 无法控制 outlayer
    - TWAP 按时间 equal-weighted time schedule

2. Liquidity Seeking 在不同市场中寻找流动性，适合小盘股

    Take advantage of market liquidity **across multiple venues by trading faster** when liquidity exists at a favourable price.

    - Pros: Appropriate for **large order**, coz can execute quickly without substantial impacts
    - Cons: Prices are likely to move unfavourably during the trade horizon

3. Arrival Price

    trade close to current market prices 尽可能按市场价格完成交易

    - Front-loaded strategy 一开始可能快速成交，然后流动性没了，就交易不出去了

    - 适合 Trade Urgency 高的投资者
    - 适合 prices are likely to move unfavourably during the trade horizon 适合着急买，预期价格会变差，所以赶紧交易的投资者

4. Dark Strategies / Illiquidity Aggregators

    - Dark Aggregator Algorithm  适合需要匿名交易
    - Appropriate 适合 for: 
        - 大单 large order size, 
        - illiquid asset with higher ask-bid spread, 
        - no need to execute the order entirely

5. Smart Order Routers (SORs)

    交给algorithm自己算，把所有的单都执行出去

    - 寻求 highest probability of executing, best market price

### Comparison of Markets

交易平台 看 (1) Size (2) liquidity

- 流动性差， Size 高 => 选 high-touch 人工交易
    - Principal (dealer risks 挣 spread 多): Urgency高的在此交易
    - Agency (broker without risks 挣 commission 少) : Urgency低的在此交易，T.C.低

- 流动性好，size 小 => 选 low-touch 电子化平台
    - （5个 algorithm）

- P.S. (on-the-run) Treasury 国债，可以选 Algorithm 交易，因为流动性好

