# Problem: User Password Policy Combinations (Fundamental Counting Principle)

## 📌 Problem Overview

A system administrator is defining password requirements for an internal service. A temporary password must be exactly **$4$ characters** long, structured as follows:

* **1st character:** A uppercase letter ($A\text{--}Z$, $26$ possibilities)
* **2nd character:** A lowercase letter ($a\text{--}z$, $26$ possibilities)
* **3rd character:** A digit ($0\text{--}9$, $10$ possibilities)
* **4th character:** A special character ($!\, @\, \#\, \$\, \%\, \hat{}\, \&\, *$, $8$ possibilities)

* **Objective:** Determine the total number of unique valid passwords that can be generated under this rule.

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule

By the **Fundamental Counting Principle**, if a sequence of choices consists of $n_1, n_2, \dots, n_k$ independent choices, the total number of possible outcomes is the product of the number of choices for each step.

* **Formula:** $N = n_1 \times n_2 \times n_3 \times \dots \times n_k$

---

### 🧮 Step 2: Compute the Total Outcomes

* $n_1 = 26$ (Uppercase letters)
* $n_2 = 26$ (Lowercase letters)
* $n_3 = 10$ (Digits)
* $n_4 = 8$ (Special characters)

$$N = 26 \times 26 \times 10 \times 8$$
$$N = 676 \times 80 = 54,080$$

---

### 📝 Step 3: Final Conclusion

* **Result:** There are **$54,080$** unique temporary passwords that can be generated using this format.

</details>
