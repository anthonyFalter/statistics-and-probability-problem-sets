# Problem: Hard Drive Quality Audit (Hypergeometric Distribution)

## 📌 Problem Overview

A storage server rack contains **$20$ hard drives**, of which **$4$ drives are defective** ($K = 4$). A technician randomly selects **$5$ drives** ($n = 5$) without replacement for diagnostics.

* **Total Population ($N$):** $20\text{ drives}$
* **Total Defective Drives in Population ($K$):** $4\text{ drives}$
* **Sample Size ($n$):** $5\text{ drives}$
* **Objective:** Calculate the probability that the technician selects **exactly $2$ defective drives** in their sample ($P(X = 2)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Distribution & Formula

Since sampling is done **without replacement** from a finite population divided into two categories (defective / non-defective), this follows a **Hypergeometric Distribution**: $X \sim \text{Hypergeo}(N = 20, K = 4, n = 5)$.

* **Formula:** $P(X = k) = \frac{\binom{K}{k} \binom{N - K}{n - k}}{\binom{N}{n}}$

---

### 🧮 Step 2: Compute the Probability

#### 1. Calculate Combinations
* **Ways to choose $2$ defective drives from $4$:**
  $$\binom{4}{2} = \frac{4 \times 3}{2 \times 1} = 6$$

* **Ways to choose $3$ non-defective drives from $16$ ($N - K = 20 - 4$):**
  $$\binom{16}{3} = \frac{16 \times 15 \times 14}{3 \times 2 \times 1} = 560$$

* **Total ways to choose $5$ drives from $20$:**
  $$\binom{20}{5} = \frac{20 \times 19 \times 18 \times 17 \times 16}{5 \times 4 \times 3 \times 2 \times 1} = 15,504$$

#### 2. Plug Values into PMF
$$P(X = 2) = \frac{6 \times 560}{15,504} = \frac{3,360}{15,504} \approx 0.2167 \quad (21.67\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** The probability that exactly $2$ out of the $5$ randomly audited hard drives are defective is approximately **$0.2167$** or **$21.67\%$**.

</details>
