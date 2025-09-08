# {{Week 1}}

Date: {{date:2025-09-08}}  
Course: {{ST 259}}  
Tags: #week #lecture  

---

## 📖 Lecture Summary

- **From Calculus**
  - Derivatives
  - Definite integrals (proper and improper)
  - Power series (geometric progression series)

- **Discrete Maths**
  - Elements of set theory and combinatorics

- **Random Experiment**
  - Phenomenon where outcome cannot be predicted

- **Outcome**
  - Result of experiment described by one and only one sample point

- **Sample Space**
  - Set of all possible outcomes of experiment  
  - Denoted by letter $S$

- **Event**
  - Subset of sample space  
  - Any part of the set (including $S$ itself and $\varnothing$)

- **Probability**
  - Number between $0$ and $1$ assigned to an event  
  - $P(S) = 1$ (something must happen for sure)

- **Examples**
  - **Tossing a coin**  
    $S = \{H, T\}$
  - **Rolling a die**  
    $S = \{1, 2, 3, 4, 5, 6\}$
  - **Human life (age in years)**  
    $S = \{1, 2, 3, \dots\}$ (countably infinite)
  - **Measurement of human height**  
    $S = \mathbb{R}^{+}$
  - **Locating a place on Earth**  
    $S \subseteq \mathbb{R}^{2}$ (longitude, latitude)

---

### Example: Tossing a Coin Three Times

- Sample space:

$$
S = \{HHH, HHT, HTH, HTT, THH, THT, TTH, TTT\}, \quad |S| = 8
$$

- **A) Only one head appears**

$$
A = \{HTT, THT, TTH\}, \quad P(A) = \frac{3}{8}
$$

- **B) At most one head appears**

$$
B = A \cup D = \{TTT, HTT, THT, TTH\}, \quad P(B) = \frac{4}{8}
$$

- **C) At least two heads appear**

$$
C = S - B = B^{c} = \{HHT, HTH, THH, HHH\}, \quad P(C) = \frac{4}{8}
$$

- **D) No heads appear**

$$
D = \{TTT\} \subset S, \quad P(D) = \frac{1}{8}
$$

---

### Repeated Toss Until First Head

- Sample space:

$$
S = \{H, TH, TTH, TTTH, \dots, T^{n-1}H, \dots\}
$$

- Event that coin is tossed exactly 4 times:

$$
E = \{TTTH\}
$$

---

### Set Operations

- **Intersection:**  
  $A \cap B$ = elements common to $A$ and $B$ (both events occur)

- **Union:**  
  $A \cup B$ = elements in $A$, $B$, or both (at least one occurs)

- **Difference:**  
  $A - B = \{x \in A \mid x \notin B\}$ (A occurs but not B)

- **Complement:**  
  $A^{c} = S - A$ (A does not occur)

- **Subset Relation:**  
  $B \subseteq A \implies A$ occurs whenever $B$ occurs

- **Disjoint Events:**  
  $A \cap B = \varnothing \quad \Rightarr
