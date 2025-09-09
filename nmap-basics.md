#

# 🔷 Nmap Notes

# **Section 1: Network Scanning**

## TCP/IP Networking:

- **TCP/IP** = Transmission Control Protocol / Internet Protocol
- **IP** transmits info across networks, provides addressing scheme, delivers packets from source to destination.
- NETWORK LAYER PROTOCOL
- Supports transport layer protocols that have higher responsibilities

**Two Main Transport Layer Protocols**

- Transmission Control Protocol (TCP)
- User Datagram Protocol (UDP)

**TCP** is responsible for the majority of network traffic

- Connection oriented protocol (establishes connections between two systems before data is tranferred.)
- Reliable protocol that guarantees delivery by having system acknowledge receipt of every packet.
- Widely used by applicatons like email and websites.
- Systems go through a "handshaking process" to create a connection before transmitting data (**Three-way Handshake**) 🤝.

TCP packets include 🚩 **flags** 🚩 that identify packets

**TCP Flags**

- **SYN:** Identifies packets that are requesting a new connection (OPEN)
- **FIN:** Identifies packets that are requesting the closure of an existing connection (CLOSE)
- **ACK:** Used to acknowledge a SYN or FIN request.

**Three-way Handshake 🤝**

- first system sends SYN packet to other system to open connection
- receiving system receives SYN packed and sends ACK and SYN packet to request a recipricol connection
- fist system receives SYN/ACK packet and sends ACK packet to final destination, completing recipricol connection.
- once this completes, the systems are open and can begin exchanging data

**UDP** Protocol is lightweight and does not use three-way handshake

- Connectionless protocol that blindly sends data and hopes it get recieved.
- Does not perform acknowlegements, therefore cannot guarantee delivery
- Often used for applications like voice and video where guaranteed delivery of every packet isn't essential.

These protocols are known as the **OSI Model** by networking professionals

- **OSI** = Open Systems Interconnection
- Describes networks as having 7 layers:
  1. Physical Layer
     - sends bits over the network using wires, radios & optics
  2. Data Layer
     - Transfers data between two nodes connected to the same physical network
  3. Network Layer
     - Expands networks to many different nodes
     - **IP** works at this layer
  4. Transport Layer
     - creates connections between systems and transfers data in a _reliable_ manner
     - TCP & UDP are transport layer protocols
  5. Session Layer
     - manages the exchange of communication between systems
  6. Presentation Layer
     - Translates data so that it may be transmitted on a network
     - Describes how to represent a layer in bits and performs encryption and decryption.
  7. Application Layer
     - Determines how user interact with data using web browsers or other client applications

## IP Addressing
