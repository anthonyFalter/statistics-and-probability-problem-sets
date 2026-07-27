# Problem: System Memory Utilization Metrics (Mean, Variance & Standard Deviation)

## 📌 Problem Overview

A DevOps engineer samples the peak RAM usage (in Gigabytes) of a web server microservice across **5 consecutive load test runs**:

$$\text{RAM Usage (GB): } [12, 14, 16, 18, 20]$$

* **Sample Size ($n$):** $5$
* **Objective:** Calculate the **sample mean ($\bar{x}$)**, **sample variance ($s^2$)**, and **sample standard deviation ($s$)** for this memory dataset.

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

$$\bar{x} = \frac{12 + 14 + 16 + 18 + 20}{5} = \frac{80}{5} = 16\text{ GB}$$

---

### 🧮 Step 3: Compute Squared Deviations & Variance ($s^2$)

Calculate $(x_i - \bar{x})^2$ for each observation:

| Observation ($x_i$) | Deviation ($x_i - 16$) | Squared Deviation $(x_i - 16)^2$ |
| :--- | :--- | :--- |
| $12$ | $-4$ | $16$ |
| $14$ | $-2$ | $4$ |
| $16$ | $0$ | $0$ |
| $18$ | $2$ | $4$ |
| $20$ | $4$ | $16$ |
| **Sum ($\sum$)** | **$0$** | **$40$** |

Substitute into the sample variance formula ($n - 1 = 4$):

$$s^2 = \frac{40}{5 - 1} = \frac{40}{4} = 10\text{ GB}^2$$

---

### 🧮 Step 4: Compute Standard Deviation ($s$)

$$s = \sqrt{10} \approx 3.162\text{ GB}$$

---

### 📝 Step 5: Final Conclusion

* **Sample Mean ($\bar{x}$):** $16\text{ GB}$
* **Sample Variance ($s^2$):** $10\text{ GB}^2$
* **Sample Standard Deviation ($s$):** $\approx 3.162\text{ GB}$

</details>
