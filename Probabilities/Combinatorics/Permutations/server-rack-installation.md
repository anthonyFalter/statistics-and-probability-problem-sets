# Problem: Server Rack Hardware Installation (Permutations - Subsets)

## 📌 Problem Overview

A datacenter technician has **$8$ distinct rack server models** available, but only **$3$ empty rack slots** remaining in a server enclosure. Since cable routing and power distribution depend on which server goes into which specific slot position, the assignment order matters.

* **Total Server Models ($n$):** $8$
* **Slots to Fill ($k$):** $3$
* **Objective:** Calculate the total number of unique ways to select and arrange $3$ servers in the $3$ available rack slots.

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule

Since we are selecting $k$ items from $n$ distinct items where the order of placement matters, we use the **Permutation Formula**.

* **Formula:** $P(n, k) = \frac{n!}{(n - k)!}$

---

### 🧮 Step 2: Compute the Permutations

$$P(8, 3) = \frac{8!}{(8 - 3)!} = \frac{8!}{5!}$$

$$\frac{8 \times 7 \times 6 \times 5!}{5!} = 8 \times 7 \times 6 = 336$$

---

### 📝 Step 3: Final Conclusion

* **Result:** There are **$336$** unique ways to select and arrange $3$ servers in the available rack slots.

</details>
