# Week 2

Date: 2025-09-11  
Course: CP 421  
Tags: #week2 #lecture3

---

## 🧠 Key Concepts

* MapReduce paradigm
* HDFS architecture
* Fault tolerance in distributed systems

## 📖 Lecture Summary

- **Step 0:** File is stored in HDFS
- **Step 1:** Map on each node
  - Each server can process one file
  - For each word in a file, generate a key-value pair
  - The job of the map phase is to create key-value pairs
  - Performed on nodes a, b, c, d
- **Step 2:** Sort and shuffle
  - Pairs with the same key are moved to the same node
  - Hashing is used to bring all similar keys together
    - Can be done in parallel
    - All nodes for the reduce phase that belong to a key will be stored at different nodes
- **Step 3:** Reduce
  - Aggregate values for the same key
  - Example: (apple, 1), (apple, 1) → (apple, 2)

- **Map → Shuffle & Sort → Reduce**
  - Step 1: Parallelization over the input
  - Step 2: Parallelization over intermediate data
  - Step 3: Parallelization over data groups

- **MapReduce is not ideal for:**
  - Frequently changing data
  - Dependent tasks (need to wait for another task before completion, halts parallelism)
  - Interactive analysis (if two nodes need to interact)

- **Chunk servers:**
  - File splits into multiple chunks (typically 16–64 MB)
  - Each chunk is replicated, usually 2x or 3x
  - Replicas are kept in different racks for fault tolerance

- **Master node:**
  - Also called the NameNode
  - Stores metadata about where files/chunks are stored
  - May be replicated for reliability

- **Client library for file access:**
  - DataNode does the job on the node itself
  - First, locate the data/chunk
  - Then, retrieve and store data
  - Map tasks are distributed across nodes
  - Talks to master to find chunk servers
  - Connects directly to chunk server to access data

- **Server vs. Map:**
  - Each server is a node, but not every server runs a map task
  - There may be more than one map task per server/node
  - Ideally, one map per server, but usually more

- **Case 1:** File too large for memory, but all `<word, count>` pairs fit in memory
  - Not commonly used

- **Case 2:** Even the `<word, count>` pairs don't fit in memory
  - Take a file and output the word count, one per line
  - Naturally parallelizable
  - This case captures the essence of MapReduce

- **Map phase:**
  - Main task is to scan the input file record by record
  - Extract something you care about from each record (the key)

- **Group by key:**
  - Sort and shuffle

- **Reduce phase:**
  - Aggregate, summarize, filter, or transform
  - Write the results

- For any chunk, you need a map task

- **Map worker failure:**
  - Map tasks completed or in-progress at failed workers are reset to idle
  - Idle tasks are eventually rescheduled on other workers

- **Reducer worker failure:**
  - Only in-progress tasks are reset to idle
  - Idle reduce tasks are restarted on other
