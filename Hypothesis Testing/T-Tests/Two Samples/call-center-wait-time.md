# Problem: Call Center Wait Time Comparison (Two-Sample Independent T-Test, Right-Tailed)

## 📌 Problem Overview

A customer service management team wants to test if legacy Routing System A results in a **longer** mean wait time (in minutes) than new Automated System B. Assume equal population variances ($\sigma_1^2 = \sigma_2^2$).

* **Group 1 (System A - Legacy):** $n_1 = 16$, $\bar{x}_1 = 8.5\text{ min}$, $s_1 = 2.1\text{ min}$
* **Group 2 (System B - Automated):** $n_2 = 16$, $\bar{x}_2 = 6.8\text{ min}$, $s_2 = 1.8\text{ min}$
* **Degrees of Freedom ($df$):** $n_1 + n_2 - 2 = 16 + 16 - 2 = 30$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing whether System A's wait time is *greater than* System B's makes this a **right-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu_1 - \mu_2 \le 0$  
  *(Legacy System A does not have a longer average wait time than System B.)*
* **Alternative Hypothesis ($H_a$):** $\mu_1 - \mu_2 > 0$  
  *(Legacy System A has a significantly longer average wait time than System B.)*

---

### 🧮 Step 2: Compute the Test Statistic ($t$-Score)

#### 1. Calculate the Pooled Variance ($s_p^2$)
$$s_p^2 = \frac{(n_1 - 1)s_1^2 + (n_2 - 1)s_2^2}{n_1 + n_2 - 2} = \frac{(15)(4.41) + (15)(3.24)}{30} = \frac{66.15 + 48.60}{30} = 3.825$$

#### 2. Calculate the Standard Error ($SE$)
$$SE = \sqrt{s_p^2 \left(\frac{1}{n_1} + \frac{1}{n_2}\right)} = \sqrt{3.825 \left(\frac{1}{16} + \frac{1}{16}\right)} = \sqrt{3.825 \times 0.125} = \sqrt{0.478125} \approx 0.6915\text{ min}$$

#### 3. Calculate the $t$-Score
$$t = \frac{(\bar{x}_1 - \bar{x}_2) - 0}{SE} = \frac{8.5 - 6.8}{0.6915} = \frac{1.7}{0.6915} \approx 2.46$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a right-tailed test at $\alpha = 0.05$ with $df = 30$:

  $$t_{\text{critical}} = 1.697$$

* **Decision Rule:** Reject $H_0$ if $t_{\text{calculated}} \ge 1.697$.
* Since $2.46 \ge 1.697$, $t_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(t_{30} \ge 2.46) \approx 0.0100 \quad (1.00\%)$$
* Since $0.0100 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ significance level to conclude that legacy System A results in a significantly longer average customer wait time than automated System B.

</details>
