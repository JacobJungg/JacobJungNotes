# {{Week 2}}

Date: {{date:2025-09-11}}
Course: {{CP 386}}
Tags: #week #lecture

---
## 🧠 Key Concepts
- 

## 📖 Lecture Summary
- fork()
  - create a Child process
  - Allocate seperate memory space for process
  - Same memory contents as parents
  - Process has its own registers
    - Program counter regiaster
    - PC
  - New process independent after createrd
  - For parent, returns Processing id (PID)
  - For child, returns 0
- wait()
  - when child process is created, located in parent process
  - parent and child not have dependency
  - applocation may want to enfore order in which they are executed
  - Parent exits only after child finishes
  - stalls parent class to WAIT until child class is finisehd running
- exec()
  - run a program different from the caller itself
    - Launch an editor
    - % echo "hello"
  - OS needs to load code (and static data) from excecutable
  - Overwrites current code segment (and current static data)
  - Initalize a new stack, initalize a new heap for new program
  - 2 parameters
    - Name of binary file
    - Array of arguments
  - when called
    - Repalce contents of memory with new memory contents
      - From binary file being excecuted
    - Does not returns
      - Starts execute the new program
    - 
