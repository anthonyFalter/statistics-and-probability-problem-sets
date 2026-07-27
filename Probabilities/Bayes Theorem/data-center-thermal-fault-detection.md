# Problem: Data Center Thermal Fault Detection (Bayes' Theorem)

## 📌 Problem Overview

An automated monitoring tool flags server racks for critical overheating using thermal sensors. Historical infrastructure metrics report:

* **Overheating Base Rate ($P(O)$):** $2\%$ of servers experience overheating during peak load ($0.02$), meaning $98\%$ operate normally ($P(N) = 0.98$).
* **True Positive Rate ($P(A|O)$):** If a server is overheating, the alert triggers $95\%$ of the time ($0.95$).
* **False Positive Rate ($P(A|N)$):** If a server is operating normally, a false alert triggers $4\%$ of the time ($0.04$).

* **Objective:** If the thermal system issues an alert ($A$), calculate the actual probability that the server is **overheating** ($P(O|A)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Formula

By **Bayes' Theorem**, the updated probability of actual overheating given an alert is:

$$P(O|A) = \frac{P(A|O) \cdot P(O)}{P(A)}$$

Where total probability of an alert triggering $P(A)$ is:
$$P(A) = P(A|O) \cdot P(O) + P(A|N) \cdot P(N)$$

---

### 🧮 Step 2: Compute the Probabilities

#### 1. Compute Total Probability of an Alert $P(A)$
$$P(A) = (0.95 \times 0.02) + (0.04 \times 0.98)$$
$$P(A) = 0.019 + 0.0392 = 0.0582$$

#### 2. Apply Bayes' Formula
$$P(O|A) = \frac{0.019}{0.0582} \approx 0.3265 \quad (32.65\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** Even with a high-accuracy sensor, because true overheating is rare ($2\%$), there is only a **$32.65\%$** chance the server is actually overheating when an alert fires (a classic false-positive paradox).

</details>
