# Chapter 5: Measuring Risk — Volatility, VaR, and Beyond

## 5.1 Introduction to Risk Measurement
Risk measurement in trading and investing is about quantifying uncertainty in returns. It helps traders assess potential losses and manage portfolios more effectively.

Key purposes:
- Compare investments on a risk-adjusted basis.
- Set position sizes and capital allocation.
- Comply with risk management regulations.

---

## 5.2 Volatility

### Definition
Volatility measures the degree of variation in returns over a specific period. It’s often used as a proxy for risk.

### Historical Volatility
- **Formula**:  
  \[
  \sigma = \sqrt{\frac{1}{N-1} \sum_{t=1}^{N} (r_t - \bar{r})^2}
  \]  
  Where \( r_t \) is the return at time \( t \), \( \bar{r} \) is the mean return, and \( N \) is the number of observations.
- Calculated using historical returns (daily, weekly, monthly).

### Annualized Volatility
To compare across assets:
\[
\sigma_{\text{annual}} = \sigma_{\text{daily}} \times \sqrt{252}
\]
(Assuming 252 trading days in a year.)

### Limitations
- Ignores direction of returns (upside vs downside volatility).
- Assumes past volatility predicts future volatility (often not true).

---

## 5.3 Value at Risk (VaR)

### Concept
Value at Risk estimates the maximum loss over a given time horizon at a certain confidence level.

Example:  
> "1-day 95% VaR of $1 million" means there’s a 5% chance of losing more than $1 million in one day.

### Methods to Calculate VaR
1. **Historical Method**  
   - Uses actual historical return distribution.
2. **Variance-Covariance Method**  
   - Assumes returns are normally distributed.
   - Formula:  
     \[
     \text{VaR} = Z_{\alpha} \times \sigma \times \sqrt{\Delta t}
     \]
3. **Monte Carlo Simulation**  
   - Generates hypothetical return paths to estimate loss distribution.

---

## 5.4 Conditional VaR (CVaR)

### Definition
Also called **Expected Shortfall**, CVaR is the average loss given that the loss has exceeded the VaR threshold.

Why it’s better:
- Considers the tail of the loss distribution.
- Provides more information about extreme risks.

---

## 5.5 Beta — Systematic Risk Measure

### Definition
Beta measures an asset’s sensitivity to market movements.

Formula:
\[
\beta = \frac{\text{Cov}(r_a, r_m)}{\text{Var}(r_m)}
\]
Where:
- \( r_a \) = asset return
- \( r_m \) = market return

Interpretation:
- β > 1: More volatile than the market.
- β < 1: Less volatile than the market.
- β < 0: Moves inversely to the market.

---

## 5.6 Sharpe Ratio

### Definition
Measures excess return per unit of risk.
\[
\text{Sharpe Ratio} = \frac{R_p - R_f}{\sigma_p}
\]
Where:
- \( R_p \) = portfolio return
- \( R_f \) = risk-free rate
- \( \sigma_p \) = portfolio volatility

Higher Sharpe = better risk-adjusted returns.

---

## 5.7 Sortino Ratio

### Definition
Similar to Sharpe but only considers downside volatility.
\[
\text{Sortino Ratio} = \frac{R_p - R_f}{\sigma_{\text{downside}}}
\]

---

## 5.8 Drawdowns

### Definition
A drawdown is the decline from a portfolio’s peak value to its lowest point before a new peak.

Formula:
\[
\text{Drawdown} = \frac{\text{Peak Value} - \text{Trough Value}}{\text{Peak Value}}
\]

---

## 5.9 Practical Considerations

- **Risk measures are estimates, not guarantees**.
- Use multiple metrics together for a comprehensive risk profile.
- Backtesting and stress testing help validate models.

---

## Summary Table

| Metric       | Measures                  | Best For                        | Limitation                    |
|--------------|---------------------------|----------------------------------|--------------------------------|
| Volatility   | Return variability        | General risk level               | No direction info              |
| VaR          | Max loss at confidence    | Regulatory reporting, limits     | Ignores tail beyond threshold  |
| CVaR         | Expected tail loss        | Extreme risk understanding       | Needs large data sets          |
| Beta         | Market sensitivity        | Market risk hedging              | Ignores idiosyncratic risk     |
| Sharpe       | Risk-adjusted returns     | Comparing investments            | Penalizes upside volatility    |
| Sortino      | Downside risk-adjusted    | Downside-sensitive strategies    | Requires downside data         |

---
