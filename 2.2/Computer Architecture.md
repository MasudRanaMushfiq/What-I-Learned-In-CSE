

# Computer Architecture and Organization

### Course Information
**Course:** CSE 2231 (Computer Architecture and Organization)
**Course Type:** Theory, 3 Credit
**Prerequisite:** EEE1131: Basic Electronics, CSE2111: Digital System Design
### Instructor
Dr. Md. Ekramul Hamid, Professor, Dept. of CSE, University of Rajshahi

### Course Motivation
> To develop basics and design knowledge on Computer Architecture and Systems.

---

## Course Contents

| Area | Topics Covered |
| ---- | -------------- |
| **Concepts and Terminology** | Digital computer components Hardware & Software and their dual nature, recent development, Role of Operating Systems (OS) |
| **Processor Design** | Introduction: Processor organization, information representation, number formats; Fixed Point Arithmetic: Addition, subtraction, multiplication, division; ALU Design: Basic ALU organization, floating point arithmetic |
| **Control Design** | Hardwired control: Design methods, multiplier control unit, CPU control unit; Basic concept of Micro programmed Control, Control memory optimization |
| **Memory Devices and its Organization** | Different types of semiconductor memory, magnetic memory, optical memory, virtual memory, memory hierarchies; High-speed Memories: Interleaved memories, caches, associative memories |
| **System Organization** | Communications: Introduction, bus control; IO Systems: Programmed IO, DMA and interrupts, IO processors |
| **Application HDL for microcomputer design** | Description of Adder, ALU by using HDL, implementation of a simple microcomputer system using HDL |

---

## Textbooks

**Primary Texts:**
1. John P. Hayes — *Computer Architecture and Organization*, McGraw-Hill
2. M. Morris Mano — *Computer Architecture*, Prentice Hall

---

## Table of Contents

1. [Chapter 1 – Introduction to Computer Architecture and Organization](#chapter-1)
2. [Chapter 2 – Computer Evolution and Performance Models](#chapter-2)
3. [Chapter 3 – Computer Arithmetic and ALU](#chapter-3)
4. [Chapter 4 – Instruction Set Architecture (ISA)](#chapter-4)
5. [Chapter 5 – Processor Structure and Function](#chapter-5)
6. [Chapter 6 – Control Unit Operation and Control Design](#chapter-6)
7. [Chapter 7 – Memory Devices and Organization](#chapter-7)
8. [Chapter 8 – System Organization (I/O and Bus)](#chapter-8)
9. [Chapter 9 – Application HDL for Microcomputer Design](#chapter-9)

---

## Chapter 1
## Introduction to Computer Architecture and Organization

### 1.1 Concepts and Terminology (Digital Computer Components, Hardware & Software)

- **Computer Architecture:** Refers to the attributes of a system visible to a programmer, such as the instruction set, data types, and I/O mechanisms. These attributes have a direct impact on the logical execution of a program.
- **Computer Organization:** Refers to the operational units and their interconnections that realize the architectural specifications. This includes hardware details transparent to the programmer, such as control signals and memory technology.
- **Digital computer components Hardware & Software and their dual nature, recent development, Role of Operating Systems (OS):** Digital computers consist of both hardware (physical components like CPU, memory, I/O devices) and software (programs and data). They have a dual nature: hardware executes software instructions, and software controls hardware operations. Recent developments include multi-core processors, cloud computing, and AI accelerators. The Operating System (OS) acts as an intermediary between hardware and application software, managing resources, scheduling tasks, and providing a virtual machine interface.

### 1.2 Structure vs. Function

- **Structure vs. Function:** **Structure** is the way components are interrelated, while **Function** is the operation of individual components as part of that structure.
- **Core Functions:** A computer performs four basic functions: data processing, data storage, data movement, and control.
- **Top-Level Structure:** The main components are the Central Processing Unit (CPU), Main Memory, Input/Output (I/O), and the System Interconnection (System Bus).

---

## Chapter 2
## Computer Evolution and Performance Models

### 2.1 IAS Computer (von Neumann Machine)

- **IAS Computer (von Neumann Machine):** A foundational model where data and instructions are stored in a single read-write memory. It consists of 1000 storage locations (words) of 40 bits each.

### 2.2 Harvard Architecture

- **Harvard Architecture:** Unlike von Neumann, this architecture uses separate memory and buses for data and instructions, allowing parallel access and faster execution.

### 2.3 Flynn's Classification

- **Flynn's Classification:** A method of organizing multiple processor systems based on the number of instruction and data streams:
    - **SISD:** Single Instruction, Single Data.
    - **SIMD:** Single Instruction, Multiple Data.
    - **MISD:** Multiple Instruction, Single Data.
    - **MIMD:** Multiple Instruction, Multiple Data.

### 2.4 Performance Metrics

- **Performance Metrics:**
    - **CPI (Cycles Per Instruction):** The average number of clock cycles required to execute an instruction.
    - **MIPS (Millions of Instructions Per Second):** A rate of instruction execution.
    - **Amdahl's Law:** Explains the overall speedup of a system when only a portion of it is enhanced.

---

## Chapter 3
## Computer Arithmetic and ALU

The Arithmetic and Logic Unit (ALU) is the part of the computer that actually processes data.

### 3.1 Processor Design: Information Representation, Number Formats

- **Processor Design: Introduction: Processor organization, information representation, number formats:** Processor organization involves the arrangement of registers, ALU, and control logic. Information representation includes how data (integers, floating-point numbers, characters) is encoded in binary. Number formats include fixed-point (integer) and floating-point representations.

### 3.2 Integer Representation

- **Integer Representation:**
    - **Sign-Magnitude:** Leftmost bit is the sign (0 for positive, 1 for negative).
    - **Two's Complement:** Used to represent negative integers by taking the Boolean complement of each bit of the positive number and adding 1. It simplifies hardware design for addition and subtraction.

### 3.3 Fixed Point Arithmetic: Addition, Subtraction, Multiplication, Division

- **Fixed Point Arithmetic: Addition, subtraction, multiplication, division:** Fixed-point arithmetic operations are performed on integer values. Addition and subtraction use standard binary addition with two's complement for negatives. Multiplication includes Booth's Algorithm. Division includes Restoring and Non-Restoring algorithms.

### 3.4 Floating-Point Arithmetic (IEEE 754)

- **Floating-Point (IEEE 754):** Numbers are represented by a sign bit, a biased exponent, and a significand (mantissa). Single precision uses 32 bits (1 sign, 8 exponent, 23 mantissa).

### 3.5 Arithmetic Algorithms

- **Arithmetic Algorithms:**
    - **Multiplication:** Booth's Algorithm is a high-speed method for multiplying signed integers.
    - **Division:** Includes Restoring and Non-Restoring algorithms.

### 3.6 Adders

- **Adders:**
    - **Ripple Carry Adder:** Simple but slow as carry bits must propagate through each stage.
    - **Carry-Lookahead Adder (CLA):** Faster because it predicts carry values in advance.

### 3.7 ALU Design: Basic ALU Organization

- **ALU Design: Basic ALU organization, floating point arithmetic:**
    - **ALU Types:** **Combinational ALUs** compute outputs instantly without storage, whereas **Sequential ALUs** use storage elements (flip-flops) and are clock-driven to perform multi-step operations like division.

---

## Chapter 4
## Instruction Set Architecture (ISA)

- **Instruction Elements:** An opcode (operation code), source operand references, and result operand references.
- **Instruction Formats:** These define the layout of bits, specifying the opcode and addresses. They vary from 3-address to 0-address (stack-based) formats.
- **Addressing Modes:**
    - **Immediate:** Operand is in the instruction.
    - **Direct:** Address field contains the memory address of the operand.
    - **Indirect:** Address field points to a memory location that contains the address of the operand.
    - **Register:** Operand is held in a CPU register.
- **RISC vs. CISC:**
    - **RISC (Reduced Instruction Set Computer):** Uses a small set of simple, fixed-length instructions that execute in one clock cycle. **Example:** ARM, MIPS.
    - **CISC (Complex Instruction Set Computer):** Uses a large set of complex, variable-length instructions that may take multiple cycles. **Example:** x86 (Intel/AMD).

---

## Chapter 5
## Processor Structure and Function

### 5.1 CPU Registers

- **CPU Registers:**
    - **PC (Program Counter):** Points to the next instruction.
    - **MAR (Memory Address Register):** Holds the address of the location in memory being accessed.
    - **MBR/MDR (Memory Buffer/Data Register):** Contains the data to be written to or read from memory.
    - **IR (Instruction Register):** Holds the most recently fetched instruction.

### 5.2 Instruction Cycle

- **Instruction Cycle:** Consists of Fetch, Decode, Execute, and sometimes Interrupt cycles.

### 5.3 Pipelining

- **Pipelining:** A technique that overlaps instruction processing stages to increase performance. For a 5-stage pipeline, stages are typically: Fetch, Decode, Execute, Memory, and Write Back.

### 5.4 Superscaling

- **Superscaling:** Allows multiple instructions to be processed in parallel across multiple execution units.

---

## Chapter 6
## Control Unit Operation and Control Design

The Control Unit (CU) generates control signals to sequence through micro-operations.

### 6.1 Hardwired Control

- **Hardwired control: Design methods, multiplier control unit, CPU control unit:**
    - **Hardwired Control:** Implementation using logic gates and flip-flops. It is fast but inflexible. Methods include the **One-Hot method** (one flip-flop per state) and **Classical methods**.
    - **Design methods, multiplier control unit, CPU control unit:** These methods involve designing combinational logic circuits that generate control signals based on the current state and instruction opcode. Specific control units include the multiplier control unit (manages multiplication operations) and the CPU control unit (manages overall instruction execution).

### 6.2 Microprogrammed Control

- **Basic concept of Micro programmed Control, Control memory optimization:**
    - **Microprogrammed Control:** Control logic is stored in a control memory as microinstructions (a sequence of micro-operations). It is more flexible and easier to modify than hardwired control but slower.
    - **Control memory optimization:** Techniques to reduce the size of control memory, such as horizontal vs. vertical microprogramming, microsubroutines, and bit-steering.

---

## Chapter 7
## Memory Devices and Organization

### 7.1 Different Types of Semiconductor Memory, Magnetic Memory, Optical Memory

- **Different types of semiconductor memory, magnetic memory, optical memory, virtual memory, memory hierarchies:**
    - **Semiconductor Memory:** RAM (SRAM, DRAM) and ROM (PROM, EPROM, EEPROM, Flash).
    - **Magnetic Memory:** Hard disk drives (HDD), magnetic tape.
    - **Optical Memory:** CD, DVD, Blu-ray.

### 7.2 Virtual Memory

- **Virtual memory:** A technique that uses secondary storage (disk) as an extension of main memory, allowing programs larger than physical memory to run and providing address space isolation between processes.

### 7.3 Memory Hierarchies

- **memory hierarchies:** A hierarchical arrangement of memory levels (registers, cache, main memory, secondary storage) with different speeds, costs, and capacities. The goal is to provide the illusion of fast, large, cheap memory.

### 7.4 High-Speed Memories

- **High-speed Memories: Interleaved memories, caches, associative memories:**
    - **Interleaved memories:** Memory divided into multiple banks that can be accessed in parallel, reducing average access time.
    - **Caches:** Small, fast memory that stores frequently accessed data to reduce average memory access time. Cache organization includes direct-mapped, fully associative, and set-associative.
    - **Associative memories (Content-Addressable Memory - CAM):** Memory that allows searching by content (data value) rather than by address.

---

## Chapter 8
## System Organization (I/O and Bus)

### 8.1 Communications: Introduction, Bus Control

- **System Organization: Communications: Introduction, bus control:**
    - **Communications: Introduction, bus control:** A system bus is a set of parallel wires that connects the CPU, memory, and I/O devices. Bus control involves arbitration (deciding which device gets bus access) and protocol (timing and signaling rules).

### 8.2 IO Systems: Programmed IO, DMA and Interrupts, IO Processors

- **IO Systems: Programmed IO, DMA and interrupts, IO processors:**
    - **Programmed I/O:** The CPU repeatedly checks the I/O device status (polling). Simple but inefficient as the CPU wastes cycles waiting.
    - **Interrupts:** The I/O device signals the CPU when it is ready, allowing the CPU to perform other work. Saves CPU cycles.
    - **DMA (Direct Memory Access):** A special controller transfers data directly between I/O device and memory without CPU intervention for each byte. Highly efficient for large data transfers.
    - **IO processors:** Specialized processors dedicated to handling I/O operations, offloading this work from the main CPU.

---

## Chapter 9
## Application HDL for Microcomputer Design

- **Application HDL for microcomputer design: Description of Adder, ALU by using HDL, implementation of a simple microcomputer system using HDL:**
    - **Description of Adder, ALU by using HDL:** Hardware Description Languages (such as VHDL or Verilog) are used to describe digital circuits at various abstraction levels. An adder (e.g., ripple-carry or carry-lookahead) and an ALU (supporting arithmetic and logic operations) can be modeled in HDL using behavioral or structural descriptions.
    - **implementation of a simple microcomputer system using HDL:** A complete simple microcomputer system (including CPU, memory, and I/O interfaces) can be described in HDL, simulated for verification, and synthesized to run on an FPGA.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Introduction to Computer Architecture and Organization | Computer Architecture, Computer Organization, Hardware, Software, OS, Structure, Function, Core Functions (Data Processing, Data Storage, Data Movement, Control), CPU, Main Memory, I/O, System Bus |
| 2 | Computer Evolution and Performance Models | IAS (von Neumann), Harvard Architecture, Flynn's Classification (SISD, SIMD, MISD, MIMD), CPI, MIPS, Amdahl's Law |
| 3 | Computer Arithmetic and ALU | ALU, Sign-Magnitude, Two's Complement, IEEE 754, Floating-Point, Booth's Algorithm, Restoring/Non-Restoring Division, Ripple Carry Adder, Carry-Lookahead Adder CLA, Combinational ALU, Sequential ALU |
| 4 | Instruction Set Architecture (ISA) | Opcode, Instruction Formats (3-address to 0-address), Addressing Modes (Immediate, Direct, Indirect, Register), RISC (ARM, MIPS), CISC (x86) |
| 5 | Processor Structure and Function | PC, MAR, MBR/MDR, IR, Instruction Cycle (Fetch, Decode, Execute, Interrupt), Pipelining (5-stage: Fetch, Decode, Execute, Memory, Write Back), Superscaling |
| 6 | Control Unit Operation | Hardwired Control, One-Hot Method, Microprogrammed Control, Control Memory, Control Memory Optimization |
| 7 | Memory Devices and Organization | Semiconductor Memory (RAM, ROM), Magnetic Memory (HDD), Optical Memory (CD, DVD), Virtual Memory, Memory Hierarchies, Interleaved Memory, Cache, Associative Memory (CAM) |
| 8 | System Organization | System Bus, Bus Control, Programmed I/O, Interrupts, DMA, IO Processors |
| 9 | Application HDL for microcomputer design | HDL (VHDL/Verilog), Adder Description, ALU Description, Microcomputer System Implementation on FPGA |

---
*CSE 2231 — Computer Architecture and Organization | Dept. of CSE, University of Rajshahi*




