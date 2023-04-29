## Financial Statement Analysis

### Financial Asset  < 20%

FVTPL, FVOCI, Amt Cost   <->  Trading Security, AFS, HTM

| Type             | FVTPL                                                        | FVOCI                                                        | Amt Cost                             |
| ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------ |
| Balance Sheet    | Fair Value                                                   | (1) Fair Value, <br /> 未实现的 (2) Unrealised G/L 进 OCI, <br />(3) 仅IFRS中，投资foreign bond的外汇变动可以进I/S | Amortised Cost                       |
| Income Statement | (1) Interest, <br />(2 )Dividend, <br />(3) Realised/Unrealised G/L | 已实现的 <br />(1) Interest, <br />(2) Dividend, <br />(3) Realised G/L | (1) Interest, <br />(2) Realised G/L |

#### Classification

- Amortised Cost - Debt
- FVTPL - D&E hold for trading
- FVOCI - D&E 垃圾桶

#### Reclassification

Equity 一律不能重分类

Amt Cost + FVTPL 可以重分类

FVOCI 垃圾桶不能重分类

### Equity Method - Associate (Investment in Associate)	

#### Valuation by BASE rule

- B/S: BASE: $ Begining + NI\times \% - Div\times \% = End $
- I/S: $Inv.Income = NI \times \%$

#### Cost 拆分: BV+ FV.appreciation + G.W.

#### NI: 将 BV 调整为 FV, so $NI: \quad BV\to FV$

#### NI: 剔除 Unrealised Profit 内部交易带来的 (顺流逆流) 未实现的

#### Valuation by Fair Value Option

如果不用BASE，而使用Fair Value核算，只能在初始计量时选择，irrevocable，之后不能再调整了。

#### Impairment

|            | IFRS                                                         | USGAAP                       |
| ---------- | ------------------------------------------------------------ | ---------------------------- |
| Impairment | recoverable amount = max ( disposal value, value in use )<br />Carrying Amount 比 Recoverable Amount<br />差值为 valuation allowance 和 impairment loss | FairValue 比 Carrying Values |

Reversal is prohibited. 都不能转回

### Business Combination - Acquesition Method

- Merger: A + B = A （吸收）
- Acquisiton: A + B = (A+B) 只有此种情况才涉及 合并报表。
- Consolidation: A + B = C

#### Control <-

A 保持 Book Value， B 用 Fair Value。资产 和 负债 都100%合并，Asset放需要 减Payment。Equity不合并，倒挤。

- IF: Payment <= Equity (FV) of B， 则 B的Equity被记为 Minority Interest
- IF: Payment > Equity (FV) of B， 则超出部分记为 Goodwill

- Full Goodwill = Partial Goodwill / %, Minority Interest 要随之调整，先算partial 再拿 % 反推
  - Full Goodwill 在 IFRS 和 USGAAP都可
  - Partial Goodwill 仅在 IFRS

#### Income Statement

从 BV -> 调整为 -> FV 后，最后的 Fair Vlaue of NI 乘 %

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

- IFRS 都合并

- USGAAP 

  - If VIE 则合并
  - If 不是 VIE，不合并

  VIE 的判断条件：（满足其一即是VIE, variable interest entity，VIE 相当于没有投票权的实体）

  - Not make descision
  - Not able to absorb losses
  - Not able to receive returns

### Employment Compensation

#### Pension

##### PBO -基于退休前的工资算得  DB

20岁开始工作，60岁退休，活到80，每年2000。工作40年，拿退休金20年

1. 在 t = 60，PMT = 2000, N = 20, I/Y = 10, FV = 0, **solve** PV
2. 把 t = 60 的PV，除以 40，得到现在每工作一年，可以获得在 t = 40时现值的 pension。$Annual UnitCredit = \frac{PV\ at\ t=60}{40}$
3. 之后每工作一年，Annual Unit Creidt * n

##### ABO -与PBO一样，除了是基于当前工资算得

因为算法与 PBO完全一样，所以   退休前工资/当前工资 = PBO/ABO

#### B/S 核算 - Funded Status (USGAAP, IFRS 一致)

##### Plan Asset - BASE

$$ PA_t = PA_{t-1} + EmployerContribution - Benefit PaidtoEmployee $$

##### PBO

$$PBO_t = PBO_{t-1} + CSC + Int.Cost + PSC \pm Actuarial \ L/G - BenefitPaid$$

- CSC - Current Service Cost
- Interest Cost = $PBO_{t-1} \times r$
- PSC - Past Service Cost - Plan Amendment during the Year. 如本来按最后一年工资的1%给，现在按2%给，带来的变化
- Actuarial Losses / Gain

$FundedStatus = PA - PBO$, overfunded if FS>0, vice versa.

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
- Amortisation of PSC & Acturial G/L

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
  - I/S: $PensionExpense \downarrow$
  - B/S: unaffected

#### Analyst View

##### Total Periodic Pension Cost - TPPC: I/S cost + OCI cost

$$TPPC = \Delta F.S. - Contribution$$

##### 调整 I/S

- CSC      -> SG&A
- Int.Cost -> Int.Exp
- -E(r)       -> Int.Income
- Amt.PSC     ->  Non-Operating
- Acturial G/L ->  Non-Operating

##### 调整 CF/S

Contribution 代表 CFF

TPPC 代表 CFO 因为pension确实是应该划入operating CF

- Contribution > TPPC

  Over Contribtuion: CFF调低，CFO调高

  contribution 相当于 实际往pension里投的钱，TPPC相当于应该跟pension花的钱。实际花的更多，相当于其中一部分还给 pension ，相当于往CFO里注入资金

- Contribution < TPPC

  Under Contribution: CFF调高，CFO调低

  相当于 融资的钱contribute 不够还给pension应该花的钱，所以往CFO借钱。

- 调整的amount: $(Contribution -TPPC)\times (1-t)$ 差额要扣税调整

### Share-Based Compensation

#### Call-Option

将 option fair value 在 GrantDate-VestingDate之间摊销，按month

#### Greeks

E.G. Volatility 提升，Option Value 提升, NI 下降













### FX Transaction

- Reporting Currency - 母公司用的货币 USD
- Local Currency - 子公司所在国家的货币 JPY
- Functional Currency - 子公司开展业务的货币 如在日本做CNY交易

如果 母&子 结合紧密，则 FC = RC，用temporal method

如果 子 独立，则子用

#### Temporal Method

$Local Currency \to Functional Currency$

先 B/S 再 I/S

1. B/S 折算
   1. Asset
      - Monetary Asset: Current Rate
      - Non-monetary Asset: Historical Rate
   2. Liability 基本上所以 lia 都是monetary，除非题目有说明
      - Monetary Asset: Current
   3. Equity (A - Lia)
      - Capital: Historical 
      - R/E: Equity - Capital
      - P.S. 这个方法没有OCI
2. I/S 折算
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

$Exposure = M.A - M.L$

因为在temporal method下，non- monetary 不受FX rate change影响，所以只考虑 Monetary的

- $Exposure >0 \to M.A >M.L$, 则 Asset 多。FX 涨 exposure 涨, Gain，vice versa
- $Exposure < 0 \to M.A < M.L$, 则 Lia 多。FX 涨 exposure 跌, Loss，vice versa

#### Current Rate Method

$FunctionalCurrency \to Reporting Currency$

先折算 I/S 再折 B/S

1. I/S折算 -> average rate -> NI
2. B/S折算: 
   1. Assets: Current Rate
   2. Liability: Current Rate
   3. Equity: 
      - Capital: Historical 
      - R/E: BASE:  $R/E_{t-1}+NI - Div = R/E_t$  
        - R/E t-1 来自上期报表
        - NI 来自 1 用 average rate折算
        - Div 为 div declare date 的当时rate
        - R/E t用前几个 deduce
   4. OCI 倒挤

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