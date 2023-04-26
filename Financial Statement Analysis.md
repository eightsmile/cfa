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