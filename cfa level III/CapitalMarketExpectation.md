# Capital Market Expectation - CME

## Framework and Macro Considerations

### Economic Forecasting - Econometric Analysis

- Structural Model: based on economic theory 有理论
- Reduced-form: might be without theory, base on data and correlation 无理论支撑，数据之间的关系

#### Pros and Cons

Pros: 

1. Many factors, 
2. Quantative, 
3. Has a model, so can easily generate output, 
4. Discipline consistency

Cons: 

1. Complex and Time-consuming
2. Data input might be hard to forecast
3. Model is static, model might be mis-specified. Model is based on past data, so the model is static, cannot be updated while the market regime changed 因为模型基于过去数据，所以模型是static的，不能随市场情况更新
4. False sense of precision 模型model cannot forecast future well
5. Not forecast turning points 无法或者滞后的预测turning points

### Indicators

- Leading indicators. A composite of leading indicators is called a **diffusion index**
- Coincident 
- Lagging

#### Pros and Cons

Pros: 

1. Simple, 
2. Could **forecast turning points**
3. Easy to Track, good availability of indicator data

Cons:

1. Time lag滞后, revised指标可能修正, rebased基期变化
2. 单一指可能给出 false signals
3. 多个指标可能结果不一致，no binary guidance

### Checklist Approach 问卷调查

Pros:

1. Simple
2. Flexible 咋问都可以

Cons:

1. Subjective 主观
2. Time Consuming
3. Manual Process limits depth analysis
4. No consistency of analysis

### Challenges in Forecast

1. Limitations to using economic data
    - 数据 revised / rebased
2. Data measurement errors and biases
    - Transcription errors 抄错了
    -  Survivorship bias. The survivorship bias might overestimate returns 如PE知有表现好的时候才公布收益，所以 survivorship bias 高估 return
    - Appraisal data. The higher the frequency of data, the lower the correlation, because data become no smoothy. Lower the correlation, higher the risks 数据频率越高，corr越低，则 risk 越低。 Return smoother biases downward the risks
3. Limitations of historical estimates
    - Regime changes make data non-stationary. 由于 regime changes，造成 data non- stationary
    - Non-stationary make data statistically non-predictable.
    - Long time period & large dataset are preferable. Asynchronous data (high frequency data) underestimate correlation and underestimate risks.
4. Ex-post (将来) risk as a biased risk measure ex-ante (过去的) risk
    - 站在将来看过去 underestimate the risks and overestimate the potential returns
5. Biases in Analyst's Methods
    - Data-mining 相关性不代表因果关系
    - Time-period Bias 时间选太长会有 regime changes，太短 asynchronous data会导致 low corr， low risks
    - Avoid Bias: 
        1. data has economic basis, 数据有经济含义 ，避免相关性因果关系的问题
        2. Scrutinty 仔细检查 examine and inspect closely and thoroughly
        3. Test relationship with out-of-sample data 用样本外数据建议

### Economic Growth

#### Exogenous Shocks (unanticipated)

Factors cause the exogenous shocks

- Changes in Government Policy
- Political Events
- Technological progress
- Natural disasters
- Discovery of natural resources
- Financial crisis

#### Application

![Screenshot 2023-10-20 at 13.06.51](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-20%20at%2013.06.51.png)

$r_e = \frac{D_1}{P_0} + g_{equity}$

By Golden Growth Model: $P_0 = \frac{D_1}{r_e-g}$, we expand that into the whole equity market, that $r_e = \frac{D_1}{P_0} + g$

1. $\frac{D_1}{P_0}$

​	$\frac{D_1}{P_0} = \frac{D_1 / EPS}{P_0/EPS} = \frac{Div\ Payout\ Ratio}{P/E\ ratio}$

2. $g_{equity}$

- Normal GDP Growth

    Growth or Shocks might be reflected into stock price and bond price.

    Growth 大 => inflation 大 => tight monetary policy ( r 提升 => yield 提升 => bong price下降

    $P_1 = GDP_1 \times \frac{E_1}{GDP_1}\times \frac{P_1}{E_1}$

    - $P_1$: stock price 
    - $E_1$: earning
    - $P_1$: Price
    - $S_1$: (%) shares of Earning / GDP

    Price_1 = Total Economy * S_1 * 市盈率

    $\frac{P_1}{P_0} = \frac{GDP_1}{GDP_0} \times \frac{E_1/GDP_1}{E_0/GDP_0} \times \frac{P_1/E_1}{P_0 / E_0}$

    $ln(\frac{P_1}{P_0}) = ln(\frac{GDP_1}{GDP_0}) + ln( \frac{E_1/GDP_1}{E_0/GDP_0}) +  ln(\frac{P_1/E_1}{P_0 / E_0})$

    Stock price growth = GDP growth + S growth + P/E ratio Growth

    $g_{equity} = g_{gdp} + \Delta S\% + \Delta P/E \%$

    - Short-term 三项都变
    - Short-term 只有 growth of GDP 变, so $g_{equity} = g_{GDP}$

- Real GDP Growth $Y = \frac{Y}{L} \times L$

    Real GDP = GDP per Capita * Labour

    **L** 劳动力规模 has two drivers: **(1)** growth in potential labour force **size**, **(2)** labour force **participation**.

    **Y/L** productivity 劳动力效率 has two drives: **(1)** capital inputs **(2)** TFP total factor productivity

3. Thus, in the long term

    **Long-term:** $g_{equity} = g_{nominalGDP } = g_{real} + \pi$

    $g_{real GDP} = (1) + (2) + (3) + (4)$

    Short-term: $g_{equity} = g_{gdp} + \Delta S\% + \Delta P/E \%$

### Business Cycle

Reason of cyclical business activities 

- imperfect information to make decision
- reversing incorrect decision can be costly

#### Phase of Business Cycle



1. Initial Recovery
    - Confidence Rising
    - Expansionary Monetary & Fiscal Policy: low interest rate, Budget deficits
    - Falling Inflation
    - Negative Output Gap: Actual GDP < Potential GDP
    - 