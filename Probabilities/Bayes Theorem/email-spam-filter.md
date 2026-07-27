# Problem: Email Spam Filter Classification (Bayes' Theorem)

## 📌 Problem Overview

An email filtering gateway uses continuous statistical learning to detect spam messages based on target keywords. Historical data shows:

* **Base Rate of Spam ($P(S)$):** $30\%$ of incoming emails are spam ($0.30$), meaning $70\%$ are legitimate ham ($P(H) = 0.70$).
* **Keyword Occurrence in Spam ($P(K|S)$):** The word *"Urgent"* appears in $60\%$ of spam emails ($0.60$).
* **Keyword Occurrence in Legitimate Email ($P(K|H)$):** The word *"Urgent"* appears in $5\%$ of legitimate emails ($0.05$).

* **Objective:** If a newly arrived email contains the word *"Urgent"*, calculate the posterior probability that the email is actually **spam** ($P(S|K)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Formula

By **Bayes' Theorem**, the posterior probability $P(S|K)$ is given by updating the prior probability $P(S)$ with the likelihood of evidence $K$:

$$P(S|K) = \frac{P(K|S) \cdot P(S)}{P(K)}$$

Where total probability of seeing keyword $K$ is:
$$P(K) = P(K|S) \cdot P(S) + P(K|H) \cdot P(H)$$

---

### 🧮 Step 2: Compute the Probabilities

#### 1. Compute Total Probability of Keyword $P(K)$
$$P(K) = (0.60 \times 0.30) + (0.05 \times 0.70)$$
$$P(K) = 0.18 + 0.035 = 0.215$$

#### 2. Apply Bayes' Formula
$$P(S|K) = \frac{0.18}{0.215} \approx 0.8372 \quad (83.72\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** Given that an incoming email contains the keyword *"Urgent"*, there is an **$83.72\%$** probability that it is spam.

</details>
