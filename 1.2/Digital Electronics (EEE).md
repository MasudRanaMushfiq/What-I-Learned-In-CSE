

# Introduction to Digital Electronics

### Course Information
**Course:** CSE 1211 (Introduction to Digital Electronics)
**Course Type:** Theory, 3 Credit
**Prerequisite:** EEE 1131: Basic Electronics
### Instructor
Dr. Md. Rokanujjaman, Professor, Dept. of CSE, University of Rajshahi

### Course Motivation
> To develop basics knowledge on Introduction to Digital Electronics.

---

## Course Contents

| Area | Topics Covered |
| ---- | -------------- |
| **Fundamentals of Digital Logic System** | Number Systems, weighted and non-weighted codes, error detection code, Binary addition and subtraction, 2's compliment methods |
| **Logic Gates and Boolean Algebra** | Logic Circuit Design, Adder, Substractor, Minimization Techniques: Algebraic Simplification, Karnaugh Map Method, Quine-McCluskey method, Consensus method, Hand |
| **Switching Devices and Integrated Circuit Logic Families** | switching characteristics of diodes, transistor and FETs. DTL & TTL logic family, standard TTL series characteristics, other TTL series, TTL loading rules, TTL open-collector outputs, tristate TTL. The ECL family. Digital MOSFET circuits, characteristics, CMOS circuits, CMOS tristate logic, TTL driving CMOS, CMOS driving TTL |
| **Flip-Flops (FF) and related devices** | Transistor Latch, NAND gate latch, NOR gate latch, D latch. Clock signals and Clocked FFs: Clocked SR, JK and D Flip-Flops, Master/Slave JK FF, timing diagram of different FFs, Edge-triggered and level-triggered timing diagrams |
| **555 Timer, A/D and D/A Converters** | Architecture of 555 Timer, different application of 555 timer, 555 as monostable, bistable and astable Multivibrators. Sample and hold circuit, weighted resistor and R-2R ladder D/A Converters, specifications for D/A converters. A/D converters: Quantization, parallel-comparator, successive approximation, counting type, dual-slope ADC, specifications of ADCs |


## Textbooks

**Primary Texts:**
1. Ronald J. Tocci — *Digital Systems: Principles and Applications*, Prentice Hall
2. V. K. Jain — *An Introduction to Switching Theory and Digital Electronics*, Khanna Publishers, New Delhi

---

## Table of Contents

1. [Module 1 – Introductory Concepts & Digital Systems](#module-1)
2. [Module 2 – Number Systems and Codes](#module-2)
3. [Module 3 – Describing Logic Circuits & Boolean Algebra](#module-3)
4. [Module 4 – Combinational Logic Minimization](#module-4)
5. [Module 5 – Digital Arithmetic Circuits](#module-5)
6. [Module 6 – MSI Logic Circuits](#module-6)
7. [Module 7 – Sequential Logic Circuits (Flip-Flops and Latches)](#module-7)
8. [Module 8 – Counters and Registers](#module-8)
9. [Module 9 – Integrated-Circuit Logic Families and Switching Devices](#module-9)
10. [Module 10 – Interfacing with the Analog World (555 Timer, ADC, DAC)](#module-10)
11. [Module 11 – Memory and Programmable Logic](#module-11)

---

## Module 1
## Introductory Concepts & Digital Systems

### 1.1 Digital vs. Analog

- **Digital vs. Analog**: **Analog** quantities vary over a continuous range of values (e.g., temperature 27.6°C), whereas **Digital** quantities take on discrete values, typically represented by two states (1 or 0).

### 1.2 Advantages of Digital

- **Advantages of Digital**: Digital systems are easier to design, provide high-accuracy information storage, are less affected by noise, and can be fabricated on integrated circuit chips.

### 1.3 Basic Block Diagram of a Computer

- **Basic Block Diagram of a Computer**: Consists of an **Input Unit**, **Memory Unit**, **Control Unit**, **Arithmetic/Logic Unit (ALU)**, and **Output Unit**. The combination of the ALU and Control Unit is known as the **Central Processing Unit (CPU)**.

---

## Module 2
## Number Systems and Codes

### 2.1 Base Conversions

- **Base Conversions**:
    - **Decimal to Binary**: Uses repeated division-by-2 for whole numbers and repeated multiplication-by-2 for fractions.
    - **Hexadecimal**: Base-16 system using digits 0-9 and letters A-F. Each hex digit represents a 4-bit binary group (nibble).

### 2.2 Digital Codes

- **Codes**:
    - **BCD (Binary Coded Decimal)**: Represents each decimal digit (0-9) as a 4-bit binary code (e.g., $17_{10} = 0001\ 0111_{BCD}$).
    - **Gray Code**: A non-weighted code where only one bit changes between successive values, useful for error prevention in mechanical encoders.
    - **Excess-3 Code**: A BCD-type code where each decimal digit is represented by its binary value plus 3.

### 2.3 Error Detection

- **Error Detection**: **Parity** bits are added to data strings to detect single-bit errors. **CRC (Cyclic Redundancy Check)** is a more advanced technique used in communication.

---

## Module 3
## Describing Logic Circuits & Boolean Algebra

### 3.1 Logic Gates

- **Logic Gates**:
    - **AND**: Output is HIGH only if all inputs are HIGH ($C = A \cdot B$).
    - **OR**: Output is HIGH if any input is HIGH ($C = A + B$).
    - **NOT (Inverter)**: Reverses the logic state ($B = \bar{A}$).

### 3.2 Boolean Laws and Theorems

- **Boolean Laws**:
    - **DeMorgan's Theorems**: $\overline{A+B} = \bar{A}\bar{B}$ and $\overline{A \cdot B} = \bar{A} + \bar{B}$.
    - **Consensus Theorem**: $AB + \bar{A}C + BC = AB + \bar{A}C$. The term $BC$ is redundant.

### 3.3 Universality of NAND and NOR

- **Universality**: **NAND** and **NOR** gates are universal because any logic function can be implemented using only one of these types.

---

## Module 4
## Combinational Logic Minimization

### 4.1 Karnaugh Map (K-map)

- **Karnaugh Map (K-map)**: A graphical tool to simplify logic expressions. Groups of 1s (pairs, quads, octets) are circled to eliminate variables that change within the group.

### 4.2 Quine-McCluskey Method

- **Quine-McCluskey Method**: A systematic tabular procedure for functional minimization, preferred over K-maps for functions with more than five or six variables because it can be easily programmed.

---

## Module 5
## Digital Arithmetic Circuits

### 5.1 Representing Signed Numbers

- **Representing Signed Numbers**:
    - **2's Complement**: The most common system. To find the 2's complement, invert all bits of the magnitude (1's complement) and add 1.

### 5.2 Adder Circuits

- **Adder Circuits**:
    - **Half-Adder**: Adds two bits; produce a SUM and a CARRY.
    - **Full-Adder**: Adds three bits (including an input carry); necessary for multi-bit addition.
    - **CSE Example**: A 3-bit adder/subtractor circuit uses three full adders and XOR gates to selectively invert the subtrahend for subtraction using 2's complement addition.

---

## Module 6
## MSI Logic Circuits

### 6.1 Decoders

- **Decoders**: Detect a specific binary input and activate a unique output. A **BCD-to-7-segment decoder** translates BCD into the signals needed to display numbers on an LED or LCD.

### 6.2 Multiplexers and Demultiplexers

- **Multiplexers (MUX)**: Also called **Data Selectors**; they select one of many inputs to be passed to a single output based on select lines.
- **Demultiplexers (DEMUX)**: The reverse of a MUX; they take one input and route it to one of many outputs.

---

## Module 7
## Sequential Logic Circuits (Flip-Flops and Latches)

### 7.1 Latch vs. Flip-Flop

- **Latch vs. Flip-Flop**: A **latch** is level-triggered (responds to input levels), while a **flip-flop** is edge-triggered (responds to transitions of a clock signal).

### 7.2 Types of Flip-Flops

- **Types**:
    - **JK Flip-Flop**: Universal flip-flop; can SET, CLEAR, or TOGGLE (change to opposite state) when $J=K=1$.
    - **D Flip-Flop**: "Data" flip-flop; the output Q follows input D at the triggering clock edge.

### 7.3 Timing Parameters

- **Timing**: **Setup time ($t_S$)** is the minimum time data must be stable *before* the clock edge; **Hold time ($t_H$)** is the time it must remain stable *after* the edge.

---

## Module 8
## Counters and Registers

### 8.1 Counters

- **Counters**:
    - **Asynchronous (Ripple)**: Each flip-flop is clocked by the previous one, leading to propagation delays (glitches).
    - **Synchronous (Parallel)**: All flip-flops are clocked simultaneously, allowing higher operating speeds.

### 8.2 Registers

- **Registers**: Groups of flip-flops used for data storage. **Shift registers** move data one bit position per clock pulse (e.g., Serial-In/Parallel-Out or SIPO).

---

## Module 9
## Integrated-Circuit Logic Families and Switching Devices

### 9.1 Key Parameters

- **Key Parameters**: **Fan-out** is the maximum number of inputs a gate can drive. **Noise Margin** is a measure of the circuit's ability to tolerate electrical noise.

### 9.2 TTL (Transistor-Transistor Logic)

- **TTL (Transistor-Transistor Logic)**: Uses bipolar transistors; characterized by fast switching and 5V power requirements.

### 9.3 CMOS (Complementary Metal-Oxide-Semiconductor)

- **CMOS (Complementary Metal-Oxide-Semiconductor)**: Uses MOSFETs; has very low power consumption and high noise immunity, making it the dominant technology today.

### 9.4 Switching Characteristics of Diodes, Transistors and FETs

- **Switching Characteristics of Diodes, Transistors and FETs:** Diodes, transistors, and FETs each have unique switching characteristics that determine their suitability for digital logic circuits.

### 9.5 DTL & TTL Logic Family

- **DTL & TTL Logic Family:** Diode-Transistor Logic (DTL) and Transistor-Transistor Logic (TTL) are bipolar logic families.

### 9.6 Standard TTL Series Characteristics

- **Standard TTL Series Characteristics:** Standard TTL series have specific propagation delays, power dissipation, and fan-out capabilities.

### 9.7 Other TTL Series

- **Other TTL Series:** Other TTL series include Low-power TTL, Schottky TTL, and Low-power Schottky TTL, each optimized for different trade-offs between speed and power.

### 9.8 TTL Loading Rules

- **TTL Loading Rules:** TTL loading rules define how many gate inputs (fan-out) a TTL output can drive without exceeding its current specifications.

### 9.9 TTL Open-Collector Outputs

- **TTL Open-Collector Outputs:** TTL open-collector outputs allow wired-AND connections and are used for driving loads like relays or LEDs.

### 9.10 Tristate TTL

- **Tristate TTL:** Tristate TTL adds a high-impedance (disabled) state to the normal HIGH and LOW outputs, enabling bus-oriented systems.

### 9.11 The ECL Family

- **The ECL Family:** Emitter-Coupled Logic (ECL) is a high-speed bipolar logic family where transistors are operated in the active region to avoid saturation, preventing charge storage and allowing very fast switching.

### 9.12 Digital MOSFET Circuits

- **Digital MOSFET Circuits:** MOSFETs (Metal-Oxide-Semiconductor Field-Effect Transistors) are the basis for CMOS logic, offering low power consumption and high packing density.

### 9.13 Characteristics

- **Characteristics:** Key characteristics of MOSFET circuits include high input impedance, low static power dissipation, and scaling capability.

### 9.14 CMOS Circuits

- **CMOS Circuits:** CMOS circuits use complementary pairs of p-channel and n-channel MOSFETs to implement logic functions with negligible static power consumption.

### 9.15 CMOS Tristate Logic

- **CMOS Tristate Logic:** CMOS tristate logic adds a high-impedance output state, allowing multiple outputs to share a common bus line.

### 9.16 TTL Driving CMOS

- **TTL Driving CMOS:** When TTL drives CMOS, a pull-up resistor may be required because the TTL HIGH output voltage (typically 2.4V) may be below the CMOS input HIGH threshold (typically 3.5V for standard CMOS).

### 9.17 CMOS Driving TTL

- **CMOS Driving TTL:** CMOS driving TTL is generally easier because CMOS outputs can typically sink/source enough current to satisfy TTL input requirements, though high-speed CMOS may still need buffering.

---

## Module 10
## Interfacing with the Analog World (555 Timer, ADC, DAC)

### 10.1 DAC (Digital-to-Analog)

- **DAC (Digital-to-Analog)**: Converts binary numbers to proportional voltages. The **R/2R ladder** is common as it requires only two resistor values.

### 10.2 ADC (Analog-to-Digital)

- **ADC (Analog-to-Digital)**:
    - **Successive Approximation**: Uses a trial-and-error approach with a DAC and comparator; has a constant, fast conversion time.
    - **Flash ADC**: The fastest type; uses multiple comparators to convert simultaneously.

### 10.3 Architecture of 555 Timer

- **Architecture of 555 Timer:** The 555 timer contains two comparators, a resistive voltage divider (three 5kΩ resistors setting reference voltages at 1/3 Vcc and 2/3 Vcc), an RS flip-flop, a discharge transistor, and an output buffer.

### 10.4 Different Applications of 555 Timer

- **Different Applications of 555 Timer:** The 555 timer can be used as a monostable multivibrator (one-shot pulse generator), an astable multivibrator (oscillator/free-running square wave generator), and a bistable multivibrator (flip-flop), as well as for pulse-width modulation, missing pulse detection, and voltage-controlled oscillators.

### 10.5 555 as Monostable, Bistable and Astable Multivibrators

- **555 as Monostable, Bistable and Astable Multivibrators:**
    - **Monostable:** Trigger input momentarily pulls the trigger pin below 1/3 Vcc, output goes HIGH for time $T = 1.1 R_A C$, then returns LOW.
    - **Astable:** Trigger and threshold pins connected to capacitor, output oscillates continuously. HIGH time $t_H = 0.693 (R_A + R_B) C$, LOW time $t_L = 0.693 R_B C$.
    - **Bistable:** Uses the reset and trigger pins to set and reset the output, acting as a memory element.

### 10.6 Sample and Hold Circuit

- **Sample and Hold Circuit:** A sample and hold circuit captures an analog voltage at a specific instant and holds it stable for the duration of an ADC conversion, preventing errors due to signal changes during conversion.

### 10.7 Weighted Resistor and R-2R Ladder D/A Converters

- **Weighted Resistor and R-2R Ladder D/A Converters:**
    - **Weighted Resistor:** Uses binary-weighted resistors (R, 2R, 4R, ..., $2^{n-1}R$) with a summing amplifier. Suffers from wide resistor value ranges for high resolution.
    - **R-2R Ladder:** Uses only two resistor values (R and 2R), making it easier to fabricate on ICs and providing better accuracy.

### 10.8 Specifications for D/A Converters

- **Specifications for D/A Converters:** Key specifications include resolution (number of input bits), accuracy (maximum deviation from ideal output), settling time (time to final output value within specified error), and linearity (maximum deviation from a straight line).

### 10.9 A/D Converters: Quantization

- **A/D Converters: Quantization:** Quantization is the process of converting a continuous analog input range into a finite number of discrete digital output codes. The quantization error is ±1/2 LSB (least significant bit).

### 10.10 Parallel-Comparator (Flash) ADC

- **Parallel-Comparator (Flash) ADC:** A flash ADC uses $2^n - 1$ comparators to simultaneously compare the input voltage against all reference levels, producing the digital output in one clock cycle at the cost of high circuit complexity ($2^n - 1$ comparators).

### 10.11 Successive Approximation ADC

- **Successive Approximation ADC:** A successive approximation ADC uses a binary search algorithm: a SAR (Successive Approximation Register) tries one bit at a time, comparing the DAC output to the input using a comparator, converging to the final digital value in $n$ steps.

### 10.12 Counting Type (Digital Ramp) ADC

- **Counting Type (Digital Ramp) ADC:** A counting type ADC resets a binary counter to zero, then counts upward while comparing the DAC output to the input voltage. When the DAC output equals or exceeds the input, the counter stops, and the count is the digital output. Conversion time is variable and depends on the input amplitude.

### 10.13 Dual-Slope ADC

- **Dual-Slope ADC:** A dual-slope ADC integrates the input voltage for a fixed time, then integrates a reference voltage of opposite polarity back to zero. The time required for the second integration is proportional to the input voltage, providing high accuracy and excellent noise rejection.

### 10.14 Specifications of ADCs

- **Specifications of ADCs:** Key ADC specifications include resolution (number of output bits), conversion time/speed (time to complete one conversion), accuracy (maximum deviation from ideal transfer function), and missing codes (output codes that never appear due to non-linearity).

---

## Module 11
## Memory and Programmable Logic

### 11.1 Memory

- **Memory**:
    - **Volatile (RAM)**: Data is lost when power is removed. **SRAM** uses latches; **DRAM** stores charge on capacitors and requires "refreshing".
    - **Non-Volatile (ROM)**: Data is retained without power (e.g., Flash memory, EEPROM).

### 11.2 PLDs

- **PLDs**: Devices like **FPGAs (Field Programmable Gate Arrays)** contain thousands of logic gates that can be reconfigured by the user to implement complex digital designs.

---

## Quick Reference Summary

| Module | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Introductory Concepts | Analog, Digital, CPU, ALU, Input, Output, Memory, Control Unit |
| 2 | Number Systems and Codes | Binary, Octal, Hexadecimal, BCD, Gray Code, Excess-3, Parity, CRC |
| 3 | Logic Circuits & Boolean Algebra | AND, OR, NOT, NAND, NOR, XOR, XNOR, DeMorgan's Theorem, Consensus Theorem |
| 4 | Combinational Minimization | SOP, POS, K-map, Quine-McCluskey, Don't-Care Conditions |
| 5 | Arithmetic Circuits | Half-Adder, Full-Adder, Half-Subtractor, Full-Subtractor, 2's Complement |
| 6 | MSI Logic Circuits | Decoder, Encoder, MUX, DEMUX, Magnitude Comparator, BCD-to-7-Segment |
| 7 | Sequential Logic (Flip-Flops) | Latch, Flip-Flop, SR, JK, D, T, Edge-triggered, Level-triggered, Setup Time, Hold Time |
| 8 | Counters and Registers | Asynchronous Counter, Synchronous Counter, Shift Register, SISO, SIPO, PISO, PIPO |
| 9 | Logic Families and Switching Devices | TTL, CMOS, ECL, Fan-out, Noise Margin, Open-Collector, Tristate, MOSFET |
| 10 | ADC, DAC, and 555 Timer | DAC (R/2R, Weighted Resistor), ADC (Flash, Successive Approximation, Dual-Slope), 555 Timer (Astable, Monostable, Bistable), Sample and Hold, Quantization |
| 11 | Memory and Programmable Logic | RAM (SRAM, DRAM), ROM (PROM, EPROM, Flash), PLD, CPLD, FPGA |

---
*CSE 1211 — Introduction to Digital Electronics | Dept. of CSE, University of Rajshahi*





