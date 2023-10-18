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

![Screenshot 2023-10-18 at 12.44.59](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-18%20at%2012.44.59.png)

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

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-18%20at%2012.43.55.png" alt="Screenshot 2023-10-18 at 12.43.55" style="zoom: 33%;" />

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

##### Constraints

incorporate real-world constraints, can restrict percentage of asset class. 

- Non-negative constraint, percentage constraint, upper limits
- **However**, if constraint is made, the problem is no longer optimisation of the original. 不再是原来的 Optimisation, 而是 optimisation with constraints.

##### Resample

resampling uses **MCS** to estimate a large number of potential capital market assumptions, simulated frontiers are saved and averaged to get the **resampled frontier**.

- As multi paths are simulated, the resampled frontier would be smoothed not in-continuous.
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

### Liability-relative Asset Allocations 

The asset allocation with considering the investor's Liability.

#### Surplus Optimisation

We consider the **Surplus**. $SurplusReturn = \frac{\Delta A}{initial A} - \frac{\Delta L}{initial A}$. Note that the Liability is subtracted.

The objective function becomes the follow, where we use the surplus expected return and surplus variance instead.

$$ U_{LiaRelative} = \mathbb{E}(R_{surplus}) - 0.005 \lambda \sigma^2_{surplus} $$

##### ALM Efficient Frontier

Asset Liability Management (ALM) approach minimise the difference between assets and liabilities at each level of risks

![Screenshot 2023-10-18 at 13.01.17](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-18%20at%2013.01.17.png)

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

##### Hedging / Return-seeking Portfolio Approach ( Two-portfolio Approach )

###### ***Basic***: A > L (hedge fully, or called True Hedge)

The Liability-relative Asset Allocation task is divided into two parts (1) **hedging portfolio**, (2) **return-seeking portfolio**.

- Hedging Portfolio is used to hedge **fully** Liability
- Return-Seeking Portfolio can be managed **independently** of the hedging portfolio (e.g. using MVO). 

###### ***Variant***: A < L (hedge partially)   - Aggressive or less conservative

Not fully hedge the Liability. **Partially** hedge the liability, and use the other to do AO-MVO

##### ***Variant of Variant***: An Alternative

use Asset to purchase derivative and use derivative to hedge the change of liability

##### Integrated Asset-Liability Approach (might be better)

- **Integrate or jointly optimise** asset and liability decision.
- Has to potential to **improve the institution's surplus**.
- Can be implemented in a **factor-based** model

##### Comparison

###### Surplus Optimisation & Two Portfolio

- **Surplus Optimisation** approach links assets and the present value of liabilities through a correlation coefficient. 用Correlation算Surplus Efficient Frontier, 而 **Two-portfolio Approch**不需要
- Two Portfolio (Basic) needs over-funded, (Variant) need not. 而Surplus Optimisation method 不考虑overfunded or not

![Screenshot 2023-10-18 at 16.58.10](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-18%20at%2016.58.10.png)

### Goals-Based Asset Allocation

### Heuristic and Other Approaches

- 120 - age
- 60/40 stock/bond
- Endowment Model (Yale Model)
  - High allocation to non-tradition assets (alternatives)
  - Seek to earn illiquidty premium
  - Commitment to active management
  - long time horizon

### Risk Budgeting and Risk Parity

#### Risk Parity 

每个资产给组合的风险贡献 $\frac{1}{n}\sigma_p$

#### Risk Budgeting

每承担1单位的风险，获得的最高风险补偿/收益 
