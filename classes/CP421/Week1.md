# Week 1

**Date:** 2025-09-09  
**Course:** CP 421  
**Tags:** #week #lecture  

---

## 📖 Lecture Summary

### 📥 Acquire Data
- Identify datasets  
- Retrieve data from sources  
- Query data for relevant attributes  

### 🧹 Prepare Data
- **Explore**
  - Understand nature of data (data types, ranges)
  - Preliminary analysis and descriptive statistics
  - Detect correlations, trends, and distributions
  - Identify duplicate columns and attributes
- **Pre-process**
  - **Clean**
    - Remove outliers  
    - Handle null values  
    - Remove or impute incomplete rows  
  - **Integrate** data from multiple sources  
  - **Package** for modeling  
  - Handle missing data intelligently (merge duplicates, decide on imputation strategy)
  - **Feature Selection** (choose most relevant attributes)
  - **Dimensionality Reduction** (e.g., project 3D → 2D using PCA)

### 📊 Analyze Data
- **Select Analytical Techniques**
  - **Classification** – predict category membership  
  - **Clustering** – group similar items together  
  - **Regression** – predict numerical values  
  - **Association Analysis** – find relationships (e.g., market basket analysis)  
  - **Graph Analytics** – find connections between entities (social networks, link analysis)
- **Build Models**
  - Select technique → Build model → Validate model  

### 🗣 Communicate Results
- Data-driven storytelling  
- Decide **what** to report and **how** to present it effectively  

### 🔁 Apply Results
- Recommend next steps  
- Identify future opportunities  
- Revisit process if necessary  
- Determine whether results are favorable  

### ❓ What is Data Mining?
- **Definition:** Knowledge discovery from large volumes of data  
- **Goal:** Discover patterns and models that are:
  - **Valid** – Generalize to new data  
  - **Useful** – Actionable and relevant  
  - **Unexpected** – Non-obvious insights  
  - **Understandable** – Interpretable by humans  

---

## 🖥 Slide Two: Big Data & Distributed Systems

### Distributed File Systems (DFS)
- **HDFS** (Hadoop Distributed File System)
  - Long-term information storage
  - Enables **parallel processing**
  - Provides access for multiple processes simultaneously  
- **Key Features**
  - Data partitioning & replication  
  - Fault tolerance (replicate chunks on different racks)
  - High concurrency  
  - Scalability (handle growing datasets)  
- **Example:** Google indexing 20B+ web pages (~400TB) and searching them in milliseconds

### Architectures
- **Single Node**
  - CPU + Memory in a single machine
  - Data stored on disk → loaded into memory → processed locally
  - Classical data mining approach (no distributed/cloud setup)

- **Cluster Architecture**
  - Multiple nodes connected via network switches
  - Data chunks stored across nodes
  - Reduces bottlenecks with parallel data transfer
  - Foundation of modern big data systems  

- **Commodity Clusters**
  - Distributed computing over inexpensive hardware
  - Enables data parallelism and lowers cost
  - Brings computation close to the data (reduces network traffic)

### Fault Tolerance
- **Common Failures**
  - Node failure
  - Link failure (between node and rack)
  - Rack failure
  - Two-node connection failure  
- **Recovery**
  - No need for full restart  
  - Use redundant data storage & restart only failed jobs

### Programming on DFS
- Split volumes of data  
- Distribute computations to nodes  
- Access and process data quickly at scale  

---

## 🧠 Key Concepts

- Data Mining Process: Acquire → Prepare → Analyze → Communicate → Apply  
- Data Cleaning & Integration Techniques  
- Feature Selection & Dimensionality Reduction  
- Classification, Clustering, Regression, Association, and Graph Analytics  
- Distributed File Systems (HDFS), Data Partitioning & Replication  
- Single Node vs. Cluster Architecture  
- Fault Tolerance & Redundancy in Big Data Systems  
- Bringing Computation to Data (Data Parallelism)

---

## 📝 Notes

Write additional examples here (e.g., PCA use case, association rules in retail).
