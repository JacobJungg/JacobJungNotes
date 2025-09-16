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
  - Dependedent tasks
    - Need to wait for another task before can complete
    - Halts parralel
  - Interactive analysis
    - If two nodes need to interact
- Chunk servers
  - File splits into multiple chunks
  - Typically 16-64mb
  - Each chunk replicated usually 2x or 3x
  - Try to keep replicas in different racks
- Master node
  - Name node
  - Everytime u give input there should be smth that knows where chunks are stored and so on
  - Stores metadata about where files are stored
  - Might be replicated
- Client libary for file access
  - Data node
  - Do the job on the node itself
  - First should know where is the data where is the chunk
  - Then the data does retrieving and storing
  - A map knows that for a program we have a number of nodes where we will do teh map tasks
  - When done store it
  - TAlks to master to find chunk servers
  - Connects directly to chunk server to access data
- YOu can consider each server as a node BUT not each server as a map
  - We map have more than one map on one server or one node
    - Best way to have one map on one server
    - Usually have more than one map on one node or one server
- Case 1: File too large for memory, but all <word, count> pairs fit in memory
  - We dont use
- Case 2:
  - Even th <word, count> pairs dont fit in memory
    - Take a file and output the word count in it, one per a line
    - GReat thing is it naturally parallelizable
    - Case 2 captures esscene of mapreduce
- Map
  - Main task is scan input file record at a time
  - Extract smething you care about from each record (key)
- Group by key
  - Sort and shuffle
- Reduce
  - Aggrergate, summarization, filter or transform
  - Write the resutls
- For any chunk you need a map
- Map worker failure
  - Map tasks completed or in-progress
  - At workers are reset to idle
  - Idle tasks eventually rescheduled on other workers
- Reducer worker failure
  - Only-in progress tasks are reset to idle 
  - Idle reduce tasks restarted on other workers
  - 
