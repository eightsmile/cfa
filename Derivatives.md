## Derivatives

### Forward Contract

If you are long a futures or forward contract and the price of the underlying has risen, the value of a futures contract is most likely lower than that of the equivalent forward contract.

Because futures contracts are marked to market daily, profits are paid out and the value is reset to zero. As a result if you are long a contract and the price has risen, the forward contract will likely have a higher value than the futures contract.

$$FP=S_0(1+r_f)^T + CarryingCost-Carrying Benefits$$

At the interception, the value of forward should be zero.

#### Cash-and-Carry Arbitrage

- $FP > S_0 \times (1+r_f)^T$ 
- Short Forwards, Long Underlying.

#### Reverse Cash-and-Carry Arbitrage

- $FP < S_0 \times (1+r_f)^T$ 
- Long Forwards, Short Underlying.
- long forward 的是 reverse 的

#### Pricing and Valuation

|                                  | Price, t=0                                                   | Value, t=t 折现到t时点的值。t可以=0<br />当然F的钱比 underlying小，F才有value |
| -------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| T-bill Forwards                  | $FP=S_0\times (1+r_f)^T$                                     | $V=S_t - \frac{FP}{(1+r_f)^{T-t}}$                           |
| Forward on Dividend-Paying Stock | $FP=(S_0-PVD_0)\times (1+r_f)^T$                             | $V=S_t - PVD_t-\frac{FP}{(1+r_f)^{T-t}}$                     |
| Forward on Equity Index          | $FP=S_0\times e^{(r_c - \delta^c)\times T}$  $r^c = ln(1+r_f)$ | $V=S_t\times e^{-\delta^c\times (T-t)} - FP\times e^{-r^c\times (T-t)} $ $V=\frac{S_t}{e^{\delta^c\times (T-t)}} - \frac{FP}{e^{r^c\times (T-t)} } $ |
| Forward on Coupon Bond           | $FP=(S_0-PV.C_0)\times (1+r_f)^T$                            | $V = (S_t - PV.C_t)-\frac{FP}{(1+r_f)^{T-t}}$                |

### Forward Rate Agreements - FRAs

FRA transaction 不需要deposite，只swap net的部分就行

Long - Borrow at the Forward Rate in the Future.`

在 $t=0$ 时刻签订，在 $t=1$ 时刻可以以 FRA 的 rate 借钱到 $t=2$ 时刻。所以借钱的区间为 $1\to2$, 还需将他们折成PV到0时刻。

#### Euribor Counterparty

因为 Euribor 是一种浮动汇率，相当于Libor，所以 long Euribor 等价于 需要long float

An FRA has two **counterparties**, a **fixed-rate receiver / float-rate payer** that is short Euribor and a **floating-rate receiver / fixed-rate payer** that is long Euribor.

### T-bond Futures 

Daily Settlement

$$FP_{standard} = FP_i\times \frac{1}{CF_i}$$

用 CF - Conversion Factor 把持有的乱七八糟的债券，等价于 标准的 用于交割的 债券。

CF 只作用于 clean price的，如果是 dirty 的要把 accrual interest 减去再除以 CF。（相反，compound只作用于dirty，因为更精准）

$$Full\ Price = Clean\ Price + Accrual\ Interest$$

$$V_{Full} =\underbrace{ FP^{clean}_{standard}\times CF }_{FP_i}+Accrual\ Interest$$

#### Non-Arbitrage for T-Bond

- $V$ here are the future value.
- Hold the Future: $V = FP_{std} \times CF  + AI -$
- Hold the Bond: $V = (S_{clean} + AI_0 )(1+r_f)^T - FVC$

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

#### Derivation of the T-bond Future

- 期货

  ​	We use $ S_0(1+r_f)^T + CarryingCost - Carrying Benefit$ to get the Equation (1)

  ​	$$V^T_{full} = V^T_{clean} + AI^T = FP_{std}\times CF +AI^T$$

- Compound 现货 (by $S_{clean} + Accrual\ Interest - PVC $) 此时持有会有PV of Coupon

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

外币固定换固定

见 practice derivatives最后6题。**0.008396**为3个月前，刚开立swap时算出的fixed rate，三个月后虽然MRR变了，但是fixed rate不变，因此swap会有价值。

#### Equity Swap

equity index return <=> float rate

$EquityReturn = \frac{Index_1-Index_0}{Index_0}$

$$FloatRate = MRR$$

$Value = EquityReturn \times NotionalAmount - FloatRate \times NotionalAmount $

(1) PV of FCF (2) Current Index Price  (1) - (2)

### Options

#### Risk Neutral Probability

$$\pi = \frac{1+r-d}{u-d}$$

$$C_0 = \frac{1}{(1+r_f)^T}\mathbb{E}^{\pi}(C)$$

Take Expectation by **Risk-Neutral Probability,**

Discount by **Risk-free Rate.**

#### Delta Hedging

$$\Delta = \frac{V^+-V^-}{S^+-S^-}$$

For a call, replicate / hedge with no options could be made:

- Long Stock: $\Delta \times S_0$
- Borrow Money: $\frac{\Delta \times S_0}{1+r_f}$

The above action is equivalent to: Sell (write) a Call

#### Option on Future Contract

$S_0$ is the current price of future.

#### Option on Interest Rate

For call,

$$Payoff = \max(0,r_{reference} - r_{exercise})\times Notional Amount$$

$$Payoff_{t-1} = Payoff_t \times \bigg[\frac{1}{2}\times r_{ref}^{up}+\frac{1}{2}\times r_{ref}^{down}\bigg]$$

In the two-period binomial model, **Node 0** represents the current state of the underlying instrument and the spot rate is the current market rate for the instrument. Therefore, the value of the underlying instrument at Node 0 is considered to be the **spot rate** because it represents the current market value of the instrument. 

See this one below,

<img src="/Users/mie/Desktop/Screenshot 2023-04-24 at 17.00.00.png" alt="Screenshot 2023-04-24 at 17.00.00" style="zoom:33%;" />

#### BSM

$$C = S_0\times N(d_1) - Xe^{-r_fT}\times N(d_2)$$

$$d_1 = \frac{ln(S_0/X) + (r_f +\frac{1}{2}\sigma^2) T}{\sigma \sqrt{T}}$$

$$d_2 = d_1 - \sigma \times \sqrt{T}$$

Note that BSM states the continuously compound return is normally distributed, not the annual return.

"using out-of-money to hedge" means buying out-of-money put option at low strike price 
"using out-of-money to long" means buying out-of-money call option at high strike price

Vega is high when option is **at the money**.

Theta is normally negative. The speed of the option value decline increases, however, as time to expiration decreases. 

##### BSM Assumption

1. The volatility of the return on the underlying is known and constant. 恒定的constant vol 

    **volatility can be predicted with certainty**

2. The model includes the assumption that arbitrage opportunities do not exist: "No arbitrage opportunities are available in the marketplace." 市场无 arbitrage op

3. The model is based on the assumption that prices do not move in discrete amounts as described in this statement. The reading states: "**Geometric Brownian motion** implies **continuous** prices, meaning that the price of the **underlying instrument does not jump from one value to another; rather, it moves smoothly from value to value.**" 连续的，**price do not jump** 因为 price GBM，所以 rate BM iid normal

    - The underlying follows a statistical process called geometric Brownian motion, which implies that the **continuously compounded return is normally distributed**.
    - Geometric Brownian motion implies continuous prices, meaning that the price of underlying instrument does not jump from one value to another; rather, it moves smoothly from value to value.

4. The options are **European-style**, meaning that early exercise is not allowed.

5. The **continuously compounded** risk-free interest rate is known and constant; borrowing and lending is allowed at the risk-free rate.

6. If the underlying instrument pays a yield, it is expressed as a continuous known and constant yield at an **annualised rate**.

7. **Liquidity of trading. Short selling is permutable. No friction and trading cost. Leverage at continuously compound risk free rate is ok.**

#### Black Model - Options on Futures

Black’s model to value a call option on a futures contract is 

$$c = e^{–rT}[F_0(T)\times N(d_1) – X\times N(d_2)]$$

#### Swaption

A swaption is an option to enter into a swap for interest. 

- Payer Swaption is an option to enter into a swap as the **fixed-rate payer.**
    - Pay fixed, 所以interest rate提升，swaption value more.
- A receiver swaption is an option to enter into a swap as the **fixed-rate receiver (the floating-rate payer)**.
    - receive fixed，pay float，所以interest rate提升，swaption value less.
