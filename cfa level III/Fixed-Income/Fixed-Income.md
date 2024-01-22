# Fixed Income

## General Knowledge

### Roles of Fixed Income in Portfolio

- **Diversification**. We may focus on how bonds **correlate** with equities. 

    1. Corr between bonds and equities might not be "1", is less than "1"
    2. **In the Stress Periods**, correlation 
        - decrease between government and equity
        - increase between high yield bond and equity
    
- **Manage Cash Flows** to meet obligations such as Tuition Fees, Pension, etc

- Hedge for **Inflation**

    - 一般情况下，bond 对 high inflation 不友好，因为 pay fixed
    - **(1) Float bond & (2) TIPS**
    
    <img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-08%20at%2008.58.01.png" alt="Screenshot 2023-11-08 at 08.58.01" style="zoom: 50%;" />

### Classify the Fixed-Income Mandates

- **Liability Based** 为了满足 lia 需求，如 tuition fees
    1. Duration matching
    2. CF matching
    3. Derivatives Overlay
    4. Contingent Immunisation
- **Total Return** Mandate 为了挣 return 
    1. Pure Index
    2. Enhanced Index
    3. Active

### Types of Lia

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-09%20at%2012.28.21.png" alt="Screenshot 2023-11-09 at 12.28.21" style="zoom:50%;" />

| Types    | Amount is Known | TIming is Known | Example                                                      |
| -------- | --------------- | --------------- | ------------------------------------------------------------ |
| Type I   | 1               | 1               | Traditional Bond (without options)                           |
| Type II  | 1               |                 | Callable bond (已知amount，不知道时间，可提前赎回), Term Life-time Insurance 寿险 |
| Type III |                 | 1               | Float Rate Note, Inflation Related Bond (金额不确定，但是有确定到期) |
| Type IV  |                 |                 | DB Plan, Property & Casualty Insurance 财险金额和时间都不确定 |

**Type I:** An advantage to knowing the size and timing of cash flows is that **yield duration statistics**—that is, Macaulay duration, modified duration, money duration, and PVBP—can be used to measure the interest rate sensitivity of the liabilities.

**With Type II, III, and IV liabilities, a curve duration statistic** known as **effective duration** is needed to estimate interest rate sensitivity. This statistic is calculated using a model for the uncertain amount and/or timing of the cash flows and an initial assumption about the yield curve.

### Fixed-Income Returns 5个部分

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240112083726046.png" alt="image-20240112083726046" style="zoom: 67%;" />

$\mathbb{E}(\Delta P) = - Mod.Dur \times \Delta Yield + \frac{1}{2}\times Convexity \times (\Delta Yield)^2 $

### Leverage

##### Leveraged Portfolio **Return**

$r_p = \frac{Portfolio\ Return}{Portfolio\ Equity} =  r_i + \frac{B}{E} \times (r_I - r_B)$

自有资金的return = 本身的return, r_i + leverage * (diff between 自己的return - borrowed return)

- $E$ value of Portfolio Equity, amount of Equity
  - $r_I$ investment funds return
- $B$ borrowed funds, amount of Bonds
  - $r_p$ levered portfolio returns
- The last eqution, and the last term represent the leverage effects on returns.
- if $r_I > r_B$, then leverage increase total portfolio return
- if $r_I < r_B$, then leverage decrease total portfolio return

##### Leverage Effects on Duration

$D_p = D_I + \frac{V_B}{V_E}(D_I - D_B)$

##### 提升 Leverage 的方式

1. Derivatives

   - Futures:
     - if $i$ increase, then price decrease, FP also decrease

   - Swap:
     - Fixed-rate payer: long float short fix 因为 float 不影响duration，所以short fixed 会减少 duration。此时 i 提升， duration 负，则 value increase
     - Fixed-rate receivers: long fix short float 为duration增加。此时 i 提升，duration 为正，value 减少


2. Repo

   1. **Repo Margin**: A 给 B asset，值100； B 给 A cash，为95 。 此时 B 少给的 5 为 Repo Margin，B少付的相当于是A给B的保证金
   2. **Repo Rate**: 结束后，A 给 B cash，为 97；B 把 Asset = 100 还给 A。那么97-95=2，多出的 2 为 repo rate，相当于借款利息	

3. Structural Financial Instruments (implicit)

   - inverse floator
   - embedded leverage

4. Securtities Lending

   <img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-08%20at%2021.50.02.png" alt="Screenshot 2023-11-08 at 21.50.02" style="zoom:50%;" />

   Rebate Rate = Collateral Earning Rate - Securitiy Lending Rate

#### Risks of Leverage

- Force Liquidation
  - Fire Sale: forced liquidations at prices that are below fair value as a result of the seller’s need for immediate liquidation.
- Higher level of Risks

### Taxation

如果实现 Capital Loss 可以减税

如果是 tax exempt account，那么可以直接 直接实现 capital gain，否则考虑实现 capital loss 来抵税

- Tax rate (rationale: 越稳定的收入 tax rate 越高，因为税务局不愿意承担风险)
  - Coupon: tax is higher 
  - Capital Gain: tax is lower

Short-term Capital Gain tax > Long term Capital Gain

Capital Loss 能抵减 Capital Gain， 不能抵减 Coupon

---

## Liability Based Mandate

1. Duration Matching
2. Cash Flow Matching
3. Contingent Immunisation

Bonds earn: (1) Coupon (2) Reinvestment (3) Price Changes

其中 Coupon 是固定的，但是 Reinvestment 和 Price Changes 受interest rate变动

因为 if interest rate increase, then (1) reinvestment return increase (2) price changes negative 所以，如果(1) & (2) 可以抵消，那么Duration matching 达成， Immunisation

- **Price Risks <- measured by Duration** 
- **Reinvestment <- measured by Horizon** 

So, we need to let 

$Duration = Horizon$

买 zero-coupon bond 最好，因为不涉及不用考虑中间 coupon reinvest的问题，但是 zero-coupon bond 只有短期。要匹配长期，只能买 coupon bearing fixed income bond

### Duration Matching (Classic Immunisation 免疫策略) 

保证 能earn IRR / Cash Flow Yield

#### For Single Lia Immunisation

Make price risks and reinvestment risks cancel each other.

- P.S.
  - 对于 single liability immunisation ，convexity 越小，受到的 structural risk （即yield curve 非平行移动带来的risks）越小。
  - 对于 port lia immunisation，convexity 越大，免疫的越好

如何 做 immunisation immunistion 

1. Portfolio Duration = Liability Duration   <- price risks
2. PV of Port = PV of Lia                     <- reinvestment risks

-  以上两个条件可以合并为: same Money Duration (BPV) or (PVBP)

3. **minimuse Convexity, in order to minimise structural risks**

Horizon 指的是 liability duration 负债的duration = 负债的到期日

- If $Port Duration < Horizon$: 如果 hold to maturity，那么不受 price risks 影响。但是受 reinvestment risk 影响大，因为
- If $Port Duration > Horizon$: 在收到 interim CF 之前就给买了，所以investment horizon小，那么受制于 reinvestment risks 小，因为没 reinvest 就卖了，反而受 price risks 影响大
- If $Port Duration = horizon = Lia Matuiry$, then the hedge is good

##### Dealing with the Structural risk / Immunisation Risks: 

Structural Risk (non-parallel steepening and flattening twists) yield curve 非平行移动会导致 structural risk 即 

- 此策略不能 cover Non-parallel changes **in interest rate** 因为 duration 衡量的是 利率的平行移动，所以如果不平行移动，则 duration match 失效
    - bond 的 CF流入有 (1) Barbell 两边流入多，中期流入少，易受 non-parallel shifts 影响 (2) Bullet 仅一期大的流入，受 non-parallel shifts 影响小。**In sum， invest 更多bullet bonds**
    - 用 convexity 判断组合是 bullet 还是 barbell。$Convexity = \frac{Mac.Dur^2 + Mac.Dur + Dispersion}{(1+yield)^2}$ 如果 dispersion越大，相当于 barbell，受收益率曲线 非平行移动（斜率变）影响大。If dispersion 大 =>  Convexity 大。 **所以 降低 portfolio's convexity 可以降低 non-parallel shift 影响**， **Structural risks 小**
- Duration 会变化 （time 变化， interest rate 变化，会使Duration变化）
    - **定期 rebalance 去平衡 duration 变化的影响**
    - 但是 rebalance 太过频繁会增加 transaction costs
- 只匹配了 duration ，没有 匹配 convexity
    - 没啥解决办法，忽略 convexity
- **如何解决 Structural risks ，最好的是买 Zero-coupon bond 只有一期现金流。其次是 买 bullet bond 现金流集中，convexity 小，受 yield curve moves 影响小**

#### For Multi-Liabilities Immunisation

1. $PV_A = PV_{Lia}$
2. $Duration_A = Duration_{Lia}$
    - 1.2 可以合并为 Money Duration (BPV) 一样 or PVBP 一样
3. （增加一条 for multi-lia ）$Range_{A} > Range_{Lia}$ 资产的周期要能覆盖 lia port的周期，为了保证最后一期有足够的现金流能 cover liability payments

- Convexity要大于 outflow convexity的最小的
    - The immunising portfolio needs to be greater than the convexity (and dispersion) of the outflow portfolio. But, the convexity of the immunising portfolio should be minimised in order to minimise dispersion and reduce structural risk.

##### Cash Flow Matching

Cash Flow matching 是最nb的，可以避免 risk from non-parallel shifts in Yield Curve

先 cover 最后一笔负债，从后往前一层一层的剥离。先匹配长期的bond 是因为 买 asset 匹配长期的 lia 的时候，asset也会产生 interim cf，那么在匹配短期的时候，这些cf inflow将被合并考虑

- Year 5: $L_4 = P_A + C_A$
- Year 4: $L_4 - C_A = P_B+ C_B$
- Year 3: $L_3 - C_A - C_B = P_C+ C_C$
- $\vdots$

, where $P_A,C_A$ are for the bond A, 5-year. and bond B is 4-year, bond C is 3-year, etc

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-08%20at%2010.13.35.png" alt="Screenshot 2023-11-08 at 10.13.35" style="zoom: 50%;" />

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-08%20at%2010.13.10.png" alt="Screenshot 2023-11-08 at 10.12.55" style="zoom: 50%;" />

- Pros: 精确度高，可以很好匹配现金流 ，Straight forward, **no assumption of non-parallel shifts of the yield curve** , **no reinvestment**,  **no rebalance**, **accounting defeasance (在 B/S 中 把 A L 轧差 remove)**
- Cons: 成本高，因为要买匹配日期的 bonds，若没有匹配的，只能买提前到期的bond，那么会损失提前到期日和pay lia日之间的时间价值。这段时间可能只能投低收益 risk- free 流动性强的资产。

Why not buy back and retire the liability early (tender offer)?

- Buyback is difficult and costly
- Might be illiquid
- Corporate has motive to improve the credit rating by doing CF matching, so do not buyback earlier.

##### Duration Matching

条件：

1. $MV_A > PV_L$ or $PV_A>PV_L$
2. $BPV_A = BPV_L$
3. $Convexity_A>Convexity_L$ 不同于 single 此时要求 convexity 比 lia 的更大，这样才增在non-parallel moves 是 cover CF  

Cash Flow matching 和 Duration matching 的区别：具体见下表



<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240112124542365.png" alt="image-20240112124542365" style="zoom: 67%;" />

##### Contingent Immunisation 用

Allow **active management** for the surplus amount of assets over liability **用surplus 的部分做 active management，其他正常部份 immunisation**

##### Derivatives Overlay 用于 Cover the Duration Gap

前三个(1) duration matching (2) CF matching (3) contingent immunisation是用来构建组合。但是 Derivatives Overly 不是用于构建，而是用来 adjust. **Rebalance the immunisation portfolio to keep it on its target duration.**

$Asset \ BPV \times \Delta Asset\ Yields + Hedge\ BPV \times \Delta\ Hedge \ Yield \approx Lia\ BPV \times \Delta Lia \ Yield$

$BPV_A + N_f \times BPV_f = BPV_L$

$BPV = V \times MD$

- Using Future

  - Required Number of Future Contract: $N_f = \frac{Lia\ Portfolio \ BPV - Asset \ Portfolio \ BPV}{futures\ BPV}$

  - $Futures BPV = \frac{BPV_{CTD}}{CF}$  cheapest to Deliver


- Using Interest Swap
  - Notional Principal: $NP = \frac{LiaBPV - Asset BPV}{Swap BPV/100}$


- Swaption

  - increase duration: enter a receiver swaption 收固定pay浮动，所以duration提升

  - Decrease duration: enter a payer swaption


Using Derivatives to adjust the duration of liability portfolio 用于调整 duration 不用于构建 asset portfolio

### Hedge Ratio

- Non hedge, Hedge ratio = 0%
- Fully Immunised, Hedge ratio = 100%

- If interest rate is low, then 有利率上升的风险，资产价值可能下降，then have higher hedging ratio

- if interest rate is higher, then 有利率下降风险，资产价值可能上升， 所以 then lower hedging ratio

### Risks in LDI

1. Model Risks: model assumptions are wrong
2. Interest Rate Risks: $Dur_A = Dur_L$, duration explains (95%) most of price movement of bonds
3. Yield Curve Risks: **non-parallel shifs of the yield curve**. 

   How to deal with the non-parallel shifts of the yield curve: Minimise the dispersion of CF can mitigate this risks.
4. Spread Risks: $YTM = Base Yield(Treasury Yield) + Spread$
   - yield on high-quality corporate bond are less volatilty than more liquid treasuries
5. Counterparty Credit Risks
6. Collateral Exhaustion Risks 由于 collateral不足，导致被平仓的risks
7. Liquidity Risks 

---

## Total Return Mandates (Index Based)

- Pure Index (Full replication)
- Enhanced Index 
- Active

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240112133640987.png" alt="image-20240112133640987" style="zoom:67%;" />

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240112134011405.png" alt="image-20240112134011405" style="zoom:67%;" />

因为 bond liquidity 比 equity 的低，所以mimic index bonds by purchasing the same bonds 可能比较难以操作。 所以 mimic **Risk Factors**

Risks Factors:

1. **Interest Rate Risks**: exposure to **parallel** shift in the Yield Curve. Measured by **Portfolio Duration**

2. **Spread Risks**: exposure to changes in spreads between Treasuries and non-Treasuries. Measured by **Spread Duration**.
   - (YTM = Benchmark Yield + Spread), so spread 涨1%带来的YTM 增加与 Benchmarked涨1%带来的YTM增加一致。thus spread duration = portfolio duration，as 都通过YTM影响 price

   - P.S.国债没有 spread

3. **Yield Curve Risks**: exposure to a **twist** in the Treasury Yield Curve. Measured by **Key Rate Duration & PV of Distribution of CF**

4. Credit Risks**: exposure to downgrades and defaults. Measured by contribution to **duration by credit rating

5. Optionality Risks**: exposure to changes in CF due to call/put features. Measured by **Portfolio Delta**

**Matching a FI Portfolio to an Index**

- **Tracking Risks**: deviation of returns on the selected portfolio from bond market index returns.
    - Tracking Error: $Active Return = Portfolio Return - Benchmark Index Return$

FX market is difficult to track, because of size and breadth, wid array of security characteristics, and unique issuance and trading pattern.

- 买 ETF 可以不用 mimic all funds, and have greater liquidity. ETF can be purchased and sold throughout the trading day at discount or premium to NAV

**Mandates:**

- **Pure Indexing:** 做一模一样的指数 replicate an existing market index by purchasing all of the constituent securities, to minimise tracking risks

    - Passive Investment: pros: diversification, cons: neither feasible nor **cost-effective** 因为要疯狂 rebalance 所以 transaction cost 高
    - Could be done by mutual fund, ETFs, Total Return Swap (TRS)

- **Enhanced Indexing**: 与指数有不同（买部分 or Mirror 主要风险因子） the investor purchases fewer securities than the full set of index constituents but matches primary risk factors reflected in the index.

    Way 1: purchase most import index

    Way 2:  Mirror Risks Factors

    - Mirror most important index characteristics, more effective than full replication

    - Risks Factors for primary indexing:

        - Interest Rate Risks: 保证 portfolio Effective duration 与 index一致

        - Yield Curve Risks: 

            1. 保证 portfolio Key rate duration与index 一致 - gauge the non-parallel yield curve shifts
            2. PVD ( present value of distribution of CF) 保证 PVD 与index一致

            <img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-10%20at%2013.16.42.png" alt="Screenshot 2023-11-10 at 13.16.42" style="zoom:33%;" />

            ![Screenshot 2023-11-10 at 13.17.20](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-10%20at%2013.17.20.png)

    - Spread Risk 保证 Spread  duration 匹配

- **Active Management**: involves taking positions in primary risk factors that deviate from those of the index in order to generate excess return

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-08%20at%2019.34.02.png" alt="Screenshot 2023-11-08 at 19.34.02" style="zoom: 67%;" /> 

---

Recall:

- Maculay Duration: weighted averaged years
- Modified Duration: percentage price change given the YTM yield changes
- Effective Duration: the sensitivity of bond price to a change in benchmarket yield (**parallel shift in the benchmark yield curve**) 仅用来分析 parallel shifts of yield curve
- Key Rate Duration: identify the sensitivity of shape of benchmark yield curve
- Empirical Duration: regressopm pf bond price on benchmarket yield curve
- Spread Duration: sensitivity to change in credit spread, $YTM = Benchmark + Spread$
- Money Duration (BPV): 利率变 1%， 价格波动的amount
- PVBP (Price Value of a Basis Point): 利率变动1bp，带来的价格波动
- Convexity: second order Derivatives of Price w.r.t. yield

#### Spread

A bond’s **yield spread** includes both **credit and liquidity risk**. Liquidity risk depends on both market conditions and the specific supply-and-demand dynamics of each fixed-income security.

##### Correlation

Below-investment-grade securities are affected more by changes in spread than by changes in general interest rate and exhibit stronger ocrrelations with equity markets.

##### Portfolio Duration in TOtal Return Mandates

- **Top-down** approach to establish the large **risk factors** (mimic the risk factors)
- **Bottom-up** to **adjust individual security selection**
- Use the **spread duration** to gauge the portfolio’s sensitivity to changes in credit spreads.
- A **second way** to increase the portfolio credit exposure is to **reduce the average credit rating of the portfolio**.

### Risks Factors for primary indexing

- Interest Rate Risks: 保证 portfolio Effective duration 与 index一致
- Yield Curve Risks: 
  1. 保证 portfolio Key rate duration与index 一致 - gauge the non-parallel yield curve shifts
  2. PVD ( present value of distribution of CF)保证 PVD 与index一致

- Spread Risk 保证 Spread  duration 匹配

### Bond Market Liquidity

Yield & Liquidity are negative correlated

### Laddered Portfolio （convexity 在 Bullet 和 Barbell 之间）

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-10%20at%2013.34.46.png" alt="Screenshot 2023-11-10 at 13.34.46" style="zoom:50%;" />

CF spreads and is diversified across the life of the bond.

The laddered approach provides both diversification over time and liquidity.

P.S. dispersion and convexity are positively correlated see equation. 

**Sample text:** A laddered portfolio has **lower convexity and dispersion than a barbell portfolio but more than a bullet portfolio,** given comparable duration and cash flow yields. Lower convexity and dispersion are desirable aspects in liquidity management. In a laddered portfolio, there is always a bond close to redemption enhancing liquidity. As bonds mature, the final coupon and principal are available for distribution or can be reinvested in a long-term bond at the back of the ladder. 

---

## Yield Curve Strategy

### Primary Yield Curve Risks Factors

- **Level**: parallel shifts in the yield curve
- **Slope**: twist / non-parallel shifts ($Y_{long-run} - Y_{short-run}$)
- **Shape or Curvatures** (butterfly movement): $2Y_m - Y_s - Y_L$
  - positive butterly: concave

- **Duration**:

  - **Maculy Duration**: weighted Average Time
  - **Modified Duration**: yield and percentage of price changes
  - **Effective Duration**: yield and percentage of price changes for **options embeded bonds**
  - **Key Rate Duration**: **at a specific time point**

- Convexity (second order)

  - effective convexity : for option embedded bonds

### Strategies

- **Static Yield Curve:** 

  1. buy and hold:
     - in upward sloping curve, active management
  2. riding the yield curve: buy long-term bond, sell short-term bond
     - in upward sloping curve, active mangetment 挣long-term bond 的 coupon 要比 short-term 的大。同时，由于假设 yield curve upward sloping, 持有bond 到短期后 rate 下降，so bond price increase。
     - 综上 ride the yield curve 假设 upward yield curve ， 挣 (1) higher coupon (2) price change
  3. Carry Trade (repo): buy security or long term bond, borrowing at low rate / or **Repo** to earn the spread between two rates
     - reqiure the yield curve to be static.
  4. Derivatives
     1. Long Future Position (用衍生品可以增加 leverage)
     2. Receive Fixed Swap  相当于carry trade，支付利率 short term MRR 比 收到利率 fixed 低，挣spread

- **Dynamic Yield Curve**

  1. **Level** Changes (parallel shifts)

     - if interest rate fall, then price increase, then strategy should be to increase the duration

     - if interest rate increase, then price decrase, then strategy should be to decrease the duration

     - Ways to reduce Duration: 
       1. sell cash bond, bullet
          1. Pay-fixed (interest rate swap)
          2. short future position

  2. **Slope** Changes
		- if getting **steepen**, then long term rate incrase, long-term bond price decrase, short-term rate decrase, short term bond price increase
		- then three strategies in three situations:
       <img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-12%20at%2015.49.56.png" alt="Screenshot 2023-11-12 at 15.49.56" style="zoom: 67%;" />
       <img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/202312232106240.png" alt="Screenshot 2023-12-23 at 21.06.33" style="zoom:67%;" />
		- i.e. in duration-neutral yield curve flattening trade, an investor typically goes long on longer-term bonds and short on shorter-term bonds, **expecting that the yield curve will flatten**.
		- if we want **duration neutral**, we should play with barbell and bullet, as bullet has more mid-term, and is less affected by slope changes; but for barbell long-term rate incrase, price decrease more than short-term price increase, so barbell overall is loss. 
			- Long bullet, short barbell 
		- if under **bear steepen**, then long term rate increase more than short-term rate increase, and rates are all increased, so prices are all decrase, but long-term price decrease more. We decrase duration
		-if under **bull steepen**, we want earn from steepen, then increase duration.
		- Risk is the yield curve moves unlike our expectation that didn't get steepen.
		- Vice Versa for **Flattening**

  3. **Shape** Changes (curvture) (diverge rate changes)

     $Butterfly\ Spread = 2Y_m - Ys- Y_L$ 计算公式

     1. negative butterfly means 蝴蝶肚子朝上 butterfly spread increase, then mid increase, long and short term decrase, 
        1. then long long barbell, short bullet
     2. Positive Butterfly means 蝴蝶翅膀朝上 V 形, long bullet (mid-term), short barbell (short short-term and long-term)

  4. **Volatility Changes** Strategies

     - Reduce in volatility, then short options 
       - long callable bonds

     - Increase in volatility, then long options and option value incrase
       - long putable bonds

- **Adjust the Duration** (**increase** duration and convexity)
  - long receiver swaption, have the right to receive fixed
  - long call option on bond future, have the right to take forward bond
  - long bond call, have to right to take a bond
  - decrease duration by the opposite trading

<img src="https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/image-20240112164349321.png" alt="image-20240112164349321" style="zoom: 67%;" />

### Evaluating Yield Curve Strategies

**Total Expected Return:**

$\mathbb{E}(R)$:

Coupon Return: coupon + reinvestment
1. Rolldown Return: when $\Delta y$, how much $\Delta P$
2. Return: when $ \Delta y$ changes, how much $\Delta P$
3. Credit Loss
4. FX G/L

#### Forward Rate Bias

Forward rate bias is defined as an observed divergence from interest rate parity conditions under which **active investors seek to benefit by borrowing in a lower-yield currency and investing in a higher-yield currency.**

Investors tend to favor unhedged fixed-income investments in higher-yielding currencies that are sometimes enhanced by borrowing in lower-yielding currencies.

---

## Credit Strategy

- Credit Risks:
  - Spread Risks -> measured by Spread Duration
  - Default Risks -> measured by CVA
  - Credit Migration -> measured by Credit Rating

#### Spread curve differs in differnt macro environments

High Yield bond and Low Yield bond behave different at differnt econ environment.

![Screenshot 2023-12-24 at 16.57.28](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/202312241657372.png)

- Low credit level issuers tend to have greater slope and level changes at different econ cycle.

  - high-yield spread curve tends to invert during a contraction

- High-rated issueres face smaller credit spread changes.
- In strong econ growth situation, low/high credit rated spread converges.
- In bad econ envir, people buy gov bond. Gov bond and high-yield bond become negative correlated.

- **Empirical Duration**: benchmark rate 对 price 实际的影响

  $\underbrace{BondYield}_{Duration} = \underbrace{RiskFreeRate}_{Benchmark Duration}+ \underbrace{Spread}_{Spread Duration}$

  - Theoretically, benchmark duration and spread duration have same impacts w.r.t. interest rate changes
  - Empirically, (in practice), credit spread tend to be **negatively corr with risk-free rate**.
    
    $\frac{\Delta P }{P}=-Modified.Dur \times Yield$
    
    Classic Duration assume spread is zero, and measure only how rf change affect price percentage change
    
    **Empirical Duration admit the negative correlation between rf and spread**, so rf change would be partially deducted by negative spread move, thus RHS side change result in less price percentage change, 
    
    A common way to calculate a bond’s empirical duration is to **run a regression of its price returns on changes in a benchmark interest rate.**
    
    ​	**In sum, Emprical Duration is less than the classic / efficient one.**
    
    - Most of yield changes are from spread changes. (Spread duration should be higher) <- that is the **empirical duration**
    - **Highly rated bond such as gov bond has low credit spread, is mostly affected by benchmark risks has greater empirical duration**  (For high-rated bond, the spread is less sensitive to benchmark rate, rf, increase)bond quality 越低，影响越大。即 low-rate bond 当 rf 提升，即经济好 CB会提升 rf，经济好，违约少，所以 spread 会减少非常大，
      - Investment-grade bonds have lower credit and default risks than high-yield bonds and are **more sensitive** to interest rate changes and credit migration, which cause credit spread volatility. 高质量的债券 对于 interest 和 credit 变化更高
    - **Junk bond or Corporate bond, are less affected by benchmark risks, (they are affected by spread risks), so negative empirical duration**

### Types of Spread

#### Fixed Rate Bonds Spread

- **Benchmark Spread** (Yield Spread) = Yield on Credit Security - Yield on Benchmark Bond
  - use for pricing
  - disadv: might have maturity mismatch **不需要将期限匹配一致**，找最近期的即可
- **G-Spread** = Yield on Credit Security - Yield on Gov Bond
  - disadv: maturity mismatch ( could **use interpolate to estimate the yield**) 用interpolate匹配期限
- **I-Spread** = YTM - Swap Rate
  - swap rate is more flexible and has different maturity then gov bond 也需要用interpolate 匹配期限
- **Asset Swap Spread (ASW)** = Coupon Rate - Swap Rate
  - i.e. corporate bond coupon = 10%。 swap float rate = MRR。把公司 interim payment 转换为对应期限的 swap会有余量即位ASW。如 8% fixed 转换为 MRR，那么 10% coupon <=> MRR + 2%，这2%即为 ASW

- **Z-Spread**: $PV = \frac{PMT}{1+r_1+Z}+ \frac{PMT}{(1+r_2+Z)^2} + \frac{PMT+FV}{(1+r_N+Z)^N}$
  - Parallel shifts of the YTM
- **CDS basis** = CDS spread - Z-Spread
  - <=> CDS fee
- **Option-Adjusted Spread (OAS):** for option embedded bond
  - 剔除了 option 后之后的 spread，用于比较 含权债券和不含权债券

#### Float Rate Bond Spread

The notion of discount margins is applied to floating-rate securities, which pay coupons based on an underlying benchmark such as Libor plus a spread. The value of FRNs is based on uncertain future cash flows as it is not known at purchase what the coupons will be as they fluctuate based on changes in the underlying index. The quoted margin on an FRN is the spread the bond pays above or below the underlying index. The **quoted margin reflects the return required to compensate investors for the credit risk they take on when investing.** If an issuer’s credit risk worsens or improves, the market’s perceptions of the quoted margin will change too. **The difference between the quoted margin and the spread the market now requires for the FRN to trade at par is the discount margin.**

- **QM:** 指的是 coupon 怎么算 a Float Rate Note (FRN) pays interest (coupon) $= MRR + \underbrace{Constant\ Yield\ Spread}_{Quoted Margin}$
  - established upon issuance, not reflect credit risls changes over time 在最开始确定，期间不改变
- **DM**: 指的是 怎么折现 Discount rate = $MRR+DiscountMargin$
  - 在每期reset date，float rate bond 会重置为par
  - DM assumes a flat MRR zero curve
- => $Quoted Margin$ v.s. $Discount Margin$ 相当于 coupon rate  v.s. discount rate
  - QM = DM, at par
  - QM > DM, at premium
- **Z-DM:** Zero-Discount Margin changes based on changes in the MRR forward curve. 
  - In an upward-sloping yield curve, **the Z-DM will be below the DM.**

MRR is based on **current MRR** and therefore implies a **flat** forward curve. 因为不知道未来的 MRR 是多少，所以会假设 flat curve，未来的 MRR 等于现在的MRR

- The yield spread for a corporate bond will be equal to the G-spread if the government benchmark yield curve is flat.

#### Impacts of Yield Spreads on Portfolio Return

Refer to the basic rate

$\Delta P = - D\Delta y + \frac{1}{2}Convexity (\Delta y)^2$

Similarly for Spread

$\%\Delta P = - Spread.D \times \Delta Spread + \frac{1}{2}\times S.Conv \times (\Delta S)^2$

However, **for lower-rated bond**, it is the **percentage of spread change** $\frac{\Delta Spread}{Spread}$would have impact on the price, not absolute basis.对于低评级bond，对价格有影响的是 spread 变动的百分比，而不 spread 变动的数值 

- **Duration Times Spread (DTS)** = $Eff.Spread.Duration \times Spread$
    - 因为 是percentage of spread对price 有影响， 所以为$\frac{\Delta Spread}{Spread}\times (\underbrace{D\times Spread}_{DTS})$

- **Excess Spread Return**

  Similarly, see the underbrace, and we get the following eq

  $Excess\ Spread = Spread/T -Spread.Dur\times \Delta Spread - LGD \times PoD$

  i.e. semi-annual payments means 2 periods per year, so Spread / 2

  if it is half year hodling, then Spread * 0.5
  
  - Instantaneous spread change = $-\Delta Spread \times Eff.Spread.Duration$
  
    Spread * 0

### Credit Strategy

$Spread \approx LGD \times PoD$

#### Bottom-up Credit Strategy

- Relative Value Analysis

    1. Financial Statement analysis, (1) comparability (2) historical data

    2. Two model

        1. Reduced form model, (1) forward not historical (2) use macro and idiosyncratic data
           - Reduced form models solve for default intensity, or the **POD** over a specific time period, using observable company-specific variables such as financial ratios and recovery assumptions as well as macroeconomic variables, including economic growth and market volatility measures. 用回归输入factors 得到 PoD
        2. Structural Credit Model, forward looking PoD
           - Structural credit models use market-based variables to **estimate the market value of an issuer’s assets and the volatility of asset value.** **The likelihood of default is defined as the probability of the asset value falling below that of liabilities.** 估计 Market value of A & L，PoD为 A < L 的概率

    3. Credit Spread => Excess Return

        $\mathbb{E}(Excess S)=S - S.D.\times \Delta S -PoD\times LGD$
        
    
    P.S. Consider (1) other features such as options (2) cost of trading

#### Transaction Cost

For buyer: $Size\times \bigg( TradePrice - \frac{Bid + Ask}{2} \bigg)$

For Seller: $Size\times \bigg( \frac{Bid+Ask}{2} - TradePrice\bigg)$

#### Top-Down Credit Strategy

Choose Sector, broader sector 大类

1. Asscess credit quality
2. Sector allocation

#### Factor-Based Credit Strategy

| Factor    | Rationale                                                    | Measures Used                                                |
| --------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Carry     | Expected Return measure if PoD or Aggregate Risk Premioum is unchanged | OAS                                                          |
| Defensive | Empirical Research suggests that safer low-risk assets deliver higher risk-adjusted returns | Market-based leverage, gross profitability, and low duration |
| Momentum  | Bonds with higher recent returns outperform those with lower recent returns | Trailing six-moth excess bond and equity returns             |
| Value     | Low market value versus fundamental value indicates greater than expected return | Bond Spread less default probability measure, which includes rating, duration, and excess return volatility |

ESG: (1) screen negative or positive, (2) filter charactireistics and invest the best-in-class, (3) directly fund , green bond 

### Risks

#### Liquidity Risks and Tail Risks

##### Liquidity Risks

Liquidity depends on 5 factors: (1) issuer's quality (2) creidt quality (3) issue frequency (4) issue size (5) maturity

Measure of Secondary Market Liquidty Risks

- use US data
- Trading Volume: 越高，liquidty risks 越小
- Spread Sensitivity to fund outflows 对于资金链收紧的敏感度越高，liquidty risks 约啊大
- Bid-ask Spreads： spread越大，risks越大

##### Tail Risks

- VaR: however VaR might be misleading
- CVaR, expected shortfalls
- Incremental VaR 当组合变化时 VaR 如何变化
- Relative VaR (relative amount, instead of the absolute amount like VaR and CVaR)

Three methods:

- Parametric Method, drawbacks: non-normally dist
- Historical Simulation, drawbacks: depends on historical data
- Monte Carlo, drawbacks: depends on assumptions

---

## Synthetic Credit Strategy: CDS 

CDS buyer 买 CDS 相当于买了保险，会在每期付"保费" fixed payment，为固定金额 1% or 5%。

CDS Spread 为实际上值多少钱，如实际上值 1.75%，但是每期只固定付 1%，那么就要在inception 付 upfront premium

- buy protection means pay fixed payment, gaining a protect. short the credit risks 
- sell protection means receive fixed payment, have obligation to pay while default. Long the credit risks

Fixed CDS Coupon 为标准化的 investment-grade = 1%, high-yield bond = 5% 。所以 实际的情况与标准的差值将作为 upfront fee 在前期支付，差值折现后求和，为 CDS quoted price。

CDS is quoted on a Issuer's CDS Spread = PV of difference between CDS Spread & Fixed Coupon

- If CDS Spread > Fixed Coupon, then **protection buyer pays the upfront premium**. Amount: $(CDS \ Spread - Fixed\ Coupon)\times Eff.Spread.Dur_{CDS}$

- Single-Name CDS,   long or short single name CDS
- Index-Based CDS,   for index-based
- Payer Option on CDS index, short CDS index-based credit spread exposure
- Receiver Option on CDS index, long CDS index-based credit spread exposure
- Sample Text:

  **Selling protection** on the CDX index is a “**long” credit spread risk position**, while purchasing protection on the CDX Financials subindex is a “short” credit spread risk position, leaving the investor with a long index position without exposure to financial reference entities in the CDX index. Both A and C increase exposure to financial sector issuers.

#### CDS Price

$CDS \ Price = NP\times \bigg[ 1+(FixedCoupon-CDS\ Spread)\times Eff.Spread.Dur_{CDS} \bigg]$

#### CDS Risk Position

Sample Text: **Selling protection on the CDX index is a “long” credit spread risk position,**  因为预期credit rating会提升，所以sell CDS protect是去赚钱。while purchasing protection on the CDX Financials subindex is a “short” credit spread risk position, leaving the investor with a long index position without exposure to financial reference entities in the CDX index. 

#### Spread Curve CDS Strategy

Same for the yield curve movement。如果expected steepening of the investment-grade credit spread curve，相当于credit spread curve twists, 长期 spread提升，短期变小。长期提升意味着 长期credit变差，所以 long long-term

a synthetic credit roll-down strategy involves **selling protection using a single-name CDS contract for a longer maturity.** 因为卖protection 收到更多 CDS spread，到短期PoD变小了，收到的Spread将会变小

- 当经济收缩时最好的策略：An **economic contraction** is often associated with a sharp rise in shorter-term high-yield spreads and spread curve flattening in investment grade and inversion in high yield
  - the most appropriate choice is to take a short risk (purchase protection) in five-year high-yield spreads and a long position (sell protection) in five-year investment-grade spreads. 
- **flight to quality**:  refers to the tendency of investors to move their money out of riskier asset classes (like technology stocks) and **into more stable asset classes (like government bonds)** during bear markets, recessions, periods of high inflation, and other times of economic uncertainty. 预期经济变糟，转入gov bond

### Global Credit Strategy

- Developed Market: Fixed-income markets usually have well-established and liquid derivative and other capital markets.
- **Emerging or Frontier Market:** face concentrated risk; have a restricted domestic currency with varying degrees of liquidity,
  - Emerging market credit is characterized by **a concentration in commodities and banking and government ownership of some entities.**
  - **Global investment provides diversification**: some differences across regions in the credit cycle providing diversification.

P.S.

-  MBS expects lower, not higher, volatility.
