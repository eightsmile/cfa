# Derivatives & Exchange

## Derivatives 

### Strategies

#### 1. Covered Call Strategy (long Stock, short Call)

i.e.  $S=2000$

- **Yield Enhancement** 为长期持有, $K = 3000$

  write a OTM call option.

- **Reduce a Position** 为了卖, $K=1800$

- **Target Price Realisation** 近期到期 combine of above two $K=2500$

As the covered call strategy is (long S, short Call)

$Profit = \underbrace{(S_T - S_0)}_{long \ S} + \underbrace{ C - \max(S_T-K,0)}_{Long\ Call}$

- if $S_T > K$, then, $Profit = K - S_0 + C$     (行权)
- if $S_T \leq K$, then, $Profit = S_T -S_0 + C$      (不行权)
- if Break-even,  $S_T - S_0 + C =0$
- if max loss, $S_T = 0$, $Loss (Profit) = -S_0 + C$
- if max gain, $S_T > X$, $Gain (Profit) = K - S_0 + C$

![ ](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-29%20at%2021.11.26.png)

#### 2. Protected Put (long Stock, long Put)

$Profit = \underbrace{(S_T - S_0)}_{longStock} + \underbrace{\max(K - S_T,0) - P}_{LongPut}$

若用分段函数探讨，

![Screenshot 2023-10-30 at 13.08.38](/Users/mie/Library/Application Support/typora-user-images/Screenshot 2023-10-30 at 13.08.38.png)

但是更简单的办法：

![Screenshot 2023-10-30 at 12.54.26](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-30%20at%2012.54.26.png)

Protected Put is a hedge, but is not a perfect hedge, because there is still the maximum loss part.

#### 3. Collar (long Stock, long Put, short Call, options are all out-the-money OTM)

$Profit = \underbrace{(S_T - S_0)}_{LongStock} + \underbrace{C - \max(S_T-K)}_{Short Call} + \underbrace{\max(K-S_T,0)-P}_{LongPut}$

![Screenshot 2023-10-30 at 13.05.19](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-30%20at%2013.05.19.png)

![Screenshot 2023-10-30 at 13.07.11](/Users/mie/Library/Application Support/typora-user-images/Screenshot 2023-10-30 at 13.07.11.png)

##### Put-Call Parity

- Case 1:

    $C+ \frac{K}{1+r} = P + S$

    Fiduciary Call = Protective Put

- Case 2:

    $S-C = \frac{K}{1+r} -P $

    Covered Call = Cash Secured Put

#### 4. Vertical Arbitrage (different exercise price X/K) 

- Bull Spread: 
    - long $Call_L$ short $Call_H$
    - Short $Put_H$ long $Put_L$
- Bear Spread: 
    - long $Put_H$ short $Put_L$
    - Short $Call_L$ long $Call_H$

![Screenshot 2023-10-30 at 13.32.52](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-30%20at%2013.32.52.png)

P.S. 如果 options 是 out-of-money，那么是 期权费之差。如果 option 是 in-the-money， 那么还要考虑行权价格的差 + 期权费。总之，现推导。

#### 5. Horizontal Arbitrage (different Expire Date)

- Long Calendar: 买长期 long $Call_{longer}$ short $Call_{shorter}$
- Short Calendar: 买短期 long  $Call_{shorter}$ short $Call_{longer}$

#### 6. Straddle

同买同卖at the same strike price. Long straddle => long volatility

- Long Straddle = + Call + Put
- Short Straddle = -Call - Put

![Screenshot 2023-11-01 at 12.46.54](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-01%20at%2012.46.54.png)

#### In Sum

![Screenshot 2023-11-01 at 12.52.13](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-01%20at%2012.52.13.png)

Sell option <=> sell volatility, long option <=> expect vol

Long call <=> long bull

![Screenshot 2023-11-01 at 12.49.52](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-01%20at%2012.49.52.png)

---

### Greek

##### Delta of Option

**Call:** $\Delta \in [0,1]$

- Out-of-Money, $\Delta \to 0$
- In-the-Money, $\Delta \to 1$
- At-the-Money, $\Delta = 0.5$

Put: $\Delta \in[-1,0]$

**Thus,** both strategies are not delta neutral.

- Delta of Covered Call = Delta of Stock (=1) + Delta of Call ([0,1])
- Delta of Protective Put = Delta of Stock + Delta of Put ([-1,0])

- **By put-call parity**

    $C+ \frac{K}{1+r} = p +S$

    Take derivative w.r.t. S

    $\Delta_C + 0 = \Delta_P + 1$

- **By Black-Scholes Model**

    $Call = S\cdot N(d_1) + K\cdot e^{-rt}\cdot N(d_2)$

    $\Delta_C = N(d_1)$

![Screenshot 2023-11-01 at 13.17.35](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-01%20at%2013.17.35.png)

##### Delta Hedging

Delta neutral hedging is a dynamic process 

$+S - \frac{1}{\Delta} C = 0$

$+\Delta S - C = 0$

####  Gamma <- Dynamic Hedging

How delta change w.r.t. S. Lower the gamma, easily the delta hedging. Because delta is less affected.

Gamma is positive, as the curve convex.

Gamma is the **maxima** while option is **at-the-money**.

#### Vega <- w.r.t. volatility, Vega > 0

#### Theta <- w.r.t. time, Theta < 0

#### Rho < w.r.t. risk-free rate, >0 for call, <0 for put

---

### Volatility Smile

1. The Black-Sholes model assumes constant Volatility

2. Emperically for **foreign currency options**, when at-the-money, implied volatility is lowest

   ![Screenshot 2023-11-01 at 21.59.45](/Users/meowmeow/Library/Application Support/typora-user-images/Screenshot 2023-11-01 at 21.59.45.png)

3. Equity Option, Skew (Smirk)

   ![Screenshot 2023-11-01 at 22.06.49](/Users/meowmeow/Library/Application Support/typora-user-images/Screenshot 2023-11-01 at 22.06.49.png)

4. Reasons for the Smile in Equity Options

   1. Crashophbia 崩盘 market crash 可能，因为option就是用来应对危机的
   2. Leverage. As equity declines in value, company's leverage increases.
   3. Volatility Feedback Effect. 反身性，相当于 负向 accelerator

5. OTM Put 的 vol 低, OTM Call 的 vol 高. Buy OTM Call (underpriced) and sell OTM put (overpriced) 

6. **Implied Volatility** is compared with $\frac{K}{S_0}$ or  $\frac{K}{F_0}$ (相当于去除量纲)

---

## Swaps, Forward, Futures

### Manage Interest Rate Risks

#### Interest Rate Swap 

Payer and Receiver 都指的是 对Float 的 pay / receive

![Screenshot 2023-11-01 at 22.47.14](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-01%20at%2022.47.14.png)

##### Duration of the Swap

$D_{payerFloat} = D_{Fix} - D_{Float}$, vice veresa

- The d**uration of float bond is nearly zero**, thus the **duration of payer float is positive**, the **duration of the receiver Float is negative**.

- Empirically, **float-rate bond duration = time period of reset** . E.G. if half-year to reset, then duration = 0.5

##### Market Value Risks and Cash Flow Risks

- Float Bond is s.t. Cash Flow Risks 因为每一期现金流都不确定
- Fixed Bond is s.t. Market Value Risks 因为pay fixed 的部分，受 market rate 影响
- **If change from float to fixed, then CF risks is neutralised and then be s.t. market value risks. Vice Versa.** 如果通过swap 把float 换成了 fixed，那么从 expose cf risks 转为 expose to market value risks

##### Formula

$MV_p \times MD_r = MD_p + N_s \times MD_s$

$D_p$ duration, 利率变动 价格变多百分比

$DD_p = D_p \times V$ dollar duration, 利率变动，价格变动多少元

$D_p = w_1 D_1 + w_2 D_2$

$DD_p = DD_1 + DD_2$, coz $D_p = w_1 D_1 + w_2 D_2$ multiply $V_p$ from the both sides,

$D_pV_p = w_1 D_1 V_p + w_2 D_2 V_p$

$DD_p = V_1D_1 + V_2 D_2$, coz $V_1 = w_1 V_p$

$DD_p  = DD_1 + DD_2$

如何通过 swap 达到目标 Durations.

$D_{original} + \underbrace{D_{Swap}}_{InterestRateSwap} = D_{target}$ 

Solution: by Dollar Duration 能相加

$DD_{target} = DD_{original} + DD_{swap}$  expand it

$D_{target} V_{target} = D_{original}V_{target} + D_{swap} \times N_{swap}$ (Notional value of the Swap)

因为在签订 swap 时， swap value = 0, 所以 $V_{target} = V_{original} + V_{swap} = V_{target} + 0$ 

Finally, 所以

$D_{target} V_{target} = D_{original} V_{target} + D_{Swap} N_{swap}$

$N_s = \frac{D_t - D_p}{D_{swap}} \times V_p$

or 

$MV_p \times MDur_p + N_s \times MDur_s = MV_p \times MDur_t$ ($MV_t = MV_p$ ， 因为市场投资组合的价值 和加入swap的一样，swap在建立时value = 0)

$N_s = \frac{MDur_t - MDur_p}{MDur_s} MV_p$

- Implication:

  $D_t - D_p $ 与 $D_{swap}$ 同向变动

##### Interest Rate Forwards (FRA)

##### Interest Rate Future (Euro-Dollar Future)

- As it is future, it's standard (not OTC as FRA). 
- Guaranteed by a clearinghouse, so counterparty risk is nearly zero. 有保证金，所以交易对手方风险基本上为0
  - Cash settled

- P.S. interest rate futures are short-term, but fixed-income futures are more long time.

Euro Dollar Futures have fixed notional value and fixed term (, as it is standardised). 

- Notional value: 1 million USD
- Term: 3 months

$\$1,000,000 \times \frac{90}{360}\times 1bp = \$25$

---

### Fixed-Income Futures

Treasury-bond is the underlying asset, we do not use corporate bond as there is less liquidity and more credit risks.

#### Delivery

There is a portfolio of T-bonds/bills for settlement. As the Fixed-Income Futures are standarised, they are traded in the exchange, and are settled daily. 标准化的future，有一个basket，交易所交割，可以 cash 可以实物交割

- the Short side has a dilivery option to choose which bond to deliver 意味着short方可以决定deliver哪个，所以有CF转换 basket里的，所以有CTD

Basket 中的 bonds 有 CF (conversion factor) 用来调节 Basket 中不同 bonds 不同期限的rates等带来的差额, 和 Accured Interest 的差别

##### Clean + Accured Int = Dirty

$Clean = \text{Quoted Futures Settlement Priec}  \times CF$

$Dirty = QuotedPrice \times CF + AI$

##### CTD

Futures contract Sell has the right to choose the CTD (cheapest-to-delivered)

$CTD = $$Quoted Price \times CF$

##### Market Yield v.s. Notional Yield

- if market yield > notional yield, then long duration bond is likely to be CTD (最合适用来交割的)	
  - 因为  market rate 大的 ，duration 长 的折价多
  - ![Screenshot 2023-11-04 at 19.00.31](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-04%20at%2019.00.31.png)
  - 如图，久期长的离 expired date 远，折价越多。但是这只是clean price 方面，还未考虑 Accured Interest  
- if market yield > notional yield 的， 短久期的 可能为 CTD （更便宜，适合交割）原因见上图，把图沿 y-axis 对称 

##### Basis Trading

Basis = S - F ,  in alternatives 为空头方的交割成本，basis converge to zero with time

$Basis = S - F \times CF$

- if basis is **positive**, **sell the basis** , ( long the future and short the bond) 因为 Basis converges to zero, 所以如果 basis 正，那么S会变小，F会变大 使basis趋近于0
- if the basis is **negative**, **buy the basis**, ( long the bond and short the future)

#### Fixed-Income Future Hedging 

担心 interest rate 上涨， 带来 T-bond Price 下跌，同时 Fixed-Income Future 价格下跌，所以 **Short Futures**

##### Basis Point Value for Bonds ( BPV )

$BPV_p = MDur_p \times MV_p \times 0.01\%$ , or    $BPV_p = MDur_p(\times) \times MV_p \times 1$

(MDur 为 Modified Duration )

similarly,

- $BPV_{CTD} = MDur_{CTD} \times MV_{CTD} \times 0.01\%$ 
  - $MV_{CTD} = (CTD\ QuotedPrice) \times Future$
- $BPV_F = MDur_F \times Price_F \times 0.01\%$

P.S. recall, irrelevent with the other content 

- $Maculy Duration$ 为时间（年）
- $MDur_F$ 修正久期: 1% 利率变动 => 投资期货合约 收益变动% ($MDur$)
- $DD_F$ 美元久期: 1% 利率变动 => 收益变动 amount $，BPV 类比 DD，为value 

##### Hedge Ratio <- Number of Future Contract 

$\Delta P =  HR \times \Delta F$   =>   $HR = \frac{\Delta P}{\Delta F }$

Similarly

- Basis Point Value Hedge Ratio (BPVHR) 即为 N
  - $BPVHR = - \frac{BPV_P}{BPV_F}$
  - $BPV_F \times CF= BPV_{CTD}$
  - => $BPVHR = - \frac{BPV_P}{BPV_{CTD} } \times CF$
  - The number of future to sell to fully hedge the portfolio is 345 future contracts

负号不能丢，表示 hedge 与 underlying 的变动是相反的

##### Adjust Portfolio Duration

$BPV_{Portfolio} + N\times BPV_{Future} = BPV_{Target}$

通过加入 $N\times BPV_{Future}$ 项，调将 portfolio 的久期调成 target 的数额

N is named BPVHR，根据上式，解出 BPVHR

$BPVHR = \frac{BPV_T - BPV_P}{BPV_F}$

- $BPV_T = MV_P \times D_{Target} \times 1bp$
- $BPV_P = MV_P \times D_{Portfolio} \times 1bp$
- $BPV_F \times CF= BPV_{CTD}$    (Accured Interest is ignored just now)
- **Finally**, $BPVHR = \frac{BPV_T - BPV_P}{BPV_{CTD}}\times  CF$

![Screenshot 2023-11-04 at 20.36.54](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-04%20at%2020.36.54.png)

### Manage Equity Risk

管理 Equity Risks 的方法 (1) Swap (2) Future and Forward <- adjust target portfolio beta & cash equitisation

#### Equity Swap

- fixed rate <-> equity return
- float rate <-> equity return
- equity return <-> another equity return (high risks)

returns are from 

1. a single stock 
2. a basket equity (ETF)
3. an equity index

#### Futures

##### Adjust Beta

Future price is quoted as: $F = \underbrace{f}_{QuoteFuturePrice} \times Multiplier$ ($f$ is %, multiplier convert the $F$ into $ amount)

$N_f = \frac{\beta_T-\beta_p}{\beta_f} \frac{MV_p}{F} $

$ N_f =  \frac{\beta_T-\beta_p}{\beta_f}  \times \frac{MV_p}{f\times Multiplier}$

$\beta_p \times MV_p+ \# \times \beta_f \times \underbrace{(f\times Multiplier)}_{F (\$ amount)} = \beta_T \times MV_p$

$\# =N_f= \frac{\beta_T \times MV_p - \beta_p MV_p}{\beta_f \times f \times Multiplier} = \frac{\beta_T -\beta_p}{\beta_f}\frac{MV_p}{f\times Multiplier}$

Or $= \frac{\beta_T -\beta_p}{\beta_f}\frac{MV_p}{F}$

$F \Leftrightarrow f \times Multiplier$ are $ amount

##### Cash Equilisation

  make $\beta_p$ or $\beta_T$ as "0".

- Synthetic Risk-free Asset $\beta_T=0$

  $N_f = \frac{0 - \beta_p}{\beta_f}\frac{MV_p}{f\times Multiplier}$

- Synthetic Equity $\beta_p = 0$

  $N_f = \frac{\beta_T -0}{\beta_f}\frac{MV_p}{f\times Multiplier}$

#### Using Derivatives to Alter Asset Allocation

如 Fund has 33.33% Bonds + 66.67% Equity， 想调整为 30% Bonds + 70% Equity。因为若fund很大，直接抛售等买卖会带来资产价格大幅变动。

为了避免价格波动，我们不直接买卖资产，而是买卖对应的 derivatives (futures and forwards)，因为这样可以最小化对市场价格的影响

通过 Cash Position make $\beta = 0, for\ Stocks$, $BPV = 0, for\ Bonds$

所以此时，并不是直接 Sell bond，而是 make $BPV_T=0$ 

不是直接 buy equity，而是 make $\beta=0$

---

### Manage Currency Risks

Cross-currency basis: additional cost of borrowing dollar (most currencies show a negative basis against dollar) 即美元有加点

$\frac{F}{S} = \frac{1+r_f+(basis)}{1+r_d +(basis)}$

##### Cross-Currency Basis Swap 期初还两个币种的本，期末换回来

Swap the notional principals, 本金可以在beginning换，在ending换回来 but periodic interest payment could not be netted 期间的利息不换

##### Synthetic Borrowing 不换本金

No exchange the principals. Instead, 

exchange CF in the future at fixed exchange rate

The amount of exchanged are based on the Exchange Rate and Interest Rate

##### Currency Forward and Futures

$HR = \frac{\text{Amount of Currency to be Exchanged}}{\text{Future Contract Size}}$

---

### Manage Volatility Risks

- Volatility Derivatives
  1. VIX Futures
  2. VIX Options
  3. Volatility index
- Variance Swap 

##### VIX Futures

VIX and Equity returns are mostly negative correlated

P.S. Cost of Carry model does not work on VIX $F = S X(1+r_f)^T - CB + CC$, because VIX spot is not able to be invested (VIX is an index, is calculated)

##### Variance Swap 

Payoff of Variance Swaps is based on **Variance** rather than **Volatility (s.d.)**.

Swap 的双方为 $\sigma^2$ and $K^2$

- Variance Stike (Implied Volatiltiy),  $K^2$: the implied vol **at the beginning**
  - $Strike = K , \text{and } variance \ strike = K62$
- Realised Variance,  $\sigma^2$: Actual Vol over the life of the swap

No Exchange of Notional Principal and No interim Settlement periods

- Settlement Amount (long): $=variance\ notional \times (\sigma^2 - K^2)$
  - Long 方为 收浮动，支固定
- Settlement Amount (long): $=vega\ notional \times \frac{\sigma^2-K^2}{2K}$
- , where $vega \ notional = variance \ notional \times 2K$    ($vega\ notional = variance\ notional \times (\sigma +K)$, and $\sigma+K \approx K+K=2K $)
- $vega \ notional$ 是指一般意义上的本金，题目会给的数值

###### Mark-to-Market (MtM) Value of Variance Swap

盯市，因为 swap 在 beginning is made to be zero value，但是随着时间和市场变化（$\sigma^2 \ \text{and}\ K^2$ 变化） swap开始有价值

MtM 指在 t 时间估计出来的，对到期日 var 的估计（加权平均）

![Screenshot 2023-11-05 at 16.10.21](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-05%20at%2016.10.21.png)

$Expected \ Variance\ to \ Maturity = (\sigma^2_t \times \frac{t}{T}) + (K^2_{T-t} \times  \frac{T-t}{T})$

$weights_1 = t / T,  weight_2 = (T-t)/T$

---

### Inferring Market Expectation

| Application                                 | Derivative              |
| ------------------------------------------- | ----------------------- |
| Inferring Expectation of FOMC moves         | Fed Funds Futures       |
| Inferring Expectation of Inflation          | CPI Swaps               |
| Inferring Expectation of Futures Volatility | VIX Futures and Options |

- **Fed Funds Futures**

  - $Fed Funds Future \ ContractPrice = 100 - Expected FFE\ rate$

  - **Eurdollar Futures**
    - Dollar deposited in the outside of US
    - Quoted Price = 100 - Future Interest Rate
  - **Federal Fund Rate**: overnight rate deposite rate by the Fed
  - **Federal Fund Target Rate**, set by FOMC meetings

- **Expected Probability**

  假设利率在区间内服从均匀分布，所以 分子/分布 = Prob

---

## Currency Management

### Currency Swap 

### Mark-to-Market Value

MtM 指在 currency swap 存续期，swap 的value （因为 initial 的时候 value = 0）

### FX Swap 本质上是 forward 借新还旧

- **Similar to currency swaps**, FX swaps **involve an exchange of principal amounts in different currencies at swap initiation** that is **reversed at swap maturity.** 与 currency swap 相同的是 在 initiation 和 expire 
- **Unlike currency swaps**, FX swaps have **no interim interest payments**不同点是 不互换中期的

### Effects of Currency on Portfolio

- Foreign Currency Return, $R_{FC}$ 指的是 资产价格的变动 foreign asset @ foreign currency 的return
- Local Currency Return, $R_{FX}$ 指的是 the percentage of foreign currency agaisnt the domestic currency 指的是汇率的变动
- Domestic Currency Return , $R_{DC}$ 指的是 rate of return stated in domestic currency term

#### Returns

$1+ R_{DC} = (1+R_{FC})(1+R_{FX})$

in a portfolio

$1+R_{DC} = \sum_i^n w(1+R_{FC})(1+R_{FX})$

$R_{DC} = \sum_i^n w(1+R_{FC})(1+R_{FX}) - 1$

#### Variance

$Var(R_{DC}) = Var\bigg((1+R_{FC})(1+R_{FX}) - 1\bigg)$

$\sigma^2_{R_{DC}}\approx  \sigma^2_{R_{FC}} + \sigma^2_{R_{FX}} + 2\sigma_{R_{FC}}\sigma_{R_{FX}}\times Corr$

#### Other Considerations

- if Correlated is low, $Corr \downarrow$, then $\sigma^2_{R_{DC}} \downarrow$, Implication 如果外汇和资产负相关，那么 risk 低

- **if there is not exchange rate risks**, of says if there the exchange rate pegged, then $R_{FX}=0$, then $ \sigma^2_{R_{DC}} \approx  \sigma^2_{R_{FC}}  $

- **if $R_{FC}$ is a risk-free return,** then $R_{FX} =r_f = Constant$ is a constant

  $Var(R_{DC}) = Var\bigg((1+R_{FC})(1+R_{FX}) - 1\bigg)$

  $Var(R_{DC}) = Var\bigg((1+r_f)(1+R_{FX}) - 1\bigg) = Var\bigg((1+r_f)R_{FX} \bigg)$

  $\sigma (R_{DC}) = \sigma\bigg((1+r_f)R_{FX} \bigg)$

### Strategic Currency Management

- **Fomulate IPS**: general objectives, risk tolerance, time horizon, ongoing income and liquidity, benchmark (rebalance周期)

- **Choice of Currency Exposures**: 要对冲多少

- 1. Diversification Consideration

     1. in the long run, it would not matter if the portfolio was hedged or not

     1. if $R_{FC}$ and $R_{DC}$ are negatively correlated, then $\sigma_{R_{DC}}$ is small, so less exposure is enough

     1. Correlation $\rho_{R_{FX},R_{FC}}^{Bond} > \rho_{R_{FX},R_{FC}}^{Equity}$. This assertion makes intuitive sense: both bonds and currencies react strongly to movements in interest rates, whereas equities respond more to expected earnings. So, less hedge on $\rho_{R_{FX},R_{FC}}^{Equity}$ because low corr low risks, more hedge on $\rho_{R_{FX},R_{FC}}^{Bond}$ because more corr more risks

  2. Cost Consideration

     1. trading expense while rebalance frequency is high

     2. if options are OTM (out of the moeny), then less expense

     3. As Forwards need to be "rolled" and produce cost, we use FX swap.

        however, as rolling hedges will generate cash inflows and outflows, and thus more volatiltity on cash account

     4. Opportunity of the hedge. (rule of the thumb, 50% hedge ratio). Hedge the larger advese moments, ignore the minor.

  3. Choice of Currency Management Strategies

     1. Passive Hedge, 100% hedge with benchmark portfolio used to evaluate performance
     2. Discretionary Hedge, with limits 80% hedge
     3. Active Currency Management, 20% hedge, more active management
     4. Currency Overlay， 0% hedge 有专员负责 trade and bargin with the FX, speculate

  4. Formulate a CUrrency Mgt. Program

     The situation we need bias toward more-fully hedged currency mgt programs 需要更多对冲的情况

     1. have a short term objective
     2. Risk averse
     3. Immediate Income/Liqudity needs
     4. Fixed-income assets are held as $\rho_{R_{FX},R_{FC}}^{Bond}$ is higher
     5. hedge program is cheap
     6. financial mkt is volatile or risky
     7. Skeptical the benefical owners 客户怀疑 / management oversight active mgt 监管控制 active currency mgt

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

![Screenshot 2023-11-07 at 13.02.53](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-07%20at%2013.02.53.png)![Screenshot 2023-11-07 at 13.02.53](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-07%20at%2013.02.53.png)

#### **Strangle** 

Long Call and long put OTM, but as options are OTM, so lower premium 期权费便宜.

The Green Curve is Straddle, Yellow Curve is Strangle, in the below figure.

![Screenshot 2023-11-07 at 13.05.09](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-07%20at%2013.05.09.png)

Pros: lower premium fees

Cons: lower returns

However, strangle could have a trading position that has net Vega and delta exposures (可以被做成不是围绕 current stock price 中心对称的，如向左和向右平移通过调整 call & put 的 strike price，这样可以结合 traders 对涨和跌的 expectations)

![Screenshot 2023-11-07 at 13.13.10](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-07%20at%2013.13.10.png)

Discontinue the Carry Trade 意味着 终止 Carry Trade

---


### Tools for Currency Management

Assume $d/f$ direct quote, the base is foreign currency. 我们担心外币贬值，所以产生一下策略

#### Forward Contracts 

Roll Yield / Roll Return $=\frac{F-S}{S}$

##### Over/Under Hedged

i.g. 在未来会收到 100 US Asset，then enter a forward contract 卖100 USD 换 CNY

如果 forward contract 是 卖 120 USD 换 CNY 那么 over hedged

如果 forward contract 是 卖 80 USD 换 CNY 那么 under hedged

#### Options

#### Protective Put using OTM Options

- ATM Options are expense
- keep some downside risks as well as upside potential

#### Risk Reversal

Long put OTM, short call OTM ( the underlying asset is the currency )

may reduce the cost, as we short a option

#### Bear Put Spread

buy an OTM put and wrote a deeper OTM put with same maturity

#### Seagull

one type: bear put spread position with a short call position

### Expotic Options

- Asian Options = $\max(S_T - ave,0)$

- Digital Option

   ![Screenshot 2023-11-07 at 22.05.31](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-07%20at%2022.05.31.png)

- Knock-in Options (trigger once touch a pre-specificed level)

- Knock-out Options (exit once triggered)

---

### Hedging Multiple Currencies & Emerging Market Currency Management

#### Hedging Multiple Currencies

- **Cross hedge (proxy hedge)**: hedge with an instrument that is not the same as the exposure 通过hedge 与目标相关的资产，如原要hedge 航空燃油，实际 hedge 原油，这样可以达成相同的效果
- **Macro Hedge**: focus on the entire portfolio, not individual assets or currency pair,, as assets themselves inside the portfolio might hedge themselves, so we care what left from the entire portfolio 
- **Minimum-variance hedge ratio**: using OLS to get the cross hedging ratio ($\beta$, the slope in regression is the **optimal hedging ratio**).

#### Emerging Mkt Currency Management

- Might have higher trading costs
    - Larger ask bid spread
    - Crosses in currency pair (coz might not have direct pair)
- Might have Capital Control in the emerging mkt, so use **non-deliverable forwards (NDFs)** 不直接交还本金，cash settled rather than physically settled

