# Problem: E-commerce Order Value Check (One-Sample Z-Test, Fail to Reject)

## 📌 Problem Overview

An e-commerce store launched a free shipping promotion threshold expecting it to **increase** average customer spending beyond the historical average of $50.00.

* **Baseline Mean ($\mu_0$):** $\$50.00$
* **Sample Size ($n$):** $40\text{ orders}$
* **Sample Mean ($\bar{x}$):** $\$51.20$
* **Population Standard Deviation ($\sigma$):** $\$8.00$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing whether the promotion *increased* average spending makes this a **right-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu \le 50$  
  *(The promotion did not increase average order value.)*
* **Alternative Hypothesis ($H_a$):** $\mu > 50$  
  *(The promotion successfully increased average order value.)*

---

### 🧮 Step 2: Compute the Test Statistic ($Z$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{\sigma}{\sqrt{n}} = \frac{8}{\sqrt{40}} = \frac{8}{6.3246} \approx 1.2649$$

#### 2. Calculate the $Z$-Score
$$Z = \frac{\bar{x} - \mu_0}{SE} = \frac{51.20 - 50.00}{1.2649} = \frac{1.20}{1.2649} \approx 0.95$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a right-tailed test at $\alpha = 0.05$:

  $$Z_{\text{critical}} = 1.645$$

* **Decision Rule:** Reject $H_0$ if $Z_{\text{calculated}} \ge 1.645$.
* Since $0.95 < 1.645$, $Z_{\text{calculated}}$ falls in the **non-rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(Z \ge 0.95) = 1 - 0.8289 = 0.1711 \quad (17.11\%)$$
* Since $0.1711 > 0.05$, the result is **not statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Fail to Reject $H_0$** (Retain the Null Hypothesis).
* **Contextual Conclusion:** There is not enough statistical evidence at the $5\%$ significance level to conclude that the free shipping promotion increased the average customer order value. The observed difference ($\$51.20$ vs. $\$50.00$) can be attributed to random sampling variation.

---

### 💡 Key Takeaway
Failing to reject $H_0$ does **not** mean you proved the promotion had zero effect; it simply means the evidence isn't strong enough yet to rule out random chance!

</details>
