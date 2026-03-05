# EXPERIMENT NO 17 BINARY PHASE SHIFT KEYING (BPSK)

---

# INTRODUCTION:

Binary Phase Shift Keying (BPSK) is a digital modulation technique commonly used in digital communication systems and frequency division multiplexing (FDM) environments. 
In BPSK, digital information is transmitted by shifting the phase of a carrier signal between two discrete values, typically 0° and 180°, to represent logic 1 and logic 0. 
Unlike amplitude and frequency-based modulation schemes, the carrier’s amplitude and frequency remain constant while only the phase changes. One of the key advantages of BPSK 
is its strong immunity to noise, making it one of the most robust digital modulation techniques. Since information is encoded in the phase of the carrier, BPSK performs well 
in noisy channels and requires relatively low signal power for reliable transmission.

---

# OBJECTIVES:

In this experiment, we will be able to use the **ETT-101 Trainer** to generate a **BPSK signal using the Multiplier module** to implement its mathematical model. Additionally,
we will be able to understand the **demodulation and restoration process** of a BPSK signal using a **Product Detector and Comparator**.

---

# EQUIPMENT TO BE USED:

1. Emona Telecoms-Trainer 101 (plus power-pack)  
2. Dual channel 20 MHz Oscilloscope  
3. Two Emona Telecoms-Trainer Oscilloscope leads  
4. Assorted Emona Telecoms-Trainer 101 patch leads  
5. One set of Headphones (stereo)

---

# PROCEDURE:

## Part A – Generating a BPSK Signal

1. Gather all the equipment listed above.  
2. Set up the oscilloscope according to the instructions in the previous experiment.  
3. Set the oscilloscope **Trigger Source control to EXT**.  
4. Set the **Trigger Source Coupling control to HF REJ**.  
5. Set the **Channel 1 and Channel 2 input coupling controls to DC**.  
6. Set the oscilloscope **Timebase control to 0.1 ms/div**.  
7. Locate the **Sequence Generator module** and set its **DIP switches to 00**.  
8. Connect the circuit setup according to the diagram provided in the manual.  
9. Set the oscilloscope **Mode control to DUAL** to view both the digital signal and the BPSK signal.  
10. Activate the oscilloscope **Sweep Magnification control**.  
11. Adjust the **Horizontal Position control** if necessary to observe at least one transition of the digital signal.  
12. Compare the **digital signal** with the **BPSK signal** displayed on the oscilloscope.  
13. Deactivate the **Sweep Magnification control**.  
14. Adjust the **Channel 1 Vertical Position control** so that the digital signal aligns with the BPSK signal envelope.

### Figure 3 
<img width="490" height="379" alt="image" src="https://github.com/user-attachments/assets/972b5bd4-2a07-494e-a56e-5a12dccc862c" />

---

## Part B – Demodulating a BPSK Signal Using a Product Detector

15. Locate the **Tuneable Low-Pass Filter (LPF)** module and turn its **Cut-off Frequency Adjust control fully clockwise**.  
16. Set the **LPF Gain control** to about the **middle of its travel**.  
17. Modify the circuit setup to include the **Product Detector configuration** as shown in the diagram.  
18. Observe the **demodulated BPSK signal** on the oscilloscope.  
19. Compare the **original digital signal** with the **recovered signal** from the demodulator.

### Figure 5 
<img width="418" height="321" alt="image" src="https://github.com/user-attachments/assets/65096daa-aab5-4051-ba07-bfdf47590a5d" />

---

## Part C – Restoring the Recovered Data using a Comparator

20. Set the **Variable DC module’s control** to about the **middle of its travel**.  
21. Connect the **Comparator module** to the recovered signal output.  
22. Adjust the **Variable DC reference voltage** until the comparator output aligns with the original digital signal.  
23. Observe the restored digital waveform on the oscilloscope and compare it with the original data signal.

### Figure 7 
<img width="467" height="355" alt="image" src="https://github.com/user-attachments/assets/a815c56e-190e-4ee7-b0cb-48ef12cf6f4c" />

---

# SUMMARY OF FINDINGS AND RESULTS:

## 1. Generating an BPSK Signal
In the first part of the experiment, we generated a BPSK signal using the **Multiplier module** which implements the mathematical model of BPSK modulation. 
The digital signal from the **Sequence Generator** controls the phase of the carrier signal.

### 1.1 OBSERVATION
As observed in the oscilloscope output, two distinct signals are displayed. The **top waveform (red)** represents the digital message signal from the Sequence
Generator, showing a clear pulse train acting as the data input. The **bottom waveform (yellow)** represents the modulated BPSK signal. When the digital input 
changes state, the phase of the **100 kHz carrier signal shifts by 180 degrees**, producing the BPSK modulation.

---

## 2. Demodulating a BPSK Signal using a Product Detector
In the second part of the experiment, the BPSK signal was demodulated using a **Product Detector**, which is a common method used in **DSBSC demodulation**. 
The demodulator multiplies the received BPSK signal with a locally generated carrier signal and passes the result through a low-pass filter.

### 2.1 OBSERVATION
The oscilloscope shows the successful recovery of the original message signal through product detection. The **top waveform (red)** represents the original
digital signal before modulation. The **bottom waveform (yellow)** shows the demodulated signal after passing through the product detector and the low-pass 
filter. Although the waveform follows the digital logic levels, it exhibits **rounded edges and slight ripples** due to filtering effects.

---

## 3. Restoring the Recovered Data using a Comparato
In the final stage, the recovered signal is passed through a **Comparator circuit** to restore a clean digital waveform. The comparator compares the filtered 
signal with a reference voltage generated by the **Variable DC module**.

### 3.1 OBSERVATION
The restoration of the digital signal depends on the correct adjustment of the **DC reference voltage**. By setting the threshold at approximately the midpoint 
of the signal amplitude, the comparator converts the filtered analog waveform into a clean digital signal. If the reference voltage is set too high or too low, 
incorrect pulse widths or missed transitions may occur.

---

# LAB QUESTIONS AND ANSWERS:

**Question 1: What happens to the BPSK signal on the data stream logic transition?**  
The BPSK signal undergoes a 180° phase reversal whenever the digital data changes state between logic 0 and logic 1. This phase shift represents the change in the transmitted binary information.

**Question 2: What feature of the BPSK signal suggests that it is a DSBSC signal?**  

A key feature of the BPSK signal is the absence of a visible carrier component and the polarity inversion of the waveform. These characteristics indicate that
the signal behaves like a Double Sideband Suppressed Carrier (DSBSC) signal.

**Question 3: Why is the recovered digital signal not a perfect copy of the original?**  

The recovered signal passes through filters and demodulation circuits that introduce rounded edges, slight delays, and small ripples in the waveform. In addition, noise and bandwidth limitations 
affect the sharpness of the signal transitions, preventing it from being an exact replica of the original digital signal.

**Question 4: What can be used to clean up the recovered digital signal?**  

A comparator circuit can be used to clean up the recovered signal. It converts the distorted analog waveform into a clean digital signal with clear logic levels..

**Question 5: What does varying the DC voltage on the comparator’s input change in the digital signal?**  
Adjusting the DC reference voltage changes the switching threshold of the comparator. When set correctly, it produces accurate and clean logic levels. If the threshold is set too high or too low, 
it may result in missed transitions or distorted pulse widths
---

# CONCLUSION:

This experiment successfully demonstrated the principle of **Binary Phase Shift Keying (BPSK)** modulation and demodulation using the **Emona Telecoms-Trainer 101**. The digital signal generated by
the Sequence Generator controlled the phase of a carrier signal, producing a BPSK waveform where phase changes represent digital data. 
Through the use of a **Product Detector and a Tuneable Low-Pass Filter**, the original message signal was successfully recovered from the modulated waveform.
However, the recovered signal exhibited **rounded edges and slight distortions** due to filtering effects and system limitations. By introducing a **Comparator circuit**, the demodulated 
signal was restored into a clean digital waveform with accurate logic levels. The experiment demonstrated the importance of proper **threshold adjustment and signal processing techniques** 
in restoring digital data in communication systems. Overall, the experiment highlights how **BPSK provides reliable digital communication with strong noise immunity**, making it widely used 
in modern digital communication technologies such as satellite communication, wireless systems, and digital broadcasting.
