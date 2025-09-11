# {{Week 2}}

Date: {{date:2025-09-11}}  
Course: {{CP 386}}  
Tags: #week2 #lecture3  

---

## 🧠 Key Concepts
- **fork()** – process creation, separate memory space, returns different values in parent vs. child  
- **wait()** – parent process waits for child to finish before continuing  
- **exec()** – replaces current process image with a new program, does not return  

---

## 📖 Lecture Summary

### 🟢 fork()
- Creates a **child process** from the parent process.
- Allocates **separate memory space** but copies parent’s memory contents.
- Child process has its own **registers** (including Program Counter).
- After creation, the child process is **independent**.
- **Return values:**
  - Parent receives **PID** (process ID) of the child.
  - Child receives **0**.

### 🟢 wait()
- Makes the **parent process wait** until the child finishes execution.
- Used to **enforce execution order** between parent and child.
- Without `wait()`, parent and child run **concurrently** and independently.
- Commonly used to **synchronize** parent’s exit with child completion.

### 🟢 exec()
- **Replaces** the current process image with a new program.
- Loads code and static data from an **executable file**.
- **Overwrites** current code segment and static data.
- **Initializes** a new stack and heap for the new program.
- **Parameters:**
  - Binary file name.
  - Array of arguments.
- **Behavior:**
  - Replaces memory contents with the new program.
  - **Does not return** – the current process becomes the new program.

---

## ✏️ Key Notes
- `fork()` + `exec()` are often used **together**:  
  1. `fork()` creates a child.  
  2. Child uses `exec()` to run a new program.  
- `wait()` ensures **deterministic order** by stalling the parent until the child completes.
- Together, these calls form the foundation for **process creation and program execution** in UNIX-like systems.
