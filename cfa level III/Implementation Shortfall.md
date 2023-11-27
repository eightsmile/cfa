## Trade Evaluation

### Implementation Shortfall IS 执行落差 显性+隐性

- IS Formulation

  $IS = Execution\ Cost + Opportunity\ Cost + Fees$

- Expanded Implementation Shortfall

  $Expanded \ IS = Delay\ Cost + Trading\ Cost + Opportunity\ Cost+ Fees$

- Delay Cost 决策和下单时间不一样，降低方法：减少时间
- 减少opp costr的方法：Appropriate Order size => minimise the opportunity cost

#### Calculation

- Cost in Dollar per share: $Cost(\$/share) = Side \times (\bar{P}-P^*)$
- Cost in Total Dollar: $Cost(\$) = Side \times (\bar{P}-P^*) \times Shares $
- Cost in Basis Points (bps): $Cost (bps) = Side\times \frac{\bar{P}-P^*}{P^*} \times 10,000bp$
- $P^*$ is the reference price
- $\bar{P}$ is the average execution price

#### Market Adjusted Cost

用于 separate the trading cost from the general market movement 把由于市场price变动带来的trading cost 拆开

$Market-Adjusted\ Cost (bps) = Arrival Cost (bps) - \beta \times Index \ Cost (bps)$

相当于自己的成本比市场贵多少

$Index\ Cost = \frac{Index VWAP - Index\ Arrival Price}{Index\ Arrival Price} \times 10^4bps$

#### Trade Government 交易政策描述

List of Policy, boring