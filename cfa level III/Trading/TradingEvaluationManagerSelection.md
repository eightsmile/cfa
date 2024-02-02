# Trading Evaluation & Manager Selection

## Trading

### Motivations to Trade 交易的目标 *4

- 1 **Profit Seeking**:
    - Trade Urgency 越urgent to trade，受market impact影响越大，TC越高
    
    - Alpha Decay, Alpha 随着时间过去会越来越小，所以时间过的越久，alpha 超额收益越少
        - Alpha Decay 越大，即很快 alpha就会 decay到0，那么 trade urgency 越大。
    
- 2 **Risk Management**: 
    1. Remain at targeted risks level
    2. Hedge risks
    
- 3 **Cash Flow Needs**: 
    - 避免 cash drag
        - **Equitisation**: invest cash temporarily to futures and ETFs 
        - 用于避免 cash drag。花一部分钱买 equity futures 股指期货 或者 ETFs 挣收益
    
- 4 **Corporate Actions** 其他事项
    1. Dividends / coupons
    2. Index tracking
    3. Margin or Collateral calls

### Trading Strategies and Strategy Selection

### Trade Strategy Inputs 影响价格的因素 作为 inputs

- Order Characteristics:
    - **Side**: 买 or 卖
        - Demand Liquidity Side: 需要买的，与大多数人一致，demand越多，价格推升越多，T.C.(trading cost) 越大
        - Supply Liquidity Side 可以高价卖，提供流动性，T.C.小
    - **Size**: 绝对交易量
    - **Relative Size**: 自己的交易量占整个security 当天交易量的占比 ADV (average daily volume)
- Market Conditions
    - Liquidity Crises
    - Mkt Volatility
- **Market Impacts and Execution Risks**
    - Market Impact 由于越卖越贵导致的价格提升，带来的T.C.提升
    - Execution Risks 建仓时，由于价格波动带来的建仓成本影响
        - **提升 trade urgency 可以在更短时间内建仓**，避免时间长，价格波动带来的成本变化
        
          **Trading with greater urgency results in lower execution risk**
- Security Characteristics
    - 如 海外equity，Individual Security Liquidity
- User-Based Consideration
    - 个人越厌恶风险，trade urgency 越高（越急着做交易）

### Reference Pirce

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
    - **DMA Direct Market Access (for small + liquid trades)**
    - Dark Pools 不会披露交易信息，匿名交易，便于机构投资者 做大笔的交易
- Algorithmic Trading
    - Execution Algorithms 用于执行
    - Profit-seeking Algorithms 通过交易挣超额收益的算法

### Execution Algorithm 电子化 execution trading 的五个交易方法

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240116103026785.png" alt="image-20240116103026785" style="zoom: 67%;" />

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240116103049792.png" alt="image-20240116103049792" style="zoom:67%;" />

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240116103104155.png" alt="image-20240116103104155" style="zoom:67%;" />

1. Scheduled (POV, VWAP, TWAP) 适用小订单，不适用大订单，**有可能完不成交易如果illiquid**

    Scheduled algorithms are appropriate for orders in which **portfolio managers or traders do not have expectations for adverse price movement during the trade horizon**. These algorithms are also used by portfolio managers and traders who have **greater risk tolerance for longer execution time periods** and are more concerned with **minimizing market impact**. Scheduled algorithms are often appropriate **when the order size is relatively smal**l (e.g., no more than 5%–10% of expected volume), the **security is relatively liquid**, or the orders are part of a risk-balanced basket and trading all orders at a similar pace will maintain the risk balance.

    1. POV (percentage of volume) 如 交易量为市场交易量的1%
        - Pros: take advantage of increase liquidity 因为与市场保持一致
        - Cons: Higher Trading Cost 由于自己与市场一致，所以价格会被推高 ，有 T.C.
        - Cons: trade may not be complete 无法保障交易达成
    2. VWAP 按交易量 （前一天的交易量分时点给做权重）然后按权重分配到此次交易中，对订单拆分
        - 有 schedule
        - 由于empirically，一个trading day 开始和结束时交易多，所以为VWAP curve 是 U shape
        - Pros: 能 compete the trade
        - Cons: 对于 illiquid stock 还是可能完不成交易
        - Cons: 无法控制 **outlayer**
    3. TWAP 按时间 equal-weighted time schedule
        - 有 schedule
        - Pros: **exclude outlayers**
        - Text Sample: Portfolio managers may choose TWAP when they wish to **exclude potential trade outliers**. Trade outliers may be **caused by trading a large buy order at the day’s low or a large sell order at the day’s high 价格的过高和过低**. **If market participants are not able to fully participate in these trades, then TWAP may be a more appropriate choice.** The TWAP benchmark is used by portfolio managers and traders to evaluate fair and reasonable trading prices in market environments with high volume uncertainty and for securities that are subject to spikes in trading volume throughout the day.
        - VWAP and TWAP algorithms release orders to the market following a time-specified schedule, trading a predetermined number of shares within the specified time interval (e.g., one day). Following a fixed schedule as VWAP algorithms do, however, may not be optimal for certain stocks because such algorithms may not complete the order in cases where volumes are low. Furthermore, while POV algorithms incorporate real-time volume by following (or chasing) volumes, they may not complete the order within the time period specified.
          TWAP algorithms, which send the same number of shares and the same percentage of the order to be traded in each time period, will help ensure the specified number of shares are executed within the specified time period. Given Bean’s stated priority of complete execution in one day, he is likely to use a TWAP algorithm for the Dynopax sell order.

2. Liquidity Seeking 在不同市场中寻找流动性，适合小盘股，**适合大单交易**

    Take advantage of market liquidity **across multiple venues by trading faster** when liquidity exists at a favourable price.

    - Pros: Appropriate for **large order**, coz can execute quickly without substantial impacts
    - Cons: Prices are likely to move unfavourably during the trade horizon

3. Arrival Price

    trade close to current market prices 尽可能按市场价格完成交易

    - Front-loaded strategy 一开始可能快速成交，然后流动性没了，就交易不出去了

    - 适合 Trade Urgency 高的投资者
    - 适合 prices are likely to move unfavourably during the trade horizon 适合着急买，预期价格会变差，所以赶紧交易的投资者

4. Dark Strategies / Illiquidity Aggregators

    - Dark Aggregator Algorithm  适合需要匿名交易 Dark pools provide anonymity because no pre-trade transparency exists. 不确定性 uncertainty 高
    - Appropriate 适合 for: 
        - 大单 large order size, 
        - **illiquid asset with higher ask-bid spread,** 
        - **no need to execute the order entirely**

5. Smart Order Routers (SORs)

    交给algorithm自己算，把所有的单都执行出去

    - 寻求 highest probability of executing, best market price

### Comparison of Markets 交易方法

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240116120542401.png" alt="image-20240116120542401" style="zoom:67%;" />

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240116120556570.png" alt="image-20240116120556570" style="zoom:67%;" />



<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240103131328037.png" alt="image-20240103131328037" style="zoom:33%;" />



交易平台 先看 (1) Size, 再看 (2) liquidity

- 流动性差， Size 高 => 选 high-touch 人工交易
    - Principal (**dealer** risks 挣 spread 多): **Urgency高 **的在此交易
    - Agency (**broker** without risks 挣 commission 少) : **Urgency低** 的在此交易，T.C.低

- 流动性好，size 小 => 选 low-touch 电子化平台
    - （5个 algorithm）

- P.S. (on-the-run) Treasury 国债，可以选 Algorithm 交易，因为流动性好

- For Fixed Income: low transparency low price discoverying ability, 
    1. Large + urgent => high touch broker
    2. Large + non-urgent => trading algorithms
    3. Small + Liquid => electronic trading


### Trade Evaluation

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240103131841288.png" alt="image-20240103131841288" style="zoom:33%;" />

#### Implementation Shortfall IS （执行落差 显性+隐性） 交易成本拆分

The implementation shortfall (IS) metric7 is the most important ***ex post*** trade cost measurement used in finance.

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240103131940941.png" alt="image-20240103131940941" style="zoom: 67%;" />

- $P_n$ current price
- $P_d$  price at the time of investment decision **(decision price)**
- $P_0$ arrival price

$Implementation\ Shortfall = Paper\ Return - Actual\ Return = Total\ Return$ ，再把 total cost 拆分成 1,2,3三部分

Paper 是 打算买 #1000 share @ \$10，预计能涨价到 $12 , Real Cost 是 实际只买到了 #900 share (#900 = #800@\$10.5 + #100@\$11 其中#800股用\$10.5买到，#100股用\$11买到).

- Total return: 

  - Paper Return = (\$12 - \$10) * #100 = 2000  (paper return 指的是想象中的 return)

  - Actual Return = \$12 * #900 - ( $10.5 * #800 + \$11 * #100 ) **- 50(fees)** = 1250 (real return 指的是实际交易发生的return)

  - Total Cost = Paper Return - Real Return = 750

  - 把 Total Cost 拆分成 1，2，3

    1. execution cost 由于交易的慢了，导致买贵了的cost （即 买到的 900 其中 800@\$10.5 100@\$11 与 理想情况 900@\$10 的差值

       (\$10.5 - \$10 ) * #800 + (\$11 - \$10) * #100

    2. opportunity cost 由于 no being execute 没买到的机会成本 （即有 100 没买到）

       (#1000 - #800 - #100) * (\$12 - $10)

    3. Fee

       50

-  Formulation

  $IS = 1. Execution\ Cost + 2. Opportunity\ Cost + 3. Fees$

- 继续拆分 Further Expanded Implementation Shortfall, **Execution Cost = Delay Cost + Trading Cost**

  $Expanded \ IS = 1.1.Delay\ Cost + 1.2.Trading\ Cost + 2.Opportunity\ Cost+ 3.Fees$

- 把 Total Cost 拆分成 1.1, 1.2，2，3

  1. execution cost 由于交易的慢了，导致买贵了的cost （即 买到的 900 其中 800@\$10.5 100@\$11 与 理想情况 900@\$10 的差值

     (\$10.5 - \$10 ) * #800 + (\$11 - \$10) * #100 = 500

     1. **Delay Cos**t:  arrival price: $P_0$ 注意这里是交易了多少的 # 

        **Delay cost = (Number of shares sold × Arrival price) – (Number of shares sold × Decision price)**

         **= Value of shares sold at arrival price – Value of shares sold decision price**

        (\$10.2 - \$10) * #900 = 180

     2. **Trading Cost**

        **Trading cost = (Total shares sold × Execution price) – (Number of shares sold × Arrival price)**

         **= Value of shares sold at execution price – Value of shares sold at arrival price**

        (\$10.5 - \$10.2 ) * #800 + (\$11 - \$10.2) * #100 = 320

     - 1.1 + 1.2 = 1 = 500

  2. opportunity cost 由于 no being execute 没买到的机会成本 （即有 100 没买到）

     (#1000 - #800 - #100) * (\$12 - $10)

  3. Fee

     50

- Delay Cost 决策和下单时间不一样，降低方法：减少时间

- 减少opp costr的方法：Appropriate Order size => minimise the opportunity cost

#### Trade Cost Measurement :$ \frac{ave - *} {*}$

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240103132041810.png" alt="image-20240103132041810" style="zoom:67%;" />

- \* **Cost in Dollar per share**: $Cost(\$/share) = Side \times (\bar{P}-P^*)$
- \* **Cost in Total Dollar**: $Cost(\$) = Side \times (\bar{P}-P^*) \times Shares $
- \* **Cost in Basis Points (bps)**: $Cost (bps) = Side\times \frac{\bar{P}-P^*}{P^*} \times 10,000bp$
- $P^*$ is the reference price 可以是 arrival price / TWVP / VWAP 等
- $\bar{P}$ is the average execution price

#### Market Adjusted Cost

用于 separate the trading cost from the general market movement 把由于市场price变动带来的trading cost 拆开: Trade cost evaluation calculates **trading costs and performance relative to a specified trading cost or trading performance benchmark**. 自己的交易 将对于 benchmark 交易。Costs are determined by the transaction amount paid above the reference price benchmark for a buy order. The market-adjusted cost calculation involves three steps:

$Market-Adjusted\ Cost (bps) = Arrival Cost (bps) - \beta \times Index \ Cost (bps)$

相当于自己的成本比市场贵多少

$Index\ Cost = \frac{Index VWAP - Index\ Arrival Price}{Index\ Arrival Price} \times 10^4bps$

#### Trade Government 交易政策描述

List of Policy, Borning 确保合规 **procedures are in line with the fiduciary duty**

- Meaning of best execution
- factors determing the optimal order execution approach
- listo f brokers and execution venue
- monitor execution arrangement

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

### Performance Attribution 只管分析 return / risks 的来源，不管分析 investment quality 不管投资好坏

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240126125409951.png" alt="image-20240126125409951" style="zoom:67%;" />

1. **Return-based attribtuion** 

   **Sample Text:**  The returns-based attribution method is most appropriate when the underlying portfolio holdings are not readily available with sufficient frequency at the required level of detail (e.g., hedge funds).

   用 total portfolio return 总收益 来算，有的产品如 hedge funds 不会公布 return 那么 return based attribution 就不能用

   **Pros:** Easy

   **Cons:** Least accurate

   **Cons:** can be manipulate 因为没有分配到个股，total port容易被操纵

2. **Holding-based attribution** 会考虑个体持仓，个体的收益率

   **Sample Text**: The holdings-based attribution method is most appropriate for investment strategies with little turnover (e.g., passive strategies) because it only references the beginning-of-period and end-of-period holdings and ignores individual transactions.

   **Pros:** more accurate 

   **Cons:** fails to capture the impact of transaction 只考虑了起初期末，期中的交易没考虑到

   也因此，适用于 passive strategy 因为turnover低，适用于短期的，也是因为 turnover 低

3. **Transaction-based attribution** 考虑了 both holdings and transaction

   **Sample Text:** The transactions-based attribution method is most effective for active stock selection portfolios because it captures both the holdings and the transactions (purchases/sales) completed within the defined period, which would allow the entire excess return to be quantified and explained.

   **Pros:** accurate

   **Cons:** difficult to calculate

### Return Attribution

#### Equity

##### Brinson Model 画长方形 asset allocation + securities selection

- BHB Model

  起点是 0

  <img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/202311292050277.png" alt="Screenshot 2023-11-29 at 20.50.19" style="zoom:50%;" />

- BF Model

  纵坐标起点是 B, 整个benchmark 的总收益率 P.S. B_i 为各行业的 benchmark return

  $B = \text{total benchmark return}$
  
  $B_i$ portfolio 中不同 component 的 benchmark return
  
  $W_i$ Benchmark weight, 
  
  $w_i$ portfolio component weight
  
  <img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/202311292127418.png" alt="Screenshot 2023-11-29 at 21.27.20" style="zoom:50%;" />

- allocation是sponsor决定的。所以才导致有了题干是单纯的selection，但答案却是S+I的情况。(Sponsor 决定行业配比 **sector weights**，即 allocation)
- 宏观归因把selection和interaction混在一起，宏观归因中，认为**选股和交叉项是由manager**决定的，( FM 在给定 sector weights 后决定 selection, 即sector 内股票的return, **sector return**)
- interaction 给以给 allocation 也可以给 selection， 但是一般会归给 FM 即 selection + interaction

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

### Risk Attribution 风险归因

$Active Risks = \sigma_A = \sqrt{\frac{\sum (R_A^i-\bar{R})^2}{n-1}}$

Type of Attribution Analysis

| Investment Decision Making Process | Relative (vs. Benchmark)                                     | Absolute                                                     |
| ---------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Bottom up 从个体security 看        | Position’s marginal contribution to **tracking risk**        | Position’s marginal contribution to **total risk**           |
| Top down 由行业看到个体            | Attribute **tracking risk** to relative allocation and selection decisions | Factor’s marginal contribution to **total risk and specific risk** |
| Factor based 四因子                | Factor’s marginal contribution to **tracking risk and active specific risk** | Same as the above                                            |

### Benchmarking Investments and Managers

- Asset-Based Benchmark
- Liability-Based Benchmark

#### Property of being a Good Benchmark (SAMURAI)

- Specified in Advanced 事先确定
- Appropriate 能否反应 portfolio style
- Measurable
- Un-ambiguous 权重 weights are clearly identifiable
- Reflective of Current Investment Opinions 让benchmark能够对应portfolio的特征，如积极的投资者，benchmark也要相对积极，且有对应的 factor exposures
- Accountable
- Investable

#### Asset-Based Benchmarks

- **Absolute return benchmarket**

  minimum target return, 比如 hurdle rate

  ​	An absolute return benchmark is a minimum target return that the manager is expected to beat. It will not determine how the manager performed relative to other managers.

  Cons: 问题在于 不能做到 un-ambiguous 因为为指定的rate，没有成分的weights

- **Broad Market Indexes 用大盘指数 做benchmark**

  Cons: 不 appropriate 可能无法反应portfolio的风格

- **Style Index 比较好的选择，可以反映风格**

  Cons: 无法分散化，因为集中于某个 style

- **Factor-Model-Based Benchmark 随便取factors**

  通过回归构建一个模型，作为benchmark

  ​	Factor-model-based benchmarks are constructed by regressing the portfolio’s return against the factors believed to influence returns.

  Cons: not intuitive 无解释效益

  Ambiguous 因为不同模型会有不同结果 ，misspecificed

- **Return-Baed Benchmark 固定有 style factor 作为因子，如 Four Factors**

  Cons: 能反映style，但是不能反映 what they own 持仓

  Cons: 不能反映 style 改变

- **Manger Universe, Manager Peer Group 投资经理们的业绩比较**

  Pros 可以与选定的style的FM比

  ​	A manager universe—or manager peer group—is a broad group of managers **with similar investment disciplines**. Although not a benchmark, per se, a manager universe allows investors to make comparisons with the performance of other managers following similar investment disciplines.

  Cons: survivor bias , cannot be specified in advance, not investable

- Custom 自己定制 benchmark

### Evaluating Benchmark Quality

$P=M+S+A$

B 左边 相当于 与基金经理能录无关

B 右边 相当于基金经理通过自己能力挣的钱

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/202311301659035.png" alt="Screenshot 2023-11-30 at 16.59.35" style="zoom:50%;" />

- P - Portfolio Returns
- M - Market Index Return
- **S - Style Return**
- **A - Active Management Return**
- E = (P-M), difference between the portfolio and the broad market index
- If the benchmark is a broad market index, then $S$ is assume to be zero. Then, $P = M+A$

If 一个benchmark好，要能把A、S区分开。那么 A 与 S 的相关性要低, $\rho(A,S)=0$。因为 A 为基金经理的能力， S 不为能力

If 一个benchmark好，$\rho(S,E) = \rho(S,S+A) $ 高，这个相关系数高与上式一致，意味着 S & A的相关性低$\rho(A,S)=0$，则$\rho(S,E) = \rho(S,S+A) $ 高

### Benchmark for Alternatives Investment

Rationale

- 因为 Alternative 的 Liquidity 低， 所以用 Appraisal 价格评估，

  We smooth the data, 这样会导致 sigma 数据的方差或标准差被低估，会导致 diversification 分散度被高估

- 因为没有要求披露业绩，是自愿披露的 Self-Reported，那么会有 

  1. survivorship bias 愿意披露的恰好是表现好的
  2. Backfill Bias 高业绩的会被包含进来

- 因为 Leverage 大，所以收益率高。此时用有杠杆的和无杠杆的 port & benchmark 比，是不可比的

### Performance Appraisal 用来分析FM水平

- Sharpe Ratio

  $Sharpe = \frac{\bar{R_A}-\bar{r_f}}{\hat{\sigma_A}}$

  Risk -> excess return

  Cons: Risks have upside and downside, only downside vol worries

  无法解决 非正态分布的问题

- Treynor Ratio

  $Treynor = \frac{\bar{R_A}-\bar{r_f}}{\hat{\beta_A}}$

  Beta represents the **systematic risk**, so excess retrun per unit of systematic risks

- Infomration Ratio

  $IR = \frac{R_A}{\sigma_A} = \frac{R_p-R_b}{\sigma{(R_p-R_b)}}$

  Active return per unit of active risk

- Appraisal Ratio (AR)

  $AR = \frac{\alpha}{\sigma_{\epsilon}}$

  $R_p - R_f = \alpha + \beta (R_m-R_f)+\epsilon$ CAPM regression

  , where $\alpha$ is the abnormal return, and $\sigma_{\epsilon}$ is the s.d. of error term

  $\alpha = R_p - CAPM\ Return$ <- Jensen's Alpha

  $\sigma_p^2 = \beta^2\sigma_m^2 + \sigma_{\epsilon}^2$

  $\sigma_{\epsilon}= \sqrt{\sigma_p^2 - \beta^2\sigma_m^2 + }$

  abnormal return per unit of abonormal risks (as the return is portfolio return in excess of CAPM, the market), so what left with is the unsystematic return

  So, the ratio measure, excess reutrn per unit of unsystematic returns

- Sortino Ratio

  $Sor R = \frac{R_p - MAR}{\sigma_{Downside}}$​

  1. Downside var
  2. investor-specific preference, use MAR not rf

  - $MAR$ is the minimum required return, e.g. hurdle rate

  - The semi-standard deviation : $\sigma_D = \sqrt{\frac{\sum min(r_t-r_T,0)}{N}}$ 目标半方差 ，只考虑 downside risks

    <img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/202311301901297.png" alt="Screenshot 2023-11-30 at 19.01.05" style="zoom:50%;" />

    Excess return w.r.t. Target, per unit of downside return 
    
    **The Sortino ratio penalizes a manager when portfolio return is less than the MAR (minimum acceptable return) and thus is preferred when the investor’s goal is to preserve capital.** The Sortino ratio penalizes a manager when portfolio return is less than the MAR (minimum acceptable return) and thus is preferred when the investor’s goal is to preserve capital.

- **Capture Ratio**

  $CR = \frac{UC}{DC}$

  用compound return算 Rb or Rp, $1+ R_b = \sqrt[3]{ (1+R_1)(1+R_2)(1+R_3)}$

  - $UpsideCapture = \frac{R_p}{R_b}$ benchmark上涨1，portfolio上涨的比率为UC，UC大于一好

  - $DownsideCapture = \frac{R_p}{R_b}$ benchmark下跌1，portfolio下跌的比率为DC，DC小于一好

  - 综上 CR 越大越好

  - CR > 1 : positive asymmetric, convex 涨多跌少，为convex

  - CR < 1 : negative asymmetric, concave 

    <img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-12-01%20at%2013.28.23.png" alt="Screenshot 2023-12-01 at 13.28.23" style="zoom:50%;" />

- Drawdown: cumulative peak-to-trough loss **during a continuous period**

- Drawdown Duration 从peak最高点跌下来，再回到peak的时间  **strat of the drawdown** until the cumulative drawdown **recovers to zero**.

---

## Manager Selection Process

Insert 1

### Manager Universe 先确定可选的范围

所有 feasible manager 可选的基金经理

The manager universe 提前根据 **IPS** filter了符合的 

1. suitability
2.  style, 
3. passive/active suitable

### Type I & Type II Error of Manager Selection

特别扯淡part Type I and Type II errors in manager selection

- Null Hypothesis: the manager is not skillful 基金经理skill=0

- Type I: 去真，reject the null when it is true。FM是垃圾，但是还是雇了他（reject the true null） **(error of commission 雇了个sb)**
- Type II: 纳伪，accept the null when it is false。FM nb 但是没雇 **(error of omission 错过了人才**)
- Decision Makers worry more about Type I errors than Type II errors. coz
    1. 请神容易送神难，雇sb往往会更糟
    2. Psychologically, people seek to avoid feelings of regret 因为 type I 是做错了， type ii 是错过了。人们容易忽略错过了，而放大做错的
    3. Type I errors are straightforward to measure 因为与雇员业绩相关，共容易观测
    4. Type I errors liked to decision makers' compensation 与雇人相关，会给工资的
- **efficient market** exihibts **smaller differences** in skilled and unskilled manager 有效市场情况下，skilled 和 unskilled 的差距少，因为alpha 少
- 影响 expected cost的因素，size, shape, mean, dispersion, etc. 
    - 如 skilled & un-skilled FM 的 mean 差距小, dispersion 大（方差大），则cost的差距小
- 市场越有效，超额收益越少，opportunity cost of hiring a unskilled FM 越小
- In deciding which fund to hire, the **goal is to avoid making decisions based on short-term performance** (trend following) and to **identify evidence of behavioral biases** in the evaluation of managers during the selection process.
- **Psychologically, people seek to avoid feelings of regret.** Type I errors are errors of commission, active decisions that turn out to be incorrect, whereas Type II errors are errors of omission, or inaction. **Type I errors create explicit costs, whereas Type II errors create opportunity costs.** Because individuals appear to put less weight on opportunity costs, **Type I errors are psycho­logically more painful than Type II errors.**
- **Type I errors are more transparent to investors, so they entail not only the regret of an incorrect decision but the pain of having to explain this decision to the investor.** Type II errors, such as firing (or not hiring) a manager with skill, are less transparent to investors—unless the investor tracks fired managers or evaluates the universe themselves.
-  突然说因为 Type I error 更显性 explicit，更透明 transparent，同同时 Behaviourally, people seek to avoid the feelings of regret 所有 Type I error 跟被重视。而 Type II error is about the opportunity cost, which is less tranparent unless they evaluate un-hired FM. 所以经常被忽视

### Quantitative

##### Style analysis 时刻关注是否FM的投资style 有变化

- Returns-Based Style Analysis (RBSA) 回归 Top-Down，用 style factor做 **regression** ，比较基金的收益和 那个style factor  的beta 大，那么port就是哪个style
    - Pros: 可以纵向比较，看FM不同时间的style。
    - Pros: require less efforts to acquire data 尽管需要跑回归，但是由于进入时间序列数据比较好获取，所有数据好收集
    - **Not subject to window dressing 不受持仓的影响，因为不看持仓**
    - Cons: **对于 illiquid securities， 由于样本量小，return data is fluent 被平滑,** may understate the risks exposure
    - Cons: 不精确 因为没看持仓
- Holding-based style analysis (HBSA)
    - Bottom up 选某个时点的weights
        - Cons: s.t. window dressing 受制于粉饰，

##### Capture Ratio 见此前提到 UC/DC

- help assess manager **suitability relative** to the investors' IPS
- can evaluate the **consistency** between the stated and reported investment portfolio

##### Drawdown 见此前提到 

**Stress-test** of the investment process **when princple-agent conflicts arise**

### Quality 

#### Investment Due Diligence

- Philosophy 投资理念
    - Passive Strategy seek to capture return from systematic risk premium
    - Active Strategy seek return from misplacing. The **inefficiency is from (1) behavioural and (2) structural**
    - Style Drift: 与投资决策过程不一致
- Investment Personnel: Process, People, Portfolio 投资团队为people
- Investment Decision MakeingProcess:
    - Signal Creation 市场产生信号，产生观点 (idea generation): unique, timely, interpreted differently
    - Signal Capture 落实观点 (idea implimentation)
    - Portfolio Construction 建仓
    - Portfolio Monitor 后期

#### Operational DD 定性分析公司**运营、治理情况**，制度等

- Process and Procedure 制度是否完善
- Firm & terms 企业文化 条款条例等
- Investment vehicle 
    - (1) individual separate account SMA 可以定制的，自己玩的 
        - Owner 归客户
        - 可 customised
        - tax efficiency 可以做税务筹划
        
          **investors who is focused on tax efficiency would prefer a separately managed account** because a separate account allows the implementation of tax-efficient investing and trading strategies
        - transparency  账户情况可以给client公开
        - Cons: cost 贵因为客制化，tracking risk高因为客制化，
    - (2) pooled vehicles 大家一起玩
    - Liquidity: ETFs, closed-end fund 流动性好，因为有二级市场可以赎回（open-end fund 只能找 FM 赎回，所有流动性差）
    
        - ETFs Close-end > Open-end > LP & PE
        - **Limited partnerships and private equity funds typically require investors to invest their money for longer periods.**
    
    Insert 2
- Management Team 管理，比 个人管理Fund好，因为 key person risk降低

#### Management Fee

- AUM Fee = $AUM \times \%$

- Performance-based Fees (**maximum and high-water mark,** or **clawback**)

    1. A **symmetrical structure** in which the manager is fully exposed to both the downside and upside (Computed fee = Base + Sharing of performance);
    
        利润profit为正，收fee，为负扣钱

    2. A **bonus structure in which the manager is not fully exposed to the downside but is fully exposed to the upside** [Computed fee = Higher of either (1) Base or (2) Base plus sharing of positive performance]; or
    
       挣钱有奖励，亏了不罚钱。有可能导致 FM **has the greatest incentive to assume additional risk to earn a higher investment management fee**  因为挣得多了给incentive多，亏了也不亏incentive。不像3，如果亏了则亏管理费
    
    3.  **bonus structure in which the manager is not fully exposed to either the downside or the upside** [Computed fee = Higher of (1) Base or (2) Base plus sharing of performance, to a limit].
    
       上下两端都有limit，亏有限，奖有限
    
    - 看题目思考分析，没有固定的收费标准，因为每个公司都不一样
    
- Three basic ways of performance-based fees

    - symmetrical structure: conputed fee = base + sharing of performance
    - bonus 看题说话

- Other Considerations

**Performance-based fee structures** convert symmetrical gross active return distributions into asymmetrical net active return distributions, reducing variability on the upside but not the downside. As a result, a single standard deviation calculated on a return series that incorporates active returns, above and below the base fee, can lead to the underestimation of downside risk. In contrast, fully symmetric fees (fully exposing the manager to both upside and downside results) tend to yield closer alignment in risk and effort than bonus-style fees.



一般来说 performance fee 高，意味着 Higher active investment

- Sample Text: about fee & volatility

  Which of the following fee structures *most likely* decreases the volatility of a portfolio’s net returns?

  Incentive fees are fees charged as a percentage of returns (reducing net gains in positive months and reducing net losses in negative months), its use lowers the standard deviation of realized returns. Charging a management fee (a fixed percentage based on assets) lowers the level of realized return without affecting the standard deviation of the return series. Incentive fee 利润高的时候收到高，低的时候收的低，所以 decrease volatility

  Management fee 相当于减去固定的值（常数），方差不变

- **Sharing based on active return / based on return net of base fee**

  如果基于 active return,  则 用( port return - benchmarket ) * sharing %

  如果基于 base fee， 则用 (port return - base fee) * sharing %
