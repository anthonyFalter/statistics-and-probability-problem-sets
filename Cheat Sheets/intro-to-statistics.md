# 📈 Introduction to Statistics Reference Guide

A standalone reference guide covering core descriptive statistics: Measures of Central Tendency, Measures of Dispersion, Measures of Position, and Data Distribution Rules.

---

## 📌 1. Measures of Central Tendency

Measures of central tendency summarize a dataset by identifying a single central or "typical" value around which data points cluster.

* **Mean ($\mu$ or $\bar{x}$):** The arithmetic average of all numerical values in a dataset. Highly sensitive to extreme values (outliers).
  * **Population Mean:** $\mu = \frac{\sum X}{N}$
  * **Sample Mean:** $\bar{x} = \frac{\sum x}{n}$
* **Median ($\tilde{x}$):** The exact middle value when data is arranged in ascending order. **Robust against outliers.**
  * *Odd $n$:* Exact middle value located at position $\frac{n+1}{2}$.
  * *Even $n$:* Average of the two middle values located at positions $\frac{n}{2}$ and $\frac{n}{2} + 1$.
* **Mode:** The most frequently occurring value(s) in a dataset.
  * *Unimodal:* 1 mode | *Bimodal:* 2 modes | *Multimodal:* >2 modes | *No Mode:* All values occur with equal frequency.

---

<details>
<summary>👁️ <b>Click to reveal Metric Selection Matrix & Skewness Rules</b></summary>

<br>

### ⚖️ Selection Matrix: When to Use Which Metric?

| Metric | Best Used For | Handles Outliers? | Example |
| :--- | :--- | :---: | :--- |
| **Mean** | Symmetric / Normal continuous data | ❌ No | Test scores, physical heights |
| **Median** | Skewed continuous data or ordinal data | ✅ Yes | Income levels, home values |
| **Mode** | Categorical / Nominal data | ✅ Yes | Most popular color, car brands |

---

### 📊 Shape of Distribution & Skewness

* **Symmetrical (Normal):** $\text{Mean} = \text{Median} = \text{Mode}$
* **Right-Skewed (Positive Skew):** Long tail extends to the right $\rightarrow \text{Mode} < \text{Median} < \text{Mean}$
* **Left-Skewed (Negative Skew):** Long tail extends to the left $\rightarrow \text{Mean} < \text{Median} < \text{Mode}$

</details>

---

## 📏 2. Measures of Dispersion (Spread)

Measures of dispersion describe how spread out or varied data points are relative to the center.

* **Range:** The total distance between the largest and smallest values.
  $$\text{Range} = X_{\text{max}} - X_{\text{min}}$$
* **Variance ($\sigma^2$ or $s^2$):** The average of the squared deviations from the mean.
  * **Population Variance:** $\sigma^2 = \frac{\sum (X_i - \mu)^2}{N}$
  * **Sample Variance:** $s^2 = \frac{\sum (x_i - \bar{x})^2}{n - 1} \quad \text{(Bessel's correction prevents underestimation bias)}$
* **Standard Deviation ($\sigma$ or $s$):** The square root of variance. Restores measurement spread to the **same physical units** as the original data.
  * **Population SD:** $\sigma = \sqrt{\sigma^2}$
  * **Sample SD:** $s = \sqrt{s^2}$

---

<details>
<summary>👁️ <b>Click to reveal Empirical Rule (68-95-99.7) & Coefficient of Variation</b></summary>

<br>

### 🎯 The Empirical Rule (68–95–99.7 Rule)
Applies specifically to symmetric, **bell-shaped (Normal) distributions**:

* $\approx \mathbf{68\%}$ of data falls within $\mu \pm 1\sigma$
* $\approx \mathbf{95\%}$ of data falls within $\mu \pm 2\sigma$
* $\approx \mathbf{99.7\%}$ of data falls within $\mu \pm 3\sigma$

---

### 📐 Coefficient of Variation ($CV$)
Measures relative variability, making it easy to compare spread between datasets with completely different units *(e.g., height in cm vs. weight in kg)*:

$$CV = \left( \frac{s}{\bar{x}} \right) \times 100\%$$

</details>

---

## 📍 3. Measures of Position

Measures of position pinpoint where a specific data value falls relative to the rest of the dataset.

* **Percentiles ($P_k$):** Values that divide a sorted dataset into 100 equal parts ($P_{50}$ is the Median).
* **Quartiles ($Q_1, Q_2, Q_3$):** Values that divide a sorted dataset into 4 equal quarters ($25\%$ of data each).
  * **$Q_1$ (Lower Quartile):** 25th percentile ($P_{25}$).
  * **$Q_2$ (Second Quartile):** 50th percentile ($P_{50}$) = **Median**.
  * **$Q_3$ (Upper Quartile):** 75th percentile ($P_{75}$).
* **Deciles ($D_1 \dots D_9$):** Values that divide data into 10 equal parts ($D_1 = P_{10}, D_5 = P_{50}$).

---

<details>
<summary>👁️ <b>Click to reveal IQR, Outlier Detection & Z-Scores</b></summary>

<br>

### 📦 Interquartile Range ($IQR$) & Outlier Detection

The $IQR$ measures the spread of the middle $50\%$ of data:

$$IQR = Q_3 - Q_1$$

#### The $1.5 \times IQR$ Rule for Outlier Fences:
A data point $x$ is classified as a **potential outlier** if it falls outside these boundaries:
* **Lower Fence:** $Q_1 - 1.5 \times IQR$
* **Upper Fence:** $Q_3 + 1.5 \times IQR$

---

### 🎯 Standardized Position ($Z$-Score)
The $Z$-score measures exact relative position by stating how many standard deviations a raw score $x$ lies above or below the mean:

$$Z = \frac{x - \mu}{\sigma} \quad \text{or} \quad Z = \frac{x - \bar{x}}{s}$$

* $Z = 0 \rightarrow \text{Value equals the mean.}$
* $|Z| > 3 \rightarrow \text{Standard rule-of-thumb threshold for extreme outliers in bell-shaped data.}$

</details>
