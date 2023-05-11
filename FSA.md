## Financial Statement Analysis

### Financial Asset  < 20%

FVTPL, FVOCI, Amt Cost   <->  Trading Security, AFS, HTM

| Type             | FVTPL                                                        | FVOCI                                                        | Amt Cost                             |
| ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------ |
| Balance Sheet    | Fair Value                                                   | (1) Fair Value, <br /> (2) 未实现的 Unrealised G/L 进 OCI, <br />(3) 仅IFRS中，投资foreign bond的外汇变动可以进I/S | Amortised Cost                       |
| Income Statement | (1) Interest, <br />(2 )Dividend, <br />(3) Realised/Unrealised G/L | 已实现的 <br />(1) Interest, <br />(2) Dividend, <br />(3) Realised G/L | (1) Interest, <br />(2) Realised G/L |

#### Classification

- Amortised Cost - Debt
- FVTPL - D&E hold for trading
- FVOCI - D&E 垃圾桶

#### Reclassification

- Equity 一律不能重分类
- Debt:
    - Amt Cost + FVTPL 可以重分类
    - FVOCI 垃圾桶不能重分类

### Equity Method - Associate (Investment in Associate)	

1. **Valuation by BASE rule**

   - B/S: BASE: $ Begining + NI\times \% - Div\times \% = End $

   - I/S: $Inv.Income = NI \times \%$


​	Cost 拆分: BV+ FV.appreciation + G.W.

​	NI: 将 BV 调整为 FV, so $NI: \quad BV\to FV$

2. **NI: 剔除 Unrealised Profit 内部交易带来的 (顺流逆流) 未实现的**
   - **PPE (Fair Value - Book Value) / # Yr * %**

#### Valuation by Fair Value Option

如果不用BASE，而使用Fair Value核算，只能在初始计量时选择，irrevocable，之后不能再调整了。

#### Impairment

|            | IFRS                                                         | USGAAP                        |
| ---------- | ------------------------------------------------------------ | ----------------------------- |
| Impairment | recoverable amount = max ( disposal value, value in use )<br />Carrying Amount 比 Recoverable Amount<br />差值为 valuation allowance 和 impairment loss | Fair Value 比 Carrying Values |

Reversal is prohibited. 都不能转回

### Business Combination - Acquesition Method

- Merger: A + B = A （吸收）
- Acquisiton: A + B = (A+B) 只有此种情况才涉及 合并报表。
- Consolidation: A + B = C

#### Control <- B/S

A 保持 Book Value， B 用 Fair Value。资产 和 负债 都100%合并，Asset放需要 减Payment。Equity不合并，倒挤。

Asset = $BV.A_母$ - Purchase Pirce + Goodwill (Partial/Full) + $FV_子$

Lia = $BV.Lia_母$ + $FV_子$

Equity = $BV.E_母$ + Minority Interest

- IF: Payment <= Equity (FV) of B， 则 B的Equity被记为 Minority Interest
- IF: Payment > Equity (FV) of B， 则超出部分记为 Goodwill 

- Full Goodwill = Partial Goodwill / %, Minority Interest 要随之调整，先算partial 再拿 % 反推
  - Full Goodwill 在 IFRS 和 USGAAP都可
  - **Partial Goodwill 仅在 IFRS**

#### Income Statement

- Equity Method = NI 母 + Equity Income (= NI被投 * %)
- Acquisiton Method = NI母 + 100% NI子 -  Non-own/Minority NI (1-%  * NI子)

母 子 的都加起来，最后调 non-own NI

 BV -> 调整为 -> FV 后，最后的 Fair Value of NI 乘 %

- Inventory  ->  COGS
- Fixed Asset  ->  **D**&A
- Intangible Asset  ->  D&**A**

### Goodwill

Goodwill's Impairment 来自被收购的公司 是否有减值

##### IFRS (One Step)

Recoverable Amount = Max( Disposal Value, Value in Use )

Carrying Amount 比 Recoverable Amount 。如果小了，先减少Goodwill。

如果Goodwill减到 0 了，则 pro rate 减其他的 asset

##### USGAAP (Two Steps)

Step1. 减值测试： Carrying Value > Fair Value，如果有，则确定要减，减多少由step2算出

Step2. 减少多少：Impairment Loss = Implied Fair Value (如果当前重新再收购一次公司计算的值) 比 Carrying Amount

### Equity Mehtod -> Acqusition Method

NI 不变， 但是

Equity 增加 -> ROE 下降

Asset 增加 -> ROA 下降

Sales 增加 -> Net Profit Margin 下降

### SPE 在海外设立的的 子

- **IFRS 都合并**

- USGAAP 

  - If VIE 则合并 Variable Interest Entity
  - If 不是 VIE，不合并

  VIE 的判断条件：（满足其一即是VIE, variable interest entity，VIE 相当于没有投票权的实体）

  - Not make descision
  - Not able to absorb losses
  - Not able to receive returns

### Employment Compensation

#### Pension

DC plan 没有 PBO PA。只有 DB Plan 有

##### PBO -基于退休前的工资算得  DB

20岁开始工作，60岁退休，活到80，每年2000。工作40年，拿退休金20年

1. 在 t = 60，PMT = 2000, N = 20, I/Y = 10, FV = 0, **solve** PV
2. 把 t = 60 的PV，除以 40，得到现在每工作一年，可以获得在 t = 40时现值的 pension。$Annual UnitCredit = \frac{PV\ at\ t=60}{40}$
   - AUC 是未折现概念
3. 之后每工作一年，Annual Unit Creidt * n
4. Discount Rate = current rates of return on high-quality corporate bonds (or government bonds, in the absence of a deep market in corporate bonds) with currency and durations consistent with the currency and durations of the benefits.

![image-20230511133911835](/Users/mie/Library/Application Support/typora-user-images/image-20230511133911835.png)

##### ABO -与PBO一样，除了是基于当前工资算得

因为算法与 PBO完全一样，所以   退休前工资/当前工资 = PBO/ABO

#### B/S 核算 - Funded Status (USGAAP, IFRS 一致)

##### Plan Asset - BASE

$$ PA_t = PA_{t-1} + EmployerContribution - Benefit PaidtoEmployee $$

##### PBO

$$PBO_t = PBO_{t-1} + CSC + Int.Cost + PSC \pm Actuarial \ L/G - BenefitPaid$$

- CSC - Current Service Cost
  - CSC = AUC / (1+r)^t  把annual unit cost 折现

- Interest Cost = $PBO_{t-1} \times r$
- PSC - Past Service Cost - Plan Amendment during the Year. 如本来按最后一年工资的1%给，现在按2%给，带来的变化
- Actuarial Losses / Gain

##### Funded Status

$FundedStatus = PA - PBO$, overfunded if FS>0, vice versa.

Funded Status = Net Pension Liability (-) / Net Pension Asset (+)

PBO = PVDBO

- On the B/S, F.S. is reported as the lower of the Net Pension Asset/Lia & the **Ceiling**.
  - Ceiling: the present value of future economic benefits, such as refunds from the plan or reductions of future contributions

#### I/S 核算

##### IFRS

- CSC
- PSC
- Int.Cost = PBO_{t-1} * r
- Int.Income = - PA_{t-1} * r

P.S. 

1. Actuarial G/L 进 OCI
2. Remeasurement = Acutal Return - Int.Income 进 OCI

##### USGAAP

- CSC
- Int.Cost
- \-  E(R) = PA * E(r)    Expected Return
- **Amortisation** of PSC & Actuarial G/L

P.S. 

1. Un-amortised PSC & Acturial G/L 进 OCI
2. Actuarial G/L 的摊销 不考

#### Actuarial Assumption 精算假设改变，对报表的影响

- Discount Rate, $r \uparrow$
  - B/S: $r \uparrow,  \quad PBO\downarrow ,\quad F.S. \uparrow$ 
  - I/S: $r\uparrow \quad and\quad CSC\downarrow \quad Int.Cost = PBO_{t-1}\times r$ 一般PBO下降的幅度高于，r上升的幅度，所以 Int.Cost 下降
- Growth, $g \downarrow$, => 退休前工资 下降
  - B/S: $PBO\downarrow ,\quad F.S. \uparrow$
  - I/S: $CSC\downarrow \quad and\quad Int.Cost \downarrow$
- $E(r) \uparrow$ (USGAAP only)
  - I/S: $PensionExpense \downarrow$, so NI up
  - B/S: unaffected

#### Analyst View

##### Total Periodic Pension Cost - TPPC: I/S cost + OCI cost

$$TPPC = \Delta F.S. - Contribution$$

##### 调整 I/S

- CSC              -> SG&A
- Int.Cost         -> Int.Exp
- -E(r)               -> Int.Income
- Amt.PSC       -> Non-Operating
- Actuarial G/L -> Non-Operating

##### 调整 CF/S

Contribution 代表 CFF

TPPC 代表 CFO 因为pension确实是应该划入operating CF

- Contribution > TPPC

  Over Contribtuion: CFF调低，CFO调高

  contribution 相当于 实际往pension里投的钱，TPPC相当于应该跟pension花的钱。实际花的更多，相当于其中一部分还给 pension ，相当于往CFO里注入资金

  - Contribution <-> CFF多了，调减CFF

- Contribution < TPPC

  Under Contribution: CFF调高，CFO调低

  相当于 融资的钱contribute 不够还给pension应该花的钱，所以往CFO借钱。

  - Contribution <-> CFF少了，调增CFF (CFF inflow 增加 outflow减少)

- 总的来说，TPPC代表CFO outflow （因为这个指标设计的意义就是把 pension 相关的进I/S & OCI 的expense 调回到 NI 中）。我们要做的是把 contribution 向 TPPC 调齐。tppc小，则把 contribution 调小，即把 CFF 调小。

- 调整的amount: $(Contribution -TPPC)\times (1-t)$ 差额要扣税调整

Another set of explanations

- If a sponsoring company’s periodic **contributions** to a plan **exceed** the total pension costs of the period, the **excess** can be viewed from an economic perspective as a **reduction of the pension obligation**. The contribution covers not only the pension obligation arising in the current period but also the pension obligations of another period. **Such a contribution would be similar in concept to making a principal payment on a loan in excess of the scheduled principal payment.**  
  - **所以 CFF 减少， 所以 CFF outflow 增加，或CFF inflow减少。 CFF减少，流入CFO**

- Conversely, a periodic contribution that is less than the total pension cost of the period can be viewed as a source of financing.  
  - **所以CFF 增加**


### Share-Based Compensation

#### Call-Option

将 option fair value 在 GrantDate-VestingDate之间摊销，按month

compensation expense for restricted stock grants is measured as the fair value (usually market value) of the shares issued at the grant date. This compensation is allocated over the employee service period

按 grant date 的 fair value 算价格， 然后摊销

#### Greeks

E.G. Volatility 提升，Option Value 提升, NI 下降

#### Stock Grant

不受 volatility影响，有vesting period

### FX Transaction

- Reporting Currency - 母公司用的货币 USD
- Local Currency - 子公司所在国家的货币 JPY
- Functional Currency - 子公司开展业务的货币 如在日本做CNY交易

如果 母&子 结合紧密，则 FC = RC，用temporal method，有T.G/L

如果 子 独立，则子用 Current Rate Method，有OCI

IFRS requires that Ambleu disclose “the amount of exchange differences recognized in profit or loss” when determining net income for the period. Because companies may present foreign currency transaction gains and losses in various places on the income statement, it is useful for companies to disclose both the amount of transaction gain or loss that is included in income as well as the presentation alternative used.

#### Temporal Method - Exposure 来自 Monetary

$Local Currency \to Functional Currency: Local. GBP \to Funcational. USD$ 用于更**不**自主和不独立的子

先 B/S 再 I/S

1. B/S 折算
   1. Asset
      - Monetary Asset: Current Rate
      - Non-monetary Asset: Historical Rate (Inventory, Fixed Asset, etc)
   2. Liability 基本上所有 lia 都是monetary，除非题目有说明
      - Monetary Asset: Current
   3. Equity (A - Lia)
      - Capital: Historical 
      - R/E: 倒挤 Equity - Capital
      - P.S. 这个方法没有OCI
2. I/S 折算 - 由 R/E _t  - R/E _t-1 倒挤出
   1. 由 1.2.的items 算出 NI before Translation G/L
      - COGS, D&A: Historical Rate
      - Others: Current
      - NI before Translation G/L
   2. 用 BASE,  $R/E_{t-1} + NI - Div = R/E_t$
      - R/E t-1 来自上年
      - Div 宣告日 declaration date
      - R/E t 由 B/S算出
      - 反推出 NI after Translation G/L
   3. 两个 NI 的差额，即为 Translation G/L

##### 判断 T.G/L  <-  Exposure

$Exposure = M.A - M.L$, Exposure 来自 Net Monetary. Monetary A & Monetary L 哪个多，哪个易受 current FX rate影响。

因为在temporal method下，non- monetary 不受FX rate change影响，所以只考虑 Monetary的

- $Exposure >0 \to M.A >M.L$, 则 Asset 多。FX 涨 exposure 涨, Gain，vice versa
- $Exposure < 0 \to M.A < M.L$, 则 Lia 多。FX 涨 exposure 跌, Loss，vice versa

#### Current Rate Method - Exposure 来自 Equity 

$FunctionalCurrency \to Reporting Currency: Local.GBP\to Reporting .GBP$

用于更加自主的 subsidies. The current rate method is utilised in instances where the [subsidiary](https://www.investopedia.com/terms/s/subsidiary.asp) isn't well integrated with the parent company, and the local currency where the subsidiary operates is the same as its [functional currency](https://www.investopedia.com/terms/f/functional-currency.asp). The current-rate translation method is ideal if the subsidiary is mainly independent of the parent company’s activities. It also applies where the functional and local currencies are the same.

先折算 I/S 再折 B/S

1. I/S折算 -> average rate -> NI (记得用 期间平均 rate)
2. B/S折算: 
   1. Assets: Current Rate
   2. Liability: Current Rate
   3. Equity: 
      - **Capital: Historical** 
      - R/E: BASE:  $R/E_{t-1}+NI - Div = R/E_t$  
        - R/E t-1 来自上期报表
        - NI 来自 1 用 average rate折算
        - Div 为 div declare date 的当时rate
        - R/E t用前几个 deduce
   4. **OCI 倒挤**

#### Temoral Method & Current Rate Method

- FX Depreciation: H > A > C  , *vice versa*

E.G.

|                                        | Temporal Method | Current Rate Method |
| -------------------------------------- | --------------- | ------------------- |
| $F.A. Turnover = \frac{Revenue}{F.A.}$ | $\frac{A}{H}$   | $\frac{A}{C}$       |
| If FX depreciation                     | $H$ 大          | $C$                 |

#### Hyper-Inflation

- 复利 三年 > 100%
- 每年 > 26%

USGAAP 不管 依然是 temporal method

IFRS:

- Monetary Item: 不用调整，依然用 current rate
- Non-Monetary Item, Equity, I/S/ Items: 根据物价变化重溯
  1. Restate
  2. 重新折算
- 不进 OCI，直接进 I/S

如何抗通胀？

1. Asset
   - 买海外资产
   - 买 non-monetary asset
2. Lia
   - 加杠杆 借钱，增加lia，因为钱便宜了

### Intefration of Financial Statement Analysis

#### DuPont 5

$ROE = \frac{NI}{EBT}\times \frac{EBT}{EBIT}\times \frac{EBIT}{Rev}\times \frac{Rev}{A}\times \frac{A}{E}$

当去除Equity Inv的影响

- Tax Burden = $\frac{NI - Equity Income}{EBT}$
- Total Asset Turnover $= \frac{Rev}{A-Equity Inv}$

#### Earning Quality <- Accrual 企业可操纵的部分

- Cash 多，好（财报质量高），cash不好操纵
- Accrual多，不好，可被操作
- 所以, Accrual ratio 越大越不好

1. B/S Approach

​	$NOA(Net.OA) = Operating.A - Operating.L$

​	$NOA_{B/S} = \bigg( Total.A - Cash-Securities \bigg) - \bigg( Total.L - Debt \bigg)$。 其中cash，security 和debt都是不可操纵的，减去。那么剩下的就是Earning中易被操纵的部分。

​	$AggregateAccrual = \Delta NOA = NOA_t - NOA_{t-1}$

​	$Accrual Ratio = \frac{\Delta NOA}{(NOA_0+NOA_1)/2}$, 流量比存量，存量ave

2. CF/S Approach

   $Accrual_{CF/S} = NI - \bigg( CFO+CFI \bigg)$

   $Accrual Ratio = \frac{NI-(CFO+CFI)}{(NOA_0+NOA_1 )/2}$。 依然，流量比存量，存量ave

3. Reduced Form 

​	$Earning_{t+1} = \beta_0 +\beta_1 Cash + \beta_2 Accrual +error$

​	$\beta_1$ 越大越好，$\beta_2$ 越小越好

4. Accrual 内的分类 Discretionary自主的多，则manipulation多

​	Earnings with a larger component of accruals are typically less persistent and of lower quality. An important distinction is between accruals that arise from normal transactions in the period (called non-discretionary) and accruals that result from transactions or accounting choices outside the normal (called discretionary accruals). The discretionary accruals are possibly made with the intent to distort reported earnings. Outlier discretionary accruals are an indicator of possibly manipulated—and thus low quality earnings. Thus, Martinez is primarily focused on discretionary accruals, particularly outlier discretionary accruals (referred to as abnormal accruals).

we need to pay attention to the increase on absolute terms, not if it is +ve or -ve. 只要绝对值变大了，哪怕是越来越负了，也意味着accrual变多了

##### 财报质量

- Higher growth in revenue than that of industry peers is an accounting warning sign of potential overstatement or non-sustainability of operating income. 
- Shortening the depreciable lives of capital assets is a conservative change and not a warning sign. 
- An increase (not a decrease) in discounts and returns would be a warning sign.

#### CF Analysis

- CFO & NI

  - 因为CFO中扣了tax，所以与NI比时加回来

    CFO + I + T = CFO before I&T 与NI比

### Financial Institute

#### BASEL

Basel III (2018) consider the liquidity

#### CAMELS

- Calpital Adequacy
  - Tier 1: Common Stock, R/E, AOCI; Other Tier 1: Preferred Stock; Tier 2: Long-term Debt
  - Common Equity Tier 1 - 4.5%
  - Total Tier 1 Capital: - 6%
  - Total Capital (Tier 1 + Tier 2) - 8%
- Asset Quality: Liquidty Asset %
- Mabagement Capability
- Earning
  - Earning 来源: 1. Net Interest Income 借贷利差 2. Trading Income 投资收益 3. Service Income 服务费
  - 其中 Trading Income 是 Low Quality 因为 highly Volatile
- Liquidity Positions
  - Liquidity Coverage Ratio (流动性覆盖率) = $\frac{HihglyLiquidyAssets}{Bank's ExpectedCFoutflow (压力测试下30天流出的钱)}$
  - Net Stable Funding Ratio (NSFR) = $\frac{Stable Funding}{Bank'sRequiredStable Funding}$
- Sensitivity to Market Risks
  - Exposure to Market Movement 期限错配
    1. Mismatch in Duration of Loan
    2. Reference Rating
    3. Currency
    4. Prepay Frequency
  - VaR

#### Insurance Company

No Capital Adequacy requirements.  

Aims to Protect Adverse Events

- Rev 来源: 1. Premium 保费 2. Float 浮存金

- P&C 财险 L&H 寿险

| Types               | P&C                          | L&H                       |
| ------------------- | ---------------------------- | ------------------------- |
| Duration            | Short                        | Long                      |
| Predicability       | Variable, Lumpier            | High                      |
| Business Profile    | Loss on Property             | On Death & Saving Vehicle |
| Invest Return       | Conservative 因为难预测+短期 | High Return               |
| Liqidity            | High Liquid                  | Low                       |
| Capital Requirement |                              |                           |

- Profitability - ratio 都是越小越好

  1. Loss and Loss Adj Ratio $=\frac{LossExp + LossAdj Exp}{Net Premium Earned}$

     越小越好，表示同样premium收入，费用（Loss.Exp理赔费用+Loss.AdjExp其他费用）越少

     Implication: Indicate the **Degree of Success in Estimating risk Insured**

  2. Underwriting Expense Ratio 承保费用 $= \frac{Undertaking Exp}{Net Premium Written} $

     越小越好

     Indicate the Efficiency of Money Spent in obtaining **new Premium**

  3. Combined Ratio = 1 + 2

     <1则effective

### Evaluating Quality of Financial Report

#### Qunantitive Tools

1. Beneath Model 用 reg model to estimate prob of Earning Manipulation

   - M-Score > **-1.78** 操纵，empirical statistical result 别问为啥

2. Altman Model

   - Z-score < 1.81  Bankrupt
   - Z-score > 3      no Bankrupt
   - between  (1.81, 3) unknown


- ROIC -  Return on invested capital is net operating profit minus adjusted taxes divided by invested capital, where invested capital is defined as operating assets minus operating liabilities. $ROIC = \frac{NetOperatingProfit - Adj.Tax}{OperatingA - OperatingL}$
- ROI = EBIT / Capital Expenditure