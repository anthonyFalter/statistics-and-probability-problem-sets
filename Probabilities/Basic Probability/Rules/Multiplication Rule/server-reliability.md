# Problem: Server Dual-Power Reliability (Multiplication Rule - Independent Events)

## 📌 Problem Overview

A mission-critical data center server relies on two independent power supplies: Power Unit A ($P_A$) and Power Unit B ($P_B$). The probability that Unit A remains operational during a power surge is **$98\%$**, while the probability that Unit B remains operational is **$95\%$**.

* **Probability Unit A Operates ($P(A)$):** $0.98$ ($98\%$)
* **Probability Unit B Operates ($P(B)$):** $0.95$ ($95\%$)
* **Objective:** Find the probability that **both** power units remain operational during a surge ($P(A \cap B)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule

Since the two power units function independently of each other, we apply the **Multiplication Rule for Independent Events**.

* **Formula:** $P(A \cap B) = P(A) \cdot P(B)$

---

### 🧮 Step 2: Compute the Probability

$$P(A \cap B) = P(A) \cdot P(B)$$
$$P(A \cap B) = 0.98 \times 0.95 = 0.931 \quad (93.1\%)$$

---

### 📝 Step 3: Final Decision & Conclusion

* **Result:** The probability that both power units withstand the surge and keep the server running is **$0.931$** or **$93.1\%$**.

</details>
