# Problem: Smartphone Battery Life Comparison (Two-Sample Z-Test for Means, Left-Tailed)

## 📌 Problem Overview

A hardware review site tests if **Brand A smartphones** have a **shorter** average battery lifespan than **Brand B smartphones**.

* **Brand A Sample ($n_1$):** $40\text{ phones}, \quad \bar{x}_1 = 11.2\text{ hours}, \quad \sigma_1 = 1.5\text{ hours}$
* **Brand B Sample ($n_2$):** $45\text{ phones}, \quad \bar{x}_2 = 12.1\text{ hours}, \quad \sigma_2 = 1.8\text{ hours}$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing whether Brand A's mean is *less than* Brand B's mean ($\mu_1 < \mu_2$) makes this a **left-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu_1 - \mu_2 \ge 0$  
  *(Brand A battery life is not shorter than Brand B.)*
* **Alternative Hypothesis ($H_a$):** $\mu_1 - \mu_2 < 0$  
  *(Brand A battery life is significantly shorter than Brand B.)*

---

### 🧮 Step 2: Compute the Test Statistic ($Z$-Score)

#### 1. Calculate Standard Error ($SE$)
$$SE = \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}} = \sqrt{\frac{1.5^2}{40} + \frac{1.8^2}{45}} = \sqrt{\frac{2.25}{40} + \frac{3.24}{45}} = \sqrt{0.05625 + 0.072} \approx 0.3581\text{ hours}$$

#### 2. Calculate $Z$-Score
$$Z = \frac{(\bar{x}_1 - \bar{x}_2) - 0}{SE} = \frac{11.2 - 12.1}{0.3581} = \frac{-0.9}{0.3581} \approx -2.51$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a left-tailed test at $\alpha = 0.05$:

  $$Z_{\text{critical}} = -1.645$$

* Since $-2.51 \le -1.645$, $Z_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(Z \le -2.51) \approx 0.0060 \quad (0.60\%)$$
* Since $0.0060 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is strong evidence at the $5\%$ significance level to conclude that Brand A smartphones have a significantly shorter average battery life than Brand B smartphones.

</details>
