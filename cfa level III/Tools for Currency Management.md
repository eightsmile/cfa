---

### Tools for Currency Management

Assume $d/f$ direct quote, the base is foreign currency. 我们担心外币贬值，所以产生一下策略

#### Forward Contracts 

##### Over/Under Hedged

i.g. 在未来会收到 100 US Asset，then enter a forward contract 卖100 USD 换 CNY

如果 forward contract 是 卖 120 USD 换 CNY 那么 over hedged

如果 forward contract 是 卖 80 USD 换 CNY 那么 under hedged

#### Options

#### Protective Put using OTM Options

- ATM Options are expense
- keep some downside risks as well as upside potential

#### Risk Reversal

Long put OTM, short call OTM ( the underlying asset is the currency )

may reduce the cost, as we short a option

#### Bear Put Spread

buy an OTM put and wrote a deeper OTM put with same maturity

#### Seagull

one type: bear put spread position with a short call position

### Expotic Options

- Asian Options = $\max(S_T - ave,0)$

- Digital Option

   ![Screenshot 2023-11-07 at 22.05.31](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-11-07%20at%2022.05.31.png)

- Knock-in Options (trigger once touch a pre-specificed level)

- Knock-out Options (exit once triggered)

---

### Hedging Multiple Currencies & Emerging Market Currency Management

#### Hedging Multiple Currencies

- **Cross hedge (proxy hedge)**: hedge with an instrument that is not the same as the exposure 通过hedge 与目标相关的资产，如原要hedge 航空燃油，实际 hedge 原油，这样可以达成相同的效果
- **Macro Hedge**: focus on the entire portfolio, not individual assets or currency pair,, as assets themselves inside the portfolio might hedge themselves, so we care what left from the entire portfolio 
- **Minimum-variance hedge ratio**: using OLS to get the cross hedging ratio ($\beta$, the slope in regression is the **optimal hedging ratio**).

#### Emerging Mkt Currency Management

- Might have higher trading costs
  - Larger ask bid spread
  - Crosses in currency pair (coz might not have direct pair)
- Might have Capital Control in the emerging mkt, so use n**on-deliverable forwads (NDFs)** 不直接交还本金，cash settled rather than physically settled