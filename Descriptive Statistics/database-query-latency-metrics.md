# Problem: Database Query Response Latency Metrics (Mean, Variance & Standard Deviation)

## 📌 Problem Overview

A backend engineer measures the response latency (in milliseconds) of a SQL database query across **6 consecutive benchmark executions**:

$$\text{Latency (ms): } [42, 46, 50, 54, 58, 74]$$

* **Sample Size ($n$):** $6$
* **Objective:** Calculate the **sample mean ($\bar{x}$)**, **sample variance ($s^2$)**, and **sample standard deviation ($s$)** for this latency dataset.

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Formulas

For a sample dataset of size $n$:

* **Sample Mean:** $\bar{x} = \frac{\sum x_i}{n}$
* **Sample Variance:** $s^2 = \frac{\sum (x_i - \bar{x})^2}{n - 1}$
* **Sample Standard Deviation:** $s = \sqrt{s^2}$

---

### 🧮 Step 2: Compute the Sample Mean ($\bar{x}$)

$$\bar{x} = \frac{42 + 46 + 50 + 54 + 58 + 74}{6} = \frac{324}{6} = 54\text{ ms}$$

---

### 🧮 Step 3: Compute Squared Deviations & Variance ($s^2$)

Calculate $(x_i - \bar{x})^2$ for each observation:

| Observation ($x_i$) | Deviation ($x_i - 54$) | Squared Deviation $(x_i - 54)^2$ |
| :--- | :--- | :--- |
| $42$ | $-12$ | $144$ |
| $46$ | $-8$ | $64$ |
| $50$ | $-4$ | $16$ |
| $54$ | $0$ | $0$ |
| $58$ | $4$ | $16$ |
| $74$ | $20$ | $400$ |
| **Sum ($\sum$)** | **$0$** | **$640$** |

Substitute into the sample variance formula ($n - 1 = 5$):

$$s^2 = \frac{640}{6 - 1} = \frac{640}{5} = 128\text{ ms}^2$$

---

### 🧮 Step 4: Compute Standard Deviation ($s$)

$$s = \sqrt{128} \approx 11.314\text{ ms}$$

---

### 📝 Step 5: Final Conclusion

* **Sample Mean ($\bar{x}$):** $54\text{ ms}$
* **Sample Variance ($s^2$):** $128\text{ ms}^2$
* **Sample Standard Deviation ($s$):** $\approx 11.314\text{ ms}$

</details>
