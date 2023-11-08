# Fixed-Income

## Overall

### Roles of Fixed Income in Portfolio

- **Diversification**. We may focus on how bonds **correlate** with equities. 

    1. Corr between bonds and equities might not be "1", is less than "1"
    2. **In the Stress Periods**, correlation 
        - decrease between government and equity
        - increase between high yield bond and equity
    3. Less volatile than equity

- **Manage Cash Flows** to meet obligations such as Tuition Fees, Pension, etc

- Hedge for **Inflation**

    ![Screenshot 2023-11-08 at 08.58.01](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-08%20at%2008.58.01.png)

### Classify the Fixed-Income Mandates

- **Liability Based** 为了满足 lia 需求，如 tuition fees
    1. Duration matching
    2. CF matching
    3. Derivatives Overlay
    4. Contingent Immunisation
- **Total Return** 为了挣 return

#### Liability Based Mandate

Bonds earn: (1) Coupon (2) Reinvestment (3) Price Changes

其中 Coupon 是固定的，但是 Reinvestment 和 Price Changes 受interest rate变动

因为 if interest rate increase, then (1) reinvestment return increase (2) price changes negative 所以，如果(1) & (2) 可以抵消，那么Duration matching 达成， Immunisation

- **Price Risks <- measured by Duration** 
- **Reinvestment <- measured by Horizon** 

So, we need to let 

$Duration = Horizon$

##### Duration (Classic Immunisation)

###### For Single Lia Immunisation

1. Portfolio Duration = Liability Duration
2. PV of Port = PV of Lia

Horizon 指的是 liability duration 负债的duration = 负债的到期日

- If $Port Duration < Horizon$: 如果 hold to maturity，那么不受 price risks 影响。但是受 reinvestment risk 影响大，因为
- If $Port Duration > Horizon$: 在收到 interim CF 之前就给买了，所以investment horizon小，那么受制于 reinvestment risks 小，因为没 reinvest 就卖了，反而受 price risks 影响大
- If $Port Duration = horizon = Lia Matuiry$, then Great

**Immunisation Risks**: 

- 此策略不能 cover Non-parallel changes **in interest rate** 因为 duration 衡量的是 利率的平行移动，所以如果不平行移动，则 duration match 失效
    - bond 的 CF流入有 (1) Barbell 两边流入多，中期流入少，易受 non-parallel shifts 影响 (2) Bullet 仅一期大的流入，受 non-parallel shifts 影响小。**In sum， invest 更多bullet bonds**
    - $Convexity = \frac{Mac.Dur^2 + Mac.Dur + Dispersion}{(1+yield)^2}$ 如果 dispersion越大，相当于 barbell，受收益率曲线 非平行移动（斜率变）影响大。If dispersion 大 =>  Convexity 大。 **所以 降低 portfolio's convexity 可以降低 non-parallel shift 影响**
- Duration 会变化 （time 变化， interest rate 变化，会使Duration变化）
    - **定期 rebalance 去平衡 duration 变化的影响**
- 只匹配了 duration ，没有 匹配 convexity
    - 没啥解决办法，忽略 convexity

###### For Multi-Liabilities Immunisation

1. $PV_A = PV_{Lia}$
2. $Duration_A = Duration_{Lia}$
3. （增加一条 for multi-lia ）$Range_{A} > Range_{Lia}$ 资产的周期要能覆盖 lia port的周期，为了保证最后一期有足够的现金流能 cover liability payments

##### Cash Flow Matching

先 cover 最后一笔负债，从后往前一层一层的剥离。先匹配长期的bond 是因为 买 asset 匹配长期的 lia 的时候，asset也会产生 interim cf，那么在匹配短期的时候，这些cf inflow将被合并考虑

![Screenshot 2023-11-08 at 10.13.35](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-08%20at%2010.13.35.png)

![Screenshot 2023-11-08 at 10.12.55](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-08%20at%2010.13.10.png)

Pros: 精确度高，可以很好匹配现金流 

Cons: 成本高，因为要买匹配日期的 bonds，若没有匹配的，只能买提前到期的bond，那么会损失提前到期日和pay lia日之间的时间价值

##### Contingent Immunisation

Allow active management for the surplus amount of assets over liability

##### Derivatives Overlay

Using Derivatives to adjust the duration of liability portfolio 用于调整 duration 不用于构建 asset portfolio

#### Total Return Mandates (Index Based)

因为 bond liquidity 比 equity 的低，所以mimic index bonds by purchasing the same bonds 可能比较难以操作。 所以 mimic returns

Risks:

- **Interest Rate Risks**: exposure to parallel shift in the Yield Curve. Measured by **Portfolio Duration**
- **Spread Risks**: exposure to changes in spreads between Treasuries and non-Treasuries. Measured by **Spread Duration**.
    -  (YTM = Benchmark Yield + Spread), so spread 涨1%带来的YTM 增加与 Benchmarked涨1%带来的YTM增加一致。thus spread duration = portfolio duration，as 都通过YTM影响 price
    - P.S.国债没有 spread
- **Yield Curve Risks**: exposure to a twist in the Treasury Yield Curve. Measured by **Key Rate Duration & PV of Distribution of CF**
- **Credit Risks**: exposure to downgrades and defaults. Measured by contribution to **duration by credit rating**
- **Optionality Risks**: exposure to changes in CF due to call/put features. Measured by **Portfolio Delta**

**Mandates:**

- Pure Indexing
- Enhanced Indexing
- Active Management