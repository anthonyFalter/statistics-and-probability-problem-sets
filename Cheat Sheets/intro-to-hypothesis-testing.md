# 🧪 Introduction to Hypothesis Testing Reference Guide

A fundamental cheat sheet covering core hypothesis testing principles, key terminology, step-by-step procedures, decision errors, and test selection logic.

---

## 📌 1. Core Terminology & Definitions

* **Hypothesis:** An assumption or claim about a population parameter *(e.g., mean $\mu$, proportion $p$, or variance $\sigma^2$)* that is tested using sample data.
* **Null Hypothesis ($H_0$):** The baseline status-quo statement that assumes no effect, no difference, or no change. It is presumed true until proven otherwise *(contains $=$, $\le$, or $\ge$)*.
* **Alternative Hypothesis ($H_a$ or $H_1$):** The research claim or hypothesis you are actively trying to gather evidence to support *(contains $\neq$, $<$, or $>$)*.
* **Test Statistic:** A standardized numeric value calculated from sample data *(e.g., $Z$, $t$, $F$, $\chi^2$)* used to evaluate whether to reject $H_0$.
* **Significance Level ($\alpha$):** The threshold probability of making a Type I Error, pre-determined by the analyst *(commonly set at $0.05$, $0.01$, or $0.10$)*.
* **Critical Value:** The boundary mark on the test distribution that separates the acceptance region from the rejection region.
* **$P$-value:** The probability of obtaining a sample result as extreme as, or more extreme than, the observed data, assuming $H_0$ is true.

---

## ⚖️ 2. The Four Outcomes & Statistical Decision Errors

Every hypothesis test carries a risk of reaching an incorrect conclusion due to random sampling variability:

| | **$H_0$ is Actually True** | **$H_0$ is Actually False** |
|---|---|---|
| **Reject $H_0$** | **Type I Error ($\alpha$)**<br>*(False Positive)* | **Correct Decision ($1 - \beta$)**<br>*(Statistical Power)* |
| **Fail to Reject $H_0$** | **Correct Decision ($1 - \alpha$)**<br>*(Confidence Level)* | **Type II Error ($\beta$)**<br>*(False Negative)* |

* **Type I Error ($\alpha$):** Rejecting the null hypothesis when it is actually true.
  * *Example:* Finding a drug effective when it actually has no effect.
* **Type II Error ($\beta$):** Failing to reject the null hypothesis when it is actually false.
  * *Example:* Failing to detect a true disease presence in a patient.
* **Statistical Power ($1 - \beta$):** The probability of correctly rejecting $H_0$ when $H_a$ is true *(ability to detect a real effect)*.

---

## 🛠️ 3. The Standard 4-Step Hypothesis Testing Framework

<details>
<summary>👁️ <b>Click to reveal the 4-Step Testing Procedure</b></summary>

<br>

### 🎯 Step 1: Formulate the Hypotheses
Define $H_0$ and $H_a$ based on the research question and state the significance level ($\alpha$).

* **Two-Tailed Test ($\neq$):** Checks for difference in *either direction*.
* **Left-Tailed Test ($<$):** Checks if the parameter is *less than* the baseline.
* **Right-Tailed Test ($>$):** Checks if the parameter is *greater than* the baseline.

---

### 🧮 Step 2: Compute the Test Statistic
Calculate the test statistic using sample summaries ($n$, $\bar{x}$, $s$, or $p$).

* **One-Sample $Z$-Test (Known $\sigma$):**
  $$Z = \frac{\bar{x} - \mu_0}{\frac{\sigma}{\sqrt{n}}}$$

* **One-Sample $t$-Test (Unknown $\sigma$):**
  $$t = \frac{\bar{x} - \mu_0}{\frac{s}{\sqrt{n}}} \quad \text{with } df = n - 1$$

---

### 📏 Step 3: Evaluate Using Decision Rules

Choose one of two mathematically equivalent methods to decide whether to reject $H_0$:

#### Method A: Critical Value Approach
* **Rule:** Compare the calculated test statistic to $Z_{\text{critical}}$ or $t_{\text{critical}}$.
* **Action:** Reject $H_0$ if the calculated statistic falls into the **rejection region** (beyond the critical value boundaries).

#### Method B: $P$-value Approach
* **Rule:** Compare the calculated $P$-value directly to $\alpha$.
* **Action:** 
  $$\text{If } P\text{-value} \le \alpha \implies \textbf{Reject } H_0 \quad (\text{Statistically Significant})$$
  $$\text{If } P\text{-value} > \alpha \implies \textbf{Fail to Reject } H_0 \quad (\text{Not Significant})$$

---

### 📝 Step 4: Final Decision & Contextual Conclusion
State whether you **Reject $H_0$** or **Fail to Reject $H_0$**, and interpret what that decision means in plain terms relevant to the original problem.

</details>

---

## 🔍 4. Deep Dive: Decision Rules & Tails

<details>
<summary>👁️ <b>Click to reveal Rejection Regions for Tail Configurations</b></summary>

<br>

### 🔹 Tail Rejection Criteria ($\alpha = 0.05$, $Z$-Distribution)

1. **Two-Tailed Test ($H_a: \mu \neq \mu_0$)**
   * Critical Values: $Z_{\text{critical}} = \pm 1.96$
   * Rejection Region: $Z_{\text{calc}} \le -1.96$ or $Z_{\text{calc}} \ge 1.96$
   * $P$-value: $2 \times P(Z \ge |Z_{\text{calc}}|)$

2. **Left-Tailed Test ($H_a: \mu < \mu_0$)**
   * Critical Value: $Z_{\text{critical}} = -1.645$
   * Rejection Region: $Z_{\text{calc}} \le -1.645$
   * $P$-value: $P(Z \le Z_{\text{calc}})$

3. **Right-Tailed Test ($H_a: \mu > \mu_0$)**
   * Critical Value: $Z_{\text{critical}} = 1.645$
   * Rejection Region: $Z_{\text{calc}} \ge 1.645$
   * $P$-value: $P(Z \ge Z_{\text{calc}})$

</details>

---

## 📊 5. Selecting the Correct Test

<details>
<summary>👁️ <b>Click to reveal Test Selection Cheat Sheet</b></summary>

<br>

| Scenario / Objective | Data Type | Sample Size / Conditions | Recommended Test |
|---|---|---|---|
| Compare **1 mean** to a baseline (known $\sigma$) | Continuous | Any $n$, Normal distribution | **One-Sample $Z$-Test** |
| Compare **1 mean** to a baseline (unknown $\sigma$) | Continuous | Small $n$ ($n < 30$) or sample $s$ used | **One-Sample $t$-Test** |
| Compare **2 independent means** | Continuous | Independent samples ($\sigma_1^2 = \sigma_2^2$) | **Two-Sample Independent $t$-Test** |
| Compare **2 related/paired means** | Continuous | Same subjects (Before vs. After) | **Paired Samples $t$-Test** |
| Compare **1 proportion** to a baseline | Categorical | $np \ge 10$ and $n(1-p) \ge 10$ | **One-Sample $Z$-Proportion Test** |
| Compare **observed vs. expected categorical counts** | Categorical | Count data across categories | **Chi-Square ($\chi^2$) Goodness-of-Fit** |

</details>
