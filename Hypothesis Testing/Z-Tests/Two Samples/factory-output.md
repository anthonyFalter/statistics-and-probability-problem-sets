# Problem: Shift Efficiency Evaluation (Two-Sample Z-Test for Means, Fail to Reject)

## 📌 Problem Overview

An industrial plant wants to check if **Day Shift (Shift 1)** and **Night Shift (Shift 2)** produce different average units of product per hour.

* **Day Shift Sample ($n_1$):** $50\text{ hours}, \quad \bar{x}_1 = 210\text{ units}, \quad \sigma_1 = 15\text{ units}$
* **Night Shift Sample ($n_2$):** $50\text{ hours}, \quad \bar{x}_2 = 206\text{ units}, \quad \sigma_2 = 18\text{ units}$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing for *any difference* makes this a **two-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu_1 - \mu_2 = 0$  
  *(There is no difference in average hourly output between shifts.)*
* **Alternative Hypothesis ($H_a$):** $\mu_1 - \mu_2 \neq 0$  
  *(There is a significant difference in average hourly output.)*

---

### 🧮 Step 2: Compute the Test Statistic ($Z$-Score)

#### 1. Calculate Standard Error ($SE$)
$$SE = \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}} = \sqrt{\frac{15^2}{50} + \frac{18^2}{50}} = \sqrt{\frac{225}{50} + \frac{324}{50}} = \sqrt{4.5 + 6.48} = \sqrt{10.98} \approx 3.3136$$

#### 2. Calculate $Z$-Score
$$Z = \frac{(\bar{x}_1 - \bar{x}_2) - 0}{SE} = \frac{210 - 206}{3.3136} = \frac{4}{3.3136} \approx 1.21$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a two-tailed test at $\alpha = 0.05$:

  $$Z_{\text{critical}} = \pm 1.96$$

* Since $-1.96 < 1.21 < 1.96$, $Z_{\text{calculated}}$ falls in the **non-rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = 2 \times P(Z \ge 1.21) = 2 \times (1 - 0.8869) = 2 \times 0.1131 = 0.2262 \quad (22.62\%)$$
* Since $0.2262 > 0.05$, the result is **not statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Fail to Reject $H_0$** (Retain the Null Hypothesis).
* **Contextual Conclusion:** There is insufficient evidence at the $5\%$ significance level to prove a difference in average hourly production between the Day Shift and Night Shift. The difference of 4 units can be attributed to natural variation.

</details>
