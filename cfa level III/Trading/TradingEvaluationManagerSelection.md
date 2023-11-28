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

### Trade Implementation Choices 

交易平台选择

51min