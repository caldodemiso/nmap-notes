# 🔷 Nmap Notes

# **Section 1: Network Scanning**

These notes summarize Section 1 of my LinkedIn Learning Nmap course.  
They cover essential networking concepts (TCP/IP, ports, ICMP, and OSI layers) that Nmap builds on when scanning.

---

## TCP/IP Networking

- **TCP/IP** = Transmission Control Protocol / Internet Protocol
- **IP** transmits info across networks, provides addressing scheme, and delivers packets from source to destination.
- Operates at the **Network Layer** of the OSI model.
- Supports transport layer protocols that have higher responsibilities.

**Two Main Transport Layer Protocols**

- **Transmission Control Protocol (TCP)**
- **User Datagram Protocol (UDP)**

### TCP

- Responsible for the majority of network traffic.
- **Connection-oriented** protocol (establishes connections before transferring data).
- Reliable — guarantees delivery by requiring acknowledgements for every packet.
- Common for email, web traffic, file transfers, etc.
- Uses a **three-way handshake 🤝** to establish connections.

**TCP Flags**

- **SYN:** Request to open a new connection.
- **FIN:** Request to close an existing connection.
- **ACK:** Acknowledges a SYN or FIN request.

**Three-way Handshake 🤝**

1. First system sends a SYN packet to request a connection.
2. Receiving system replies with SYN + ACK (acknowledge + reciprocal connection request).
3. First system sends ACK back, completing the handshake.  
   ➡ Connection is established, and data can flow.

### UDP

- **Connectionless** protocol — just sends packets without handshakes.
- Lightweight, but cannot guarantee delivery (no acknowledgements).
- Often used for voice, video, or streaming where speed > guaranteed reliability.

---

## OSI Model

Networking professionals often describe TCP and UDP in relation to the **OSI Model**, which organizes communication into 7 layers:

1. **Physical Layer**
   - Transmits bits over wires, radios, or optics.
2. **Data Link Layer**
   - Transfers data between nodes on the same network segment.
3. **Network Layer**
   - Routes packets between multiple nodes and networks.
   - **IP** works here.
4. **Transport Layer**
   - Ensures reliable connections between systems.
   - **TCP & UDP** live here.
5. **Session Layer**
   - Manages sessions between applications.
6. **Presentation Layer**
   - Translates data formats; handles encryption/decryption.
7. **Application Layer**
   - Where users interact with data (e.g., web browsers, clients).

---

## 🔗 Nmap Tie-In

- Nmap leverages **TCP flags (SYN, ACK, FIN)** during different scan types (`-sS`, `-sT`, etc.).
- Understanding the **three-way handshake** helps explain how Nmap identifies open vs. closed ports.
- Recognizing where **IP, TCP, and UDP** fit in the OSI model makes it easier to interpret scan results.

---
