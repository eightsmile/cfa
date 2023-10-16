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