# {{Week2}}

Date: {{date:2025-09-11}}
Course: {{CP 421}}
Tags: #week2 #lecture3

---
## 🧠 Key Concepts


## 📖 Lecture Summary
- Step 0: File is stored in HDFS
- Step 1: Map on each node
  - Each server can run on one File
  - for each word in a file generate a key-value
  - job as a map is to create key-values
  - Do for node a b c d
- Step 2: Sort and shuffle
  - Pairs with same key moved to same node
  - Do hashing to bring all similar keys next to each other
    - We can do in parallel
    - All nodes for the reduce that belong to that key will be stored at different nodes
- Step 3: reduce
  - Add values for same key
  - (apple, 1), (apple, 1) >>> (apple, 2)
  - 
- Map >>> Shuffle & Sort >>> Reduce
  - Step 1: Parralezation over the input
  - Step 2: Parralezation over intermediate data
  - Step 3: Parralezation over data groups
- Map Reduce is bad for
  - Frequently changing data
    - 
  - Dependedent tasks
  - Interactive analysis
- 
