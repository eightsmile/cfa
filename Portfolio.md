## Portfolio

### ETFs

Investors -> AP -> Portfolio Managers

在US：投资者 只能找AP买二级ETF。 只有AP可以一级create / redemption ETF 通过拿 a basket of stocks 换

#### Expense Ratios

- Rolling Return Assessment - Tracking Difference. Allows for comparison with other annual metrics such as fund's expense ratio.
- ETF's Expense ratio does not reflect the cost of portfolio rebalancing or other fees.

#### Tracking Error

Annualised Standard Deviation of daily (ETF returns - Benchmark Returns)

It does not reveal whether the fund is over/under-performed, or whether that tracking error is concentrated over a few days.

**Sources of Tracking Error**: 

- Fees and Expenses 大
- Representative sampling/optimisation 大
- Index Changes 当权重变的时候产生，但是会立刻调整 小

#### Capital Gain Distribution

The issue of **capital gains distributions affects all investors** in taxable accounts. ETFs are said to be “tax fair” and “tax efficient” because they have certain advantages over traditional mutual funds regarding capital gains distributions. On average, they **distribute less in capital gains than competing mutual funds**.

**Reasoning**:

- In a **traditional mutual fund**, when an investor sells, the fund must (with a few exceptions) sell portfolio securities to raise cash to pay the investor. **Any securities sold at a profit incur a capital gains charge, which is distributed to remaining shareholders**.
- In contrast, an investor sells ETF shares to another investor in the secondary market.  - No Tax. If an AP redeems ETF shares, redemptions do not trigger capital gain realizations. - No Tax
- When an AP submits shares of an ETF for redemption, the ETF manager can choose which underlying share lots to deliver in the redemption basket. By choosing shares with the largest unrealized capital gains—that is, those acquired at the lowest cost basis—ETF managers reduce potential capital gains in the fund. 

#### Trading Costs + Management Fee

Round-Trip Trading Cost (%) = One-way Commission * 2 + 1/2 Bid-Ask Spread * 2

Total Fees = Round-Trip Trading Cost + Management Fees = One-way Commission * 2 + Bid-ask Spread + Management fee

### Multi-factor Model

$$r = \beta_0+\beta_1x_1x+\beta_2x_2+...+\beta_kx_k$$

- $\beta_0$ is the expected return, mean return. / risk free rate
- Compare each factors with the benchmark

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

### Economics and Investment Market

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
  - E.G. If $m$ is low. If bond price currently is too high, then less are affordable to people, so less people invest by buying bonds for future. They not invest future, and they consume  more today, so MU0 decrease, and $m$ gradually increase.
- Real Risk Free Ratee, $1+R = \frac{1}{m} $. There higher the GDP growth, the higher $R$ - **One-period Real Interest Rate**.

#### Normal Risk-free Interest Rate $r$

Inflation = Expected Inflation $\pi$ + Risk Premium for Uncertainty, $\theta$

$$r_{long} = R +\pi + \theta$$

$$r_{short} = R +\pi $$

短期，不考虑uncertainty $\theta$， 因为 uncertainty is not realised，但是长期需要考虑

Break-even inflation rate (BEI), $BEI = r_{non-inflation Index} - r_{inflation-indexed}$, then what left with is the inflation.

#### Two Key Points

- **Economic Growth** $\uparrow$, then **Credit Spread**  narrow $\downarrow$
- Valuation Ratios $\uparrow$, coz price increase.
- Stylised Factors, small-cap outperform

#### Risk-covariance

$P_t = E(P_{t+1}\times m)=E(P_{t+1})E(m) + cov(P_{t+1},m)$

$1+R = \frac{1}{m}$, so $m=\frac{1}{1+R}$, so $P_t=\frac{E(P_{t+1})}{1+R} + cov(P_{t+1},m)$

**PV = Discounted FV + Cov(FV, intertemporal Substitution)**

- In general with **risk-averse investors**, the covariance term for most risky assets is expected to be negative. That is, when the expected future price of the investment is high, the marginal utility of future consumption relative to that of current consumption is low.
- Note that with a one-period default-free bond, the covariance term is zero because the future price is a known constant ($1) and the **covariance of a random quantity with a constant is zero**; and intuitively, its value is given by the first term.

#### GDP Growth and Interest Rate

Real Risk Free Ratee, $1+R = \frac{1}{m} $. There higher the GDP growth, the higher $R$ - **One-period Real Interest Rate**.

Pay more attention to the **intuition of intertemporal substitution**. 

- Assume GDP growth $\uparrow$. If desire more on current, then demand for future is less(invest in bond for future is less). So bond price is low, the return of saving/investing $R$ is high. Mathematically, if MU0 is larger, $m$ then is lower, $1+R = \frac{1}{m} \uparrow$, so the real default-free interest rate increase.

Similarly, if volatility of GDP growth $\uparrow$, then desire of consume 

#### BEI 

BEI = zero coupon **Nominal** Bond  -  zero coupon **Real** Bond = $\pi$ + $\theta$, equals to the sum of expected inflation + volatility of inflation (the premium of uncertainty of inflation).

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

- $R_A = R_p - R_B$
- $\alpha = R_p - w\times R_B$

#### Active Weights

$$\Delta w_i = w_{p,i} - w_{B,i}$$

- The sum of those $\sum \Delta w =0$
- Active Return, $R_A = \sum \Delta w_i \times (R_i-R_B)$

Decompose the **Value Added \ Active Return**, there would be (1) Security Selection $w_p(R_p - R_B)$, and (2) Asset Allocation $(w_p - w_B)R_B$.

<img src="C:\Users\Cooper\AppData\Roaming\Typora\typora-user-images\image-20230318222804800.png" alt="image-20230318222804800" style="zoom:33%;" />

#### Sharpe Ratio is Unaffected by Leverage

$$SR = \frac{R_a-R_B}{\sigma_a}=\frac{c(R_a-R_B)}{c\sigma_a}$$

SR is unaffected by cash. CML slope，怎么延长斜率都不变

#### Information Ratio - aggressiveness of active weights

Active Return relative to a benchmark with volatiltiy of the active reutrn.

$$IR = \frac{R_p - R_B}{\sigma_{R_p - R_B}}=\frac{R_A}{\sigma_A}=\frac{ActiveReturn}{ActiveRisks}$$

Affected by leveraging cash，因为cash多了，active management就少了，所以受cash比例影响

$$SR_p^2 = SR^2_B + IR^2$$



- $IC = Corr(\frac{R_A}{\sigma_i},\frac{\mu_i}{\sigma_i})$
- $TC = Corr(\frac{\mu_i}{\sigma_i},\Delta w_i\sigma_i)$

- $IR = TC\times IC\times \sqrt{BR}$
- Corr(\frac{R_A}{\sigma_i},\frac{\mu_i}{\sigma_i})$$
- $\mathbb{E}(R_A) = TC\times IC\times \sqrt{BR}\times \sigma_A$