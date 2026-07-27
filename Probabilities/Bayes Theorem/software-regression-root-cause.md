# Problem: Software Regression Root Cause Attribution (Bayes' Theorem)

## 📌 Problem Overview

A production incident team is investigating a database latency spike. The backend pipeline routes queries through two primary service modules: **Module A** (Legacy Query Engine) and **Module B** (New Cache Engine). 

* **Module Traffic Allocation:** $60\%$ of incoming traffic goes to Module A ($P(M_A) = 0.60$), and $40\%$ goes to Module B ($P(M_B) = 0.40$).
* **Failure Rate in Module A ($P(F|M_A)$):** $5\%$ of requests routed to Module A experience a latency failure ($0.05$).
* **Failure Rate in Module B ($P(F|M_B)$):** $1\%$ of requests routed to Module B experience a latency failure ($0.01$).

* **Objective:** If a randomly logged query experiences a latency failure ($F$), calculate the probability that the failure originated from **Module A** ($P(M_A|F)$).

---

<details>
<summary>👁️ <b>Click to reveal the Formula, Step-by-Step Calculation, and Solution</b></summary>

<br>

### 🎯 Step 1: Identify the Formula

By **Bayes' Theorem**, the posterior probability that Module A caused the recorded failure $P(M_A|F)$ is:

$$P(M_A|F) = \frac{P(F|M_A) \cdot P(M_A)}{P(F)}$$

Where the total probability of experiencing a latency failure $P(F)$ across all modules is:
$$P(F) = P(F|M_A) \cdot P(M_A) + P(F|M_B) \cdot P(M_B)$$

---

### 🧮 Step 2: Compute the Probabilities

#### 1. Compute Total Failure Probability $P(F)$
$$P(F) = (0.05 \times 0.60) + (0.01 \times 0.40)$$
$$P(F) = 0.030 + 0.004 = 0.034$$

#### 2. Apply Bayes' Formula
$$P(M_A|F) = \frac{0.030}{0.034} \approx 0.8824 \quad (88.24\%)$$

---

### 📝 Step 3: Final Conclusion

* **Result:** Given that a database request suffers a latency failure, there is an **$88.24\%$** probability that the issue originated from **Module A**.

</details>
