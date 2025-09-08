# {{Week 2}}

Date: {{date:2025-09-08}}  
Course: {{CP372}}  
Tags: #week #lecture  

---

## 🗝 Key Notes
- **Internet Goal:** Enable communication between billions of devices worldwide.
- **Everything is Packets:** Any data generated is a packet; routers forward them across networks.
- **Two Communication Links:** Wired (Ethernet) & Wireless (Radio spectrum).
- **Routing vs Forwarding:**
  - **Routing:** Selects best path from source → destination.
  - **Forwarding:** Chooses correct outgoing link inside a router.
- **5-Layer Architecture:**  
  1. **Physical** – transmission medium  
  2. **Data Link** – node-to-node, error control, MAC  
  3. **Network** – IP addressing, routing, forwarding  
  4. **Transport** – end-to-end delivery, port numbers  
  5. **Application** – user-level services (web, email, games)
- **Devices & Layers:**
  - End Node → all 5 layers  
  - Switch → Data Link + Physical layers  
  - Router → Network + Data Link + Physical layers

---

## 📖 Lecture Summary

### 🌐 Internet Overview
- **Mobile Networks:** every phone connects to cell service.
- **ISPs:**
  - Local or Regional ISP  
  - National or Global ISP
- **Who Uses the Internet?**
  - Hosts and users (main components)
  - Communication from **source node** → **destination node**

---

### 🔗 Communication Links
- **Wired:** Ethernet, physical connection.
- **Wireless:** Radio spectrum, frequency-based communication.  
  - Most important component = Radio  
  - Devices use different frequencies to avoid interference  

---

### 📦 Packets & Packet Switching
- Any data generated = **packet**
- Packet = information + header data
- Packets must travel via **packet switching**
  - Requires switches or routers to forward packets from one node to another

---

### 🎯 Internet Goals & Design Challenges
- Connect billions of devices globally
- Complex architecture but runs smoothly
- **Analogy:** Like mail services  
  - Mailbox = Router  
  - Address = IP Address (unique for every device/host)

---

### 🛠 Key Internet Functions
| Function | Description |
|---------|-------------|
| **Application Identification** | Identify which application generated data (e.g., web, email) |
| **Process Identification** | Identify process within device (application ID) |
| **Routing** | Determine best path for packet to reach destination |
| **Forwarding** | Choose correct outgoing link at router |
| **Segmentation** | Break large files into small segments (1, 2, 3...) |
| **Error Control** | Detect & handle lost/out-of-order segments (e.g., 1,3,2,4) |
| **Medium Access Control** | Handle multiple devices sharing medium (avoid collisions) |
| **Physical Connectivity** | Determine physical link setup between devices |
| **Data Conversion** | Convert digital data → signals for transmission |
| **Security** | Ensure safe communication, optional connection setup |

---

### 🛰 Medium Access Control (MAC)
- Multiple devices sending simultaneously → collisions  
- If collision occurs, receivers can’t listen  
- MAC protocols coordinate so devices don’t interrupt each other  
- Important for **wireless communication** where radio frequencies are limited

---

### 🏗 5-Layer Architecture (Layer Model)
1. **Application Layer**  
   - End-user services: web browsing, gaming, email, file transfer
2. **Transport Layer**  
   - End-to-end packet transfer  
   - Port numbers = like a "person’s name" identifying application
3. **Network Layer**  
   - IP address = "home address" identifying device  
   - Routing and forwarding
4. **Data Link Layer**  
   - Node-to-node communication  
   - Error control + medium access control
5. **Physical Layer**  
   - Actual physical transmission of bits

---

### 📡 TCP/IP Architecture
- **TCP (Transmission Control Protocol):** reliable transport layer protocol
- Internet architecture is **based on postal service model**
- End node has all 5 layers, router has 3 (network, link, physical), switch has 2 (link, physical)

---

### 📚 Chapter Coverage
- Covers **Ch. 1.1 – 1.3**

---

## 🧠 Key Concepts
- Packets, packet switching, routing vs forwarding
- IP addressing and process identification
- Error control, segmentation, MAC protocols
- 5-layer network model (Application → Physical)
- TCP/IP model parallels postal service

---

## 📝 Side Notes
- Lecturer compared internet to mail services ("back in my day" story)
- Mentioned reliability, error control, collisions
- Skipped several slides — might need to revisit textbook/YouTube to clarify 5-layer model
- “Okay she is screaming she is very passionate about this”
- Stopped paying attention near the end
