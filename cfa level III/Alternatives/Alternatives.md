# Alternative Investments for Portfolio Management

## Hedge Fund Strategy

### Equity Strategy 

#### Long/Short Equity

- Extract Alpha return,
- Return is similar as long-only approach, but standard deviation is 50% lower because short parts hedge risks.
- May have leverage.

##### Dedicated Short Selling and Short-biased

bottom up

- Look for poorly managed and overvalued companies 如 浑水
- Activist short selling 在short后出报告
- Typically take a **bottom-up** approach   short的全是bottom-up
- the stock’s **high short-interest ratio** and **high cost to borrow** (“on special”) are very concerning. Both factors suggest significant potential that a dangerous **short-squeeze situation**.

- **Dedicated short-selling** funds take **only** short positions.
- **Short-biased** hedge fund focues on good short-side stock picking.
- Activist short-selling funds take short positions and publicly share their negative fundamental views. 

##### Equity Market Neutral (EMN)

- Construct a **zero beta portfolio**, so **immune to market risk**, **earn only alpha**
- Types:
    1. Pairs Trading: two stocks hedge each other
    2. Stub Trading: long short subsidiary and parent
    3. Multi-class Trading: long short mispriced share classes of the same firm
- The **availability** and **cost of leverage** are considered in terms of desired return profile and acceptable potential portfolio drawdown risk.
- Low return, because market neutral. 
- Short horizon and active trading, so highly diversified and liquid
- **High leverage**. EMN strategies typically do not meet regulatory leverage limits for mutual fund vehicles. So, **limited partnerships** are the preferred vehicle.
- Work well when the market is vulnerable and weak.
- Equity market–neutral managers are likely to have high levels of diversification and turnover ratios.

**Sample Text:** Overall, EMN managers are more useful for portfolio allocation **during periods of non-trending or declining markets**. EMN hedge fund strategies take opposite (long and short) positions in similar or related equities having divergent valuations while attempting to maintain a near **net zero portfolio exposure to the market**. EMN managers **neutralize market risk by constructing their portfolios such that the expected portfolio beta is approximately equal to zero**. Moreover, EMN managers often **choose to set** the **betas** for sectors or industries as well as for common risk factors (e.g., market size, price-to-earnings ratio, and book-to-market ratio) **equal to zero**. Since these portfolios **do not take beta risk and attempt to neutralize many other factor risks**, they typically **must apply leverage** to the long and short positions to **achieve a meaningful return profile** from their individual stock selections. 因为风险小，return小，所以加杠杆才能扩大收益

EMN strategies typically deliver return profiles that **are steadier and less volatile** than those of many other hedge strategy areas. Over time, their conservative and constrained approach typically results in a less dynamic overall return profile than those of managers who accept beta exposure. Despite the use of substantial leverage and because of their more standard and overall steady risk/return profiles, equity market-neutral managers are often a preferred replacement for fixed-income managers during periods when fixed-income returns are unattractively low.

---

### Event-Driven Strategy

#### Merger Arbitrage

Merger arbitrage is a good uncorrelated source of alpha.

- A: Acquirer
- T: Target

If the merger successes, then use the T stock to A stock, and take cost difference.

If the merger fails, then prices should revert back to their pre-merger announcement levels

##### Cash-for-Stock

Buy target, T

##### Stock-for-Stock

Buy share of T, sell share of A. Because A issue share to buy T, then share price to A decrease, and demand of A stock increase, so A price increase.

Overall Characteristics:

- If the deals fail, this strategy has market sensitivity and left-tail risk attributes.
- The preferred vehicle is **limited partnership** because of merger arbitrage’s use of significant **leverage**, but some low-leverage, low volatility liquid alts merger arbitrage funds do exist.
    - typically apply 3 to 5 times leverage in order to achieve lowdouble-digit returns.
- Kind diversified, because the Acquirer and Target together is a composite, pretty much irrelevant with other portfolio. Thus, diversified.

特点：

- expose to **left-tail** risks，因为若失败了，损失格外大
- Leverage：高杠杆（只要是arbitrage的，都高杠杆）一般3-5倍

#### Distressed Securities

Focus on firms that are (1) in bankruptcy, (2) under financial stress. Focus on:

- Recovery Value
- Undervalued Debt Securities

Characteristics:

- High return, but return is cyclical. The distressed securities strategy works better under postive Econ environment.
- High level of illiquidity
- Low leverage

**Sample Text**: Event-driven strategies, such as merger arbitrage, tend to be exposed to some natural equity market beta risk. Event-driven merger arbitrage strategies have **market sensitivity and left-tail risk attributes**. Also, **while event-driven strategies may have less beta exposure than simple, long-only beta allocations, the higher hedge fund fees effectively result in a particularly expensive form of embedded beta.** 由于会受tail risk影响，而全部白给

---

### Relative Value Strategy

#### Fixed-Income Arbitrage

- Yield Curve Trades: taking long and short positions at different points on the yield curve
  - **Sample Text**: For yield curve trades, the prevalent calendar spread strategy involves taking long and short positions at different points on the yield curve where the relative mispricing of securities offers the best opportunities, such as in a curve flattening or steepening.

- Carry Trades: long a higher yielding security and shorting a lower yielding security
  - **Sample Text**: Carry Trade: A classic example of a fixed-income arbitrage trade involves buying lower-liquidity, off-the-run government securities and selling higher-liquidity, duration-matched, on-the-run government securities.


**Return profile is like put option.**

- If the strategy unfolds as expected, it returns a positive carry plus a profit from spread narrowing.
- If the spread unexpectedly widens, then the payoff becomes negative.

#### Convertible Bond Arbitrage

long short volatility 与 long short option方向一致，因为option 与 vol 正相关

Convertible bond = straight debt + long equity call option

- Conversion value = stock price * conversion ratio
    - If conversion value > bond value, then in-the-market
    - Vice versa
- Conversion ratio = # of share a bond can exchange

Convertible bond is complex structured, so generally under-valued. **Buy Convertible bond, short corresponding # of stocks.**

If the convertible bond’s current price is near the conversion value, then the **combination of a long convertible and short equity delta exposure will create a situation** where for small changes in the share price and ignoring dividends and borrowing costs, **the profit/loss will be the same.**

---

### Opportunistic Hedge Fund

#### Global Macro Strategy

- **Top-down**, fundamental model, trend driven 追逐全球趋势
- Heterogeneity 包括多种 assets 特异
- leveraged 用杠杆放大风险
- 受制于全球经济risks，so perform worst during recession 。no diversified in crisis 全球金融危机时，全完蛋

#### Managed Futures

- exotic contract: furtures on weather / derivatives on carbon emission, etc.
- time-series momentum trend 
    - Absolute basis: can net long / net short

- cross-sectional momentum
    - **Net zero** or **market neutral** 
    - Work well when market is out / underperformed relative to other mkt  因为net zero


#### Characteristics

- **Both**: Derivative 多 -> leverage 多 -> 风险多，volatility 
- **Both**: 但是因为有derivatives可以hedge 风险，所以当经济差的时候 left tail的风险可控，right-tail skewness
- **Both** are highly liquid

- **Managed futures** take more **systematic approach**
- **global macro managers** are **more discretionary**

---

### Specialist Strategies

#### Volatility Trading

Roll down: Source and buy cheap volatility and sell more expensive volatility, earn premium 

**Equities and volatility are negatively correlated. In order to hedge the equity exposure in the portfolio, a long volatility position is necessary.** 

VIX option和stock之间可以diversify

- Strategy:
    1. Outright long volatility, 买期权 with **delta hedging of the gamma exposure** 交易所交易
    2. OTC options 期限maturity长于2年的，OTC交易
    3. VIX index
    4. OTC volatility swap / variance swap
- Characteristics:
    - **Long volatility strategy is a convex strategy**. Skew to the right 凸性策略，比较好 （期限越长越好
    - Liquidity 交易所交易的liquidity好，但期限短。OTC liquidity 差，但期限长
    - options 自带 leverage

#### Reinsurance and Life Settlements

- insurance contracts are not liquid and difficult to sell.
- the insurance and reinsurance themselves are independent with the market, so uncorrelated with the equity mkt. Thus, diversified

Hedge Fund 会一次性买一个 pool的保单， pay lump sum fee 一次性一笔的买断费，然后pay ongoing premium payments 按期付保费，在受保人die 的时候挣 death benefits：

- Hedge funds look for policies in which the **ongoing premium payments to keep the policy active are relatively low**. 每期支付保费少的
- Hedge funds also look for life settlements where the **surrender value offered to the insured individual is also relatively low**,不懂 surrender value 指的是提前终止 提出来的钱。可能是相对应，收益人想要提前终止，要把钱还给收益人，因为之前一次买断过，收益人会找hedge fund surrender
- and the probability that the designated insured person is likely to die **earlier** than predicted by standard actuarial methods is relatively high. 先死给的理赔多

---

### Multi-Manager Strategy

#### ![Screenshot 2023-10-29 at 00.50.27](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-29%20at%2000.50.27.png)

![Screenshot 2023-10-29 at 10.40.41](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-29%20at%2010.40.41.png)

**FoF一定有 double layer fees**: **FoFs have double layers of fees** without being able to net performance fees on individual managers. The FoF investor always faces netting risk and is responsible for paying performance fees that are due to winning underlying funds while suffering return drag from the performance of losing underlying funds. Even if the FoF’s overall performance (aggregated across all funds) is flat or down, FoF investors must still pay incentive fees that are due to the managers of the winning underlying funds. 

**MSF (Multi-Strategy Fund) 的 fee 可以内部抵消（gain 的 loss 的可以net）**The fee structure is more investor friendly at MSFs, where the general partner absorbs the **netting risk arising from the divergent performance** of the fund’s different strategy teams. This is an attractive outcome for the MSF investor because (1) the GP is responsible for netting risk and (2) the only investor-level incentive fees paid are those due on the total fund performance after netting the positive and negative performances of the various strategy teams.

**MSF更方便切换战略做TAA，因为内部有自己的小团队**。**MSFs can reallocate capital into different strategy areas more quickly and efficiently than is possible in FoFs**, allowing MSFs to react faster to real-time market impacts. This shorter tactical reaction time, combined with MSFs’ better strategy transparency, makes MSFs more resilient than FoFs in preserving capital.

**FoF的FM更多，所以operational risks diversidied，但是MSF相对应内部有一大堆FM，还是有较高concentrated operational risks.** MSFs have higher manager-specific operational risks than FoFs. In MSFs, teams of managers dedicated to running different hedge fund strategies share operational and risk management systems under the same roof. This means that the MSF’s operational risks are not well diversified because all operational processes are performed under the same fund structure. FoFs, in contrast, have less operational risk because each separate underlying hedge fund is responsible for its own risk management

More Sample Text: 

1. Multi-strategy managers like Hedge Fund B can reallocate capital into different strategy areas more quickly and efficiently than would be possible by a fund-of-funds (FoF) manager like Hedge Fund C. The multi-strategy manager has full transparency and a better picture of the interactions of the different teams’ portfolio risks than would ever be possible for FoF managers to achieve. Consequently, the multi-strategy manager can react faster to different real-time market impacts—for example, by rapidly increasing or decreasing leverage within different strategies depending upon the perceived riskiness of available opportunities.
2. The fees paid by investors in a multi-strategy fund can be structured in a number of ways, some of which can be very attractive when compared to the FoFs’ added fee layering and netting risk attributes. Conceptually, FoF investors always face netting risk, whereby they are responsible for paying performance fees due to winning underlying funds while suffering return drag from the performance of losing underlying funds. Even if the FoF’s overall performance is flat or down, FoF investors must still pay incentive fees due to the managers of winning funds.

Multistrategy funds typically use **more leverage** and have **more volatile return profiles** than funds of funds.

Multistrategy funds have **faster reaction times for tactical allocation changes**.

Funds of funds potentially offer a **more diverse mix** of strategies.

---

## Analysis of Hedge Fund Strategy

### Conditional Factor Risk model - turbulent market period

in order to analyse whether hedge fund **risk exposures** that are **insignificant during calm market** periods may become **significant during turbulent market period.**

$Return_{hedgeFund} = \alpha_i + \beta_1 F_1 + \beta_2 F_2 + \beta\times Dummy+\beta \times D\times  F_2 ...+\epsilon$

The Unexplained Returns are (1) alpha; (2) alpha (FM investment skills); (3) omitted factor; (4) random error

### Conditional Factor Risk Model

reg HF return on 

1. Equity Risks (S&P500) 整个市场的风险
2. Currency Risks (USD) 外汇风险
3. Credit Risks (CREDIT) 债券风险
4. Volatility Risks (VIX) Options风险

- It is a conditional model as there is a dummy variable that distinguishes between calm market and turbulent market condition. 用dummy区分market condition

Traditional Portfolio: 60/40 Equity/Debt

If hedge fund is added, there could **increase Sharpe and Sortino ratios, and diversify risks**. 降低风险 提高收益

#### Risk-Adjusted Measure

- high Sharpe and Sortino Ratio 指标好的策略

    1. Systematic Futures
    2. Equity Market Neutral
    3. Global Macro
    4. Event Driven Hedge Fund Strategy

- Do not enhance risk-adjusted performance 指标不好的策略

    1. FoF
    2. Multi-Strategy

    - 因为 分散风险 risk 降低，所以 return 也降低了

#### Drawdown

the higher the drawdown, the greater the **tail risks**

- Event-driven (MA) 策略，是为了挣 high earning，若MA失败，会暴露大 tail-risks
- Relative Value: 因为high leverage, 所以 market volatile 会带来大drawdown

---

## Alternative Investment

### Timber

- Earn: Capital Growth, Inflation Resistance
- Risks: Even Risks <- Insurance

### Commodity * 4

1. Metals
2. Energy
3. Livestock/ Meat
4. Agriculture

Invest in  (1) future (2) 实物 farmland 

### Real Estate

**Public real estate** has had a fairly **high, positive correlation with equities**, as well as a **high, positive equity beta.** In contrast, fixed income has broadly had a negative correlation with equity and a small but negative equity beta. Switching from fixed income to real estate will likely **decrease** portfolio diversification an**d increase return volatility.**

### Investment Consideration

- **Risk Characterisitcs**

    1. MVO might be s.t. constarints
    2. Returns are not normally dist
    3. Might not be able to allocate assets as target

- **Establishing Return Expectation**

    1. limited data availability

- **Investment vehicle**

    - LP 出钱，GP 管理 参与运营

    1. Large investors, invest in LP
    2. FoF <- lack of enpertise investors (pros: access and diversify, cons: additional fees layer)
    3. Seperately Managed Accounts (SMA, funds of one) 由GP独立管理，专户管理，给 large investors
    4. Open-ended Mutual Funds and UCITS, give smaller investors access to alternatives 降低准入门槛，给小invetors

- Liquidity

    - Notation:

        1. Commitment 承诺出资，如commit 10b
        2. Call 召款，相当于花3年把10万投完，每投一笔之前都要 call
        3. Calldown Period，相当于召款周期

        - Commited Captial （10b） = Paid in Capital （已经call的，已经投入的） + 未投的

        4. Distribution

    - Drawdown Structure

        1. Captial Call and Distribtuion do not have predertermined schedule , 打款和提款的时间都没有确定
        2. Opportunity, risks of missing a capital call 没办法按时打款，而错过投资机会的风险
        3. Side-Pocket. 侧袋账户。普通账户的钱可以按redemption polcy赎回，但是 side pocket的不行。所以 若 side pocket钱越多，则流动性越大

    - Types:

        1. Event-driven Strategy: frequent redemption period
        2. Relative value funds: hold significant portions of illiquid investments,
        3. Leverage: Margin calls may force a leveraged fund to sell its most liquid holdings 

- Expense and Fee

    - 2/20

- Tax Consideration

- Build v.s. Buy

### Asset Classification

- Traditional Approach 看表面 
  - 按流动性分：private 的流动性都差，public 的都好，包括REITs / Public Real Estate，包括上市公司股票的HF
  - 按通胀，高通胀 real estate / commodity, 高通胀+low growth : inflation-linked bond TIPS, Gold
  - Limitation: 主观判断投资的asset，容易 over-estimate the diversification
  - doesn’t group assets together based on a few shared characteristics. 不会通过risk factor 对asset分类，如 traditional approach 会对待 high yield bond 和 gov bond 会在同一个 fixed-income portfolio中。但是 risk-based approach 会把两种bond 不同对待
- Risk-Based Approach 和 risk fator 回归 
  - 因为是回归，所以 sensitive to hisorical look-back period

## Investment Consideration

![Screenshot 2024-01-14 at 17.51.00](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/202401141751337.png)

![Screenshot 2024-01-14 at 17.51.19](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/202401141751904.png)

![Screenshot 2024-01-14 at 17.51.37](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/202401141751129.png)

#### Suitability Consideration

- Investment Horizon: long
- Enterprise: Skilled Manager
- Governance: formal investment policy
- Transparency: low
- 不能用 s.d. 分析风险，因为 risk 不对称

In sum, alternatives are suitable to high risk tolerance investors.

#### Soft Skills

- commnication skills
- social skill, interpersonal skills
- education and coaching skills
- Business development and sales skills, lead new business development 

P.S. 与 soft skill 对应的是 technical skills 包含: captial market proficiency, portfolio construction ability, financial planning knowledge, technology skills, **language skill** 多会说一种外语

### Approach to Asset Allocation

- Monte Carlo Simulation 
- MVO
    - establish limits
    - incorporate downside risks (mean-CVAR optimisation)
    - consider skewness
    - Cons: sensitive to small change of inputs 
- Risk Factor Based Optimisation

### Liquidity Planning

- Capital Contribution = Rate of Contribution * (Capital Commitment - Paid-in-Capital)
- Distribution = Rate of Distrubiton_t * NAV * (1 + growth rate)
- NAV_1 = NAV_0 (1+g) + Capital Contribution - Distribution

#### NAV 

NAV net asset value 资产净值 , by BASE

$NAV_e = NAV_b +A - S$

$NAV_t = NAV_{t-1} \times (1+g) + Captial Contribtuion - Distribution$

- A: Capital Contribution 打款 <- Call, 

    Capital Contribution = Rate of Contribution * (Capital Commitment - Paid-in Capital) 

    承诺要付的CC - 已经付的 Paid-in

#### Avoid Cash Drag

为了保证 Capital Contribution / call 的时候有钱可以投进去，又避免持有 cash 导致 return过低。

在 call 之前，把准备投

1. 投 PE 的钱，投 Public Equity
2. 投 RE 的钱，投 REITs

#### Prepare for Unexpectation (Stress-test)

Stree test for unexpectred events 

### Performance Evaluation

Benchmark:

- Custom Index Proxies (i.e. MSCI world index + 3%)
- Peer Group Comparison, percentile of Peers

Others:

- Private Equity, Credit, Real Estate 流动性最差的三种 用 IRR  , 

    - Cons 受CF出现的时间点影响，只考虑了 percentage 没考虑 Value Amount

- Private Equity 还可以用 $MOIC = \frac{Cummulative Distribution}{Paid-inCapital} = \frac{D_1 + D_2 + D_3}{C_1+C_2 +C_3}$

    直接把现金流相加，不折现。Pros: 不受CF时点影响，Cons: 但是没考虑Time Value of Money

### Monitor the Investment Program

投之前需要考虑的

- Key person risk 关键FM离职的风险，p.s. 对于量化基金 关键的是model，所以Key Person Risk 不大
- Alignment of Interests, whether FM's interests remain closely aligned with their own 是否执行之际的interest
- investor 要理解 FM 的 Risk Management Philosophy 不会随意 提取钱出来
- Investor gauge the profile
