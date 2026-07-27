# Problem: Software Engineer Salaries by Region (Two-Sample Z-Test for Means, Right-Tailed)

## 📌 Problem Overview

A tech recruitment agency wants to determine if software engineers in **City A** earn significantly **more** on average than software engineers in **City B**.

* **City A Sample ($n_1$):** $60\text{ engineers}, \quad \bar{x}_1 = \$115,000, \quad \sigma_1 = \$12,000$
* **City B Sample ($n_2$):** $75\text{ engineers}, \quad \bar{x}_2 = \$108,000, \quad \sigma_2 = \$10,000$
* **Significance Level ($\alpha$):** $0.01$ ($1\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing whether City A's average salary is *greater than* City B's makes this a **right-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu_1 - \mu_2 \le 0$  
  *(Engineers in City A do not earn more than engineers in City B.)*
* **Alternative Hypothesis ($H_a$):** $\mu_1 - \mu_2 > 0$  
  *(Engineers in City A earn significantly more than in City B.)*

---

### 🧮 Step 2: Compute the Test Statistic ($Z$-Score)

#### 1. Calculate Standard Error ($SE$)
$$SE = \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}} = \sqrt{\frac{12000^2}{60} + \frac{10000^2}{75}} = \sqrt{2,400,000 + 1,333,333.33} \approx \$1,932.18$$

#### 2. Calculate $Z$-Score
$$Z = \frac{(\bar{x}_1 - \bar{x}_2) - 0}{SE} = \frac{115,000 - 108,000}{1932.18} = \frac{7000}{1932.18} \approx 3.62$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a right-tailed test at $\alpha = 0.01$:

  $$Z_{\text{critical}} = 2.326$$

* Since $3.62 \ge 2.326$, $Z_{\text{calculated}}$ falls deep into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(Z \ge 3.62) \approx 0.0001 \quad (0.01\%)$$
* Since $0.0001 \le 0.01$, the result is **highly statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is overwhelming statistical evidence at the $1\%$ significance level to conclude that software engineers in City A earn significantly higher average salaries than those in City B.

</details>
