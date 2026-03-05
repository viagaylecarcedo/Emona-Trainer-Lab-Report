Experiment No. 18 QUADRATURE PHASE SHIFT KEYING (QPSK)

---

# INTRODUCTION

Quadrature Phase Shift Keying (QPSK) is a digital modulation technique that improves data transmission efficiency by encoding two bits of information in a single symbol. 
It is an extension of Binary Phase Shift Keying (BPSK), where the carrier signal can take four different phase states instead of two. In QPSK, the incoming digital data 
stream is divided into two separate bit streams known as the **In-phase (I)** and **Quadrature (Q)** components. These signals modulate two carrier signals that are **90°
out of phase** with each other. The two modulated signals are then combined to produce the QPSK signal. QPSK is widely used in modern communication systems such as **satellite 
communication, wireless networks, and digital broadcasting** because it allows higher data transmission rates while maintaining good resistance to noise and signal distortion.

---

# OBJECTIVES

The objectives of this experiment are:

* To understand the principle of **Quadrature Phase Shift Keying (QPSK)** modulation
* To observe how a **serial data stream is converted into parallel data streams** for QPSK transmission
* To generate two **BPSK signals that form the I and Q components** of the QPSK signal
* To combine the two BPSK signals to produce a **QPSK waveform**
* To analyze the **demodulation of the QPSK signal**

---

# EQUIPMENT

1. Emona Telecoms Trainer 101 (plus power pack)
2. Dual Channel 20 MHz Oscilloscope
3. Two Oscilloscope Leads
4. Assorted Patch Leads
5. Sequence Generator Module
6. Serial-to-Parallel Converter Module
7. Multiplier Modules
8. Adder Module
9. Phase Shifter Module
10. Tuneable Low Pass Filter Module

---

# PROCEDURE

## Part A – Generating the Digital Data Streams

1. Gather all required equipment listed above.
2. Set up the oscilloscope according to the experiment instructions.
3. Set the oscilloscope **Trigger Source to EXT**.
4. Set the oscilloscope **input coupling to DC**.
5. Adjust the oscilloscope **Timebase control to approximately 0.5 ms/div**.
6. Configure the **Sequence Generator** to produce a digital data sequence.
7. Connect the circuit according to the experiment diagram.
8. Observe the **Serial-to-Parallel Converter outputs** representing the even and odd bits.

### Figure 2

### figure 6 


---

## Part B – Generating the BPSK Signals

9. Connect the outputs of the Serial-to-Parallel Converter to the **Multiplier modules**.
10. Apply the **carrier signals that are 90° out of phase** to the multipliers.
11. Observe the resulting **BPSK signals** on the oscilloscope.
12. Compare the phase changes of the carrier signals with the digital input signals.

---

## Part C – Generating the QPSK Signal

13. Connect the outputs of the multiplier modules to the **Adder module**.
14. Adjust the Adder control until a stable output signal is observed.
15. Observe the resulting **QPSK waveform** on the oscilloscope.
16. Compare the QPSK waveform with the individual BPSK signals.

---

## Part D – Demodulating the QPSK Signal

17. Modify the circuit according to the **demodulation block diagram**.
18. Use **product detectors and a tuneable low-pass filter** to recover the digital data.
19. Adjust the **Phase Shifter module** until the recovered signals are visible.
20. Compare the recovered signals with the original digital data.

---

# SUMMARY OF FINDINGS AND RESULTS

## 1. Generating the Digital Data Streams

In the first stage of the experiment, the digital data stream produced by the sequence generator was divided into two signals using a **Serial-to-Parallel Converter**. 
These signals represent the **even and odd bits** of the original digital sequence. This process allows two bits to be transmitted simultaneously in the QPSK modulation scheme.

### 1.1 OBSERVATION

The oscilloscope displayed two digital square-wave signals representing the even and odd data streams. These signals operate at **half the bit rate** of the original signal 
because the serial data stream is divided into two parallel streams.

---

## 2. Generating the BPSK Signals

Each digital signal was used to modulate a carrier using a **Multiplier module**, generating two BPSK signals corresponding to the **I (In-phase)** and **Q (Quadrature)** components.

### 2.1 OBSERVATION

The oscilloscope showed phase reversals in the carrier waveform whenever the digital input changed state. These signals were observed to be **90° out of phase**, confirming 
the required relationship between the I and Q components.

---

## 3. Generating the QPSK Signal

The two BPSK signals were combined using an **Adder module**, producing the final QPSK signal.

### 3.1 OBSERVATION

The resulting waveform showed **four distinct phase states**, corresponding to the four possible combinations of two input bits. This confirmed that the output signal is a
QPSK signal capable of transmitting **two bits per symbol**.

---

# LAB QUESTIONS AND ANSWERS

### Q1: What is the relationship between the bit time of the two digital signals and the bit rate of the sequence generator output?
The bit time of the two digital signals is **twice that of the original signal** because the serial data stream is divided into two parallel streams.

### Q2: What feature of the multiplier output suggests that it is a BPSK signal?
The carrier waveform undergoes a **180° phase shift** whenever the input digital signal changes state.

### Q3: What type of signal is present on the multiplier output?
The multiplier output produces a **Binary Phase Shift Keying (BPSK) signal**.

### Q4: According to theory, what type of signal is present at the adder output?
The signal at the adder output is a **Quadrature Phase Shift Keying (QPSK) signal**.

### Q5: Why is there only one sine wave when the QPSK signal is made up of two BPSK signals?
The two BPSK signals combine into a **single waveform whose phase changes depending on the input data**.

### Q6: What causes the multi-level signals observed at the tuneable LPF output?
The multi-level signals occur due to **phase differences between the local carrier and the transmitted carrier** during demodulation.

### Q7: What phase relationship must exist between the local carrier and the transmitted carrier signals?
The local carrier must have the **same frequency and proper phase alignment** with the transmitted carrier signals.

### Q8: What phase relationship is required for correct demodulation?
Correct demodulation requires the **local carrier to be synchronized in both frequency and phase** with the original carrier.

### Q9: Why is the demodulator considered only half of a full QPSK receiver?
The demodulator implemented in the experiment only recovers **one of the two BPSK components**. A complete QPSK receiver requires **two demodulators to recover both I and Q signals**.

---

# CONCLUSION

This experiment demonstrated the operation of **Quadrature Phase Shift Keying (QPSK)** modulation and demodulation using the Emona Telecoms Trainer. The experiment showed how a single
digital data stream can be divided into two parallel streams that modulate two carriers separated by 90 degrees. These two BPSK signals were then combined to form the final QPSK waveform.
The experiment also showed that QPSK allows the transmission of **two bits per symbol**, making it more bandwidth-efficient than BPSK. Through observation and analysis using the oscilloscope,
the relationship between the digital data, carrier phase shifts, and the resulting QPSK signal was clearly demonstrated.
