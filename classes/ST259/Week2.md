# {{Week 2}}

Date: {{date:2025-09-15}}  
Course: {{ST 259}}  
Tags: #week2 #lecture3  

---

## 🧠 Key Concepts
- Probability rules: complements, inclusion-exclusion  
- Counting principles: multiplication rule, permutations, ordered vs unordered samples  
- Sampling with and without replacement  
- Probability problems with arrangements  

---

## 📖 Lecture Summary

### Probability Basics
- $P(A' \cup A) = P(A) + P(A') = 1$  
- Can only do $P(A) - P(B)$ when **B is a subset of A**.  
- **Inclusion-Exclusion Formula** applies when sets overlap.  

---

### Example: Ontario Licence Plates
1. **With replacement (letters/digits can repeat)**  
   - Letters: $26^4$  
   - Digits: $10^3 = 1000$  
   - Total: $26^4 \times 1000 = 456{,}976{,}000$  

2. **Without replacement (no repeats)**  
   - $26 \times 25 \times 24 \times 23 \times 10 \times 9 \times 8$  

---

### Ordered vs Unordered Samples
- **Ordered sample**: Order matters.  
  - Example: phone numbers, letters in a word.  
- **Unordered sample**: Order does not matter.  
  - Example: subsets of a set.  

---

### Sampling With/Without Replacement
- **With replacement**: Repetition allowed (e.g., licence plate part a).  
- **Without replacement**: Repetition not allowed (e.g., licence plate part b).  

---

### Examples with a Deck of Cards
- Ordered, with replacement: $52 \times 52$  
- Ordered, without replacement: $52 \times 51$  
- Unordered, without replacement: $\dfrac{52 \times 51}{2}$  
  - Order doesn’t matter (e.g., 2♥ and A♦ is the same as A♦ and 2♥).  

---

### Ordered Sample with Replacement
- Example: Stock price can go **up** or **down** each period.  
- For 3 periods: $2^3 = 8$ possible scenarios.  
- Represented as a **non-recombining binomial tree**.  

---

### Ordered Sample without Replacement
- General case: if $k = n$, then $n!$ arrangements.  

**Example: Letters {a, b, c}**  
- $3! = 6$ arrangements:  
  - abc, acb, bac, bca, cab, cba  

**Example: Set {1, 2, 3, 4}, choose 2**  
- $4!/2! = 12$ permutations  
- Formula: $P(n,k) = \dfrac{n!}{(n-k)!}$  

**Example: 2 letters from {a, b, c, d}**  
- $P(4,2) = \dfrac{4!}{(4-2)!} = \dfrac{24}{2} = 12$  

---

### Probability Example: Friends in a Line
- **Scenario**: 10 people line up randomly. What is the probability that there are exactly 3 people between me and my friend?  

**Steps**:  
1. Total outcomes: $10!$  
2. Place the 2 people with 3 spaces between → 6 possible slots.  
3. Each slot arrangement has 2 orders → $6 \times 2 = 12$ ways.  
4. Arrange the remaining 8 people → $8!$ ways.  
5. Favorable outcomes: $12 \times 8!$  
6. Probability: $\frac{12 \times 8!}{10!} = \frac{12}{10 \times 9} = \frac{2}{15} \approx 13.33\%$
