# CN-SKILL-ASSESSMENT-2
# NAME: KARTHICK E S
# REG NO: 212223060114

# 🌐 Flow Control in Communication Networks

## 📘 Data Communication and Computer Networks

### Department of Computer Science & Engineering

---

# 📌 Report Details

| Field | Details |
|---|---|
| **Topic** | Flow Control in Communication Networks |
| **Subject** | Data Communication and Computer Networks |
| **Prepared By** | Network Research Team |
| **Year** | 2026 |
| **Category** | Technical Report |

---

# 🧠 Introduction

Flow Control is a mechanism used in communication networks to regulate the rate of data transmission between sender and receiver.

Its primary purpose is to ensure that a fast sender does not overwhelm a slow receiver, thereby preventing:

- Buffer overflow
- Packet loss
- Excessive retransmissions
- Network performance degradation

Flow control plays a critical role in maintaining reliable and efficient communication across modern computer networks.

---

# 🎯 Objectives

- Understand the concept of Flow Control
- Study various Flow Control protocols
- Analyze working principles and mechanisms
- Compare different protocols
- Explore real-world applications

---

# 🌐 Concept of Flow Control

Flow Control coordinates the amount of data transmitted before acknowledgements are received.

It ensures:

- Reliable communication
- Receiver protection
- Efficient bandwidth utilization
- Controlled packet transmission

---

# ❓ Why Flow Control is Necessary

Without Flow Control:

- Receiver buffers may overflow
- Packets may be dropped
- Network congestion increases
- End-to-end delay becomes high
- Quality of Service (QoS) decreases

---

# 📂 Categories of Flow Control

| End-to-End Flow Control | Link-Level Flow Control |
|---|---|
| Operates between source and destination | Operates between adjacent nodes |
| Implemented at Transport Layer | Implemented at Data Link Layer |
| Example: TCP Sliding Window | Example: IEEE 802.3x PAUSE |

---

# 🔑 Flow Control Mechanisms

## 1. Stop-and-Wait Protocol

- Sender sends one frame
- Waits for ACK
- Sends next frame only after acknowledgment

### Features

- Simple implementation
- Reliable
- Low efficiency on long-delay links

---

## 2. Sliding Window Protocol

- Multiple frames can be sent before ACK
- Window size determines transmission limit
- Window slides as ACKs arrive

### Features

- High throughput
- Better bandwidth utilization
- Efficient communication

---

## 3. Go-Back-N Protocol

- Sender sends N frames
- If one frame is lost, retransmits from error frame onwards

### Features

- Moderate complexity
- Retransmits correct frames unnecessarily

---

## 4. Selective Repeat Protocol

- Only erroneous frame is retransmitted
- Receiver buffers out-of-order frames

### Features

- High efficiency
- Better performance
- More complex implementation

---

# 📊 Protocol Comparison

| Protocol | Complexity | Efficiency |
|---|---|---|
| Stop-and-Wait | Low | Low |
| Go-Back-N | Medium | Moderate |
| Selective Repeat | High | High |
| TCP Sliding Window | Dynamic | Very High |

---

# 🏗️ Network Design Considerations

Flow Control is implemented across multiple OSI layers.

| OSI Layer | Flow Control Role |
|---|---|
| Physical Layer | Bit-rate matching |
| Data Link Layer | Frame-level flow control |
| Network Layer | Queue management |
| Transport Layer | End-to-End flow control |
| Application Layer | Adaptive rate control |

---

# 📈 TCP Receive Window Mechanism

TCP uses a Receive Window (**rwnd**) to indicate available buffer space.

### Working

1. Sender transmits data
2. Receiver processes data
3. Receiver sends ACK with window size
4. Sender adjusts transmission rate

This prevents receiver overload.

---

# ⚙️ Simulation Tools

Common tools used to study Flow Control:

- NS-3
- GNS3
- MATLAB / Simulink
- Wireshark
- Python (Scapy / SimPy)

---

# 📡 Working Principle

## TCP Flow Control Process

### Step 1: Connection Setup

- TCP handshake occurs
- Receive window advertised

### Step 2: Data Transmission

- Sender sends data within window size

### Step 3: ACK with Window Update

- Receiver acknowledges data
- Updated window size sent

### Step 4: Window Adjustment

- Sender adjusts transmission rate

### Step 5: Zero Window

- Receiver buffer becomes full
- Sender pauses transmission

### Step 6: Window Probe

- Sender checks if receiver is ready

### Step 7: Resume Transmission

- Receiver advertises non-zero window
- Data transfer continues

---

# 🔄 Sliding Window Operation

### Sender Maintains

- Send Base (SB)
- Next Sequence Number (NSN)
- Window Boundary

### Benefits

- Continuous transmission
- Reduced waiting time
- Increased throughput

---

# 🌍 Real-Time Applications

## Video Streaming

Examples:

- Netflix
- YouTube

Flow control regulates video delivery rate according to client buffer capacity.

---

## File Transfer

Examples:

- FTP
- SFTP

TCP window scaling enables high-speed file transfer.

---

## Cloud Data Centers

Examples:

- AWS
- Azure

Uses:

- RDMA
- Credit-Based Flow Control

---

## Industrial IoT

Examples:

- PROFINET
- EtherNet/IP

Ensures reliable communication between industrial devices.

---

## Satellite Communication

Uses:

- TCP Window Scaling
- Performance Enhancing Proxies

Handles high latency links effectively.

---

# 🌟 Advantages of Flow Control

- Prevents receiver buffer overflow
- Improves reliability
- Maximizes bandwidth utilization
- Supports Quality of Service
- Enables fair resource sharing
- Reduces retransmissions
- Supports heterogeneous networks

---

# ⚠️ Disadvantages of Flow Control

- Additional ACK overhead
- Increased protocol complexity
- Latency in Stop-and-Wait
- Bufferbloat issues
- Requires buffer management
- Not sufficient for congestion control

---

# 🏭 Applications

| Domain | Flow Control Mechanism |
|---|---|
| Web Browsing | TCP Flow Control |
| Email | TCP Sliding Window |
| Video Conferencing | RTCP + Rate Control |
| Cloud Computing | TCP BBR, DCQCN |
| Mobile Networks | PDCP/RLC Flow Control |
| Satellite Internet | TCP + Window Scaling |

---

# 🔍 Comparison with Other Mechanisms

## Flow Control vs Congestion Control

| Flow Control | Congestion Control |
|---|---|
| Protects Receiver | Protects Network |
| Uses rwnd | Uses cwnd |
| Receiver-driven | Network-driven |

---

## Flow Control vs Error Control

| Flow Control | Error Control |
|---|---|
| Controls transmission rate | Detects and corrects errors |
| Uses windows | Uses CRC, ARQ |

---

# 📊 Efficiency Comparison

| Protocol | Throughput Efficiency |
|---|---|
| Stop-and-Wait | 5 – 15% |
| Go-Back-N | 60 – 75% |
| Selective Repeat | 80 – 90% |
| TCP Window Scaling | 95 – 99% |
| RDMA / CBFC | 99.9% |

---

# ✅ Conclusion

Flow Control is an essential component of modern communication networks.

It:

- Matches sender speed with receiver capacity
- Prevents packet loss
- Improves throughput
- Ensures reliable communication

Modern implementations such as TCP Sliding Window, Selective Repeat, and RDMA-based flow control provide high performance across cloud computing, video streaming, industrial automation, and satellite communication systems.

---

# ❓ Viva / Question Bank

## Short Questions

1. Define Flow Control.
2. What is TCP Receive Window?
3. Difference between Flow Control and Congestion Control?
4. What is Sliding Window?
5. What is Stop-and-Wait Protocol?

---

## Long Questions

1. Explain Stop-and-Wait Protocol.
2. Explain Sliding Window Protocol.
3. Compare GBN and Selective Repeat.
4. Describe TCP Flow Control.
5. Explain real-time applications of Flow Control.

---

# 📚 End of Report

## Flow Control in Communication Networks – Technical Report 2026
