

# Computer Networks

### Course Information
**Course:** CSE 3251 (Computer Networks)
**Course Type:** Theory, 3 Credit
**Prerequisite:** ICE3161 Communication Engineering
### Instructor
Dr. Asif Zaman, Peofessor, Dept. of CSE, University of Rajshahi 

### Course Motivation
> To develop basics knowledge on designing, installing, maintaining and monitoring Computer Network and its standard protocols.

---

## Course Contents

| Area | Topics Covered |
| --- | --- |
| **Introduction** | Classification, topology, protocol hierarchies, OSI model, and example networks |
| **Physical and Data Link layers** | Transmission media, IEEE standards, PSTN, circuit/packet switching, framing, error detection, and sliding window protocols |
| **Medium Access Sub-layer** | ALOHA, CSMA/CD, wireless LAN, Ethernet, and Bluetooth |
| **Network Layer** | IP addressing, routing algorithms, congestion control, and internetworking |
| **Transport Layer** | Services, elements of protocols, three-way handshake, and TCP congestion control |
| **Presentation and Application layers** | Data compression, DNS, Email, and the World Wide Web |

---

## Textbooks

**Primary Texts:**
1. Andrew S. Tanenbaum — *Computer Networks*, Prentice Hall

---

## Table of Contents

1. [Chapter 1 – Introduction to Networking and Distributed Systems](#chapter-1)
2. [Chapter 2 – Network Architecture and Reference Models](#chapter-2)
3. [Chapter 3 – The Physical Layer and Switching](#chapter-3)
4. [Chapter 4 – The Data Link Layer (DLL)](#chapter-4)
5. [Chapter 5 – Medium Access Control (MAC) Sublayer](#chapter-5)
6. [Chapter 6 – The Network Layer](#chapter-6)
7. [Chapter 7 – The Transport Layer](#chapter-7)
8. [Chapter 8 – The Presentation and Application Layers](#chapter-8)

---

## Chapter 1
## Introduction to Networking and Distributed Systems

### 1.1 Fundamentals of Computer Networks

**Course Overview:** This course provides a comprehensive exploration of Computer Networks, covering the fundamental principles of data communication, network architecture, and protocol design. It is structured around the OSI (Open Systems Interconnection) and TCP/IP reference models, analyzing the functionality of each layer—from the Physical layer that transmits raw bits to the Application layer that provides end-user services. Key topics include network hardware (hubs, switches, routers), addressing schemes (IPv4, CIDR, VLSM), routing algorithms, and reliable data transfer mechanisms (TCP, sliding window protocols).

**Definition of Computer Network:** A collection of autonomous computers interconnected by a single technology. Two computers are interconnected if they can exchange information via copper wire, fiber optics, microwaves, or satellites.

**Computer Network vs. Distributed System:**
- **Network:** Computers are separate; users must manually connect to and access machines.
- **Distributed System:** Appears to the user as a single unified system. Middleware (a software layer) hides the differences between machines.

---

### 1.2 Network Classification and Transmission Technologies

**Network Classification by Scale:**
- **PAN (Personal Area Network):** Range of a person (e.g., Bluetooth connecting a phone to earbuds).
- **LAN (Local Area Network):** Covers a home, office, or building (e.g., Ethernet, Wi-Fi).
- **MAN (Metropolitan Area Network):** Covers a city (e.g., cable TV networks, WiMAX).
- **WAN (Wide Area Network):** Spans a country or continent (e.g., the Internet).

**Network Classification by Topology:** Network topology refers to the physical or logical arrangement of nodes and links in a network. Common topologies include: bus (single shared cable), star (central hub/switch), ring (each node connected to two others forming a circle), mesh (fully or partially interconnected), and tree (hierarchical).

**Network Transmission Technologies:**
- **Unicast:** Point-to-point communication between one sender and one receiver.
- **Broadcast:** Communication shared by all machines on a network; every machine receives the packet, but only the one with the correct address processes it.
- **Multicast:** Sending packets to a selected group of machines.

**Protocol hierarchies:** Protocol hierarchies organize network protocols into layers. Each layer offers services to the layer above and communicates with its peer layer on another machine using a protocol. This layered architecture simplifies network design and implementation.

**Example networks:** Example networks include the Internet (global WAN), Ethernet LANs (wired office networks), Wi-Fi networks (wireless home/office), cellular networks (4G/5G), Bluetooth PANs, and satellite networks.

---

## Chapter 2
## Network Architecture and Reference Models

### 2.1 Protocols and Architecture

**Protocols and Architecture:**
- **Protocol:** An agreement between communicating parties on how communication proceeds.
- **Peers:** Entities on the same layer in different hosts that communicate with each other.
- **Protocol Stack:** A list of protocols used by a system, one per layer.

---

### 2.2 OSI Reference Model

**OSI Reference Model (7 Layers):**
1.  **Physical:** Transmits raw bits over a channel.
2.  **Data Link:** Converts raw transmission into error-free frames.
3.  **Network:** Handles routing and congestion control.
4.  **Transport:** Ensures reliable process-to-process data delivery.
5.  **Session:** Manages dialog control and synchronization.
6.  **Presentation:** Handles syntax, semantics, and data compression/encryption.
7.  **Application:** Directly provides services to users (e.g., HTTP, Email).

**Critique of OSI Model:** It failed largely due to bad timing (TCP/IP was already established), bad technology (layers like Session/Presentation were nearly empty), and bad implementations.

---

### 2.3 TCP/IP Reference Model

**TCP/IP Reference Model:** A practical model focusing on protocols. It consists of the Link, Internet, Transport, and Application layers.
- **Link Layer (Network Interface):** Corresponds to OSI Physical + Data Link; handles communication with the physical network hardware.
- **Internet Layer (Network):** Corresponds to OSI Network; handles routing, IP addressing, and packet forwarding.
- **Transport Layer:** Corresponds to OSI Transport; provides end-to-end communication (TCP reliable, UDP unreliable).
- **Application Layer:** Corresponds to OSI Session, Presentation, and Application; includes protocols like HTTP, FTP, DNS, SMTP.

**Layers 1-3 (Physical, DLL, Network) are hardware/network-centric**, focused on moving bits and packets between machines.

**Layers 4-7 (Transport, Session, Presentation, Application) are software/host-centric**, focused on ensuring data arrives correctly for specific applications.

---

## Chapter 3
## The Physical Layer and Switching

### 3.1 Transmission Media and IEEE Standards

**Transmission Media:**
- **Guided:** Signals travel via physical paths (Copper wire, UTP/STP, Coaxial cable, Optical fiber).
- **Unguided:** Signals transmitted through air/vacuum (Radio, Microwaves, Infrared).

**IEEE Standards:** The IEEE (Institute of Electrical and Electronics Engineers) defines standards for networking technologies, including:
- **IEEE 802.3:** Ethernet (wired LAN)
- **IEEE 802.11:** Wireless LAN (Wi-Fi)
- **IEEE 802.15:** Bluetooth (personal area networks)
- **IEEE 802.16:** WiMAX (wireless MAN)

**PSTN (Public Switched Telephone Network):** The traditional telephone network that originally used analog circuit switching. It now uses digital switches and fiber optics but retains the circuit-switched model for voice calls.

---

### 3.2 Switching Types and X.25 Protocol

**Switching Types:**
- **Circuit Switching:** A dedicated physical path is established between sender and receiver before data is sent (e.g., traditional telephone network).
- **Packet Switching:** Data is divided into packets that travel independently and are routed toward the destination (e.g., the Internet).

**X.25 Protocol:** An early packet-switching protocol specifying three layers: Physical, Frame, and Packet. It uses DTE (Data Terminal Equipment) like PCs and DCE (Data Circuit-terminating Equipment) like modems.

---

### 3.3 Network Hardware

**Network Hardware:**
- **NIC (Network Interface Card):** A hardware component providing a physical network address and MAC address.
- **Repeater:** A Layer 1 device that amplifies signals to extend cable length; it does not understand frames.
- **Hub:** A Layer 1 device that broadcasts incoming data to all ports; it is essentially a multiport repeater.
- **Switch:** A Layer 2 device that forwards data only to the destination port based on MAC addresses.
- **Router:** A Layer 3 device that connects multiple networks and routes packets based on IP addresses.

**Collision Domain:** A network area where data packets can collide. In switched networks, each port is its own domain.

**CAM Table:** A fast memory table in a switch storing MAC addresses and their corresponding ports.

---

## Chapter 4
## The Data Link Layer (DLL)

### 4.1 Key Functions and Framing

**Key Functions of the Data Link Layer:** Framing, error control, and flow control.

**Framing:** Breaking the bit stream into discrete units. Methods include Byte Count, Flag bytes with byte stuffing, and Flag bits with bit stuffing.

**Byte Count:** A frame begins with a count field indicating how many bytes are in the frame. Problem: if the count field is corrupted, synchronization is lost.

**Flag bytes with byte stuffing:** Frames are delimited by special flag bytes (e.g., 01111110). If the flag pattern appears inside the data, a special escape byte is inserted (byte stuffing) to distinguish it from the real flag.

**Flag bits with bit stuffing:** Used in HDLC. A flag pattern (01111110) marks frame boundaries. Whenever five consecutive 1s appear in the data, the sender inserts a 0. The receiver removes that 0 after five 1s.

---

### 4.2 Error Control

**Error Control:**
- **Error Detection:** Using CRC or checksums to find corrupted bits.
- **Error Correction:** Using redundant bits to repair corrupted data.
- **ARQ (Automatic Repeat Request):** The process of retransmitting lost or corrupted frames.

**HDLC (High-Level Data Link Control):** A bit-oriented protocol using flag patterns (01111110) to delimit frames. Frame types include I-frames (Information), S-frames (Supervisory/Flow Control), and U-frames (Unnumbered/Link Management).

---

### 4.3 Flow Control and Sliding Window Protocols

**Flow Control:** Prevents a fast sender from overwhelming a slow receiver.

**Stop-and-Wait:** Sender sends one frame and waits for an ACK before sending the next.

**Sliding Window Protocols:** Allow multiple frames to be sent without waiting for an immediate ACK, increasing efficiency.
- **Go-Back-N:** On error, retransmits all frames from the point of error.
- **Selective Repeat:** Only retransmits the specific rejected/lost frame.

**Piggybacking:** Attaching an acknowledgement (ACK) to an outgoing data frame to save bandwidth.

**Reliability is an end-to-end argument:** While lower layers detect errors, the Transport layer (TCP) is ultimately responsible for ensuring the entire message arrives intact.

---

## Chapter 5
## Medium Access Control (MAC) Sublayer

### 5.1 Multiple Access Protocols

**Multiple Access Protocols:** Used to determine who sends next on a shared channel.

**ALOHA:**
- **Pure ALOHA:** Users transmit whenever they have data; collisions are resolved by retransmitting after a random delay.
- **Slotted ALOHA:** Time is divided into slots; users can only transmit at the start of a slot, reducing collisions.

**CSMA (Carrier Sense Multiple Access):** Stations listen to the channel before transmitting.
- **CSMA/CD (Collision Detection):** Detects collisions and stops transmitting immediately; used in wired Ethernet.
- **CSMA/CA (Collision Avoidance):** Avoids collisions; used in Wi-Fi (802.11).

---

### 5.2 Ethernet and Wireless LAN

**Ethernet (802.3):**
- **Classic Ethernet:** Uses a single shared cable (bus topology); all devices are in one collision domain.
- **Switched Ethernet:** Uses switches to provide dedicated links; each port is a separate collision domain.

**Wireless LAN (802.11):** Standards include 802.11b/a/g/n/ac, offering varying speeds and frequencies (2.4 GHz and 5 GHz). CSMA/CA is used instead of CSMA/CD because a wireless station cannot listen while transmitting (hidden terminal problem).

**Bluetooth (802.15):** A short-range wireless technology for personal area networks (PANs) connecting devices like phones, headsets, keyboards, and mice. Bluetooth uses frequency hopping spread spectrum (FHSS).

---

## Chapter 6
## The Network Layer

### 6.1 Functions and IPv4 Addressing

**Functions of the Network Layer:** Assigning logical addresses, fragmentation/reassembly, packetizing, and routing.

**IPv4 Addressing:** A 32-bit unique number.
- **NetID:** Identifies the network.
- **HostID:** Identifies the specific device.

**Address Space:** The total set of addresses available in a system (for $N$ bits, space = $2^N$).

**Classful Addressing:**
- **Class A:** Range 1–126; Mask 255.0.0.0 (/8). First bit is 0.
- **Class B:** Range 128–191; Mask 255.255.0.0 (/16). First two bits are 10.
- **Class C:** Range 192–223; Mask 255.255.255.0 (/24). First three bits are 110.
- **Class D (Multicast):** Range 224–239; first four bits are 1110.
- **Class E (Reserved):** Range 240–255; first four bits are 1111.

> 💡 **Class C IP Calculation Example:** For IP 192.168.1.130 with mask 255.255.255.0, the NetID is 192.168.1 and HostID is 130. The network address is 192.168.1.0.

---

### 6.2 Subnetting, CIDR, and VLSM

**Subnetting and CIDR:**
- **Subnetting:** Borrowing bits from the HostID to create smaller, internal networks.
- **CIDR (Classless Inter-Domain Routing):** Allows any number of network bits (e.g., /20), ending fixed class boundaries to save address space. CIDR notation: IP address followed by a slash and the number of network bits (e.g., 192.168.1.0/24).
- **VLSM (Variable Length Subnet Masking):** Allows subnets of different sizes within the same network block.

**NAT (Network Address Translation):** Replaces private IPs with one public IP to connect to the Internet and save address space.

**Subnetting/VLSM are essential for managing the limited IPv4 address space efficiently by matching network size to actual host needs.**

---

### 6.3 Routing Algorithms

**Routing Algorithms:**
- **Distance Vector:** Routers share tables with neighbors and use metrics like hop count (e.g., RIP – Routing Information Protocol). Simple but slow to converge; may suffer from count-to-infinity problem.
- **Link State:** Routers build a complete map of the network (link-state database) and calculate the shortest path using Dijkstra's algorithm (e.g., OSPF – Open Shortest Path First). Faster convergence but more computationally intensive.

**Routing Algorithms in detail:**
- **Distance Vector algorithm:** Each router maintains a table of the best known distance to each destination and which neighbor to use to get there. Routers periodically exchange their tables with neighbors.
- **Link State algorithm:** Each router discovers its neighbors, measures the cost to each neighbor, builds a link-state packet (LSP) containing this information, floods the LSP to all other routers, and then runs Dijkstra's algorithm to compute shortest paths.

**Congestion Control in the Network Layer:** When too many packets enter the network, routers' queues fill up, causing packet loss and delay. Congestion control techniques include: traffic shaping (leaky bucket, token bucket), choke packets (send a warning back to the source), and explicit congestion notification (ECN) marking packets to signal congestion.

**Internetworking:** Connecting multiple networks (possibly using different technologies) to form an internetwork (internet). Routers are the key devices that interconnect networks and forward packets between them.

**Network Protocols:**
- **ARP (Address Resolution Protocol):** Maps an IP address to a MAC address on a local network.
- **RARP (Reverse Address Resolution Protocol):** Maps a MAC address to an IP address (mostly obsolete, replaced by BOOTP/DHCP).
- **ICMP (Internet Control Message Protocol):** Carries control and error messages (e.g., ping uses ICMP Echo Request/Reply).
- **DHCP (Dynamic Host Configuration Protocol):** Automatically assigns IP addresses to devices on a network.

> 💡 **ARP Example:** A host knows a destination IP (192.168.1.5) and uses ARP to find the physical MAC address (00:1A:2B:3C:4D:5E) for delivery on the local LAN.

**DORA Process:** The four-step DHCP message exchange: Discover, Offer, Request, Acknowledge.

---

## Chapter 7
## The Transport Layer

### 7.1 Transport Layer Services

**Responsibilities of the Transport Layer:** End-to-end reliability, multiplexing/demultiplexing, and congestion control.

**Transport Layer Services:** Connection-oriented service (TCP) and connectionless service (UDP), segmentation and reassembly, error control, flow control, and multiplexing (multiple applications using the same network connection via ports).

**Elements of transport protocols:** Addressing (ports), connection establishment (active/passive open), connection release (graceful/abrupt), error control (checksum, sequence numbers, retransmission), flow control (sliding window), and congestion control.

---

### 7.2 UDP and TCP

**UDP (User Datagram Protocol):** Connectionless and unreliable; used for speed or simple request-response (e.g., DNS, streaming, VoIP). UDP has a minimal 8-byte header and no congestion control.

**TCP (Transmission Control Protocol):** Connection-oriented, reliable byte stream.

**Three-Way Handshake:** Connection establishment (SYN → SYN+ACK → ACK).
1. Client sends SYN segment (seq=x).
2. Server responds with SYN+ACK (seq=y, ack=x+1).
3. Client sends ACK (seq=x+1, ack=y+1).
Connection is now established.

**Flow Control in TCP:** Managed via a dynamic sliding window (the Window size field in the TCP header). The receiver advertises how much data it is willing to accept.

**Congestion Control in TCP:** TCP slows down when it detects packet loss at routers (using algorithms like slow start, congestion avoidance, fast retransmit, and fast recovery). TCP assumes packet loss is due to congestion (AIMD – Additive Increase Multiplicative Decrease).

**Sockets:** An API using an IP Address + Port Number to uniquely identify an application process.

> 💡 **Socket Example:** A web server running on port 80 combined with its IP (e.g., 142.250.190.14:80) allows a browser to reach that specific service.

---

## Chapter 8
## The Presentation and Application Layers

### 8.1 Presentation Layer

**Presentation Layer functions:** Handles syntax and semantics of exchanged information, including data compression, encryption, and data conversion (e.g., EBCDIC to ASCII).

**Data Compression:**
- **Lossless compression:** No data lost (e.g., Run Length Encoding, Huffman coding, LZW). Used for text and executable files.
- **Lossy compression:** Some data lost for higher reduction (e.g., JPEG for images, MP3 for audio, MPEG for video).

**Encryption:**
- **SSL (Secure Sockets Layer) / TLS (Transport Layer Security):** Provides secret communication, data integrity, and authentication for network connections (used in HTTPS).

---

### 8.2 Application Layer Services

**Application Layer:** Directly provides services to users. Key protocols include DNS, Email (SMTP), and HTTP for the World Wide Web.

**DNS (Domain Name System):** A distributed hierarchical database mapping domain names (google.com) to IP addresses (142.250.190.14). DNS uses UDP on port 53 for queries and TCP for zone transfers.

**Email Services:**
- **SMTP (Simple Mail Transfer Protocol):** Used to send messages between mail servers (port 25). SMTP pushes email from client to server and between servers.
- **POP3 (Post Office Protocol version 3):** Downloads email from server to client, typically deleting it from the server (port 110).
- **IMAP (Internet Message Access Protocol):** Keeps email on the server, allowing multiple clients to access the same mailbox (port 143).

**WWW (World Wide Web):** A distributed information system where documents (web pages) are identified by URLs and transmitted using HTTP/HTTPS.

**HTTP (Hypertext Transfer Protocol):** Request-response protocol used to fetch web pages. Methods include GET (retrieve a resource), POST (submit data), PUT (upload a resource), and DELETE (remove a resource).

**HTTPS:** HTTP encrypted using SSL/TLS to provide secure communication for sensitive transactions (e.g., banking, e-commerce).

**URL (Uniform Resource Locator):** A string that identifies a resource on the web, e.g., `https://www.example.com:8080/path/to/file?key=value#section`.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Introduction | Network (autonomous computers), Distributed system (middleware), PAN/LAN/MAN/WAN, Unicast/Broadcast/Multicast |
| 2 | Reference Models | OSI (7 layers: Physical, Data Link, Network, Transport, Session, Presentation, Application), TCP/IP (Link, Internet, Transport, Application), Protocol stack, Peer entities |
| 3 | Physical Layer | Guided/Unguided media, Circuit/Packet switching, X.25 (DTE/DCE), NIC, Repeater, Hub (Layer 1), Switch (Layer 2, MAC), Router (Layer 3, IP) |
| 4 | Data Link Layer | Framing (byte count, byte stuffing, bit stuffing), Error detection (CRC), ARQ, Flow control (Stop-and-Wait, Sliding Window), Go-Back-N, Selective Repeat, HDLC (I/S/U frames) |
| 5 | MAC Sublayer | ALOHA (Pure/Slotted), CSMA/CD (Ethernet), CSMA/CA (Wi-Fi), Switched Ethernet, Bluetooth (802.15), Collision domain |
| 6 | Network Layer | IPv4 (32-bit, NetID/HostID), Classful (A,B,C,D,E), CIDR (/n), VLSM, Subnetting, NAT, Routing (Distance Vector/RIP, Link State/OSPF), ARP, ICMP, DHCP (DORA) |
| 7 | Transport Layer | UDP (unreliable, connectionless), TCP (reliable, connection-oriented, byte stream), Three-way handshake, Flow control (window), Congestion control (AIMD, slow start), Socket (IP:port) |
| 8 | Presentation/Application | Lossless/Lossy compression, SSL/TLS, DNS (domain → IP), Email (SMTP, POP3, IMAP), HTTP/HTTPS, URL |

---
*CSE 3251 — Computer Networks | Dept. of CSE, University of Rajshahi*




