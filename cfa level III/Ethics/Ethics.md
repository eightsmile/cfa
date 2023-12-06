# Ethics

## AMC Asset Manager Code

### Basic

- Differences between AMC and Professional Standards

    - **Code and Standards**

        : for **individual** investment professionals who are member or candidate of CFA

    - **AMC**

        : for **investment management firms** 不必须遵守，协会鼓励遵守

### Components of AMC

- A: Loyalty to Clients
- B: Investment process and actions
- C: Trading
- **D: Risk Management, Compliance, and Support**
- **E: Performance and Valuation**
- **F: Disclosure**

ABC 与 codes and standards 一致

#### D: Risk Management, Compliance, and Support

1. Managers must **comply with code and legal requirements** 需要符合codes和当地法律要求
2. **Appoint a compliance officer** 公司需要任命一个合规负责人
    - Compliance Officer should **competent, knowledgeable, and credible**
    - should be **independent from** the investment and operations
    - **Report directly** to the CEO or board of directors.

3. Portfolio info that are supplied to clients should be confirmed or review by **Independent from third-party**. 需要有独立第三方确认提供给客户的信息是对的

4. **Maintain records** for an appropriate periods 留存就行，没说存多久

5. Employ **qualified staff, and sufficient human and technological resources**.

6. Establish a **business-continuity plan**

    ![Screenshot 2023-12-04 at 13.03.52](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-12-04%20at%2013.03.52.png)

7. Establish a **firm-wide risk management process**

#### E. Performance and Valuation

- Preset performance information that is **fair, accurate**, relevant, timely and complete. **No misrepresentation**.
- **Use fair-market prices**

#### F. Disclosure

1. Communicate with clients **timely**
2. Disclosures are **truthful, accurate, complete, and understandable**
3. Include **material facts**
4. Include: 
    1. conflicts of interests 
    2. regulatory or disciplinary action 
    3. Investment process, including information regarding lock-up periods, strategies, risk factors, and use of derivatives and leverage
    4. Gross-and net-of-fees returns, unusual expenses
    5. Retrospectively disclose
    6. Disclosure specific management fee, incentive fee, etc
    7. Disclose average or expected enpenses
    8. Soft or bundled commission
    9. Valuation methods
    10. Shareholder voting policies
    11. Review or audit
    12. Significant personnel or organisational changes
    13. Risk management processes

In sum,

Compliance Officer 

-> Business Continuity Plan 

-> Fees Related Disclosure

---

## GIPS

### Key Terms

- **Composite**: an aggregate of one or more portfolio 很多个 portfolio 的集合
- **Segregated Account (SMA**): a portfolio owned by a single client. 
- Pooled Fund
  - Broad distribution: mutual funds
  - Limited distribution: hedge fund
- **Fair representation and full disclosure**, **GIPS is voluntar**y 自愿的，不是强制的
- GIPS consist of (1) **requirements** which must be followed, (2) **recommendations** which are **optional**
- when GIPS conflict with law, then **comply with the law, and disclose the conflicts**
- GIPS is applied **Firm-wide**
- **Total Firm Assets** refers to the **aggregate FV of all assets**, including sub-advisors, but not including advisory-only assets (committed capital)
- Changes in firm's orgamosatopm are not permitted, to lead to changes in historical performance 不能通过改 organisation 去改变 historical return，return不能重溯
- Discretionary Portfolio 指 FM 能管控的，non-discretionary 指受限的restricted investment process，不能由 FM 决定，所以 non-discretionary 的表现不能代表公司业绩的好坏
  - Although both discretionary and non-discretionay portfolios are included in total firm assetes, **only discretionary portfolios are included in composites** 指把 discretionary 的纳入 composite 中
- GIPS reports need to be given to the potential clients
- not like actual performance to historical theoretical performance 不能混淆历史和模拟的 return 与 真实的 return

### Return Calculation Methodologies

#### TWR & MWR

- MWR:
    - If firm has control over the external CF
    - Portfolios are **closed-end**, **fixed life**, or **fixed commitment**, or **illiquid investment**
- TWR:
    - Others all

#### Calculation Frequency

- MWR **at least annually**
- All portfolios except private market investment portfolios, **monthly**
- Private market investment portfolio, **quarterly**
- Pooled funds ( not included in composites), **annually**

P.S. 

- Monthly return is through **calendar month end** or **last business day**
- for Pooled Funds: be valued at the time of **any subscriptions or redemptions** 有申购赎回就要value it

True TWR: valuate and calculate returns with every external CF.

##### For large CF

Returns are calculated geometrically, where $r_{t,1}, r_{t,n}$ are the sub-period returns

$1+r_{TWR} = (1+r_{t,1})(1+r_{t,2})...(1+r_{t,n})$

##### For non-large CF

We use the following methods to estimate TWRs

- Modified Dietz Method

    $r_{ModDeitz} = \frac{V_1 - V_0 - CF}{V_0 + \sum (CF_i \times w_i)}$

    $w_i = \frac{CD-D_i}{CD}$

    , where $CD$ is the total number of calendar days, $D_i$ is the number of calendar day till the time CF occurs 至CF发生的时点 

- Modified IRR method

    $EndValue = V_1 = \sum (CF_i \times (1+r)^{w_i})+V_0 \times (1+r)$

    把中间现金流按对应时间compound到未来，把initial value compound到未来

    倒挤出 r

##### P.S.

Return period less than one year should not be annualised

算 total returns 时要包括 Cash, and Cash Equivalents 。所以会导致 cash drag

**Return should be calculated after deducting transaction costs** 费用需要扣除 (brokerage commissions, exchange fees, taxes, spread of brokers, legal / financial / advisory / investment banking fees)

Custody Fees 托管费，不用扣除

Bundled Fees 可扣除可不扣除，如果 bundled fee 中，transaction fee占大多数，则扣除

### Composite Return Calculations

- All, (1) Actual, (2) Fee-paying, (3) Discretionary (4) Pooled Portfolio must be included into at least one composite.
- **Non-discretionary,** **Segregated Accounts** (SMA), and **Pooled Funds** must not be included into composites
- Non-fee-paying discretionary segregated accounts and pooled funds **may** be included in a composite, but additional disclosures may be required 可放可不放

#### TWR Calculations

- Asset Weighting using beginning value
- Asset weighting using beginning value and external cash flow
- Aagregate return method

### Discretion, Mandates, Composite Construction

- **Discretion**: discretionary 业绩能否反应 FM 的投资能力
    - if constraint is not material, then discretionary, then include in composite 如果client设置的constraint 不重要，port依然能反映 FM 的能力，那么放入 composite 中
    - 否则（不能反映FM能力），则为 non-discretionary, 不放入 composite 
- Mandates
    - No model or hypothetical portfolio should be included into composite 只能纳入 actual 的，假设的模型的理论的都不能纳入
        - Model, hypothetical, back-tested, or simulated returns are all considered as theoretical performance
- Include or Exclude
    - New portfolio should be included as of **the beginning of the next full performance measurement period.** 下个完整期间业绩出来之后，才纳入。如5.15纳入，则6月完整业绩出来后，才能算上，五月不算
    - Terminated portfolio 入月中终止，则当月全都不算了。如5.15截止，那么从包含这个 port 的只能出现在4月，5月整月都不能包含了
    - Switch from one composite to another. 
        - Iff revise mandates
        - Iff no longer fit the original
        - Otherwise, stay in the original composite, do not switch
    - Significant Cash Flow, may be temporarily removed.
        - "Significant "should be defined ex ante
        - Otherwise, use temporary new accounts for remove the effects of significant CF
    - Could define minimum asset level
        - Do not retroactively use updated minimum level 不能回溯
        - Prior performance must remain 保留历史业绩

### Presentation, Reporting, Valuation, Verification

#### GIPS Report

Firm comply with GIPS must provide GIPS report to all **prospective clients**, and **limited distribution pooled fund investors**.

Two reports:

- GIPS Composite Report
- GIPS Pooled Fund Report

##### Years

- Annual performance should be at **least 5 years**, **extended each year until at least 10 years**.
- If the composite's **existence for less than 5 years**, then present returns **since inception**, and build over time to 10 years. 如果存在少于5年，则从建立日起，直到存续10年

##### Required Elements of GIPS Composite Report

1. Compote and Benchmark annual returns for all years
2. The number of portfolios (if >= 6) in the composite
3. The amount of assets in the composite
4. The Amount of total firms assets at the end of each period
5. A measure of internal dispersion of individual portfolio returns for each annual period if the composite contains >= 6 portfolio
6. If monthly composite returns are available, a three-year annualised ex post s.d. of the composite and benchmark returns as the end of each annual period.