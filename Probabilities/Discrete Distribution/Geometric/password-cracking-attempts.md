# Problem: Password Cracking Attempts (Geometric Distribution)

## 📌 Problem Overview

A cybersecurity penetration tester executes a brute-force script against an authentication endpoint. Each attempt has a constant, independent **$5\%$** chance of discovering a valid password credential ($p = 0.05$).

* **Success Probability ($p$):** $0.05$
* **Failure Probability ($q = 1 - p$):** $0.95$
* **Objective:** Calculate the probability that the tester successfully cracks the password on **exactly their 4th attempt** ($P(X = 4)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Distribution & Formula

Since this scenario models the number of independent trials required until the **first success** occurs, it follows a **Geometric Distribution**: $X \sim \text{Geom}(p = 0.05)$.

* **Formula:** $P(X = k) = (1 - p)^{k-1} \cdot p$

---

### 🧮 Step 2: Compute the Probability

#### 1. Substitute Values into the Geometric PMF ($k = 4, p = 0.05$)
$$P(X = 4) = (1 - 0.05)^{4-1} \cdot (0.05)$$

#### 2. Evaluate Components
$$P(X = 4) = (0.95)^3 \cdot (0.05)$$
$$(0.95)^3 = 0.857375$$

#### 3. Calculate $P(X = 4)$
$$P(X = 4) = 0.857375 \cdot 0.05 = 0.04286875 \approx 0.0429 \quad (4.29\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** The probability that the script achieves its first successful authorization on exactly the 4th attempt is approximately **$0.0429$** or **$4.29\%$**.

</details>
