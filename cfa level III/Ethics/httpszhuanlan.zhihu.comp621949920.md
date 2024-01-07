https://zhuanlan.zhihu.com/p/621949920

**Monte Carlo simulation（专题）**

定义：Monte Carlo simulation allows asset manager to model the uncertainty of several key variables. Generates random outcomes according to assumed probability distribution for these key variables. It is flexible approach for exploring different market or investment scenario. 蒙特卡洛模拟是将变量（事先定义好分布）的值随机发射，生成了结果，可灵活的探索不同市场、投资环境下的状态。

较MVO的优势：

1, Rebalancing and taxes, Monte carlo simulation allow to analyze different rebalancing policies and their cost over time（in multi-period situation）. 蒙特卡洛模拟可以用于分析执行不同的再平衡策略、税收时的影响。

2, Path dependent. As there are cash out flow each year, terminal wealth（the portfolio’s value at a given point） will be path-dependent because of the interaction of cash flows and returns. 如果每年都有资金流出，指定时间的组合价值会受这些资金流出和收益的影响 Cash flows in and out of a portfolio and the sequence of returns will have a material effect on terminal wealth, this is termed path-dependent.

3, Monte Carlo can incorporate statistical properties outside the normal distribution, such as skewness and excess kurtosis.蒙特卡洛模拟可用于建模非正态分布。

4, Monte Carlo simulation is able to incorporate the effect of changes to variable over time, it is a multi-period framework. MVO is a single-period framework, it can not be used to evaluate the likelihood of the foundation dropping below 5 m desired spending lever in the future.蒙特卡洛模拟可包含不同变量长时间变化的影响。

Monte Carlo Simulation结果显示成功率低，如何解决？

1, increasing the amount of contribution for the goal.

2, reducing the goal amount, reduce the size of their investment portfolio needed when retire by accepting a lower standard of living.

3, delaying the time of goal.

4, adopting an investment strategy with higher expected return, **within the client's acceptable risk tolerance and risk capacity**.

Monte Carlo Simulation的优缺点

Advantage: 

1,applicability to the client's actual asset allocation; 

2,aggregating the result of many trials of probability-based estimates of key variables;

3,flexibly model different scenarios and explore issues that are important to client; 

4,provides a distribution of probable outcomes rather than a point estimate, allow the investor to determine the likelihood of reaching their retirement goal.

Limitations: 

1,can not predict the future; 

2,include the probability of reaching a goal, but no necessary shortfall magnitude; 

3,does not consideration of unique belief, Monte simulation rely on the past data, but do not incorporate expectation for future financial market.

4, highly sensitive to small change in input assumption.

**Behavioral Finance**

从行为金融的角度，分析客户可能存在的bias，对用户进行分类，进而实现更好的与客户沟通。

Reading 1 & Reading 2

1. 对于传统金融与行为金融的区别 : Risk-averse vs loss-averse
2. Cognitive & Emotional bias。(简答题：各项bias的定义)
3. Cognitive error：primarily due to faulty reasoning, need to be corrected(moderate); Emotional bias: impulse and intuition, influenced by feelings, accommodate (adapt)进而无法无法达到理性.
4. Cognitive error- Belief perseverance (RICCH) 涉及到固执己见，与认知失调（当新信息与过去的认知和信念相冲突时造成的心智不适，对此人们会选择性的关注感兴趣的新信息，忽略与现有观念相冲突的信息）相关
   Conservative bias/ representative bias/ illusion of control/ hindsight bias/ confirmation bias
   Conservative bias: 坚持以往的观点或预测结果，没有充分的了解新信息maintain their prior view or forecast inadequately incorporating new information
   Confirmation bias: 只关注支持自己想法的消息，忽视与自己观点不同的消息tend to look for and notice what confirms their belief, ignore or underweight what contradicts their belief
   Representative bias: 用以往的经验或分类方法，来理解新消息tend to classify new information based on past experience and classifications。Extrapolation线性外推，即将新信息简单归类，得出错误结论，overweight new information or new feather, neglect base rate; neglect sample-size(law of small numbers)(例如过去三个月业绩好即代表业绩好). Viewing the new information as representative of a long-term trend.
   Illusion of control: 错误的认为可控制或影响结果tend to believe that they can control or influence outcomes, in fact they can not
   Hindsight bias: 现在目前这个时间点，认为过去发生的事，自己在过去是能够判断到的，过高的估计自己预测的准确性may see past event could be predictable, and they may remember their prediction more accurate than they actually were
5. Cognitive error- Information-process (FAMA) 会以不符合逻辑以及非理性的方式来处理信息
   Anchoring and adjustment bias/ Framing bias/ mental account bias/ availability bias
   Anchoring and adjustment bias: 当需要预测某个数字时，先设定一个锚定值，然后再根据情况进行调整，但对于锚定值却不做调整when estimating a value, people begin by set an initial number (anchor), which they then adjust up or down to reflect subsequent information, but tend to adjust their anchor insufficiently.
   Framing bias：回答问题时，答案取决于题目的问法。answer differently based on the way in which it is asked。Narrow framing只捡好听的说。As a result of a framing bias, tend to choose an allocation based on 1/N naive diversification strategy.
   mental account bias：对相同大小但来源不同的金额有着不同的对待方式，treat one sum of money differently from another equal-sized sum based on which mental account the money is assigned to。**Suggest that tend to consider his investments in layers**也就是说只要看到portfolio in layers （而不是mean-variance optimized）就说明有mental account bias, Would not consider her principle and income together, but rather as two distinct account.
   availability bias: 容易被一些给自己留下深刻印象的事件影响自己的判断，特别是这些事件很容易被想起时。tend to be overly influenced by events that have left a strong impression which is easy to recall. 这个bias辨别的重点在于easy to recall上，无论是广告，还是让人能够回想起来的successful investment history.
6. Emotional bias (LOSSER)

Loss aversion bias/ over confidence bias/ self-control bias/ status-quo bias/ regret-aversion bias/ endowment bias 

1. Loss aversion bias: 倾向于避免实现损失，相对于实现利润来说tend to prefer avoiding losses as opposed to achieving gains
   Myopic loss aversion: 例如，只看短期数据，股票的波动大，感觉不如债券好，但如果看长期，则收益明显好。
2. over confidence bias：表现出对自己判断的无理由的自信show unwarranted faith in their own judgement。Self-attribution bias & illusion of knowledge

Certainty overconfidence/prediction(the range of outcomes in his forecast is narrow)

1. self-control bias: 由于缺乏自律，为了短期目标而放弃的长期目标fail to pursuit long-term goal because lack of self-discipline。更重视短期目标，如为了获得interest income来支持消费，配置更多的bond。
2. status-quo bias：选择默认值，因懒惰而拒绝改变choose to do nothing instead of making a change。Inertia and default。后果：leaving the asset allocation fixed over time may result in risk and return becoming inconsistent with a participant’s changing circumstances.
3. regret-aversion bias：倾向于避免做出决策，因为决策可能会带来损失tend to avoid making decision out of fear that the decision may end up poorly。Herding behavior羊群效应.
   Maintain his previous judgement (incorrect) avoid admitting his forecast may have been incorrect.
4. endowment bias：认为一些资产有着超越其自身公允价值的价值value an asset more when they hold right to it than when they do not
5. 其他bias
   1/N diversification : ignore correlation that create diversifiable risk, total risk and return are likely not optimized
   Naive extrapolation: representative bias
   Home bias(familiarity): familiarity with a country may lead investor to hold high amounts of domestic investments, this is an illusion of control（认为自己熟悉的公司，对于经营的结果有控制力） leading to concentration and diversifiable risk. 
   Gambler’s fallacy: expecting reversals to occur more frequently than actually happens预计均值快速回归mean reversion，认为其会立刻回归，早于实际发生时间 a misunderstanding of probabilities in which people wrongly project reversal to a long-term mean
   Price move is unrelated to past price movement.
   Conjunction fallacy
   Social proof: follow the belief of a group
   Recent effect: availability
   Disposition effect 处置效应. more willing to sell winners, which can encourage excess trading
   Halo effect: 明星公司是好的投资标的 favorable evaluation of some characteristics to other characteristics
6. 如何克服这些bias ？
7. be as neutral as possible and open-minded as possible when interpreting investment-related situation在做投资决策是尽可能的保持客观和开放的思维
8. Develop an appropriate investment policy strategy, carefully research and analyze investment decisions before making them, and focus on long-term result.采用合适的投资策略，在实施投资决策前谨慎的进行研究分析，聚焦长期结果
9. A disciplined approach to investment based on fundamental analysis 基于基本面分析，保持纪律性的投资方法
10. Qualify the risk-reducing and return-enhancing advantages of diversification and proper asset allocation. 量化分散化和合适的资产配置的风险降低和收益增强的优势

7、简答题：Dealing with behavior biases 针对一些Bias，用哪些投资方法可以应对

（1）loss-aversion：goal-based investing

（2）illusion of control:global market portfolio

（3）mental accounting: for each sub-portfolio, do MVO

（4）representative bias: 客观的AA流程和强化管理框架objective asset allocation process and strong governance framework

（5）framing bias：as neutral as possible, open-mind for multiple perspective

（6）availability bias: using global market portfolio as the starting point in developing the asset allocation

三、投资者的分类，两分、四分、五分法，客户分类的限制。

1、两分法：passive investor vs active investor

2、五分发: AA - adventurer, II - individualist, PP - Guardian, FF - Celebrity, Straight Arrow (简答题：各自分类的特点)

3、四分法：PP - passive preserver, FF - friendly follower, II - independent individualist, AA - active accumulator (简答题：各自分类的特点) 

| General type     | Passive                                                      |                                                              |                                                              | active                                                       |
| ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Risk tolerance   | Low                                                          |                                                              |                                                              | high                                                         |
| Investment style | Conservative                                                 | Moderate                                                     | Growth                                                       | Aggressive                                                   |
| bits             | PP                                                           | FF                                                           | II                                                           | AA                                                           |
| Emotional bias   | EndowmentLoss aversionStatus quoRegret aversion              | Regret aversion                                              | Overconfidence and self-attribution                          | OverconfidenceSelf-control                                   |
| Cognitive bias   | Mental accountingAnchoring and adjustment                    | AvailabilityHindsightFraming                                 | ConservatismAvailabilityConfirmationRepresentativeness       | Illusion of control                                          |
| Advising         | Big picture advice(such as how to help him/her to meet the retirement goal)Focus on what the money will accomplishBe persuaded about the soundness of advisers’ general philosophy | Offering education in a clear, unambiguous waySay yes to advice without adequately considering the risk involved | Listen to sound advice when it is presented in a way that respect their intelligence（注意与FF的区别） | Most difficult client to controlTake control of the situation |

注：注意各个投资者分类在investment style和risk tolerance上的区别，可用于辨别各自的分类。

（1）如果与不同分类的客户沟通

PP & AA(emotional bias): big picture; safety; generation

FF & II(cognitive error) : quantitative method; data

4、简答题：客户分类的限制:

（1）客户会同时表现出cognitive和emotional两种bias

（2）会同时表现出多种分类的特征exhibit characteristics of multiple investor types

（3）即使分类准确，客户也会要求被特殊对待likely to require unique treatment even if they are classified as the same type because human is complex

（4）随着年龄增长，会表现出不同的行为特征will likely to go through behavioral changes as they age

5、简答题：如何降低social proof的影响

（1）多元化人员背景diverse background

（2）支持表达自己的独立看法express and support their own view

（3）鼓励不同意见encourage alternative opinions

（4）多元化人员经历、文化、技能diverse in skills,experience and culture

**Capital Market Expectation**

为了后续做资产配置，需要先对宏观经济进行分析，得到各类资产的预期回报、风险。

Reading 3. Framework and Macro Consideration

针对宏观经济的分析：

1、3种分析方法

1. 分析用数据的9个局限
2. 经济增长原因的分解
3. 经济周期

一、数据准备，Challenge in Forecasting, 九大挑战。

1. 经济数据的缺点：时滞效应time lag、事后修正revised、基准改变rebased
2. 数据计量错误data measurement errors and biases（基于历史数据所作的分析这两个错误均存在）：幸存者偏差survivorship bias: when back-test use only those company that are currently in business today, they ignore the stocks that have left the investment universe due to bankruptcy, this lead to overly optimistic results and can cause investor to arrive at incorrect conclusions（return is overestimated）、评估数据偏差appraisal data(risk underestimated, 数据smooth，低估standard deviation)
3. 使用历史数据的局限性limitation of historical estimates：regime change(long time-series), a change in regime is a shift in the technology/political/legal/economic/regulatory environment, regime change alters the risk-return relationship since the asset’s risk and return characteristics vary with economic and market environment; asynchronism (异步性，非同步数据，using short time period)
4. Ex post risk is a biased risk measure of Ex ante risk
5. Data-mining (没有规律硬找规律，把短期的现象总结成了长期规律，overfitting) repeatedly searching a data set until a statistically significant pattern emerges. 
6. Fail to account for conditional information
7. Misinterpretation of correlation 有相关性不代表存在因果关系 Correlation relationships should not be used in a predictive model without understanding the underlying linkages between the variables.
8. Behavioral biases
9. Model uncertainty: model/parameter/input uncertainty

二、经济增长的原因（GDP），分解为4项。

1. 投资收益分解为：股利（dividend）+资本利得（capital gain）
2. Capital gain（share price增长）分解为：GDP增长+企业利润增长（earning/GDP）+P/E估值的增长
3. GDP的增长可分解为（来自cobb-Douglas生产函数）：Real GDP增长 + Inflation

Real GDP 增长= labor input 增长（劳动力增长+劳动参与率增长）+ Capital input per worker增长 + total factor productivity增长

output gap = actual GDP - potential GDP 

三、Approaches to Economic Forecasting，Econometric Analysis计量经济学/Economic Indicator/Checklist Approach。（简答题：各自分析方法的优缺点）

1、Econometric analysis计量经济学

（1）structural model 因子有经济学含义/ reduced-form model 通过回归得到，因子可能无经济学理论支撑

（2）优点：模型稳定model can be quite robust、模型建立完成后新数据输入后可迅速得到结果new data may be used within model to quickly generate output、得出量化分析的结果deliver quantitative estimate

（3）缺点：很难预测经济的拐点rarely forecast turning point well、模型建立复杂且耗时complex and time-consuming to formulate、模型中的相关性不稳定relationship not static

1. Economic indicator经济指标 (也称为diffusion index，以测定各个经济指标循环波动为基础，可得到一定时点上扩散程度的排序 )
2. leading(stock price)/coincident(PPI)/lagging indicators(inflation/ inventory/ sales)
3. 优点：直观且模型建立简单intuitive and simple in construction、主要聚焦于预测经济拐点focus primarily on identifying turning point
4. 缺点：数据会不停修正history subject to frequent revision、拐点信号可能错误can provide false signal、只能提供方向性的指导may provide little more than one directional guidance、相关性不稳定relationship not static
5. Checklist approach
6. 优点：简单、灵活limited complex/flexible
7. 缺点：主观、费时subjective/time-consuming

四、经济周期（宏观经济学），周期的五个阶段，Inflation/Monetary policy(Interest Policy)/Confidence/Capital Market与周期的关系（同步、领先、滞后）

1. Inflation 与 business cycle相比是滞后的
2. Monetary policy(interest rate)、confidence与cycle同期
3. 财政政策滞后
4. 股市领先
5. 债券市场（反映利率）跟随央行的货币政策表现出同期性

| Phase            | Inflation                 | Interest rate & policy            | Capital Market                                               |
| ---------------- | ------------------------- | --------------------------------- | ------------------------------------------------------------ |
| Initial Recovery | Inflation still declining | Low interest rate, budget deficit | Bond yield bottom out, rising stock price                    |
| Early Expansion  | Low inflation             | Rising short-term interest rate   | Bond yield stable to up lightly, stock price trending upward |
| Late Expansion   | Increasing inflation      | Limit the growth of money supply  | Bond yield rising, stock price topping out with volatile     |
| Slowdown         | Inflation rising          | Short-term interest rate at peak  | Bond yield peak and possible falling(inverted), stock declining |
| Recession        | Inflation peak            | Short rate declining              | Bond yield dropping, stock bottoming and start to rise       |

1. Taylor rule(Monetary Policy), Fiscal Policy(关注deficit的变动，而不是绝对值)
2. Monetary policy针对inflation
3. Fiscal policy针对real rate

Taylor rule: optimal interest rate = neutral interest rate + 0.5*(forecast - target GDP) + 0.5*(forecast - target inflation)

其中neutral interest rate = real policy rate + expected inflation rate

注意forecast - target GDP，这一项是real增速而不是nominal增速（毕竟公式中已经有inflation了）

六、Yield Curve的形状，重点关注何时inverted。

1、Yield curve 形状取决于短期利率

2、货币政策一般影响短期利率

3、财政政策影响长期利率

4、经济grow or contraction 取决于货币政策和财政政策是否同时stimulative or restrictive

5、stimulative or restrictive

（1）货币政策刺激 & 财政政策刺激：短期利率下降，长期利率上升（财政政策刺激需要钱，政府要多发行债券，长期利率上涨），steep，经济grow

（2）货币政策刺激 & 财政政策紧缩：短期利率下降（下降的更多），长期利率下降，steep（程度小），经济less clear

（3）货币政策紧缩 & 财政政策刺激：短期利率上升（上升的更多），长期利率上升，flat（虽然转动的方向一致，但没有到inverted的地步），经济less clear

（4）货币政策紧缩 & 财政政策紧缩：短期利率上升，长期利率下降，inverted，经济contraction

七、进行CME的步骤

1、明确CME是针对对哪项资产、哪个时间段等性质

2、研究历史数据

3、明确（specify）用那种方法、模型进行研究

4、搜集所需数据

5、针对当前经济投资环境，对所选数据和方法，进行研究

6、得出结论

7、监测结果，并与预期做对比，提供反馈以优化预测过程 monitor actual outcomes and compare them with expectations, providing feedback to improve the expectation-setting process.

Read 4. Forecasting Asset class Returns.

基于不同的经济周期，预期不同资产的表现，收益&风险

一、Return Forecasting :

1. Fixed Income : DCF/risk premium
2. Equity : GK model/ST model
   GK model计算的是expected return，
   ST model算的是risk premium (expected return = risk free rate + risk premium + illiquidity premium)
3. Real estate : Risk premium/ NOI(GGM)
   Cap rate = NOI(net operating income) / value
   永续：Return = cap rate + NOI growth rate (里面包含real + inflation)
   短期（租几年后会将房子卖掉），需要考虑房价收益的变动： return = cap rate + NOI growth rate - %cap rate变化
   当cap rate上升时，房价下降，即导致收益率下降
4. Exchange rate : 影响汇率的各项因素
5. Volatility Forecasting :
6. Multi-factor model：利用Long/short 提取风险因子 （提取inflation/credit spread/duration）
7. Shrinkage estimate: 既考虑历史情况，也考虑分析师自身判断，做加权平均
8. Smoothed return to estimate volatility (for Real Estate)

**Asset Allocation**

此部分内容即开始介绍资产配置，首先介绍资产配置的基本情况，然后开始构建组合，最后是组合构建时会遇到的一些限制。

Reading 5 Overview of Asset Allocation & Reading 6 Principles of Asset Allocation

一、在资产配置前，首先需要搞清楚一个人到底有多少资产

Economic net worth(also known as Net wealth) = Net worth + Extended asset - Extended Liability

二、构建Asset class, 简答题：criteria for specifying asset class for the purpose of asset allocation.资产大类的划分方法

1. 单一资产大类内资产应该性质相同, homogeneous
2. 资产大类之间应互斥, mutually exclusive
3. 资产大类应该分散化，diversifying, should not have high expected correlation with other asset class
4. 资产大类应占可投资资产的大部分
5. 资产大类应占投资人组合中的大部分
6. Rebalancing (Range的大小及其影响因素)
7. Rebalancing range大小，正相关：transaction cost/risk tolerance/correlation ; 负相关：volatility（standard deviation越大，则range越小）
8. 简答题：Rebalancing 好处（与战略资产配置保持一直、分散化、做空波动性）
9. 税后的range大于税前range，由于税后的收益波动小，所以range大
10. Asset allocation的3种方法

| Asset allocation方法 | 目的                                                         | 风险                                                         | 细分方法                                                     |
| -------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Asset only           | maximize Sharpe ratio for acceptable level of volatility     | volatility/tracking risk or information ratio/ downside risk(VaR, conditional VaR) | MVO,mean-variance-optimization, 及其6种改进模型Factor-based asset allocation : 即 Risk-factor MVO, 可解决risk factor overlapping |
| Liability-relative   | Fund liabilities(minimization shortfall risk）               | shortfall risk                                               | Surplus optimization, hedge/return seeking, Integrated asset-liability |
| Goal-based           | achieve goals with specified required probability of success(相当于mental accounting) | maximum acceptance probability of not achieving a goal       |                                                              |

五、Asset Only (AO)：如何构建MVO，传统MVO的优缺点，及如何改正

1. 传统MVO的优点：广泛使用、是其他更复杂AA方法的基础
2. 缺点及其解决方法：
3. Highly concentrated : add constraints/re-sample/ reverse/ BL
4. Highly sensitive to small change in the input : resample MVO, Reverse MVO, black-litterman model
5. Skewness and kurtosis (即non-normal distribution ）： non-normal optimization approaches
6. Less liquidity asset 三种应对方法: exclude less liquidity asset/ factor based (model the inputs to represent the specific risk characteristics) / proxy 
7. Risk may not be diversified : risk-factor MVO
8. Single-period framework : monte carlo simulation
9. Liability or consumption no consider : surplus MVO (ALM)
10. 解决方法的优缺点
11. add constraints : 
    优点：包含真实世界的限制、克服传统MVO的部分缺点
    缺点：如果加入了过多的限制，则不再是MVO，而是指定的资产配置方法
12. Resampled MVO (引入monte carlo simulation，多次模拟后取平均)
    缺点：可能出现收益降低反而风险提升、风险资产过度分散化、缺少理论基础
13. Reverse optimization: 利用Global index中隐含的各项资产大类的weight，反向MVO得出implied return，然后再利用implied return再次与risk，covariance一起进行MVO，得出optimal weighting。另外，也可以用CAPM模型计算出implied return。
14. Black-litterman model： 与reverse optimization一致，但加入了分析师观点
15. Monte Carlo simulation较MVO的优点（见MCS专题）

六、Liability-relative (ALM) 三种方法

1、Surplus optimization

（1）将liability也作为资产放入MVO中

（2）与传统MVO的区别：效用函数不同、MVO目标不同、Surplus可以<0，Conservative资产不同

2、Hedging/ Return seeking：

1. basic(fully hedge)、variant(partial hedge)
2. 另一个variant（利用衍生品，对冲掉liability的变化） limitation: 对冲是无法做到与liability完全一致，有basis risk

3、Integrated asset-liability: 将影响liability的因子细分出来，直接cover liability的因子，此方法更精确的原因：

（1）Integrated asset-liability 将资产和负债放在一起综合考虑，其他两个方面是分别考虑了资产和负债the previous two approaches consider independently for asset and liability. However, integrated approach jointly optimizes asset and liability decisions.

（2）此方法使用量化建模this approach can be implemented in a factor-based model

（3）可提升surplus,即提升funded ratio, has the potential to improve the funded ratio

4、三种Liability-relative方法的对比

| Surplus            | Hedging/return seeking            | Integrated                      |
| ------------------ | --------------------------------- | ------------------------------- |
| Simplicity         | Simplicity                        | Increased complexity            |
| Linear correlation | Linear or non-linear              | Linear or non-linear            |
| All level of risk  | Conservative level of risk(basic) | All level of risk               |
| Any fund ratio     | Positive fund ratio(basic)        | Any fund ratio                  |
| Single period      | Single period                     | Multiple period (dynamic动态的) |

1. Risk budgeting (Marginal contribution to total risk), Risk parity（absolute contribution to total risk）
2. Risk budgeting (MCTR): 每承担一单位的风险，要获得最高的风险补偿，追求optimal risk budgeting
   MCTR = asset beta relative to portfolio * portfolio standard deviation(注意是整个组合的波动，而不是单个资产)
3. Risk parity (ACTR) :Portfolio内各项资产对组合风险的总贡献一致

ACTR = weight * MCTR

3、简答题：risk parity 的优缺点

1. 优点：风险分散化the source of risk are diversified、后评估表现良好back test show promising result
2. 缺点：未考虑收益ignores expected return、需要加杠杆（需要低利率环境）depend on use large leverage at low borrow rates、有look-back bias，不同时段表现不一致（比如金融危机期间或股票牛市期间）

Reading 7 Asset Allocation with real-world constraints

1. 简答题：Advanteges and Limitation of Large asset and small asset.
2. large asset 缺点：
3. 投资小市值资产时会遇到流动性不足illiquidity occurred when invest in small-cap 
4. 投资小市值资产会导致更大的市场冲击invest in small-cap will cause market wildly fluctuate
5. 决策缓慢slow down decision making
6. small asset 缺点：
7. 某些资产有最小投资额限制，无法达到insufficient amount to meet the minimum requirement for some investment
8. 管理和人力资源受限lower governance and manpower resources
9. 管理成本高higher internal management cost
10. 由于资产规模小，分散化能力有限too small to diversify across the range of asset classes

二、Tax consideration 

1、rebalancing时税后range大于税前的range：因为tax高时，cost高，导致range应该提高以减少损失

2、债券放入tax deferred account; 股票放入taxable account

**Derivatives and Currency Management**

Reading 8 Option Strategy

1. 交易策略：
2. 股票核心测算：covered call, protective put, collar. （breakeven均为初始投资）
3. Spread (vertical): bull spread, bear spread.（breakeven = 低执行价格+premium）
4. Calender spread (horizontal arbitrage 到期时间不同，执行价格相同): long calender(买长期，卖短期，如long long-term option, short short-term option), short calender.
5. Straddle (at the money)，(strangle, out of the money): long, short (strangle, out of the money)（有两个breakeven price）
6. 期权交易策略总结

|            | direction                         | direction           | direction                         |
| ---------- | --------------------------------- | ------------------- | --------------------------------- |
| Volatility | Bearish                           | Neutral             | Bullish                           |
| high       | Buy put                           | Buy straddle        | Buy call                          |
| average    | Write call & buy put(short stock) | Spread(bull & bear) | Buy call & write put (long stock) |
| low        | Write call                        | Write straddle      | Write put                         |

注：如何合成期权，如long put = long call + short stock

1. Greeks
2. Delta: delta=change on option/change on stock, call delta 0 ~ 1, put delta -1 ~ 0; at the money delta约等于0.5, OTC趋向于0，ITM趋向于1(随着到期时间的临近，会越来越趋向于1)
3. Gamma: Gamma is largest when option is at the money, Deep OTM/deep ITM Gamma 均趋向于0，Gamma越大dynamic hedging越困难
4. Vega, Theta, Rho.

| Greeks            | Sensitivity factor | Call option (relationship)                  | Put option(relationship)                                     |
| ----------------- | ------------------ | ------------------------------------------- | ------------------------------------------------------------ |
| Delta             | Underlying price   | Positive (delta > 0)                        | Negative (delta < 0)                                         |
| Gamma             | Underlying price   | Positive                                    | Positive                                                     |
| Vega              | volatility         | Positive                                    | Positive                                                     |
| Rho               | Risk-free rate     | Positive                                    | Negative                                                     |
| Theta(time decay) | Passage of time    | Closer to maturityValue declines(theta < 0) | Closer to maturityValue declines(theta < 0)(除非European put option deep in the money) |

即long call, long put时， theta为负；long call/put Gamma为正，short call/put Gamma为负

1. Volatility smile:

1、Foreign currency option

2、Equity option (skew or smirk)：put价格被高估

简答题：为什么会出现smirk？

1. leverage：股价下跌，公司杠杆上升，风险上升，波动率上升
2. Volatility feedback effect: 反身性，波动上升——要求回报上升——股价下跌
3. Crashophobia : 害怕下跌

Reading 9 Swaps, Forwards, and Futures strategies

1. 管理Interest rate risk
2. Interest rate swap（同一种货币）: change exposure, adjust duration（adjust duration: receiver swpa,收固定支浮动，duration上升）
3. Forward rate agreement: underlying asset rate标价是利率 （long FRA，按固定利率借入，例2*6，第60天即是虚拟的开始借款日，也是结算日）
4. Short-term interest rate (STIR) Futures : underlying asset 100-r
5. Longer-dated fixed-income futures (T-bond futures): conversion factor, CTD principle (cheapest to deliver)

报价为标准化的虚拟债券FP（A), 交割是真实的债券（CTD原则）FP（f）,CTD是实际交割品

FP(A) = FP(f) * CF(A) 即 FP(CTD) = CF(CTD) * FP(f)，有CTD优先用CTD数据计算

注意BPV与Duration公式的转换

1. 管理Equity risk: cash equitization（通过期货讲equity的beta调整为0），调整equity的beta，股债之间的转换都要通过cash
2. 管理Volatility risk: VIX, variance notional/vega notional, time-weighted volatility
   1、Settlement amount = variance notional * (variance - strike variance)
   Vega notional(gain or loss 1% change in volatility) = variance notional * 2 * strike standard deviation
   2、variance swap如何mark to market, 加权计算公差 time-weighted average of realized variance
3. Inferring market expectation (Fed fund futures)

Fed fund futures contract price (美联储联邦利率期货) = 100 - expected FFE rate

反应市场对于美联储利率调整的预期（25bps为调整单位）

Reading 10 Currency Management: An Introduction

一、利率平价公式：假设各国真是利率相等，从长期来看，利率高是因为inflation高；利率高时，短期汇率升值，长期汇率贬值

二、外汇对冲

1、简答题：是否应该进行外汇对冲？

（1）Argument for not hedging currency risk :外汇对冲需花费时间和对冲成本；零和博弈 （zero-sum game）；长期来看，外汇会回到均衡水平in the long run, currencies revert to a theoretical fair value

（2）Argument for active management of currency risk：短期来看，外汇波动可能会非常剧烈short-run, currency movement can be extreme；很多外汇交易并不是由于公允价值，而会受到央行政策和国际贸易的扭曲many foreign exchange trade are dictated by international trade or central bank policy, not motivated by fair value

2、choice of currency management

1. passive hedging (与benchmark一样，并非不对冲): goal is to keep the portfolio’s currency exposure close to benchmark which used to evaluate performance
2. discretionary hedging: in contrast to a strictly passive hedging, the portfolio manager now has some limited discretion on how far to allow actual portfolio risk exposures to vary from neutral position
3. active currency management 通过主动管理，增加收益: the portfolio manager is allowed to express directional opinion on exchange rates, but should kept within mandated risk limits.
4. **currency overlay** 将外汇作为一个资产大类管理，但设立单独的外汇基金经理 : accepting and managing currency risk for profit can be considered as a portfolio objective

3、外汇对冲的原则：

（1）短期hedge，长期不hedge

（2）相关性，如果外汇与资产负相关就不用hedge

（3）相关性会改变，不能照搬历史数据

（4）债券更容易与外汇正相关，更需要hedge （外汇与债券背后的核心都是利率）

（5）hedge ratio 对冲比例会出现改变

三、外汇交易策略：

1、 relative currency/ volatility/ market condition

| Expectation       |              | action                            |
| ----------------- | ------------ | --------------------------------- |
| Relative currency | appreciation | Reduce hedge/ increase position   |
| Relative currency | depreciation | Increase hedge/ decrease position |
| volatility        | rising       | Long straddle (strangle)          |
| volatility        | falling      | Short straddle (strangle)         |
| Market condition  | stable       | Carry trade                       |
| Market condition  | crisis       | Discontinue the carry trade       |

2、carry trade: 

（1）covered interest rate parity长期成立(成立时则carry trade无意义)；短期可以利用carry trade exploit profit by investing higher yield currency and borrowing low yield currency (forward rate bias)

（2）如果美国人投资英国股票（股票风险+外汇风险）

If fully hedge 股票风险，则获得投资英国无风险收益率

If 进一步hedge外汇风险，则获得美国无风险收益率

1. Tactical trading decision : Roll yield
   positive roll yield 会让人倾向于hedge
   F > S, positive roll yield, 对象货币的远期价格高于现货，那么将对象货币以高于现货价格通过Forward对冲掉即有利可图
   当基金经理有观点时，比较Forward价格和预期的未来价格
   当基金经理无观点时，只比较spot价格和forward价格
   另外，对于Bond Futures, 如何arbitrage
   If the basis is positive即该债券的期货价格**低**于现货，即贴水backwardation(为什么贴水是positive basis，可以这样记忆：正常情况下，期货的价格都是应该低于现货的，这种情况下即为positive)，那么, a trader would make a profit by ‘selling the basis’,which is selling the bond and buying the futures
   If the basis is negative即该债券的期货价格**高**于现货，即升水contango, a trader would make a profit by ‘buying the basis’, which is purchasing the bond, and sell the futures
   Forward premium (aka Forward rate bias) , 即汇率远期价格高于现货
   例如IND/USD，USD较IND 利率高，可以做carry trade,USD有Forward premium, 即USD远期价格高于现货，即可以理解为有positive roll yield，这时远期做空美元，即higher forward premium on lower yielding currency，more profitable
2. 如何降低hedging cost
3. forward contract
4. Option
5. 多币种hedge策略
6. 通常多币种不用hedge， natural hedge
7. 如果要hedge，那么：

cross-hedge (proxy hedge) 用澳元代替新西兰元做hedge （当资产与期货变动不一致时，产生basis risk）

Macro-hedge一揽子对冲，即买入fixed-weight basket (属于cross-hedge的特殊情况).

Minimum-variance hedge ratio (MVHR,可以理解为回归方程的coefficient)

NDF， non-deliverable forward 元气不交割合同，而是采用主流货币进行现金结算

**Fixed-Income Portfolio Management**

固定收益资产的管理有三大类：ALM、AO、信用债

Reading 11 Overview of Fixed-Income Portfolio Management 

Reading 12 liability-driven and index-based strategies

Reading 13 Yield curve strategies

1. 基础知识：
2. Duration:
3. Macaulay duration : immunization, 以现金为权重的现金流的加权回收时间weighted average of the time to receipt of the bond’s promised payments
4. Modified duration : 用于研究价格变动
5. Effective duration :用于含权债券
6. Key rate duration：非平行移动，也叫partial duration。一般用于对比指数，所以用于AO场景下，对比某个关键时间点的利率改变，对比portfolio和benchmark价格变化的差异。
7. Empirical duration : 实践中观察利率变化对债券价格的影响，回归得到
8. Spread duration :有spread变化带来的债券价格的变化
9. Duration times spread DTS = spread duration * spread
10. Money duration = dollar * duration
    在实际应用中，也可以将dollar*duration *0.01作为money duration，可以从题目中的数字大小来判断是否需要乘0.01
11. Duration的计算，equity duration = asset duration - liability duration； portfolio duration = long asset duration - short asset duration. 在duration的计算中，要注意用value进行加权
12. BPV：price value of a basis point, bond price change given 0.01% change in yield to maturity
13. Convexity :用于衡量现金流的离散程度（dispersion）
    涨多跌少(在volatility上涨时获益)，当较大的平行移动时，需要用convexity+duration一起衡量 （含权债券价格的变动位effective convexity）。如何增convexity：long barbell, short bullet; long putable bond(putable bond convexity大), short callable bond(callable bond convexity为负)
    Callable bond significantly underperform non-callable bond when interest rate decline because of their negative convexity. Because the price increase of callable bond is limited by call price. 
    Callable bond: 发行商手里有call option， 债券价格=non-callable bond + short call option (即 - call option)， 即callable bond里面可以理解为内嵌了一个short call option
    MBS embedded with short call option (repay the debt early), and short call option has negative convexity.
14. Repurchase agreement (repo）：借入短期资金，买入长期债券
15. Liability分类

| Type               | I          | II            | III             | IV                                       |
| ------------------ | ---------- | ------------- | --------------- | ---------------------------------------- |
| Cash outlay amount | Known      | Known         | Unknown         | Unknown                                  |
| time               | Known      | Unknown       | Known           | Unknown                                  |
| example            | Fixed bond | Callable bond | Float rate bond | DB plan, property and casualty insurance |

1. swaption : receiver swaption 有权利进入一个swap，可以receive fixed， increase duration
2. Laddered portfolio : convexity 居中。优点：diversified/convexity in the middle/liquidity management ; 缺点：不如直接买ETF or mutual fund/ higher cost/ mutual fund can be redeemed quickly than bond

二、Asset-Liability Management (ALM): Liability-based

ALM :Asset-liability management 同时管理资产和负债

ADL: asset driven liability 资产固定（租约），管理负债，如租赁公司的融资经理

LDI: liability driven investing 负债固定，管理资产，如pension plan

1. cash flow matching : accounting defeasance, eliminate interest rate risk
   简答题：为什么不提早还？
   Buyback would be difficult and costly/ most bond illiquid/ corporate has motivation to improve the company’s credit rating by cash flow matching
2. Immunization: single liability(asset>liability, Macaulay duration match, convexity小)(convexity小，目的是minimize dispersion,即structural risk), multi-liability（asset>liability, Macaulay duration match, convexity of asset>convexity of liability）
   Structural risk : 由收益率曲线非平行移动导致immunization失效的风险叫structural risk（twist or non-paralleled shift），structural risk来源于非cash flow matching(zero-coupon bond), 即dispersion. Lead to changes in the cash flow yield that do not track the change in the yield on zero-coupon bond, this risk is minimized by lower convexity (low dispersion of cash flow)
   For multi-liability immunization, the convexity of asset should be higher than liability, but the convexity of the immunizing portfolio should be minimized in order to minimize the dispersion and reduce structural risk.
   Duration matching (immunization)只能应对较小的平行移动，convexity可以应对较大的平行移动
3. Derivative overlay: 期货份额（BPV，CTD）,保证金交易（Margin），流动性更好（注意与currency overlay虽然名字类似，但意义完全不同）
4. Contingent immunization: significant surplus

三、Total Return （AO）

1. Pure indexing ： full replication approach，risk factor match exactly (risk factor参见三中介绍)。优点：best diversification；缺点：neither feasible nor cost-efficient。
2. Enhanced indexing： stratified sampling, most primary risk closely matched (duration 要 match)。优点：efficient；缺点：less diversification
   Smart beta: involving the use of simple/transparent / rule-based strategies 主要用于股票，基于简单透明的原则进行交易。在股票中属于passive投资，在债券中属于enhanced indexing strategy
3. Active (在以下的不同市场情况下，如何做债券的主动投资): deviation from benchmark
4. Stable：Buy & Hold (买入高YTM的债券并持有到期), stable & steep (ride the yield curve)（买10年债券，三年底卖出）, carry trade（赚利差，借入短期低利率资金，买入长期高利率债券，repo/long future position使用保证金 / receive fixed swap支浮息收固息）
   Forward rate bias : investing in higher-yield currency, borrowing from low-yield currency, purpose : exploit uncovered interest rate party
5. Dynamic：

| Type                                     |                                                           | 交易策略                                                     |
| ---------------------------------------- | --------------------------------------------------------- | ------------------------------------------------------------ |
| Shift (Level)                            | 平行移动                                                  | 调duration                                                   |
| Slope （twist）                          | Steepen/ flatten （inverted）角度（长端-短端）            | Steepen: 卖长买短，duration neutral/bull steepen/bear steepenFlatten: 买长卖短，也是有三种情况 |
| Shape or curvature or butterfly movement | 收益率曲线突起的程度                                      | Negative butterfly (positive butterfly spread): short bullet,long barbell |
| Volatility (option)                      | Yield curve的volatility发生改变，进而带来option的价格改变 |                                                              |

Butterfly spread (positive or negative)= 2*middle term yield - long term yield - short term yield

Positive butterfly spread 也叫negative butterfly, 因为positive butterfly spread意味着中端利率上升，长短端的利率下降，这是就要long barbell (wings), short bullet (body)，由于body是主体，所以叫negative butterfly

1. Alternative method for passive investment
2. mutual fund: economies of scale规模效应，better diversification
3. 债券ETF: great liquidity, discount or premium relative to NAV (股票ETF的折溢价会因为套利而很快消失，但债券由于流动性不好，折溢价可能长期存在)
4. Total return swap : receive 债券指数，pay libor + pre-determined spread. 优点：no requiring of full cash outlay; 缺点：not actually own the underlying asset
5. 加杠杆的风险：
6. forced liquidation
7. Fire sale
8. Higher level of risk

四、Risk factor：衡量来自收益率变动的风险

1. 无风险收益率：
2. 平行移动：小用Duration衡量，大用Duration+Convexity。含权用effective Duration/Convexity
3. 非平行移动：key rate duration (PVD, present value of distribution)
4. Spread (广义)
5. Spread risk: 来自宏观经济，spread duration （研究组合时，duration contribution = spread duration * weight）
6. Credit risk ：来自微观，研究违约问题

五、债券收益的五因子分解（expectation）

1. Yield income
2. Rolldown return
   (1+2合称**roll yield**）
3. 由于利率曲线改变
4. Prob * LGD
5. 外汇

Reading 14 Fixed-Income Active Management : Credit Strategies

Credit rating ： BBB及以上级别的债券叫investment grade bond/ BB及以下级别的债券叫high-yield bond (trash bond)

1. General Credit Cycle characteristics

Early expansion/ Late expansion/ Peak/ Contraction

1. Credit Migration: 信用评级下调一级的概率高于上调的概率
2. 在任何信用周期内，high yield债券的收益率一定高于investment grade
3. Contraction & Early expansion时, high yield为inverted，contraction的inverted程度更严重，即短期违约概率高，长期违约概率低。简答题：why inverted ? The probability of downgrade or default is higher in the near term than longer term.
4. Bottom-up credit strategy
5. Reduced form model: 建模，使用specific company variable，估计一段时间内的违约概率（z-score)，内在原理不清晰
6. Structural credit model: 基于经济学理论，更精确，预测每天还有多久违约（defining the likelihood of default as the probability of the asset value falling below liability, with zero net asset defined as the default threshold），use market-based variables.
7. Empirical Duration (通过回归得到的实证久期)
8. in practice, credit spread tend to be negatively correlated with risk free interest rate.
9. Change in risk-free rate tend to generate smaller change in corporate bond yield than theoretical measure of duration suggest. 由于无风险收益率改变带来的公司债收益率的改变，影响较理论的小，因为部分被credit spread的反向运动抵消（negatively correlated）
10. Bond with large credit spread have less sensitivity to interest rate change than bond with smaller credit spread.垃圾债更像股票
11. 有时duration会是负数，即经济上升，利率上升，同时垃圾债券价格上升。
12. Spread
13. G-spread = yield on credit security - yield on government bond (G-spread指的是同maturity的债券，企业债相较于国债的spread，并不是国债相较于无风险利率的spread)
    国债 **when interpolated weighted by maturity(not by duration)**. 优：simplicity；缺：not smoother, interpolated 不够市场化。
14. I-spread = YTM - swap rate (ASW asset swap rate = coupon rate (corporate bond) - swap rate)
    这里的swap rate较government yield也会有spread。 优：smoother更加市场化；缺swap rate是由大型金融机构交易出来的。
15. Z-spread：基于不同的收益率曲线上的spot rate测算出来的spread （不含权债券优先用Z-spread，含权债券优先用OAS）

4、G-spread和I-spread是用不变的折现率，浮息时用DM；Z-spread是根据到期市场长短不同采用的折现率不同，浮息时用ZDM(zero discount margin)。

1. Excess spread
   Excess spread = spread * t - effective spread duration * change in spread - POD * LGD
2. Average credit rating
   Moody/ S&P/Fitch: 其中S&P与Fitch是同一体系，arithmetic Factor (分数为线性)；Moody的体系为每一级几何倍数增长，因此评级更保守。
3. Tail risk 作为风险
4. Var，value at risk, （5% 1.65倍标准差； 1% 2.33倍标准差， 年5%即每20年一遇）
5. VaR可能会misleading的原因
6. VaR tend to underestimate the frequency and severity of extreme adverse events. Fail to capture the downside correlation and liquidity risk associated with market stress scenarios. VaR会低估极端情况发生的频率和严重程度，没有考虑在市场极端情况下流动性与下行风险的相关性。
7. Fail to quantify the expected loss under an extreme adverse market scenario.并没有量化在极端市场情况下的损失有多大（只知道5%概率时的最小损失额），这个问题就引出了CVaR
8. VaR是度量某个区间内小概率情况下的损失，VaR其实是分位数的概念
9. CVaR，average & expected loss
10. Incremental VaR (partial VaR) 先计算VaR，引入一项新资产后再计算VaR，得出变化
11. Relative VaR 相较于benchmark
12. 度量尾部风险的3种方法
13. Parametric method：expected return & standard deviation。 优：简单透明；缺：不适用于非正态分布和含权组合。
14. Historical simulation：优：真实数据，适用于含权组合，对收益率分布无要求；缺：依赖所取历史数据的周期，依赖历史会重复。
15. Monte carlo simulation：优：适用于含权组合，从可能的分布中随机产生结果；缺：不透明，高度依赖模型假设。
16. CDS strategy
17. 利用CDS合成债券：long AAA(3%), sell CDS on B bond(4% short risk)= long B bond (7%)
18. CDS spread 可以认为是市场交易出来的公允报价，CDS coupon rate 对于investment grade为1%，对high yield 为5%
    CDS price = 1 + (Fixed coupon - CDS spread) * effective spread duration of CDS
19. Payer swaption on CDS ， 有权利付premium买入CDS
20. 信用债收益：五因子分解 + excess spread

**Equity Portfolio Management**

1. Passive Equity Investing
2. Benchmark selection : SAMURAI
3. Buffering 缓冲： 设立进入和推出的区间，解决migration问题
4. Packeting ：如1支股票符合两个指数（large & middle）的要求，那么将市值split，在下一个reconstitution date如市值仍符合large指数的要求，则股票的全部市值整体归到large指数中。
5. Rebalance调权重 ；Reconstitution调成分股
6. Weighting method
7. Market-cap weighting: most common, bias大市值。Free-float weighting自由流通股。符合mean-variance efficient
8. Price-weigh：每支股票买同样的数量，bias高价股
9. Equal-weight：每支股票买同样的金额，bias小市值。需要频繁的rebalance，least concentrated，higher volatility, limited investment capacity
10. Effective number of stock = 1/HHI = 1/每只股票权重的平方的和，衡量stock concentration. For equal weighed index effective number of stock = number of stock.
11. Passive Investment Strategy
12. Passive factor-based strategy（Smart beta） 复制指数的风险因子。优：less costly,get pure exposure to specific market segment ，offer factor exposure based on investor’s view of market (factor rotation, smart beta)；缺：风险(调高某一个factor时)和成本较复制指数高，track error高。
13. 复制指数：Full replication。要求成分股少。优：closely match；缺：costly。
14. 复制指数：stratified sampling。例如可用九宫格，或行业分。优：better cost,straight forward and technically unsophisticated；缺：higher tracking error,must consider size of sample。
15. 复制指数：optimization。量化方法，复制return/risk。优：lower tracking error than stratified sampling,account for covariance；缺：base on historical relationship and those can change,costly, create mean-variance inefficient。
16. 复制指数：blended approach。混合方法，例如大市值公司full replication, 小市值公司stratified sampling + optimization
17. 被动投资的工具：
18. Pooled investment：集合理财mutual fund/ETF。ETF优：handle shareholder redemption cheaply and efficiently,reduce taxable gain and loss；缺：higher transaction cost compare to replication by investor himself, illiquidity in secondary market。
    ETF has tracking error result from premiums and discount to net asset value/cash drag.
19. Derivative-based strategy：利用derivative调整exposure，不用于配置只调整。优：quick,efficient,liquid,cheap, easy to leverage the portfolio；缺：position limit, need to rollover(limited expiration),basis risk。
    有三种，completion overlay调偏离（相比于benchmark）; rebalancing overlay调资产配置（如股债比例）; currency overlay调外汇exposure
20. Separated-managed index-based portfolio 专户
21. Tracking error

Causes:

1. management fees
2. Commission to execute trade
3. Higher transaction cost for less liquid security
4. The use of intra-day trading to manage the portfolio (benchmark is closing price)
5. Cash drag

Controlling tracking error:

1. minimizing trading cost
2. Netting investor cash inflow and redemption
3. Using equitization tools like derivative to compensate for cash drag
4. Active Equity Investing
5. Fundamental (discretionary, subjective)
6. bottom-up strategy:
   Value-based: relative value; contrarian investing; high-quality value; income investing; deep-value investing; restructuring and distressed investing; special situation
   Growth-based: consistent long-term growth; shorter-term earning momentum; GARP growth at reasonable price
7. Top-down strategy: country and geographic allocation to equity; sector and industry rotation; volatility-based strategy; thematic investment strategy
8. Pitfall in fundamental investing:value trap(may in fact be over value and decline further)/growth trap(future growth prospects already reflected in price)
9. Quantitative (systematic, objective), 即factor-based strategy

Rewarded (persistent/long term excess return) and unrewarded factor

1. Hedge portfolio approach：基于某个因子排序，最空后10%，做多前10%
2. Factor mimicking portfolio (Pure factor model)：只对某一个因子有exposure，对其他因子beta为0
3. Factor timing：因子择时，因子随时间的变化而变化

Pitfall in quantitative investing:

1. survivorship bias: if back-test are only applied to existing company, then will overlook the failed company in the past
2. Look-ahead bias: use information in the model to give trading signal at a time when the information is not available
3. Data mining/overfitting : excessive search analysis to find in data that show a strategy working
4. Turnover: constraint on turnover
5. Lack of availability of stock to borrow
6. Transaction cost
7. Quant overcrowding: occur if many quantitative manager follow similar strategy
8. Activist strategy

Activist strategy特点：

1. typically less than 10% share
2. Time horizon shorter than buy and hold

Target company:

1. Slower revenue and earning growth
2. Suffer negative share price momentum
3. Weaker-than-average corporate governance
4. Other strategy
5. statistical arbitrage
6. Pair trading
7. Event-driven strategy

5、Portfolio construction ：Top-down/bottom-up 与 systematic/discretionary

|            | Top-down                                                     | Top-down                                                     |               |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------- |
| systematic | Emphasize macro factorFactor timingDiversified               | Emphasize macro factorFactor timingDiversified or concentrated depending on strategy and style | discretionary |
| systematic | Emphasize security specific factorNo factor timingDiversified | Emphasize security specific factorPotential factor timingDiversified or concentrated depending on strategy and style | discretionary |
|            | Bottom-up                                                    | Bottom-up                                                    |               |

1. 识别基金经理风格
2. Holding-base：偏定性 style box
3. Return-base：看组合的收益水平与哪个指数高相关
4. Self-identification：自我识别
5. Holding-base vs return-base

|              | Advantage                                                    | Disadvantage                                                 |
| ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Return-base  | Require minimal informationExecute quickly,cost effectiveMore widely applied | Inefficient to identify current style,Difficult to detect more aggressive position |
| Holding-base | More accurate comparison of individual position便于不同风格之间的比较,Capture change in style quickly | More data needed,Less effective for fund with substantial position in derivative |

1. Return来源
2. Factor weighting：overweight or underweight factor, rewarded and unrewarded factor
3. Alpha skill: 择股 & 择时（factor timing, skillful timing exposures to factors）
4. Positioning (头寸， exposure)
   Expected active return = IC * √BR * standard deviation of active return*TC
   IC :information coefficient 决策能力（预测能力）
   Breadth:独立决策的次数
   TC: transfer coefficient 行动能力
5. Absolute vs relative return :

|           | Absolute return       | Relative return            |
| --------- | --------------------- | -------------------------- |
| objective | Maximize sharpe ratio | Maximize information ratio |
| Risk      | Volatility            | Tracking error             |

1. Risk
2. Active share
   (Weigh of portfolio - weight of benchmark)/2
3. Active risk: factor 有偏离，一定有active share; 但有active share却不一定factor有偏离
   Factor neutral and diversified stock picks: 如两只股票在benchmark的权重不同，但factor sensitivity一直，active risk受到degree of correlation影响
   Active risk increase when a portfolio becomes more uncorrelated with its benchmark.
   Closet indexing：宣称是主动投资，但active share小，复制指数 (is the strategy used to describe fund that claims to actively investment but wind up with a portfolio not much different from the benchmark)
4. Risk budgeting：计算出又A股票贡献的波动占总portfolio的比重（将weight替换成beta，即可计算出基于factor的absolute risk比重）
5. 持仓策略
6. Long-only

Long-only的好处：

1. long-term risk premium
2. Capacity (借不到股票做空)
3. Limited legal liability laws
4. Regulation (short selling)
5. Transactional complexity
6. Cost
7. Personal ideology
8. Long/short
9. Long extension portfolio: 130/30
10. market neutral (pair trading): beta = 0

Long/short strategy benefit

1. short position can reduce market risk
2. Short expand benefit from other risk premium and alpha
3. Combination of long and short greater diversification

Long/short strategy drawback:

1. short position reduce market return premium
2. Short amplify the active risk
3. Higher implementation cost, greater complex
4. 加杠杆后的收益：

例：leverage factor is 2

Return = leverage factor * expected arithmetic return - (leverage factor * standard deviation of return)²/2

**Alternative Investment for Portfolio Management (hedge fund strategy)**

1. Equity Strategy
2. long/short equity: net long 
3. Dedicated short selling and short-biased
4. Dedicated short-selling fund 只做空（take a bottom-up approach）
5. short-biased 偏向于做空
6. activist short selling

3、Equity market neutral：策略使用时机during periods of market vulnerability and weakness

A market-neutral portfolio carries no systematic risk, therefore has a zero beta and should be measured as the risk-free rate.

二、Event-driven strategy

1、Merger arbitrage

2、Distressed securities: liquidation买债券（senior secured debt > junior secured debt > unsecured debt > convertible debt > preferred stock > common stock）；re-organization买股票

三、Relative value strategy

1、Fixed-income arbitrage (Pair trading)

2、Convertible bond arbitrage

四、Opportunistic strategy：大量使用衍生品，right-tail，top-down

1、Global macro strategy: Focus on global relationship across a wide range of asset classes and investment instruments. Global macro strategy are typically top-down and employ a range of macroeconomic and fundamental models to express a view regarding the direction or relative value of an asset. 以基金经理的主观判断为准discretionary

2、Managed futures: Focus on futures/options on futures and forward & swap, show a characteristics that natural positive skewness. 量化systematic

1. time-series momentum trend following 趋势追踪
2. cross-sectional momentum strategies 赌价差托大

五、Specialist strategy: require highly specialized skill sets for trading, two such typical specialist strategies which are aimed at generating uncorrelated, attractive risk-adjusted returns

1、Volatility trading

1. time-zone arbitrage 同一资产不同时区的波动率差异pair trading
2. cross-asset volatility trading 两个资产的波动率出现差异pair trading

2、Reinsurance/Life settlement

简答题：对冲基金要投资具有以下特征的保单：

1. surrender value low 退保价值低（保单转让的成本低）,即被保险人由于退保价值低，进行退保操作的可能性低
2. The ongoing premium payment to keep the policy active is low 维持保单有效持续的保费缴纳金额低
3. The probability is high that the designated insured person is likely to die with a certain period of time (earlier than predicted by standard actuarial method) 被保险人早于预期死亡（即更早获得赔偿）

六、Multi-manager strategy

1、Fund-of-funds

2、Multi-strategy hedge funds

3、FOF vs multi-strategy

|      | FOF                                                          | Multi-strategy                                               |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 优   | DiversificationLow left-tail riskLow volatility (low return) | Better fee structureEfficient TAA (tactical asset allocation)transparent |
| 缺   | Low transparencyAdditional layer of feeNot efficient TAA     | High left-tail riskHigh leverageComplexHigh risk             |

七、Asset-allocation

1、Traditional approach

优：easy to communicate; relevance for liquidity management and operational considerations

缺：over-estimation of portfolio diversification (risk-factor overlapping; obscured primary drivers of risk 不知道风险的驱动因素)

2、Risk-based approach

优：common risk factor identification(investor is able to identify common risk factors across all investment, whether public or private, passive or active); integrated risk framework(is able to build an integrated risk management framework, leading to more reliable portfolio-level risk quantification); develop more robust asset allocation

缺：sensitivity to historical look-back period; implementation hurdles执行困难；determining which risk factor to use and measure can be subjective

八、Private equity fund performance Evaluation

1、IRR & MOIC (multiple on invested capital)

MOIC = (NAV + distribution)/paid-in-capital

2、IRR vs MOIC：如果PE早期的现金流入多，则IRR较高，limited partner（LP）不喜欢用IRR来评价业绩，因为支付给general partner（GP）的奖金incentive 多，反之亦然

**Private Wealth Management**

私人财富管理的流程，个人IPS的构建。

This IPS identifies the needs, goals, and risk tolerance of the investor, as well as constrains under which the investment portfolio must operate.

Reading 21 Overview of Private Wealth Management

1. Private Client versus Institutional Client
2. Client Goal of Private Client
3. Planned Goal
4. Unplanned Goal: Property repairs/ medical expenses/ other unforeseen spending
5. Investment Planning Methods
6. Capital Sufficiency Analysis: also known as Capital Needs Analysis. To meet financial goals and objectives, clients must have sufficient capital or follow a plan that will likely result in sufficient capital.
7. deterministic forecasting
8. Monte Carlo simulation
9. Retirement planning：three methods to analyze a retirement goal
10. Mortality tables：indicate individual life expectancy at specified age每一年的花费*当年的存活概率，现值的和
11. Annuities: mitigate the longevity risk. Immediate annuity/deferred annuity (简答题annuity puzzle, individual’s tend to not to prefer to invest in annuity: reluctant to give up the hope of substantial lifestyle improvement/ dislike of losing control over the asset/ the high cost of annuity)
12. Monte Carlo Simulation
13. Investment policy statement (IPS): 6 parts
14. Background and investment objective
15. Investment parameters: RRTTLLU
16. Portfolio asset allocation
17. Portfolio management: discretionary authority/ rebalancing/ tactical change/ implementation
18. Duties and responsibilities : IPS report/ IPS review
19. IPS appendix: 
20. Tax Strategy
21. Tax avoidance
22. Tax reduction
23. Tax deferral: TDA/ time period management/ tax loss harvesting/ HIFO, highest in, first out
    这里要注意TDA内存入的钱是pre-tax，所以在取钱的时候并不是赚钱的部分要交capital gain tax，而是本金+利润作为一个整体一起交税，比如20%。（TEA，tax exempt存入的是税后资金，账户内和取钱时均无需交税，TEA与TDA哪个账户合算需要具体问题具体分析）
    tax loss harvesting的好处？
    Pushing a portion of tax liability into subsequent years, even though the total tax liability does not change. Realizing an already incurred loss for tax purpose save tax in the current year, which could lead to a greater future wealth accumulation.
24. Tax location: tax inefficient asset-- TDA/TEA, tax efficient asset-- taxable account
25. Tax rollover
26. Evaluation the success of an investment program

简答题：从4个方面判断目标是否完成

1. Goal achievement with an acceptable amount of risk to achieve goal.
2. Process consistency. (if followed the IPS)
3. Portfolio performance: absolute or relative
4. Definition of success for client’s investment program.

Reading 22 Topics in Private wealth management

Three issue :

1. the impact of taxes on wealth accumulation
2. The management of concentrated positions in public or private assets
3. Basic tools and techniques for preserving wealth through generations
4. Tax
5. Tax location :
6. Tax efficiency and tax inefficiency asset各类资产放入不同的税收账户（taxable account/TDA/TEA）
7. Decumulation strategies for a retirement account (简答题：退休后从哪个账户取钱最优Withdraw from taxable account first and allow the retirement account to continue to compound. Under progressive tax regime (累进税制) more tax-efficient strategy is withdraw from retirement account until the lowest tax bracket have been fully utilized.)
8. Basic concept of taxation
9. Measuring tax efficiency效果的四种方法
10. After-tax holding period return: 税后收益率，可Annualized也可Cumulative
11. After-tax post-liquidation return: embedded capital gain
12. After-tax excess return: 不同税收管理方案中比较tax alpha哪个更好，tax alpha = after-tax excess return(与benchmark比较)和pre-tax excess return的差
13. Tax-efficiency ratio
14. Impact of taxes on capital accumulation : taxable account/TDA/TEA
15. 从税收的角度考虑如何selection of investment vehicle
16. Partnership: avoid double taxation
17. Mutual fund (简答题：为什么mutual fund tax inefficiency : tax liability is influenced by co-investor and for all shareholders/ distribution of capital gain tax/ loss can not be the tax shield for other asset (unlike SMA separate-management-account)/ potential capital gain exposure PCGE(PCGE越小越好))
18. The management of concentrated positions
19. 对象：public traded stocks/ private owned business/ real estate
20. 目标：
21. Reduce risk
22. Generate liquidity
23. Tax efficient way
24. Risks of concentrated position
25. company-specific risk
26. Lack of diversification
27. Liquidity risk
28. Outsize tax bill (normally low tax basis for concentrated position)
29. Ways to mitigate the risks
30. Sell and diversify: lose control, tax, endowment
31. Staged diversification: tax avoidance & tax deferral
32. Tax-free exchange 交换基金，缺点为持有周期长、diversify效果不足（取决于基金内的股票）
    A partnership in which each of the partners have each contributed low cost-basis stock to the fund.
33. Hedging and monetization strategy
    Equity monetization: receive cash for their stock position without an outright sale, structured to avoid triggering the capital gain tax. 分为两步，首先对冲风险，已提升loan-to-value ratio, 然后股权质押borrow against the hedged position.
34. Charitable giving strategy: charitable remainder trust. Make donation without trigger of tax event, no longer have ownership of the asset. Within the trust, the shares could be sold and reinvested in a diversified portfolio without incurring capital gain tax, and the trust could provide income for the life of the named beneficiaries, when all beneficiaries dies, any asset remaining in the trust would be distributed to the charity named in the trust.本质是一个irrevocable trust
35. Strategies for managing concentrated positions in public equity
36. Staged diversification and completion portfolios
    Staged diversification其实就是在一段时间内分成几份卖出, and reinvest the proceeds in a diversified portfolio。advantage: spreading the tax liability across multiple year, but it also extend the time that investor will be overly exposed to the stock (concentrated position)
    Completion portfolio: 将concentrated position卖出（或staged sell out）,剩余部分(could minimize the tax liability)+另行购入其他股票，组成portfolio similar to the benchmark. The completion portfolio can exclude the stock which has high correlation with the concentrated position.
37. Tax-optimized equity strategy：equity monetization/ collar/ call write
38. Strategies for managing concentrated positions in private equity
39. Sale to an insider
40. Divestiture of non-core assets
41. Personal line of credit secured by company shares(即已公司股份为抵押的贷款)/ Leverage recapitalization
42. Employee stock ownership plan
43. Strategies for managing concentrated positions in real estate
44. Mortgage financing 将房产抵押后贷款
45. Real estate monetization for the Charitably inclined (DAF donor-advised fund)
46. preserving wealth through generations
47. Gift vs Bequest: 活着时赠予为gift，死后遗产赠予为bequest。考虑税的情况下，哪种赠予的方式更合算，需要考虑财产所有人和受益人的tax、investment return.
48. 如何规避Probate: Joint ownership共同所有权 / life insurance/ Trust
    Forced heirship 强制继承权（剩下的财产按遗嘱），community共同财产（夫妻）涉及到夫妻共同财产的部分
49. Trust: revocable/ irrevocable(against claim from creditor of settler)

Settler -- Trustee -- Beneficiary

Fixed trust/ discretionary trust (against claim from creditor of beneficiary)

Irrevocable trust的好处？

1. Protection of the asset within the trust from claims outside the family (beneficiary)
2. Avoid dispute within the family
3. Transfer of asset without the potential publicity associated with probate, keep privacy
4. Worried about their children can not manage the asset themselves because children are minors

Reading 23 Risk management for individuals

1. Human capital, financial capital, economic net worth
2. Economic net worth (net wealth) = net worth (traditional asset- liability) + present value of future earning -present value of future expense
   其中unvested pension plan属于present value of future earning中，vested pension plan是属于个人的所以在net worth中
3. Human capital: 未来工资折现求和
   由于工资有年化增长，且有折现率，因此可简化计算：（1+折现率）/（1+工资增长率）
4. Financial capital: 即individual’s asset 包含personal asset and investment asset, 比如房产就属于financial asset,因为既有投资属性又可自住，所以属于mixed asset
5. Individual risk exposures
6. Earning risk: disable insurance
7. Mortality risk(也叫premature death risk): life insurance
   Life insurance protect against the loss of human capital from future earning 所以当human capital低时就没有必要选择life insuance了
8. Longevity risk: annuity
9. Liability risk: liability insurance责任险（如第三者责任险）
10. Risk Management strategy

| Loss characteristics | High frequency         | Low frequency                  |
| -------------------- | ---------------------- | ------------------------------ |
| High severity        | Risk avoidance(如滑雪) | Risk transfer (insurance)      |
| Low severity         | Risk reduction         | Risk retention(self-insurance) |

self-insurance：事先不监控风险，风险事件发生后，用准备好的钱弥补损失，是最消极的风险管理方式

1. Type of life insurance
2. temporary life insurance: for a certain period of time specified at purchase
3. Permanent life insurance: lifetime coverage
4. whole life insurance
5. Universal life insurance 万能险，兼顾保障+投资需求
6. Life insurance的一些条款
7. non-forfeiture clause : could still receive some portion of benefit if premium payment is missed (forfeiture:财产等的没收，名誉丧失)
8. Health maintenance organization plan : allow office visit at no cost
9. Waiver-of-premium rider: the premium need not to be paid if the insured becomes disabled （waiver：对权力的放弃）
10. Guaranteed insurability rider: allow the owner to purchase more insurance in the future at certain predefined intervals
11. Cash value

Gross premium (保费) = net premium (通过死亡概率计算得出) + cash value + expense（sales + operational）+ profit (保险公司)

1. Annuity
2. 投保人之间Yield的收益率高低：身体差的Yield高
3. Inflation hedge
4. 是否允许退保
5. Cost
6. 年金的支付方式：Joint-life(夫妻双方有1人存活则继续领取年金) / Ordinary or refund（被保险人死亡时如果没回本，则退还本金） / period-certain(年金最少给10年，即使提前死亡)
7. Advanced life deffer annuity’s payment : begin later in life, payment will be received far in the future, for longevity risk
8. Low interest rate environment: when buying a fixed annuity the investor locks in payments based on current low interest rate, will lock in relatively low payment.
9. High expected inflation: the real value of payment from a fixed annuity declines over time due to inflation, and rising inflation exacerbates this problem.
10. Fixed annuity is not liquid (especially for non-trade-out provision)

**Portfolio management for institutional investors**

1. 机构投资者分类（六类）：

| 机构投资者类型         | Tax        | Liability         | Time horizon                                                 |
| ---------------------- | ---------- | ----------------- | ------------------------------------------------------------ |
| Pension plan (DB & DC) | 免税       | Legal liability   |                                                              |
| Sovereign wealth fund  | 免税       |                   |                                                              |
| University endowment   | 免税       | 非legal liability | Perpetual                                                    |
| Private foundation     | 有条件免税 | 非legal liability | Limited-life (虽然很长的投资周期)                            |
| Bank                   | 需交税     | Legal liability   | Liquidity core considerationShort time horizon               |
| Insurer                | 需交税     | Legal liability   | Life insurer:long-duration，确定性高certaintyP&C(property&casualty):short-duration,uncertainty,流动性要求高 |

Foundation vs Endowment

|                | Foundation                                               | Endowment                       |
| -------------- | -------------------------------------------------------- | ------------------------------- |
| Liability      | 5% of asset                                              | 无强制，自己指定spending policy |
| Liquidity need | At least 5%                                              | 2%~4% 有固定捐赠                |
| Time horizon   | Limited-life foundation                                  | Perpetual                       |
| Risk           | High risk tolerance with some short-term liquidity needs | Higher than Foundation          |

注：Endowment spending policy: spending下一期 = spending上一期*（1+inflation）*w + （1-w) * (spending rate * average AUM average under management)

Life insurance & non-life insurance 不同点

1. Time horizon: life insurance长
2. 巨灾险：loss long-tailed, 理赔周期长
3. Replacement cost coverage
   Non-life : inflation提高，则赔款会逐年增加
   Life insurance ：除条款规定的，不会受inflation的影响
4. Underwriting cycle: 承保周期（与经济周期相关）
   寿险：不明显
   非寿险：周期性明显（如车险，经济好，买车的人多则车险销售好）
5. Liquidity needs：非寿险needs高
6. Asset allocation：
7. 寿险annuity ：要求现金流稳定，投资债券
8. Life-insurance：liquidity一次性大额，以投资股票为主
9. Non-life insurance : 流动性cash + equity
10. 对利率的敏感性：寿险高（因为久期大）
11. 分析框架（RRTTLLU, risk/return/time horizon/tax/liquidity/legal/unique）

| New分析框架                         | Old分析框架             |
| ----------------------------------- | ----------------------- |
| Stakeholder 利益相关者如Gov、投委会 |                         |
| Liquidity needs 现金流出            | Liquidity needs         |
| Liability and investment horizon    | Time horizon            |
| External constraints                | Legal, tax, unique      |
| Risk (only for DB & DC)             | Risk (only for DB & DC) |
| Asset allocation (重点为ALM)        |                         |

1. Asset Allocation方法
2. Asset only (AO)：MVO，对整体进行优化求解
3. ALM：Asset与liability互相匹配。LDI liability driven investment 现金流匹配，适用于DB、bank、insurer
4. 机构投资者的优劣势：

优：diversification; hire professional

劣：high market impact; 有些arbitrage大资金不好做；diseconomy of scale规模不经济（PE or mutual fund, 市场上好项目有限）

1. Investment Approach
2. Norway Model (sovereign wealth fund): AO，保守，passive，传统股债60/40
   优：tracking error小，transparent，cost小，easy for board to understand
   劣：limited value-added potential
3. Endowment model (university endowment): high alternative exposure, active management, outsourced, AO
   优：high potential return
   劣：cost大，tracking error大，波动大，may concentrated
4. Canada model: AO, high alternative exposure,active management, internally managed
   优：high potential return
   劣：cost大，tracking error大，波动大，may concentrated
5. LDI model: ALM, bank & insurer & DB plan (duration match, return-generating portfolio)

优：考虑了负债

劣：只能对冲一部分风险，通胀、长寿风险无法完全对冲掉

Funded ratio = asset/obligation(PBO)

1. Sovereign wealth fund

从上到下依次liquidity needs 从低到高

1. saving fund 储蓄基金，用于wealth across generation
2. Development fund 项目主导，infrastructure：long/medium time horizon
3. Reserve fund 外汇储备基金，reduce negative carry cost
4. Pension reserve fund 养老基金， accumulation stage/ decumulation stage
5. Budget stabilization fund 平准基金：市场好时抗通胀，市场差时促发展（短期）

**Trading, performance evaluation and manger selection**

Reading 25 Trade Strategy and Execution

1. 交易前：reference price选择
2. Pre-trade benchmark：is a reference price that is known before the start of the trading take place. 总体上risk tolerance低，urgency高，不愿意承担execution risk(is the risk of an adverse price movement occurring over the trading horizon because of change in fundamental value of the security or trading-induced volatility). Pre-trade benchmark is widely used for seeing short-term alpha by buying undervalued or selling overvalued.
3. decision price/previous close: quantitative portfolio manager
4. Opening price: Fundamental portfolio manager, no overnight risk, not suitable for transaction during opening auction
5. Arrival price: greater trade urgency. At the time the order is entered into the market for execution.

Goal : transaction at or close to current market price

1. Intra-day benchmark: is based on a price that occurs during the trading period. urgency程度一般，一般为日内完成即可, manager without view on short-term price movement
2. VWAP: volume-weighted average price
3. TWAP：exclude potential trade outliers 
4. Post-trade benchmark（收盘价，适用于mutual fund/ETF，申购subscribe赎回redeem均按照收盘价, receiving proceeds at NAV）: a reference price that is determined at the end of trading. minimize tracking error (NAV)
   优：minimize potential tracking error
   劣：not know until the trade complete
5. Price target：urgency程度高，适用于short term & overvalue/undervalue

目的：seeking short-term alpha, more favorable price

1. 交易中
2. 交易场所选择
3. higher-touch approach 人工，用于大单
   Principle trader (dealer) : urgent, bid-ask spread
   Agency trade (broker) : non-urgent 撮合交易
4. Low-touch

OTC：non-exchange (AFS & MTF)

Direct market access (DMA)交易所智联 : buy side, small, non-urgent, derivative，对冲基金

Dark pool暗盘 : large, illiquid, non-urgent, less information leakage

1. 算法算则algorithmic trading
2. Scheduled : urgency程度一般
   POV (percentage of volume) 参与度算法：定一个参与度，下单量=成交量*参与度
   优：take advantage of increased liquidity
   劣：higher trading cost, may not complete within the time period specified
   VWAP: for illiquid stock, time slicing, may not complete
   TWAP：没有利用流动性，scheduled交易算法中完成可能性最高的
   优：ensure the specified number of shares are executed within the specified time period
   劣：will not take advantage of increased liquidity condition
3. Liquidity-seeking (opportunistic algorithms) : large order, execute quick without impact, liquidity sweeping, sweep the book, dark pool
   Take advantage of market liquidity across multiple venue by trading faster when liquidity exist at a favourable price
   优：appropriate for large order; executed quickly without having a substantial market impact; 寻找隐藏的流动性hidden order
4. Arrival price algorithm : urgency高，small to medium order
   Seek to trade close to current market price; front-loaded strategy; suitable for traders who believe price will move unfavorably during the trade horizon
5. Dark strategy (liquidity aggregator),如dark pool, 反义词即是lit market(交易所) : large, illiquid, non-urgent, less information leakage，less transparent
   Appropriate for order size large; illiquid; wide bid-ask spread, urgency程度低
6. Smart order router (SORs) 智能定价路由: small, monitor lit & dark market

Highest probability of executing small order with best price; continuously monitor market in real time; appropriate for small order and high-urgency

1. 交易后：trade evaluation交易评估
2. implementation shortfall (IS) = paper return - actual return
3. Expanded IS = delay cost + trading cost + opportunity cost + fees
   Delay cost + trading cost 合称execution cost（execution risk: a risk of adverse price movement during the trading horizon）
   注意区分trading cost 和 transaction cost
   Delay cost: from decision price ----- arrival price
   Trading cost: From arrival price ----- actual price of finish the trading
4. Implementation shortfall (bs) cost in basis bps = IS/(total shares * decision price) . IS 从 decision price开始，分母不是损失，而是总成本
5. Cost in basis point (bps) = side * (trading price - benchmark price)/benchmark price
   cost<0说明outperform
   Side: +1 buy, -1 sell
   比如计算arrival cost in bp, 是 （trading price - arrival price）/arrival price, 注意并不是arrival price - decision price
   Arrival cost = actual trading price - arrival price (aka trading cost) 即arrival cost是从arrival这里开始算的，损失的利润
   注意这里的计算很单纯，不需要考虑成交的数量，只需要trading和arrival两个数据就够了
6. Market-adjusted cost (bps) = arrival cost (bps) - beta * (index VWAP - index arrival price)/index arrival price
   Separate trading cost due to trading the order from the general market movement
   不是看大盘涨跌是否赚钱，而是大盘涨跌与做交易的方向是否一致。当卖出时，大盘越跌表示卖出的价格越低，即实际成交的价格优于benchmark的难度越大，cost<0说明outperform
7. Add-value (真实-预测) = arrival cost (bps) - estimated pre-trade cost (bps)

Add-value >0, 即underperform

Reading 26 portfolio performance evaluation & reading 27 investment manager selection

1. 业绩归因
2. 归因角度

| Macro contribution                   | Micro contribution          |
| ------------------------------------ | --------------------------- |
| Fund sponsor 从manager角度，多个账户 | Individual manager(account) |
| Strategic asset allocation           | Tactical deviation          |
| 为多个account做整体归因              | 某一个具体账户              |

1. 宏观归因macro：站在sponsor角度，strategic asset allocation
2. 微观归因micro：站在manager角度，找alpha的来源

| Micro归因方法     | 特点                                                         |
| ----------------- | ------------------------------------------------------------ |
| Return-based      | Easiest method;Not use the underlying holding, least accurate;Most vulnerable to data manipulation |
| Holding-base      | Fails to capture the impact of any transaction;Suitable for little turnover |
| Transaction-based | Use both holding and transaction;Most accurate;Most difficult and time-consuming |

1. Equity归因
2. Holding: 
   BHB：

| Selection alpha       | Interaction alpha |
| --------------------- | ----------------- |
| 纵轴Return/横轴weight | Allocation alpha  |


BF: 更精确，原点从整个benchmark return开始计算

1. Factor-based (return-based)

factor tilt 因子偏离产生的收益，要看beta*factor哪个大，不能只看beta

市场因子RMRF：当beta>0则说明存在对该factor的tilt，index - T-bill

小市值因子SMB：small minus big

价值因子HML：high minus low, high for high book value即价值股(L代表成长股)，HML的sensitivity如果是负数（或者小于benchmark）则可判断组合tilt towards growth stock

趋势因子WML：winner minus loser 

1. Fixed-income归因
2. Holding
   Exposure decomposition: duration based 简单，short/long exposure, government/corporate bond, weighting
   Yield curve decomposition: duration based 精确，shift/slope/curvature分别判断
3. Transaction base：Yield curve decomposition, full repricing based 最精确
4. Risk attribution

|              | Relative risk (vs Benchmark)                                 | Absolute risk （绝对数字）                                   |
| ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Bottom-up    | Position’s marginal contribution to tracking risk            | Position’s marginal contribution to total risk               |
| Top-down     | Attribution tracking risk to relative allocation and selection | Factor’s marginal contribution to total risk and specific risk |
| Factor-based | Factor’s marginal contribution to tracking risk and active specific risk | Factor’s marginal contribution to total risk and specific risk |

1. Benchmark
2. portfolio收益的分解：market/style/active, 要求active与style收益的相关性低
   Active return = portfolio return - benchmark return
   Style return = benchmark return - market portfolio 即当benchmark本身就是大盘指数时，style return为0
3. Benchmark特点，SAMURAI
   Specified in advance
   appropriate
   Measurable
   Unambiguous
   Reflective of current investment opinion 能反应基金经理观点
   Accountable 靠谱的，客户与manager都同意，如双方都可接受、合理的benchmark
   Investable
4. 几种典型benchmark

Absolute return/broad market index

Style index

Factor-based base 回归，因子可随意指定，如GDP，所以可能不满足investable

Return-based 回归，因子时风格指数构成的，满足investable。Return-based的原理是用过去的自己作为benchmark，即用以往自己的return回归得到了方程，只要跑赢了过去的自己就可以

Manager universe: peer group 中位数

Custom security-based

1. Performance appraisal业绩评价指标
2. sharpe ratio = （portfolio return - risk free return）/portfolio risk：适用于concentrated portfolio
3. Treynor ratio = (portfolio return - risk free return)/portfolio beta：适用于diversified portfolio，衡量承担市场风险所带来的超额回报
4. Information ratio : active risk
5. Capture ratio = upside capture ratio/downside capture ratio 衡量凸性，即涨多跌少
6. Appraisal ratio = Jensen’s alpha / SEE 承担非系统性风险的超额回报estimate the alpha per unit of company-specific risk to make security selection decisions.
7. Sortino ratio = (portfolio return - minimum acceptable return (MAR))/downside standard deviation
   Characteristics:
   只惩罚了harmful deviation下行风险；
   非对称，offer the ability to accurately assess performance when return distribution is not asymmetrical;(由于是衡量非对称的风险，所以sortino ratio适合衡量option writing and commodity derivatives)
   关于tail risk；
   Preservation capital 适用于想保留利润时；
   Limitation：不同的人MAR不同，无法放在一起比较（想要比较需MAR相同时，就像大家的risk free return都相同）
8. Roy’s safety-first criterion = (E(r)- return threshold level)/standard deviation of return for the portfolio
9. Maximum drawdown/ maximum drawdown duration

注意区分maximum drawdown begin(从最低点开始回升计算) 和maximum drawdown recovered（净值回到历史最高点）

Reading 27 Investment manager selection

1. Type I & Type II error

原假设：the manager add no value (希望基金经理有alpha，即将原假设设定为相反的，用于推翻原假设)

1. Type I error：去真（基金经理本身能力不行，即假设检验结果为拒绝了能力不行的假设，留用）occurs when a manager is hired or retained who subsequently underperform expectation. Hiring because its recent outperformance, if he underperform expectation in the future, it will lead to a type I error.
2. Type II error：受伪（基金经理本身有能力，但假设检验没有拒绝能力不行的原假设，开除）when a manager who subsequently outperform in line with expectation, but not hired

The smaller the difference in sample size and distribution mean, and the wider the dispersion of the distribution, the smaller the expected cost of Type I and Type II error. 样本量和mean收益差不多的情况下，离散大的时候更容易分辨基金经理的好坏。

1. 基金经理风格判断（style drift 检查）
2. return-based: top down, 回归，看哪个因子的beta大，即属于哪个风格
   优：not require large amount of data; can be estimated even for complicated strategy, is comparable across managers
   缺：based on static portfolio(inaccuracy，发现style drift速度慢，用回归时需要较长时间才能影响到回归结果); illiquid security(if the portfolio contains illiquid security, the lack of current price on those positions may lead to an underestimation of portfolio’s volatility)
3. Holding-based：bottom-up
   优：estimation of current risk factor(accuracy, 发现style drift速度快)
   缺：additional computational effort; accuracy may be compromised by stale pricing and window dressing; may not be useful in projecting the future
4. Investment philosophy

Behavioral inefficiency : mispricing, 偏short-term，短期可消除

Structural inefficiency：law and regulation, 偏long-term，短期不会消除

1. SMA，separate management account 优缺点

优：

1. ownership : own the securities directly (which provides additional safety when liquidity event occur)
2. Tax efficiency: tax-loss 可作为其他资产的tax shield (mutual fund的loss不可以)
3. Customization: investor express their own individual constrains or preference
4. Transparency: real time, position-level detail

缺：

1. cost : additional cost
2. Tracking risk: customized strategy create tracking risk
3. Investor behavior: transparency combined with control and customization allow micromanagement by investor
4. Fee structure
5. Symmetrical
6. Bonus structure: not fully exposed to downside but fully to upside: max (base, base plus sharing of positive performance)
7. Not fully exposed to either upside or downside risk: base plus sharing of performance to a limit （设置limit可以防止manager为了分红而承担过多的风险）

More attractive compensation package advantage优点：

This incentive its investment professionals to stay in the company; leading to greater longevity and experience over time; additionally, increase the reward to its manager when performance exceed benchmark, this better align their interest with client. Motivate the manager to work harder to improve performance.

**Ethical and Professional Standards**

分为三部分

1. code & standards 针对个人，强制遵守（欢迎公司遵守）
2. AMC asset manager code of professional conduct: 其中有关于个人的部分与code & standards一致，是针对资产管理机构，可自愿选择是否遵守
3. GIPS global investment performance standards 针对公司，可自愿选择是否遵守

Reading 31 Code and ethics and standards of professional conduct

Reading 32 Guidance for standards I-VII

Reading 33 Application of the code and standards I-VII

七大条：

1、Professionalism：knowledge of the law/Independence and objectivity/Misrepresentation/Misconduct

2、Integrity of capital markets：material nonpublic information/Market manipulation

3、Duty to clients：loyalty, prudence and care/Fair dealing/Suitability/Performance presentation/Preservation of confidentiality

4、Duty to employers：Loyalty/Additional compensation arrangement/Responsibility of supervisors

5、Investment：diligence and reasonable basis/Communication with clients/Record retention

6、Conflicts of interest：disclosure of conflict/Priority of transaction/Referral fees

7、Responsibility as members：conduct as members and candidates/Reference to CFA institute, designation

Reading 34 Asset Manager Code of Professional Conduct

1. 要求：对个人要求与code and standards 一致；对公司有组织架构的规定
   如选择遵守AMC，则cover all employees and all laws and regulation
   如生成遵守AMC，则后面需要加一句：this claim has not been verified by CFA Institute
2. 公司可要求基金经理put their own capital alongside with client, 但仍需遵守在客户后面交易的要求，即虽然买一样的标的，但两笔资金并非放在一起
3. AMC要求risk management风控；compliance合规；support后台支持
4. qualified staff, sufficient human and technological resources
5. Business continuity plan: address disaster recovery ；关键员工死亡和离职的应对计划
6. Firm-wide risk management process

Plans for contacting and communicating with client during a period of extended disruption 如果持续中断需告知用户，如果短暂终端无需告知用户（但需要与员工和供应商vender沟通）

风控、合规均可外包给第三方

1. disclose management fee: gross and net-of-fee return, disclose any unusual expense
   这里的return均为已扣除transaction cost交易手续费，gross return未扣除管理费
   Determining all fixed and contingent fees and costs, and what will trigger these expense
   Retrospectively disclose to each client with itemization of such charges 费用的明细也需要disclose
   Prospective client the average or expected expense or fees 需要disclose预估数，不能光讲费用的比例
2. 业绩的报告最少要季度报告一次，季度末月后30天内需报告该季度业绩。不要求准备月度业绩以备用户查阅。
3. Valuation Method：依据Fair Value，这里面包含closing market value, third-party valuation, internal valuation model, or other method 均可

Reading 35 Overview of the Global Investment Performance Standard (GIPS)

1. 概述
2. Composite定义：把类似的风格、策略的portfolio加权平均在一起进行报告，报告业绩时以composite作为整体，但基金经理实际管理的依旧是portfolio
3. GIPS composite report( segregated account,client)和 GIPS pooled fund report（investor）
4. GIPS不强制要求对业绩报告进行verified，但被verified报告会增加可信度
5. 哪些公司可以遵守GIPS：distinct business entity, 而这个entity如何定义？要求manage asset on a discretionary basis，组织和功能上独立，拥有独立决策权即可宣布遵守GIPS
6. when GIPS standards conflict with law, could claim that comply with law and disclose in GIPS report 如果GIPS条款与当地法律冲突，只要披露该冲突，并遵守法律，此时并不视为违反GIPS
7. 管理账户分类
8. Total Firm Asset：including discretionary/non-discretionary/fee-paying, not include advisory-only asset or uncalled committed capital
9. All discretionary fee paying portfolio must be included in at least one composite
10. Non-fee-paying discretionary may be included in composite
11. Non-discretionary must not be included in composite
12. Discretionary and constraint, 如何理解账户是否属于discretionary，尤其是当IPS有constraint时，即看是否对决策有material effect，典型的几种constraints如下：

A, 仓位限制：依旧为discretionary

1. ESG要求：不一定，比如禁止投军工类企业这种就可能影响决策（比如军工类企业本身是大盘的重要组成部分）
2. Retain specific holding(例如 must not sell) : non-discretionary
3. Pattern of external cash flow: 比如每个月都要取钱，might non-discretionary

个人理解：有一些限制是可以在composite层面进行规定的，但类似于gain security can not be sold这种不可能在composite层面设置的条款则会影响是否discretionary

1. Return计算：
2. Portfolio return 计算方法：
3. 对外部现金流无掌握时：
4. large cash flow: TWRR (Time-weighted rate of return), 更精确
5. Non-large cash flow: Modified Dietz & Modified IRR

Modified IRR method, 当in/out cash flow没有那么大时，可得到类似结果，将一段时间的IRR分别计算出来，利用compound link在一起

（2）对外部现金流有掌握时has control over external cash flow：money-weighted return，例如PE，通过要求LP按时call down capital

2、Composite return 计算方法，基于TWRR的composite，有三种方法，其中第2、3方法计算结果一致：

（1）Asset-weighting : beginning of the period, 以beginning asset为权重计算value

（2）beginning value + external CF

（3）Aggregate return method: 把多个portfolio合并成一个，用modified Dietz方法计算，combine all composite asset and external cash flow

3、业绩报告规定：

（1）cash and cash equivalent held in portfolio must be included in total return calculation

（2）return must be calculated after deduction of transaction cost 

Transaction cost中包含brokerage commission, exchange fee, tax, bid-ask spread

custody fee托管费 should not be considered as transaction fee, 而是应该属于administrative fee

Gross-of-fee和net-of-fee都扣除了transaction cost, net-of-fee 又额外扣除了management fee

（3）bundle fee : 将所有费用打包计算（management fee, transaction fee, custody fee, administrative fee）,打包费中的交易费用不能预估，需要用发生的实际值

1. composite业绩报告: 
2. 把类似的portfolio 放在一起，那么如何定义类似的portfolio：investment mandate, objective, strategy相同，简单来说就是相同的投资策略
3. Composite must include all portfolio that meet the composite definition, require composite include new portfolio on a timely and consistent basis after the portfolio comes under management 符合要求的全部portfolio需要都包含在对应的composite中
4. Must include terminated portfolio in the history of performance of composite 中止后的composite也需要继续保存在历史业绩的展示中
   Through last full measurement period 中止的portfolio业绩需要保存最后一个报告周期（如果是季度则保存最后一个完整季度，注意这里业绩是不能年华（半年化），return less than one year must not be annualized）
   如2019年3月15日portfolio中止，在展示composite历史业绩时需要保留2018年及之前
5. History performance must remain with the original composite 由于策略改变，部分不符合新策略的portfolio需要移动到新的composite中，但这部分portfolio历史上已经产生的业绩需要仍旧保留在原composite中
6. Significant cash flow (注意与large cash flow 不同，这两个都是专有名词)：为防止cash drag对其他投资人不公平，可建立temporary new account，先建仓，待建仓完毕后再归并
   Significant cash flow: is a client-directed cash flow sufficiently large that it may temporarily prevent the firm from implementing the strategy 公司firm需要事前就对significant CF进行定义
   Large cash flow: an external cash flow of such size that may distort the return
7. Composite可规定minimum asset level: 公司可规定composite有对portfolio的最小资产规模，但不可以追溯must not be applied retroactively（即不可以通过设置最小资产规模将portfolio从过去的业绩中剔除）, 只能应用于未来
   If a portfolio fell below the minimum, it could be removed from the composite, its prior performance must remain in the composite。这里要注意的是，转移出去的资金不能进去miscellaneous (混杂的)composite，即公司不能有一个composite作为一个垃圾桶能够吸收不符合其他composite的资金。
8. Minimum years of performance: 公司在宣布遵守GIPS时最少需要公布5年的收益数据（年化），如果composite不满5年，可以公布自从创立以来的业绩，当公布的业绩满10年后，才可以将大于10年的之前历史业绩删除
9. Internal dispersion: 当composite中包含多个portfolio，因portfolio之间的业绩不同，如何报告portfolio之间业绩的dispersion：
10. high/low range 即最高-最低
11. Equal-weighted standard deviation
12. Asset-weighted standard deviation
13. 当大公司收购其他投资公司时，哪些情况下被收购公司的历史业绩可以被合并如大公司：
14. 原公司的decision maker也加入的新公司
15. 投资流程保持不变
16. 不能有中断工作的情况：no break in the track record
17. 如遵守GIPS的公司收购不遵守GIPS的公司，可给予1年的时间作为过渡期give one year ‘grace period’
18. 对业绩的第三方验证verification不强制执行，但当执行时需要对整个公司进行验证(可以抽样)，不可以针对单个的composite或pooled fund

当完成了对公司整体的verification后，可以对某一个composite进行examination