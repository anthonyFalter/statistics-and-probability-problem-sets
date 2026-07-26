# Problem: Machine Net Weight Check (One-Sample Z-Test, Two-Tailed)

## 📌 Problem Overview

A beverage factory uses an automated machine to fill coffee jars with a target net weight of 200 grams. Quality control wants to verify whether the machine is miscalibrated (filling jars with **either too much or too little** coffee).

* **Target / Baseline Mean ($\mu_0$):** $200\text{ grams}$
* **Sample Size ($n$):** $36\text{ jars}$
* **Sample Mean ($\bar{x}$):** $201.8\text{ grams}$
* **Population Standard Deviation ($\sigma$):** $4\text{ grams}$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Since the quality control team is checking for *any* deviation (higher or lower than 200g), this is a **two-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu = 200$  
  *(The machine is correctly calibrated; average weight is 200 grams.)*
* **Alternative Hypothesis ($H_a$):** $\mu \neq 200$  
  *(The machine is miscalibrated; average weight is not equal to 200 grams.)*

---

### 🧮 Step 2: Compute the Test Statistic ($Z$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{\sigma}{\sqrt{n}} = \frac{4}{\sqrt{36}} = \frac{4}{6} \approx 0.6667\text{ grams}$$

#### 2. Calculate the $Z$-Score
$$Z = \frac{\bar{x} - \mu_0}{SE} = \frac{201.8 - 200}{0.6667} = \frac{1.8}{0.6667} \approx 2.70$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a two-tailed test at $\alpha = 0.05$, split the error into two tails ($\alpha/2 = 0.025$ per tail):

  $$Z_{\text{critical}} = \pm 1.96$$

* **Decision Rule:** Reject $H_0$ if $Z_{\text{calculated}} \ge 1.96$ or $Z_{\text{calculated}} \le -1.96$.
* Since $2.70 \ge 1.96$, $Z_{\text{calculated}}$ falls into the upper **rejection region**.

#### Method B: $P$-value Approach
* For a two-tailed test, multiply the single-tail probability by 2:

  $$P\text{-value} = 2 \times P(Z \ge 2.70) = 2 \times (1 - 0.9965) = 2 \times 0.0035 = 0.0070 \quad (0.70\%)$$

* Since $0.0070 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ significance level to conclude that the coffee filling machine is significantly miscalibrated and overfilling the jars on average.

</details>
