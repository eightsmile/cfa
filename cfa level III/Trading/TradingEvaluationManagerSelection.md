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

## Trade Evaluation

### Implementation Shortfall IS 执行落差 显性+隐性

- IS Formulation

  $IS = Execution\ Cost + Opportunity\ Cost + Fees$

- Expanded Implementation Shortfall

  $Expanded \ IS = Delay\ Cost + Trading\ Cost + Opportunity\ Cost+ Fees$

- Delay Cost 决策和下单时间不一样，降低方法：减少时间

- 减少opp costr的方法：Appropriate Order size => minimise the opportunity cost

#### Calculation

- Cost in Dollar per share: $Cost(\$/share) = Side \times (\bar{P}-P^*)$
- Cost in Total Dollar: $Cost(\$) = Side \times (\bar{P}-P^*) \times Shares $
- Cost in Basis Points (bps): $Cost (bps) = Side\times \frac{\bar{P}-P^*}{P^*} \times 10,000bp$
- $P^*$ is the reference price
- $\bar{P}$ is the average execution price

#### Market Adjusted Cost

用于 separate the trading cost from the general market movement 把由于市场price变动带来的trading cost 拆开

$Market-Adjusted\ Cost (bps) = Arrival Cost (bps) - \beta \times Index \ Cost (bps)$

相当于自己的成本比市场贵多少

$Index\ Cost = \frac{Index VWAP - Index\ Arrival Price}{Index\ Arrival Price} \times 10^4bps$

#### Trade Government 交易政策描述

List of Policy, Borning

---

## Performance Evaluation

$Active \ Return \leftrightarrow \alpha$

- Arithmetic Attribution <- Single period (default situation in this part)

  $A = R-B$

- Geometric Attribtuion <- Multi-period

  $(1+G)(1+B)=1+R$

  - G: geometric attribution
  - B: benchmark
  - R: portfolio return

  $G = \frac{1+R}{1+B}-1=\frac{R-B}{1+B} =\frac{A}{1+B}$

### Performance Attribution

1. Return-based attribtuion 

   用 total portfolio return 总收益 来算，有的产品如 hedge funds 不会公布 return 那么 return based attrituion 就不能用

   **Pros:** Easy

   **Cons:** Least accurate

   **Cons:** can be manipulate 因为没有分配到个股，total port容易被操纵

2. Holding-based attribution 会考虑个体持仓，个体的收益率

   **Pros:** more accurate 

   **Cons:** fails to capture the impact of transaction 只考虑了起初期末，期中的交易没考虑到

   也因此，适用于 passive strategy 因为turnover低，适用于短期的，也是因为 turnover 低

3. Transaction-based attribtuon 考虑了 both holdings and transaction

   **Pros:** accurate

   **Cons:** difficult to calculate

### Return Attribtuon

#### Equity

##### Brinson Model 画长方形 asset allocation + securities selection

- BHB Model

  起点是 0

  ![Screenshot 2023-11-29 at 20.50.19](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/202311292050277.png)

- BF Model

  纵坐标起点是 B <- 整个benchmark 的总收益率 P.S. B_i 为各行业的 benchmark return

  ![Screenshot 2023-11-29 at 21.27.20](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/202311292127418.png)

##### Carhart 4 Factor Model

$R_p-R_f = \alpha + \beta_{1}RMRF + \beta_{2}SMB + \beta_{3}HML + \beta_{4}WML + \epsilon$ 

通过回归拆出来，哪个因子对 portfolio return 贡献更大，从而分享组合因为什么因素，带来的收益

- RMRF = the return on a value-weighted equity index in excess of the one-month T-bill rate

- SMB = small minus big, a **size (market-capitalization) factor** (SMB is the average return on three small-cap portfolios minus the average return on three large-cap portfolios)

- HML = high minus low, a **value factor** (HML is the average return on two high-book-to-market portfolios minus the average return on two low-book-to-market portfolios) 

  Fama French 用的是 $\frac{BV}{MV}$ ，相当于一单位的market value 能买到 多少  book value。一般 market value 越接近 BV，则为 价值股。market value 远高于 BV 的为成长股 growth stock

  WML = **winners minus losers**, a **momentum factor** (WML is the return on a portfolio of the past year’s winners minus the return on a portfolio of the past year’s losers)

####   Fixed-Income

1. Exposure Decomposition - Duration Based 使用给clients画饼

   把 gov 和 corporate debt 拆分 Top Down

   按 duration 把债券分为 长中短期

   - Duration Effects
   - Curve Effects

2. Yield Curve Decomposition - Duration Based 适用于分析师

   可 Top-down 可 bottom-up

   $Total Return = Income Return +Price Return$

   $Price Return = - Duration \times \Delta YTM$

3. Yield Curve Decomposition - Full Repricing Based 过程复杂但精确，适用professional

   计算每个时点 sport rate 对价格的影响 

   Bottom-up

#### Return Attribution Analysis at Multiple Levels

- Macro Attribution: determine the impact of the **fund sponsor’s** decisions
- Micro Attribution: determine the impact of the **portfolio managers’** decisions on total fund performance
- 用 BF 模型画矩形，BF模型纵坐标从B开始
