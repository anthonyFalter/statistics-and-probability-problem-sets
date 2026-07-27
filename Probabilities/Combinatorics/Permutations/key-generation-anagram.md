# Problem: Key Generation from Anagram Patterns (Permutations with Repetition)

## 📌 Problem Overview

A security algorithm generates cryptographic salt tokens by rearranging the letters in the word **`DATABASE`**. Because some letters appear multiple times, swapping identical letters does not produce a distinct new string.

* **Total Letters ($n$):** $8$ (`D, A, T, A, B, A, S, E`)
* **Letter Frequencies:**
  * `A`: $3$
  * `D`: $1$
  * `T`: $1$
  * `B`: $1$
  * `S`: $1$
  * `E`: $1$
* **Objective:** Calculate the total number of **unique (distinguishable)** $8$-character tokens that can be formed using all the letters in `DATABASE`.

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Rule

Since we are arranging a set of elements where some items are identical, we apply the **Distinguishable Permutations Formula**.

* **Formula:** $P = \frac{n!}{n_1! \cdot n_2! \dots n_k!}$

---

### 🧮 Step 2: Compute the Permutations

$$P = \frac{8!}{3! \cdot 1! \cdot 1! \cdot 1! \cdot 1! \cdot 1!}$$

$$P = \frac{8!}{3!} = \frac{40,320}{6} = 6,720$$

---

### 📝 Step 3: Final Conclusion

* **Result:** There are **$6,720$** unique cryptographic tokens that can be generated from the word `DATABASE`.

</details>
