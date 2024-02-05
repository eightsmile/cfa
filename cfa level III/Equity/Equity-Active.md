## Equity, Active 2 chapters

### Behavioural Bias

- fundamental-based 投资容易受到 confirmation bias **Confirmation bias**, a cognitive error sometimes referred to as “stock love bias,”

  **fundamental-based analysts** and investors to look for information that confirms their existing beliefs about their favorite companies and to ignore or undervalue any information that contradicts their existing beliefs.

- 量化投资受到 survivorship bias **Survivorship bias** is a risk inherent in backtesting a **quantitative active strategy**. 

- 量化受到look-ahead bias。同时，算 B/S 数的时候容易受到此bias。 **Look-ahead bias** is a risk inherent in backtesting a **quantitative active strategy**.  This bias results from using information that was unknown or unavailable at the time an investment decision was made. An example of this bias is **the use of financial accounting data for a company** at a point in time before the data were actually released by the company.

  与财报相关的问题会有 look-ahead bias

  An example of this bias is using financial accounting data for a company at a point before the data were actually released by the company. Nowacki computed historical P/Bs and P/Es using calendar year-end (31 December) stock prices and companies’ financial statement data for the same calendar year, even though **the financial statement data for that calendar year were likely unavailable at year-end.**

- 对于 emotional bias （ f 人不讲道理，emotional damage）止损不能帮助解决 emotional bias

  Establishing stop-loss rules is most likely to address loss aversion bias, which is an emotional bias whereby investors tend to prefer avoiding losses over achieving gains. **Stop-loss rules do not address illusion of control or confirmation bias.** Index 

### Style Consistency

- 看 portfolio 是否符合 style 的时候，优先看 holding-based 的结果

  Holdings-based style analysis is generally more accurate than returns-based style analysis because it uses the actual portfolio holdings

- 非标的，derivatives多的，要用specific identification。As a non-standard hedge fund that extensively uses short positions and derivatives 用 specific identification



- 不同公司辨认 value or growth 的方式不同。Morningstar calculates a score for value and growth on a scale of 0 to 100 using five proxy measures for each. The value score is subtracted from the growth score. A strongly positive net score leads to a growth classification, and a strongly negative score leads to a value classification. A score relatively close to zero indicates a core classification. To achieve a blend classification, the portfolio must have a balanced exposure to stocks classified as value and growth, a dominant exposure to stocks classified as core, or a combination of both.

### Methods

- 会受到 structural change带来的影响，做stop loss可以弥补。Pair Trading: The biggest risk in pairs trading is that the observed price divergence is not temporary and could be due to structural reasons. Frequent use of stop-loss rules, which are set to exit trades when a loss limit is reached, addresses this risk.
- Activist: Asgard invests in firms that have strong business models and good governance. Also, it approaches investing as a long-term investor looking to use its voice to improve the company’s asset management. Asgard is **unlikely to use an aggressive posturing or to invest or stay invested in companies with weak governance or where managers may be in breach of fiduciary duties**.
- The use of the rewarded factor price **momentum** is subject to extreme tail risk. 用 momentum factor 可能带来更多的 tail risks

### Facts about Fundamental & Quantitative / Top-Down & Bottom-Up

- The **quantitative** decision-making process is systematic and non-discretionary (whereas the fundamental decision-making process is more discretionary),

  1. the quantitative approach invests in baskets of stocks, the risks lie at the **portfolio level**
  2. a quantitative process that relies on historical information and does not integrate future expectations about cash flows or profitability may be unable to detect a value trap.

- **fundamental analysis** (not quantitative analysis) emphasizes **forecasting** future prospects, including the future earnings and cash flows of a company.

  **fundamental investors see risk at the company level.**

Growth at a reasonable price (GARP), however—a **growth-based approach**—is a **bottom-up** asset selection strategy

### Building Block of Active Portfolio Construction

The three main building blocks of portfolio construction are alpha skills, position sizing, and rewarded factor weighting.

### IR

Information Ratio = Active Return / Active Risks = IC \* TC * \sqrt{BR}

Expected Active Return = IR * Active Risks

(Active Risks = \sigma_{R_A}) 是s.d. 没有 squared

### Well Constructed Portfolio

A well constructed portfolio has lower "un-explained" part.

### Active Share & Risks

- Fees: Active Share大，则investor原因pay higher fee， Investors are more likely to be willing to pay higher fees for higher Active Share as an indicator of greater active management, 
- Sector Bets: 有 sector bets 的 active risk大
- 用 factor 的， concentration 大
- Dispersion of Return: return dispersion 越大，相当于 sector bets 越大 relative to the benchmark，active risk 越大。This greater dispersion of returns is a direct consequence of the higher active risk and is indicative of a more aggressive or differentiated investment strategy relative to the benchmark.

Efficiency of Active Investment

因为# 大，diversification大，active risk 理应被 diversified。但是如果 # 少，active risk 还小，那么就是 cost-efficient

- 加入 cov 大的进portfolio 可以降低 active risks

  Adding an asset with higher covariance to a portfolio can lower the active risk. Active risk (AR) is defined as
  AR = sqrt(Var(Rp - Rb)),
  where Rp is the return of the portfolio, and Rb is the return of the benchmark.

  The variance of the difference between these two variables can be expressed as
  Var(Rp - Rb) = Var(Rp) + Var(Rb) - 2 * Cov(Rp, Rb),
  where Cov(Rp, Rb) is the covariance between the portfolio's returns and the benchmark's returns.

  A higher covariance between the new asset and the benchmark implies more aligned returns. Adding such an asset increases the portfolio’s covariance with the benchmark, thereby reducing Var(Rp - Rb). This decrease in variance results in a lower active risk, since active risk is the square root of this variance. Thus, selecting the fund with the highest covariance, i.e. Ash, will minimize the active risk for the Amity Equity Portfolio.

### Investment Approach

Active Risk: the extra volatility caused from not exactly copying the benchmark 取决于tilt, & diversification

Active Share 只要 active 了就有

- Stock Picking: high active risk, **high exposure to risk from a single security**, and low sector deviations

- Diversified stock picking: High Active Share indicates that a manager’s holdings differ substantially from the benchmark, and low active risk indicates low idiosyncratic risk resulting from diversification

- Sector Rotation: high active risk and a high tolerance for sector deviations. High Sector Risks

  high active risk and could have either high or low Active Share, depending on whether a concentrated or diversified portfolio approach was followed.

- Multi-factor: between those two. Modest active risks, flexible sector deviation

## Alternatives

### Strategies

- Dedicated short bias: 只要 short： managers look for possible short selling targets among companies that are overvalued, that are experiencing declining revenues and/or earnings, or that have internal management conflicts, weak corporate governance, or even potential accounting frauds.
- **global macro hedge** fund strategy is an example of an **opportunistic hedge fund strategy.** Opportunistic hedge fund strategies take a top-down approach, focus on a multi-asset opportunity set, and include global macro strategies. 高杠杆，低

Event Driven:

tend to be exposed to some natural equity market beta risk. 受 market beta 影响小（因为对冲了一部分），因为 neutralised，但是受 left-tail risks like in the stress market period.

- **Convertible Bond Arbitrage**: A convertible bond arbitrage hedge fund strategy is an example of a **relative value strategy.** Relative value hedge fund strategies focus on the relative valuation between two or more securities. Relative value strategies are often exposed to credit and liquidity risks because the valuation differences from which these strategies seek to benefit are often due to differences in credit quality and/or liquidity across different securities.

  Convertible bond arbitrage strategies frequently use **high levels of leverage** and are **net neutral**.

- M&A: use derivative hedge when the Merger fails:

  **Long out-of-the-money calls on AA shares and long out-of-the-money puts on TT shares**

  When merger deals do fail, the initial price rise of the target’s shares and the initial price fall of the acquirer’s shares are typically reversed. Arbitrageurs who jumped into the merger situation after its initial announcement stand to incur substantial losses on their long positions in the target’s shares and their short positions in the acquirer’s shares.

  To manage the risk of the acquisition failing, the manager can buy out-of-the-money calls on AA shares (to cover the short position) and buy out-of-the money puts on TT shares (to protect against loss in value). Such a position will provide protection that would likely satisfy the IC’s concern about losses with this strategy.

Opportunistic Strategy

- high leverage, have high liquidity, and exhibit right-tail skewness.

1. Global Macro Strategy

2. Managed Future Strategy

   - cross-sectional momentum approach are implemented with a cross-section of assets (generally within an asset class, which in this case is highly rated corporate bonds) by going long those that are rising in price the most and by shorting those that are falling the most.

   - Time-series trading strategies are driven by the past performance of the individual assets. The manager will take long positions for assets that are rising in value and short positions for assets that are falling in value. 

- **equity market-neutral (EMN)** equity strategy. Overall, EMN managers are more useful for portfolio allocation **during periods of non-trending or declining markets**. **EMN strategies typically deliver return profiles that are steadier and less volatile than those of many other hedge strategy areas.** Despite the use of **substantial leverage** and because of their more standard and overall steady risk/return profiles, equity market-neutral managers are often a preferred replacement for fixed-income managers during periods when fixed-income returns are unattractively low.