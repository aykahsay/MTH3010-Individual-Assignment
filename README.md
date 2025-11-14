# Monte Carlo Option Pricing – README

This project implements Monte Carlo simulations to estimate **European call and put option prices** using the **Geometric Brownian Motion (GBM) model**.

---

## 1️⃣ Base Case Analysis

**Parameters:**

* Initial Stock Price (S₀): 100
* Strike Price (K): 105
* Risk-Free Rate (r): 5%
* Volatility (σ): 20%
* Time to Maturity (T): 1 year
* Number of Simulations (N): 10,000

**Results:**

| Metric               | Value   |
| -------------------- | ------- |
| Expected Stock Price | 105.336 |
| Standard Deviation   | 21.125  |
| Call Option Price    | 8.088   |
| Put Option Price     | 7.769   |

**Interpretation:**

* The **expected stock price** is slightly above the initial price, reflecting growth at the risk-free rate.
* The **standard deviation** measures the uncertainty in the stock price at maturity; moderate volatility produces a noticeable spread.
* The **call option** price is higher than the intrinsic value at-the-money due to potential upward movement in the stock.
* The **put option** price reflects the value of protection against downside risk.

**Plot Placeholder:**
`[Insert histogram of simulated stock prices for base case here]`

---

## 2️⃣ Volatility Impact Study

**Volatilities Tested:** 10%, 20%, 30%

**Observations:**

* **σ = 10%**: Stock prices tightly cluster around the expected value → options are cheaper.
* **σ = 20%**: Wider spread of stock prices → both call and put options gain value.
* **σ = 30%**: Large spread → highest option prices; extreme outcomes are more likely.

**Key Insight:** Increasing volatility **increases the spread of stock prices** and therefore **increases option values** due to higher probability of extreme outcomes.

**Plot Placeholder:**
`[Insert overlay histogram showing effect of volatility on stock price distribution here]`

---

## 3️⃣ Random Variable Z Analysis

**Concept:** Z ~ N(0,1) represents the **standard normal randomness** in stock price movement.

* **Financial Meaning:** Unpredictable market shocks or daily return fluctuations.
* **Importance:** Introduces stochasticity and uncertainty into stock price modeling.
* **Role in GBM:** Determines how each simulated stock path deviates from the deterministic trend.

**Plot Placeholder:**
`[Insert histogram of Z values overlaid with standard normal PDF here]`

---

## 4️⃣ Summary Table of Option Prices by Volatility

| Volatility (σ) | Expected Price | Std Dev | Call Price | Put Price |
| -------------- | -------------- | ------- | ---------- | --------- |
| 10%            | [value]        | [value] | [value]    | [value]   |
| 20%            | 105.336        | 21.125  | 8.088      | 7.769     |
| 30%            | [value]        | [value] | [value]    | [value]   |

**Interpretation:**

* As volatility increases, the **expected price stays around the deterministic growth**, but the **spread increases**, resulting in **higher call and put prices**.

**Plot Placeholder:**
`[Optional: Combined visualization of option values vs volatility]`

---

## ✅ Notes

* Monte Carlo simulation allows **visual and numerical understanding** of stock price uncertainty and option pricing.
* **Histograms** help interpret probabilities of stock price outcomes.
* **Overlaying volatility histograms** demonstrates the effect of risk on option valuation.

---
