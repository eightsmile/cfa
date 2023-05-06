## Portfolio

### ETFs

Investors -> AP -> Portfolio Managers

在US：投资者 只能找AP买二级ETF。 只有AP可以一级create / redemption ETF 通过拿 a basket of stocks 换

ETF intraday trading cost > arbitrage cost, then AP can create new ETF shares to earn the profits.

#### Expense Ratios

- Rolling Return Assessment - Tracking Difference. Allows for comparison with other annual metrics such as fund's expense ratio. 因为ETF的标的是benchmark，ETF performance是他是否与Benchmark return表现一致。所以 **Rolling Return Assessment reflects the impact of portfolio rebalancing expenses and other fees**.
- ETF's Expense ratio does not reflect the cost of portfolio rebalancing or other fees.

#### Tracking Error

- Annualised Standard Deviation of daily ( ETF returns - Benchmark Returns )

It does not reveal whether the fund is over/under-performed, or whether that tracking error is concentrated over a few days.

**Sources of Tracking Error**: 

- Fees and Expenses 大 - 会导致rolling return assessment变大
- Representative sampling/optimisation 大 - 会导致rolling return assessment变大
- Index Changes 当权重变的时候产生，但是会立刻调整 小 - 因为ETF is daily adjusted

#### Capital Gain Distribution

The issue of **capital gains distributions affects all investors** in taxable accounts. ETFs are said to be “tax fair” and “tax efficient” because they have certain advantages over traditional mutual funds regarding capital gains distributions. On average, they **distribute less in capital gains than competing mutual funds**.

**Reasoning**:

- In a **traditional mutual fund**, when an investor sells, the fund must (with a few exceptions) sell portfolio securities to raise cash to pay the investor. **Any securities sold at a profit incur a capital gains charge, which is distributed to remaining shareholders**.
- In contrast, an investor sells ETF shares to another investor in the secondary market.  - No Tax. If an AP redeems ETF shares, redemptions do not trigger capital gain realizations. - No Tax
- When an AP submits shares of an ETF for redemption, the ETF manager can choose which underlying share lots to deliver in the redemption basket. By choosing shares with the largest unrealized capital gains—that is, those acquired at the lowest cost basis—ETF managers reduce potential capital gains in the fund. 

#### Trading Costs + Management Fee

Round-Trip Trading Cost (%) = One-way Commission * 2 + 1/2 Bid-Ask Spread * 2

Total Fees = Round-Trip Trading Cost + % * Management Fees = One-way Commission * 2 + Bid-ask Spread + % * Management fee

#### ETF Dividends

"Although exchange traded funds (ETFs) are primarily associated with index-tracking and growth investing, there are many that offer income by owning dividend-paying stocks. When they do, they collect the regular dividend payments and then distribute them to the ETF shareholders. These dividends can be distributed **in two ways** at the discretion of the fund's management: **cash paid to the investors** or **reinvestments into the ETFs' underlying investments**."

#### ETF Risks

**Fund-closure risk** is the risk that an ETF may shut down. The reasons that lead to an ETF closing down often have to do with **changes in regulations, increased competition, and corporate activity** (merger and acquisition activity within the ETF industry).

#### Smart Beta

**Factor strategy ETFs** are usually benchmarked to an index created with predefined rules for screening and/or weighting stock holdings and are considered **longer-term, buy-and-hold investment** options **rather than tactical trading instruments**.

### Multi-factor Model

$$r = \beta_0+\beta_1x_1x+\beta_2x_2+...+\beta_kx_k$$

- $\beta_0$ is the expected return, mean return. The **Expected Return** is the **Intercept**.
- Compare each factors with the benchmark

#### Between Fundamental Model & Macro-Factor Model

A second distinction between macroeconomic multi-factor models and fundamental factor models is that with the former, we develop the factor (**surprise**) series first and then estimate the factor sensitivities through regressions. With the latter, we generally specify the factor sensitivities (attributes) first and then estimate the factor through regressions.

- Macro Model - 1st calculate surprise 2nd calculate sensitivity.
    - Use **Surprise** as Factors.
- Fundamental Model - 1st calculate sensitivity
    - book-value-to-price ratio, market capitalisation, the price-to-earnings ratio, and financial leverage.

#### Statistical Model

In a statistical factor model, statistical methods are applied to historical returns of a group of securities to extract factors that can explain the observed returns of securities in the group. In statistical factor models, the factors are actually portfolios of the securities in the group under study and are therefore defined by portfolio weights.

- An advantage of statistical factor models is that they make minimal assumptions. 
- However, the interpretation of statistical factors is generally more difficult than the interpretation of macroeconomic and fundamental factor models.

#### Information Ratio

$$IR = \frac{R_p - R_B}{\sigma_{R_p - R_B}} = \frac{Avtive Return}{TrackingError}$$

#### Three Types

- Macro  - Factors are **Surprise** .Consider Last
- Fundamental - Consider Firstly
- Statistics - Explain Historical Return Covariance

### VaR

- Parametric  <- Assume the distribution (normal), $\mu$, $\sigma$.
- Historical
- Monte Carlo - Advantages:
    -  can also more easily accommodate the large number of portfolio holdings. 
    - allows the user to develop her own forward-looking assumptions about the portfolio’s risk and return characteristics.

Drawbacks: Do not consider the Liquidity, and thus VaR could underestimate the risks.

Expected Shortfall: **Conditional VaR** is defined as the weighted average of all loss outcomes in the return distribution that exceed the VaR loss. 

### Economics and Investment Market

- In recession, yield curve would be downward sloping.

- **Output Gap**: An economy operating with a **positive output gap**—that is, where the level of actual GDP exceeds potential GDP—is producing beyond its sustainable capacity. 

    - **Positive output gaps** are usually associated with high and/or rising inflation  经济好，actual output大，positive gap，高增长伴随高通胀

    - , while high levels of unemployment usually accompany **negative output gaps**. 经济不好，negative gap 高失业

#### PV Model

$$ P = \sum \frac{CF_i}{(1+r)^i}$$

- $r = R + \pi + RP$, where there are 
  - (1) default free interest rate
  - (2) expected inflation
  - (3) **risk premium**

#### Inter-temporal Rate of Substitution

- $ m = \frac{MU_{1}}{MU_0}$, there are each marginal utility of consumption in time 0 or 1
  - Marginal Utility of Consumption at t=0 (current time) is normally larger than at t=1 (in the future), thus $m<1$.
  - Intuitively, $m$ describe people's desire. If people desire more on current, then current is more attractive, then MU0 is greater than MU1.
  - E.G. In “good” economic condition, individuals may have relatively high levels of current income so that current consumption is high. In this case, the **utility** derived from **an additional unit of consumption** today will be relatively low. 
  - E.G. If $m$ is low. If bond price currently is too high, then less are affordable to people, so people invest less by buying bonds for future. They not invest future, and they consume more today, so MU0 decrease, and $m$ gradually increase.
- Real Risk Free Rate, $1+R = \frac{1}{m} $. There higher the GDP growth, the higher $R$ - **One-period Real Interest Rate**.
    - $Nominal\  GDP\ Growth = Inflation+RealGrowth$
    - $R_f / Rate = Inflation + RealInterestRate$


#### Normal Risk-free Interest Rate $r$

Inflation = Expected Inflation $\pi$ + Risk Premium for Uncertainty, $\theta$

$$r_{long} = R +\pi + \theta$$

$$r_{short} = R +\pi $$

短期，不考虑uncertainty $\theta$， 因为 uncertainty is not realised，但是长期需要考虑

#### Two Key Points

- **Economic Growth** $\uparrow$, then **Credit Spread**  narrow $\downarrow$
- Valuation Ratios $\uparrow$, coz price increase.
- Stylised Factors, small-cap outperform
    -  When **spreads are narrowing**, investors seem to be **less sensitive** between issues with weak versus strong credit, and the rate of improvement will tend to be greater for those bonds issued by entities with a relatively weaker ability to pay. Thus, **during times when corporate bond spreads are narrowing relative to government bonds and the spreads between higher- and lower-rated bond categories are also narrowing**, corporate bonds will generally **outperform** government bonds and lower-rated corporate bonds will tend to **outperform** higher-rated corporate bonds.

- The **sensitivity** of a **corporate bond’s spread** to changes in the business cycle and the level of cyclicality tend to be **positively** correlated. **The greater the level of cyclicality, the greater the sensitivity of the bond’s spread to changes in the business cycle.** 这里cyclicality指的是周期性，周期性越强的行业，spread越大

#### Risk-covariance

$P_t = E(P_{t+1}\times m)=E(P_{t+1})E(m) + cov(P_{t+1},m)$

$1+R = \frac{1}{m}$, so $m=\frac{1}{1+R}$, so $P_t=\frac{E(P_{t+1})}{1+R} + cov(P_{t+1},m)$

**PV = Discounted FV + Cov(FV, intertemporal Substitution)**

- In general with **risk-averse investors**, the covariance term for most risky assets is expected to be negative. That is, when the expected future price of the investment is high, the marginal utility of future consumption relative to that of current consumption is low.
- Note that with a one-period default-free bond, the covariance term is zero because the future price is a known constant ($1) and the **covariance of a random quantity with a constant is zero**; and intuitively, its value is given by the first term.

#### GDP Growth and Interest Rate

Real Risk Free Ratee, $1+R = \frac{1}{m} $. There higher the GDP growth, the higher $R$ - **One-period Real Interest Rate**.

Pay more attention to the **intuition of intertemporal substitution**. 

- Assume GDP growth $\uparrow$. If desire more on current, then demand for future is less (invest in bond for future is less). So bond price is low, the return of saving/investing $R$ is high. Mathematically, if MU0 is larger, $m$ then is lower, $1+R = \frac{1}{m} \uparrow$, so the real default-free interest rate increase.

Similarly, if volatility of GDP growth $\uparrow$, then desire of consume 

#### BEI 

BEI = zero coupon **Nominal** Bond  -  zero coupon **Real** Bond = $\pi$ + $\theta$, equals to the sum of expected inflation + volatility of inflation (the premium of uncertainty of inflation).

Break-even inflation rate (BEI), $BEI = r_{non-inflation Index} - r_{inflation-indexed}$, then what left with is the inflation.

The **break-even inflation** rate is the difference between the yield on **(1)** a zero-coupon, default-free **nominal** bond and on **(2)** a zero-coupon, default-free **real** bond of the same maturity.

都是 zero-coupon + default free ，但是 real 和 nominal不同

#### Upward-sloping, default-free government bond nominal yield curve.

The yield curve is determined by two factors: **expected rate + risk premium**

#### Consumption Outcomes

Equity investors will demand an equity risk premium if the consumption hedging properties of equities are poor—that is, if equities tend not to pay off in bad times. 

An upward sloping curve would be associated with bond risk premiums that are positively, not negatively, related to the consumption hedging benefits of government bonds.

#### Business Cycle

Short-term nominal interest rates will be positively related to short-term real interest rates and to short-term inflation expectations. 

Other things being equal, we would also expect these interest rates to be higher in economies with higher, more volatile growth and with higher average levels of inflation over time.

**Consumer Discretionary** is in the heavy Business Cyclical Industry. Because the consumer discretionary sector is closely tied to consumer spending, it relies heavily on business cycles and economic conditions, which makes it a cyclical sector.

### Notes

1. Real interest rates are high when the **expected consumption growth** is high (intertemporal substitution) or when risk is low (precautionary saving).
2. During **good economic times**, current consumption is high since individuals have relatively high current income. This makes the **marginal utility of consumption low today**.
3. As **wealth increases**, investors’ **marginal utility of consumption declines since they have already satisfied their basic needs.** Investors would, therefore, benefit more from an asset that pays off more in bad economic times relative to one that pays off in good economic times.
4. A risk-averse individual is one who demands compensation for uncertainty. An investor’s **absolute risk aversion decreases with an increase in wealth or income.** In particular, an investor **invests more in risky assets as their wealth or income increases**. This decreases the marginal utility of holding risky assets.
5. The **risk premium is lower for wealthier individuals**, which implies that wealthier individuals are more willing to bear a given risk relative to more indigent individuals. However, when the markets are at equilibrium, all investors, regardless of whether they are wealthy or poor, have the same willingness to hold risky assets.
6. **GDP growth forecast is usually high** since we expect more goods in the future than today. **An increase in real GDP growth leads to an increase in the real default-free interest rate**. Consequently, investors’ willingness to substitute across time **falls**. Subsequently, there will be less saving and more borrowing. The end result of all these is an increment in the real default-free rate of interest.
7. Remember, however, that it is not easy to correctly predict GDP growth from one period to another. Under these uncertainties, the interest rates are positively related to the expected GDP growth rate, as well as the expected volatility of GDP growth.
8. In conclusion, we **expect a higher average level of real short-term interest rate in an economy with high and volatile growth, all else being equal**. The converse is also true. We can deduce that **due to a higher risk premium, the real short-term interest rate is positively correlated with the volatility in GDP growth.**

### Analysis of Active Portfolio Management

#### Active Return (Value Added) & Alpha

**Alpha Return** and **Alpha** are not the same.

- $R_A = R_p - R_B$
- $\alpha = R_p - w\times R_B$

#### Active Weights

$$\Delta w_i = w_{p,i} - w_{B,i}$$

- The sum of those $\sum \Delta w =0$
- Active Return / Value Added, $R_A = \sum \Delta w_i \times (R_i-R_B)$
- Benchmark Weights / Allocation - Strategic Allocation
- (Sub-) portfolio allocation - Active Allocation

Decompose the **Value Added \ Active Return**, there would be:

- (1) **Value Added from Security Selection** $w_A(R_{sub-portfolio} - R_B)$, 用**Active weights**, and 
- (2) **Value Added from Asset Allocation** $(w_A - w_B)R_B$.

#### Sharpe Ratio is Unaffected by Leverage

$$SR = \frac{R_a-R_f}{\sigma_a}=\frac{c(R_a-R_f)}{c\sigma_a}$$

SR is **unaffected by cash**. CML slope，怎么延长斜率都不变。所以如果portfolio中有cash的话，用SR评估对比，会不准。

#### Information Ratio - aggressiveness of active weights

Active Return relative to a benchmark with volatiltiy of the active reutrn.

$$IR = \frac{R_p - R_B}{\sigma_{R_p - R_B}}=\frac{R_A}{\sigma_A}=\frac{ActiveReturn}{ActiveRisks}$$

- **Affected** by leveraging cash，因为cash多了，active management就少了，所以受cash比例影响
- **Unaffected** by Aggressiveness of the active weights
    - The information ratio is **unaffected** by the **aggressiveness of the active weights (deviations from benchmark weights**) because both the active return and the active risk increase proportionally. $cR_A/c\sigma_A$

$$SR_p^2 = SR_B^2+IR^2$$

While the Sharpe ratio measures reward per unit of risk in ***absolute*** returns, the information ratio measures reward per unit of risk in *benchmark **relative*** returns.

#### Closet Return / Closet Portfolio

- Sharpe ratio is close to the Benchmark
- Active Risk is low
- Information ratio = ActiveReturn / ActiveRisks can be indeterminate, it's often negative due to management fees. IC is in-determined, because 分子分母可以抵消。 

### Fundamental Law of Active Management

- **IC**: Information Coefficient: about **Forecasting** returns: $IC = Corr(\frac{R_A}{\sigma_i},\frac{\mu_i}{\sigma_i})$ -  represents the extent to which the portfolio manager’s expectations are realised. (**Risk-adjusted active return**, corr to **Risk-ajusted Anticipated Return**). **多少anticipated return能实现为active return。**
- **TC**: Transfer Coefficient in **portfolio construction**: $TC = Corr(\frac{\mu_i}{\sigma_i},\Delta w_i\sigma_i)$ -  how well the anticipated (*ex ante*), risk-adjusted returns correlate with the risk-adjusted active weights. 多少**anticipated return**能转换成active **weight**。
- **BR**: Breath <- 独立的 个数，独立的次数（如monthly）。要求一定要是独立的，否则**overestimate** the BR. （assets之间互相corr 会降低有效的 "独立个数" 导致overestimate）。
- $IR = TC\times IC\times \sqrt{BR}$
- $\mathbb{E}(R_A) = TC\times IC\times \sqrt{BR}\times \sigma_A$

Value Added is decomposed by four elements: $\mathbb{E}(R_A) = TC\times IC\times \sqrt{BR}\times \sigma_A$

- **IC - Skill / Forecast**
- **TC - Portfolio Construction** - 代表 investment constraint
    - A low TC results from the formal or informal constraints imposed on the structure of the portfolio. In fact, at TC = 0.00, there would be no correspondence between the **active return forecasts** and **active weights taken** and thus no expectation of value added from active management. In contrast, TC = 1.00 (no binding constraints) represents a **perfect correspondence between active weights taken and forecasted active returns**. 预测了就能实现，代表 less constraint

- **Breadth - number of independent decisions per year**
    - **Constraints**: an investment policy might not allow for short positions. Similarly, some securities are correlated with each other (such as all bonds being subject to duration risk), and thus **breadth is considerably less than the number of securities held in the portfolio.** **Breadth** is **overestimated** than truly the manager did.
    - 原则：有constraint的，能灵活支配的stocks少，所以breadth小，跟unconstraint的比。
- **Aggressiveness** - benchmark tracking risk / sigma

#### Constructing Optimal Portfolio

$$SR_p^2 = SR^2_B + IR^2$$

The above equation implies that the **active portfolio with the highest (squared) information ratio** will also have the **highest (squared) Sharpe ratio.** 

For unconstrained portfolios, the level of active risk that leads to the optimal result,

$$\sigma_{R_A} = \frac{IR}{SR_B}\sigma_{B}$$

$$\frac{R_B-r_f}{\sigma^2_B}=\frac{SR}{\sigma_B} = \frac{IR}{\sigma_A}=\frac{R_A}{\sigma^2_A}$$

### Trading Cost 记得*2

$$\text{Effective Bid-ask Spread}=2 \times \bigg(Trade price − \frac{Ask price + Bid price}{2}\bigg) $$

$$\text{Effective Bid-ask Spread}=2 \times \bigg(Trade price − MidPrice\bigg) $$

- Average Effective Spread 直接 加起来/n 不用加权重平均
- Volume-weighted average effective spread 按交易量加权平均

#### True Transaction Cost

##### Disadvantage of Effective Spread: 

Effective spread transaction cost estimates are not well suited to measure the true transaction cost when an order is filled over several trades and there are market impact and delay costs. 

当多笔交易时，effective spread不精准

1. The effective spread is a poor estimate of transaction costs when traders split large orders into many parts to fill over time. Such orders often move the market and cause bid and ask prices to rise or fall. The impact of the order on market prices, called **market impact**, makes trading expensive—especially for the last parts to fill—but the effective spread will not fully identify this cost if it is computed separately for each trade. 因为买的太多带来对market price的影响（也叫market impact）并不能被 effective spread 解释。
2. Effective spreads also do not measure **delay costs**(also called **slippage**) that arise from the inability to complete the desired trade immediately because of its size in relation to the available market liquidity. 另一个cons是effective spread不能解释delay，来自交易量过大，使市场不能消化造成的

##### Disadvantage of volume-weighted average price (VWAP) 

与effective spread一样，不能解释

VWAP transaction cost estimates are not well suited to measure the true transaction cost when an order is filled over several trades and there are market impact and delay costs. The VWAP method of estimating transaction costs compares average fill prices to average market prices during a period surrounding the trade. It tends to produce **lower transaction cost estimates than does implementation shortfall** because it often does not measure the **market impact** of an order well. 

##### Advantage of Implementation Shortfall

Implementation Shortfall 好，因为算了隐性和显形的成本。考虑了 (1)  market impact cost (2) delay cost (3) opportunity cost

The implementation shortfall method of measuring trading costs addresses the problems associated with the effective spread method. Implementation shortfall is also attractive because it views trading from an investment management perspective and measures the total cost of implementing an investment decision by **capturing all explicit and implicit costs**. The implementation shortfall method **includes the market impact costs and delay costs as well as opportunity costs**, which are often significant for large orders.

### Market Fragmentation

**Increases** the potential for price and liquidity **disparities across venues** because buyers and sellers often are not in the same venues at the same time.

#### Players and Notations

- Electronic Front Runner - low-latency trader who use AI to identify orders and trades. 抢在大订单前先下单（可能是内幕消息，可能是AI算出来的），需要系统low latency
    - Break Orders into Pieces
    - 要应对front runner 可以拆小单
- Electronic Arbitrageurs - look for across-market arbitrage opportunity.
- Electronic Dealer - 通过 round trips 的bid ask spread来获利
- Electronic news traders - high-speed electronic news feeds 利用合法新闻来交易，需要系统low latency， 也叫Low-latency traders
- Electronic Quote Matchers - try to exploit the **standing orders**. 用standing orders的best ask & best bid来保护自己，苗头不对马上脱手, 存在limit loss。 通过识别机构投资者的意图来获利, 需要low latency
    - **Standing Order** - limit order waiting to be filled.
- Buy Sider: 
    - Advanced Orders: Limit Order with limit prices that change as mkt conditions change.
    - **Flickering Order/Quotes** - electronic traders submit and then cancel shortly thereafter, often within a second. They do not want their orders to stand in the market.
    - **Leapfrogging quotes** - （小跳蛙**不是市场操纵**，因为是为了竞价购买或者卖出，在spread区间内，**大spread时适用**，当spread小则leap的可能性变小）When bid–ask spreads are wide, dealers often are willing to trade at better prices than they quote. They quote **wide spreads** because they hope to trade at more favorable prices. **When another trader quotes a better price, dealers often immediately quote an even better price.** If the spread is sufficiently **wide**, a game of leapfrog may ensue as the dealer jumps ahead again.
- Market Manipulation: Improper operations and Distorting activities, such as
    - (1) Trading for market impact 操纵价格; 
    - (2) **Rumour mongering**: 散布谣言dissemination of false info; 
    - (3) **wash trading: create the impression of market activity at a particular price**; 
    - (4) **Spoofing / Layering**: traders place exposed standing limit orders to convey an impression to other traders that the market is more liquid than it is, or to suggest to other traders that the security is under- or overvalued. 通过limit order造成liquidity的假象。
    - (5) **Bluffing**: influence other traders’ **perceptions** of value, especially **momentum** traders.
    - (6) **Gunning the Market**: Selling quickly to push prices down with the hope of triggering stop-loss sell orders.
- Traders:
    - **Electronic proprietary traders (专属交易员)** can include **high-frequency traders** who complete round trips of a purchase followed by a sale within a short period of time and news traders who trade quickly in response to new information. They would generally not have the same interests as parasitic traders.
    - **Electronic dealers** ***make markets*** by placing bids and offers with the expectation that they can profit from round trips at favourable net spreads. On the first indication that prices may move against their inventory positions, they immediately take steps to reduce their exposure.
    - **Quote matchers** are **parasitic** traders (做front running) who base their predictions about future prices on information they obtain about orders that other traders intend to fill. Buy-side traders and their brokers are aware of the efforts quote matchers make to detect and front run their orders. Accordingly, they submit orders at random times and in various sizes in order to make detection more difficult.
    

#### Nouns

- **Bluffers** often prey on momentum traders, who buy when prices are rising and sell when prices are falling.
- **Spoofing** is a trading practice in which traders place exposed standing limit orders to convey an impression to other traders that the market is more liquid than it is or to suggest to other traders that the security is under- or overvalued.
- **Wash trading** consists of trades arranged among commonly controlled accounts to create the impression of market activity at a particular price. The purpose of wash trading is to fool investors into believing that a market is more liquid than it truly is and to thereby increase investors’ confidence both in their ability to exit positions without substantial cost and in their assessments of security values.
- Algorithmic trading generally **decrease** the impact of large trades and the cost of executions. 因为 algorithm trading可以拆单子