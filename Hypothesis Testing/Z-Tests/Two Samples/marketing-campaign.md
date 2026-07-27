# Problem 5: Customer Churn Rate Reduction (Two-Sample Z-Test for Proportions, Left-Tailed)

## 📌 Problem Overview

A SaaS provider launched a new onboarding tutorial program to check if it **reduces customer churn** compared to the standard onboarding process.

* **Standard Onboarding ($n_1$):** $500\text{ users}, \quad x_1 = 45\text{ churned} \quad (\hat{p}_1 = 0.090)$
* **New Tutorial Onboarding ($n_2$):** $500\text{ users}, \quad x_2 = 28\text{ churned} \quad (\hat{p}_2 = 0.056)$
* **Significance Level ($\alpha$):** $0.01$ ($1\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing if the new tutorial reduces churn ($p_2 < p_1$, or $p_2 - p_1 < 0$) is a **left-tailed test**.

* **Null Hypothesis ($H_0$):** $p_2 - p_1 \ge 0$  
  *(The new onboarding program did not reduce customer churn.)*
* **Alternative Hypothesis ($H_a$):** $p_2 - p_1 < 0$  
  *(The new onboarding program significantly reduced customer churn.)*

---

### 🧮 Step 2: Compute the Test Statistic ($Z$-Score)

#### 1. Calculate Pooled Proportion ($\hat{p}$)
$$\hat{p} = \frac{x_1 + x_2}{n_1 + n_2} = \frac{45 + 28}{500 + 500} = \frac{73}{1000} = 0.073$$

#### 2. Calculate Standard Error ($SE$)
$$SE = \sqrt{\hat{p}(1 - \hat{p}) \left( \frac{1}{n_1} + \frac{1}{n_2} \right)} = \sqrt{0.073 \times 0.927 \times \left( \frac{1}{500} + \frac{1}{500} \right)} \approx 0.01645$$

#### 3. Calculate $Z$-Score
$$Z = \frac{\hat{p}_2 - \hat{p}_1}{SE} = \frac{0.056 - 0.090}{0.01645} = \frac{-0.034}{0.01645} \approx -2.07$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a left-tailed test at $\alpha = 0.01$:

  $$Z_{\text{critical}} = -2.326$$

* Since $-2.07 > -2.326$, $Z_{\text{calculated}}$ does **not** reach the critical boundary.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(Z \le -2.07) \approx 0.0192 \quad (1.92\%)$$
* Since $0.0192 > 0.01$ (the strict $1\%$ significance level), the result is **not statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Fail to Reject $H_0$** (Retain the Null Hypothesis).
* **Contextual Conclusion:** Although the churn rate was lower in the new program ($5.6\%$ vs $9.0\%$), there is insufficient evidence at the strict $1\%$ significance level ($\alpha = 0.01$) to conclusively prove the tutorial was responsible. *(Note: At $\alpha = 0.05$, this result would have been significant!)*

</details>
