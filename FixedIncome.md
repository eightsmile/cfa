## Fixed Income

### Rate

#### Spot Rate

For **Option-free**, **Default-free**, **Zero-coupon** Bond, with single payment at maturity.

#### Forward Rate

$F_{6,9}$ - 从第6个月开始到第九个月结束的rate，相当于是三个月的rate，但是在第六个月开始。

$$F_{6,9} = \frac{DF_9}{DF_6}$$

##### Relationship between spot rate and forward rate

- When the spot curve is upward sloping, the forward curve will lie above the spot curve.
- When the spot curve is downward sloping, the forward curve will lie below the spot curve.
- See .`ipynb` file for details

##### Active Bond Management

Future Spot Rate $\downarrow$ **=>** Future Bond Price $\uparrow$ **=>** Long at Forward would gain.

##### **Riding the Yield Curve / Rolling Down the Yield Curve**

Yield Curve is upward sloping: If the trader believe that the yield curve will not change its level and shape over an investment horizon, then **buying bonds with a maturity longer** than the investment horizon would provide a total return **greater** than the return on a maturity-matching strategy.

#### Par Curve

YTM on **coupon-paying** **government bonds**, **priced at par**, over a range of maturities。 与 spot 不同的是，par curve 用 coupon-paying bonds

- Usually use **on-the-run** bonds, because newly issued ones have price close to the par.
- **Zero-coupon rates** could be determined by using the par yields, via via **forward substitution** known as **bootstrapping**.

#### YTM

A rate of return for a bond that is **held until its maturity**, assuming that all coupon and principal payments are made in full when due and that **coupons are reinvested at the original YTM**.

The YTM can provide a poor estimate of expected return, if 

- interest rates are volatile; 
- the yield curve is steeply sloped, either upward or downward; 
- there is significant risk of default; 
- the bond has one or more embedded options (e.g., put, call, or conversion).
- It's **not** realistic to re-invest at YTM.

**Flat Yield Curve** - long / short term bond offer equivalent yields. So, there is **no benefit to invest in longer-term** one. 

#### Swap Rate Curve

Subsume from MRR.

##### Swap Rate Curve & Gov Spot Curve

- The swap market is a highly **liquid** market. Swap markets have more maturity.
- Swap market is **unregulated** (not controlled by governments), so swap rates are more comparable across different countries.

### Spread

| Type               | Calculation                                                  | How it Uses?                                |
| ------------------ | ------------------------------------------------------------ | ------------------------------------------- |
| Swap Spread        | Swap Rate - Treasury Yield                                   | Default Risk & Liquidity Risk               |
| I - Spread         | $Yield_{i}$ - Swap Rate, with same maturity                  | Credit Risk & Liquidity Risk                |
| Z - Spread         | $$P = \frac{C}{1+S_1+Z}+\frac{C}{(1+S_2+Z)^2}+\frac{C+Principal}{(1+S_3+Z)^3}$$ | Credit Risk & Liquidity Risk & Option Risk  |
| TED Spread         | $MRR - TBill$, with same maturity                            | Default Risk in the system                  |
| Libor - OIS Spread | LIBOR - OIS rate  , where OIS rate 相当于隔夜拆借            | Risk and Liquidity of Money Market Security |

### Term Structure of Interest Rate

| Type                     | Description                                                  | Shapes                                                       |
| ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Pure expectations theory | The forward rate is an unbiased predictor of the future spot rate. Fail to consider the riskiness of bond investing. | • Upward <br />• Downward <br />• Flat yield                 |
| Local expectation Theory | Expected return for bonds over short time periods is risk free | • Same with Pure expectations theory                         |
| Liquidity theory         | Forward rates = expectation of future rates + liquidity premium | • Upward: either rising expected future rates or remain but liquidity premium added <br />• Downward: fall |
| Segmented market theory  | Yield is solely function of demand and supply                | • Independent maturity segment                               |
| Preferred habitat theory | Forward rates = expectation of future rates + premium for moving out of the preferred habitats | • Explain almost any yield curve shape                       |

The **typical** term structure of credit spreads is upward sloping because investors typically want more compensation for future credit uncertainty. 

The two examples he gives for when credit term structure can be inverted are valid: high-yield issuers in cyclical industries at the bottom of a cycle where investors are looking past the bottom of the cycle and bonds that have a very high likelihood of default where a primary pricing mechanism is based on the recovery amount in default.

### Factors affecting Interest Rate

1. Monetary Policy explains mostly in the short-term, and 1/3 in the long-term of bond yield variation. Long-term rate is mostly affected by inflation and economic activities.
2. Volume of Economic Activity
3. Monetary Policy - Bearish Flattening / Bullish Steepening
4. Fiscal Policy - Fiscal **supply-side** effects affect bond prices and yields. If the budget deficits rise (fall), then yield would increase (decrease).

- During highly **uncertain** market periods, investors flock to government bonds in what is termed a **flight to quality**, often associated with **bullish flattening**, in which the yield curve flattens as **long-term rates fall** by more than short-term rates. 当市场不确定时，投资者开始买 长期gov bond，拉高价格，拉低长期rate。导致bullish flattening

##### Investors' View - Interest Rate & Bond Future Contract

- Investors expecting **interest rates to fall** will generally **extend portfolio duration** relative to a benchmark to take advantage of bond price increases from falling rates, *vice versa*. 因为利率下降，如果duration大，则bond price提升多
- To capitalise on a **steeper** curve, traders will **short long-term bonds** and **purchase short-term bonds**. Steep curve意味着 预期短期rate小长期rate大，则 预期短期price升，长期price降。所以short long-term，long short-term
- Long-only investor 可以切换 Bullet Investment & Barbell Investment. E.G. Expected Bullish Flatten则预期长期rate下降，长期bond价格上升，则invest Barbell

### Arbitrage Opportuntiy

- **Value Additivity**: Whole = Sum of Parts

- **Dominance**: a financial asset with a risk-free payoff in the future must have a positive price today.

- **Rational**: **when the profit happens in year 0 only, it's a value additivity arbitrage **

    **and when happens at year 1 it's a dominance arbitrage**.

#### Binomial Interest Rate Tree - Arbitrage Free

$$i_L = i_H \times e^{2\sigma}$$

- , where $\sigma$ is the volatility of the one-year rate. To proxy the volatility, we may use (1) Historical Interest rate's Volatility; (2) observed market prices of interest rate derivatives.
- We assume equal probability of up and down.
- Interest rate tree is referred as a log-normal tree, using lognormal random walk.
- Number of Path is $2^{N-1}$, 如 4 期有 $2^3=8$ 条path.

#### Monte Carlo Forward-Rate Simulation

Could be used if the Cash Flow is **path dependent**.

- MBS is path dependent on the interest rate. MBS can not be properly valued with the binomial model or any other model that employs the backward induction methodology.
- 当用 Monte Carlo 测 bond时，如果bond 没有 embedded option，那么 volatility of Monte Carlo 不会对 bond估值有影响。提高 simulation num 到一定程度后，不会再提高模型精准度。此时， 每期 tree + constant

#### Term Structure Models

- Equilibrium Model - describe how interest rate evolves. 用rate本身做mean reverting

    - Cox-Ingersoll-Ross Model - CIR model

    $$ dr_t = k(\theta - r_t)dt + \sigma \sqrt{r_t} dX $$

    - Vasicek Model

    $$dr_t = k(\theta -r_t)dt + \sigma dX$$

​		They are both mean reverting. CIR model make the volatility proportional to the squared root of the short-term rate. That property make the volatility increase with the level of interest rate.

- **Arbitrage-Free Models** - match the current market data 用市场的数据推算 rate - to **calibrate** 

    - Ho-Lee Model - simple S.D.E.

    $$ dr_t = \theta_t d_t + \sigma dX $$

    - Kalotay-Williams-Fabozzi (KWF) Model

    $$ d\ ln(r_t) = \theta_t d_t + \sigma dX $$

    ​	, the log term ensure the rate cannot be negative.

    , where $\theta_t$ is time dependent to calibrate the market data, allow for time-varying parameter. Arbitrage-Free model is more accurate.

### Embedded Option Bond Valuation

Volatility increase the value of options and so embedded option bond, but do not affect the value of straight bond.

Option-free bond (包括MBS)不会收到 implied volatility影响，那

#### OAS

当只给 利率二叉树，还要算option embedded bond时，要在利率二叉树的基础上 + OAS

把 embedded option bond 的现金流折成 without option bond 的 spread

$$ PV_{BondWithoutOption} = \frac{CF_1}{1+r+OAS} +\frac{CF_2}{(1+r + OAS)^2}+... +\frac{CF_n}{(1+r+OAS)^n}$$

$$PV_{BondWithoutOption} \pm  V_{option} = PV_{BondEmbedded Option}$$

换句话说，OAS 把 $PV_{BondWithoutOption} $ 折成了$PV_{BondEmbedded Option}$. 

- OAS 大，则把 Cash Flow折成的PV更小，那么就意味着，Value of Option更大。
- 对于 call:  $V_{CallableBond} = V_{Bond} - V_{call}$
- 对于 put: $V_{PutableBond} = V_{Bond}+V_{put}$

所以，如果Volatility of Interest增大，Value of Option增大。则 $V_{CallableBond}$ 变小

因为market value of bond remains the same, so we need a small OAS to discount the $V_{callableBond}$ to the current market value of bond, 所以OAS小。$V_{PutableBond}$ 变大，所以OAS变大。

P.S.The price of the bond doesn’t change; it’s the market price of the bond. What changes is ***your assumption about interest rate volatility*** in ***your binomial tree***. The market doesn’t know about your binomial tree, and if it did know about it, it wouldn’t care.

##### Effect of Volatility on OAS

| Voliltiy     | Call         | Put          | Callable     | Putable      | OAS_Call     | OAS_Put      |
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
| $\uparrow$   | $\uparrow$   | $\uparrow$   | $\downarrow$ | $\uparrow$   | $\downarrow$ | $\uparrow$   |
| $\downarrow$ | $\downarrow$ | $\downarrow$ | $\uparrow$   | $\downarrow$ | $\uparrow$   | $\downarrow$ |

### Durations

#### Effective Duration

Effective duration indicates the sensitivity of a bond’s price to a **100 bps parallel shift** of the benchmark yield curve assuming no change in the bond’s credit spread.

$$ ED = \frac{ P_+ - P_- }{2\times\Delta curve \times P_0} $$

$$EC = \frac{P_- + P_+ - 2P_0}{(\Delta curve)^2 \times P_0}$$

- Assuming **parallel shifts** in the benchmark yield curve.
- Effective durations are normally calculated by averaging the changes resulting from shifting the benchmark yield curve up and down by the same amount. 

- This calculation works well for option-free bonds, but the results can **be misleading in the presence of embedded options**. 如果embedded option 则不好使
- The price sensitivity of bonds with embedded options is not symmetrical to positive and negative changes in interest rates of the same magnitude.
- For the **Floater**, Effective Duration is close to the period. For example, a one-year set floater has ED = 1.
- E.G. As **rates rise** the call is less likely to be called therefore increasing duration. Think of it like this straight bond - call option, because it is a benefit to the issuer. As interest rates rise, a call option moves out of the money, which **increases the value of the callable bond and lengthens its effective duration**.

#### One-side Duration

One-side duration states the sensitivity of bond with **embedded options** is not symmetrical to interest rate increase / decrease.

One-side duration is better at capturing the interest rate sensitivity of a callable or putable bond than the (two-sided) effective durations, particularly when the embedded option is **near the money**.

与ED相同，时parallel shift of yield curve，但是是单边的。

#### Key-rate Duration

- **Key rate durations** reflect the sensitivity of the bond’s price to changes in specific maturities on the benchmark yield curve. 用来衡量 yield curve 形状的变化
- help portfolio managers and risk managers **identify the “shaping risk” for bonds**—that is, the bond’s sensitivity to **changes in the shape** of the yield curve (e.g., **steepening and flattening**).
- 可以用来分析 change of shape of yield curve。因为关键点变了，可以理解为整条线变了。

#### Capped / Floored Floater

- Value of Capped Floater = Value of Straight Bond  -  Value of Embedded Cap
- Value of Floored Floater = Value of Straight Bond  -  Value of Embedded Floor

#### Convertible Bond

- Conversion Ratio = # of shares of common stock
- $\text{Conversion Price} = \frac{\text{Issue Price}}{\text{Conversion Ratio}}$
- **Market** Conversion Pirce $= \frac{Bond's Mkt Price}{Conversion Ratio}$, 现在就以 mkt price 买入bond，就转换成 stock 的 每股的价格。
- $\text{Premium} = \text{Mkt Conversion Pirce} - \text{Share Price}$， 用convertible bond转 stock比stock成本贵的部分。
- $\text{Conversion Premium Ratio} = \frac{Premium}{Share Price}$， 跟share price 比
- $\text{Conversion Value} = \text{Share Price} \times \text{Conversion Ratio}$

### Credit Risk

- Expected Exposure: The expected exposure is the projected amount of money that an investor could lose if an event of default occurs, before factoring in possible recovery. 

    - The expected exposure for both 1-Yr Bond I and Bond II is 100 + 5 = 105. 如是 principal + coupon，与概率无关
    - t=0时是price or value，把时间逐步往回推到 t = 1， t = 2，etc。算当时的 expected cf sum。记得当前的 coupon不用折现了

- Probability of Default (POD)

- Loss Given Default (LGD) % = 1 - Recovery Rate

- Expected Loss = Default Prob * Loss Severity given Default

- Credit Valuation Adjustment (CVA)

- Fair Value of Corporate Bond = VND - CVA
    - VND - Value if No Default
    - VND 由 二叉树算出，或者由折现算出。正常算出的值就是 VND
    - CVA 由 default exposure recovery discount 那个表算出来

- The **risk–return characteristics** of a convertible bond depend on the market price of the issuer’s common stock (underlying share price) relative to the bond’s conversion price. When the underlying **share price is well below the conversion price**, the convertible bond exhibits mostly **bond risk–return characteristics**. **In this case, the price of the convertible bond is mainly affected by interest rate movements and the issuer’s credit spreads.** In contrast, when the underlying share price is above the conversion price, the convertible bond exhibits mostly stock risk–return characteristics. 

    当不太可能转换时，Convertible bond相当于bond，那么受interest rate影响。当很可能转时（换句话说，market price of share 比 convertible price大）则相当于share，受价格影响多。

- A Statement:

    The **actual default probabilities** do not include the default risk premium associated with the uncertainty in the timing of the possible default loss. The **observed spread over the yield** on a risk-free bond in practice does include liquidity and tax considerations, in addition to credit risk.

- Credit Spread = VND对应rate - (VND - CVA)对应的rate

##### Credit Spread Migration Matrix

$\Delta Expected Return=$Sum of % * (Spread_i - Base.Spread)    * (-1) Modified Duration

$$\%\Delta \mathbb{E}(r_i) = - Mod.Duration \times \sum (CS_{base} - CS_i )P$$

- 记得是乘 负的 mod.Duration
- 注意是 diff of rate 即 拿 matrix 算出来的 - 原来的的差 * 负Mod.Duration，得到结果为 rate 的变化量，再加上原来的 YTM，得到的即是 next year expected return

因为modified duration 转换 $\Delta rate$ 和 $\Delta price$ 的关系，其中$\Delta Price$ 就相当于 expected return.

**Credit Spread Migration** typically has a **negative impact that reduces the expected return**, for mainly two reasons. **First**, the probabilities for rating changes are not symmetrically distributed around the current rating; they are **skewed toward a downgrade rather than an upgrade**. **Second**, the increase in the **credit spread is much larger for downgrades than is the decrease in the spread for upgrades**. 两个原因，一、降级的概率高。二、降级时spread的变化量大。

##### Default Risk Model

- Structural Model - explain why default 
    - Assume the **Balance Sheet structure with options**.
    - If the asset value falls below the barrier, the company defaults on the debt.
    - Probability of Default is endogenous
    - Provide an Option analogy: consider a company with asset financed by equity and zero-coupon debt. 
        - call option on the asset with a strike price equal to the face value of debt (K).
    - It provides insight into the nature of credit risk. The company defaults when the value of its assets dips below the default barrier.
    - **Used for internal risk management**.
- Reduced Form Model - explain when
    - the default is an **exogenous** (external) variable that occurs randomly.
    - Regression including company specific and macro-economic variables.
    - Inputs are observable.
    - Reflect the changing business cycle.
    - Weakness: (1) result needs to be back-tested; (2) default comes as 'surprise'.

#### Securitised Debt

- Granularity - actual number of obligations 数量，约granular 约多
- Homogeneity - Similarity 相似度，约homo约相似

- Based on Statistics: (1) short-term, (2) Granular, (3) Homo
    - E.G. Credit Card MBS, Trade Receivables MBS
- Based on Portfolio: (1) mid-term, (2) Granular, (3) Homo
    - E.G. Auto MBS
- Loan by Loan: (1) non-granular / small number, (2) Hetero
    - E.G. CMBS, CLO

"Investors, however, seek to benefit from greater diversification, more stable and predictable underlying cash flows, and a return that is greater than that of securities with similar ratings, which provide a reward for accepting the greater complexity associated with collateralised debt."  - For Auto MBS

### CDS

Rationale: 

- Buy Credit deteriorated assets/bonds. 买风险变大的
- Sell Credit Enhanced ones. 卖风险减少的
- Credit Deterioration Signals: Leverage Increase. 
- Large CDS spread, large risks.
- Cheapest-to-Deliver Obligation
    - The payoff of the CDS is determined by the cheapest-to-deliver obligation, which is the debt instrument that can be purchased and delivered at the lowest cost but has the same seniority as the reference obligation.

#### Type of CDS

- **Single Name CDS** - The reference obligation is not the only instrument covered by the CDS. Any debt obligation issued by the borrower that is *pari passu* (ranked equivalently in priority of claims) or higher relative to the reference obligation is covered.
    - 给一个reference，比这个好的，同一个borrower的 都是single name CDS
    - Cheap-to-Deliver
- **Index CDS** allows investors to take a position on the credit risk of multiple companies, although higher credit correlations make the index CDS more expensive to purchase.
- **Tranche CDSs** also cover multiple borrowers, but losses are covered only up to a specific level.

#### Settlement

- Physical Settlement: 给loan，收CDS par value
- Cash Settlement: 直接 收到 CDS par value 和 loan的差值。
- 但是因为 cash settlement 可以有cheapest-to-deliver obligation原则。换句话说是 “收到 CDS par value 和 loan的差值”中loan可以选最便宜的loan，这样 可以收到更多的钱 然后把之前的loan 按市场价卖了。

#### Credit Event

- Bankruptcy
- Failure to pay 不需要 formal bankruptcy filling, 只要没付，哪怕是coupon也算 credit event
- Restructuring
    - refers to a number of possible events, including **reduction** or **deferral of principal or interest**, **change in seniority** or **priority** of an obligation, or change in the currency in which principal or interest is scheduled to be paid.
    - 在 US, Restructuring 不算 credit event

#### Factor Affecting CDS Valuation

- Prob of Default
- Loss Given Default

#### Pricing

Upfront Premium 提前一次付的钱

- Upfront premium on a CDS $ \approx (Credit Spread - Fixed Coupon) \times Duration$
- CDS price can be quoted as ≈ 100 - upfront premium (%)
    - If the price of CDS > 100, the protection seller needs to pay upfront premium 
    - If the price of CDS < 100, the protection buyer needs to pay upfront premium

### Others

- OAS - Tree moves
- Effective Duration - Curve moves
- Key Rate Duration - Shapen changes