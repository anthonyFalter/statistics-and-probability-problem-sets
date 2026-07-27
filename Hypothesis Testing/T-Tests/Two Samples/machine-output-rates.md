# Problem: Machine Output Rates (Two-Sample Independent T-Test, Left-Tailed)

## 📌 Problem Overview

A factory operations manager wants to test if older Machine Model Alpha produces **fewer** defective parts per shift than newer Machine Model Beta. Assume equal population variances ($\sigma_1^2 = \sigma_2^2$).

* **Group 1 (Model Alpha):** $n_1 = 10$, $\bar{x}_1 = 12.4\text{ parts}$, $s_1 = 2.8\text{ parts}$
* **Group 2 (Model Beta):** $n_2 = 10$, $\bar{x}_2 = 16.2\text{ parts}$, $s_2 = 3.1\text{ parts}$
* **Degrees of Freedom ($df$):** $n_1 + n_2 - 2 = 10 + 10 - 2 = 18$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing whether Model Alpha's defective count is *less than* Model Beta's makes this a **left-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu_1 - \mu_2 \ge 0$  
  *(Model Alpha does not produce fewer defective parts than Model Beta.)*
* **Alternative Hypothesis ($H_a$):** $\mu_1 - \mu_2 < 0$  
  *(Model Alpha produces significantly fewer defective parts than Model Beta.)*

---

### 🧮 Step 2: Compute the Test Statistic ($t$-Score)

#### 1. Calculate the Pooled Variance ($s_p^2$)
$$s_p^2 = \frac{(n_1 - 1)s_1^2 + (n_2 - 1)s_2^2}{n_1 + n_2 - 2} = \frac{(9)(7.84) + (9)(9.61)}{18} = \frac{70.56 + 86.49}{18} = 8.725$$

#### 2. Calculate the Standard Error ($SE$)
$$SE = \sqrt{s_p^2 \left(\frac{1}{n_1} + \frac{1}{n_2}\right)} = \sqrt{8.725 \left(\frac{1}{10} + \frac{1}{10}\right)} = \sqrt{8.725 \times 0.20} = \sqrt{1.745} \approx 1.3210\text{ parts}$$

#### 3. Calculate the $t$-Score
$$t = \frac{(\bar{x}_1 - \bar{x}_2) - 0}{SE} = \frac{12.4 - 16.2}{1.3210} = \frac{-3.8}{1.3210} \approx -2.88$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a left-tailed test at $\alpha = 0.05$ with $df = 18$:

  $$t_{\text{critical}} = -1.734$$

* **Decision Rule:** Reject $H_0$ if $t_{\text{calculated}} \le -1.734$.
* Since $-2.88 \le -1.734$, $t_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(t_{18} \le -2.88) \approx 0.0051 \quad (0.51\%)$$
* Since $0.0051 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ level to conclude that Machine Model Alpha produces significantly fewer defective parts per shift than Machine Model Beta.

</details>
