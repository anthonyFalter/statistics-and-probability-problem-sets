# Problem: Server Throughput Estimation (95% Confidence Interval)

## 📌 Problem Overview

A network engineering team wants to estimate the true average throughput (in Requests Per Second, RPS) of a load-balanced cluster. They collect **$36$ random performance snapshots** ($n = 36$) during peak business hours.

* **Sample Size ($n$):** $36$
* **Sample Mean ($\bar{x}$):** $1,250\text{ RPS}$
* **Known Population Standard Deviation ($\sigma$):** $120\text{ RPS}$
* **Confidence Level:** $95\%$
* **Objective:** Construct a **$95\%$ Confidence Interval** for the true population mean throughput ($\mu$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Formula

When the population standard deviation ($\sigma$) is known and the sample size is large ($n \ge 30$), we use the **Z-Confidence Interval** formula:

$$\text{CI} = \bar{x} \pm Z_{\alpha/2} \cdot \left(\frac{\sigma}{\sqrt{n}}\right)$$

* **Margin of Error (ME):** $\text{ME} = Z_{\alpha/2} \cdot \left(\frac{\sigma}{\sqrt{n}}\right)$
* For a **$95\%$ Confidence Level** ($\alpha = 0.05$), the critical value $Z_{0.025} = 1.96$.

---

### 🧮 Step 2: Compute the Standard Error & Margin of Error

#### 1. Calculate Standard Error ($\sigma_{\bar{x}}$)
$$\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}} = \frac{120}{\sqrt{36}} = \frac{120}{6} = 20\text{ RPS}$$

#### 2. Calculate Margin of Error ($\text{ME}$)
$$\text{ME} = 1.96 \times 20 = 39.2\text{ RPS}$$

---

### 🧮 Step 3: Calculate Confidence Interval Bounds

* **Lower Bound:** $1,250 - 39.2 = 1,210.8\text{ RPS}$
* **Upper Bound:** $1,250 + 39.2 = 1,289.2\text{ RPS}$

$$\text{CI} = [1,210.8, \, 1,289.2]$$

---

### 📝 Step 4: Final Conclusion

* **Result:** We are **$95\%$ confident** that the true average throughput of the load-balanced cluster lies between **$1,210.8\text{ RPS}$** and **$1,289.2\text{ RPS}$**.

</details>
