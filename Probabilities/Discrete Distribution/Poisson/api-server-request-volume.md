# Problem: API Server Request Volume (Poisson Distribution)

## 📌 Problem Overview

A web server receives an average rate of **$4$ API requests per second** during peak traffic hours. Assuming request arrivals are independent and occur at a constant average rate, the team wants to estimate traffic spikes.

* **Average Rate ($\lambda$):** $4\text{ requests/sec}$
* **Objective:** Calculate the probability that the server receives **exactly $6$ API requests** in a given one-second interval ($P(X = 6)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Distribution & Formula

Since this scenario models the number of events occurring within a fixed time interval at a known average rate, it follows a **Poisson Distribution**: $X \sim \text{Poisson}(\lambda = 4)$.

* **Formula:** $P(X = k) = \frac{\lambda^k \cdot e^{-\lambda}}{k!}$
* **Constants:** $e \approx 2.71828$

---

### 🧮 Step 2: Compute the Probability

#### 1. Substitute Values into the Poisson PMF ($k = 6, \lambda = 4$)
$$P(X = 6) = \frac{4^6 \cdot e^{-4}}{6!}$$

#### 2. Evaluate Components
* $4^6 = 4096$
* $e^{-4} \approx 0.0183156$
* $6! = 720$

#### 3. Calculate $P(X = 6)$
$$P(X = 6) = \frac{4096 \cdot 0.0183156}{720} = \frac{75.0207}{720} \approx 0.1042 \quad (10.42\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** The probability that the server receives exactly $6$ requests in a one-second interval is approximately **$0.1042$** or **$10.42\%$**.

</details>
