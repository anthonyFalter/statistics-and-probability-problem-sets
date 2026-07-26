# Problem: Online Delivery Time Reduction (One-Sample Z-Test)

## 📌 Problem Overview

An online delivery company wants to test if a new training program reduced average delivery time from 40 minutes. 

* **Baseline / Population Mean ($\mu_0$):** $40\text{ minutes}$
* **Sample Size ($n$):** $50\text{ deliveries}$
* **Sample Mean ($\bar{x}$):** $38\text{ minutes}$
* **Population Standard Deviation ($\sigma$):** $5\text{ minutes}$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Because the company specifically wants to test if the training *reduced* (decreased) the delivery time, this is a **left-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu \ge 40$  
  *(The training program had no effect, or delivery time increased/remained at least 40 minutes.)*
* **Alternative Hypothesis ($H_a$):** $\mu < 40$  
  *(The training program successfully reduced average delivery time to less than 40 minutes.)*

---

### 🧮 Step 2: Compute the Test Statistic ($Z$-Score)

#### 1. Calculate the Standard Error ($SE$)
The standard error measures the variability we expect between sample means due to random sampling:

$$SE = \frac{\sigma}{\sqrt{n}} = \frac{5}{\sqrt{50}} = \frac{5}{7.0711} \approx 0.7071\text{ minutes}$$

#### 2. Calculate the $Z$-Score
The $Z$-score measures how many standard errors our sample mean ($\bar{x} = 38$) sits below the baseline population mean ($\mu_0 = 40$):

$$Z = \frac{\bar{x} - \mu_0}{SE} = \frac{38 - 40}{0.7071} = \frac{-2}{0.7071} \approx -2.83$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

We can evaluate the decision using two equivalent statistical methods:

#### Method A: Critical Value Approach
* For a left-tailed test at $\alpha = 0.05$, the critical value from the Standard Normal Distribution table is:

  $$Z_{\text{critical}} = -1.645$$

* **Decision Rule:** Reject $H_0$ if $Z_{\text{calculated}} \le Z_{\text{critical}}$.
* Since $-2.83 \le -1.645$, we fall deep into the **rejection region**.

#### Method B: $P$-value Approach
* The $P$-value represents the probability of obtaining a sample mean as extreme as $38$ minutes purely by random chance if $H_0$ were true:

  $$P\text{-value} = P(Z \le -2.83) \approx 0.0023 \quad (0.23\%)$$

* **Decision Rule:** Reject $H_0$ if $P\text{-value} \le \alpha$.
* Since $0.0023 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is strong statistical evidence at the $5\%$ significance level ($\alpha = 0.05$) to conclude that the new training program significantly reduced the average delivery time below 40 minutes.

---

### 💡 Key Takeaways for Data Science

1. **Why a Z-Test instead of a t-Test?**
   * The population standard deviation ($\sigma = 5$) is **known**, and the sample size is large ($n = 50 \ge 30$), satisfying the Central Limit Theorem. If only the sample standard deviation ($s$) were known, a **One-Sample t-Test** would be required instead.
2. **Practical Significance vs. Statistical Significance:**
   * While a 2-minute reduction ($40 \rightarrow 38$) is statistically proven here ($p = 0.0023$), in real-world business analytics, you would also evaluate if a 2-minute savings justifies the financial cost of running the training program.

</details>
