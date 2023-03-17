### OAS

把 embedded option bond 的现金流折成 without option bond 的spread

$$ PV_{BondWithoutOption} = \frac{CF_1}{1+r+OAS} +\frac{CF_2}{(1+r + OAS)^2}+... +\frac{CF_n}{(1+r+OAS)^n}$$

$$PV_{BondWithoutOption} \pm  V_{option} = PV_{BondEmbedded Option}$$

换句话说，OAS 把 $PV_{BondWithoutOption} $ 折成了$PV_{BondEmbedded Option}$. 

- OAS 大，则把 Cash Flow折成的PV更小，那么就意味着，Value of Option更大。
- 对于 call:  $V_{CallableBond} = V_{Bond} - V_{call}$
- 对于 put: $V_{PutableBond} = V_{Bond}+V_{put}$

所以，如果Volatility of Interest增大，Value of Option增大。则 $V_{CallableBond}$ 变小，所以OAS变大。$V_{PutableBond}$ 变大，所以OAS变小。

### Durations

#### 1. Effective Duration

$$ ED = \frac{ P_+ - P_- }{2\times\Delta curve \times P_0} $$

- Assuming **parallel shifts** in the benchmark yield curve.
- Effective durations are normally calculated by averaging the changes resulting from shifting the benchmark yield curve up and down by the same amount. 

- This calculation works well for option-free bonds, but the results can **be misleading in the presence of embedded options**.
- The price sensitivity of bonds with embedded options is not symmetrical to positive and negative changes in interest rates of the same magnitude.

#### 2. One-side Duration

- One-side duration is better at capturing the interest rate sensitivity of a callable or putable bond than the (two-sided) effective durations, particularly when the embedded option is near the money.

#### 3. Key-rate Duration

- **Key rate durations** reflect the sensitivity of the bond’s price to changes in specific maturities on the benchmark yield curve.
- help portfolio managers and risk managers **identify the “shaping risk” for bonds**—that is, the bond’s sensitivity to **changes in the shape** of the yield curve (e.g., **steepening and flattening**).

### Convertible Bond

- $\text{Conversion Price} = \frac{\text{Issue Price}}{\text{Conversion Ratio}}$
- $\text{Market Conversion Pirce} = \frac{Bond's Mkt Price}{Conversion Ratio}$, 现在就以 mkt price 买入bond，就转换成 stock 的 每股的价格。
- $\text{Premium} = \text{Mkt Conversion Pirce} - \text{Share Price}$， 用convertible bond转 stock比stock成本贵的部分。
- $\text{Conversion Premium Ratio} = \frac{Premium}{Share Price}$， 跟share price 比
- $\text{Conversion Value} = \text{Share Price} \times \text{Conversion Ratio}$

### CDS

Rationale: 

- Buy Credit deteriorated assets/bonds. 买风险变大的
- Sell Credit Enhanced ones. 卖风险减少的
- Credit Deterioration Signals: Leverage Increase. 
- Large CDS spread, large risks.