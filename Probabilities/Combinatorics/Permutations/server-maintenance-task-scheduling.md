# Problem: Server Maintenance Task Scheduling (Permutations)

## 📌 Problem Overview

A system administrator needs to execute **$6$ distinct, sequential system update scripts** ($A, B, C, D, E, F$) during a scheduled maintenance window. The order in which these scripts run strictly matters, and no script can be executed more than once.

* **Total Tasks ($n$):** $6$
* **Tasks Selected ($k$):** $6$
* **Objective:** Calculate the total number of unique execution sequences possible for running all $6$ scripts.

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule

Since we are arranging **all** distinct items where order matters, we use the **Permutation Rule** for $n$ items.

* **Formula:** $P(n, k) = \frac{n!}{(n - k)!}$
* **For $n = k$:** $P(n) = n!$

---

### 🧮 Step 2: Compute the Permutations

$$P(6) = 6!$$
$$P(6) = 6 \times 5 \times 4 \times 3 \times 2 \times 1 = 720$$

---

### 📝 Step 3: Final Conclusion

* **Result:** There are **$720$** unique ordered sequences in which the system administrator can execute the $6$ maintenance scripts.

</details>
