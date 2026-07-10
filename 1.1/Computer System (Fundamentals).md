

# Introduction to Computer Systems

### Course Information
**Course:** CSE 1111 (Introduction to Computer Systems) 
**Course Type:** Theory, 3 Credit 
**Prerequisite:** None

### Instructor
Dr. Somlal Das, Professor, Dept. of CSE, University of Rajshahi 

---

### Course Motivation

> To accrue adequate fundamental knowledge required to build a sound base for studying computer science.


## Course Contents

|Area|Topics Covered|
|---|---|
|**Computer Basics**|Introduction to computers, history and development, generations, types, characteristics, modern digital devices|
|**Computer Hardware and Peripherals**|Basic units of hardware, internal structure of CPU and multi-core CPU, RAM, ROM, cache memory, HDD, CD-ROM, SSD, monitors, projector, printers, scanner, typical computer specifications|
|**Software**|Classifications, system software, OS concepts (DOS, Windows, Mac, Linux, Android, iOS), application software, utility programs, malware|
|**Data Processing**|Concepts of data, information and database, traditional file processing, DBMS|
|**Computer Networks**|Network goals, LAN, MAN, WAN and internet systems, internet services, common network devices and software, cloud computing|

---

## Textbooks

**Primary Texts:**
1. Peter Norton — _Introduction to Computer_, McGraw-Hill Publishers
2. J. Stanley Warford — _Computer Systems_, Jones & Bartlett Publishers

---

## Table of Contents

1. [Module 1 – Introduction to Computer Basics](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#module-1)
2. [Module 2 – Computer Hardware and Internal Architecture](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#module-2)
3. [Module 3 – Memory and Data Storage Systems](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#module-3)
4. [Module 4 – Peripheral Devices (Input and Output)](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#module-4)
5. [Module 5 – Computer Software and Programming Languages](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#module-5)
6. [Module 6 – Data Representation and Processing](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#module-6)
7. [Module 7 – Computer Networks and Internet Systems](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#module-7)
8. [Module 8 – Computer Security and Future Trends](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#module-8)

---

## Module 1

## Introduction to Computer Basics

### 1.1 Definition of a Computer

A **computer** is an **electronic data processor** — a machine that accepts raw data, processes it, and produces meaningful output.

**Five Basic Functions:**

|Function|Description|
|---|---|
|**Accept**|Take input data from the user or environment|
|**Store**|Hold data in memory for later use|
|**Process**|Perform arithmetic or logical operations on data|
|**Retrieve**|Fetch stored data when needed|
|**Print**|Produce output in a human-readable or machine-readable form|

---

### 1.2 Characteristics of Computers

|Characteristic|Meaning|
|---|---|
|**Speed**|Executes millions of instructions per second|
|**Accuracy**|Results are precise; errors only occur from bad input|
|**Diligence**|Never gets tired; performs repetitive tasks consistently|
|**Versatility**|Can perform a wide variety of tasks across many fields|
|**Power of Remembering**|Can store vast amounts of data for long periods|
|**No IQ**|Cannot think on its own; only follows programmed instructions|
|**No Feelings**|Has no emotions, bias, or intuition|

> 📌 The last two characteristics are **limitations**, not advantages — they highlight the dependency on human programmers and decision-makers.

---

### 1.3 Historical Evolution of Computers

#### Early Calculating Machines

|Device|Description|
|---|---|
|**Abacus**|Ancient counting frame; earliest manual calculating tool|
|**Napier's Bones**|Multiplication rods invented by John Napier (1617)|
|**Slide Rule**|Analog device for multiplication/division using logarithms|
|**Pascal's Machine**|First mechanical adding machine (1642), invented by Blaise Pascal|

#### The Mechanical Era

|Inventor / Device|Contribution|
|---|---|
|**Charles Babbage — Difference Engine**|Designed to compute mathematical tables mechanically|
|**Charles Babbage — Analytical Engine**|Concept of a general-purpose programmable computer (store, mill, input, output)|
|**Jacquard's Loom**|Used punched cards to control weaving patterns — a precursor to data input|

> 💡 Charles Babbage is widely regarded as the **"Father of the Computer"** for his Analytical Engine concept.

#### Modern Electronic Development

The transition from mechanical gears to **electronic components** (vacuum tubes → transistors → ICs) marked the beginning of modern computing.

---

### 1.4 Generations of Computers

|Generation|Period|Technology Used|Key Features|
|---|---|---|---|
|**1st**|1940s–1950s|**Vacuum Tubes**|Large, hot, slow, expensive; machine language only|
|**2nd**|1950s–1960s|**Transistors**|Smaller, faster, more reliable; assembly language|
|**3rd**|1960s–1970s|**Integrated Circuits (ICs)**|Multiple transistors on one chip; high-level languages|
|**4th**|1970s–1980s|**VLSI** (Very Large Scale Integration)|Microprocessors; personal computers emerge|
|**5th**|1980s–present|**ULSI** (Ultra Large Scale Integration)|Parallel processing; early AI and expert systems|
|**6th**|Present–future|**Artificial Intelligence (AI)**|Machine learning, neural networks, natural language|

---

### 1.5 Classification of Computers

#### By Purpose

|Type|Description|
|---|---|
|**Special Purpose**|Designed for a single specific task (e.g., ATM, weather computer)|
|**General Purpose**|Capable of performing a wide variety of tasks (e.g., desktop PC)|

#### By Signal / Data Type

|Type|Data Handled|Example|
|---|---|---|
|**Analog**|Continuous signals (voltage, temperature)|Thermometer, speedometer|
|**Digital**|Discrete binary data (0s and 1s)|Modern PC|
|**Hybrid**|Both analog and digital|Hospital ICU monitors|

#### By Size and Processing Power

|Type|Description|Examples|
|---|---|---|
|**Micro-computer**|Smallest; designed for personal use|PCs, Laptops, Tablets|
|**Mini-computer**|Mid-range; supports multiple users|Departmental servers|
|**Mainframe**|Large; handles massive simultaneous transactions|Banking systems, airlines|
|**Super-computer**|Most powerful; used for complex scientific tasks|Weather forecasting, nuclear simulation|

---

## Module 2

## Computer Hardware and Internal Architecture

### 2.1 System Unit and Motherboard

The **motherboard** is the **main circuit board** of the computer. Everything connects to it.

**Key Components on the Motherboard:**

|Component|Function|
|---|---|
|**CPU Socket**|Holds the processor|
|**RAM Slots**|Hold the primary memory modules|
|**Expansion Slots**|Allow adding GPU, sound cards, etc.|
|**Chipsets**|Manage communication between CPU, RAM, and peripherals|

---

### 2.2 Central Processing Unit (CPU)

The CPU is the **"brain"** of the computer — it executes all instructions.

#### Internal Structure

|Unit|Full Name|Function|
|---|---|---|
|**ALU**|Arithmetic Logic Unit|Performs arithmetic (+, −, ×, ÷) and logical (AND, OR, NOT) operations|
|**CU**|Control Unit|Directs and coordinates all CPU operations; manages the machine cycle|
|**Registers**|—|Ultra-fast, small storage locations inside the CPU for immediate data|

#### Specialized Units

|Unit|Function|
|---|---|
|**FPU** (Floating Point Unit)|Handles complex decimal/floating-point arithmetic|
|**Prefetch Unit**|Fetches the next instruction before the current one finishes (pipeline)|
|**Decode Unit**|Translates fetched instructions into signals the ALU can execute|

#### Multi-core Technology

|Type|Cores|Benefit|
|---|---|---|
|**Dual-core**|2|Two processors on one chip; better multitasking|
|**Quad-core**|4|Four processors; better parallel processing and performance|

---

### 2.3 The Machine Cycle

Every instruction a computer executes goes through **four steps**, collectively called the **machine cycle** (also called the **instruction cycle**):

```
FETCH → DECODE → EXECUTE → STORE
```

|Step|What Happens|
|---|---|
|**Fetch**|CU retrieves the next instruction from memory|
|**Decode**|Decode Unit translates the instruction into control signals|
|**Execute**|ALU or other unit carries out the instruction|
|**Store**|Result is written back to a register or memory|

> 📌 **System Clock:** A crystal oscillator that synchronises all CPU operations. Speed is measured in **GHz** (gigahertz — billions of cycles per second).

---

### 2.4 Computer Buses

A **bus** is a communication pathway that transfers data between components.

|Bus Type|Role|
|---|---|
|**Address Bus**|Carries the **memory address** of data (one direction only)|
|**Data Bus**|Carries the actual **data** between CPU, memory, and I/O (bidirectional)|
|**Control Bus**|Carries **control signals** (read/write commands) from the CU|

|Bus Category|Scope|
|---|---|
|**System Bus**|Internal; connects CPU, RAM, and chipset|
|**Expansion Bus**|Connects CPU to peripheral devices via expansion slots|

---

### 2.5 Ports and Connectors

Physical interfaces that connect external devices to the computer:

|Port|Use|
|---|---|
|**USB**|Universal; connects keyboards, mice, storage, phones|
|**HDMI**|High-definition video and audio output|
|**VGA**|Older analog video output|
|**Ethernet**|Wired network connection|
|**Audio (3.5mm)**|Headphones and microphones|
|**Bluetooth**|Short-range wireless connection|
|**Thunderbolt**|High-speed data transfer and video (Apple and modern PCs)|

---

## Module 3

## Memory and Data Storage Systems

### 3.1 Memory Concepts

- **Memory Hierarchy:** A ranking of storage types from fastest/most expensive (registers) to slowest/cheapest (secondary storage).
- **Volatile Memory:** Loses data when power is off (e.g., RAM).
- **Non-volatile Memory:** Retains data without power (e.g., ROM, HDD, SSD).

**Memory Hierarchy (Fastest to Slowest):**

```
Registers → Cache (L1/L2/L3) → RAM → Secondary Storage (HDD/SSD) → Cloud/Tape
```

---

### 3.2 Primary Memory

#### RAM (Random Access Memory) — Volatile

|Type|Full Name|Description|
|---|---|---|
|**SRAM**|Static RAM|Uses flip-flops; faster, more expensive; used in cache|
|**DRAM**|Dynamic RAM|Uses capacitors; needs constant refresh; used in main RAM|
|**SDRAM**|Synchronous DRAM|Synchronised with the system clock for faster access|

#### ROM (Read-Only Memory) — Non-volatile

|Type|Full Name|Description|
|---|---|---|
|**MROM**|Mask ROM|Pre-programmed at manufacture; cannot be changed|
|**PROM**|Programmable ROM|Can be written once by the user|
|**EPROM**|Erasable PROM|Can be erased with UV light and rewritten|
|**EEPROM**|Electrically Erasable PROM|Erased and rewritten electrically; basis of flash memory|

> 📌 **BIOS (Basic Input/Output System):** Stored on ROM; the first program that runs when the computer starts — it performs POST and loads the OS.

#### Cache Memory

Sits between CPU and RAM to reduce access time. The CPU checks cache before going to slower RAM.

|Level|Location|Speed|Size|
|---|---|---|---|
|**L1 Cache**|Inside CPU core|Fastest|Smallest (KB range)|
|**L2 Cache**|Inside or near CPU|Fast|Medium (MB range)|
|**L3 Cache**|Shared among all cores|Slower than L1/L2|Largest (several MB)|

---

### 3.3 Secondary Storage

#### Magnetic Storage

|Device|Mechanism|
|---|---|
|**Hard Disk Drive (HDD)**|Spinning magnetic **platters**; data written in **tracks** (circles) subdivided into **sectors**|
|**Magnetic Tape**|Sequential access; slow but cheap; used for large backups|

#### Solid State Storage

|Device|Description|
|---|---|
|**SSD (Solid State Drive)**|No moving parts; uses flash memory chips; much faster than HDD|
|**Flash Memory**|Portable chips (same technology as SSD) used in memory cards|
|**Pen Drive (USB Drive)**|Compact, portable flash memory device|

#### Optical Storage

Data stored as microscopic **pits** (indentations) and **lands** (flat areas) on a reflective disc. A laser beam reads them.

|Medium|Capacity|Notes|
|---|---|---|
|**CD-ROM**|~700 MB|Read-only; audio and small data|
|**DVD**|4.7 GB – 17 GB|Video and software distribution|
|**Blu-ray**|25 GB – 100 GB|HD video; uses shorter-wavelength blue laser|

---

### 3.4 Virtual Memory

When RAM is full, the OS uses a portion of the **hard disk** as temporary RAM — this is **virtual memory**.

**Implementation techniques:**

|Technique|Description|
|---|---|
|**Demand Paging**|Pages (fixed blocks) of a program loaded into RAM only when needed|
|**Swap-in / Swap-out**|Pages moved from disk (swap-in) to RAM or from RAM to disk (swap-out) as required|

> ⚠️ Virtual memory is significantly **slower** than physical RAM because disk access is much slower.

---

## Module 4

## Peripheral Devices (Input and Output)

### 4.1 Input Devices

#### Standard Devices

|Device|Notes|
|---|---|
|**Keyboard**|Various layouts (QWERTY, DVORAK); key groups include function keys, alphanumeric, navigation, numeric pad|
|**Mouse**|**Optical mechanism** — uses LED and sensor to detect movement; buttons and scroll wheel|

#### Specialised Input Devices

|Device|Use|
|---|---|
|**Joystick**|Gaming and flight simulation|
|**Microphone**|Audio input; voice recognition|
|**Digitizer**|Converts drawings/graphics into digital coordinates (e.g., drawing tablet)|

#### Automated Data Entry Devices

|Device|Full Name|Function|
|---|---|---|
|**Scanner**|—|Converts physical documents/images to digital form|
|**OMR**|Optical Mark Reader|Detects marks on paper (e.g., multiple-choice answer sheets)|
|**OCR**|Optical Character Recognition|Reads and converts printed/handwritten text to digital text|
|**Barcode Reader**|—|Scans and decodes barcode data (e.g., in shops)|

---

### 4.2 Output Devices

#### Monitors

|Technology|Description|
|---|---|
|**CRT** (Cathode Ray Tube)|Older, bulky; uses electron beam to illuminate phosphor screen|
|**LCD** (Liquid Crystal Display)|Flat panel; uses liquid crystals and backlight|
|**LED** (Light Emitting Diode)|Flat panel; uses LEDs as backlight; brighter and more energy-efficient than LCD|

#### Printers

|Category|Type|Mechanism|
|---|---|---|
|**Impact**|Dot Matrix|Pins strike a ribbon against paper; can print carbon copies|
|**Non-impact**|Laser|Uses static electricity, toner powder, and heat (fusing)|
|**Non-impact**|Inkjet|Sprays tiny droplets of ink onto paper|

**Printer Evaluation Criteria:** Speed (PPM), Resolution (DPI), Cost per page, Noise level, Colour capability.

#### Other Output Devices

|Device|Use|
|---|---|
|**Plotter**|Draws precise vector graphics (e.g., engineering diagrams, maps)|
|**Speakers**|Audio output|
|**Projector**|Projects screen image onto a large surface for presentations|

---

## Module 5

## Computer Software and Programming Languages

### 5.1 Software Classification

|Category|Description|Examples|
|---|---|---|
|**System Software**|Manages hardware and provides platform for other software|OS, Device Drivers|
|**Application Software**|Performs specific user tasks|MS Word, Photoshop, Chrome|
|**Programming Software**|Tools used to write and test programs|Compilers, IDEs, Debuggers|
|**Utility Programs**|Performs maintenance and optimisation tasks|Antivirus, Disk Cleaner|
|**Package Programs**|Bundled suites of related software|MS Office, Adobe Creative Suite|

---

### 5.2 Operating Systems (OS)

#### Definition and Importance

The **OS** is the master system software that:

- Acts as an **interface** between the user and hardware
- Manages all system **resources**

#### Core OS Functions

|Function|Manages|
|---|---|
|**Memory Management**|Allocates and deallocates RAM to programs|
|**Process Management**|Controls running programs (scheduling, multitasking)|
|**Device Management**|Manages I/O devices through device drivers|
|**File Management**|Organises and controls access to files and directories|

#### Types of Operating Systems

|Type|Description|
|---|---|
|**Batch OS**|Processes jobs in batches without user interaction|
|**Real-Time OS (RTOS)**|Responds to inputs immediately (e.g., aircraft control, medical devices)|
|**Multi-user OS**|Multiple users access the system simultaneously|
|**Multi-tasking OS**|Runs multiple programs concurrently on one machine|
|**Network OS**|Manages network resources and user access|
|**Mobile OS**|Designed for smartphones and tablets|

#### User Interfaces

|Interface|Description|
|---|---|
|**GUI** (Graphical User Interface)|Icons, windows, mouse-driven; user-friendly|
|**Command-Line Interface (CLI)**|Text commands typed by user; powerful but requires knowledge|
|**Menu-Driven**|User selects options from on-screen menus|

#### Specific Operating Systems

|OS|Key Feature|
|---|---|
|**DOS**|Disk Operating System; text-based CLI; studied for internal structure (kernel, shell, command processor)|
|**Windows**|GUI-based; most widely used desktop OS|
|**Linux**|Open-source; **kernel** manages hardware; **shell** is the user interface layer|
|**Mac OS**|Apple's Unix-based OS; known for stability and design|
|**Android**|Linux-based mobile OS|
|**iOS**|Apple's mobile OS|

#### The Booting Process

**Booting** is the process of starting up a computer.

|Type|Description|
|---|---|
|**Cold Boot**|Starting from a completely powered-off state|
|**Warm Boot**|Restarting without full power-off (e.g., Ctrl+Alt+Del or software restart)|

**Boot Sequence:**

```
Power ON → BIOS activates → POST (Power-On Self-Test) → OS Loader → OS starts
```

> 📌 **POST** checks that essential hardware (RAM, CPU, keyboard, storage) is functioning before the OS loads.

---

### 5.3 Programming Languages

#### Evolution of Languages

|Level|Type|Description|Example|
|---|---|---|---|
|**Low-Level**|Machine Language|Binary (0s and 1s); directly executed by CPU|`10110000 01100001`|
|**Low-Level**|Assembly Language|Mnemonic codes; one-to-one with machine instructions|`MOV AX, 1`|
|**High-Level**|—|Human-readable syntax; must be translated|C, Python, Java|

#### Language Translators

|Translator|Works On|How It Works|
|---|---|---|
|**Assembler**|Assembly → Machine code|Converts assembly mnemonics to binary|
|**Compiler**|High-level → Machine code|Translates the **entire** program at once; produces executable|
|**Interpreter**|High-level → Machine code|Translates and executes **line by line**; slower but easier to debug|

---

### 5.4 Utility and Application Software

|Software|Function|
|---|---|
|**Antivirus**|Detects and removes malware|
|**Disk Tools**|Disk defragmenter, disk cleaner, partition manager|
|**MS Office Package**|Word (documents), Excel (spreadsheets), PowerPoint (presentations), Access (database)|

---

## Module 6

## Data Representation and Processing

### 6.1 Data vs. Information

|Term|Definition|
|---|---|
|**Data**|Raw, unprocessed facts and figures (e.g., "42", "Dhaka")|
|**Information**|Processed, meaningful, and useful output derived from data|

**The Data Processing Cycle:**

```
Input (Data) → Processing → Output (Information) → Storage → Feedback
```

---

### 6.2 Data Representation

|Unit|Description|
|---|---|
|**Bit**|Smallest unit; a single binary digit (0 or 1)|
|**Byte**|8 bits; can represent one character|
|**KB** (Kilobyte)|1,024 Bytes|
|**MB** (Megabyte)|1,024 KB|
|**GB** (Gigabyte)|1,024 MB|
|**TB** (Terabyte)|1,024 GB|
|**PB** (Petabyte)|1,024 TB|

---

### 6.3 Coding Systems

|System|Full Name|Bits|Description|
|---|---|---|---|
|**BCD**|Binary Coded Decimal|4 bits per digit|Represents each decimal digit in binary|
|**ASCII**|American Standard Code for Information Interchange|7/8 bits|Standard for English text (128 or 256 characters)|
|**EBCDIC**|Extended Binary Coded Decimal Interchange Code|8 bits|IBM's alternative to ASCII; used in mainframes|

#### Parity Bit System

A **parity bit** is added to data to detect transmission errors:

|Type|Rule|Purpose|
|---|---|---|
|**Even Parity**|Total 1-bits must be even|If odd number received → error detected|
|**Odd Parity**|Total 1-bits must be odd|If even number received → error detected|

---

### 6.4 Database Management Systems (DBMS)

#### Traditional File Processing — Limitations

- Data **redundancy** (same data stored in multiple files)
- Data **inconsistency** (different versions of the same data)
- Difficulty in **concurrent access**
- Poor **security** control

#### DBMS Concepts

|Term|Definition|
|---|---|
|**Database**|An organised collection of structured data|
|**DBMS**|Software that manages, accesses, and controls a database|
|**Field**|A single attribute (e.g., Name, Age) — one column|
|**Record**|A complete set of fields for one entity — one row|
|**Table**|A collection of records for the same entity type|

**Basic Data Manipulation Operations:**

- **Insert** — Add new records
- **Delete** — Remove records
- **Update** — Modify existing records
- **Query/Retrieve** — Search and display specific records

---

## Module 7

## Computer Networks and Internet Systems

### 7.1 Networking Fundamentals

**Goals of Networking:**

- **Resource Sharing** — Share printers, files, internet connections
- **Communication** — Email, messaging, video calls
- **Centralised Data Management** — One server, multiple users

**Risks:** Unauthorised access, virus spreading, data theft, single point of failure.

---

### 7.2 Network Classifications (by Geographic Scope)

|Type|Full Name|Range|Example|
|---|---|---|---|
|**PAN**|Personal Area Network|~10 metres|Bluetooth devices around a person|
|**LAN**|Local Area Network|Building / Campus|Office network, school lab|
|**MAN**|Metropolitan Area Network|City-wide|City cable TV network|
|**WAN**|Wide Area Network|Country / Global|The Internet|

---

### 7.3 Network Topology

The **physical layout** of how devices are connected:

|Topology|Structure|Advantage|Disadvantage|
|---|---|---|---|
|**Bus**|All devices on a single cable|Simple, cheap|One break disables all|
|**Star**|All connected to a central hub/switch|Easy to manage; fault isolation|Hub failure disables all|
|**Ring**|Devices connected in a circle|Orderly data flow (token passing)|One failure can break the ring|
|**Mesh**|Every device connected to every other|Highly reliable, redundant|Expensive, complex wiring|
|**Tree**|Hierarchical; root connects to branches|Scalable|Root failure affects all|
|**Hybrid**|Combination of topologies|Flexible|Complex design|

> 📌 **Choice factors:** Cost, scalability, fault tolerance, ease of maintenance, and network size.

---

### 7.4 Networking Hardware

|Device|Function|
|---|---|
|**Router**|Connects different networks; determines best path for data packets|
|**Switch**|Connects devices within a LAN; smarter than a hub (sends to specific device)|
|**Hub**|Connects devices in a LAN; broadcasts to all devices (less efficient)|
|**Gateway**|Connects networks with different protocols; acts as a translator|
|**Modem**|**Mo**dulates (digital → analog) and **dem**odulates (analog → digital); connects to ISP|

---

### 7.5 Internet and Web Services

|Term|Description|
|---|---|
|**WWW** (World Wide Web)|A system of interlinked web pages accessed via the Internet|
|**Web Browser**|Software to access and display web pages (e.g., Chrome, Firefox)|
|**Search Engine**|Tool to search and index web content (e.g., Google, Bing)|
|**HTTP**|HyperText Transfer Protocol; rules for transferring web pages|
|**IP**|Internet Protocol; rules for addressing and routing data packets|

> ⚠️ **Browser vs. Search Engine:** A browser is an **application**; a search engine is a **website/service** accessed through the browser.

---

### 7.6 Intranet vs. Extranet

|Type|Access|Description|
|---|---|---|
|**Intranet**|Internal (employees only)|Private network using internet technology within an organisation|
|**Extranet**|Limited external access|Intranet extended to specific outside users (e.g., partners, suppliers)|

---

### 7.7 Cloud Computing

**Cloud Computing** is the delivery of computing services (servers, storage, databases, software) over the Internet **on-demand**.

|Feature|Description|
|---|---|
|**Scalability**|Resources can be scaled up or down as needed|
|**On-demand delivery**|Pay only for what you use; no need to own hardware|

---

## Module 8

## Computer Security and Future Trends

### 8.1 Types of Malware and Threats

|Threat|Description|
|---|---|
|**Virus**|Attaches to legitimate files and spreads when files are shared|
|**Worm**|Self-replicating; spreads through networks without human action|
|**Trojan Horse**|Disguises itself as useful software but causes harm in the background|
|**Spyware**|Secretly collects user information and sends it to a third party|
|**Ransomware**|Encrypts the victim's files and demands payment for decryption|
|**Phishing**|Fraudulent emails/websites tricking users into revealing credentials|
|**Logic Bomb**|Malicious code that activates when specific conditions are met|

---

### 8.2 Spreading Mechanisms and Protection

**How malware spreads:**

- Infected email attachments
- Malicious websites and downloads
- Infected USB/pen drives
- Network vulnerabilities

**Protection Methods:**

|Method|Function|
|---|---|
|**Antivirus Software**|Detects, quarantines, and removes known malware|
|**Firewall**|Monitors and controls incoming/outgoing network traffic based on rules|

---

### 8.3 Hacking vs. Cracking

|Term|Meaning|
|---|---|
|**Hacking**|Gaining unauthorised access; can be ethical (white hat) or malicious (black hat)|
|**Cracking**|Strictly malicious; breaking into systems or bypassing software protection for harmful purposes|

---

### 8.4 Future Trends in Computing

|Trend|Description|
|---|---|
|**Pipelining**|Improved CPU architecture where multiple instructions are processed in overlapping stages — increases throughput|
|**Nanotechnology**|Use of materials at the nanometre scale; **carbon nanotubes** as potential replacements for silicon transistors|
|**Tera-Scale Computing**|Processing trillions of operations per second; supports massive parallel workloads|
|**3D Chips**|Stacking processor and memory layers vertically to reduce distance, increase speed, and save space|

---

## Quick Reference Summary

|Module|Core Topic|Key Terms|
|---|---|---|
|1|Computer Basics and History|Generations, Analog/Digital/Hybrid, Mainframe/Supercomputer|
|2|Hardware and Architecture|CPU, ALU, CU, Machine Cycle, Buses, Ports|
|3|Memory and Storage|RAM, ROM, Cache, HDD, SSD, Optical, Virtual Memory|
|4|Peripherals|Keyboard, Scanner, OMR, OCR, CRT, LCD, Impact/Non-impact Printers|
|5|Software and OS|System/Application Software, OS Types, Booting, Compiler vs. Interpreter|
|6|Data Representation|Bit/Byte, ASCII, BCD, EBCDIC, Parity Bit, DBMS|
|7|Networks and Internet|LAN/WAN, Topology, Router/Switch, WWW, Cloud Computing|
|8|Security and Future|Virus/Worm/Trojan, Firewall, Pipelining, Nanotechnology, 3D Chips|

---
_CSE 1111 — Introduction to Computer Systems  | Dept. of CSE, University of Rajshahi_







