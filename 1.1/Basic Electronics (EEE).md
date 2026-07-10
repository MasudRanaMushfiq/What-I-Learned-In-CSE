

# Basic Electronics

### Course Information
**Course:** EEE 1131 (Basic Electronics) 
**Course Type:** Theory, 3 Credit 
**Prerequisite:** None
### Instructor
Dr. Bimal Kumar Pramanik, Professor, Dept. of CSE, University of Rajshahi 

---

### Course Motivation
> To develop basic knowledge on Electrical circuits and Electronics.


## Course Contents

|Area|Topics Covered|
|---|---|
|**Semiconductor Diodes**|Semiconductor, n- and p-type semiconductors, p-n junction diode and V-I characteristics, Zener diode, half- and full-wave rectifiers, voltage regulation using Zener diodes|
|**Transistor**|Transistor action, transistor biasing, DC characteristics of CE, CB and CC configurations, CE/CB/CC amplifiers, current/voltage/power gains, oscillators, astable and monostable multivibrators|
|**Field Effect Transistor**|FET, MOSFET, characteristics, biasing and applications|
|**Operational Amplifier**|Inverting and non-inverting amplifier, difference amplifier, comparator|
|**Optoelectronic Devices**|LED, LCD, photodiode, phototransistor, solar cell, tunnel diode|
|**Instrumentation**|Avometer (AVO meter/multimeter), oscilloscope (CRO)|

---

## Textbooks

**Primary Texts:**

1. S. G. Tarnekar, A. K. Teraja, B. L. Theraja — _Digital Systems: Principles and Applications_ (Part I and IV), S. Chand

---

## Table of Contents

1. [Chapter I – Semiconductor Physics and P-N Junctions](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#chapter-i)
2. [Chapter II – Semiconductor Diodes and Power Supplies](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#chapter-ii)
3. [Chapter III – Optoelectronic and Special Purpose Devices](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#chapter-iii)
4. [Chapter IV – Bipolar Junction Transistors (BJT)](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#chapter-iv)
5. [Chapter V – Transistor Amplifiers and Models](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#chapter-v)
6. [Chapter VI – Field Effect Transistors (FET)](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#chapter-vi)
7. [Chapter VII – Operational Amplifiers (Op-Amp)](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#chapter-vii)
8. [Chapter VIII – Oscillators and Multivibrators](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#chapter-viii)
9. [Chapter IX – Digital Electronics and Integrated Circuits](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#chapter-ix)
10. [Chapter X – Electronic Instrumentation and Laboratory Practice](https://claude.ai/chat/8630d0be-2b7d-497e-b5d1-aae2dcec83e8#chapter-x)

---

## Chapter I

## Semiconductor Physics and P-N Junctions

### 1.1 Atomic Structure and Energy Bands

Materials are classified based on their **energy band structure**:

|Material Type|Band Structure|Example|
|---|---|---|
|**Conductor**|Valence and conduction bands **overlap**|Copper, Aluminium|
|**Insulator**|**Large** energy gap between bands|Glass, Rubber|
|**Semiconductor**|**Small** gap (~2–3 eV); valence band full, no overlap|Silicon (Si), Germanium (Ge)|

> 💡 **Key Insight:** The small band gap in semiconductors makes them uniquely controllable — their conductivity can be tuned by doping, temperature, or light.

---

### 1.2 Doping

**Doping** is the deliberate introduction of impurity atoms into a pure semiconductor to alter its electrical conductivity.

- **n-type:** Impurity atoms donate **extra electrons** → majority carriers are electrons
- **p-type:** Impurity atoms create **holes** (absence of electrons) → majority carriers are holes

---

### 1.3 P-N Junction Formation

When p-type and n-type materials are joined:

1. **Diffusion** occurs — electrons from n-side cross to p-side; holes from p-side cross to n-side.
2. Carriers **recombine** near the junction.
3. A **depletion layer** (region depleted of free carriers) forms.
4. A **barrier voltage** (built-in potential) is established across the junction, opposing further diffusion.

---

### 1.4 Biasing the P-N Junction

|Bias Type|Connection|Effect|
|---|---|---|
|**Forward Bias**|p-type → (+), n-type → (−)|Narrows depletion layer; **current flows**|
|**Reverse Bias**|p-type → (−), n-type → (+)|Widens depletion layer; **current blocked** (until breakdown voltage)|

---

## Chapter II

## Semiconductor Diodes and Power Supplies

### 2.1 P-N Junction Diode

- A **two-terminal** device (Anode + Cathode).
- Acts as a **one-way valve** for electric current — conducts in forward bias, blocks in reverse bias.

---

### 2.2 Rectification (AC to DC Conversion)

Diodes are used to convert **Alternating Current (AC)** to **Direct Current (DC)**:

|Rectifier Type|Diodes Used|Output|
|---|---|---|
|**Half-Wave**|1 diode|Pulsating DC (only positive half-cycles)|
|**Full-Wave (Bridge)**|4 diodes|Continuous DC (both half-cycles used)|
|**Full-Wave (Center-Tapped)**|2 diodes + center-tapped transformer|Continuous DC|

---

### 2.3 Zener Diode

- Specifically engineered for **reverse breakdown** operation.
- In breakdown, voltage across it stays **nearly constant** regardless of current.
- **Primary Application:** Voltage regulation — maintains a stable output voltage despite variations in input or load.


---

## Chapter III

## Optoelectronic and Special Purpose Devices

### 3.1 Display Technologies

|Device|Full Name|Working Principle|Use|
|---|---|---|---|
|**LED**|Light Emitting Diode|Converts electrical energy → light (electroluminescence)|Indicators, status displays|
|**LCD**|Liquid Crystal Display|Liquid crystals modulated by electric fields to block/pass light|Screens, monitors|

---

### 3.2 Special-Purpose Diodes

|Device|Function|
|---|---|
|**Photodiode**|Detects light → converts to electrical current|
|**Phototransistor**|Like a photodiode but with amplification|
|**Tunnel Diode**|Exploits **quantum tunneling** for ultra-high-speed switching|
|**Solar Cell**|Converts **light energy directly into electrical energy** (photovoltaic effect)|

---

## Chapter IV

## Bipolar Junction Transistors (BJT)

### 4.1 Physical Architecture

A BJT consists of **three doped semiconductor regions**:

|Region|Doping Level|Physical Feature|
|---|---|---|
|**Emitter (E)**|Highest doping|Injects carriers|
|**Base (B)**|Thin, low doping|Controls carrier flow|
|**Collector (C)**|Medium doping, large area|Collects carriers|

**Types:**
- **NPN** — most commonly used in practice
- **PNP** — complementary type

---

### 4.2 Transistor Action

A BJT is a **current-controlled device**:

- A small **base current** controls a much larger **collector current**.
- **Two primary uses:**
    - **Amplification** — boosting weak signals
    - **Switching** — acting as an electronic ON/OFF switch

---

### 4.3 Transistor Configurations

|Configuration|Input/Output|Key Characteristics|
|---|---|---|
|**Common Base (CB)**|Input: E–B, Output: C–B|High voltage gain; **low input impedance**|
|**Common Emitter (CE)**|Input: B–E, Output: C–E|**Most widely used**; provides both voltage AND current gain|
|**Common Collector (CC)**|Input: B–C, Output: E–C|Also called **Emitter Follower**; used for impedance matching|


### 4.4 Biasing and the Q-Point

- **Biasing** establishes a stable DC operating point called the **Q-point** (Quiescent Point).
- The Q-point must be stable against variations in **temperature** and **β (current gain)**.
- **Voltage Divider Bias** — the most reliable biasing method; provides excellent Q-point stability.

---

## Chapter V

## Transistor Amplifiers and Models

### 5.1 Hybrid (h-parameter) Model

- A **small-signal mathematical model** treating the transistor as a "black-box."
- Defined by four parameters for the Common Emitter (CE) configuration:

|Parameter|Symbol|Description|
|---|---|---|
|Input impedance|$h_{ie}$|Input resistance with output short-circuited|
|Reverse voltage ratio|$h_{re}$|Feedback from output to input|
|Forward current gain|$h_{fe}$|Small-signal current gain (≈ β)|
|Output admittance|$h_{oe}$|Output conductance with input open|

> 💡 **CSE Relevance:** This "black-box" model is conceptually similar to treating components as abstract modules with defined input/output behaviour — a core principle in system design.

---

### 5.2 T-Model

- Uses **physical internal resistances** to model transistor behaviour:
    - $r_e$ — emitter resistance
    - $r_b$ — base resistance
    - $r_c$ — collector resistance

---

### 5.3 Performance Metrics

When analysing an amplifier circuit, calculate:

|Metric|Symbol|Meaning|
|---|---|---|
|**Input Impedance**|$Z_{in}$|Resistance seen by the source|
|**Output Impedance**|$Z_{out}$|Resistance seen by the load|
|**Voltage Gain**|$A_v$|Ratio of output voltage to input voltage|
|**Current Gain**|$A_i$|Ratio of output current to input current|

---

## Chapter VI

## Field Effect Transistors (FET)

### 6.1 Key Characteristics

> **Unlike BJTs (current-controlled), FETs are voltage-controlled devices.**

- Extremely **high input impedance** (gate draws virtually no current)
- Better **thermal stability** than BJTs
- Easier to integrate into **ICs** (Integrated Circuits)

---

### 6.2 Types of FET

#### JFET (Junction Field Effect Transistor)

- Uses a **reverse-biased p-n junction** as the gate.
- Controls channel width (and thus current) via gate voltage.

#### MOSFET (Metal-Oxide-Semiconductor FET)

- Gate is **insulated** by a thin layer of metal oxide (SiO₂).
- Two modes of operation:

|Mode|Operation|
|---|---|
|**Depletion Mode**|Conducts with zero gate voltage; gate voltage reduces current|
|**Enhancement Mode**|Does NOT conduct at zero gate voltage; gate voltage increases current|

---

## Chapter VII

## Operational Amplifiers (Op-Amp)

### 7.1 Definition and Terminals

An **Op-Amp** is an active circuit element designed to perform **mathematical operations** on signals.

**Terminals:**

- **Inverting Input (−)**
- **Non-inverting Input (+)**
- **Output**

---

### 7.2 Applications

|Application|Function|
|---|---|
|**Adder (Summing Amplifier)**|Sums multiple input voltages: $V_{out} = -(V_1 + V_2 + \ldots)$|
|**Subtractor (Difference Amplifier)**|Finds the difference between two input signals|
|**Comparator**|Compares two input levels; switches output HIGH or LOW accordingly|

> 💡 **Key Note:** Op-Amps are building blocks for **analog signal processing** — filters, integrators, differentiators, and waveform generators all use them.

---

## Chapter VIII

## Oscillators and Multivibrators

### 8.1 Sinusoidal Oscillators

These produce **continuous sine wave** outputs using **regenerative (positive) feedback**.

|Oscillator Type|Frequency-Determining Element|
|---|---|
|**Hartley Oscillator**|Tapped inductor + capacitor (LC tank)|
|**Colpitts Oscillator**|Two capacitors + inductor (LC tank)|
|**Phase Shift Oscillator**|RC network providing 180° phase shift|

---

### 8.2 Multivibrators (Non-Sinusoidal)

Multivibrators generate **square/rectangular waves** and switching signals.

|Type|Stable States|Behaviour|Application|
|---|---|---|---|
|**Astable**|0 (none)|Oscillates continuously between HIGH and LOW|Clock generators, timers|
|**Monostable**|1|Rests in stable state; moves temporarily to other state on trigger, then returns|Pulse generators, timers|
|**Bistable**|2|Stays in either state until triggered to switch|**Flip-flops** (memory storage)|

> 💡 **CSE Connection:** Bistable multivibrators are the foundation of **flip-flops**, which are the basic memory elements in digital circuits and registers.

---

## Chapter IX

## Digital Electronics and Integrated Circuits (IC)

### 9.1 Number Systems

|System|Base|Digits Used|CSE Use|
|---|---|---|---|
|**Binary**|2|0, 1|Machine-level data representation|
|**Decimal**|10|0–9|Human-readable numbers|
|**Hexadecimal**|16|0–9, A–F|Memory addresses, colour codes (e.g., `#FF5733`)|

> 💡 **CSE Example:** `0xFF` in hex = `255` in decimal = `11111111` in binary.

---

### 9.2 Logic Gates

Fundamental building blocks of all digital circuits:

|Gate|Symbol|Output Condition|
|---|---|---|
|**AND**|A · B|HIGH only if **all** inputs are HIGH|
|**OR**|A + B|HIGH if **any** input is HIGH|
|**NOT**|Ā|Inverts the input|
|**NAND**|¬(A · B)|LOW only if all inputs HIGH (universal gate)|
|**NOR**|¬(A + B)|HIGH only if all inputs LOW (universal gate)|
|**XOR**|A ⊕ B|HIGH if inputs are **different**|

---

### 9.3 Boolean Algebra and Simplification

- **Boolean Laws** — Commutative, Associative, Distributive, Identity, Complement
- **DeMorgan's Theorems:**
    - $\overline{A \cdot B} = \bar{A} + \bar{B}$
    - $\overline{A + B} = \bar{A} \cdot \bar{B}$
- **Karnaugh Maps (K-Maps)** — Visual tool to minimise Boolean expressions and reduce the number of logic gates required in a circuit.

---

### 9.4 IC Fabrication Process

All components (transistors, resistors, capacitors) are built on a **single Silicon wafer** through:

1. **Oxidation** — Grow SiO₂ layer on silicon wafer
2. **Photolithography** — Pattern the oxide layer using UV light and a mask
3. **Etching** — Remove unwanted oxide to expose silicon
4. **Diffusion** — Introduce dopant atoms into exposed silicon regions

---

## Chapter X

## Electronic Instrumentation and Laboratory Practice

### 10.1 Measurement Tools

|Instrument|Full Name|Measures / Used For|
|---|---|---|
|**AVO Meter (Multimeter)**|Ampere-Volt-Ohm Meter|Current (A), Voltage (V), Resistance (Ω)|
|**CRO**|Cathode-Ray Oscilloscope|Observing and measuring waveforms; frequency, amplitude, phase|

---

### 10.2 Standard Lab Report Structure

All laboratory experiments should be documented following this structure:

1. **Experiment Name** — Title of the experiment
2. **Objectives** — What is being investigated or demonstrated
3. **Circuit Diagram** — Properly drawn schematic with component labels
4. **Procedure** — Step-by-step method followed
5. **Results / Data Tables** — Measured values, observations
6. **Conclusions** — Analysis of results; do they match theory? Sources of error?

---

## Quick Reference Summary

|Chapter|Core Concept|Key Term|
|---|---|---|
|I|Semiconductors and junctions|Depletion Layer, Barrier Voltage|
|II|Diodes and power supplies|Rectification, Zener Regulation|
|III|Light and special diodes|LED, Photodiode, Solar Cell|
|IV|BJT transistor|Q-point, CE Configuration|
|V|Amplifier models|h-parameters, $A_v$, $Z_{in}$|
|VI|FET transistor|Voltage-controlled, MOSFET|
|VII|Op-Amp|Inverting/Non-inverting, Adder|
|VIII|Oscillators|Astable, Monostable, Bistable|
|IX|Digital logic|Logic Gates, K-Maps, IC Fabrication|
|X|Lab instruments|Multimeter, CRO|

---
*EEE 1131 — Basic Electronics | Dept. of CSE, University of Rajshahi*







