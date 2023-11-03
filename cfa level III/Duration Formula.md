Duration Formula

$D_p$ duration, 利率变动 价格变多百分比

$DD_p = D_p \times V$ dollar duration, 利率变动，价格变动多少元

$D_p = w_1 D_1 + w_2 D_2$

$DD_p = DD_1 + DD_2$, coz $D_p = w_1 D_1 + w_2 D_2$ multiply $V_p$ from the both sides,

$D_pV_p = w_1 D_1 V_p + w_2 D_2 V_p$

$DD_p = V_1D_1 + V_2 D_2$, coz $V_1 = w_1 V_p$

$DD_p  = DD_1 + DD_2$

如何通过 swap 达到目标 Durations.

$D_{original} + \underbrace{D_{Swap}}_{InterestRateSwap} = D_{target}$ 

Solution: by Dollar Duration 能相加

$DD_{target} = DD_{original} + DD_{swap}$  expand it

$D_{target} V_{target} = D_{original}V_{target} + D_{swap} \times N_{swap}$ (Notional value of the Swap)

因为在签订 swap 时， swap value = 0, 所以 $V_{target} = V_{original} + V_{swap} = V_{target} + 0$ 

Finally, 所以

$D_{target} V_{target} = D_{original} V_{target} + D_{Swap} N_{swap}$

$N_s = \frac{D_t - D_p}{D_{swap}} \times V_p$

or 

$MV_p \times MDur_p + N_s \times MDur_s = MV_p \times MDur_t$ ($MV_t = MV_p$ ， 因为市场投资组合的价值 和加入swap的一样，swap在建立时value = 0)

$N_s = \frac{MDur_t - MDur_p}{MDur_s} MV_p$

- Implication:

  $D_t - D_p $ 与 $D_{swap}$ 同向变动

##### Interest Rate Forwards (FRA)

##### Interest Rate Future (Euro-Dollar Future)

- As it is future, it's standard (not OTC as FRA). 
- Guaranteed by a clearinghouse, so counterparty risk is nearly zero. 有保证金，所以交易对手方风险基本上为0
    - Cash settled

- P.S. interest rate futures are short-term, but fixed-income futures are more long time.

Euro Dollar Futures have fixed notional value and fixed term (, as it is standardised). 

- Notional value: 1 million USD
- Term: 3 months

$\$1,000,000 \times \frac{90}{360}\times 1bp = \$25$

---

### Fixed-Income Futures

Treasury-bond is the underlying asset, we do not use corporate bond as there is less liquidity and more credit risks.