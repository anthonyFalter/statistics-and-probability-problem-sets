# Problem: App Load Time Optimization (One-Sample T-Test, Left-Tailed)

## 📌 Problem Overview

A mobile software dev team refactored their app's codebase to optimize load speeds. They want to verify if the average startup time has decreased below the previous release benchmark of **3.2 seconds**.

* **Baseline Mean ($\mu_0$):** $3.2\text{ seconds}$
* **Sample Size ($n$):** $18\text{ launch tests}$ (Degrees of Freedom, $df = 17$)
* **Sample Mean ($\bar{x}$):** $2.75\text{ seconds}$
* **Sample Standard Deviation ($s$):** $0.85\text{ seconds}$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing for a *decrease* in load time makes this a **left-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu \ge 3.2$  
  *(The code refactoring did not reduce average load time.)*
* **Alternative Hypothesis ($H_a$):** $\mu < 3.2$  
  *(The code refactoring significantly reduced average load time.)*

---

### 🧮 Step 2: Compute the Test Statistic ($t$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{s}{\sqrt{n}} = \frac{0.85}{\sqrt{18}} \approx \frac{0.85}{4.2426} \approx 0.2003\text{ seconds}$$

#### 2. Calculate the $t$-Score
$$t = \frac{\bar{x} - \mu_0}{SE} = \frac{2.75 - 3.2}{0.2003} = \frac{-0.45}{0.2003} \approx -2.25$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a left-tailed test at $\alpha = 0.05$ with $df = 17$:

  $$t_{\text{critical}} = -1.740$$

* **Decision Rule:** Reject $H_0$ if $t_{\text{calculated}} \le -1.740$.
* Since $-2.25 \le -1.740$, $t_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(t_{17} \le -2.25) \approx 0.0190 \quad (1.90\%)$$
* Since $0.0190 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ level to conclude that the refactored code significantly reduced app load time.

</details>

---
