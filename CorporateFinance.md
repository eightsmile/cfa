## Corporate Finance

without tax: $r_E = r_0 + (r_0-r_d)\times \frac{D}{E}$

With tax: $r_E = r_0 + (r_0+r_D)\times \frac{D}{E}(1-t)$

$V_L=V_{UL}+t\times D$

$WACC = w_D r_D(1-t)+w_Er_E + w_Pr_P$

### Stock Manipulate

- **Stock Dividends:** 

    1. **R/E -> Capital** Contribution. 
    2. Only **Price per Share** decrease.
    3. 因为有付div的能力，与 initiation相反的是omission和reduction而不是retention for growth。所以是个好的指标。Dividend initiations convey positive information and are associated with future earnings growth, whereas dividend omissions or reductions convey negative information and are associated with future earnings problems.
    4. **Bad Signal!** Dividend omissions or reductions convey negative information and are associated with future earnings problems.

    - Gradual Dividend Policy. 为了防止当年利润高，payout高，未来利润低的时候减div是不好的现象。所以，把超额的div匀给未来的年份。

- **Stock Split**

    - For P/E: P decrease, EPS also decreases. So, P/E remains unchanged.

- **Stock Repurchase** 

    - Stock Repurchase with external financing, 对比debt融资的成本rate 和 EPS的 rate：

        - $ EPS^{new}=\frac{Total Earning - Debt Cost}{\# \ of \ Shares - \#\ Repurchases} $
        - 所以，如果 debt cost 与 EPS相同，则EPS.new不变
        - 如果 debt cost大，则分子小，则EPS.new变小

    - **Methods:**

         1. **In open market**  -  gives the company maximum flexibility, because there is **no legal obligation** to undertake or complete the repurchase program; a company may not follow through with an announced program for various reasons, such as unexpected cash needs for liquidity, acquisitions, or capital expenditures.

         2. **fixed price tender offer**  -   typically at a premium to the current market price.

         3. **Dutch Auction**  -  **also a tender offer** to existing shareholders, but **instead** of specifying a fixed price for a specific number of shares, the company stipulates **a range of acceptable prices**.

         4. **Repurchase by direct negotiation**  -  a company may negotiate with a major shareholder to buy back its shares, often at a **premium** to the market price (but could be at discount). The company may do this to **keep a large block of shares from overhanging the market** (and thus acting to dampen the share price).  **Prevent an “activist”**.  

            **Greenmail** - detrimental to remaining shareholders.

- If no tax on dividends and repurchase(capital gain tax), then A decreases, E decreases, end with same wealth (div + after-div NI) for equity-holders. $NI_{no-div} = NI_{after -div}+Div$

### ESG

- **Proprietary method** to identify company and industry ESG factor is an approach that relies on using company-specific ESG data that is publicly available from annual reports, proxy reports, corporate sustainability reports, and regulatory filings such as the 10-K 用10-K的数据获取ESG信息，但是主要问题是，10-K的披露说voluntary的，无法评定。
- **Principal-principal problem**: The controlling shareholders can potentially divert resources for their own benefit at the expense of the minority shareholders. Shareholder 的大股东和小股东 之间。
  - The controlling shareholders may be able to allocate resources to their own benefit at the expense of the minority shareholders. This situation is known as the principal–principal problem.
  - Dual Class Share - AB股会导致 principal-principal problem.

- **CEO duality**: ceo和董事一起做 - 不好。CEO and chairperson are not separate. The controlling shareholders may be able to allocate resources to their own benefit at the expense of the minority shareholders. 
- **Family control** lowers the risks associated with principal-agent problems, but poor transparency, modest considerations for minority shareholder rights, and difficulty in attracting quality management talent.
- **Number of Independent Board**: OECD recommend 20-50%.
- **Average board tenure** 在3.9-9.9 中间好。太长太短都不好
- **Two-Tier Board** 有两批board 好，有助于 decision-making, build a more balanced, positive outlook on production, prevents a single board from getting overwhelmed with handling the management, system and function of a business.。一批人负责直接管理，一批负责远期决策

Equity Analysis - **identify potential opportunities**.

Fixed-income Analysis - **mitigate downside risk**.

**Greenwash** - is the risk that the bond’s proceeds are not actually used for a beneficial environmental or climate-related project. 用green bond 融钱，去做不green的事，不好

### Cost of Capital

#### ERP - Equity Risk Premium

$$r_e = \mathbb{E}(r_f)+Systematic ERP + Company ERP$$

- Survivorship Bias 用 index 的 historical data 时。因为活着才在index成分股里。
- Survivorship Bias **inflate** the estimate of ERP.

#### Earnings Growth

Earning Growth per Share = Expected Inflation + RealEconomicGrowth + changes in Share Outstanding

$$EarningGrowthPerShare = i + g + \Delta S$$

$$ERP = DY + \Delta(P/E)+i+g+\Delta S - E(r_f) $$

- $DY$ - Expected Income Component
- $\Delta P/E$ - Expected Growth Rate in P/E
- $i$ - Expected Inflation
- $g$ - Expected Growth in Real Earnings per Share - Real GDP growth
- $\Delta S$ - Expected Change in Share Outstading

#### Country Risk Premium 

$$CRP = Sovereign YieldSpread \times \frac{\sigma_{Equity}}{\sigma_{Bond}}$$

#### International CAPM

$$E(r_e) = r_f + \beta_1\bigg(E(r_{gm}) - r_f\bigg) + \beta_2 \bigg( E(r_c) - r_f \bigg)$$

- $E(r_{gm})$ - global market index
- $E(r_c)$ - foreign currency index