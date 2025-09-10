# Week 1

**Date:** 2025-09-08  
**Course:** ST 259  
**Tags:** #week #lecture  

---

## 🧠 Key Concepts

- **Sample Space ($S$):** Set of all possible outcomes  
- **Event:** Subset of sample space  
- **Probability:** $P(E) \in [0, 1]$ where $P(S) = 1$  
- **Set Operations:** Union, Intersection, Difference, Complement  
- **Laws:**
  - **Commutative:** $A \cup B = B \cup A$, $A \cap B = B \cap A$  
  - **Associative:** $(A \cup B) \cup C = A \cup (B \cup C)$  
  - **Distributive:** $(A \cup B) \cap C = (A \cap C) \cup (B \cap C)$  
  - **De Morgan's Laws:**  
    - $(A \cap B)' = A' \cup B'$  
    - $(A \cup B)' = A' \cap B'$  
- **Axioms of Probability:**
  1. **Non-negativity:** $P(E) \geq 0$  
  2. **Certainty:** $P(S) = 1$  
  3. **Countable Additivity:** For disjoint $A_i$, $P\left(\bigcup A_i\right) = \sum P(A_i)$  

---

## 📖 Lecture Summary

### From Calculus
- Derivatives  
- Definite integrals (proper & improper)  
- Power series (geometric progression series)  

### Discrete Mathematics
- Elements of set theory  
- Combinatorics  

### Random Experiment
- Phenomenon where the outcome cannot be predicted  

### Outcome
- Result of an experiment, corresponds to one sample point  

### Sample Space
- Set of all possible outcomes  
- Denoted $S$  

### Event
- Subset of sample space  
- Can be $S$ itself or $\varnothing$  

### Probability
- Assigns a number in $[0,1]$ to an event  
- $P(S) = 1$ (something must happen)  

---

## 🎲 Examples

### Tossing a Coin
- $S = \{H, T\}$  

### Rolling a Die
- $S = \{1, 2, 3, 4, 5, 6\}$  

### Tossing a Coin Three Times
Sample space:

$$
S = \{HHH, HHT, HTH, HTT, THH, THT, TTH, TTT\}, \quad |S|=8
$$

- **A) Only one head:**  
  $A = \{HTT, THT, TTH\}, \quad P(A)=\frac{3}{8}$  

- **B) At most one head:**  
  $B = \{TTT, HTT, THT, TTH\}, \quad P(B)=\frac{4}{8}$  

- **C) At least two heads:**  
  $C = S - B = B^{c} = \{HHT, HTH, THH, HHH\}, \quad P(C)=\frac{4}{8}$  

- **D) No heads:**  
  $D = \{TTT\}, \quad P(D)=\frac{1}{8}$  

---

### Repeated Toss Until First Head
Sample space:  

$$
S = \{H, TH, TTH, TTTH, \dots, T^{n-1}H, \dots\}
$$

Event that coin is tossed exactly $4$ times:  

$$
E = \{TTTH\}
$$

---

## 🔧 Set Operations

- **Intersection:** $A \cap B$ → both occur  
- **Union:** $A \cup B$ → at least one occurs  
- **Difference:** $A - B$ → $A$ occurs but not $B$  
- **Complement:** $A^{c} = S - A$  
- **Subset:** $B \subseteq A \Rightarrow A$ occurs whenever $B$ occurs  
- **Disjoint:** $A \cap B = \varnothing$

---

## 🧮 Example Event Expressions

- $E_1 = A - (B \cup C)$  
- $E_2 = (A \cap B) - C$ → $A$ and $B$ occur but not $C$  
- $E_3 = (A \cap B) \cap C$  
- $E_4 = (A \cup B \cup C)^{c}$  
- Exactly one of $A, B, C$ occurs:  
  $$(A - (B \cup C)) \cup (B - (A \cup C)) \cup (C - (A \cup B))$$  

---

## 🎲 Probability of Die Outcome
Example: Die comes up even:

$$
P(\{2, 4, 6\}) = P_2 + P_4 + P_6 = \frac{1}{6} + \frac{1}{6} + \frac{1}{6} = \frac{1}{2}
$$
