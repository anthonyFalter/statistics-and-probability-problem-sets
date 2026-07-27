# Problem: IT Bug Diagnostics (Addition Rule - Non-Mutually Exclusive)

## 📌 Problem Overview

In a software QA audit of a web application, engineers found that **$20\%$** of reported issues are UI rendering bugs ($U$), **$15\%$** are API latency issues ($A$), and **$5\%$** of reported issues involve **both** a UI rendering bug and an API latency issue ($U \cap A$).

* **Probability of UI Bug ($P(U)$):** $0.20$ ($20\%$)
* **Probability of API Issue ($P(A)$):** $0.15$ ($15\%$)
* **Probability of Both ($P(U \cap A)$):** $0.05$ ($5\%$)
* **Objective:** Find the probability that a randomly flagged ticket contains a UI bug **or** an API latency issue ($P(U \cup A)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule

Because a ticket can suffer from both issues simultaneously ($P(U \cap A) > 0$), these events are **not mutually exclusive**. We apply the **General Addition Rule**.

* **Formula:** $P(A \cup B) = P(A) + P(B) - P(A \cap B)$

---

### 🧮 Step 2: Compute the Probability

$$P(U \cup A) = P(U) + P(A) - P(U \cap A)$$
$$P(U \cup A) = 0.20 + 0.15 - 0.05 = 0.30 \quad (30\%)$$

---

### 📝 Step 3: Final Decision & Conclusion

* **Result:** The probability that a randomly chosen bug ticket involves either a UI rendering bug or an API latency issue (or both) is **$0.30$** or **$30\%$**.

</details>
