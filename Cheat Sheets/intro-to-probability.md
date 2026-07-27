# 📊 Comprehensive Statistics & Probability Reference Guide

A fundamental master cheat sheet combining Descriptive Statistics, Fundamental Probability, Bayesian Reasoning, Counting Principles, and Theoretical Distributions.

---

## 📈 1. Descriptive Statistics

Descriptive statistics summarize and organize characteristics of a dataset.

### 🔹 A. Measures of Central Tendency
Central tendency describes the center or "typical value" of a dataset.

* **Mean ($\mu$ or $\bar{x}$):** The arithmetic average of all values. Highly sensitive to extreme outliers.
  * **Population Mean:** $\mu = \frac{\sum X}{N}$
  * **Sample Mean:** $\bar{x} = \frac{\sum x}{n}$
* **Median ($\tilde{x}$):** The middlemost value when data is sorted in ascending order. **Robust to outliers.**
  * *Odd $n$:* Middle value at position $\frac{n+1}{2}$.
  * *Even $n$:* Average of two middle values at positions $\frac{n}{2}$ and $\frac{n}{2} + 1$.
* **Mode:** The most frequently occurring value(s) in a dataset. 
  * *Unimodal:* 1 mode | *Bimodal:* 2 modes | *Multimodal:* >2 modes | *No Mode:* All values occur equally.

---

### 🔹 B. Measures of Dispersion (Spread)
Dispersion describes how spread out or varied data values are relative to the center.

* **Range:** The total distance between maximum and minimum values ($X_{\text{max}} - X_{\text{min}}$).
* **Variance ($\sigma^2$ or $s^2$):** Average squared deviation from the mean.
  * **Population Variance:** $\sigma^2 = \frac{\sum (X_i - \mu)^2}{N}$
  * **Sample Variance:** $s^2 = \frac{\sum (x_i - \bar{x})^2}{n - 1} \quad \text{(Bessel's correction)}$
* **Standard Deviation ($\sigma$ or $s$):** Square root of variance; expressed in original physical units.
  * **Population SD:** $\sigma = \sqrt{\sigma^2}$
  * **Sample SD:** $s = \sqrt{s^2}$

---

### 🔹 C. Measures of Position
Position metrics identify where a specific data point falls relative to the entire dataset.

* **Percentiles ($P_k$):** Values dividing sorted data into 100 equal parts ($P_{50} = \text{Median}$).
* **Quartiles ($Q_1, Q_2, Q_3$):** Values dividing sorted data into 4 equal quarters ($25\%$ each).
  * **$Q_1$ (Lower Quartile):** 25th percentile ($P_{25}$).
  * **$Q_2$ (Second Quartile):** 50th percentile ($P_{50}$) = **Median**.
  * **$Q_3$ (Upper Quartile):** 75th percentile ($P_{75}$).
* **$Z$-Score (Standardized Position):** Number of standard deviations a raw score $x$ sits from the mean:
  $$Z = \frac{x - \mu}{\sigma} \quad \text{or} \quad Z = \frac{x - \bar{x}}{s}$$

---

<details>
<summary>👁️ <b>Click to reveal Descriptive Statistics Breakdown: Skewness, Empirical Rule & Outlier Rules</b></summary>

<br>

#### ⚖️ Central Tendency Selection Matrix

| Metric | Best Used For | Handles Outliers? | Example |
| :--- | :--- | :---: | :--- |
| **Mean** | Symmetric / Normal continuous data | ❌ No | Exam test scores, heights |
| **Median** | Skewed continuous or ordinal data | ✅ Yes | Income levels, house prices |
| **Mode** | Categorical / Nominal data | ✅ Yes | Popular shirt color, car brands |

---

#### 📊 Skewness & Distribution Shape
* **Symmetrical (Normal):** $\text{Mean} = \text{Median} = \text{Mode}$
* **Right-Skewed (Positive Skew):** Long right tail $\rightarrow \text{Mode} < \text{Median} < \text{Mean}$
* **Left-Skewed (Negative Skew):** Long left tail $\rightarrow \text{Mean} < \text{Median} < \text{Mode}$

---

#### 🎯 Empirical Rule (68–95–99.7 Rule for Normal Distributions)
* $\approx \mathbf{68\%}$ of data falls within $\mu \pm 1\sigma$
* $\approx \mathbf{95\%}$ of data falls within $\mu \pm 2\sigma$
* $\approx \mathbf{99.7\%}$ of data falls within $\mu \pm 3\sigma$

---

#### 📦 $1.5 \times IQR$ Rule for Outlier Detection
Interquartile Range: $IQR = Q_3 - Q_1$
* **Lower Fence:** $Q_1 - 1.5 \times IQR$
* **Upper Fence:** $Q_3 + 1.5 \times IQR$
*(Any data point outside these fences is a potential outlier).*

</details>

---

## 🎲 2. Core Probability Concepts

* **Experiment:** A repeatable process or trial yielding an uncertain outcome.
* **Outcome:** A single specific result of an experiment.
* **Sample Space ($S$ or $\Omega$):** The set containing **all** possible outcomes of an experiment.
* **Event ($A, B$):** A subset of outcomes from the sample space.
* **Probability ($P(A)$):** Likelihood of event $A$ occurring ($0 \le P(A) \le 1$).

---

## 📐 3. The Three Axioms of Probability (Kolmogorov)

1. **Non-Negativity:** $P(A) \ge 0$ for every event $A$.
2. **Normalization:** $P(S) = 1$ (sum of all possible probabilities equals $100\%$).
3. **Additivity:** For mutually exclusive events $A_1, A_2, \dots$:
   $$P(A_1 \cup A_2 \dots) = \sum P(A_i)$$

---

## 🛠️ 4. Fundamental Rules of Probability

<details>
<summary>👁️ <b>Click to reveal Core Probability Formulas</b></summary>

<br>

* **Complement Rule:** $P(A') = 1 - P(A)$ *(event $A$ does NOT occur)*.
* **Addition Rule (Union - "OR"):**
  $$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$
  * *If Mutually Exclusive ($P(A \cap B) = 0$):* $P(A \cup B) = P(A) + P(B)$
* **Multiplication Rule (Intersection - "AND"):**
  $$P(A \cap B) = P(A) \cdot P(B \mid A)$$
  * *If Independent ($P(B \mid A) = P(B)$):* $P(A \cap B) = P(A) \cdot P(B)$
* **Conditional Probability:**
  $$P(A \mid B) = \frac{P(A \cap B)}{P(B)} \quad \text{where } P(B) > 0$$

</details>

---

## 🧠 5. Deep Dive: Bayes' Theorem & Conditional Reasoning

Bayes' Theorem provides a framework for updating our belief in a hypothesis ($H$) based on new evidence ($E$).

* **Hypothesis ($H$):** Underlying condition being tested *(e.g., Patient is sick)*.
* **Evidence ($E$):** Observed test data *(e.g., Positive test result)*.
* **Prior $P(H)$:** Initial probability before observing evidence.
* **Posterior $P(H \mid E)$):** Updated probability after observing evidence.
* **Likelihood $P(E \mid H)$:** Chance of seeing evidence given hypothesis is true.
* **False Positive Rate:** Test returns positive when hypothesis is false ($P(E \mid H')$).

---

<details>
<summary>👁️ <b>Click to reveal Master Bayes Formula, Worked Example & Naive Bayes</b></summary>

<br>

### 🧮 Master Bayes' Theorem Formula

$$P(H \mid E) = \frac{P(E \mid H) \cdot P(H)}{P(E \mid H) \cdot P(H) + P(E \mid H') \cdot P(H')}$$

---

### 📝 Worked Example: Rare Disease Test

> **Scenario:** Disease affects **$1\%$** of population ($P(\text{Sick}) = 0.01$). Test is **$95\%$ accurate** ($P(\text{Pos} \mid \text{Sick}) = 0.95$) with a **$5\%$ false positive rate** ($P(\text{Pos} \mid \text{Healthy}) = 0.05$).

1. **Calculate Total Positive Rate $P(\text{Pos})$:**
   $$P(\text{Pos}) = (0.95 \times 0.01) + (0.05 \times 0.99) = 0.0095 + 0.0495 = 0.0590$$

2. **Calculate Posterior Probability $P(\text{Sick} \mid \text{Pos})$:**
   $$P(\text{Sick} \mid \text{Pos}) = \frac{0.0095}{0.0590} \approx 0.1610 \quad (16.1\%)$$

---

### 🤖 Machine Learning: Naive Bayes Classifier
Calculates class probability assuming all features ($X_1, X_2, \dots$) are conditionally independent:

$$P(y \mid X_1, \dots, X_n) \propto P(y) \prod_{i=1}^{n} P(X_i \mid y)$$

</details>

---

## 🎯 6. Counting Principles (Combinatorics)

<details>
<summary>👁️ <b>Click to reveal Permutations & Combinations Formulas</b></summary>

<br>

* **Fundamental Counting Principle:** If task 1 has $m$ ways and task 2 has $n$ ways, combined they have $m \times n$ ways.
* **Permutations ($P(n, r)$):** Selecting $r$ items from $n$ **where order matters**.
  $$P(n, r) = \frac{n!}{(n - r)!}$$
* **Combinations ($C(n, r)$):** Selecting $r$ items from $n$ **where order DOES NOT matter**.
  $$C(n, r) = \binom{n}{r} = \frac{n!}{r!(n - r)!}$$

</details>

---

## 📊 7. Random Variables & Common Distributions

<details>
<summary>👁️ <b>Click to reveal Random Variables & Distribution Descriptions</b></summary>

<br>

### 🔹 Core Concepts
* **Expected Value ($E[X]$ or $\mu$):** Long-run average value across infinite trials ($E[X] = \sum x \cdot P(x)$).
* **Probability Mass Function (PMF):** Exact probability for discrete outcomes $P(X = x)$.
* **Probability Density Function (PDF):** Relative likelihood density for continuous outcomes.

---

### 🔹 Discrete Distributions

1. **Binomial Distribution ($X \sim \text{Binom}(n, p)$):**
   * Successes in $n$ independent trials with constant probability $p$.
   * *Formula:* $P(X = k) = \binom{n}{k} p^k (1 - p)^{n-k}$
   * *Mean:* $E[X] = np$

2. **Poisson Distribution ($X \sim \text{Poisson}(\lambda)$):**
   * Count of rare events occurring in a fixed interval at constant rate $\lambda$.
   * *Formula:* $P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$
   * *Mean & Variance:* $E[X] = Var(X) = \lambda$

---

### 🔸 Continuous Distributions

1. **Uniform Distribution ($X \sim U(a, b)$):**
   * All equal-length intervals between minimum $a$ and maximum $b$ are equally likely.
   * *Density:* $f(x) = \frac{1}{b - a}$

2. **Normal (Gaussian) Distribution ($X \sim N(\mu, \sigma^2)$):**
   * Symmetric, bell-shaped distribution defined by mean $\mu$ and standard deviation $\sigma$.
   * *Standard Normal Conversion:* $Z = \frac{X - \mu}{\sigma}$

</details>
