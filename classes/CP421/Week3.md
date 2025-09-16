# Week 3

Date: 2025-09-16  
Course: CP 421  
Tags: #week3 #lecture4

---

## 🧠 Key Concepts

* Join operations in MapReduce
* Matrix multiplication in MapReduce

## 📖 Lecture Summary

### Algorithms in MapReduce

- **Join operation in MapReduce:**
  - Joins are performed on foreign keys, similar to SQL.
  - Large tables cannot be loaded entirely into memory.
  - Both tables are divided into files.
  - Key-value pairs are created as a map task.
  - Summarization is done in the reducer.
  - The reducer receives key-value pairs.
  - Values sent to the reducer are the remaining elements of the tuple.
    - Indicate to the reducer which row and table each value belongs to.
    - Reducer might process two tuples from the same table, which is not desired.
  - The goal is to have (key, value) pairs in the mapper, making the reducer simple.
  - The key is an element from any row of any table that is similar (e.g., value B).
    - Example: (b1, <a1, R>)
      - b1 is the key.
      - <a1, R> is the value, where a1 is a column and R is the table.
    - All these pairs are sent to the reducer.
    - When the reducer sees similar keys but different values, it can perform the join.

- **Matrix multiplication in MapReduce:**
  - May involve a chain of matrices.
  - Matrices may not fit into memory.
  -
