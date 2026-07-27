# Problem: E-Commerce Delivery Time (One-Sample T-Test, Left-Tailed)

## 📌 Problem Overview

An online retailer promised faster shipping by switching to a local courier network. They want to evaluate if the average delivery time has dropped below their traditional standard of **5.0 days**.

* **Baseline Mean ($\mu_0$):** $5.0\text{ days}$
* **Sample Size ($n$):** $16\text{ shipments}$ (Degrees of Freedom, $df = 15$)
* **Sample Mean ($\bar{x}$):** $4.4\text{ days}$
* **Sample Standard Deviation ($s$):** $1.2\text{ days}$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing for a *reduction* in shipping time makes this a **left-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu \ge 5.0$  
  *(The new courier did not reduce delivery time.)*
* **Alternative Hypothesis ($H_a$):** $\mu < 5.0$  
  *(The new courier significantly reduced delivery time.)*

---

### 🧮 Step 2: Compute the Test Statistic ($t$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{s}{\sqrt{n}} = \frac{1.2}{\sqrt{16}} = \frac{1.2}{4} = 0.30\text{ days}$$

#### 2. Calculate the $t$-Score
$$t = \frac{\bar{x} - \mu_0}{SE} = \frac{4.4 - 5.0}{0.30} = \frac{-0.6}{0.30} = -2.00$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a left-tailed test at $\alpha = 0.05$ with $df = 15$:

  $$t_{\text{critical}} = -1.753$$

* **Decision Rule:** Reject $H_0$ if $t_{\text{calculated}} \le -1.753$.
* Since $-2.00 \le -1.753$, $t_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(t_{15} \le -2.00) \approx 0.0320 \quad (3.20\%)$$
* Since $0.0320 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ significance level to conclude that the new courier network significantly reduced delivery time.

</details>

---
### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ level to conclude that the loyalty program successfully increased average daily revenue above \$1,500.

</details>
