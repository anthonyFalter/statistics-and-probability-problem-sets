# Problem: Server Configuration Options (Fundamental Counting Principle)

## 📌 Problem Overview

A cloud deployment pipeline allows users to customize a virtual machine instance by choosing options across **4 independent setup categories**:

* **Processor Core Count:** 2, 4, 8, or 16 cores (4 options)
* **RAM Configuration:** 8 GB, 16 GB, or 32 GB (3 options)
* **Storage Type:** HDD, SSD, or NVMe (3 options)
* **Operating System:** Ubuntu, Debian, CentOS, or Windows (4 options)

* **Objective:** Determine the total number of unique virtual machine configurations available to deploy.

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule

By the **Fundamental Counting Principle**, if a sequence of choices consists of $n_1, n_2, \dots, n_k$ independent choices, the total number of possible outcomes is the product of the number of choices for each step.

* **Formula:** $N = n_1 \times n_2 \times n_3 \times \dots \times n_k$

---

### 🧮 Step 2: Compute the Total Outcomes

* $n_1 = 4$ (Processor options)
* $n_2 = 3$ (RAM options)
* $n_3 = 3$ (Storage options)
* $n_4 = 4$ (OS options)

$$N = 4 \times 3 \times 3 \times 4$$
$$N = 12 \times 12 = 144$$

---

### 📝 Step 3: Final Conclusion

* **Result:** There are **144** unique virtual machine configurations available.

</details>
