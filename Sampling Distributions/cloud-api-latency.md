# Problem: Cloud API Latency Sampling (Central Limit Theorem & Standard Error)

## 📌 Problem Overview

An infrastructure team monitors response times for an API endpoint. Across millions of daily transactions, the individual request latency is heavily skewed, with a **population mean ($\mu$)** of **$180\text{ ms}$** and a **population standard deviation ($\sigma$)** of **$40\text{ ms}$**.

To monitor stability, the team automatically samples batches of **$100$ requests** ($n = 100$) every minute and calculates the **sample mean ($\bar{X}$)**.

* **Population Mean ($\mu$):** $180\text{ ms}$
* **Population Standard Deviation ($\sigma$):** $40\text{ ms}$
* **Sample Size ($n$):** $100$
* **Objective:** Calculate the **Standard Error of the Mean ($\sigma_{\bar{x}}$)** and find the probability that a random batch sample mean is **less than $174\text{ ms}$** ($P(\bar{X} < 174)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule & Formulas

By the **Central Limit Theorem (CLT)**, because the sample size is sufficiently large ($n = 100 \ge 30$), the sampling distribution of the sample mean $\bar{X}$ is approximately **Normally Distributed**, even though the underlying population is skewed:

$$\bar{X} \sim N\left(\mu, \sigma_{\bar{x}}^2 = \frac{\sigma^2}{n}\right)$$

* **Standard Error of the Mean:** $\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}$
* **Z-Score for Sample Means:** $Z = \frac{\bar{X} - \mu}{\sigma_{\bar{x}}}$

---

### 🧮 Step 2: Compute the Standard Error ($\sigma_{\bar{x}}$)

$$\sigma_{\bar{x}} = \frac{40}{\sqrt{100}} = \frac{40}{10} = 4\text{ ms}$$

---

### 🧮 Step 3: Compute the Z-Score & Probability

#### 1. Calculate the Z-Score for $\bar{X} = 174$
$$Z = \frac{174 - 180}{4} = \frac{-6}{4} = -1.50$$

#### 2. Find Cumulative Probability $P(Z < -1.50)$
Using the standard normal Z-table:
$$P(Z < -1.50) \approx 0.0668 \quad (6.68\%)$$

---

### 📝 Step 4: Final Conclusion

* **Standard Error ($\sigma_{\bar{x}}$):** **$4\text{ ms}$**
* **Result:** There is a **$0.0668$** (or **$6.68\%$**) probability that a sample batch of $100$ requests will average less than $174\text{ ms}$.

</details>
