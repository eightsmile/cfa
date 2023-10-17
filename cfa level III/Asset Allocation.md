# Asset Allocation

## Economic Balance Sheet

Definition:  includes (1) conventional assets and liabilities (in Accounting Statement) and (2) **extended portfolio assets** and liabilities (not appear in conventional B/S).

**Extended Portfolio Assets** includes: 

1. Human Capital (PV of Future Earnings), 
2. PV of Pension Income (Un-vested Benefits), 
3. PV of Expected Inheritances (Bequest).

- Above is for individual investors, and before is for institutional investors.

1. Underground Mineral Resources
2. PV of Future Intellectual Property Royalties

**Extended Portfolio Liabilities** include:

-  PV of Future Consumption.

Economic Net Worth = Net Worth (Financial Asset - Fin Lia) + 1,2,3

| Asset                                            | Lia and Net Worth                                       |
| ------------------------------------------------ | ------------------------------------------------------- |
| **Financial Assets**                             | Financial Liabilities                                   |
| **Extended Assets**: PV of Expected Contribution | **Extended Liabilities**: PV of Expected Future Support |
|                                                  | **Net Worth**                                           |

<img src="/Users/mie/Library/Application Support/typora-user-images/Screenshot 2023-10-12 at 13.32.36.png" alt="Screenshot 2023-10-12 at 13.32.36" style="zoom:25%;" />

## Asset Allocation Approach

1. Asset Only - MVO
2. Liability-Relative - fund a lia
3. Goals-Based - address goal

| **Asset Allocation Approach** | **Relation to Economic Balance Sheet**         | **Typical Objective**                                        | **Typical Uses and Asset Owner Types**                       | Risk Objectives                                              |
| ----------------------------- | ---------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Asset only                    | Does not explicitly model liabilities or goals | Maximise Sharpe ratio for acceptable level of volatility     | Liabilities or goals not defined and/or simplicity is importantSome foundations, endowmentsSovereign wealth fundsIndividual investors | augmented by Monte Carlo simulation, which can provide tail risks. |
| Liability relative            | Models legal and quasi-liabilities             | Fund liabilities and invest excess assets for growth         | Penalty for not meeting liabilities highBanksDefined benefit pensionsInsurers | focus on the risk of having insufficient assets to pay obligations when due |
| Goals based                   | Models goals                                   | Achieve goals with specified required probabilities of success | Individual investors                                         | concerned with the risk of failing to achieve goals          |

## Asset Classification Rationale

1. Homogenous. Assets in the same class have similar attributes.
2. Mutually Exclusive. Not Overlapping.
3. Diversifying. Not highly expected correlated with other classes.
4. Preponderance of world investable wealth. Increase Expected Return for a given level of risks.
5. Asset classes selected for investment should have the capacity to **absorb a meaningful proportion of an investor’s portfolio.** 

Asset classes often include:

1. Global public equity
2. Global private equity: VC, LBO
3. Global fixed income
4. Real assets: includes assets that provide sensitivity to inflation, such as private real estate equity, private infrastructure, and commodities. Sometimes, global inflation-linked bonds are included as a real asset rather than fixed income because of their sensitivity to inflation.

( Inflation-Linked Bonds are a proxy for REAL interest rate, because inflation linked bonds' prices vary with inflation so if you remove the effect of inflation, you should end up with the real rate.

## Strategic Asset Allocation

$$ \max_w U=\mathbb{E}(r_p) - \frac{1}{2}A\sigma^2_p,\quad s.t. w^T\mathbb{1}=1, w\geq 0$$

And allocation between the portfolio and risk-free asset.

$$\max_w r_pw + r_f(1-w) - \frac{1}{2}A w^2\sigma_p^2$$

F.O.C. w.r.t. $w$, $r_p - r_f -w\cdot A \cdot \sigma_p^2 = 0$

$$w = \frac{1}{A}\frac{r_p - r_f}{\sigma_p^2}$$

### Two Dimensions

- Passive Management: **does not react** to changes in the investor’s CME or insights into individual investments; 
- Active Management **will respond** to changing CME

### Tactical asset allocation (TAA) and dynamic asset allocation (DAA) 

- TAA involves deliberate **short-term deviations** from the SAA; 
- DAA incorporates **deviations from the SAA that are motivated by longer-term valuation signals or economic views.**

### Rebalancing - make portfolio close to SAA

Two Approaches: 

- Calendar Rebalancing: on a certain period basis
- Percent-Range Rebalance (or Corridor)
    - Factors affecting the Optimal Corridor level
        1. Transaction Cost: high costs, high hurdle for rebalancing, high corridor. **Positive**
        2. Risk Tolerance: high tolerance, less sensitive to divergences from SAA, high corridor. 
        3. Risk Aversion. **Negative**
        4. Asset Class Correlation: highly correlated, high corridor. **Positive**
        5. Belief in Momentum: has momentum, high corridor. **Positive**
        6. Liquidity: Less liquidity, higher cost, high corridor. **Negative**

---

### Rebalance Frequency

- The narrower the corridor, the more frequent to rebalance
- More frequent monitor, the greater the precision
- More frequent rebalance, more cost

### Rebalance earns return, and the returns are generated from being short volatility

In the case of a portfolio consisting of a risky asset and a risk-free asset, the return to a rebalanced portfolio **can be replicated by** creating **a buy-and-hold position in the portfolio**, writing out-of the-money puts and calls on the risky asset, and investing the premiums in risk-free bonds. 

As the value of puts and calls is positively related to volatility, such a position is called being short volatility

## Principal of  Asset Allocation

### Asset-Only: MVO

$$ U = \mathbb{E}(R_m) - 0.005 \lambda \sigma^2_m $$

<img src="C:\Users\zh-zhaofy\AppData\Roaming\Typora\typora-user-images\image-20231017160825929.png" alt="image-20231017160825929" style="zoom:50%;" />

if the non-negative constraint is made, then there are points on the efficients frontier becoming unavailable. The efficient frontier becomes non-continuous. To approximate the standard deviation of those points, we use **adjacent corner portfolios**.

Reasoning: 

1. the adjacent corner portfolios (use D, L to approximate C) give more accurate results, than far away portfolios (A,F to approx C). 
2. one of the adjacent portfolio has the high Sharpe ratio. *The adjacent portfolios would artificially have a max Sharpe one*
3. assume the adjacent portfolios have correlation of 1. Then the variance of approximation is $\sigma_{approx}^2 = w^2 \sigma^2_D + (1-w)^2 \sigma_L^2 + 2\rho w(1-w)\sigma_D\sigma_L$, $\rho=1$, so $\sigma_{approx} = w\sigma_D + (1-w)\sigma_L$. As we assume the fully correlated situation, the s.d. is the upper limit / highest possible. *It would artificially within the range*

If there is a risk-free asset, then combine the **risk-free asset** with the **tangent portfolio**.

#### Pros and Cons of MVO

Pros: commonly, widely, easily, used

Cons:

1. The optimisation process make output **highly sensitive** to inputs
2. Outputs are **highly concentrated** 结果weights集中在某个资产上 *(apply constraints)*
3. MVO assume standard normal **dist**, so **not account for Skewness and Kurtosis** *(use other dist instead)*
4. **sources of risks may not be diversified** *(use factor-based model instead)*
5. no consider **liability or consumption stream** *(use ALM instead)*
6. MVO is a **single-period framework** that not consider trading / rebalance cost and tax *(use MCS instead)*

#### Overcome those Cons

- **Constraints**: incorporate real-world constraints, can restrict percentage of asset class. 
    - Non-negative constraint, percentage constraint, upper limits
    - **However**, if constraint is made, the problem is no longer optimisation of the original. 不再是原来的 Optimisation, 而是 optimisation with constraints.
- **Resample**: resampling uses **MCS** to estimate a large number of potential capital market assumptions, simulated frontiers are saved and averaged to get the **resampled frontier**.
    - As multi paths are simulated, the resampled frontier would be smoothed not in-continuous.
    - **However**, there might be 
        1. **concave bump** where expected return decreases as expected risk increases
        2. Risky asset allocations are **over-diversified**. (as there are simulations)
        3. inherit estimation errors. (有estimate by Monte Carlo 就有estimation errors)
        4. Lack of theoretical foundation.

