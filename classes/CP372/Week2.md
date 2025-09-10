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


- Node to node layer
  - IP Addressing
    - Routing
    - Forwarding
  - Data Link Layer
    - Node to node
    - version of transport layer
      - Error control
      - Medeium access control
  - Physical layer
    - Line coding
    - Modulation
- Look into encapsulation and decapsulation



## Packet Switch
- In network layer they support two protocols
- Connection oriented and connection less
  - Connectionless is datagram
  - Connection is packet
- Segmentation, divide
  - When reach destination combine everything
- Assembly and reassembly process
  - Send one message
  - Segment into multiple packets
  - Each packet is stored at each node
  - Forwarded to the next until destination
  - Recieve the packet
  - Reassemble
  - Recieve the message
- PSTN
  - Public switch telephone network
  - Circuit establishmetn
  - Data transfer
  - Circuit disconnect
- Circuit switching vs packet switch
  - Circuit was originally to handle voice traffic but also digital data, this was inefficent
  - Inefficent Connectionless
  - Channel capacity dedicated for duration of connection
    - Even if no data being transfered
  - Even for voice utilization is high but not 100% (idk what 100% means)
  - Data connection (client server) capacity idle during most of connection
  - Circuit does not accept bursty traffic
    - Calls can be blocked
    - In packet swithcing it still accepts but deilvery delay increases
  - Packet supports fairness of packets 
    - Fairness to user
  - PAcket switch has delay
    - aloways looking for faster Speed
    - to minimize delay
    - Queing delay
      - Packets arrivie at a busy link, must queue up
      - Wait their turn
      - before being sent to link
    - Packet loss
      - If queue is full packet is dropped
    - These two only happen if links are not reserved
    - PAcket processing delay
      - EAch packet must have a destination address
      - EAch router must check to direct it to suitable next router
    - Packet transmission delay
      - PAcket must be fully placed at link for transmission
    - Transmission delay
      - Time taken to put all bits of a packet onto the link
      - Li = Size of packet (number of bits)
      - R = Link rate (bps)(# of bits per second)
      - dtrans = Li/R
      - this is a formula put it in key Notes
    - Propogation delay
      - Time it takes for head of packet to travel from sender to receiversl = length of phtiscal link (dist between two devices)
      - s = propagation speed (2x10^8m/s)
      - dprop = l/s
        - Distance / Speed

- processing delay in router
- queing delay waiting on router or smth how long waiting in que
- send packet to line, transmission delay
  - from sending que to line
  - L/R
- propogration delay
  - l/s
- dnode = dproc + dque + dtrans + dprop
- Remeber all four of five of these and the equations

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
