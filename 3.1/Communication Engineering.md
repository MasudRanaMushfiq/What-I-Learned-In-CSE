

# Communication Engineering

### Course Information
**Course:** ICE 3161 (Communication Engineering)
**Course Type:** Theory, 2 Credit
**Prerequisite:** None
### Instructor
Dr. Asif Zaman, Peofessor, Dept. of CSE, University of Rajshahi

### Course Motivation
> To develop fundamental concepts on Communication system.

---

## Course Contents

| Area                       | Topics Covered                                                                                                                                                                                                                                                                                                        |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Fundamentals**           | Communication Engineering Fundamentals, Waveforms Spectra, Periodic waveforms and its properties, Fourier series, Noise and its different types                                                                                                                                                                       |
| **Amplitude Modulation**   | Amplitude modulation, Amplitude modulation index, Frequency spectrum for sinusoidal AM                                                                                                                                                                                                                                |
| **Frequency Modulation**   | Frequency Modulation, Sinusoidal FM, Frequency spectrum for Sinusoidal FM, FM transmitter. Phase Modulation                                                                                                                                                                                                           |
| **Pulse Modulation**       | Pulse Codes Modulation (PCM), Quantization, Compression, PCM Receiver, Differential PCM, Delta Modulation, Pulse Frequency Modulation (PFM), Pulse Time Modulation (PTM), Pulse Position Modulation (PPM)                                                                                                             |
| **Digital Communication**  | Digital Communication, Basic Digital Communication System, Synchronization, Asynchronous Transmission, Probability of Bit Error in Base band Transmission, Matched Filter, Eye Diagrams, Digital Carrier Systems, Amplitude Shift keying, Frequency Shift Keying, Phase Shift Keying, Differential Phase Shift Keying |
| **Radio Wave Propagation** | Mode of Propagation, Satellite Communication, Fiber Optic Communication: Fiber Optic Communication, Propagation within a Fiber, Modes of Propagation, Losses in Fibers, Light sources for Fiber optics, Photo detectors                                                                                               |

---

## Textbooks

**Primary Texts:**
1. Behrouz A. Forouzan — *Data Communications and Networking*, Tata McGraw-Hill Edition

---

## Table of Contents

1. [Chapter 1 – Foundations of Data Communication](#chapter-1)
2. [Chapter 2 – Physical Layer: Signals and Analysis](#chapter-2)
3. [Chapter 3 – Transmission Impairments and Channel Capacity](#chapter-3)
4. [Chapter 4 – Digital Transmission (Line Coding, Block Coding and Conversion)](#chapter-4)
5. [Chapter 5 – Bandwidth Utilization (Multiplexing and Spread Spectrum)](#chapter-5)
6. [Chapter 6 – Transmission Media and Satellite Networks](#chapter-6)
7. [Chapter 7 – Error Detection and Correction](#chapter-7)
8. [Chapter 8 – Modulation Techniques](#chapter-8)
9. [Chapter 9 – Pulse Modulation](#chapter-9)
10. [Chapter 10 – Digital Communication Systems](#chapter-10)
11. [Chapter 11 – Radio Wave Propagation and Fiber Optics](#chapter-11)

---

## Chapter 1
## Foundations of Data Communication

### 1.1 Fundamentals

**Communication Engineering Fundamentals:** This course provides a comprehensive foundation in the principles of data communication and network engineering. It covers how data is transformed into electromagnetic signals for transmission across various media. Key areas of study include signal analysis in time and frequency domains, transmission impairments, encoding techniques (digital-to-digital, analog-to-digital, and vice versa), bandwidth utilization through multiplexing and spread spectrum, physical transmission media, satellite networks, and error detection/correction mechanisms.

**Data and Communication:** Data is a collection of discrete or continuous values conveying information. Data communication is the exchange of data between two devices via a transmission medium.

**Fundamental Characteristics:**
1.  **Delivery:** Data must reach the correct destination only.
2.  **Accuracy:** Data must remain unaltered during transmission.
3.  **Timeliness:** Delivery must be in a timely manner (real-time for audio/video).
4.  **Jitter:** Refers to variation in packet arrival times, leading to uneven quality.

**Components of a System:** Message, Sender, Receiver, Transmission Medium, and Protocol (the set of rules governing communication).

**Protocol:** Rules governing data exchange (Syntax, Semantics, Timing).

---

### 1.2 Network Criteria and Structures

**Network Criteria:**
- **Performance:** Measured by transit time and response time; evaluated via throughput and delay.
- **Reliability:** Measured by frequency of failure and recovery time.
- **Security:** Protecting data from unauthorized access or damage.

**Throughput:** Rate of successfully transmitted data.

**Physical Structures:**
- **Connection Types:** Point-to-point (dedicated link) and multipoint (shared link).
- **Topologies:** Mesh (fully connected, secure), Star (robust, central hub), Bus (easy installation, shared backbone), and Ring (easy fault isolation).

**Waveforms Spectra:** Waveforms represent the shape of a signal over time; the spectrum is the distribution of the signal's energy across different frequencies.

**Periodic waveforms and its properties:** A periodic waveform completes a pattern within a timeframe (period) and repeats it. Properties include period (time per cycle), frequency (cycles per second), amplitude (strength), and phase.

**Fourier series:** According to Fourier analysis, any composite signal is a combination of simple sine waves with different frequencies. The Fourier series decomposes a periodic function into a sum of sines and cosines.

**Noise and its different types:** Noise is any unwanted signal added during transmission.
- **Thermal noise** (due to random electron motion)
- **Induced noise** (from external sources like motors)
- **Crosstalk** (signal from one line leaking into another)
- **Impulse noise** (sudden spikes, e.g., from lightning)

---

## Chapter 2
## Physical Layer: Signals and Analysis

### 2.1 Analog vs. Digital Signals

**Analog vs. Digital:** Analog signals have infinitely many levels of intensity; digital signals have a limited set of defined values.

**Periodic Signals:** Complete a pattern within a timeframe (period) and repeat it.
- **Sine Wave:** A basic periodic analog signal defined by **Peak Amplitude** (highest intensity), **Frequency** (periods per second), and **Phase** (position relative to time zero).

---

### 2.2 Domains and Composite Signals

**Domains:**
- **Time Domain:** Shows amplitude vs. time.
- **Frequency Domain:** Shows amplitude vs. frequency. It is essential for dealing with composite signals.

**Composite Signals:** According to Fourier analysis, any composite signal is a combination of simple sine waves with different frequencies.
- If periodic, the frequency domain shows discrete spikes.
- If non-periodic, the frequency domain is a continuous curve.

**Bandwidth:** The range of frequencies contained in a composite signal ($B = f_{high} - f_{low}$).

**Baseband vs. Broadband:** Baseband sends signals without modulation over a low-pass channel; broadband uses modulation over a band-pass channel.

**Self-synchronization:** Digital signals containing timing info in transitions, allowing the receiver's clock to align.

---

## Chapter 3
## Transmission Impairments and Channel Capacity

### 3.1 Impairments

**Impairments:**
1.  **Attenuation:** Loss of energy as a signal travels. Measured in decibels (dB).
2.  **Distortion:** Change in the signal's form or shape.
3.  **Noise:** Extra signals added during transmission (Thermal, Induced, Crosstalk, Impulse).

**Signal-to-Noise Ratio (SNR):** The ratio of average signal power to average noise power. High SNR is better for transmission.

> 📌 **Example (Attenuation Calculation):** If a signal's power is reduced to one-half, the loss in dB is $10 \log_{10}(0.5) \approx -3$ dB.

---

### 3.2 Data Rate Limits

**Data Rate Limits:**
- **Nyquist Bit Rate (Noiseless Channel):** $BitRate = 2 \times \text{bandwidth} \times \log_2 L$ (where $L$ is signal levels).
- **Shannon Capacity (Noisy Channel):** $Capacity = \text{bandwidth} \times \log_2 (1 + SNR)$.
- **Usage:** Shannon gives the theoretical upper limit; Nyquist determines the required signal levels to reach that limit.

> 💡 **Example (Data Rate):** For a noiseless channel with 3000 Hz bandwidth and two signal levels: $BitRate = 2 \times 3000 \times \log_2(2) = 6000$ bps.

> 💡 **Example (Nyquist vs Shannon):** If a channel has 1 MHz bandwidth and SNR = 63, the Shannon Capacity is $10^6 \times \log_2(1+63) = 6$ Mbps. To achieve 4 Mbps, signal levels required: $4 \times 10^6 = 2 \times 10^6 \times \log_2(L) \rightarrow L = 4$.

---

## Chapter 4
## Digital Transmission (Line Coding, Block Coding and Conversion)

### 4.1 Line Coding

**Line Coding:** Converting bit sequences to digital signals.
1. **Unipolar (e.g., NRZ):** All signal levels are on one side of the time axis (either positive or zero). It is rarely used today due to high power consumption.
2. **Polar:** Voltages are on both sides of the axis (positive and negative).
    - **NRZ-L (Level):** The voltage level determines the bit value.
    - **NRZ-I (Invert):** An inversion (change) in voltage represents bit 1; no change represents bit 0.
    - **RZ (Return-to-Zero):** The signal returns to zero in the middle of each bit interval, requiring three voltage levels but helping with synchronization.
    - **Biphase (Manchester and Differential Manchester):** Combined ideas of RZ and NRZ. Manchester uses a transition at the middle of each bit for both synchronization and bit representation.
3. **Bipolar (e.g., AMI and Pseudoternary):** Uses three levels (positive, negative, zero). In **AMI**, 0 is zero voltage, and 1s alternate between positive and negative.
4. **Multilevel (mBnL):** Encodes patterns of m bits into patterns of n signal elements using L levels to increase data rates (e.g., **2B1Q**, **8B6T**).
5. **Multitransition (MLT-3):** Uses three levels and specific transition rules (no transition for 0, transitions for 1) to reduce required bandwidth.

**Scrambling:** Technique to replace long strings of 0s without increasing bit count to maintain synchronization.

### 2. Block Coding

**Block coding** provides redundancy to ensure synchronization and inherent error detection capabilities. It transforms a block of m bits (a **dataword**) into a larger block of n bits (a **codeword**).

**The Three-Step Process**
1. **Division:** The bit stream is divided into groups of m bits.
2. **Substitution:** Each m-bit group is replaced with an n-bit codeword.
3. **Combination:** The codewords are combined into a final stream.

**Common Schemes**
- **4B/5B:** Replaces 4-bit datawords with 5-bit codewords. It is designed so that a codeword never has more than one leading zero or two trailing zeros, ensuring no more than three consecutive 0s appear in the stream when combined with **NRZ-I**.
- **8B/10B:** Replaces 8 bits with 10 bits. It offers superior error detection and synchronization compared to 4B/5B.

**Error Detection and Hamming Distance**
- **Invalid Codewords:** Since n>k, there are 2n−2k bit combinations that are "illegal." If the receiver receives an invalid codeword, it knows an error occurred.
- **Hamming Distance:** This is the number of differences between corresponding bits of two words. The **Minimum Hamming Distance (**dmin​**)** determines how many errors a code can detect or correct. To detect up to s errors, dmin​ must be at least s+1.
- **Linear Block Codes:** A common subset where the XOR (modulo-2 addition) of any two valid codewords results in another valid codeword. Examples include **Parity-check** and **CRC (Cyclic Redundancy Check)**.


---

### 4.2 Conversion Methods

**Conversion Methods:**
- **Analog-to-Digital:** Uses **Pulse Code Modulation (PCM)** involving sampling, quantizing, and encoding.
- **Digital-to-Analog:** Modulates a carrier signal using **ASK** (Amplitude), **FSK** (Frequency), **PSK** (Phase), or **QAM** (combined Amplitude/Phase).

**Sampling Rate ($f_s$):** Must be at least twice the highest frequency of the analog signal (Nyquist Theorem).

**Transmission Modes:**
- **Parallel:** Multiple bits sent simultaneously using multiple wires.
- **Serial:** Bits sent one after another. Includes **Asynchronous** (start/stop bits), **Synchronous** (timed frames), and **Isochronous** (guaranteed fixed rate).

---

## Chapter 5
## Bandwidth Utilization (Multiplexing and Spread Spectrum)

### 5.1 Multiplexing

**Multiplexing:** simultaneous transmission of multiple signals across one link.
- **FDM (Frequency):** Analog technique; signals are modulated onto different carrier frequencies.
- **WDM (Wavelength):** Used for fiber optics; combines different wavelengths of light.
- **TDM (Time):** Digital technique; users share time slots. **Statistical TDM** only assigns slots to active lines to improve efficiency.

---

### 5.2 Spread Spectrum

**Spread Spectrum:** Spreading the signal bandwidth over a wider range to prevent interference/eavesdropping.
- **FHSS (Frequency Hopping):** Signal jumps rapidly between frequencies.
- **DSSS (Direct Sequence):** Each data bit is multiplied by a high-speed "chipping code".

---

## Chapter 6
## Transmission Media and Satellite Networks

### 6.1 Guided Media

**Guided Media:**
- **Twisted-Pair:** Used for telephony/LANs; twisting reduces noise.
- **Coaxial Cable:** Higher frequency range than twisted-pair.
- **Fiber Optic:** Uses light pulses; higher bandwidth, less attenuation, and immune to EMI. Propagation modes include **Multimode** (Step-index or Graded-index) and **Single-mode**.

---

### 6.2 Unguided Media and Satellite Networks

**Unguided (Wireless) Media:** Radio waves (omnidirectional), Microwaves (line-of-sight), and Infrared (short-range).

**Satellite Networks:** Combination of nodes (satellites and Earth stations).
- **Orbits:** **GEO** (Geostationary, equatorial, fixed position), **MEO** (Medium Earth Orbit, e.g., GPS), and **LEO** (Low Earth Orbit).

**Footprint:** The area on Earth where a satellite's signal can be received.

---

## Chapter 7
## Error Detection and Correction

### 7.1 Error Types and Hamming Distance

**Error Types:** **Single-bit** (one bit altered) and **Burst** (multiple bits altered).

**Redundancy:** Adding extra bits to data to detect errors.

**Hamming Distance:** Number of bit differences between two words. The **Minimum Hamming Distance** ($d_{min}$) determines detection/correction capability ($d_{min} = s + 1$ to detect $s$ errors).

---

### 7.2 Detection Schemes

**Detection Schemes:**
- **Parity Check:** Simple bit added to make the total number of 1s even or odd.
- **Cyclic Redundancy Check (CRC):** Based on binary division. Dataword is augmented with 0s and divided by a predefined divisor; the remainder is the CRC appended to the codeword.
- **Checksum:** Used in the network/transport layers; data is divided into segments and summed using one's complement.

> 💡 **Example (CRC Generation):** To encode dataword `1001` with divisor `1011`:
> 1.  Augment `1001` with three 0s → `1001000`.
> 2.  Perform modulo-2 division by `1011`.
> 3.  Remainder is `110`.
> 4.  Codeword sent → `1001110`.

---

## Chapter 8
## Modulation Techniques

### 8.1 Amplitude Modulation

**Amplitude modulation (AM):** A technique where the amplitude of a high-frequency carrier signal is varied in proportion to the instantaneous amplitude of the modulating (information) signal.

**Amplitude modulation index:** The modulation index ($m$) in AM is the ratio of the amplitude of the modulating signal to the amplitude of the carrier signal. It determines the depth of modulation.

**Frequency spectrum for sinusoidal AM:** For a sinusoidal modulating signal, the AM spectrum consists of the carrier frequency ($f_c$) and two sidebands: upper sideband ($f_c + f_m$) and lower sideband ($f_c - f_m$).

---

### 8.2 Frequency and Phase Modulation

**Frequency Modulation (FM):** A technique where the instantaneous frequency of the carrier signal is varied in proportion to the amplitude of the modulating signal.

**Sinusoidal FM:** Frequency modulation where the modulating signal is a single sine wave.

**Frequency spectrum for Sinusoidal FM:** The FM spectrum consists of the carrier frequency plus an infinite number of sidebands spaced at multiples of the modulating frequency, with amplitudes determined by Bessel functions.

**FM transmitter:** A device that generates an FM signal, typically consisting of an oscillator, modulator, and power amplifier.

**Phase Modulation (PM):** A technique where the instantaneous phase of the carrier signal is varied in proportion to the amplitude of the modulating signal. PM is closely related to FM.

---

### 8.3 Digital Modulation

**Amplitude Shift Keying (ASK):** Digital modulation where the amplitude of the carrier is switched between two levels (typically on/off) to represent binary 1 and 0.

**Frequency Shift Keying (FSK):** Digital modulation where the frequency of the carrier is switched between two distinct frequencies to represent binary 1 and 0.

**Phase Shift Keying (PSK):** Digital modulation where the phase of the carrier is shifted (e.g., 0° for binary 0, 180° for binary 1) to represent data.

**Differential Phase Shift Keying (DPSK):** A form of PSK where the data is encoded as the phase difference between successive transmitted symbols, rather than absolute phase, making it easier to decode.

---

## Chapter 9
## Pulse Modulation

### 9.1 Pulse Code Modulation (PCM)

**Pulse Codes Modulation (PCM):** A method of converting an analog signal into a digital bit stream by sampling, quantizing, and encoding.

**Quantization:** The process of mapping a continuous range of sampled amplitudes into a finite set of discrete levels. Quantization introduces quantization error (noise).

**Compression:** In PCM, compression (such as µ-law or A-law) is used to reduce the number of bits needed for encoding by applying non-linear quantization that gives more levels to low-amplitude signals and fewer to high-amplitude signals.

**PCM Receiver:** A device that receives a PCM bit stream and reconstructs the original analog signal through decoding, de-quantization, and low-pass filtering.

---

### 9.2 Differential PCM and Delta Modulation

**Differential PCM (DPCM):** A variation of PCM where the difference between consecutive samples is encoded instead of the absolute sample value, reducing the number of bits required.

**Delta Modulation (DM):** A simple form of DPCM where only one bit per sample is transmitted, indicating whether the signal has increased or decreased relative to the previous sample.

---

### 9.3 Other Pulse Modulation Techniques

**Pulse Frequency Modulation (PFM):** A modulation technique where the frequency of a pulse train is varied in proportion to the amplitude of the modulating signal.

**Pulse Time Modulation (PTM):** A class of modulation where the timing characteristics (width or position) of pulses are varied.

**Pulse Position Modulation (PPM):** A PTM technique where the position of each pulse (relative to a reference time) is varied according to the modulating signal amplitude.

---

## Chapter 10
## Digital Communication Systems

### 10.1 Digital Communication Fundamentals

**Digital Communication:** The transmission of discrete (digital) messages using a communication system.

**Basic Digital Communication System:** A system consisting of: a source, source encoder, channel encoder, modulator, transmission medium, demodulator, channel decoder, source decoder, and destination.

**Synchronization:** The process of aligning the receiver's clock with the transmitter's clock to correctly interpret the incoming bit stream.

**Asynchronous Transmission:** A serial transmission method where each character is framed with start and stop bits, allowing the receiver to synchronize at the beginning of each character.

---

### 10.2 Performance Metrics

**Probability of Bit Error in Base band Transmission ($P_b$ or $P_e$):** The likelihood that a transmitted bit is incorrectly received due to noise and other impairments. For a given modulation and SNR, $P_b$ can be calculated using error function (erfc) relationships.

**Matched Filter:** A filter designed to maximize the signal-to-noise ratio (SNR) at its output for a known transmitted symbol shape; it is optimal for detecting a known signal in additive white Gaussian noise (AWGN).

**Eye Diagrams:** An oscilloscope display that shows multiple overlapped symbol intervals, used to evaluate the quality of a digital transmission. Parameters measured include eye opening, jitter, rise/fall times, and noise margin.

---

### 10.3 Digital Carrier Systems

**Digital Carrier Systems:** Systems that use a sinusoidal carrier to transmit digital data, employing modulation techniques such as ASK, FSK, PSK, and QAM.

**Synchronization in digital carrier systems:** Includes carrier synchronization (phase-locked loops for demodulation) and symbol timing synchronization (recovering the symbol clock).

---

## Chapter 11
## Radio Wave Propagation and Fiber Optics

### 11.1 Radio Wave Propagation

**Mode of Propagation:** The path that radio waves take from the transmitter to the receiver. The three primary modes are:
- **Ground wave (surface wave):** Follows the Earth's curvature; used for low-frequency bands (AM broadcasting).
- **Sky wave (ionospheric wave):** Reflected by the ionosphere back to Earth; enables long-distance communication (shortwave radio).
- **Line-of-sight (space wave):** Travels directly from transmitter to receiver with no reflection; used for VHF, UHF, and microwaves (TV, FM, cellular).

**Satellite Communication:** Communication that uses orbiting satellites as relay stations to receive and retransmit signals between Earth stations. Satellite communication provides global coverage and broadcast capability.

---

### 11.2 Fiber Optic Communication

**Fiber Optic Communication:** A communication method that uses light pulses traveling through optical fibers to transmit data. It offers extremely high bandwidth, low attenuation, and immunity to electromagnetic interference.

**Propagation within a Fiber:** Light propagates through an optical fiber by total internal reflection. Light entering the fiber at an angle less than the acceptance angle will be guided along the core.

**Modes of Propagation:** The distinct patterns (electromagnetic field distributions) in which light propagates through a fiber.
- **Multimode fiber:** Supports multiple propagation modes; larger core diameter; used for short distances.
  - **Step-index multimode:** Refractive index changes abruptly at core-cladding boundary.
  - **Graded-index multimode:** Refractive index decreases gradually from center of core outward, reducing modal dispersion.
- **Single-mode fiber:** Supports only one propagation mode (the fundamental mode); very small core diameter; used for long distances and high bandwidth.

**Losses in Fibers:** Attenuation mechanisms in optical fibers include:
- **Absorption:** Light energy converted to heat by impurities (e.g., water (OH⁻) ions).
- **Scattering:** Rayleigh scattering due to microscopic variations in density; intrinsic loss that increases with higher frequency.
- **Bending losses:** Macrobending (large radius bends) and microbending (small-scale irregularities) cause light to escape from the core.

**Light sources for Fiber optics:** Devices that convert electrical signals into optical signals for transmission through fiber.
- **LED (Light Emitting Diode):** Lower cost, longer lifetime, but less power and wider spectral width; used for multimode, short-distance links.
- **Laser Diode (LD):** Higher power, narrower spectral width, faster switching; used for single-mode, long-distance, high-bandwidth links.

**Photo detectors:** Devices that convert received optical signals back into electrical signals. Common types include:
- **PIN photodiode:** Simple, low-cost, good sensitivity.
- **Avalanche Photodiode (APD):** Provides internal gain (avalanche multiplication) for higher sensitivity, but requires higher bias voltage.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Foundations | Protocol, Delivery/Accuracy/Timeliness/Jitter, Topologies (Mesh, Star, Bus, Ring), Throughput |
| 2 | Signals | Analog/Digital, Sine wave (Amplitude, Frequency, Phase), Time/Frequency domains, Bandwidth |
| 3 | Impairments | Attenuation (dB), Distortion, Noise types (Thermal, Induced, Crosstalk, Impulse), SNR, Nyquist, Shannon |
| 4 | Digital Transmission | Line coding (Unipolar NRZ, Polar NRZ, Manchester), PCM, ASK/FSK/PSK/QAM, Serial/Parallel modes |
| 5 | Bandwidth Utilization | FDM, WDM, TDM (Statistical TDM), Spread Spectrum (FHSS, DSSS) |
| 6 | Transmission Media | Twisted-pair, Coaxial, Fiber optic (Multimode/Single-mode), Wireless (Radio, Microwave, Infrared), Satellite (GEO, MEO, LEO) |
| 7 | Error Detection | Hamming distance, Parity, CRC (binary division), Checksum |
| 8 | Modulation | AM (index, spectrum), FM (Bessel sidebands, transmitter), PM, ASK, FSK, PSK, DPSK |
| 9 | Pulse Modulation | PCM (sampling, quantization, compression), DPCM, Delta Modulation, PFM, PTM, PPM |
| 10 | Digital Communication | Matched filter, Eye diagram, Probability of bit error, Asynchronous transmission |
| 11 | Propagation & Fiber Optics | Ground/Sky/Line-of-sight waves, Satellite, Fiber losses (absorption, scattering, bending), LED/Laser, PIN/APD |

---
*ICE 3161 — Communication Engineering | Dept. of ICE, University of Rajshahi*





