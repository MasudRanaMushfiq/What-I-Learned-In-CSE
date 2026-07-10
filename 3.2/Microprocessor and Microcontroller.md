

# Microprocessor and Microcontroller

### Course Information
**Course:** CSE 3231 (Microprocessor and Microcontroller)
**Course Type:** Theory, 3 Credit
**Prerequisite:** CSE2111: Digital System Design, CSE2231: Computer Architecture and Organization
### Instructor
Mr. Md. Morshedul Arefin, Associate Professor, Dept. of CSE, University of Rajshahi
Dr. Md. Rokanujjaman, Professor, Dept. of CSE, University of Rajshahi 

### Course Motivation
> To develop knowledge on Microprocessor and Microcontroller architecture and programming skills with STM32 microcontroller.

---

## Course Contents

| Area                             | Topics Covered                                                                                                                               |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Microprocessor Fundamentals**  | Architecture of 8085 and 8086 microprocessors, including execution and bus-interface units, registers, flags, and the 8086 programming model |
| **Cortex®-M3 processor (STM32)** | Programmers model, execution privilege levels, stacks, core registers, and exceptions/interrupts                                             |
| **Cortex®-M3 Memory model**      | Regions, types, attributes, access ordering, bit-banding, endianness, and synchronization primitives                                         |
| **Exception model**              | Types, handlers, priorities, and power management (sleep modes)                                                                              |

---

## Textbooks

**Primary Texts:**
1. STMicroelectronics — *Reference manuals and programming manuals for STM32F10xxx series*

---

## Table of Contents

1. [Chapter 1 – Introduction to Microcomputer Systems](#chapter-1)
2. [Chapter 2 – Intel 8085 Microprocessor (8-bit)](#chapter-2)
3. [Chapter 3 – Intel 8086 Architecture (16-bit)](#chapter-3)
4. [Chapter 4 – Assembly Language Programming (8086)](#chapter-4)
5. [Chapter 5 – ARM Cortex-M3 Processor (STM32)](#chapter-5)
6. [Chapter 6 – Cortex-M3 Memory Model](#chapter-6)

---

## Chapter 1
## Introduction to Microcomputer Systems

### 1.1 Fundamentals

**Definition of Microprocessor:** A single integrated circuit (IC) containing the arithmetic, logic, and control units of a computer; essentially the "brain" of a microcomputer.

**The Microcomputer System:** Comprised of the Central Processing Unit (CPU), Memory (RAM/ROM), and Input/Output (I/O) units.

**Microprocessor vs. Microcontroller:**
- **Microprocessor:** Contains only the CPU on a single chip; requires external memory and I/O chips.
- **Microcontroller:** A "true computer on a single chip," integrating the CPU, memory, timers, and I/O ports.

**Evolution:** Progressed from 8-bit (8085) to 16-bit (8086) and 32-bit (80386/ARM Cortex-M3) architectures, increasing data path width and memory addressability.

---

### 1.2 Important Concepts

**Pipelining:** Overlapping the fetch and execute cycles to improve processor throughput.

**Stack:** A LIFO (Last-In, First-Out) data structure used for temporary storage, procedure calls, and interrupts.

**Interrupts:** Signals that temporarily halt the main program to execute a specific Interrupt Service Routine (ISR).

**Program Segment Prefix (PSP):** A 256-byte control block created by DOS at the start of a program's memory segment to manage execution.

**Memory-Mapped I/O:** Treating I/O ports as memory locations, using the same instructions for both (e.g., `MOV`).

**Isolated I/O:** Using a separate address space and dedicated instructions (`IN`, `OUT`) for I/O ports.

---

## Chapter 2
## Intel 8085 Microprocessor (8-bit)

### 2.1 Intel 8085 Microprocessor (8-bit)

Introduced in 1977, the 8085 is an 8-bit microprocessor built using **N-MOS technology**. It is widely used in inexpensive, low-speed applications and serves as a classic model for learning microprocessor architecture.

- **Architecture and Registers:**
    - **Word Size:** It processes **8 bits of data** at a time.
    - **Accumulator (A):** An 8-bit register used for all arithmetic and logic operations; it also serves as the primary destination for results.
    - **General Purpose Registers:** Six 8-bit registers (B, C, D, E, H, L) that can be paired (BC, DE, HL) to handle 16-bit data. The **HL pair** often acts as a memory pointer.
    - **Program Counter (PC):** A 16-bit register that holds the address of the next instruction to be executed.
    - **Stack Pointer (SP):** A 16-bit register pointing to the top of the stack in RAM (LIFO logic).
- **Memory and Bus:**
    - **Address Capacity:** It has a **16-bit address bus**, allowing it to address up to **64 KB** of memory.
    - **Multiplexing:** To save pins, the lower 8 bits of the address (A0-A7) and the 8-bit data bus (D0-D7) are multiplexed onto the same pins (**AD0-AD7**). The **ALE (Address Latch Enable)** signal is used to distinguish between them.
- **Flags:** The 8085 has a 5-bit active flag register: **Carry (CY)**, **Parity (P)**, **Auxiliary Carry (AC)**, **Zero (Z)**, and **Sign (S)**.
- **Interrupts:** It supports five hardware interrupts: **TRAP** (highest priority, non-maskable), **RST 7.5**, **RST 6.5**, **RST 5.5**, and **INTR** (lowest priority).

---

## Chapter 3
## Intel 8086 Architecture (16-bit)

### 3.2 Intel 8086 Microprocessor (16-bit)

The 8086, introduced in 1978, is a **16-bit processor** designed using **HMOS technology**. It significantly advanced processing speed through its internal organization and larger memory reach.

- **Internal Organization (BIU and EU):** The 8086 is divided into two independent functional units to enable **pipelining**:
    - **Bus Interface Unit (BIU):** Handles all external bus operations, including fetching instructions, reading/writing data, and maintaining a **6-byte instruction prefetch queue**.
    - **Execution Unit (EU):** Decodes and executes instructions from the queue using the 16-bit ALU and general registers.
- **Memory Management and Segmentation:**
    - **Address Capacity:** With a **20-bit address bus**, it can address up to **1 MB** of memory.
    - **Segmentation:** The 1 MB space is divided into logical segments of **64 KB**. Four segment registers in the BIU manage this: **CS** (Code), **DS** (Data), **SS** (Stack), and **ES** (Extra).
    - **Physical Address Calculation:** The 8086 uses a 16-bit segment value and a 16-bit offset. The formula is: `Physical Address = (Segment Register × 10H) + Offset`.
- **Memory Banking:** Memory is physically implemented in two **512 KB banks**: the **Even (Lower) Bank** (D0-D7) and the **Odd (Upper) Bank** (D8-D15). Accessing a word at an even address takes one bus cycle, while an odd address requires two.
- **Registers and Flags:**
    - **General Registers:** AX (Accumulator), BX (Base), CX (Count), and DX (Data). Each can be split into high/low 8-bit registers (e.g., AX into AH/AL).
    - **Flags:** It features a 16-bit FLAGS register with **9 active flags**: 6 status flags (Carry, Parity, Auxiliary Carry, Zero, Sign, Overflow) and 3 control flags (Trap, Interrupt, Direction).
- **Operating Modes:** It can be configured in **Minimum Mode** (single processor) or **Maximum Mode** (multiprocessor systems) using the MN/MX pin.

Comparison Summary

|Feature|Intel 8085|Intel 8086|
|---|---|---|
|**Data Bus**|8-bit|16-bit|
|**Address Bus**|16-bit|20-bit|
|**Memory Capacity**|64 KB|1 MB|
|**Pipelining**|No|Yes (6-byte queue)|
|**Arithmetic**|Basic (No Hardware Mul)|Powerful (Hardware Mul/Div)|
|**Memory Structure**|Linear|Segmented|
|**Active Flags**|5|9|
|**Vectored Interrupts**|4|256|.

---

### 3.2 Memory Segmentation and Banking

**Memory Segmentation:** Addresses a **1 MB** space by dividing it into 64 KB logical segments.

**Physical Address Calculation:** `Physical Address = (Segment Register × 10H) + Offset`.

> 💡 **Example 1: Physical Address Calculation (8086):**
> If `CS = 0A32H` and `IP = 0028H`:
> `Physical Address = (0A32H × 10H) + 0028H = 0A320H + 0028H = 0A348H`.

**Memory Banking:** Memory is split into an **Even (Lower) Bank** (D0-D7) and an **Odd (Upper) Bank** (D8-D15). Accessing a 16-bit word at an odd address requires two bus cycles, whereas an even address requires only one.

**8085 vs 8086:** 8085 is 8-bit/64KB memory; 8086 is 16-bit/1MB memory with pipelining and segmentation.

---

## Chapter 4
## Assembly Language Programming (8086)

### 4.1 Program Structure and Directives

**Assembly Language Programming (8086):** Assembly language is a low-level programming language that has a strong correspondence between its instructions and the architecture's machine code instructions.

**Statement Fields:** `Name`, `Operation` (opcode or pseudo-op), `Operand(s)`, and `Comment` (starts with `;`).

**Assembler Directives (Pseudo-ops):**
- **Data Definition:** `DB` (Byte), `DW` (Word), `DD` (Doubleword).
- **Memory Models:** `.MODEL SMALL` (one code, one data segment).
- **Segment Directives:** `.DATA`, `.CODE`, `.STACK`.

---

### 4.2 Addressing Modes

**Addressing Modes:**
1.  **Register:** Operand is in a register (e.g., `MOV AX, BX`).
2.  **Immediate:** Operand is a constant (e.g., `MOV AL, 5`).
3.  **Direct:** Operand is a variable/memory address (e.g., `MOV AX, [1000H]`).
4.  **Register Indirect:** Register holds the offset (e.g., `MOV AX, [SI]`).
5.  **Based/Indexed:** Offset = Base/Index Register + Displacement (e.g., `MOV AX, [BX+4]`).

**Addressing Recap:** Always check register sizes (e.g., `MOV AX, BL` is illegal) and avoid direct memory-to-memory moves.

---

### 4.3 Key Instruction Groups

**Key Instruction Groups:**
- **Data Transfer:** `MOV`, `XCHG`, `PUSH`, `POP`, `LEA`.
- **Arithmetic:** `ADD`, `SUB`, `INC`, `DEC`, `MUL` (unsigned), `IMUL` (signed).
- **Logic:** `AND`, `OR`, `XOR`, `NOT`, `TEST` (affects flags without storing result).
- **Flow Control:** `JMP` (unconditional), `JZ`, `JNZ`, `JC`, `JNC` (conditional), `CALL`, `RET`.

💡 Example 2: Simple 8086 Assembly Program (Add Two Numbers)
```assembly
.MODEL SMALL
.STACK 100H
.DATA
A DW 2
B DW 5
SUM DW ?
.CODE
MAIN PROC
MOV AX, @DATA   ; Initialize Data Segment
MOV DS, AX
MOV AX, A       ; AX = 2
ADD AX, B       ; AX = 2 + 5 = 7
MOV SUM, AX     ; SUM = 7
MOV AX, 4C00H   ; Exit to DOS
INT 21H
MAIN ENDP
END MAIN
```

---

## Chapter 5
## ARM Cortex-M3 Processor (STM32)

### 5.1 Architecture and Programmers Model

**Architecture:** 32-bit RISC with a **3-stage pipeline** (fetch, decode, execute) and **Harvard architecture** (separate buses for code and data).

**Programming Model:**
- **Registers R0-R12:** General-purpose.
- **Stack Pointer (R13):** Two banked versions: **MSP** (Main) and **PSP** (Process).
- **Link Register (R14):** Stores return address.
- **Program Counter (R15):** Points to current instruction.

**Programmers model:** The programmers model defines the set of registers, memory organization, and execution modes visible to the programmer for writing software.

**Execution privilege levels:** The Cortex-M3 supports two privilege levels: **Privileged mode** (full access to all resources) and **Unprivileged mode** (restricted access for user applications). This enforces memory protection and system security.

**Stacks:** The Cortex-M3 uses a full-descending stack (the stack pointer points to the last pushed item, and the stack grows downward in memory). Two stack pointers exist: MSP (used in handler mode and as the default for thread mode) and PSP (used in thread mode when unprivileged).

**Core registers:** The core registers include R0-R12 (general purpose), R13 (Stack Pointer, banked), R14 (Link Register), R15 (Program Counter), and special registers such as the Program Status Register (xPSR), PRIMASK, FAULTMASK, BASEPRI, and CONTROL.

**Exceptions/interrupts:** Exceptions are events that alter the normal program flow. Interrupts are a type of exception triggered by external or internal hardware. The Cortex-M3 includes a **Nested Vectored Interrupt Controller (NVIC)** for efficient interrupt handling with configurable priorities.

---

### 5.2 STM32 Peripherals

**STM32 Peripherals:** Includes **GPIO** (configurable as input/output/alternate function), **ADC** (12-bit, successive approximation), **DMA** (7 or 12 channels for CPU-free data transfer), and various **Timers** (Advanced, General-purpose, Basic).

**Cortex-M3 Perks:** Provides superior power efficiency, 32-bit performance, and simplified interrupt handling (NVIC) compared to older 8/16-bit models.

**STM32 Development:** Typically involves configuring peripherals via **HAL (Hardware Abstraction Layer)** and using IDEs like STM32CubeIDE.

---

## Chapter 6
## Cortex-M3 Memory Model

### 6.1 Memory Organization and Attributes

**Cortex-M3 Memory model:** The Cortex-M3 memory model defines a 4 GB linear address space with predefined regions, each with specific default memory types, attributes, and access ordering rules.

**Memory regions:** The 4 GB address space is divided into regions: Code (0x00000000 – 0x1FFFFFFF), SRAM (0x20000000 – 0x3FFFFFFF), Peripherals (0x40000000 – 0x5FFFFFFF), External RAM (0x60000000 – 0x9FFFFFFF), External Device (0xA0000000 – 0xDFFFFFFF), and System (0xE0000000 – 0xFFFFFFFF including NVIC and MPU).

**Memory types:** Three memory types are defined:
- **Normal memory:** Allows reordering and speculation (used for RAM and Flash).
- **Device memory:** Strictly ordered; no speculation, read/write cannot be reordered (used for peripherals).
- **Strongly-ordered memory:** All accesses complete in program order with no reordering or speculation.

**Memory attributes:** Attributes include cacheability, bufferability, shareability, and execute-never (XN) permissions, which control how the processor interacts with each memory region.

**Access ordering:** Access ordering rules determine how memory accesses are sequenced. For strongly-ordered and device memory, the processor ensures that accesses complete in program order without merging or reordering.

**Bit-banding:** Bit-banding maps individual bits in SRAM and peripherals to a 32 MB "alias" region, allowing **atomic bit manipulation**.

> 💡 **Example 3: Bit-Banding (Cortex-M3)**
> Mapping bit 2 of address `0x20000300` to the alias region:
> Accessing address `0x22006008` (calculated via formula) will directly set or clear that specific bit.

**Endianness:** Endianness defines the byte order in memory. The Cortex-M3 supports both **little-endian** (least significant byte at lowest address) and **big-endian**, with little-endian being the default.

**Synchronization primitives:** Synchronization primitives include the exclusive access instructions (`LDREX` and `STREX`) that enable atomic read-modify-write operations for multi-core and multi-threaded synchronization without disabling interrupts.

## Cortex-M3 Instruction Set
**Cortex-M3 instruction set:** The Cortex-M3 implements the Thumb-2 instruction set (a mixture of 16-bit and 32-bit instructions) that provides high code density combined with powerful operations.

**Operands:** Operands can be registers, immediate constants, or memory addresses. Most instructions support:
- Three-operand format: `ADD Rd, Rn, Rm` (Rd = Rn + Rm)
- Two-operand format: `ADD Rd, Rn` (Rd = Rd + Rn)
- Immediate operands: `ADD Rd, Rn, #immed` (Rd = Rn + constant)

**Shift operations:** Shift operations include:
- **LSL (Logical Shift Left):** Shift left, fill with zeros.
- **LSR (Logical Shift Right):** Shift right, fill with zeros.
- **ASR (Arithmetic Shift Right):** Shift right, preserve sign bit (for signed arithmetic).
- **ROR (Rotate Right):** Circular shift.

Shifts can be performed as separate instructions (`LSL Rd, Rn, #shift`) or as part of another instruction (`ADD Rd, Rn, Rm, LSL #shift`).

**Address alignment:** Most memory access instructions require naturally aligned addresses (e.g., 32-bit word accesses must have address divisible by 4). Unaligned accesses are permitted for certain instructions but may incur a performance penalty.

**Conditional execution:** In Thumb-2, many instructions can be conditionally executed using condition codes (e.g., `ITE`, `ITTE`, `MOVNE`, `ADDPL`). Condition codes include: EQ (equal), NE (not equal), CS/HS (carry set/unsigned higher or same), CC/LO (carry clear/unsigned lower), MI (minus/negative), PL (plus/positive), VS (overflow set), VC (overflow clear), HI (unsigned higher), LS (unsigned lower or same), GE (signed greater or equal), LT (signed less than), GT (signed greater than), LE (signed less or equal), and AL (always).

---

## Quick Reference Summary

| Chapter | Core Topic            | Key Terms                                                                                                                                                                                  |
| ------- | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1       | Microcomputer Systems | Microprocessor (CPU only), Microcontroller (CPU+Memory+I/O on chip), Pipelining, Stack (LIFO), Interrupts (ISR), Memory-Mapped vs. Isolated I/O                                            |
| 2       | Intel 8085 (8-bit)    | 16-bit address bus (64 KB), Accumulator (A), General purpose (B,C,D,E,H,L), PC, SP, ALE, Fetch-Decode-Execute                                                                              |
| 3       | Intel 8086 (16-bit)   | BIU (6-byte queue), EU, Segmentation (1 MB via CS,DS,SS,ES), Physical Address = (Segment × 10H) + Offset, Memory Banking (Even/Odd banks)                                                  |
| 4       | 8086 Assembly         | Directives (DB, DW, .MODEL), Addressing modes (Register, Immediate, Direct, Indirect, Based/Indexed), Instructions (MOV, ADD, JMP, PUSH, POP), Flags (CF, ZF, SF, OF)                      |
| 5       | ARM Cortex-M3 (STM32) | 32-bit RISC, Harvard architecture, 3-stage pipeline, MSP/PSP (R13), LR (R14), PC (R15), Privileged/Unprivileged modes, NVIC, Peripherals (GPIO, ADC, DMA, Timers), HAL, STM32CubeIDE       |
| 6       | Instruction Set       | Thumb-2 (16/32-bit), Intrinsics, Shifts (LSL, LSR, ASR, ROR), Conditional execution (IT, ITE), Memory ops (LDR, STR, PUSH, POP), Data processing (ADD, SUB, AND, ORR), MPU (8 regions, XN) |

---
*CSE 3231 — Microprocessor and Microcontroller | Dept. of CSE, University of Rajshahi*




