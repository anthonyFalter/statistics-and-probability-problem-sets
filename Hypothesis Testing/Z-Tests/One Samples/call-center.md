# Problem: Support Call Duration Reduction (One-Sample Z-Test, Left-Tailed)

## 📌 Problem Overview

A tech support team introduced an AI knowledge base system to assist support agents. They want to test if the new tool **reduced** average customer resolution time below the historical standard of 12 minutes.

* **Baseline Mean ($\mu_0$):** $12\text{ minutes}$
* **Sample Size ($n$):** $64\text{ call logs}$
* **Sample Mean ($\bar{x}$):** $11.4\text{ minutes}$
* **Population Standard Deviation ($\sigma$):** $2.8\text{ minutes}$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing for a *reduction* makes this a **left-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu \ge 12$  
  *(The AI tool did not reduce resolution time.)*
* **Alternative Hypothesis ($H_a$):** $\mu < 12$  
  *(The AI tool successfully reduced resolution time.)*

---

### 🧮 Step 2: Compute the Test Statistic ($Z$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{\sigma}{\sqrt{n}} = \frac{2.8}{\sqrt{64}} = \frac{2.8}{8} = 0.35\text{ minutes}$$

#### 2. Calculate the $Z$-Score
$$Z = \frac{\bar{x} - \mu_0}{SE} = \frac{11.4 - 12}{0.35} = \frac{-0.6}{0.35} \approx -1.71$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a left-tailed test at $\alpha = 0.05$:

  $$Z_{\text{critical}} = -1.645$$

* **Decision Rule:** Reject $H_0$ if $Z_{\text{calculated}} \le -1.645$.
* Since $-1.71 \le -1.645$, $Z_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(Z \le -1.71) \approx 0.0436 \quad (4.36\%)$$
* Since $0.0436 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ significance level to conclude that the AI knowledge base tool significantly reduced average support call duration.

</details>
