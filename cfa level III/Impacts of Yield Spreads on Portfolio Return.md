#### Impacts of Yield Spreads on Portfolio Return

Refer to the basic rate

$\Delta P = - D\Delta y + \frac{1}{2}Convexity (\Delta y)^2$

Similarly for Spread

$\%\Delta P = - Spread.D \times \Delta Spread + \frac{1}{2}\times S.Conv \times (\Delta S)^2$

However, **for lower-rated bond**, it is the **percentage of spread change** $\frac{\Delta Spread}{Spread}$would have impact on the price, not absolute basis.对于低评级bond，对价格有影响的是 spread 变动的百分比，而不 spread 变动的数值 

- Duration Times Spread (DTS) = $Eff.Spread.Duration \times Spread$
    - 因为 是percentage of spread对price 有影响， 所以为$\frac{\Delta Spread}{Spread}\times (\underbrace{D\times Spread}_{DTS})$

#### Excess Spread Return

$\mathbb{E}(R) = \underbrace{Coupon + Reinvest}_{YTM} + \underbrace{\Delta p}_{-D\times\Delta Y} - CreditLoss $, ignore the foreign G/L for this equation.

Similarly, see the underbrace, and we get the following eq

$ExcessReturn = Spread + (-SD\times \Delta S) - LGD \times PoD$

### Credit Strategy

#### Bottom-up Credit Strategy

- Relative Value Analysis

    1. Financial Statement analysis, (1) comparability (2) historical data

    2. Two model

        1. Reduced form model, (1) forward not historical (2) use macro and idiosyncratic data
        2. Structural Credit Model, forward looking PoD

    3. Credit Spread => Excess Return

        $\mathbb{E}(Excess S)=S - S.D.\times \Delta S -PoD\times LGD$

    P.S. Consider (1) other features such as options (2) cost of trading

#### Top-Down Credit Strategy

Choose Sector, broader sector 大类

1. Asscess credit quality
2. Sector allocation

#### Factor-Based Credit Strategy