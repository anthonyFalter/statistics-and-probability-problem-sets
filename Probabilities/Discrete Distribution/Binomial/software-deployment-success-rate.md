# Problem: Software Deployment Success Rate (Binomial Distribution)

## 📌 Problem Overview

A DevOps engineer deploys **$10$** microservices to a staging cluster. Historically, each microservice deployment has an independent **$90\%$** chance of succeeding without build errors ($p = 0.90$).

* **Number of Trials ($n$):** $10\text{ microservices}$
* **Success Probability ($p$):** $0.90$
* **Failure Probability ($q = 1 - p$):** $0.10$
* **Objective:** Calculate the exact probability that **exactly $8$** microservices deploy successfully ($P(X = 8)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Distribution & Formula

Since there are a fixed number of independent trials with two possible outcomes (success/failure), this follows a **Binomial Distribution**: $X \sim \text{Binom}(n = 10, p = 0.90)$.

* **Formula:** $P(X = k) = \binom{n}{k} p^k (1 - p)^{n-k}$
* **Combinations Formula:** $\binom{n}{k} = \frac{n!}{k!(n-k)!}$

---

### 🧮 Step 2: Compute the Probability

#### 1. Calculate Combinations $\binom{10}{8}$
$$\binom{10}{8} = \frac{10!}{8! \cdot 2!} = \frac{10 \times 9}{2 \times 1} = 45$$

#### 2. Plug Values into PMF
$$P(X = 8) = 45 \cdot (0.90)^8 \cdot (0.10)^2$$
$$P(X = 8) = 45 \cdot (0.43046721) \cdot (0.01)$$
$$P(X = 8) = 45 \cdot 0.0043046721 \approx 0.1937 \quad (19.37\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** The probability that exactly $8$ out of $10$ microservices deploy successfully is approximately **$0.1937$** or **$19.37\%$**.

</details>
