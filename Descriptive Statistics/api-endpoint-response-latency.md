# Problem: Microservice API Endpoint Response Latency Metrics

## 📌 Problem Overview

A DevOps engineer tracks the processing time (in milliseconds) of a critical user authentication API endpoint across **5 consecutive load test runs**:

$$\text{Latency (ms): } [12, 18, 20, 22, 28]$$

* **Sample Size ($n$):** $5$
* **Objective:** Compute the **sample mean ($\bar{x}$)**, **sample variance ($s^2$)**, and **sample standard deviation ($s$)** for this performance dataset.

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Formulas

For a sample dataset of size $n$:

* **Sample Mean:** 
  $$\bar{x} = \frac{\sum x_i}{n}$$

* **Sample Variance:** 
  $$s^2 = \frac{\sum (x_i - \bar{x})^2}{n - 1}$$

* **Sample Standard Deviation:** 
  $$s = \sqrt{s^2}$$

---

### 🧮 Step 2: Compute the Sample Mean ($\bar{x}$)

$$\bar{x} = \frac{12 + 18 + 20 + 22 + 28}{5} = \frac{100}{5} = 20\text{ ms}$$

---

### 🧮 Step 3: Compute Squared Deviations & Variance ($s^2$)

Calculate $(x_i - \bar{x})^2$ for each observation:

| Observation ($x_i$) | Deviation ($x_i - 20$) | Squared Deviation $(x_i - 20)^2$ |
| :--- | :--- | :--- |
| $12$ | $-8$ | $64$ |
| $18$ | $-2$ | $4$ |
| $20$ | $0$ | $0$ |
| $22$ | $2$ | $4$ |
| $28$ | $8$ | $64$ |
| **Sum ($\sum$)** | **$0$** | **$136$** |

Substitute into the sample variance formula ($n - 1 = 4$):

$$s^2 = \frac{136}{5 - 1} = \frac{136}{4} = 34\text{ ms}^2$$

---

### 🧮 Step 4: Compute Standard Deviation ($s$)

$$s = \sqrt{34} \approx 5.831\text{ ms}$$

---

### 📝 Step 5: Final Conclusion

* **Sample Mean ($\bar{x}$):** $20\text{ ms}$
* **Sample Variance ($s^2$):** $34\text{ ms}^2$
* **Sample Standard Deviation ($s$):** $\approx 5.831\text{ ms}$

</details>
