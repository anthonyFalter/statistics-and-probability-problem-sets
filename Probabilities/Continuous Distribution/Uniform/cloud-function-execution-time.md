# Problem: Cloud Function Execution Time (Continuous Uniform Distribution)

## 📌 Problem Overview

A serverless cloud function process takes anywhere between **10 seconds** and **30 seconds** to complete its task. The execution time is uniformly distributed across this continuous interval.

* **Lower Bound ($a$):** 10 seconds
* **Upper Bound ($b$):** 30 seconds
* **Objective:** Calculate the probability that a randomly triggered cloud function completes its execution in **less than 15 seconds** ($P(X < 15)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Distribution & Formula

Since the outcome is a continuous variable uniformly spread between a minimum $a$ and maximum $b$, it follows a **Continuous Uniform Distribution**: $X \sim U(10, 30)$.

* **Probability Density Function (PDF):** $f(x) = \frac{1}{b - a}$ for $a \le x \le b$
* **Cumulative Probability Formula:** $P(X \le x) = \frac{x - a}{b - a}$

---

### 🧮 Step 2: Compute the Probability

#### 1. Substitute Values into the CDF ($a = 10, b = 30, x = 15$)
$$P(X < 15) = \frac{15 - 10}{30 - 10}$$

#### 2. Evaluate
$$P(X < 15) = \frac{5}{20} = 0.25 \quad (25\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** The probability that the cloud function takes less than 15 seconds to execute is **0.25** or **25%**.

</details>
