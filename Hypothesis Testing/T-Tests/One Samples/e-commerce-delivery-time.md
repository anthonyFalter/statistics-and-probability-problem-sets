# Problem: E-Commerce Delivery Time (One-Sample T-Test, Left-Tailed)

## 📌 Problem Overview

An online retailer promised faster shipping by switching to a local courier network. They want to evaluate if the average delivery time has dropped below their traditional standard of **5.0 days**.

* **Baseline Mean ($\mu_0$):** $5.0\text{ days}$
* **Sample Size ($n$):** $16\text{ shipments}$ (Degrees of Freedom, $df = 15$)
* **Sample Mean ($\bar{x}$):** $4.4\text{ days}$
* **Sample Standard Deviation ($s$):** $1.2\text{ days}$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing for a *reduction* in shipping time makes this a **left-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu \ge 5.0$  
  *(The new courier did not reduce delivery time.)*
* **Alternative Hypothesis ($H_a$):** $\mu < 5.0$  
  *(The new courier significantly reduced delivery time.)*

---

### 🧮 Step 2: Compute the Test Statistic ($t$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{s}{\sqrt{n}} = \frac{1.2}{\sqrt{16}} = \frac{1.2}{4} = 0.30\text{ days}$$

#### 2. Calculate the $t$-Score
$$t = \frac{\bar{x} - \mu_0}{SE} = \frac{4.4 - 5.0}{0.30} = \frac{-0.6}{0.30} = -2.00$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a left-tailed test at $\alpha = 0.05$ with $df = 15$:

  $$t_{\text{critical}} = -1.753$$

* **Decision Rule:** Reject $H_0$ if $t_{\text{calculated}} \le -1.753$.
* Since $-2.00 \le -1.753$, $t_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(t_{15} \le -2.00) \approx 0.0320 \quad (3.20\%)$$
* Since $0.0320 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ significance level to conclude that the new courier network significantly reduced delivery time.

</details>

---

# Problem 2: Manufacturing Fill Volume (One-Sample T-Test, Right-Tailed)

## 📌 Problem Overview

A beverage bottling plant calibrated a machine designed to fill bottles with **500 mL** of liquid. Quality control suspects the machine is overfilling bottles, causing product waste.

* **Baseline Mean ($\mu_0$):** $500\text{ mL}$
* **Sample Size ($n$):** $25\text{ bottles}$ (Degrees of Freedom, $df = 24$)
* **Sample Mean ($\bar{x}$):** $503.5\text{ mL}$
* **Sample Standard Deviation ($s$):** $7.0\text{ mL}$
* **Significance Level ($\alpha$):** $0.01$ ($1\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing for *overfilling* makes this a **right-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu \le 500$  
  *(The machine is not overfilling bottles.)*
* **Alternative Hypothesis ($H_a$):** $\mu > 500$  
  *(The machine is overfilling bottles.)*

---

### 🧮 Step 2: Compute the Test Statistic ($t$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{s}{\sqrt{n}} = \frac{7.0}{\sqrt{25}} = \frac{7.0}{5} = 1.40\text{ mL}$$

#### 2. Calculate the $t$-Score
$$t = \frac{\bar{x} - \mu_0}{SE} = \frac{503.5 - 500}{1.40} = \frac{3.5}{1.40} = 2.50$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a right-tailed test at $\alpha = 0.01$ with $df = 24$:

  $$t_{\text{critical}} = 2.492$$

* **Decision Rule:** Reject $H_0$ if $t_{\text{calculated}} \ge 2.492$.
* Since $2.50 \ge 2.492$, $t_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(t_{24} \ge 2.50) \approx 0.0098 \quad (0.98\%)$$
* Since $0.0098 \le 0.01$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $1\%$ significance level to conclude that the machine is significantly overfilling the bottles.

</details>

---

# Problem 3: Battery Lifetime Verification (One-Sample T-Test, Two-Tailed)

## 📌 Problem Overview

A tech hardware company claims its smartwatches have a mean battery life of **48.0 hours**. An independent consumer watchdog tests a random sample to check if the true average differs from this claim.

* **Baseline Mean ($\mu_0$):** $48.0\text{ hours}$
* **Sample Size ($n$):** $20\text{ smartwatches}$ (Degrees of Freedom, $df = 19$)
* **Sample Mean ($\bar{x}$):** $46.2\text{ hours}$
* **Sample Standard Deviation ($s$):** $4.0\text{ hours}$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing whether battery life *differs* in either direction makes this a **two-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu = 48.0$  
  *(Mean battery life is equal to 48 hours.)*
* **Alternative Hypothesis ($H_a$):** $\mu \neq 48.0$  
  *(Mean battery life is significantly different from 48 hours.)*

---

### 🧮 Step 2: Compute the Test Statistic ($t$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{s}{\sqrt{n}} = \frac{4.0}{\sqrt{20}} \approx \frac{4.0}{4.4721} \approx 0.8944\text{ hours}$$

#### 2. Calculate the $t$-Score
$$t = \frac{\bar{x} - \mu_0}{SE} = \frac{46.2 - 48.0}{0.8944} = \frac{-1.80}{0.8944} \approx -2.01$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a two-tailed test at $\alpha = 0.05$ ($\alpha/2 = 0.025$) with $df = 19$:

  $$t_{\text{critical}} = \pm 2.093$$

* **Decision Rule:** Reject $H_0$ if $|t_{\text{calculated}}| \ge 2.093$.
* Since $|-2.01| = 2.01 < 2.093$, $t_{\text{calculated}}$ **does not** fall into the rejection region.

#### Method B: $P$-value Approach
* $$P\text{-value} = 2 \times P(t_{19} \le -2.01) \approx 0.0588 \quad (5.88\%)$$
* Since $0.0588 > 0.05$, the result is **not statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Fail to Reject $H_0$**.
* **Contextual Conclusion:** There is not enough statistical evidence at the $5\%$ level to conclude that the actual battery life differs significantly from the company's 48-hour claim.

</details>

---

# Problem 4: Employee Onboarding Efficiency (One-Sample T-Test, Left-Tailed)

## 📌 Problem Overview

HR introduced a self-paced video onboarding module designed to reduce training hours below the old classroom average of **30.0 hours**.

* **Baseline Mean ($\mu_0$):** $30.0\text{ hours}$
* **Sample Size ($n$):** $12\text{ new hires}$ (Degrees of Freedom, $df = 11$)
* **Sample Mean ($\bar{x}$):** $26.5\text{ hours}$
* **Sample Standard Deviation ($s$):** $4.8\text{ hours}$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing for a *reduction* in training time makes this a **left-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu \ge 30.0$  
  *(The video module did not reduce onboarding time.)*
* **Alternative Hypothesis ($H_a$):** $\mu < 30.0$  
  *(The video module reduced onboarding time.)*

---

### 🧮 Step 2: Compute the Test Statistic ($t$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{s}{\sqrt{n}} = \frac{4.8}{\sqrt{12}} \approx \frac{4.8}{3.4641} \approx 1.3856\text{ hours}$$

#### 2. Calculate the $t$-Score
$$t = \frac{\bar{x} - \mu_0}{SE} = \frac{26.5 - 30.0}{1.3856} = \frac{-3.50}{1.3856} \approx -2.53$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a left-tailed test at $\alpha = 0.05$ with $df = 11$:

  $$t_{\text{critical}} = -1.796$$

* **Decision Rule:** Reject $H_0$ if $t_{\text{calculated}} \le -1.796$.
* Since $-2.53 \le -1.796$, $t_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(t_{11} \le -2.53) \approx 0.0139 \quad (1.39\%)$$
* Since $0.0139 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ level to state that the self-paced video module significantly reduced average onboarding time.

</details>

---

# Problem 5: Retail Store Daily Revenue (One-Sample T-Test, Right-Tailed)

## 📌 Problem Overview

A coffee shop chain launched a new loyalty program with the goal of driving daily store revenue past its historical benchmark of **\$1,500**.

* **Baseline Mean ($\mu_0$):** $\$1,500$
* **Sample Size ($n$):** $30\text{ days}$ (Degrees of Freedom, $df = 29$)
* **Sample Mean ($\bar{x}$):** $\$1,580$
* **Sample Standard Deviation ($s$):** $\$210$
* **Significance Level ($\alpha$):** $0.05$ ($5\%$)

---

<details>
<summary>👁️ <b>Click to reveal the Hypotheses, Step-by-Step Calculation, and Conclusion</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses

Testing whether daily revenue *increased* makes this a **right-tailed test**.

* **Null Hypothesis ($H_0$):** $\mu \le 1500$  
  *(The loyalty program did not increase daily revenue.)*
* **Alternative Hypothesis ($H_a$):** $\mu > 1500$  
  *(The loyalty program increased daily revenue.)*

---

### 🧮 Step 2: Compute the Test Statistic ($t$-Score)

#### 1. Calculate the Standard Error ($SE$)
$$SE = \frac{s}{\sqrt{n}} = \frac{210}{\sqrt{30}} \approx \frac{210}{5.4772} \approx 38.3421\text{ dollars}$$

#### 2. Calculate the $t$-Score
$$t = \frac{\bar{x} - \mu_0}{SE} = \frac{1580 - 1500}{38.3421} = \frac{80}{38.3421} \approx 2.09$$

---

### 📏 Step 3: Determine Decision Rules ($P$-value & Critical Value)

#### Method A: Critical Value Approach
* For a right-tailed test at $\alpha = 0.05$ with $df = 29$:

  $$t_{\text{critical}} = 1.699$$

* **Decision Rule:** Reject $H_0$ if $t_{\text{calculated}} \ge 1.699$.
* Since $2.09 \ge 1.699$, $t_{\text{calculated}}$ falls into the **rejection region**.

#### Method B: $P$-value Approach
* $$P\text{-value} = P(t_{29} \ge 2.09) \approx 0.0227 \quad (2.27\%)$$
* Since $0.0227 \le 0.05$, the result is **statistically significant**.

---

### 📝 Step 4: Final Decision & Conclusion

* **Statistical Decision:** **Reject $H_0$** (the Null Hypothesis).
* **Contextual Conclusion:** There is sufficient evidence at the $5\%$ level to conclude that the loyalty program successfully increased average daily revenue above \$1,500.

</details>
