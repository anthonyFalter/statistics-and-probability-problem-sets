# Problem: Database Query Latency Audit (One-Sample T-Test, Two-Tailed)

## 📌 Problem Overview

A backend infrastructure team claims that a database index update keeps the average query response time at **250.0 ms**. A QA engineer tests a sample of API calls to verify if the actual performance deviates in either direction from this targeted benchmark.

* **Baseline Mean ($\mu_0$):** $250.0\text{ ms}$
* **Sample Size ($n$):** $25\text{ query logs}$ (Degrees of Freedom, $df = 24$)
* **Sample Mean ($\bar{x}$):** $241.5\text{ ms}$
* **Sample Standard Deviation ($s$):** $18.0\text{ ms}$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing whether the mean latency *differs* from 250.0 ms in either direction makes this a **two-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu = 250.0$  
  *(The average query response time equals 250.0 ms.)*
* **Alternative Hypothesis ($H_a$):** $\mu \neq 250.0$  
  *(The average query response time differs significantly from 250.0 ms.)*

---

### 🧮 Step 2: Compute the Test Statistic ($t$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{s}{\sqrt{n}} = \frac{18.0}{\sqrt{25}} = \frac{18.0}{5} = 3.60\text{ ms}$$

#### 2. Calculate the $t$-Score
$$t = \frac{\bar{x} - \mu_0}{SE} = \frac{241.5 - 250.0}{3.60} = \frac{-8.5}{3.60} \approx -2.36$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a two-tailed test at $\alpha = 0.05$ ($\alpha/2 = 0.025$) with $df = 24$:

  $$t_{\text{critical}} = \pm 2.064$$

* **Decision Rule:** Reject $H_0$ if $|t_{\text{calculated}}| \ge 2.064$.
* Since $|-2.36| = 2.36 \ge 2.064$, $t_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = 2 \times P(t_{24} \le -2.36) \approx 0.0267 \quad (2.67\%)$$
* Since $0.0267 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ level to conclude that the actual query latency significantly differs from the 250.0 ms baseline (specifically, running faster than expected).

</details>
