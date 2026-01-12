# Background: Alpha and Beta

> In quantitative investing, Alpha (α) represents "excess returns" and Beta (β) represents "market benchmark returns." Understanding the relationship between these two is core to building hedging strategies and risk management.

---

## 1. Core Concept Definitions

### 1.1 Beta (β): Systematic Risk and Returns
**Beta** measures the volatility sensitivity of a portfolio relative to the market (benchmark). It reflects the portion of profit you receive from "market appreciation" and also reflects the structural risk you bear.

- **Formula**: $\beta_i = \frac{Cov(r_i, r_m)}{Var(r_m)}$
  - $r_i$: Asset return
  - $r_m$: Market benchmark return
- **Benchmark values**:
  - **β = 1**: Moves with the market (e.g., S&P 500 index fund)
  - **β > 1**: Aggressive (typically growth stocks, tech stocks)
  - **β < 1**: Defensive (typically utilities, consumer staples)
  - **β < 0**: Negative correlation (rare, e.g., inverse leveraged ETFs)
  - **β ≈ 0**: **Market Neutral**, returns don't fluctuate with the market.

### 1.2 Alpha (α): Excess Returns
**Alpha** is the pure profit after risk adjustment (excluding Beta's influence). It's viewed as the investment manager's "skill" or the model's "secret sauce."

- **Modern definition**: Returns that cannot be explained by known factors (such as market cap, value, momentum).
- **Current state**: As market efficiency improves, traditional Alpha is gradually decaying (Alpha Decay) and evolving into benchmark returns.

---

## 2. CAPM Model and Formula

The classic Capital Asset Pricing Model (CAPM) reveals the composition of returns:

$$E(R_i) = R_f + \beta_i (E(R_m) - R_f) + \alpha_i$$

- $R_f$: Risk-free rate
- $E(R_m) - R_f$: Market risk premium
- **Essence of Alpha**: The difference between actual return and CAPM-predicted return.

---

## 3. Evolution: From Alpha to Smart Beta

Modern quantitative investing further decomposes returns:

1. **Traditional Beta**: Pure market movement.
2. **Smart Beta (Factor Returns)**: Between α and β. Returns obtained through systematic exposure to certain factors (e.g., Size, Value, Momentum).
3. **Pure Alpha**: True excess skill (e.g., high-frequency arbitrage, alternative data mining, AI deep pattern recognition).

| Dimension | Beta (β) | Smart Beta | Alpha (α) |
| :--- | :--- | :--- | :--- |
| **Source of Returns** | Overall market performance | Factor exposure | Unique information/algorithms |
| **Cost** | Very low (index funds) | Relatively low | High (hedge funds) |
| **Scalability** | Very high | High | Limited |
| **Transparency** | Fully transparent | Rules are transparent | Black box/non-public |

---

## 4. US vs China Market Differences

| Characteristic | A-Share (China) Market | US Stock Market |
| :--- | :--- | :--- |
| **Alpha Environment** | **Alpha-rich**. Many retail investors, inefficient pricing. | **Beta-driven**. High institutionalization, Alpha hard to find. |
| **Difficulty** | Higher but relatively stable (high volatility). | Extremely high (highly efficient market). |
| **Neutral Strategies** | Effective but limited by hedging instrument costs. | Extremely rich tools, excellent liquidity. |

---

## 5. Python Implementation: Calculating Alpha and Beta

Using `statsmodels` for linear regression:

```python
import numpy as np
import pandas as pd
import statsmodels.api as sm

def calculate_alpha_beta(portfolio_returns, market_returns, rf_rate=0.02/252):
    """
    Calculate daily Alpha and Beta
    """
    # 1. Calculate excess returns
    y = portfolio_returns - rf_rate
    x = market_returns - rf_rate

    # 2. Linear regression: y = alpha + beta * x
    x = sm.add_constant(x)
    model = sm.OLS(y, x).fit()

    alpha = model.params[0]
    beta = model.params[1]

    return alpha, beta

# Example usage
# alpha_daily, beta = calculate_alpha_beta(returns_df['strategy'], returns_df['benchmark'])
# print(f"Daily Alpha: {alpha_daily:.4f}, Beta: {beta:.2f}")
```

---

## 6. What Top Quantitative Funds Pursue

- **Renaissance (Medallion Fund)**: Famous for **low Beta, extremely high Alpha**. Their logic is to find "statistical arbitrage" opportunities that don't move with the market.
- **Market Neutral Strategies**: By going long an Alpha portfolio while shorting a corresponding amount of index futures (Beta → zero), stable profits can be achieved regardless of whether the market goes up or down.

---

> **Summary**: For retail investors, focus on long-term growth from Beta; for quantitative researchers, the core task is mining **Alpha signals** with predictive power from raw data.
