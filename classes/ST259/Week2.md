# {{Week 2}}

Date: {{date:2025-09-15}}
Course: {{ST 259}}
Tags: #week2 #lecture3

---
## 🧠 Key Concepts
- 

## 📖 Lecture Summary
- P(A' U A) = P(A) + P(A') = 1
- Can only do P(A) - P(B), when B is subset of A
- Inclusion Exclusion formula
- A licence plate number in Ontario consists of four letters followed by three digits.
  - n1 = 26^4 letters
  - n2 = 10 * 10 * 10 = 1000
  - n1 * n2
  - = 456, 976, 000
  - (b) How many distinct licence plates are possible if no digit or letter can occur twice?
    - L1 L2 L3 L4 D1 D2 D3
    - 26 * 25 * 24 * 23 * 10 * 9 * 8
- Permutation
  - Arrangments in some order
- ORdered versus unorderd sample
  - Ordered all elements in the sample have a distinct order
  - Phpne numberletters in a word
  - Unordered order is irrelevent
    - Elements in a subset
- Sample with replacement
  - Repetition of same elemnt is allwoed
    - Numbers in a linscence plate (part a)
- WIthout replacement
  - Repetition not allowed, licesnse plate (part b)
- Examples: pick two cards from a deck
  - Ordered sample with replacement
    - 52x52
  - Ordered sample without replacement
    - 52x51
  - Unordered sample without replacement
    - 52x51/2
    - Does not matter which odrder u pull cards in
    - Mush together two outcomes
    - If you pull a 2 of hearts and a ace of diamonds, its same as ace of diamonds and 2 of hearts
## Order sample with replacement
- In each period, the stock price my go up or down. List all possible scenarios for three periods. Illustrate them using a non-recombining binomial tree.
  - n = 2 {up, down}
  - k = 3 (3 periods)
  - n^k = 2^3 = 8
## Ordered sample without replacement
- k = n
  - n factorial
  - list all possible arrangments of letters a, b, C
    - n = 3
    - k = 3
      - Thinkin gof arrangments
    - n! = 3! = 3 * 2 * 1 = 6
    - abc
    - acb
    - cab
    - cba
    - bac
    - bca
- Consider a set {1,2,3,4}
  - Permutaion us nonrepeating list ex. 4132
  - 1124 is not Permutaion
  - now imagine chosing only 2 like 41, 32, 13
  - By multiplication rule
  - 12 = 4*3 = 4!/2!
- 1 <= k <= n
  - an ordered arrangment of a set of objects is a Permutaion
  - n(n-1)(n-2) ... (n - k + 1)
  - = n!/(n-k)!
- List all possible permuations of 2 letters from a,b,c,d
  - 4!/(4-2)!
  - 24/2
  - 12
- Ten people, including myself and a friend, randomly arrange ourselves in a line. How likely is it that there are exactly three people between me and my friend?
  - n = 10
  - k = 10
  - n! = 10! = outcomes
  - 10 positions
  - Place the 2 people 3 slots apart
    - 6 spots to work with that allow for three people in bweteen
    - 6 spots time 2 reservations
    - 6 * 2
    - engineer outcome where u have three peopel in between
  - Arrange the 8 people
    - 8!
  - 12 * 8!
  - but what is probability?
  - Assumptions, all accounts are equally rightful
  - 12 * 8! / 10!
  - 12 * 8! / 10 * 9 * 8!
  - 12 / 10 * 9
  - 12 / 90
  - 2/15
  - 13.13%
- 
