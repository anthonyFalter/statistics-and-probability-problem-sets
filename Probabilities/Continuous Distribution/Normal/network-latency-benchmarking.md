# Problem: Network Latency Benchmarking (Normal Distribution & Z-Scores)

## 📌 Problem Overview

Network latency for requests sent to a regional datacenter follows a **Normal Distribution** with a mean latency of **$50\text{ ms}$** and a standard deviation of **$8\text{ ms}$**.

* **Mean ($\mu$):** $50\text{ ms}$
* **Standard Deviation ($\sigma$):** $8\text{ ms}$
* **Target Latency ($X$):** $66\text{ ms}$
* **Objective:** Calculate the probability that a randomly chosen request experiences a latency **greater than $66\text{ ms}$** ($P(X > 66)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Distribution & Standard Score Formula

Since the variable is normally distributed, $X \sim N(\mu = 50, \sigma^2 = 64)$, we standardize $X$ to the standard normal distribution $Z \sim N(0, 1)$ using the Z-score formula.

* **Z-Score Formula:** $Z = \frac{X - \mu}{\sigma}$

---

### 🧮 Step 2: Compute the Z-Score and Probability

#### 1. Calculate the Z-Score for $X = 66$
$$Z = \frac{66 - 50}{8} = \frac{16}{8} = 2.0$$

#### 2. Find Cumulative Probability $P(Z \le 2.0)$
Using the standard normal table (Z-table):
$$P(Z \le 2.0) = 0.9772$$

#### 3. Calculate Upper Tail Probability $P(Z > 2.0)$
$$P(X > 66) = P(Z > 2.0) = 1 - P(Z \le 2.0)$$
$$P(X > 66) = 1 - 0.9772 = 0.0228 \quad (2.28\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** The probability that a network request suffers a high latency exceeding $66\text{ ms}$ is **$0.0228$** or **$2.28\%$**.

</details>
