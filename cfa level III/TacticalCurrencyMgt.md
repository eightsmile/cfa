### Tactical Currency Management

- Domestic Currency would appreciate if
    1. Long-run equilibrium **real exchange rate** increases
    2. Real and nominal **interest rate** increase
    3. Expected foreign inflation increase (so foreign currency depreciates)
    4. Foreign risks premium increase 

### Technical Analysis

- Golden Cross, Dead Cross
- Overbought or Oversold
- Support and Resistance levels cluster
    - Price gets sticky, gov control in the background. But, Once certain price points breached, the price would accelerate.

### Carry Trade

#### UIP & CIP 

UIP states 如果F国的利率高，那么投资者会把钱存入F国挣高收益率。但是F国远期的汇率一定会降，去保证UIP holds

In sum, **country with high rate of return would have forward discount 远期比现在低** , we invest in high return one, (, equivalent to invest in forward discount one)

Carry Trade can make money iff the UIP is violated 只有违背 UIP 才有 carry trade 赚钱的机会

$1+r_d = \frac{1+r_f}{S}F$ , where $F$ or $S$ is $(\frac{d}{f})$. Base Currency is the foreign currency, 我们主要以foreign currency 为参考，if F 提升，意味着 d > f，意味着外币升值

$\frac{F}{S} = \frac{1+r_d}{1+r_f}$

- on a longer-term average, the return on an unhedged foreign-currency asset investment will be the same as a domestic-currency investment.
- The yield spread advantage for the high-yielding currency (the right side of the equation) will, on average, be matched by the depreciation of the high-yield currency.

#### **Arbitrage**

if $\frac{F}{S} > \frac{1+r_d}{1+r_f}$, $\frac{F}{S} ({1+r_f})> {1+r_d}$, then borrow $r_d$ as its is low cost, and invest in $f$. The arbitrage return would be $\frac{F}{S} ({1+r_f}) - ({1+r_d})$

if $\frac{F}{S} < \frac{1+r_d}{1+r_f}$, $\frac{S}{F} ({1+r_d})> {1+r_f}$, then borrow $r_d$ as its is low cost, and invest in $f$, then the arbitarge return would be $\frac{S}{F} ({1+r_d}) -( {1+r_f})$,

remember always let F/S or S/F be in the larger side.

#### Returns from Carry Trade

**However, in reality**, high-yield countries often see their currencies appreciate, not depreciate, for extended periods of time. Reasoning:

1. Captial Inflow
1. yield difference

#### Forward Rate Bias & Carry Trade

Carry Trade 的逻辑，借入 $r$ 小的，投资 $r$ 大的，挣$\Delta r$ 

- **Forward Bias**: **buying** currencies selling at a forward discount ($F<S$, 即高利率货币), and **selling** currencies trading at a forward premium.

  $F/S = \frac{1+r_d}{1+r_f}$ (, where (d/f) the base is f, , if $r_f > r_d$, then <=> $F<S$, that is forward discount, then borrow $d$ and invest in $f$. So, if forward discount, then invest in the base $f$.

- Connection between Carry Trade & Forward Bias. Forward Rate Bias, 低利率的货币，远期是溢价的，所以卖。高利率货币，远期折价，所以买  

### Volatility Trading

#### **Straddle** <- bet on volatility

By **Delta Hedging**, we can get a **delta-neutral position**. Straddle is a long call and a long put ATM.

Straddle is delta Neutral, because it is symmetric at the current stock price.

![Screenshot 2023-11-07 at 13.02.53](/Users/mie/Library/Application Support/typora-user-images/Screenshot 2023-11-07 at 13.02.53.png)![Screenshot 2023-11-07 at 13.02.53](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-07%20at%2013.02.53.png)

#### **Strangle** 

Long Call and long put OTM, but as options are OTM, so lower premium 期权费便宜.

The Green Curve is Straddle, Yellow Curve is Strangle, in the below figure.

![Screenshot 2023-11-07 at 13.05.09](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-07%20at%2013.05.09.png)

Pros: lower premium fees

Cons: lower returns

However, strangle could have a trading position that has net Vega and delta exposures (可以被做成不是围绕 current stock price 中心对称的，如向左和向右平移通过调整 call & put 的 strike price，这样可以结合 traders 对涨和跌的 expectations)

![Screenshot 2023-11-07 at 13.13.10](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-07%20at%2013.13.10.png)

Discontinue the Carry Trade 意味着 终止 Carry Trade
