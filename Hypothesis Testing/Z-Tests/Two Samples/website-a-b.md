# Problem: E-commerce Conversion Rate A/B Test (Two-Sample Z-Test for Proportions, Two-Tailed)

## 📌 Problem Overview

An e-commerce team is conducting an A/B test comparing a **Red Buy Button (Variant A)** against a **Green Buy Button (Variant B)** to check if there is any difference in conversion rates.

* **Variant A Sample Size ($n_1$):** $1,000\text{ visitors}$
* **Variant A Conversions ($x_1$):** $120$ ($\hat{p}_1 = 0.12$)
* **Variant B Sample Size ($n_2$):** $1,200\text{ visitors}$
* **Variant B Conversions ($x_2$):** $180$ ($\hat{p}_2 = 0.15$)
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing for *any difference* between the two conversion rates makes this a **two-tailed test**.

* **Null Hypothesis ($H_0$):** $p_1 - p_2 = 0$ or $p_1 = p_2$  
  *(There is no difference in conversion rates between the red and green buttons.)*
* **Alternative Hypothesis ($H_a$):** $p_1 - p_2 \neq 0$ or $p_1 \neq p_2$  
  *(There is a statistically significant difference between conversion rates.)*

---

### 🧮 Step 2: Compute the Test Statistic ($Z$-Score)

#### 1. Calculate Pooled Proportion ($\hat{p}$)
$$\hat{p} = \frac{x_1 + x_2}{n_1 + n_2} = \frac{120 + 180}{1000 + 1200} = \frac{300}{2200} \approx 0.1364$$

#### 2. Calculate Standard Error ($SE$)
$$SE = \sqrt{\hat{p}(1 - \hat{p}) \left( \frac{1}{n_1} + \frac{1}{n_2} \right)} = \sqrt{0.1364 \times 0.8636 \times \left( \frac{1}{1000} + \frac{1}{1200} \right)} \approx 0.0147$$

#### 3. Calculate $Z$-Score
$$Z = \frac{\hat{p}_1 - \hat{p}_2}{SE} = \frac{0.12 - 0.15}{0.0147} = \frac{-0.03}{0.0147} \approx -2.04$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a two-tailed test at $\alpha = 0.05$:

  $$Z_{\text{critical}} = \pm 1.96$$

* Since $-2.04 \le -1.96$, $Z_{\text{calculated}}$ falls into the lower **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = 2 \times P(Z \le -2.04) = 2 \times 0.0207 = 0.0414 \quad (4.14\%)$$
* Since $0.0414 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ significance level to conclude that button color significantly affects conversion rate, with Variant B (Green) outperforming Variant A (Red).

</details>
