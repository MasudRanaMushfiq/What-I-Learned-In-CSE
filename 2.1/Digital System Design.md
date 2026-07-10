

# Digital System Design

### Course Information
**Course:** CSE 2111 (Digital System Design)
**Course Type:** Theory, 3 Credit
**Prerequisite:** CSE1211: Introduction to Digital Electronics
### Instructor
Mahboob Qaosar, Associate Professor, Dept. of CSE, University of Rajshahi

### Course Motivation
> To develop basics and design knowledge on Digital Systems

---

## Course Contents

| Area | Topics Covered |
| --- | --- |
| **Combinational Logic** | Code converters, advanced arithmetic circuits, carry-look-ahead adder, binary parallel adder, BCD adder. Magnitude comparator. |
| **MSI Logic Circuits** | Encoders, decoders, multiplexers, demultiplexers, application of decoder and multiplexer: realizing for min-terms and max-terms, Binary Multiplier Parity generator and checker. |
| **Sequential Circuits** | Latches, flip flops (FF), analysis of clocked sequential circuits, state reduction and assignments. |
| **Registers and Counters** | Registers, shift registers, parallel loading of shift register, counters, synchronous and asynchronous counter, up and down counter, ripple counter, counters using SR and JK FF, design of sequential counter, application of counter: parallel to serial communication, other types of counters. |
| **Memory and Programmable Logic** | Random access memory (RAM), memory addressing, Programmable Array Logic (PAL), Programmable Logic Array (PLA), Introduction to CPLDs, FPGAs. |
| **Introduction to Hardware Description Language (HDL)** | Verilog HDL/VHDL, Syntax and program structure of HDL (Verilog HDL/VHDL). Application of HDL: Description and simulation of common combinational circuits using HDL: Adder, decoder, multiplexer etc. Description and simulation of sequential circuits, registers, counters. |

## Textbooks

**Primary Texts:**
1. Ronald J. Tocci — *Digital Systems: Principles and Applications*, Prentice Hall.
2. M. Morris Mano — *Digital Logic and Computer Design*, Prentice Hall.

---

## Table of Contents

1. [Chapter 1 – Binary Codes and Error Detection](#chapter-1)
2. [Chapter 2 – Combinational Logic Circuits](#chapter-2)
3. [Chapter 3 – MSI Logic Circuits](#chapter-3)
4. [Chapter 4 – Sequential Logic Circuits](#chapter-4)
5. [Chapter 5 – Registers and Counters](#chapter-5)
6. [Chapter 6 – Memory and Programmable Logic](#chapter-6)
7. [Chapter 7 – Hardware Description Language (Verilog HDL)](#chapter-7)

---

## Chapter 1
## Binary Codes and Error Detection

Digital systems use various binary codes to represent information.

### 1.1 Binary Codes

- **Weighted Binary Codes:** These obey the positional weight principle where each bit position has a specific weight, such as **BCD (Binary-Coded Decimal)** using the 8421 weight.
- **Non-Weighted Codes:** Positional weights are not assigned. Examples include:
    - **Excess-3 Code:** Often used in certain arithmetic operations.
    - **Gray Code (Unit Distance Code):** Successive values differ by only one bit position, which minimizes errors during transitions in digital systems.

### 1.2 Error Detection

- **Error Detection (Parity):** A simple method involving adding an extra "parity bit" to binary data.
    - **Even Parity:** The total number of 1s (including the parity bit) is even.
    - **Odd Parity:** The total number of 1s (including the parity bit) is odd.
- **Hamming Code:** A more advanced code used for error detection and correction.

---

## Chapter 2
## Combinational Logic Circuits

In combinational logic, the output depends **only on current inputs** and has no memory of past states.

### 2.1 Adders and Arithmetic Circuits

**Combinational Logic: Code converters, advanced arithmetic circuits:**

- **Adders:**
    - **Parallel Adder (Binary Parallel Adder):** Adds all bits simultaneously; fast but hardware-intensive.
    - **Serial Adder:** Adds bits sequentially one at a time; slower but uses fewer components.
- **Carry-Look-Ahead Adder:** An advanced arithmetic circuit that speeds up addition by computing carry signals in advance, eliminating the ripple delay.
- **BCD Adder:** A circuit that adds two BCD digits and produces a valid BCD output (0-9), with correction logic for sums exceeding 9.
- **Binary Multiplier:** A combinational circuit that multiplies two binary numbers using AND gates and adders.
- **Magnitude Comparator:** A combinational circuit that compares two binary numbers and determines whether they are equal, or which is greater.

### 2.2 Multiplexers and Demultiplexers

- **Multiplexer (MUX):** A digital switch that selects one output from multiple sources based on select lines.
    - **Example:** An MP3 player, laptop, and satellite receiver can all be sources for one surround sound system; the MUX selects which audio plays.
- **Demultiplexer (DEMUX):** The inverse of a MUX; it directs a single input to one of several possible outputs.
    - **Example:** Directing a single computer's print command to either a laser printer, fax machine, or color inkjet.

### 2.3 Decoders and Encoders

- **Decoder:** Converts $n$ coded inputs into a maximum of $2^n$ unique outputs. A common example is the **BCD-to-7-segment decoder**, which converts 4-bit binary digits into signals to drive a digit display (0-9).
- **Encoder:** The inverse of a decoder, converting $2^n$ inputs into $n$ outputs. A **Priority Encoder** specifically outputs the binary code of the highest-priority active input.

### 2.4 MSI Logic Circuits

**MSI logic circuits: Encoders, decoders, multiplexers, demultiplexers, application of decoder and multiplexer: realizing for min-terms and max-terms, Parity generator and checker.**

- **Application of Decoder and Multiplexer:** Using decoders and multiplexers to realize logic functions by implementing min-terms (for SOP) and max-terms (for POS).
- **Parity Generator and Checker:** Circuits that generate the parity bit before transmission and verify the parity bit after reception to detect errors.

---

## Chapter 3
## MSI Logic Circuits

### 3.1 MSI Components Summary

| Component | Function | Application |
| --- | --- | --- |
| **Encoder** | Converts $2^n$ inputs into $n$ outputs | Priority encoders for interrupt handling |
| **Decoder** | Converts $n$ inputs into $2^n$ outputs | BCD-to-7-segment display |
| **Multiplexer (MUX)** | Selects one input from many to output | Data routing, audio/video switching |
| **Demultiplexer (DEMUX)** | Routes one input to one of many outputs | Serial-to-parallel conversion |
| **Parity Generator** | Adds parity bit for error detection | Memory systems, data transmission |
| **Parity Checker** | Verifies parity to detect errors | Communication receivers |

---

## Chapter 4
## Sequential Logic Circuits

Unlike combinational logic, sequential circuit outputs depend on **both current inputs and previous states**, requiring memory elements.

**Sequential Circuits: Latches, flip flops (FF), analysis of clocked sequential circuits, state reduction and assignments.**

### 4.1 Latches vs. Flip-Flops

- **Latches vs. Flip-Flops:**
    - **Latch:** Level-sensitive (changes state while the control signal is high/low) and asynchronous.
    - **Flip-Flop:** Edge-triggered (changes state only on the rising or falling edge of a clock) and synchronous.

### 4.2 Common Flip-Flop Types

- **Common Flip-Flop Types:**
    - **SR (Set-Reset):** Basic storage; has an invalid state when both inputs are 1.
    - **D (Data/Delay):** Stores the input bit on the clock edge; ensures S and R inputs are never 1 simultaneously.
    - **JK:** Similar to SR but has a "toggle" mode when both inputs are 1, eliminating the invalid state.
    - **T (Toggle):** Reverses its state if the input is 1 and holds it if 0.

### 4.3 Timing Constraints

- **Timing Constraints:**
    - **Setup Time ($t_S$):** Minimum time the input must be stable **before** the clock edge.
    - **Hold Time ($t_H$):** Minimum time the input must remain stable **after** the clock edge.

### 4.4 State Reduction and Assignments

- **Analysis of clocked sequential circuits:** Determining the behavior of a sequential circuit by examining its flip-flop inputs and state transitions.
- **State reduction:** The process of reducing the number of states in a sequential circuit's state table while preserving input-output behavior.
- **State assignments:** Assigning binary codes to each state in a sequential circuit; affects the complexity of the resulting combinational logic.

---

## Chapter 5
## Registers and Counters

These are groups of flip-flops used for data storage and sequencing.

**Registers and Counters: Registers, shift registers, parallel loading of shift register, counters, synchronous and asynchronous counter, up and down counter, ripple counter, counters using SR and JK FF, design of sequential counter, application of counter: parallel to serial communication, other types of counters.**

### 5.1 Registers

- **Registers:** A group of storage elements read/written as a unit.
    - **Shift Register:** Capable of shifting binary information left or right. Modes include **Serial-In/Serial-Out (SISO)**, **Parallel-In/Serial-Out (PISO)**, etc.
- **Parallel loading of shift register:** The ability to load all bits of a shift register simultaneously (in parallel) rather than one bit at a time.

### 5.2 Counters

- **Counters:** Registers that go through a predetermined sequence of states.
    - **Asynchronous (Ripple) Counter:** Only the first flip-flop is clocked externally; others are clocked by the previous flip-flop's output. It is slower due to propagation delays.
    - **Synchronous Counter:** All flip-flops are clocked simultaneously, making it faster and more reliable.
    - **Up and Down Counter:** Counters that can increment (up) or decrement (down) based on a control input.
    - **Ripple Counter:** Another name for asynchronous counter; the clock "ripples" through the flip-flops.
    - **Counters using SR and JK FF:** Implementing counters using SR flip-flops or JK flip-flops as the storage elements.
    - **Design of sequential counter:** The systematic process of creating a counter with a specified sequence using state tables and excitation tables.

### 5.3 Special Counters and Applications

- **Special Counters:** **Ring Counters** (output of LSB connected to MSB input) and **Johnson Counters** (complement output of LSB connected to MSB).
- **Other types of counters:** Modulus counters (MOD-N), BCD counters, decade counters.
- **Application of counter: parallel to serial communication:** Using a counter to sequence the parallel loading and serial shifting of data in a shift register for converting parallel data to serial format.

---

## Chapter 6
## Memory and Programmable Logic

**Memory and Programmable Logic: Random access memory (RAM), memory addressing, Programmable Array Logic (PAL), Programmable Logic Array (PLA), Introduction to CPLDs, FPGAs.**

### 6.1 Memory

- **Random Access Memory (RAM):** A type of memory where data can be accessed in any order (random) and read or written; volatile memory (loses data when power is removed).
- **Memory addressing:** The method of selecting a specific memory location using an address bus; if there are $n$ address lines, $2^n$ memory locations can be addressed.

### 6.2 Programmable Logic Devices

- **Programmable Array Logic (PAL):** A programmable logic device with a programmable AND array and a fixed OR array; easier to program but less flexible than PLA.
- **Programmable Logic Array (PLA):** A programmable logic device where both the AND array and the OR array are programmable; more flexible than PAL but more complex.
- **Introduction to CPLDs (Complex Programmable Logic Devices):** A more complex programmable logic device containing multiple PAL-like blocks interconnected by a programmable switch matrix.
- **Introduction to FPGAs (Field-Programmable Gate Arrays):** A highly flexible programmable logic device containing an array of configurable logic blocks (CLBs) and programmable interconnects; can implement very large digital circuits.

---

## Chapter 7
## Hardware Description Language (Verilog HDL)

HDL is used for circuit verification, simulation, and logic synthesis.

**Introduction to hardware description language (HDL): Verilog HDL/VHDL, Syntax and program structure of HDL (Verilog HDL/VHDL). Application of HDL: Description and simulation of common combinational circuits using HDL: Adder, decoder, multiplexer etc. Description and simulation of sequential circuits, registers, counters.**

### 7.1 Design Flow and Abstraction Levels

- **Design Flow:** Includes design specification, behavioral description, RTL description, logic synthesis, and physical layout.
- **Levels of Abstraction:**
    1.  **Behavioral:** Describes the algorithm (highest level, similar to C).
    2.  **Dataflow:** Describes how data moves between registers.
    3.  **Gate Level:** Interconnects logic gates (AND, OR, NOT).
    4.  **Switch Level:** Interconnects transistors (lowest level).

### 7.2 Verilog Concepts

- **Verilog Concepts:**
    - **Module:** The basic building block representing a digital circuit.
    - **Ports:** Interface for modules (input, output, or inout).
    - **Data Types:** **Net types** (e.g., `wire`) represent physical connections, while **Register types** (e.g., `reg`) store values in procedures.

### 7.3 Syntax and Program Structure

- **Syntax and program structure of HDL (Verilog HDL/VHDL):**
    - Verilog modules begin with `module` and end with `endmodule`.
    - Ports are declared as `input`, `output`, or `inout`.
    - `assign` statements describe combinational logic (dataflow).
    - `always @(posedge clk)` blocks describe sequential logic.

### 7.4 Applications of HDL

- **Application of HDL: Description and simulation of common combinational circuits using HDL: Adder, decoder, multiplexer etc.**
- **Description and simulation of sequential circuits, registers, counters:** Using Verilog to model and test flip-flops, synchronous and asynchronous counters, shift registers (SISO, PISO), and state machines.
- **Stimulus Block (Test Bench):** A separate module used to apply inputs (stimuli) to a design block and check the results.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Binary Codes and Error Detection | BCD (8421), Excess-3, Gray Code, Even/Odd Parity, Hamming Code |
| 2 | Combinational Logic Circuits | Parallel Adder, Serial Adder, Carry-Look-Ahead Adder, BCD Adder, Magnitude Comparator |
| 3 | MSI Logic Circuits | MUX, DEMUX, Decoder (BCD-to-7-segment), Encoder, Priority Encoder, Parity Generator/Checker |
| 4 | Sequential Logic Circuits | Latch (level-sensitive), Flip-Flop (edge-triggered), SR, D, JK, T, Setup/Hold Time |
| 5 | Registers and Counters | Shift Register (SISO, PISO), Asynchronous (Ripple) Counter, Synchronous Counter, Ring/Johnson Counter |
| 6 | Memory and Programmable Logic | RAM, Memory Addressing, PAL, PLA, CPLD, FPGA |
| 7 | Hardware Description Language | Module, Ports (input/output/inout), wire, reg, Behavioral/Dataflow/Gate Level, Test Bench |

---
*CSE 2111 — Digital System Design | Dept. of CSE, University of Rajshahi*






