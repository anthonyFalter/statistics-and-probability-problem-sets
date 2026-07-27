# Problem: Marketing Campaign Conversion Rates (Two-Sample Independent T-Test, Two-Tailed)

## 📌 Problem Overview

A digital marketing team tested two distinct landing page designs (Page A vs. Page B) to see if there is a significant difference in average user session duration (in seconds) before making a purchase. Assume equal population variances ($\sigma_1^2 = \sigma_2^2$).

* **Group 1 (Page A):** $n_1 = 15$, $\bar{x}_1 = 142.5\text{ s}$, $s_1 = 12.0\text{ s}$
* **Group 2 (Page B):** $n_2 = 12$, $\bar{x}_2 = 131.0\text{ s}$, $s_2 = 10.5\text{ s}$
* **Degrees of Freedom ($df$):** $n_1 + n_2 - 2 = 15 + 12 - 2 = 25$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing for *any difference* between the two group means makes this a **two-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu_1 - \mu_2 = 0$  
  *(There is no difference in mean session duration between Page A and Page B.)*
* **Alternative Hypothesis ($H_a$):** $\mu_1 - \mu_2 \neq 0$  
  *(There is a significant difference in mean session duration between the two pages.)*

---

### 🧮 Step 2: Compute the Test Statistic ($t$-Score)

#### 1. Calculate the Pooled Variance ($s_p^2$)
$$s_p^2 = \frac{(n_1 - 1)s_1^2 + (n_2 - 1)s_2^2}{n_1 + n_2 - 2} = \frac{(14)(144) + (11)(110.25)}{25} = \frac{2016 + 1212.75}{25} = 129.15$$

#### 2. Calculate the Standard Error ($SE$)
$$SE = \sqrt{s_p^2 \left(\frac{1}{n_1} + \frac{1}{n_2}\right)} = \sqrt{129.15 \left(\frac{1}{15} + \frac{1}{12}\right)} = \sqrt{129.15 \times 0.15} = \sqrt{19.3725} \approx 4.4014\text{ s}$$

#### 3. Calculate the $t$-Score
$$t = \frac{(\bar{x}_1 - \bar{x}_2) - 0}{SE} = \frac{142.5 - 131.0}{4.4014} = \frac{11.5}{4.4014} \approx 2.61$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a two-tailed test at $\alpha = 0.05$ ($\alpha/2 = 0.025$) with $df = 25$:

  $$t_{\text{critical}} = \pm 2.060$$

* **Decision Rule:** Reject $H_0$ if $|t_{\text{calculated}}| \ge 2.060$.
* Since $|2.61| \ge 2.060$, $t_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = 2 \times P(t_{25} \ge 2.61) \approx 0.0150 \quad (1.50\%)$$
* Since $0.0150 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ level to conclude that user session duration differs significantly between landing Page A and Page B.

</details>
