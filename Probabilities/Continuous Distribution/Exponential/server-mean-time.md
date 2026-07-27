# Problem: Server Mean Time Between Failures (Exponential Distribution)

## 📌 Problem Overview

The time until a high-performance database server experiences a hardware failure follows an **Exponential Distribution**. On average, the server experiences **$0.2$ failures per year** ($\lambda = 0.2$), corresponding to a Mean Time Between Failures (MTBF) of $5$ years ($\mu = 1 / \lambda = 5$).

* **Failure Rate ($\lambda$):** $0.2\text{ failures/year}$
* **Time Horizon ($x$):** $3\text{ years}$
* **Objective:** Calculate the probability that the server fails **within the next 3 years** ($P(X \le 3)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Distribution & Formula

The exponential distribution models continuous time until a Poisson process event occurs: $X \sim \text{Exp}(\lambda = 0.2)$.

* **Probability Density Function (PDF):** $f(x) = \lambda e^{-\lambda x}$ for $x \ge 0$
* **Cumulative Distribution Function (CDF):** $P(X \le x) = 1 - e^{-\lambda x}$

---

### 🧮 Step 2: Compute the Probability

#### 1. Substitute Values into the CDF ($\lambda = 0.2, x = 3$)
$$P(X \le 3) = 1 - e^{-(0.2)(3)}$$
$$P(X \le 3) = 1 - e^{-0.6}$$

#### 2. Evaluate the Exponential Term
* $e^{-0.6} \approx 0.5488$

#### 3. Calculate Final Probability
$$P(X \le 3) = 1 - 0.5488 = 0.4512 \quad (45.12\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** The probability that the database server suffers a hardware failure within 3 years is approximately **$0.4512$** or **$45.12\%$**.

</details>
