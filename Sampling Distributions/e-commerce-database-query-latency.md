# Problem: E-Commerce Database Query Latency (Central Limit Theorem & Standard Error)

## 📌 Problem Overview

A backend database team tracks execution times for complex search queries on an e-commerce platform. The individual query durations are heavily skewed right due to occasional heavy joins, with a **population mean ($\mu$)** of **$250\text{ ms}$** and a **population standard deviation ($\sigma$)** of **$60\text{ ms}$**.

To assess system load, the monitoring system periodically logs random batches of **$144$ queries** ($n = 144$) and computes the **sample mean ($\bar{X}$)**.

* **Population Mean ($\mu$):** $250\text{ ms}$
* **Population Standard Deviation ($\sigma$):** $60\text{ ms}$
* **Sample Size ($n$):** $144$
* **Objective:** Calculate the **Standard Error of the Mean ($\sigma_{\bar{x}}$)** and determine the probability that a random batch sample mean **exceeds $258\text{ ms}$** ($P(\bar{X} > 258)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule & Formulas

By the **Central Limit Theorem (CLT)**, because the sample size is sufficiently large ($n = 144 \ge 30$), the sampling distribution of the sample mean $\bar{X}$ is approximately **Normally Distributed**, despite the skewness of the underlying population:

$$\bar{X} \sim N\left(\mu, \sigma_{\bar{x}}^2 = \frac{\sigma^2}{n}\right)$$

* **Standard Error of the Mean:** $\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}$
* **Z-Score for Sample Means:** $Z = \frac{\bar{X} - \mu}{\sigma_{\bar{x}}}$

---

### 🧮 Step 2: Compute the Standard Error ($\sigma_{\bar{x}}$)

$$\sigma_{\bar{x}} = \frac{60}{\sqrt{144}} = \frac{60}{12} = 5\text{ ms}$$

---

### 🧮 Step 3: Compute the Z-Score & Probability

#### 1. Calculate the Z-Score for $\bar{X} = 258$
$$Z = \frac{258 - 250}{5} = \frac{8}{5} = 1.60$$

#### 2. Find Upper-Tail Probability $P(Z > 1.60)$
Using the standard normal Z-table:
$$P(Z < 1.60) \approx 0.9452$$
$$P(Z > 1.60) = 1 - 0.9452 = 0.0548 \quad (5.48\%)$$

---

### 📝 Step 4: Final Conclusion

* **Standard Error ($\sigma_{\bar{x}}$):** **$5\text{ ms}$**
* **Result:** There is a **$0.0548$** (or **$5.48\%$**) probability that a sample batch of $144$ queries will have an average execution time greater than $258\text{ ms}$.

</details>
