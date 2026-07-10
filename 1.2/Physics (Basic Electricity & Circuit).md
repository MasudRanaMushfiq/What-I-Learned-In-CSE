

# Basic Electricity and Electrical Circuits

### Course Information
**Course:** PHY 1211 (Basic Electricity and Electrical Circuits)
**Course Type:** Theory, 3 Credit
**Prerequisite:** None
### Instructor
Dr. Bimal Kumar Pramanik, Professor, Dept. of CSE, University of Rajshahi

### Course Motivation
> To know basic Electrical and Magnetic laws required to understand computer hardware.

---

## Course Contents

| Area | Topics Covered |
| ---- | -------------- |
| **Electrostatics** | Electric dipole; electric field due to a dipole; dipole on external electric field; Gauss's Law and its applications |
| **Capacitors** | Parallel plate capacitors with dielectric; dielectrics and Gauss's Law; susceptibility, permeability, and dielectric constant; energy stored in an electric field |
| **Electric Current** | Electron theory of conductivity; conductor, semiconductors and insulators; superconductors, current and current density, Kirchhoffs Law and its applications |
| **Electromagnetic Induction** | Faraday's experiment; Faraday's law; Ampere's law, motional e.m.f.; self and mutual inductance galvanometers-moving coil, ballistic and deadbeat types |
| **Networks Analysis** | Kirchhoff's laws; Superposition theorem; Millman's theorem; Reciprocity theorem, Thevenin's theorem, Norton's theorem, Maximum power transfer theorem, Mesh and Node circuit analysis, Reduction of complicated networks, T and p-section network |
| **DC and AC Circuits** | D.C. circuits with LR, RC, and LCR in series; A.C. circuits with LR, RC, LC, and LCR in series |

---

## Textbooks

**Primary Texts:**
1. J David Halliday, Robert Resnick and Kenneth S. Krane — *Physics (Part-I & II)*, Wiley

---

## Table of Contents

1. [Module 1 – Electrostatics and Gauss's Law](#module-1)
2. [Module 2 – Capacitance, Dielectrics, and Conduction](#module-2)
3. [Module 3 – Electromagnetism and Induction](#module-3)
4. [Module 4 – DC Network Analysis and Theorems](#module-4)
5. [Module 5 – Transient Response and AC Circuits](#module-5)

---

## Module 1
## Electrostatics and Gauss's Law

### 1.1 Electric Field and Point Charges

- **Definition:** An **electric field** is the environment created by an electric charge in the surrounding space; if another charge enters this space, it experiences a force.
- **Field Intensity ($E$):** Defined as the force exerted on a unit positive test charge ($q_0$) placed at a point: $\vec{E} = \vec{F}/q_0$.
- **Field of a Point Charge:** The magnitude of the field at a distance $r$ from a charge $q$ is $E = \frac{1}{4\pi\epsilon_0} \cdot \frac{q}{r^2}$.

### 1.2 Electric Dipoles

- **Definition:** An **electric dipole** consists of two equal and opposite charges ($q$ and $-q$) separated by a small distance $d$.
- **Dipole Moment ($\vec{p}$):** A vector with magnitude $p = qd$, pointing from the negative to the positive charge.
- **Electric field due to a dipole:** At distant axial points, the field magnitude is $E = \frac{1}{2\pi\epsilon_0} \cdot \frac{p}{z^3}$. It decreases more rapidly ($1/r^3$) than the field of a single point charge ($1/r^2$) because the opposite charges nearly cancel each other out.
- **Dipole on external electric field:** In a uniform external field $\vec{E}$, a dipole experiences a **torque** $\vec{\tau} = \vec{p} \times \vec{E}$ and possesses **potential energy** $U = -\vec{p} \cdot \vec{E}$.
- **CSE Example: Microwave Cooking.** Water molecules are electric dipoles. An oscillating electric field in the oven exerts torques on them, causing them to "flip-flop" and transfer energy to food as heat.

### 1.3 Gauss's Law and Its Applications

- **Definition:** The **electric flux** ($\Phi$) measures the flow of the electric field through an area. **Gauss's Law** states that the net flux through any closed surface is proportional to the net enclosed charge ($q_{enc}$): $\epsilon_0 \Phi = \epsilon_0 \oint \vec{E} \cdot d\vec{A} = q_{enc}$.
- **Applications:**
    - **Infinite Line of Charge:** $E = \frac{\lambda}{2\pi\epsilon_0 r}$.
    - **Nonconducting Sheet:** $E = \frac{\sigma}{2\epsilon_0}$.
    - **Spherical Shell:** The field outside ($r > R$) is $E = \frac{1}{4\pi\epsilon_0} \cdot \frac{q}{r^2}$; the field inside ($r < R$) is zero.

---

## Module 2
## Capacitance, Dielectrics, and Conduction

### 2.1 Capacitance and Energy Storage

- **Capacitance ($C$):** A measure of a device's ability to store charge; it is the ratio of charge $q$ to potential difference $V$ ($C = q/V$). The SI unit is the **Farad (F)**.
- **Parallel-Plate Capacitor with Dielectric:** For two plates of area $A$ separated by distance $d$, $C = \frac{\epsilon_0 A}{d}$. When a dielectric is inserted, the capacitance becomes $C = \frac{k\epsilon_0 A}{d}$, where $k$ is the dielectric constant.
- **Energy Stored in an Electric Field:** Energy is stored in the electric field between the plates: $U = \frac{1}{2}CV^2$. **Energy density** (energy per unit volume) is $u = \frac{1}{2}\epsilon_0 E^2$.
- **CSE Example: RAM.** A storage capacitor on a Random Access Memory chip stores bits of data as electrical charge.

### 2.2 Dielectrics

- **Definition:** Insulating materials (e.g., mica, porcelain) that increase capacitance by a factor $k$, the **dielectric constant**.
- **Atomic View:** Dielectrics contain molecules that are either **polar** (permanent dipole moments) or **nonpolar** (induced dipoles in an external field). These dipoles align to create an internal field that opposes and weakens the external field.
- **Susceptibility, Permeability, and Dielectric Constant:** The **dielectric constant** $k$ (also called relative permittivity $\epsilon_r$) is related to the electric susceptibility $\chi_e$ by $k = 1 + \chi_e$. **Permeability** ($\mu$) is a measure of a material's ability to support the formation of a magnetic field, while **permittivity** ($\epsilon$) measures the ability to support an electric field.
- **Dielectrics and Gauss's Law:** $\oint k\vec{E} \cdot d\vec{A} = \frac{q_{free}}{\epsilon_0}$.

### 2.3 Conduction and Resistivity

- **Electric Current:** The rate of flow of charge: $i = dq/dt$. Unit: **Ampere (A)**.
- **Current Density ($J$):** Current per unit area ($J = i/A$).
- **Electron Theory of Conductivity:** According to the **electron theory of conductivity**, $\rho = \frac{m}{ne^2\tau}$, where $\tau$ is the mean free time between electron collisions.
- **Drift Speed ($v_d$):** The average speed of charge carriers moving due to an electric field. It is related to current density by $J = (ne)v_d$.
- **Conductor, Semiconductors and Insulators, Superconductors:**
    - **Conductors:** Materials with low resistivity (e.g., copper, silver) where electrons are free to move.
    - **Semiconductors:** Materials with intermediate resistivity (e.g., silicon, germanium) whose conductivity can be controlled by doping.
    - **Insulators:** Materials with very high resistivity (e.g., rubber, glass) where electrons are tightly bound.
    - **Superconductors:** Materials that exhibit zero electrical resistance below a critical temperature.
- **Resistivity ($\rho$):** A material property that opposes current.

---

## Module 3
## Electromagnetism and Induction

### 3.1 Faraday's Experiment and Faraday's Law

- **Magnetic Flux ($\Phi_B$):** Measure of magnetic field passing through an area: $\Phi_B = \int \vec{B} \cdot d\vec{A}$. Unit: **Weber (Wb)**.
- **Faraday's Experiment:** Faraday discovered that a changing magnetic field induces an electromotive force (emf) in a circuit.
- **Faraday's Law:** The magnitude of the emf ($\epsilon$) induced in a conducting loop equals the rate of change of magnetic flux: $\epsilon = -N \frac{d\Phi_B}{dt}$.
- **Motional e.m.f.:** The emf induced when a conductor moves through a magnetic field. For a conductor of length $L$ moving with velocity $v$ perpendicular to a uniform field $B$, the motional emf is $\epsilon = BLv$.

### 3.2 Lenz's Law

- **Lenz's Law:** An induced current flows in a direction such that its magnetic field opposes the flux change that produced it.

### 3.3 Ampere's Law

- **Definition:** The line integral of the magnetic field $\vec{B}$ around a closed Amperian loop is proportional to the net current enclosed: $\oint \vec{B} \cdot d\vec{s} = \mu_0 i_{enc}$.
- **Applications:** Used to find the magnetic field inside straight wires, solenoids, and toroids.

### 3.4 Inductance (Self and Mutual)

- **Inductance ($L$):** The ability of a coil to oppose changes in current and store energy in a magnetic field. Unit: **Henry (H)**.
- **Self-Inductance:** A changing current in a coil induces an emf in the same coil: $\epsilon_L = -L \frac{di}{dt}$.
- **Mutual Inductance:** A changing current in one coil induces an emf in a nearby second coil: $\epsilon_2 = -M \frac{di_1}{dt}$.
- **CSE Example: MRI.** Magnetic resonance imaging uses induction and magnetic fields for medical diagnostics.

### 3.5 Galvanometers (Moving Coil, Ballistic and Deadbeat Types)

- **Moving Coil Galvanometer:** A device that detects and measures small electric currents by the torque produced when a current-carrying coil rotates in a magnetic field.
- **Ballistic Galvanometer:** A type of galvanometer designed to measure the total charge passed through it, rather than steady current. It has a long period of oscillation.
- **Deadbeat Galvanometer:** A galvanometer that comes to rest quickly without oscillation, achieved through electromagnetic damping.

---

## Module 4
## DC Network Analysis and Theorems

### 4.1 Kirchhoff's Laws and Their Applications

- **Kirchhoff's Current Law (KCL):** The algebraic sum of currents at a junction is zero ($\Sigma I = 0$).
- **Kirchhoff's Voltage Law (KVL):** The algebraic sum of potential rises and drops around a closed loop is zero ($\Sigma V = 0$).
- **Mesh and Node Circuit Analysis:**
    - **Mesh Analysis:** A method that applies KVL to independent loops (meshes) in a circuit to solve for unknown currents.
    - **Node Analysis:** A method that applies KCL to independent nodes in a circuit to solve for unknown voltages.

### 4.2 Key Network Theorems

- **Superposition Theorem:** In a linear network with multiple sources, the total current/voltage across an element is the sum of the effects of each source acting alone.
- **Thevenin's Theorem:** Any two-terminal linear DC network can be replaced by an equivalent circuit with a single voltage source ($V_{Th}$) in series with a resistor ($R_{Th}$).
- **Norton's Theorem:** Replaces a network with a current source ($I_N$) in parallel with a resistor ($R_N$, where $R_N = R_{Th}$).
- **Maximum Power Transfer Theorem:** A load receives maximum power when its resistance ($R_L$) equals the network's Thevenin resistance ($R_{Th}$).
- **Millman's Theorem:** A method to simplify a circuit with multiple parallel voltage sources into a single equivalent voltage source and series resistance.
- **Reciprocity Theorem:** In a linear bilateral network, the ratio of a voltage source in one branch to the current response in another branch is the same if the source and response locations are interchanged.

### 4.3 Network Reduction Techniques

- **Reduction of Complicated Networks:** Combining series and parallel resistors, star-delta transformations, and applying network theorems to simplify complex circuits.
- **T and π-Section Network:** T-networks (three resistors arranged like the letter T) and π-networks (three resistors arranged like the Greek letter π) are equivalent and can be transformed into each other using star-delta (Y-Δ) transformation formulas.

---

## Module 5
## Transient Response and AC Circuits

### 5.1 DC Circuits with LR, RC, and LCR in Series (Transient Response)

- **RC Circuits (DC):** When charging, current decays while charge $q$ rises. The **time constant** ($\tau = RC$) is the time to reach ~63.2% of full charge.
- **RL Circuits (DC):** Current rises toward a steady value $\epsilon/R$. The time constant is $\tau = L/R$.
- **LCR Circuits (DC):** When a DC source is applied to a series LCR circuit, the response may be overdamped, underdamped (oscillatory), or critically damped depending on the relative values of $R$, $L$, and $C$.

### 5.2 AC Fundamentals

- **Alternating Current (AC):** Current that periodically reverses direction; $v(t) = V_m \sin(\omega t)$.
- **RMS Values:** Effective values used for power calculations; $V_{rms} = V_m / \sqrt{2}$.

### 5.3 AC Circuits with LR, RC, LC, and LCR in Series

- **Series RL Circuit (AC):** Current lags voltage by a phase angle $\phi = \tan^{-1}(X_L/R)$.
- **Series RC Circuit (AC):** Current leads voltage by a phase angle $\phi = \tan^{-1}(-X_C/R)$.
- **Series LC Circuit (AC):** At resonance ($X_L = X_C$), impedance is zero (ideal case) or minimum, and current is maximum.
- **Series RLC Circuits (AC):**
    - **Impedance ($Z$):** Total opposition to current; $Z = \sqrt{R^2 + (X_L - X_C)^2}$.
    - **Resonance:** Occurs when inductive reactance equals capacitive reactance ($X_L = X_C$), minimizing impedance and maximizing current. Resonant frequency $\omega_0 = 1/\sqrt{LC}$.
- **Phase Relations:** In a capacitor, current **leads** voltage by 90°. In an inductor, current **lags** voltage by 90°.

---

## Quick Reference Summary

| Module | Core Topic | Key Terms / Formulas |
|---|---|---|
| 1 | Electrostatics and Gauss's Law | Electric dipole, $\vec{p} = qd$, Torque $\vec{\tau} = \vec{p} \times \vec{E}$, Energy $U = -\vec{p} \cdot \vec{E}$, Gauss's Law $\epsilon_0 \oint \vec{E} \cdot d\vec{A} = q_{enc}$, Infinite line $E = \lambda/(2\pi\epsilon_0 r)$, Spherical shell $E = q/(4\pi\epsilon_0 r^2)$ |
| 2 | Capacitance, Dielectrics, and Conduction | Capacitance $C = q/V$, $C = \epsilon_0 A/d$, Dielectric constant $k$, Energy $U = \frac{1}{2}CV^2$, Current $i = dq/dt$, Current density $J = i/A$, Drift speed $J = nev_d$, Resistivity $\rho = m/(ne^2\tau)$ |
| 3 | Electromagnetism and Induction | Magnetic flux $\Phi_B = \int \vec{B} \cdot d\vec{A}$, Faraday's Law $\epsilon = -N d\Phi_B/dt$, Lenz's Law, Ampere's Law $\oint \vec{B} \cdot d\vec{s} = \mu_0 i_{enc}$, Self-inductance $\epsilon_L = -L di/dt$, Mutual inductance $\epsilon_2 = -M di_1/dt$, Moving coil galvanometer |
| 4 | DC Network Analysis and Theorems | KCL ($\Sigma I = 0$), KVL ($\Sigma V = 0$), Superposition, Thevenin ($V_{Th}, R_{Th}$), Norton ($I_N, R_N$), Maximum Power Transfer ($R_L = R_{Th}$), Millman's Theorem, Reciprocity Theorem, Mesh Analysis, Node Analysis, T and π networks |
| 5 | Transient Response and AC Circuits | RC time constant $\tau = RC$, RL time constant $\tau = L/R$, AC $v(t) = V_m \sin(\omega t)$, $V_{rms} = V_m/\sqrt{2}$, Impedance $Z = \sqrt{R^2 + (X_L - X_C)^2}$, Resonance $\omega_0 = 1/\sqrt{LC}$, Phase: current leads voltage in C, lags in L |

---
*PHY 1211 — Basic Electricity and Electrical Circuits | Dept. of CSE, University of Rajshahi*





