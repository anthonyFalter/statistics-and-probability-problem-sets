# 🎲 Introduction to Probability Reference Guide

A fundamental cheat sheet covering core probability principles, key terms, set operations, rules of probability, and common theoretical distributions.

---

## 📌 1. Core Terminology & Definitions

* **Experiment:** Any repeatable process, action, or trial that yields an uncertain outcome *(e.g., tossing a coin, measuring delivery time)*.
* **Outcome:** A single, specific result obtained from performing a random experiment *(e.g., getting a "Heads")*.
* **Sample Space ($S$ or $\Omega$):** The complete set containing all possible outcomes of an experiment *(e.g., $S = \{1, 2, 3, 4, 5, 6\}$ for a 6-sided die)*.
* **Event ($A, B$):** A specific outcome or collection of outcomes from the sample space that you are interested in measuring *(e.g., rolling an even number)*.
* **Probability ($P(A)$):** A numerical value constrained between $0$ and $1$ representing the likelihood or chance that event $A$ will occur.
* **Equally Likely Outcomes:** A condition where every outcome in the sample space has the exact same chance of occurring *(e.g., a fair coin or die)*.

---

## 📐 2. The Three Axioms of Probability (Kolmogorov)

The mathematical rules that govern all valid probability systems:

1. **Non-Negativity:** $P(A) \ge 0$ for every event $A$.
   * *Description:* A probability can never be negative.
2. **Normalization:** $P(S) = 1$.
   * *Description:* The combined probability of all possible outcomes in the entire sample space always equals $100\%$ ($1.0$).
3. **Additivity:** For any mutually exclusive events $A_1, A_2, A_3, \dots$:
   $$P(A_1 \cup A_2 \dots) = \sum P(A_i)$$
   * *Description:* The probability of any of multiple non-overlapping events occurring is simply the sum of their individual probabilities.

---

## 🛠️ 3. Fundamental Rules of Probability

<details>
<summary>👁️ <b>Click to reveal Core Probability Rules & Key Term Descriptions</b></summary>

<br>

### 1. Complement Rule
* **Complement ($A'$ or $A^c$):** The event that $A$ does **not** happen.
$$P(A') = 1 - P(A)$$

---

### 2. Addition Rule (Union - "OR")
* **Union ($A \cup B$):** The event that event $A$, event $B$, or **both** occur.
$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

> **Mutually Exclusive (Disjoint) Events:** Two events that cannot occur at the same time ($P(A \cap B) = 0$).
> * *Formula:* $P(A \cup B) = P(A) + P(B)$

---

### 3. Multiplication Rule (Intersection - "AND")
* **Intersection ($A \cap B$):** The event that **both** $A$ and $B$ occur simultaneously.
$$P(A \cap B) = P(A) \cdot P(B \mid A)$$

> **Independent Events:** Two events where the occurrence of one provides zero information about the likelihood of the other.
> * *Formula:* $P(A \cap B) = P(A) \cdot P(B)$

---

### 4. Conditional Probability
* **Conditional Probability ($P(A \mid B)$):** The updated probability of event $A$ occurring, given the known condition that event $B$ has already occurred.
$$P(A \mid B) = \frac{P(A \cap B)}{P(B)} \quad \text{where } P(B) > 0$$

---

### 5. Law of Total Probability & Bayes' Theorem
* **Partition:** Dividing a sample space into mutually exclusive subsets $B_1, B_2, \dots$ that together cover the entire sample space.
* **Prior Probability ($P(B)$):** The original estimate of an event's probability before observing new evidence.
* **Posterior Probability ($P(B \mid A)$):** The updated probability of an event after accounting for new evidence $A$.

* **Law of Total Probability:**
  $$P(A) = \sum_{i=1}^{k} P(A \mid B_i) \cdot P(B_i)$$

* **Bayes' Theorem:**
  $$P(B_i \mid A) = \frac{P(A \mid B_i) \cdot P(B_i)}{\sum P(A \mid B_j) \cdot P(B_j)}$$

</details>

---

## 🎯 4. Counting Principles (Combinatorics)

<details>
<summary>👁️ <b>Click to reveal Permutations & Combinations Definitions</b></summary>

<br>

Used to count possible outcomes when calculating classical probabilities ($P(A) = \frac{\text{favorable outcomes}}{\text{total outcomes}}$):

* **Fundamental Counting Principle:** If event 1 can happen in $m$ ways and event 2 in $n$ ways, both together can happen in $m \times n$ ways.
* **Factorial ($n!$):** The product of all positive integers less than or equal to $n$ *(e.g., $4! = 4 \times 3 \times 2 \times 1 = 24$)*.
* **Permutations ($P(n, r)$):** An arrangement of $r$ objects selected from $n$ distinct objects **where sequence/order matters**.
  $$P(n, r) = \frac{n!}{(n - r)!}$$
* **Combinations ($C(n, r)$):** A selection of $r$ objects from $n$ distinct objects **where sequence/order DOES NOT matter**.
  $$C(n, r) = \binom{n}{r} = \frac{n!}{r!(n - r)!}$$

</details>

---

## 📊 5. Random Variables & Common Distributions

<details>
<summary>👁️ <b>Click to reveal Random Variables & Distribution Descriptions</b></summary>

<br>

### 🔹 Core Concepts
* **Random Variable ($X$):** A variable whose numeric value is determined by the outcome of a random phenomenon.
* **Expected Value ($E[X]$ or $\mu$):** The long-run average or mean value of a random variable across infinite repeated trials.
* **Probability Mass Function (PMF):** A function that gives the exact probability that a *discrete* random variable equals a specific value $x$.
* **Probability Density Function (PDF):** A function that describes the relative likelihood for a *continuous* random variable to fall within a specific range of values.

---

### 🔹 Discrete Distributions (Countable Outcomes)

1. **Binomial Distribution ($X \sim \text{Binom}(n, p)$):**
   * *Description:* Models the number of successes in $n$ independent trials, where each trial has a constant success probability $p$.
   * *Formula:* $P(X = k) = \binom{n}{k} p^k (1 - p)^{n-k}$
   * *Mean:* $E[X] = np$

2. **Poisson Distribution ($X \sim \text{Poisson}(\lambda)$):**
   * *Description:* Models the count of rare events occurring within a fixed interval of time or space at a constant average rate $\lambda$.
   * *Formula:* $P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$
   * *Mean & Variance:* $E[X] = Var(X) = \lambda$

---

### 🔸 Continuous Distributions (Uncountable Outcomes)

1. **Uniform Distribution ($X \sim U(a, b)$):**
   * *Description:* Models continuous outcomes where every interval of equal length between minimum $a$ and maximum $b$ is equally likely.
   * *Density:* $f(x) = \frac{1}{b - a}$

2. **Normal (Gaussian) Distribution ($X \sim N(\mu, \sigma^2)$):**
   * *Description:* The classic symmetric, bell-shaped distribution centered around mean $\mu$ with standard deviation $\sigma$.
   * *Standard Normal ($Z$):* A normal distribution standardized to have $\mu = 0$ and $\sigma = 1$ using $Z = \frac{X - \mu}{\sigma}$.

</details>

## 🧠 6. Deep Dive: Bayes' Theorem & Conditional Reasoning

Bayes' Theorem provides a mathematical framework for updating our belief in a hypothesis ($H$) as we collect new evidence ($E$).

---

### 📌 Key Terms & Terminology

* **Hypothesis ($H$):** The underlying condition or state of nature you are testing *(e.g., Patient has a disease, Email is spam)*.
* **Evidence ($E$):** The observed data or diagnostic test result *(e.g., Positive lab test, Email contains the word "FREE")*.
* **Prior Probability ($P(H)$):** The initial probability of the hypothesis **before** seeing new evidence *(e.g., Disease prevalence in the general population)*.
* **Posterior Probability ($P(H \mid E)$):** The updated probability of the hypothesis **after** observing evidence $E$.
* **Likelihood ($P(E \mid H)$):** The probability that the evidence would occur given that the hypothesis is true.
* **Marginal / Total Likelihood ($P(E)$):** The overall probability of observing the evidence across all possible hypotheses.
* **False Positive Rate (Type I Error):** Probability of the test returning positive when the hypothesis is actually false ($P(E \mid H')$).
* **False Negative Rate (Type II Error):** Probability of the test returning negative when the hypothesis is actually true ($P(E' \mid H)$).

---

<details>
<summary>👁️ <b>Click to reveal Bayes' Theorem Formulas & Step-by-Step Breakdown</b></summary>

<br>

### 🧮 1. Master Bayes' Theorem Formula

$$P(H \mid E) = \frac{P(E \mid H) \cdot P(H)}{P(E)}$$

Where the denominator $P(E)$ is expanded using the **Law of Total Probability**:

$$P(E) = P(E \mid H) \cdot P(H) + P(E \mid H') \cdot P(H')$$

* **Complete Expanded Formula:**
  $$P(H \mid E) = \frac{P(E \mid H) \cdot P(H)}{P(E \mid H) \cdot P(H) + P(E \mid H') \cdot P(H')}$$

---

### 📝 2. Classic Problem Example: Medical Diagnostic Testing

> **Scenario:** A rare disease affects **$1\%$** of the population. A test for the disease is **$95\%$ accurate** for true positives ($P(\text{Pos} \mid \text{Sick}) = 0.95$) and has a **$5\%$ false positive rate** ($P(\text{Pos} \mid \text{Healthy}) = 0.05$). If a patient tests positive, what is the probability they actually have the disease?

1. **Identify the Given Values:**
   * **Prior $P(\text{Sick})$:** $0.01$
   * **Prior $P(\text{Healthy})$:** $1 - 0.01 = 0.99$
   * **Likelihood $P(\text{Pos} \mid \text{Sick})$:** $0.95$
   * **False Positive $P(\text{Pos} \mid \text{Healthy})$:** $0.05$

2. **Calculate Total Likelihood of Testing Positive $P(\text{Pos})$:**
   $$P(\text{Pos}) = (0.95 \times 0.01) + (0.05 \times 0.99) = 0.0095 + 0.0495 = 0.0590$$

3. **Calculate Posterior Probability $P(\text{Sick} \mid \text{Pos})$:**
   $$P(\text{Sick} \mid \text{Pos}) = \frac{0.0095}{0.0590} \approx 0.1610 \quad (16.1\%)$$

* **Insight:** Even with a $95\%$ accurate test, the chance of actually having the disease after one positive test is only $16.1\%$ because the disease itself is extremely rare (base rate fallacy)!

---

### 🤖 3. Machine Learning Application: Naive Bayes Classifier

In Data Science, the **Naive Bayes algorithm** uses Bayes' Theorem to classify multi-feature data ($X_1, X_2, \dots, X_n$) into classes ($y$):

$$P(y \mid X_1, \dots, X_n) \propto P(y) \prod_{i=1}^{n} P(X_i \mid y)$$

* **Why is it called "Naive"?**
  It naively assumes that all input features ($X_1, X_2, \dots$) are **statistically independent** of each other given the class outcome $y$. While rarely 100% true in real life, this assumption drastically simplifies calculation speeds while producing surprisingly high model accuracy!

</details>
