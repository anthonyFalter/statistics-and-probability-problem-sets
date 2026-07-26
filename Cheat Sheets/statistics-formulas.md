# 🧮 Statistics & Data Science Formula Reference Guide

A complete formula cheat sheet for Descriptive Statistics, Probability, Hypothesis Testing, and Machine Learning Regression/Classification models.

---

## 📌 1. Descriptive & Summary Statistics

### Measures of Central Tendency & Dispersion

| Metric | Population Formula | Sample Formula | Notes |
| :--- | :---: | :---: | :--- |
| **Mean** | $\mu = \frac{\sum X}{N}$ | $\bar{x} = \frac{\sum x}{n}$ | Average value. |
| **Variance** | $\sigma^2 = \frac{\sum (X - \mu)^2}{N}$ | $s^2 = \frac{\sum (x_i - \bar{x})^2}{n - 1}$ | Sample uses $n-1$ (Bessel's Correction) to remain unbiased. |
| **Standard Deviation** | $\sigma = \sqrt{\sigma^2}$ | $s = \sqrt{s^2}$ | Square root of variance; in original units. |
| **Standard Error ($SE$)** | $SE = \frac{\sigma}{\sqrt{N}}$ | $SE = \frac{s}{\sqrt{n}}$ | Standard deviation of the sample distribution of the mean. |

---

## 🎲 2. Probability & Bayes' Theorem

* **Basic Probability:**
  $$P(A) = \frac{\text{Number of Favorable Outcomes}}{\text{Total Possible Outcomes}}$$

* **Complement Rule:**
  $$P(A') = 1 - P(A)$$

* **Addition Rule (Union - "OR"):**
  $$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

* **Conditional Probability:**
  $$P(A \mid B) = \frac{P(A \cap B)}{P(B)}$$

<details>
<summary>👁️ <b>Click to reveal Bayes' Theorem & Normal Distribution Formulas</b></summary>

<br>

* **Bayes' Theorem (Foundation for Naive Bayes Classifier):**
  $$P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}$$

* **Probability Density Function of Normal Distribution $N(\mu, \sigma^2)$:**
  $$f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{1}{2} \left( \frac{x - \mu}{\sigma} \right)^2}$$

</details>

---

## 🧪 3. Inferential Statistics & Hypothesis Testing

<details>
<summary>👁️ <b>Click to reveal Z-Test, t-Test, and Confidence Interval Formulas</b></summary>

<br>

### Test Statistics

* **One-Sample $Z$-Test (Population $\sigma$ Known):**
  $$Z = \frac{\bar{x} - \mu_0}{\frac{\sigma}{\sqrt{n}}}$$

* **One-Sample $t$-Test (Population $\sigma$ Unknown):**
  $$t = \frac{\bar{x} - \mu_0}{\frac{s}{\sqrt{n}}}, \quad df = n - 1$$

* **Two-Sample Independent $t$-Test (Equal Variances Assumed):**
  $$t = \frac{\bar{x}_1 - \bar{x}_2}{s_p \sqrt{\frac{1}{n_1} + \frac{1}{n_2}}}$$
  *where pooled variance $s_p^2 = \frac{(n_1 - 1)s_1^2 + (n_2 - 1)s_2^2}{n_1 + n_2 - 2}$*

---

### Confidence Intervals

* **Confidence Interval for Mean ($\sigma$ Known):**
  $$CI = \bar{x} \pm Z_{\alpha/2} \left( \frac{\sigma}{\sqrt{n}} \right)$$

* **Confidence Interval for Mean ($\sigma$ Unknown):**
  $$CI = \bar{x} \pm t_{\alpha/2, df} \left( \frac{s}{\sqrt{n}} \right)$$

</details>

---

## 🤖 4. Machine Learning & Modeling Metrics

<details>
<summary>👁️ <b>Click to reveal Regression & Classification Performance Formulas</b></summary>

<br>

### Linear Regression

* **Simple Linear Model:**
  $$\hat{y} = \beta_0 + \beta_1 x$$

* **Slope ($\beta_1$) & Intercept ($\beta_0$):**
  $$\beta_1 = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2} = r \left( \frac{s_y}{s_x} \right)$$
  $$\beta_0 = \bar{y} - \beta_1 \bar{x}$$

* **Coefficient of Determination ($R^2$):**
  $$R^2 = 1 - \frac{SS_{\text{res}}}{SS_{\text{tot}}} = 1 - \frac{\sum (y_i - \hat{y}_i)^2}{\sum (y_i - \bar{y})^2}$$

---

### Classification Evaluation Metrics

Given a Confusion Matrix ($TP, TN, FP, FN$):

* **Accuracy:**
  $$\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}$$

* **Precision (Positive Predictive Value):**
  $$\text{Precision} = \frac{TP}{TP + FP}$$

* **Recall / Sensitivity (True Positive Rate):**
  $$\text{Recall} = \frac{TP}{TP + FN}$$

* **$F_1$-Score (Harmonic Mean of Precision and Recall):**
  $$F_1 = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}} = \frac{2TP}{2TP + FP + FN}$$

</details>
