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