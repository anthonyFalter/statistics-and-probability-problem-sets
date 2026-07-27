# Problem: Database Connection Pooling Retries (Negative Binomial Distribution)

## 📌 Problem Overview

A microservice attempts to establish a connection to a database cluster during a network failover. Due to network jitter, each independent retry attempt has a **$40\%$** chance of successfully opening a connection ($p = 0.40$).

* **Target Successes ($r$):** $3\text{ successful connections}$
* **Success Probability ($p$):** $0.40$
* **Failure Probability ($q = 1 - p$):** $0.60$
* **Objective:** Calculate the probability that the microservice achieves its **3rd successful connection** on **exactly its 6th attempt** ($P(X = 6)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Distribution & Formula

Since this scenario models the number of trials ($k$) needed to achieve a specified number of successes ($r$), it follows a **Negative Binomial Distribution**: $X \sim \text{NegBinom}(r = 3, p = 0.40)$.

* **Formula:** $P(X = k) = \binom{k - 1}{r - 1} p^r (1 - p)^{k - r}$

---

### 🧮 Step 2: Compute the Probability

#### 1. Substitute Values into the PMF ($k = 6, r = 3, p = 0.40$)
$$P(X = 6) = \binom{6 - 1}{3 - 1} (0.40)^3 (0.60)^{6 - 3}$$
$$P(X = 6) = \binom{5}{2} (0.40)^3 (0.60)^3$$

#### 2. Evaluate Combinations $\binom{5}{2}$
$$\binom{5}{2} = \frac{5 \times 4}{2 \times 1} = 10$$

#### 3. Calculate $P(X = 6)$
$$P(X = 6) = 10 \cdot (0.064) \cdot (0.216)$$
$$P(X = 6) = 10 \cdot 0.013824 = 0.13824 \approx 0.1382 \quad (13.82\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** The probability that the microservice secures its 3rd active database connection on exactly the 6th attempt is approximately **$0.1382$** or **$13.82\%$**.

</details>
