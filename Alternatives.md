## Alternatives

### Real Estate

#### Valuation Approach 

- Cost Approach, Property Value = Land + Building Replacement Cost - TotalDepreciation - Obsolescence - Deterioration
- Sales Comparison
- Income Approach
    - Direct Capitalisation 用第一个月的  NOI / r-g
    - DCF

#### Loan Amount

- Loan to Value ratio $=\frac{Loan}{Value}$
- debt service coverage ratio $=\frac{NOI}{Debt Interest Expense}$

用以上两个反推

#### Others

- Shopping carters - require more management, such as tenant mix and promotion
    - A shopping centres is a type of **retail property**. A percentage lease is a unique aspect of many retail leases, which requires the tenant to pay additional rent once its sales reach a certain level. The lease will typically specify a “minimum rent” that must be paid regardless of the tenant’s sales. Percentage rent may be paid by the tenant once the tenant’s sales reach a certain level or breakpoint.

### PE Investment - VC & LBOs

#### Characteristics

| **Venture Capital**                                          | **Buyout**                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Primarily equity funded. Use of leverage is rare and very limited. | Extensive use of leverage consisting of a large proportion of senior debt and a significant layer of junior and/or mezzanine debt. |
| Returns of investment portfolios are generally characterized by very high returns from a limited number of highly successful investments and a significant number of write-offs from low performing investments or failures. | Returns of investment portfolios are generally characterized by lower variance across returns from underlying investments. Bankruptcies are rare events. |
| Venture capital firm monitors achievement of milestones defined in business plan and growth management. | Buyout firm monitors cash flow management and strategic and business planning. |
| Expanding capital requirement if in the growth phase.        | Low working capital requirement.                             |
| Assessment of risk is difficult because of new technologies, new markets, and lack of operating history. | Risk is measurable (e.g., mature businesses, long operating history, etc.). |

#### Calculations

- TVPI, Total Value to Paid-in Capital， $ TVPI=\frac{Distributed + UnDistributed}{Cumulative InvestedCapital}$
- DPI, Distributed to Paid-in Capital， $DPI=\frac{Cumulative Distributions}{Cumulated InvestedCapital}$ - 分配出去的 - **Realised Return**
- RVPI, Residual Value to Paid-in Capital, $RVPI = \frac{NAV(afterDistribution)}{Cumulative Invested Capital}$ - **Unrealised Return**
- TVPI = DPI + RVPI
- High Water Mark - Carry Interest 跟此前最高的比的 diff * rate

### Commodities

#### Types

- Contango: Upward
- backward: future price downward - theory of storage

#### Theories

- **Insurance theory** predicts that the futures price has to be lower than the current spot price as a form of payment or remuneration to the speculator who takes on the price risk and provides price insurance to the commodity seller.
- **Theory of Storage**:
    - When available inventory levels **(supply) of the commodity are high**, the buyers of that commodity keep their levels to the minimum. **Futures prices tend to be in  contango**. **The volatility of spot and futures prices tend to be low, and equal.**
    - When available inventory levels of the commodity are low (Scarcity), buyers of the commodity tend to stock up on the good. **Futures prices tend to be in backwardation.** **The volatility of nearby futures prices are raised** compared with the volatility of long term futures prices.
    - Storage Cost 大 -> future price 大
    - Convenience Yield 大 -> future price 小
- **Hedging Pressure Hypothesis**: hedging pressure occurs when both producers and consumers seek to protect themselves from commodity market price volatility by entering into price hedges to stabilise their projected profits and cash flows. **If consumers are more interested in hedging than producers are, the futures price will exceed the spot price.**
    - 买多 contango
    - 卖short多 backwardation

#### Calculation

- Total Return = Price Return + Roll Return + Collateral Return
    -  Roll return 期货合同到期后续作新的时，挣的钱 $=\frac{F_0 - F_1}{F_0}$. $F_0$ 为到期的，$F_1$ 为续作的。
    -  $Roll return = \frac{\text{Near-term futures contract closing price} −\text{ Farther-term futures contract closing price}}{\text{Near-term futures contract closing price}}$
- Calendar Spread = Near Future - Long Future
    - A **positive calendar spread i**s associated with futures markets that are in **backwardation**, whereas a negative calendar spread is associated with futures markets that are in contango. Lumber futures have successively higher prices and are in contango.
- Basis = Near Spread - Spot