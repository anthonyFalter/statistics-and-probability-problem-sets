# Problem: Microservice Response Time SLA (Normal Distribution - Range Probability)

## 📌 Problem Overview

An API gateway monitors the response times of a critical microservice. The latency follows a **Normal Distribution** with a mean response time of **$120\text{ ms}$** and a standard deviation of **$15\text{ ms}$**.

* **Mean ($\mu$):** $120\text{ ms}$
* **Standard Deviation ($\sigma$):** $15\text{ ms}$
* **Acceptable SLA Range:** Between $100\text{ ms}$ and $135\text{ ms}$
* **Objective:** Calculate the probability that a randomly sampled API request completes within the acceptable SLA range ($P(100 \le X \le 135)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Distribution & Standard Score Formula

Since latency follows $X \sim N(\mu = 120, \sigma^2 = 225)$, we convert both boundary values ($X_1 = 100$ and $X_2 = 135$) into standard Z-scores ($Z \sim N(0, 1)$).

* **Z-Score Formula:** $Z = \frac{X - \mu}{\sigma}$
* **Interval Probability Formula:** $P(a \le X \le b) = P(Z_b) - P(Z_a)$

---

### 🧮 Step 2: Compute Z-Scores and Probabilities

#### 1. Calculate Z-Score for Lower Bound ($X_1 = 100$)
$$Z_1 = \frac{100 - 120}{15} = \frac{-20}{15} \approx -1.33$$

#### 2. Calculate Z-Score for Upper Bound ($X_2 = 135$)
$$Z_2 = \frac{135 - 120}{15} = \frac{15}{15} = 1.00$$

#### 3. Find Cumulative Probabilities from standard Z-table
* $P(Z \le -1.33) \approx 0.0918$
* $P(Z \le 1.00) \approx 0.8413$

#### 4. Calculate Interval Probability
$$P(100 \le X \le 135) = P(Z \le 1.00) - P(Z \le -1.33)$$
$$P(100 \le X \le 135) = 0.8413 - 0.0918 = 0.7495 \quad (74.95\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** The probability that a request falls within the acceptable SLA bounds of 100 ms to 135 ms is **$0.7495$** or **$74.95\%$**.

</details>
