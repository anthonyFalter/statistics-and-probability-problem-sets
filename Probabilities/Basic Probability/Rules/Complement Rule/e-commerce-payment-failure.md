# Problem: E-Commerce Payment Failures (Complement Rule)

## 📌 Problem Overview

An e-commerce payment gateway logs transaction attempt outcomes. Historical logs indicate that any given checkout attempt has a **$4.5\%$** probability of failing due to network timeouts, insufficient funds, or bank rejections.

* **Probability of Failure ($P(F)$):** $0.045$ ($4.5\%$)
* **Objective:** Find the probability that a customer's transaction goes through successfully without failing ($P(F')$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule

Using the **Complement Rule**, the probability of an event not occurring is equal to $1$ minus the probability of the event occurring.

* **Formula:** $P(A') = 1 - P(A)$

---

### 🧮 Step 2: Compute the Probability

$$P(F') = 1 - P(F)$$
$$P(F') = 1 - 0.045 = 0.955 \quad (95.5\%)$$

---

### 📝 Step 3: Final Decision & Conclusion

* **Result:** The probability that a customer's checkout transaction is completed successfully is **$0.955$** or **$95.5\%$**.

</details>
