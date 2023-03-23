## Equity

### Pure Play - beta

- Step 1: select a benchmark
- Step 2: estimate the benchmark's beta.
- Step 3: Unleveraged the benchmark's beta.
    - $\beta_U = \frac{E}{E+(1-t)D}\beta_E$
- Step 4: Leverage up the target by the unleverage beta.
    - $\beta_E' = \frac{E'+(1-t)D'}{E'}\beta_U$

### WACC

$$WACC = \frac{D}{D+E}\times r_d(1-TaxRate)+\frac{E}{D+E}\times r_e$$

### DDM

#### PVGO

Present Value of Growth Opportunities (PVGO)

As $PV= \frac{E_1}{r-g}$, so,

$$PV - PVGO =\frac{E_1}{r}$$

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

$$V_0 = \frac{D_0(1+g_2)}{r-g_2}+\frac{D_0H(g_1-g_2)}{r-g_2}$$

- $g_1$ - initial high growth rate.
- $g_2$ - terminal growth rate.
- $H$ - The half-life of the high growth period.

![H-Model Graph](https://cdn.corporatefinanceinstitute.com/assets/H-Model-Graph-1-300x241.jpg)

Under the H-model, the growth rate drops **linearly** until it hits the terminal growth rate. Growth rate change in a **linear / steady rate**.

- DDM is most **suitable** when an investor takes a **noncontrol perspective** because he does **not** have the ability to meaningfully influence the timing or magnitude of a company’s **cash flows and is therefore reliant on dividend policy.** 
- DCF could be used for controlling interest.

### DCF 

#### FCFF & FCFE

- FCFE is easier and more straightforward to use in cases where the company’s capital structure is **not particularly volatile**. 如果公司capital structure变化，则E和D比例不确定，则FCFE不好用
- FCFF 适用，如果E和D的比例

#### FCFF

EBT 为 Equity holder的钱，I为Debt Holder的钱，都要收 tax. 

NI 中扣了 D&A，但是 cash中实际上没有扣，所以加回来D&A。

- From **EBIT**: $FCFF = EBIT\times(1-T) + NCC - FC_{INV}-WC_{INV}$
- From **NI**: $FCFF = NI + I\times(1-T) + NCC -FC_{INV} - WC_{INV} $. 因为debt holder的钱 I 也要收 tax
- From **EBITDA**: $FCFF=EBITDA\times(1-T)+D\&A\times T - FC_{INV} - WC_{INV}$
- From **CFO**: $FCFF = CFO + I\times(1-T)-FC_{INV}$
- P.S. 
    - $EBIT\times(1-T) = NI + I\times(1-T)$
    - $EBIT = EBITDA-D\&A$
    - $CFO = NI + NCC - WC_{INV}$

$NCC$ is the non-cash charge - Depreciation and Amortisation.

#### FCFE

$$FCFE = FCFF - I\times(1-T)+NetBorrowing$$

#### Items

- **Working Capital Investment:**

     $WC_{INV} = WC_t - WC_{t-1} = \Delta WC$

    - $WorkingCapital:\ WC = CA - CL \to = (CA-Cash)-(CL-Debt)$. 
    - $CA $ 扣去cash & cash equivalent
    - $CL$ 扣去Note Payables, current portion of long-term debt.

- **Fixed Capital Investment:** $FC_{INV} = CapEx - \text{Cash Received from Selling Long-term Assets}$

- $FC_{INV} = Purchase - Proceeds$

    - Net of Proceeds from disposal of long-term assets.

    - $FC_{INV} = CaptialExenditure=Gross.PP\&E_t - Gross.PP\&E_{t-1}$

    - $FC_{INV} = Net.PP\&E_t - Net.PP\&E_{t-1} +Dep$

    - $PP\&E_t$ is the Gross term, $Gross PP\&E = Net\ PP\&E +Accum.Dep$

    - **Disposal**: if there are **proceeds** from **Long-term Asset Disposal**:

        - $FC_{INV}=CAPEX-Proceeds \leftrightarrow Purchase - Proceeds$
        - $BV = CarryingValue = PurchaseCost - Accu.Dep - Impairment$
        - $BV_t = BV_{t-1}+Purchase - DisposalNBV - Dep$
        - So, $Purchase = BV_t - BV_{t-1} + DisposalNBV + Dep$
        - $Proceeds = FV_{disposal} = BV_{disposal}\pm G/L$

        $FC_{INV} = Purchase - Proceeds$

        $ = \bigg( BV_t - BV_{t-1} + DisposalNBV + Dep\bigg) - \bigg(DIsposal NBV \pm G/L  \bigg)$

- **New Borrowing**:

    BASE: $Debt_{t-1}+\underbrace{NewIssuing - Repayment}_{NetBorrowing} = Debt_t$