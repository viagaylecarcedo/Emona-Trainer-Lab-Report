# Experiment 20: Undersampling in Software Defined Radio (SDR)
---

# Introduction

Software Defined Radio (SDR) is a communication system in which traditional hardware components such as mixers, filters, modulators, and demodulators are implemented using software rather than dedicated 
hardware circuits.This allows communication systems to be flexible and adaptable to different communication standards. A key concept used in SDR systems is **undersampling**. Normally, according to the 
Nyquist theorem, the sampling frequency must be at least twice the highest frequency component of the signal. However, if the signal bandwidth is limited and properly positioned in frequency, it is 
possible to sample the signal at a rate lower than twice the carrier frequency while still recovering the original information. In this experiment, a **Double Sideband Suppressed Carrier (DSBSC)** signal
is generated and then sampled using a lower sampling frequency. The process demonstrates how **undersampling can still allow signal recovery** if the signal bandwidth is sufficiently limited.

---

# Objectives

The objectives of this experiment are:

* To understand the concept of **undersampling in software defined radio systems**.
* To generate a **DSBSC modulated signal** using a multiplier module.
* To observe the effect of **sampling at a lower rate**.
* To recover the original message signal using a **baseband low-pass filter**.
* To analyze the limitations and conditions required for successful undersampling.

---

# Equipment

The following equipment was used in the experiment:

* Emona Telecoms Trainer 101 (plus power-pack)
* Dual Channel 20 MHz Oscilloscope
* Two Emona Telecoms Trainer Oscilloscope Leads
* Assorted Emona Telecoms Trainer Patch Leads
* Multiplier Module
* Sample-and-Hold (S/H) Module
* Baseband Low-Pass Filter Module
* Master Signal Generator Module

---

# Procedure

## Part A – Setting up a Bandwidth-Limited Signal

1. Gather the required equipment listed in the experiment.
2. Set up the oscilloscope according to the instructions.
3. Configure the trigger source and mode control of the oscilloscope.
4. Connect the circuit according to the block diagram shown in the manual.
5. Adjust the oscilloscope timebase to display two or three cycles of the signal.
6. Observe both the **message signal** and the **DSBSC signal**.

### Figure 2 
<img width="388" height="336" alt="image" src="https://github.com/user-attachments/assets/cba5f0d4-87a0-4967-883f-e9ec14ddabac" />

### OUTPUT
<img width="490" height="368" alt="image" src="https://github.com/user-attachments/assets/4c312950-f4d4-4693-90ba-14804cb522b4" />
---

## Part B – Direct Down Conversion Using Undersampling

7. Configure the **Sample-and-Hold module** to sample the incoming DSBSC signal.
8. Set the sampling signal frequency according to the experiment instructions.
9. Observe the **undersampled signal waveform** using the oscilloscope.
10. Compare the undersampled signal with the original message signal.

### Figure 4 
<img width="345" height="241" alt="image" src="https://github.com/user-attachments/assets/c7831507-6222-4bf4-b8d4-041550a4dca5" />

###OUTPUT 
<img width="460" height="341" alt="image" src="https://github.com/user-attachments/assets/4738907e-8a9f-465a-8705-381a0201b3e6" />

---

## Part C – Synchronisation

11. Locate the **VCO module** and set its range control to the required position.
12. Adjust the VCO frequency control to the middle of its travel.
13. Connect the oscilloscope channel to observe the VCO digital output.
14. Adjust the VCO digital output frequency to approximately **8.33 kHz**.
15. Observe both the original and recovered message signals.

<img width="490" height="374" alt="image" src="https://github.com/user-attachments/assets/65b31ac9-6622-4ca3-b5bc-ec751dfe32a8" />
---

# Summary of Findings and Results

The experiment demonstrated that undersampling can be used to recover signals even when the sampling frequency is lower than twice the carrier frequency. 
By ensuring that the signal bandwidth is limited, aliasing can be controlled in such a way that the desired signal appears in the baseband frequency region.
During the experiment, a DSBSC signal was generated using the multiplier module. The signal was then sampled using the sample-and-hold circuit at a lower sampling
frequency. Despite the reduced sampling rate, the original message signal was successfully recovered using a baseband low-pass filter.
The experiment also showed that synchronization between the sampling frequency and the signal frequency is important for successful signal recovery.

---

# Observations

## 1.1 Generation of the DSBSC Signal

The multiplier module produced a DSBSC signal where the carrier component was suppressed and only the sidebands remained. The waveform observed on the oscilloscope appeared 
as an amplitude-modulated waveform with alternating polarity.

## 2.1 Undersampled Signal

When the signal was sampled using the sample-and-hold module, the waveform appeared distorted compared to the original signal. However, the sampled signal still contained enough
information to reconstruct the original message.

## 3.1 Message Recovery

After passing the undersampled signal through the baseband low-pass filter, the recovered waveform closely resembled the original message signal, confirming that undersampling 
can be used effectively in SDR systems.


# Lab Questions and Answers

### Question 1

From the inputs to the multiplier module, what are the frequencies of the two sinewaves that make up the DSBSC signal?
The DSBSC signal is composed of the **sum and difference frequencies** of the carrier and message signals. If the carrier frequency is 100 kHz and the message frequency is 
2 kHz, the resulting sideband frequencies are **98 kHz and 102 kHz**.

### Question 2

What is the bandwidth of the DSBSC signal?
The bandwidth of a DSBSC signal is **twice the message signal frequency**. If the message signal frequency is 2 kHz, then the total bandwidth is **4 kHz**.

### Question 3

What is the significance of the signal on the Baseband LPF's output?
The output of the baseband low-pass filter represents the **recovered message signal**. It removes the high-frequency components introduced by the sampling process and leaves only the original baseband signal.

### Question 4

Which harmonic in the sampling signal is demodulating the DSBSC signal?
The harmonic that matches the frequency difference between the carrier and sampling signal performs the demodulation. In this experiment, the **8.33 kHz sampling signal harmonic**
is responsible for demodulating the DSBSC signal.

### Question 5

Why doesn't adjusting the VCO frequency solve the synchronization problem?
Adjusting the VCO frequency alone cannot perfectly synchronize the demodulation process because slight frequency mismatches still exist between the sampling signal and the carrier 
frequency. These mismatches introduce phase errors that prevent stable demodulation.

---

# Conclusion

This experiment demonstrated the concept of **undersampling in Software Defined Radio (SDR)** systems. A DSBSC signal was generated and sampled at a lower frequency using a sample-and-hold circuit. 
  Despite sampling below the traditional Nyquist rate, the original message signal was successfully recovered due to the limited bandwidth of the signal.

The experiment showed that undersampling can be used effectively in communication systems when the signal spectrum is properly positioned. It also highlighted the importance of synchronization and proper filtering in recovering the original message signal.
