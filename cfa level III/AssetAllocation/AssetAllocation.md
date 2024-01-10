# Asset Allocation

## Economic Balance Sheet

Definition: includes (1) conventional assets and liabilities (in Accounting Statement) and (2) **extended portfolio assets** and liabilities (not appear in conventional B/S).

**Extended Portfolio Assets** includes: 

1. Human Capital (PV of Future Earnings), 
2. PV of Pension Income (Un-vested Benefits), 
    - P.S. $Pension\ Plan\ Ratio = \frac{Pension Asset}{Pensia Lia}$ ,  A/L
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

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-18%20at%2012.44.59.png" alt="Screenshot 2023-10-18 at 12.44.59" style="zoom:50%;" />

---

## Asset Allocation Approach

1. Asset Only - MVO
2. Liability-Relative - fund a lia
3. Goals-Based - address goal

| **Asset Allocation Approach** | **Relation to Economic Balance Sheet**         | **Typical Objective**                                        | **Typical Uses and Asset Owner Types**                       | Risk Objectives                                              |
| ----------------------------- | ---------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Asset only                    | Does not explicitly model liabilities or goals | Maximise Sharpe ratio for acceptable level of volatility     | Liabilities or goals not defined and/or simplicity is importantSome foundations, endowmentsSovereign wealth fundsIndividual investors | augmented by Monte Carlo simulation, which can provide tail risks. |
| Liability relative            | Models legal and quasi-liabilities             | Fund liabilities and invest excess assets for growth         | Penalty for not meeting liabilities highBanksDefined benefit pensionsInsurers | focus on the risk of having insufficient assets to pay obligations when due |
| Goals based                   | Models goals                                   | Achieve goals with specified required probabilities of success | Individual investors                                         | concerned with the risk of failing to achieve goals          |

### Asset Classification Rationale

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

---

## Strategic Asset Allocation

$$ \max_w U=\mathbb{E}(r_p) - \frac{1}{2}A\sigma^2_p,\quad s.t. w^T\mathbb{1}=1, w\geq 0$$

An allocation between the portfolio and risk-free asset.

$$\max_w r_pw + r_f(1-w) - \frac{1}{2}A w^2\sigma_p^2$$

F.O.C. w.r.t. $w$, 

$r_p - r_f -w\cdot A \cdot \sigma_p^2 = 0$

$$w = \frac{1}{A}\frac{r_p - r_f}{\sigma_p^2}$$

### Two Dimensions

- Passive Management: **does not react** to changes in the investor’s CME or insights into individual investments; 
- Active Management **will respond** to changing CME

### Tactical Asset Allocation (TAA) and Dynamic Asset Allocation (DAA) 

- TAA involves deliberate **short-term deviations** from the SAA;  短期 deviate from SAA
- DAA incorporates **deviations from the SAA that are motivated by longer-term valuation signals or economic views.** 长期 deviate from SAA

### Rebalancing - make portfolio close to SAA

Two Approaches: 

- Calendar Rebalancing: on a certain period basis
- Percent-Range Rebalance (or **Corridor**)
    - Factors affecting the **Optimal Corridor Level**
        1. Transaction Cost: high costs, high hurdle for rebalancing, high corridor. **Positive**
        2. Risk Tolerance: high tolerance, less sensitive to divergences from SAA, high corridor. **Positive**
        3. Risk Aversion. **Negative**
        4. Asset Class Correlation: highly correlated, high corridor. **Positive**
        5. Belief in Momentum: has momentum, high corridor. **Positive**
        6. Liquidity: Less liquidity, higher cost, high corridor. **Negative**
        
        - **Volatility**: **Positive or Negative**: 
            - Negative because The higher the volatility of the rest of the portfolio, excluding the asset class being considered, **the more likely a large divergence from the strategic asset allocation becomes**, which should point to a narrower optimal corridor, all else being equal.
            - Positive because higher vol, more transaction cost
            - 

### Rebalance Frequency

- The narrower the corridor, the more frequent to rebalance
- More frequent monitor, the greater the precision
- More frequent rebalance, more cost

### Rebalance earns return, and the returns are generated from being short volatility

In the case of a portfolio consisting of a risky asset and a risk-free asset, the return to a rebalanced portfolio **can be replicated by** creating **a buy-and-hold position in the portfolio**, writing out-of the-money puts and calls on the risky asset, and investing the premiums in risk-free bonds. 

As the value of puts and calls is positively related to volatility, such a position is called being short volatility

---

## Principal of  Asset Allocation

### Asset-Only: MVO

Characteristics: (1) sensitive to inputs 因为optimisation process makes that (2) might concentrate to certain class 会集中于某个asset class，而不是 disperse

$$ U = \mathbb{E}(R_m) - 0.005 \lambda \sigma^2_m $$

0.005 is bull shit for balancing the decimal, if the input ignore %. Use $U=\mathbb{E}(R_m) - \frac{1}{2}\lambda \sigma^2_m$ directly if input is with %。

0.005 = 1/2 /100 为了平衡 sigma^2 的量纲，输入时直接拿掉%才这么算，SB才这么算。

带小数点做input，直接用正常公式就行，不用0.005

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-18%20at%2012.43.55.png" alt="Screenshot 2023-10-18 at 12.43.55" style="zoom: 33%;" />

if the non-negative constraint is made, then there are points on the efficients frontier becoming unavailable. **The efficient frontier becomes non-continuous.** To approximate the standard deviation of those points, we use **adjacent corner portfolios**. 如果点在non-continuous的地方，用两边的adjacent点拟合

Reasoning: 

1. the adjacent corner portfolios (use D, L to approximate C) give more accurate results, than far away portfolios (A,F to approx C).  越近的点拟合越好
2. one of the adjacent portfolio has the high Sharpe ratio. *The adjacent portfolios would artificially have a max Sharpe one*
3. assume the adjacent portfolios have correlation of 1. Then the variance of approximation is $\sigma_{approx}^2 = w^2 \sigma^2_D + (1-w)^2 \sigma_L^2 + 2\rho w(1-w)\sigma_D\sigma_L$, $\rho=1$, so $\sigma_{approx} = w\sigma_D + (1-w)\sigma_L$. As we assume the fully correlated situation, the s.d. is the upper limit / highest possible. *It would artificially within the range*

If there is a risk-free asset, then combine the **risk-free asset** with the **tangent portfolio**.

#### Pros and Cons of MVO

Pros: commonly, widely, easily, used

Cons:

1. The optimisation process make output **highly sensitive** to inputs *(see 2)*
2. Outputs are **highly concentrated** 结果weights集中在某个资产上 *(1. apply constraints, 2. Resample, 3. Reverse Optimisation, 4. Black-Litterrman)*
3. MVO assume standard normal **dist**, so **not account for Skewness and Kurtosis** *(use other dist instead)*
4. **sources of risks may not be diversified** *(use factor-based model)*
5. no consider **liability or consumption stream** *(use ALM, Surplus MVO)*
6. MVO is a **single-period framework** that not consider trading / rebalance cost and tax *(use MCS instead)*

#### Overcome those Cons

##### Constraints

incorporate real-world constraints, can restrict percentage of asset class. 

- Non-negative constraint, percentage constraint, upper limits
- **However**, if constraint is made, the problem is **no longer optimisation** of the original. 不再是原来的 Optimisation, 而是 optimisation with constraints.

##### Resample

Resampling uses **MCS** to estimate a large number of potential capital market assumptions, simulated frontiers are saved and averaged to get the **resampled frontier**.

- As **multi paths** are simulated, the resampled frontier would be smoothed not in-continuous.
- **However**, there might be 
    1. **concave bump** where expected return decreases as expected risk increases
    2. Risky asset allocations are **over-diversified**. (as there are simulations)
    3. inherit estimation errors. (有estimate by Monte Carlo 就有estimation errors)
    4. Lack of theoretical foundation.

##### Reverse Optimisation

to cope with the problem that the expected return of expected return and standard deviation are not reliable. We use:

- Way 1:
    - Allocation Weights of Global Market Portfolio (Mkt Cap %) $\to$ by Reverse MVO, max Utility s.t. constraint $\to$ Implied Return
    - Input: Implied Return $\to$ by MVO output Weights
- Way 2: Reverse Beta
    - use the weights of asset class (or index) to form a **working version of the global market portfolio**;
    - use the **beta** of each asset relative to the global market portfolio.
    - use CAPM to infer expected return
    - run a MVO

##### Black-Litterman Model

view adjusted

- Like a weights average of $w\times r_{impliedReturn} + (1-w)\times View$, with uncertainty. (See my CQF Notes)
- 如果没有view，则为 implied return 即与 reverse opt结果相同

##### Non-normal Optimisation

As normal dist has only two parameter, mean and variance, the first and second moment, it do not account for further moments, such as

- Skewness - the asymmetric ~ity
- Kurtosis - the thickness of tail
- Other optimisation could be use to account for the non-normal return dist characteristics: (1) mean-semivariance opt, (2) mean-condition VaR  opt (3) mean-variance-skewness opt; (4) mean-var-skew-kurt opt. etc

##### Factor-Based Model

use investment factors. 

requires three sets of inputs: returns, risks (s.d.), correlations

- Pair-wise correlations with the market and with one another are generally low. Constructing factors in this manner removes most market exposure from the factors because of the short positions that offset long positions

##### Monte Carlo Simulation MCS

MCS is the complements of the MVO. MVO can only do with **single-period**. However, MCS can grapple with **a range of practical issues**:

- path dependence, and 
- taxes triggered by rebalance.

#### Liquidity Consideration

- Liquid Asset Classes: publicly listed equity and bond
- Less Liquid: direct real estate, infrastructure, and PE

To solve the illiquid problem, practical options include

1. exclude less liquid asset classes
2. model input by representing the highly diversified characteristics. such as use REITs instead of direct real estate.
3. ?? Include less liquid asset classes in the asset allocation decision and attempt to model the inputs to represent the specific risk characteristics associated with the likely implementation vehicles. 

---

### Liability-relative Asset Allocations  基本上只要涉及Lia 或者考虑过  lia 的就都要用 Lia-relative AA

The asset allocation with considering the investor's Liability.

#### Surplus Optimisation / Surplus MVO

We consider the **Surplus**. $SurplusReturn = \frac{\Delta A}{initial A} - \frac{\Delta L}{initial A}$. Note that the Liability is subtracted.

The objective function becomes the follow, where we use the surplus expected return and surplus variance instead.

$$ U_{LiaRelative} = \mathbb{E}(R_{surplus}) - 0.005 \lambda \sigma^2_{surplus} $$

##### ALM Efficient Frontier

Asset Liability Management (ALM) approach minimise the difference between assets and liabilities at each level of risks

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-18%20at%2013.01.17.png" alt="Screenshot 2023-10-18 at 13.01.17" style="zoom:50%;" />

##### Difference between Surplus & Asset-only

1. Expected Surplus & Variance of Surplus
2. ALM Efficient Frontier & Efficient Frontier
3. Minimum Surplus Variance Portfolio & Global Minimum Variance Portfolio
    - The Minimum Surplus Variance Portfolio might be negative
4. ALM MVO - minimise surplus variance & AO MVO - minimise portfolio variance.
5. $r_f$: ALM: corporate bond & AO: T-bill

##### Comparison

- The **most conservative mix** of **Surplus Efficient Frontier** consists mostly of **US corporate bond** 因为要考虑 -L，需要正收益的资产对冲。而the most conservative mix of Asset only is **Cash**
- 当risk 提升时，Surplus & Asset-only have **identical** **aggressive portfolio** (PE), 两者一样当aggressive时
- 当expected surplus提升到一定程度时，持有的bond将disappear，因为return不足以

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-18%20at%2013.19.26.png" alt="Screenshot 2023-10-18 at 13.19.26" style="zoom:25%;" />

#### Hedging / Return-seeking Portfolio Approach ( Two-portfolio Approach )

##### ***Basic***: A > L (hedge fully, or called True Hedge)

The Liability-relative Asset Allocation task is divided into two parts (1) **hedging portfolio**, (2) **return-seeking portfolio**.

- Hedging Portfolio is used to hedge **fully** Liability
- Return-Seeking Portfolio can be managed **independently** of the hedging portfolio (e.g. using MVO). 

##### ***Variant***: A < L (hedge partially)   - Aggressive or less conservative

Not fully hedge the Liability. **Partially** hedge the liability, and use the other to do AO-MVO

##### ***Variant of Variant***: An Alternative

use Asset to purchase derivative and use derivative to hedge the change of liability

#### Integrated Asset-Liability Approach

把 A & L 一起考虑。由于 Two Portfolio 适合用于 Over-funded pension，因为可以把大于 L 的部分拆开。

- Integratred Asset Lia Approach 可以应用于任何 A > < = L 的情况
- 逻辑倒序，但**对于 Under-funded Pension 就应该用 Integrated AL Approach** 。对于deficit pension plan 要 A L 一起考虑

- **Integrate or jointly optimise** asset and liability decision
- Has to potential to **improve the institution's surplus**
- Can be implemented in a **factor-based** model
- 因为Asset和Lia一起考虑，所以decision可能更加 紧密，也因此有可能 improve institution's surplus
- **可以考虑 multi-period**

#### Comparison

###### Surplus Optimisation & Two Portfolio

- **Surplus Optimisation** approach links assets and the present value of liabilities through a correlation coefficient. 用Correlation算Surplus Efficient Frontier, 而 **Two-portfolio Approch**不需要
- Two Portfolio (Basic) needs over-funded, (Variant) need not. 而Surplus Optimisation method 不考虑overfunded or not

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-18%20at%2016.58.10.png" alt="Screenshot 2023-10-18 at 16.58.10" style="zoom:67%;" />

与 lia一起考虑，即为非线性

---

### Goals-Based Asset Allocation

- Apply best to Individuals
- Allocate capital to **sub-portfolio**, **pick the highest probability**, use horizon-adjusted discount rate to discount the expected CF, obtain **lowest initially required capital** for each goal

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-18%20at%2022.36.55.png" alt="Screenshot 2023-10-18 at 22.36.55" style="zoom: 50%;" />

Drawback of Goal Based: (1) inefficient, (2) not consider correlation between asset class

### Heuristic and Other Approaches

- 120 - age
- 60 / 40 stock/bond (Noway Sovereign Fund)
- Endowment Model (Yale Model)
  - High allocation to non-tradition assets (alternatives)
  - Seek to earn illiquidty premium
  - Commitment to active management
  - long time horizon

### Risk Budgeting and Risk Parity

#### Risk Budgeting

The goal of risk budgeting is to **maximise return per unit of risk.** A risk budget identifies the total amount of risk and attributes risk to its constituent parts. An optimum risk budget allocates risk efficiently.

![_cgi-bin_mmwebwx-bin_webwxgetmsgimg](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/_cgi-bin_mmwebwx-bin_webwxgetmsgimg%253F%253F%2526MsgID%253D6268719542435932561%2526skey%253D%40crypt_df70b197_26e8fd2fe06b2899556fa708fc188e62%2526mmweb_appid%253Dwx_webfilehelper.png)

1. MCTR Goal: maximise the return per unit of risk 每承担一单位风险获得的收益
2. 投资 MCTR 最低的 portfolio
3. $\frac{r_A - r_f}{MCRT_A} > \frac{r_B - r_f}{MCRT_B}$, **risk budget is optimal** if the **ratio of excess return to MCTR is the same**

- **MCTR**, Marginal Contribution to Total Risks

    $MCTR = \frac{\partial \sigma_p}{\partial w_i} = \frac{cov(i,p)}{\sigma_p}$ the definition

    As, $\beta_{i,m} = \frac{cov(i,m)}{\sigma^2_m}$, so $\beta_{i,p} = \frac{cov(i,p)}{\sigma^2_p}$

    Thus, $MCTR = \sigma_p \beta_{i,p}$

- **Ratio of Excess Return to MCTR** = $\frac{ExpectedReturn - R_f}{MCTR}$

- **ACTR**, Absolute Contribution to Total Risks, how much it contributes to portfolio return volatility.

    $ACTR = MCTR \times \$ amount$, but in the CFA notes,

    $ACTR = MCTR \times w_i = w_i \beta_i \sigma_p = \frac{1}{n}\sigma_p$

    multiply $\sigma_p$ from the both side, $w_i \beta_i \sigma^2_p =\frac{1}{n}\sigma_p^2 = w_i \ cov(i,p)$

#### Risk Parity

每个资产给组合的风险贡献 $\frac{1}{n}\sigma_p$

Each asset (asset class or risk factor) should **contribute equally** to the total risk of the portfolio for a portfolio to be well **diversified**. 每个asset class贡献同样的资产，那么比如有 bond, equity, commodity, 因为bond的风险小，那么portfolio中配置的就bond就更多，这样可以达到1/3 portfolio total risk

- Pros and Cons

  - **Pros**: risks are diversified

  - **Cons**: as we include more bonds by the risk parity, risks are diversified, but expected returns are scarified.

  - **Cons**: Dependent on the ability to use extremely large amounts of leverage at low borrow rates 


---

## Real-World Constraint

### Assets Size

Large Asst: (1) illiquidity, (2) make small-cap stock price wildly fluctuate, (3) reluctant organisational hierarchies.

### Liquidity

Life-Insurance has long time horizon, so less liquidity demand. Bank has higher liquidity demand.

### Taxable Investors

$\sigma_{at} = \sigma_{pt} (1-t)$, at-after-tax, pt-pre-tax by $r_{at} = (1-t)r_{pr}$

#### Rebalance Corridor

tax 大 $\to$ cost 大 $\to$ Corridor 大, so

$range_{at} = \frac{range_{pt}}{1-t}$

因为 after tax range 大，所以 除以 1-t

#### Tax-Deferred Account (TDA)

$v_{at} = v_{pt} (1-t)$

### Deal with Behavioural Bias

#### Identify Anomalies

1. Loss-aversion bias: **Goal Based**
2. Illusion of Control (cognitive bias): **global portfolio performance**
3. Mental Accounting: **Goal Based**
4. Representative / Recency（representative problem 的三个层次：（1）过去好的投资，将来也是好的；（2）好公司就是好的投资；（3）只看了短期收益就认为是好的基金经理）: **Governance**
5. Framing Bias: **多角度看。看return同时看risk，Sharpe ratio， max drawdown等**
6. Availability Bias (买的是最先想到的股票): **global portfolio**

---

Pension Funds

影响 pension fund 的因素

1. Average Participant Age 越高，离把pension折现提出的时间越短，折现的越少，则 lia 越大
2. Salary Growth 收入越多，Fund Lia越大 commitment
3. Short term rate increase，Pension Fund 大多数是长周期，不是short term，
