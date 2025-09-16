# {{Week 3}}

Date: {{date:2025-09-16}}  
Course: {{CP 386}}  
Tags: #week #lecture5  

---

## 🧠 Key Concepts
- File descriptors
- Standard input, output, and error
- File descriptor table
- `fork()` and file descriptor inheritance

---

## 📖 Lecture Summary
- **Example process with open files**  
  - File descriptor **0**  
    - Description: Standard input  
    - Associated file: Keyboard input  
  - File descriptor **1**  
    - Description: Standard output  
    - Associated file: Console output  
  - File descriptor **2**  
    - Description: Standard error  
    - Associated file: Console error  
  - File descriptor **3**  
    - Description: File  
    - Associated file: `file.txt`  
  - File descriptor **4**  
    - Description: File  
    - Associated file: `log.txt`  

- **File descriptor**  
  - An integer that represents a file, path, or device.  
  - A process uses it to open files or directories.  
  - Each process has its own file descriptor table.  

- **`fork()`**  
  - Creates a new process.  
  - The child process inherits a copy of the parent’s file descriptor table.  
