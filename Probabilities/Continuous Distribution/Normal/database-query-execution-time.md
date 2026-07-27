# Problem: Database Query Execution Time (Empirical Rule)

## 📌 Problem Overview

A database administrator monitors complex analytical query runtimes. The execution times follow a symmetric, bell-shaped **Normal Distribution** with a mean query time of **$200\text{ ms}$** and a standard deviation of **$25\text{ ms}$**.

* **Mean ($\mu$):** $200\text{ ms}$
* **Standard Deviation ($\sigma$):** $25\text{ ms}$
* **Target Interval:** Between $150\text{ ms}$ and $250\text{ ms}$
* **Objective:** Use the **Empirical Rule (68–95–99.7 Rule)** to estimate the percentage of queries that execute within this interval ($P(150 \le X \le 250)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule

For any normally distributed dataset, the **Empirical Rule** states:
* Approximately **$68\%$** of observations fall within $\mu \pm 1\sigma$
* Approximately **$95\%$** of observations fall within $\mu \pm 2\sigma$
* Approximately **$99.7\%$** of observations fall within $\mu \pm 3\sigma$

---

### 🧮 Step 2: Determine Standard Deviations from the Mean

#### 1. Calculate Boundary Multiples
* **Lower Bound ($150\text{ ms}$):**
  $$\mu - k\sigma = 200 - k(25) = 150 \implies 25k = 50 \implies k = 2$$
  *(150 ms lies $2$ standard deviations below the mean)*

* **Upper Bound ($250\text{ ms}$):**
  $$\mu + k\sigma = 200 + k(25) = 250 \implies 25k = 50 \implies k = 2$$
  *(250 ms lies $2$ standard deviations above the mean)*

#### 2. Apply the Empirical Rule
Since the interval $[150, 250]$ corresponds strictly to $\mu \pm 2\sigma$:
$$P(150 \le X \le 250) \approx 95\% \quad (0.95)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** Approximately **$95\%$** (or $0.95$) of all analytical queries will complete within $150\text{ ms}$ to $250\text{ ms}$.

</details>
