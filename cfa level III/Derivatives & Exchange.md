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

