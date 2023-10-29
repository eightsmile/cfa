# Derivatives & Exchange

## Derivatives 

### Covered Call Strategy (long Stock, short Call)

i.e.  $S=2000$

- **Yield Enhancement** 为长期持有, $K = 3000$

  write a OTM call option.

- **Reduce a Position** 为了卖, $K=1800$

- **Target Price Realisation** 近期到期 combine of above two $K=2500$

As the coverd call strategy is (long S, short Call)

$Profit = \underbrace{(S_T - S_0)}_{long \ S} + \underbrace{ C - \max(S_T-K,0)}_{Long\ Call}$

- if $S_T > K$, then, $Profit = K - S_0 + C$     (行权)
- if $S_T \leq K$, then, $Profit = S_T -S_0 + C$      (不行权)
- if Break-even,  $S_T - S_0 + C =0$
- if max loss, $S_T = 0$, $Loss (Profit) = -S_0 + C$
- if max gain, $S_T > X$, $Gain (Profit) = K - S_0 + C$

![ ](https://cdn.jsdelivr.net/gh/eightsmile/ImageLib@main/Screenshot%202023-10-29%20at%2021.11.26.png)

### Protected Put (long Stock, long Put)