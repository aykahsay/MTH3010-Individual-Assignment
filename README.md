# Monte Carlo Option Pricing

This project implements Monte Carlo simulations to estimate **European call and put option prices** using the **Geometric Brownian Motion (GBM) model**.
Monte Carlo simulation allows visual and numerical understanding of stock price uncertainty and option pricing.
Histograms help interpret probabilities of stock price outcomes.
Overlaying volatility histograms demonstrates the effect of risk on option valuation.

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

**Histogram:**

<img width="695" height="470" alt="image" src="https://github.com/user-attachments/assets/0da3638a-e491-4c26-8b8a-3fde95d50090" />

---

## 2️⃣ Volatility Impact Study

**Volatilities Tested:** 10%, 20%, 30%

**Observations:**

* **σ = 10%**: Stock prices tightly cluster around the expected value → options are cheaper.
* **σ = 20%**: Wider spread of stock prices → both call and put options gain value.
* **σ = 30%**: Large spread → highest option prices; extreme outcomes are more likely.

**Key Insight:** Increasing volatility **increases the spread of stock prices** and therefore **increases option values** due to higher probability of extreme outcomes.

**Hitogram Plot:Effect of Volatility on Stock price Distrubtion**
<img width="850" height="547" alt="image" src="https://github.com/user-attachments/assets/8877b29d-3ac1-466b-8c1d-be26b92d45ed" />


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

| Volatility (σ) | Expected Stock Price | Standard Deviation | Call Option Price | Put Option Price |
| -------------- | -------------------- | ------------------ | ----------------- | ---------------- |
| 10%            | 105.0036             | 10.5757            | 3.9926            | 3.9892           |
| 20%            | 105.0766             | 20.9286            | 7.8912            | 7.8184           |
| 30%            | 105.4187             | 32.4544            | 12.1990           | 11.8007          |

**Interpretation:**

As volatility increases, the expected stock price remains roughly the same (~105), which aligns with the risk-free growth.

The standard deviation increases significantly with higher volatility, indicating greater uncertainty in the stock price at maturity.

Both call and put option prices increase with volatility because higher volatility increases the probability of extreme outcomes, enhancing option value.
**Plot Placeholder:**

---

