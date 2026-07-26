# Problem 3: UI Redesign Engagement (One-Sample Z-Test, Right-Tailed)

## 📌 Problem Overview

A social media company launched a new UI design hoping to **increase** the average user session length beyond the historical average of 15 minutes.

* **Baseline Mean ($\mu_0$):** $15\text{ minutes}$
* **Sample Size ($n$):** $100\text{ users}$
* **Sample Mean ($\bar{x}$):** $15.8\text{ minutes}$
* **Population Standard Deviation ($\sigma$):** $3\text{ minutes}$
* **Significance Level ($\alpha$):** $0.01$ ($1\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Because the company wants to prove that session length *increased*, this is a **right-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu \le 15$  
  *(The new UI did not increase average session time.)*
* **Alternative Hypothesis ($H_a$):** $\mu > 15$  
  *(The new UI successfully increased average session time.)*

---

### 🧮 Step 2: Compute the Test Statistic ($Z$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{\sigma}{\sqrt{n}} = \frac{3}{\sqrt{100}} = \frac{3}{10} = 0.30\text{ minutes}$$

#### 2. Calculate the $Z$-Score
$$Z = \frac{\bar{x} - \mu_0}{SE} = \frac{15.8 - 15}{0.30} = \frac{0.8}{0.30} \approx 2.67$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a right-tailed test at $\alpha = 0.01$:

  $$Z_{\text{critical}} = 2.326$$

* **Decision Rule:** Reject $H_0$ if $Z_{\text{calculated}} \ge 2.326$.
* Since $2.67 \ge 2.326$, $Z_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(Z \ge 2.67) = 1 - 0.9962 = 0.0038 \quad (0.38\%)$$
* Since $0.0038 \le 0.01$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is strong statistical evidence at the $1\%$ significance level to conclude that the UI redesign significantly increased average user session time.

</details>
