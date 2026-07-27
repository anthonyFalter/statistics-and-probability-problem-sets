# Problem: Code Review Selection (Mutually Exclusive Events)

## 📌 Problem Overview

A senior developer is reviewing pull requests in a repository. The pull requests are categorized by language: **$40\%$** are written in C#, **$35\%$** in Java, and **$25\%$** in Python. A PR can only be written in a single primary language.

* **Probability of C# PR ($P(C)$):** $0.40$
* **Probability of Java PR ($P(J)$):** $0.35$
* **Probability of Python PR ($P(P)$):** $0.25$
* **Objective:** Find the probability that the next randomly selected PR is written in either **C# or Java** ($P(C \cup J)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule

Since a single PR cannot be written in C# and Java at the same time ($P(C \cap J) = 0$), these events are **mutually exclusive (disjoint)**. We apply the **Special Addition Rule**.

* **Formula:** $P(A \cup B) = P(A) + P(B)$

---

### 🧮 Step 2: Compute the Probability

$$P(C \cup J) = P(C) + P(J)$$
$$P(C \cup J) = 0.40 + 0.35 = 0.75 \quad (75\%)$$

---

### 📝 Step 3: Final Decision & Conclusion

* **Result:** The probability that the next PR reviewed is either C# or Java is **$0.75$** or **$75\%$**.

</details>
