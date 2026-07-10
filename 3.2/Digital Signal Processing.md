

# Digital Signal Processing

### Course Information
**Course:** CSE 3221 (Digital Signal Processing)
**Course Type:** Theory, 3 Credit
**Prerequisite:** MATH 2241: Linear Algebra
### Instructor
Dr. Md. Ekramul Hamid, Professor, Dept. of CSE, University of Rajshahi 

### Course Motivation
> To know basic of the digital signal processing concepts and its analysis.

---

## Course Contents

| Area | Topics Covered |
| --- | --- |
| **Introduction** | Signals, systems and signal processing, classification of signals, frequency concept, analog to digital and digital to analog conversion, sampling and quantization |
| **Discrete time signals and systems** | Analysis of discrete time linear time invariant systems, difference equations, implementation, correlation and convolution |
| **The z-transform** | Definition, ROC of infinite duration sequence, properties, inversion, and the one-sided z-transform |
| **Frequency analysis of signals and systems** | Frequency analysis of continuous and discrete time signals, properties of Fourier transform, domain characteristics of linear time invariant systems as frequency selective filters, and inverse systems |
| **The Discrete Fourier Transform** | DFT, properties, filtering method, and frequency analysis. Fast Fourier Transform Algorithms and digital filter design (FIR and IIR) |
| **Wavelet and multiresolution processing** | Wavelet and multiresolution processing |
| **Adaptive filters** | Adaptive system, kalman filters, RLS adaptive filters, steepest-descent method, and LMS filters |
| **Application of DSP** | Speech processing, analysis and coding, and Matlab application |

---

## Textbooks

**Primary Texts:**
1. J. G. Prokis — *Digital Signal Processing*, Prentice-hall Of India
2. R. G. Lyon — *Understanding Digital Signal Processing*, Orling Kindersley India

---

## Table of Contents

1. [Chapter 1 – Introduction to Signals and Systems](#chapter-1)
2. [Chapter 2 – Sampling and Reconstruction](#chapter-2)
3. [Chapter 3 – Discrete-Time Signals and LTI Systems](#chapter-3)
4. [Chapter 4 – Correlation and Convolution](#chapter-4)
5. [Chapter 5 – The Z-Transform](#chapter-5)
6. [Chapter 6 – Frequency Domain Analysis](#chapter-6)
7. [Chapter 7 – The Discrete Fourier Transform (DFT) and FFT](#chapter-7)
8. [Chapter 8 – Digital Filter Design (FIR and IIR)](#chapter-8)
9. [Chapter 9 – Adaptive Filters](#chapter-10)
10. [Chapter 10 – Applications of DSP](#chapter-11)

---

## Chapter 1
## Introduction to Signals and Systems

### 1.1 Signal Definition and Classification

**Digital Signal Processing (DSP):** Digital Signal Processing (DSP) is the area of science and engineering that deals with the enhancement, extraction, and representation of information for the purposes of communication and analysis. It involves the mathematical manipulation of information signals to modify or improve them, representing continuous real-world signals as discrete sequences of numbers and using digital processors to perform algorithmic operations such as filtering, compression, and spectral analysis.

**Signal:** A physical quantity that varies with time, space, or other independent variables.

**Signals, systems and signal processing:** DSP involves understanding signals (the information carriers), systems (the processors that operate on signals), and signal processing (the algorithms and techniques used to extract, enhance, or transform information).

**Classification of signals:**

**Classification by Domain:**
- **Continuous-Time (Analog):** Defined for every value of time $t$.
- **Discrete-Time:** Represented as a sequence at discrete intervals $n$.

**Classification by Prediction:**
- **Deterministic:** Can be predicted exactly by a mathematical formula.
- **Random:** Cannot be predicted exactly; analyzed using probability.

**Classification by Channel/Dimension:**
- **Single Channel vs. Multichannel:** One vs. multiple sensors (e.g., ECG is multichannel).
- **1-D vs. M-D:** Number of independent variables (e.g., images are 2-D).

**Frequency concept:** Frequency is the number of cycles per unit time, measured in Hertz (Hz). It describes how often a periodic signal repeats. The frequency concept is fundamental to understanding how signals are represented, filtered, and transformed in the frequency domain.

---

### 1.2 System Classification

**System:** A physical device or algorithm that performs operations on a signal.

**Static vs. Dynamic:** A static system is memoryless (depends only on present input); a dynamic system has memory (depends on past/future inputs).

**Linear vs. Nonlinear:** A linear system satisfies the superposition principle.

**Causal vs. Non-causal:** A causal system depends only on present and past inputs.

**Time-Invariant vs. Time-Variant:** A system is time-invariant if its input-output characteristics do not change over time.

**LTI System:** A system that is both Linear and Time-Invariant.

---

### 1.3 Key Advantages of DSP over Analog Signal Processing

**Key Advantages of DSP over Analog Signal Processing:**
- **Flexibility:** Operations can be changed simply by updating software.
- **Precision:** Achieves higher accuracy through word length and numerical methods.
- **Storage:** Digital signals can be stored on magnetic media without loss of fidelity.
- **Cost:** Often cheaper due to the use of VLSI and integrated circuits.
- **Complexity:** Can implement advanced algorithms (like FFT or adaptive filtering) difficult or impossible in analog.

> 📌 **LTI System Check Example:** A system $y(n) = x^2(n)$ is dynamic and nonlinear, while $y(n) = x(n) + x(n-1)$ is dynamic, linear, and causal.

---

## Chapter 2
## Sampling and Reconstruction

### 2.1 Periodic Sampling and Conversion

**Analog to digital and digital to analog conversion:** The process of converting a continuous-time analog signal to a discrete-time digital signal (ADC) and then back to analog form (DAC) is fundamental to DSP.

**Periodic Sampling:** Converting a continuous-time signal $x_a(t)$ to discrete-time $x(n)$ by taking snapshots at intervals $T$.

**Sampling Theorem (Nyquist):** To avoid aliasing, the sampling frequency $F_s$ must be at least twice the highest frequency component $f_{max}$ in the signal ($F_s \geq 2f_{max}$).

**Aliasing:** Signal ambiguity where a high-frequency component takes the "alias" of a lower frequency due to under-sampling.

**Aliasing:** The overlap of frequency spectra that occurs when a signal is sampled below the Nyquist rate.

> 💡 **Aliasing Calculation Example:** If $f_o = 10 \text{ Hz}$ and $F_s = 40 \text{ Hz}$, its aliases are $10 + k(40)$, giving $50, 90, 130, \dots \text{ Hz}$.

**Sampling and quantization:** Sampling is the process of converting a continuous-time signal into discrete-time samples. Quantization is the process of mapping the continuous amplitude values of sampled signals into a finite set of discrete levels, introducing quantization error (noise).

**Quantization Noise:** Error introduced by representing continuous values with a finite number of bits.

---

### 2.2 Conversion Steps

**Conversion Steps:**
1.  **Input Lowpass Filter:** Removes unwanted high-frequency components to avoid aliasing (Antialiasing filter).
2.  **Analog-to-Digital Converter (ADC):** Performs sampling, quantization, and coding.
3.  **DSP Processor:** Performs the mathematical operations.
4.  **Digital-to-Analog Converter (DAC):** Converts processed data back to analog form.

**DSP Stages:** Antialiasing filter → ADC → DSP → DAC → Reconstruction filter.

---

## Chapter 3
## Discrete-Time Signals and LTI Systems

### 3.1 Discrete-Time LTI Analysis

**Discrete time signals and systems:** Analysis of discrete time linear time invariant systems involves understanding how signals are processed by systems that are both linear (satisfy superposition) and time-invariant (behavior does not change over time).

**Analysis of discrete time linear time invariant systems:** LTI systems are completely characterized by their impulse response $h(n)$. The output $y(n)$ for any input $x(n)$ is given by the convolution sum.

**Difference equations:** Difference equations are mathematical relationships that describe how the current output of a discrete-time system depends on past outputs, current and past inputs. The general form is:
$$y(n) = \sum_{k=0}^{N} b_k x(n-k) - \sum_{k=1}^{M} a_k y(n-k)$$

**Implementation:** LTI systems can be implemented in direct form (I and II), cascade form, parallel form, or lattice structures, each offering trade-offs in computational complexity, coefficient sensitivity, and stability.

**Impulse Response $h(n)$:** The output of a system when the input is a unit impulse $\delta(n)$.

**Group Delay:** A measure of the time delay of the amplitude envelope of the various sinusoidal components.

---

## Chapter 4
## Correlation and Convolution

### 4.1 Convolution

**Convolution:** A mathematical operation that expresses the relationship between input, impulse response, and output of an LTI system.

**Formula:** $y(n) = x(n) * h(n) = \sum_{k=-\infty}^{\infty} x(k)h(n-k)$.

**Circular Convolution:** Convolution used for periodic sequences or calculated via DFT.

---

### 4.2 Correlation

**Correlation:** Measures the similarity between two signal sequences.

**Types:**
- **Cross-correlation:** Between two different signals $x(n)$ and $y(n)$.
- **Autocorrelation:** Between a signal and a version of itself.

**Application:** Used in radar and sonar to determine time delay $D$ and distance to a target.

---

## Chapter 5
## The Z-Transform

### 5.1 Definition and ROC

**Definition:** Transforms a time-domain signal $x(n)$ into a complex-plane representation $X(z) = \sum_{n=-\infty}^{\infty} x(n)z^{-n}$.

**Region of Convergence (ROC):** The set of values of $z$ for which the infinite series converges.
- **Causal system:** ROC is $|z| > r$ (outside a circle).
- **Stable system:** ROC must include the unit circle ($|z| = 1$).

**ROC of infinite duration sequence:** For an infinite duration sequence (either right-sided, left-sided, or two-sided), the ROC is determined by the poles of $X(z)$. A right-sided sequence has ROC outside the outermost pole; a left-sided sequence has ROC inside the innermost pole; a two-sided sequence has ROC in an annulus between poles.

**Properties of the z-transform:** Key properties include: linearity, time shifting, scaling in the z-domain, differentiation, convolution (multiplication in z-domain), initial value theorem, and final value theorem.

**Inversion of the z-transform:** Methods to find $x(n)$ from $X(z)$ include: partial fraction expansion (for rational functions), power series expansion (long division), contour integration (inverse formula), and using tables of z-transform pairs.

**The one-sided z-transform:** The one-sided z-transform is defined as $X(z) = \sum_{n=0}^{\infty} x(n)z^{-n}$, assuming $x(n)=0$ for $n<0$. It is particularly useful for solving difference equations with initial conditions.

---

## Chapter 6
## Frequency Domain Analysis

### 6.1 Frequency Analysis of Signals and Systems

**Frequency analysis of continuous and discrete time signals:** Frequency analysis decomposes signals into their sinusoidal or complex exponential components, revealing the amplitude and phase at each frequency. For continuous-time signals, this is the Fourier transform; for discrete-time signals, it is the discrete-time Fourier transform (DTFT).

**Properties of Fourier transform:** Key properties include: linearity, time shifting, frequency shifting (modulation), scaling, convolution (multiplication in frequency domain), Parseval's theorem (energy conservation), differentiation in time, and symmetry/conjugate symmetry.

**Domain characteristics of linear time invariant systems as frequency selective filters:** LTI systems act as frequency-selective filters: they pass certain frequency components (passband) and attenuate others (stopband). The frequency response $H(e^{j\omega})$ (magnitude and phase) determines how each frequency is scaled and shifted.

**Inverse systems:** An inverse system $H_i(z)$ satisfies $H(z) H_i(z) = 1$. For a stable LTI system, the inverse is stable only if the zeros of $H(z)$ lie inside the unit circle (minimum-phase system).

**Wiener Filter:** An optimum linear filter based on statistical characteristics of the input signal and desired response.

---

## Chapter 7
## The Discrete Fourier Transform (DFT) and FFT

### 7.1 Discrete Fourier Transform (DFT)

**The Discrete Fourier Transform (DFT):** Converts a finite discrete-time signal into its discrete frequency components.

**Definition:** $X(k) = \sum_{n=0}^{N-1} x(n) W_N^{kn}$, where $k = 0, 1, \dots, N-1$, and $W_N = e^{-j2\pi/N}$.

**Twiddle Factor:** $W_N = e^{-j2\pi/N}$.

**Twiddle Factor:** The complex exponential values used as constants in FFT calculations.

**Magnitude vs. Phase:** DFT results are complex variables with a magnitude (strength of frequency) and phase (shift).

**Properties of the DFT:** Properties include: linearity, circular symmetry, time reversal, circular time shift, circular frequency shift, circular convolution (DFT of circular convolution is product of DFTs), Parseval's theorem for DFT, and duality.

**Filtering method using DFT:** Linear filtering of long sequences can be performed using the DFT with overlap-add and overlap-save methods, breaking a long input into blocks, filtering each block in the frequency domain, and combining results.

**Frequency analysis using DFT:** DFT is used to compute the frequency spectrum of finite-duration signals. The resolution is $\Delta f = F_s / N$.

> 💡 **DFT Resolution Example:** Resolution $\Delta f = F_s / N$. For $F_s = 8000 \text{ Hz}$ and $N=8$, the resolution is $1000 \text{ Hz}$.

---

### 7.2 Fast Fourier Transform (FFT) Algorithms

**Fast Fourier Transform (FFT) Algorithms:** An efficient algorithm to compute the DFT.

**Efficiency:** For $N$ points, DFT requires $N^2$ complex multiplications; FFT requires only $(N/2) \log_2 N$.

**Methods:**
- **Decimation-in-Time (DIT):** Decomposes $x(n)$ into smaller sequences (even and odd indexed samples).
- **Decimation-in-Frequency (DIF):** Decomposes the frequency samples $X(k)$.

**Radix-2 FFT:** The most common FFT algorithm, requiring $N$ to be a power of 2.

---

## Chapter 8
## Digital Filter Design (FIR and IIR)

### 8.1 FIR (Finite Impulse Response) Filters

**FIR (Finite Impulse Response) Filters:**
- **Characteristics:** Finite duration impulse response, always stable, can have linear phase.
- **Implementation:** Non-recursive structure (no feedback).
- **Design Methods:**
    - **Window Method:** Truncating the ideal impulse response using windows (Rectangular, Hamming, Hanning, Blackman).
    - **Frequency-Sampling Method:** Specifying the desired response at equally spaced frequencies.

**Filter Choice:** Use FIR for linear phase and stability; use IIR for computational efficiency and sharp roll-off.

---

### 8.2 IIR (Infinite Impulse Response) Filters

**IIR (Infinite Impulse Response) Filters:**
- **Characteristics:** Infinite duration impulse response, more efficient than FIR for same roll-off, but can be unstable.
- **Implementation:** Recursive structure (feedback).
- **Design Methods:**
    - **Impulse Invariance:** Samples the impulse response of an analog filter.
    - **Bilinear Transform:** A mapping technique that avoids aliasing during conversion from analog to digital.

---


## Chapter 9
## Adaptive Filters

### 10.1 Adaptive Filter Fundamentals

**Adaptive filters:** A digital filter whose coefficients are automatically adjusted by an algorithm to minimize an error function.

**Adaptive system:** An adaptive system is a system that automatically adjusts its parameters in response to changes in the environment or input signal statistics to optimize a performance criterion.

**Self-Modifying:** Adjusts in real-time to track variations in signal statistics.

**Error Signal:** $e(k) = d(k) - y(k)$ (Desired - Actual Output).

---

### 9.2 Adaptive Filter Algorithms

**Steepest-descent method:** The steepest-descent method is an iterative optimization algorithm that updates filter coefficients in the direction of the negative gradient of the mean square error (MSE) surface. It is the conceptual basis for the LMS algorithm.

**LMS (Least Mean Square) filters:** LMS is a gradient-based optimization method (Steepest Descent) to minimize Mean Square Error (MSE). It approximates the true gradient using instantaneous estimates: $w(n+1) = w(n) + 2\mu e(n) x(n)$.

**RLS (Recursive Least Squares) adaptive filters:** RLS provides faster convergence but higher computational complexity than LMS. It minimizes the sum of squared errors over all past inputs using an exponentially weighted forgetting factor.

**Kalman filters:** Kalman filters are recursive algorithms that estimate the state of a dynamic system from a series of incomplete and noisy measurements. They are optimal for linear systems with Gaussian noise and have applications in navigation, tracking, and control.

**Adaptation:** The LMS algorithm is the industry standard for real-time weight adjustment based on MSE minimization.

---

### 9.3 Applications of Adaptive Filters

**Applications of Adaptive Filters:**
- **System Identification:** Modeling an unknown plant or channel.
- **Noise Cancellation:** Removing unwanted interference correlated with a reference noise.
- **Channel Equalization:** Compensating for distortion in communication channels.
- **Signal Prediction:** Estimating future samples based on past values.

---

## Chapter 10
## Applications of DSP

### 11.1 Speech Processing

**Speech processing, analysis and coding, and Matlab application:** DSP is extensively used in speech processing for tasks such as speech recognition, speech synthesis, speaker identification, speech enhancement (noise reduction), and speech coding (compression standards like CELP, MELP). MATLAB provides toolboxes (DSP System Toolbox, Signal Processing Toolbox) for designing, simulating, and implementing DSP algorithms.

**Specific speech applications:**
- **Speech analysis:** LPC (Linear Predictive Coding) for modeling vocal tract.
- **Speech coding:** Compression for transmission (e.g., for mobile phones).
- **Speech recognition:** Extracting features (MFCC, Mel-frequency cepstral coefficients) and classification.
- **Speech enhancement:** Noise reduction using spectral subtraction or adaptive filtering.

**Matlab application in DSP:** MATLAB provides functions for: signal generation (sin, cos, randn), filter design (fir1, butter), transform computation (fft, ifft), spectral analysis (periodogram, pwelch), adaptive filters (lms, rls), and wavelet analysis (wavedec, waverec). It also offers Simulink for block-diagram based DSP system modeling.

---

## Quick Reference Summary

| Chapter | Core Topic                | Key Terms                                                                                                                                                       |
| ------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1       | Introduction              | Signal (Continuous/Discrete, Deterministic/Random), System (Linear, Causal, Time-Invariant), DSP advantages (Flexibility, Precision, Storage, Cost, Complexity) |
| 2       | Sampling                  | Nyquist theorem ($F_s \geq 2f_{max}$), Aliasing, Quantization noise, ADC/DAC stages                                                                             |
| 3       | Discrete-Time LTI         | Impulse response $h(n)$, Difference equations, Implementation structures                                                                                        |
| 4       | Correlation & Convolution | $y(n)=x(n)*h(n)$, Cross-correlation, Autocorrelation                                                                                                            |
| 6       | Frequency Analysis        | Fourier transform properties, LTI as frequency-selective filters, Inverse systems, Wiener filter                                                                |
| 7       | DFT & FFT                 | DFT: $X(k)=\sum x(n)W_N^{kn}$, Twiddle factor $W_N=e^{-j2\pi/N}$, FFT efficiency $(N/2)\log_2 N$ vs $N^2$, DIT/DIF                                              |
| 8       | Digital Filters           | FIR (linear phase, stable, window method), IIR (efficient, recursive, bilinear transform)                                                                       |
| 9       | Adaptive Filters          | LMS ($w(n+1)=w(n)+2\mu e(n)x(n)$), RLS (faster convergence, higher complexity), Kalman filters, Steepest-descent                                                |

---
*CSE 3221 — Digital Signal Processing | Dept. of CSE, University of Rajshahi*





