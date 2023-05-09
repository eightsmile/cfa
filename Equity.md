## Equity

### Pure Play - beta

- Step 1: select a benchmark
- Step 2: estimate the benchmark's beta.
- Step 3: Un-leveraged the benchmark's beta.
    - $\beta_U = \frac{E}{E+(1-t)D}\beta_E$
- Step 4: Leverage up the target by the unleverage beta.
    - $\beta_E' = \frac{E'+(1-t)D'}{E'}\beta_U$

### WACC

$$WACC = \frac{D}{D+E}\times r_d(1-TaxRate)+\frac{E}{D+E}\times r_e$$

### DDM

#### PVGO

Present Value of Growth Opportunities (PVGO)

$$PV_{growth} = PV_{NoGrowth}+PVGO$$

- $PV_{Growth}= \frac{D_1}{r-g}$, has dividends in part, and the other part of earning are retention to generate, that retention generates the growth opportunity.
- $PV_{NoGrowth}=\frac{E_1}{r}$, there is no dividend retention, all earning are distributed as dividends, and thus no growth at all. 

$$PV_{Growth} - PVGO =\frac{E_1}{r}$$

$$ Price_{Growth} = Price_{NoGrowth} + PVGO $$

$$ \frac{Div_1}{r-g}=PVGO + \frac{E_1}{r} $$

$$\frac{Div_0\times (1+g)}{r-g}=PVGO + \frac{E_0 \times (1+g)}{r}$$

#### P/E

- Leading PE = $\frac{P}{E_1}$
- Trailing PE = $\frac{P}{E_0}$

Leading P/E thus is,

$$ \frac{PV}{E_1} - \frac{PVGO}{E_1}=\frac{1}{r} $$

, with the growth component is the First Part on RHS.

$$ PV = PVGO + \frac{E_1}{r} $$

注意是$E_1$ 不是 $Div_1$

Leading PE: $\frac{P}{E_1} = \frac{D_1/(r-g)}{E_1}=\frac{PayoutRatio}{r-g}$

#### H-Model

$$V_0 = \frac{D_0H(g_1-g_2)}{r-g_2}+ \frac{D_0(1+g_2)}{r-g_2}$$

- $g_1$ - initial high growth rate.
- $g_2$ - terminal growth rate.
- $H$ - The half-life of the high growth period.

![H-Model Graph](https://cdn.corporatefinanceinstitute.com/assets/H-Model-Graph-1-300x241.jpg)

Under the H-model, the growth rate drops **linearly** until it hits the terminal growth rate. Growth rate change in a **linear / steady rate**.

### Model Selection

- **DDM** is most **suitable** when an investor takes a **non-control perspective** because he does **not** have the ability to meaningfully influence the timing or magnitude of a company’s **cash flows and is therefore reliant on dividend policy.** 因为非控制的不会影响div policy
- **DCF** could be used for **controlling interest**.

- **RI**: If a company has intense capital demands — for example a company does based on its investment cash flows exceeding its operating ones — it may have negative free cash flow and be unable to pay dividends. In this situation, a **residual income model** would be the most appropriate model to use.
- The residual income model considers the opportunity cost to an investor of investing in a stock, not a dividend discount model.

### DCF 

#### FCFF & FCFE

- FCFE is easier and more straightforward to use in cases where the company’s capital structure is **not particularly volatile**. 如果公司capital structure变化，则E和D比例不确定，则FCFE不好用
- FCFF 适用，如果E和D的比例不确定。(有时CF负，则可以用RI)

#### FCFF

EBT 为 Equity holder的钱，I为Debt Holder的钱，都要收 tax. 

NI 中扣了 D&A，但是 cash中实际上没有扣，所以加回来D&A。

- From **EBIT**: $FCFF = EBIT\times(1-T) + NCC - FC_{INV}-WC_{INV}$
- From **NI**: $FCFF = NI + I\times(1-T) + NCC -FC_{INV} - WC_{INV} $. 因为debt holder的钱 I 也要收 tax
- From **EBITDA**: $FCFF=EBITDA\times(1-T)+D\&A\times T - FC_{INV} - WC_{INV}$
- From **CFO**: $FCFF = CFO + I\times(1-T)-FC_{INV}$
- P.S. 
    - $EBIT\times(1-T) = NI + I\times(1-T)$
    - $EBITDA=EBIT +D\&A$
    - $CFO = NI + NCC - WC_{INV}$

$NCC$ is the non-cash charge - Depreciation and Amortisation.

#### FCFE

$$FCFE = FCFF - I\times(1-T)+NetBorrowing$$

$$FCFE=NI+NCC−FC_{INV}−WFC_{INV}+Net Borrowing$$

$$EquityValue = \frac{FCFE_1}{r-g}=\frac{FCFE_0\times (1+g)}{r-g}$$

If a company’s capital structure is relatively stable, using FCFE to value equity is more direct and simpler than using FCFF. All three sections of the cash flow statement are important in determining FCFE because one must integrate the cash flows from the company’s operations with those from its investing and financing activities to calculate a free cash flow figure. Working with FCFF is likely to be easiest when a company is levered and has negative FCFE.

#### Items

- **Working Capital Investment:**

     $WC_{INV} = WC_t - WC_{t-1} = \Delta WC$

     - $WorkingCapital:\ WC = CA - CL \to = (CA-Cash)-(CL-Debt)$. 
     - $CA $ 扣去cash & cash equivalent
     - $CL$ 扣去Note Payables, current portion of long-term debt.
     - $-\Delta CA +\Delta CL$
         - CL中包含 **A/P**, **Accrued** Tax&Expense
         - P.S. Note Payable 算borrowing，因为有单据。

- **Fixed Capital Investment:** $FC_{INV} = CapEx - \text{Cash Received from Selling Long-term Assets}$

- $FC_{INV}=Gross.FixedAsset_t - Gross.FixedAsset_{t-1}$ 注意是gross term

- $FC_{INV} = Purchase - Proceeds$

    - Net of Proceeds from disposal of long-term assets.

    - $FC_{INV} = CaptialExenditure=Gross.PP\&E_t - Gross.PP\&E_{t-1}$

    - $FC_{INV} = Net.PP\&E_t - Net.PP\&E_{t-1} +Dep$

        - $Net.PP\&E_t = FC_{INV} +  Net.PP\&E_{t-1} - Dep$

    - $PP\&E_t$ is the Gross term, $Gross PP\&E = Net\ PP\&E +Accum.Dep$

    - **Disposal**: if there are **proceeds** from **Long-term Asset Disposal**:

        - $FC_{INV}=CAPEX-Proceeds \leftrightarrow Purchase - Proceeds$
        - $BV = CarryingValue = PurchaseCost - Accu.Dep - Impairment$
        - $BV_t = BV_{t-1}+Purchase - DisposalNBV - Dep$
        - So, $Purchase = BV_t - BV_{t-1} + DisposalNBV + Dep$
        - $Proceeds = FV_{disposal} = BV_{disposal}\pm G/L$

        $FC_{INV} = Purchase - Proceeds$

        $ = \bigg( BV_t - BV_{t-1} + DisposalNBV + Dep\bigg) - \bigg(Disposal NBV \pm G/L  \bigg)$

- **New Borrowing**:

    BASE: $Debt_{t-1}+\underbrace{NewIssuing - Repayment}_{NetBorrowing} = Debt_t$
    
    - Note Payables + Long-term debt

#### Others

- Proxy of Free Cash Flows
    - EBITDA is a **poor** proxy for **FCFF**, because it does **not** account for **depreciation tax shield**.
    - Net Income is a **poor** proxy for **FCFE**, because it does not include **non-cash** item.
    - Cash Dividends, Share Repurchases, and Share Issuances **does not affect** FCFF & FCFE, because they still belong to investors / shareholders.
    
- Normalised EPS
  
    $\bar{ROE} \times BV.Equity_{without Preferred Share}$
    
    1. 用来剔除 non-recurring items的影响
    2. 用来剔除 business cycle的影响
    
     To deal with **non-recurring items** and **business cycle** influences, "Analysts address this problem by normalising EPS—that is, estimating the level of EPS that the business could be expected to achieve under mid-cyclical conditions (normalised EPS or normal EPS). Please note that we are using the term “normalized earnings” to refer to earnings adjusted for the effects of a business cycle. Some sources use the term “normalised earnings” also to refer to earnings adjusted for nonrecurring items." 
    
- EV = Mkt.Debt+Mkt.Equity+Mkt.PreferredShare **- Cash - Short-termInvestment** 把流动性最高的俩资产减去。因为EV相当于，当被收购时可以直接抵钱的 所以cash等被剪掉

- Non-recurring 要在NI中抵扣。因为并不算recurring 的，要抵减掉

### Residual Income Valuation

#### EVA

**Economic Value Added,** $EVA = EBIT\times(1-t) - TotalCaptial \times WACC$

, where $EBIT\times(1-t) = NOPAT$ - net operating profit after taxes.

**Market Value Added,** $MVA = MarketValue - TotalCaptial$. 

MVA could also be a per-share terms, so $MVA = \frac{MV-BV}{\text{\# of shares}}$

#### Residual Income (RI)

Derived from DDM.

Future RI 受 BV影响，BV 受 Dividend policy影响，所以dividend policy 会影响 RI valuation。

The main assumption underlying residual income valuation is that the earnings generated by a company must account for the true **cost of capital** (i.e., both the cost of debt and cost of equity). Although the accounting for net income considers the cost of debt (interest expenses are included in the calculation of net income), it does not take into account the cost of equity since the dividends and other equity distributions are not included in the net income calculation. Cost of Equity <-> opportunity cost is then subtracted. Therefore, RI considers the Cost of Capital.

Not affected by Operating Lease, 

Non-recurring gains and losses are reflected in the value of assets in place 意思是 non- recurring item已经在BV中反映了，调整他对RI的value影响不大。

Residual Income is **net income less a charge** (deduction) for common shareholders’ **opportunity cost** in generating net income. It is the residual or remaining income **after considering the costs of all of a company’s capital**. (Debt + Equity)

Rationale: 相当于是 $V_0 = B_0 + \sum \frac{RI}{1+r}$, 算出的$V_0$ 包含 Debt 和 Equity的两部分的。

P.S. **Exclude** **Non-recurring Charges and Earnings.**

For the **Residual Income**, (we denote $B_0$ as the book value of equity) ($V_0$ is the intrinsic value of stocks).

$$V_0 = B_0 + \frac{RI_1}{1+r}+\frac{RI_2}{(1+r)^2}+ \dots$$

We assume the **Clean Surplus Relation: BV of Equity changes are only resulted from R/E**. (进R/E则不violate clean surplus assumption。但是进OCI会影响)

Thus, 

$$B_t = B_{t-1} + EPS_t - Dividends$$

$$ RI_t = EPS - r_e\times B_{t-1}=(ROE-r_e)B_{t-1} $$

Attention here, dividends does not affect the Residual Income, as they are all in EPS. In other words, they all belongs to the equity holders.

Now, we get,

$$ V_0 = B_0 + \sum_{t=1}^{\infty} \frac{RI_t}{(1+r)^t}=B_0 + \sum_{t=1}^{\infty} \frac{E_t - rB_{t-1}}{(1+r)^t}  $$

$$V_0=B_0 + \sum_{t=1}^{\infty} \frac{(ROE_t - r)B_{t-1}}{(1+r)^t}  $$

####  First Stage RI Model

$$V_0 = B_0 + \frac{ROE-r}{r-g}B_0$$

Or,

$$ \frac{P_0}{B_0} = 1+\frac{ROE-r}{r-g} $$

#### Multi-Stage RI Model

**Intrinsic Value  =  BV + PV of High-growth RI  +  PV of Continuing RI**

$$V_0 = B_0 + \sum_{t=1}^{T-1}\frac{E_t - rB_{t-1}}{(1+r)^t} + \frac{E_T - rB_{T-1}}{(1+r-\omega)(1+r)^{T-1}}$$

$$V_0 = B_0 +\sum\frac{RI_i}{(1+r)^i} + \frac{TerminalValue}{(1+r)^T}$$

$V_0 = B_0 + \sum \frac{RI}{(1+r)^t} + \frac{MarketV_t  - BV_t}{(1+r)^t}$

- $\omega$ is the persistence factor.

**Assumptions**

- RI continuous **indefinitely** at a positive level, $PV = \frac{RI_{t+1}}{r}$.
- RI is **zero** from the terminal year forward.
- RI declines to **zero** as ROE reverts to the **cost of equity**, $PV = \frac{RI_{t+1}}{1+r-\omega}$.
    - 下一期的$RI_{t+1}$ 分母是 $1 + Cost of Equity - Persistence Factor$


**Pros**

- Terminal Value do not account large proportions of PV.
- RI can apply for company **not paying dividend**, and **have unpredictable CF**.

**Cons**

- Clean Surplus Relation need to be held.

- The residual income model’s use of accounting income **assumes that the cost of debt capital is reflected appropriately by interest expense**.

    - 因为 RI accounts for cost of debt because EPS is derived from NI which already takes in consideration of cost of debt

    - 但是 It is a weakness of residual income that **interest expense may not reflect the true cost of debt capital**.

- Manipulations of accounting data.

- ROE needs to be predicable.

#### Justified Forward P/E

Justified - used estimated P, not the market P.

$$ P_0/E_1 = \frac{\frac{Div_1}{r-g}}{ROE_0\times (1+g)} $$

- $Div_1 = ROE_1\times (1-Payout)=ROE_0\times (1+g) \times (1-Payout)$
- $g = ROE\times (1-Payout)$

#### Justified P/B

$$P = B_0 + B_0 \sum \frac{RI}{(1+r)^i}$$

$$P/B = 1+ \frac{ROE-r}{r-g}$$

#### Affections

RI valuation relies **heavily** on **ROE** and **BV of Equity**. So, factors affecting ROE and BV would have impacts on the RI valuation result.

Also, the **Clean Surplus Relation** matters. That relation assumes changes in BV are mostly from R/E. If accounting terms go into OCI, such as the following, would violate the Clean Surplus Relation, and make RI valuation less credible.

- **Unrealised** changes in the fair value of some **financial instruments**; 
- Foreign currency **translation** adjustments; 
- Certain **pension adjustments**; 
- Portion of **gains and losses on certain hedging instruments.**

#### Other Adjustments

- **Intangible assets, such as Goodwill and R&D**, have a significant effect on BV of equity.
- **Nonrecurring items and other aggressive accounting practices**.
- **Accounting standards differ internationally**.

### Multipliers

#### Harmonic Mean

The **harmonic mean** is sometimes used to reduce the impact of large outliers—which are typically the major concern in using the arithmetic mean multiple—but not the impact of small outliers (i.e., those close to zero). The harmonic mean may aggravate the impact of small outliers, but such outliers are bounded by zero on the downside.

$\bar{X} = \frac{n}{\frac{1}{x_1}+\frac{1}{x_2}+\frac{1}{x_3}+...}$

or

$$\frac{1}{\sum \frac{w_i}{x_i}}$$

Give less weights to outliers. The harmonic mean tends to mitigate the impact of outliers.

#### P/B

- Exclude Preferred Shares from Book Value of Equity, 
- Price - Common Stock Price only (no include preferred stocks)

#### EV / Sales

$Enterprise Value = Long-term\  Debt + Mkt.common + Mkt.prefer - Cash$ - (short-term investment)

EV = Equity.mkt + long-term Debt.mkt - **Cash**

#### P/E and E/P

About P/E

1. Pay attention to the dilution of EPS. - Use Diluted EPS instead.

2. Adjustments for Non-recurring Items. Exclude Non-recurring items.

3. Adjustments for Business-cycle Influence - (analyst addresses the cyclical effect by **normalising EPS**):

    **Molodovsky Effect:**  at the **bottom** of an economic cycle, earnings are low, and so P/E ratios are high. However, at the **top** of an economic cycle where there is an economic boom, earnings are high and so the P/E ratios are low.

    P/E 最高点，是earning最小的时候，可能处于行业最低谷，可能是最好的投资点。vice versa.

    <img src="https://cdn.corporatefinanceinstitute.com/assets/molodovsky-effect-1024x615.png" alt="Molodovsky Effect" style="zoom:33%;" />

    **Normalising EPS:** (1) average EPS, (2) average ROE.

4. Negative Earning: For earning, $E$, being negative, the $P/E$ would be meaningless. However, $E/P$ is still ok to use, which is also called **Inverse Price Ratio**.

#### PEG

P/E per unit of expected growth, $PEG=\frac{P/E}{g}$.

The smaller, the better. Less PEG means undervalued.

Using PEG ratio needs to consider the followings:

- Assume $g$ and $P/E$ have a linear relationship.
- No consider the (1) Duration of Growth, (2) Differences in Risks.

#### P/B

​		$$\frac{P_0}{E_1} = \frac{Div_1/(r-g)}{E_1}=\frac{1-b}{r-g}$$

​		As, $\frac{P_0}{B_0\times ROE}=\frac{P_0}{E_1}$, $b\times ROE = g$, where $b$ is the retention rate. $1-b=Payout$

​		$$\frac{P_0}{B_0} =ROE\times \frac{1-b}{r-g}=\frac{ROE\times Payout}{r-g}=\frac{ROE-g}{r-g}$$

#### International Consideration

- Differences in cross-border valuation: such as accounting methods, culture differences, economic differences, risks and growth opportunities.
- $P/CFO$,  $P/FCFE$ will be **less** affected by accounting difference. 涉及cash的不太容易受会计区别影响。
- $P/E$, $P/B$  are most affected. 涉及到earnings等这种，很容易受影响。

#### Momentum Valuation Indicator

- Unexpected Earnings: 

$$UE = EPS-\mathbb{E}(EPS)$$

- Standardised Unexpected Earnings

$$Std.UE = \frac{UE}{\sigma_{UE}}$$

### Public & Private Company

#### Excess Earnings Method - EEM

TotalEarning - FixedAssetEarning - WorkingCapitalEarning = IntangibleAsset Earning

$$\frac{IntangibleAssetEarning}{r_{intangible}-g}$$

#### Normalised Earning / Normalised Net Income

为调整了所以 adjustments之后的 NI 或者 earnings

#### Build-up Method

逐层累加rate，算出 discount rate

build-up method 全都加 ，包括 industrial premium

#### Expanded CAPM

$R = r_f + \beta \times EquityRP  +  SmallStockPremium + Company-SpecificRP$

#### Less Agency Cost for Private Firm

#### Cost of Equity - Add-on Model

Add-on method 把所有的premium加一起，不用乘 beta

#### Discount of Control

$Discount of Control=\frac{1}{1+ControlPremium}$

#### Valuation for Private Company

- Market-based Approach for Mature Firm.
- Asset Add-on Approach for Start-up Firm.
- Income Approach for High-growth Firm.
    - Income Approach contains three methods:
        1. FCF Method  -  DCF with going-concern assumption
        2. Capitalised CF Method  -   using a **single representative estimate of economic benefits** and dividing that estimate by an appropriate **capitalisation rate** to derive an indication of value.
        3. Residual Income Method / Excess Earnings Method  -  the excess earnings method consists of estimating the value of all of the company’s **intangible assets** by capitalising future earnings in excess of the estimated return requirements associated with working capital and fixed assets. **The value of the intangible assets is added to the values of working capital and fixed assets to arrive at the value of the business enterprise.**

### Others

- Survivor Bias inflates ERP

  **Historical** Equity Risk Premium (ERP) = Excess return over risk free rate. 
  
  Higher equity returns result in higher ERP (assume that Rf is flat). Inflated historic performance as result of survivorship bias or a string of positive surprises results in inflated historical ERP. That is why **historical** ERP should be **adjusted downward.**
