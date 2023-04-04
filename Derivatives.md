## Derivatives

### Forward Contract

$$FP=S_0(1+r_f)^T + CarryingCost-Carrying Benefits$$

#### Cash-and-Carry Arbitrage

- $FP > S_0 \times (1+r_f)^T$ 
- Short Forwards, Long Underlying.

#### Reverse Cash-and-Carry Arbitrage

- $FP < S_0 \times (1+r_f)^T$ 
- Long Forwards, Short Underlying.

#### Pricing and Valuation

|                                  | Price                                                        | Value                                                        |
| -------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| T-bill Forwards                  | $FP=S_0\times (1+r_f)^T$                                     | $V=S_t - \frac{FP}{(1+r_f)^{T-t}}$                           |
| Forward on Dividend-Paying Stock | $FP=(S_0-PVD_0)\times (1+r_f)^T$                             | $V=S_t - PVD_t-\frac{FP}{(1+r_f)^{T-t}}$                     |
| Forward on Equity Index          | $FP=S_0\times e^{(r_c - \delta^c)\times T}$  $r^c = ln(1+r_f)$ | $V=S_t\times e^{-\delta^c\times (T-t)} - FP\times e^{-r^c\times (T-t)} $ $V=\frac{S_t}{e^{\delta^c\times (T-t)}} - \frac{FP}{e^{r^c\times (T-t)} } $ |
| Forward on Coupon Bond           | $FP=(S_0-PVC_0)\times (1+r_f)^T$                             | $V = (S_t - PVC_t)-\frac{FP}{(1+r_f)^{T-t}}$                 |

### Forward Rate Agreements - FRAs

Long - Borrow at the Forward Rate in the Future.`

在 $t=0$ 时刻签订，在 $t=1$ 时刻可以以 FRA 的 rate 借钱到 $t=2$ 时刻。所以借钱的区间为 $1\to2$, 还需将他们折成PV到0时刻。

### T-bond Futures 

Daily Settlement

$$FP_{standard} = FP_i\times \frac{1}{CF_i}$$

用CF - Conversion Factor 把持有的乱七八糟的债券，等价于 标准的 用于交割的 债券。

$$Full\ Price = Clean\ Price + Accruial\ Interest$$

$$V_{Full} =\underbrace{ FP^{clean}_{standard}\times CF }_{FP_i}+Accrual\ Interest$$

#### Non-Arbitrage for T-Bond

- $V$ here are the future value.
- Hold the Future: $V = FP_{std} \times CF  + AI$
- Hold the Bond: $V = (S_{clearn} + AI_0 )(1+r_f)^T - FVC$

Bond price is usually quoted as **clean** price.

#### Non-Arbitrage Quote Price for T-bond Future

$$ PV_{full}\times (1+r_f)^T - AI^T = FP_{std}\times CF $$

$$ (PV_{clean}+AI^0)\times (1+r_f)^T - AI^T = FP_{std}\times CF $$

- Both LHS and RHS are the future value.
- LHS is the Future Value of the Clean Price.
    - Step 0. Get the PV(dirty price).
    - Step 1. Compound the PV(dirty price) to FV(dirty price). We always want to compound the dirty price, as it is more accurate carrying all the cash flow.
    - Step 2. Deduct the $AI^T$ to get the FV(clean price), as bond is always quoted at clean price.
- RHS is the $FP_i$, is the future price.

#### Derivation

- 期货

  ​	We use $ S_0(1+r_f)^T + CarryingCost - Carrying Benefit$ to get the Equation (1)

  ​	$$V^T_{full} = V^T_{clean} + AI^T = FP_{std}\times CF +AI^T$$

- Compound 现货 (by $S_{clean} + Accrual\ Interest - PVC $)

​			$$ (S^0_{clean} + AI^{t=0})(1+r_f)^T - FVC $$

- Let them equal, 让期货的成本 = 现货的成本，反推出FP.std

​			$$  FP_{std}\times CF +AI^T  = (S^0_{clean} + AI^0)(1+r_f)^T - FVC $$

​			$$ FP_{std} = \frac{1}{CF}\bigg(  (S^0_{clean} + AI^0)(1+r_f)^T - FVC-AI^T  \bigg) $$

### SWAP

#### Plain Vanilla Swap

$$1 = C\times B_1 + C\times B_2 + ... +(1+C)B_T$$

$$C = \frac{1-B_T}{B_1+B_2 + ...+B_T}$$

#### PV of Fixed/Floating Coupon Bond

- $PV_{fixed}=C\times B_1 + ... + C\times (1+B_T)$
- $PV_{Float} = \frac{1+f}{1+r} = (1+f_1)\times B_1$
- $Diff = PV_{fixed} - PB_{float}$

#### Currency Swap

E.G. Fixed USD <=> Fixed CNY

- USD: $C_{\$} = \frac{1-B_4}{B_1+B_2+B_3+B_4}$, then annualise it.
- CNY: $C_{cny} = \frac{1-B'_4}{B'_1+B'_2+B'_3+B'_4}$

**Valuation of the Currency Swap**

$$V_t = PV_{inflow}^{CNY} - PV^\$_{outflow}$$

-   $PV^\$_{outflow}= \bigg( \frac{3\%}{4}\times \big(B_1+B_2 +B_3+B_4\big)+(1+B_4) \bigg)\times \$1$
-  $PV_{inflow}^{CNY} = \bigg( \frac{6\%}{4}\times \big(B'_1+B'_2 +B'_3+B'_4\big)+(1+B'_4) \bigg) \times \frac{CNY}{\$}_{t=0} \times \frac{\$}{CNY}_{t=T}$
