# >xperiment No 16 FREQUENCY SHIFT KEYING (FSK)

---

# INTRODUCTION:
Frequency Shift Keying (FSK) is a digital modulation technique in which digital data is transmitted by shifting the frequency of a carrier signal 
between two discrete values. Unlike Amplitude Shift Keying (ASK), where the amplitude changes, FSK represents digital information through changes in
the carrier frequency while keeping the amplitude constant.In FSK communication systems, one frequency represents logic **1 (mark frequency)** and 
another frequency represents logic **0 (space frequency)**. Because the amplitude remains constant, FSK is generally more resistant to noise and signal 
distortion than ASK. This makes FSK suitable for many communication applications such as radio communication, modems, and data transmission systems.
In this experiment, the Emona Telecoms-Trainer 101 is used to generate an FSK signal using a Voltage Controlled Oscillator (VCO). The generated FSK signal is 
then demodulated using filtering and envelope detection, and finally the recovered digital signal is restored using a comparator.

---

# OBJECTIVES:

In this experiment, we will use the Emona Telecoms-Trainer 101 to generate an FSK signal using a Voltage Controlled Oscillator (VCO). The digital message signal
is produced using the Sequence Generator module. The generated FSK signal will be observed and analyzed. The experiment will also demonstrate how the FSK signal
can be demodulated using filtering and envelope detection. Finally, a comparator will be used to restore the recovered digital signal.

---

# EQUIPMENT TO BE USED:

1. Emona Telecoms-Trainer 101 (plus power-pack)  
2. Dual Channel 20 MHz Oscilloscope  
3. Two Emona Telecoms-Trainer Oscilloscope leads  
4. Assorted Emona Telecoms-Trainer 101 patch leads  

---

# PROCEDURE:

## Part A – Generating an FSK Signal

1. Gather the equipment listed above.
2. Set up the oscilloscope according to the instructions.
3. Set the oscilloscope **Trigger Source control to the EXT position**.
4. Set the oscilloscope **Trigger Source Coupling control to the HF REJ position**.
5. Set the oscilloscope **Channel 1 and Channel 2 input coupling controls to the DC position**.
6. Locate the **VCO module** and set its **Gain control to about half its travel**.
7. Set the **VCO Frequency Adjust control** to about one quarter of its travel.
8. Set the **VCO Range control to the LO position**.
9. Locate the **Sequence Generator module** and set its **DIP switches to 00**.
10. Connect the setup as shown in the experiment diagram.
11. Set the oscilloscope **Timebase control to 0.5 ms/div**.
12. Set the oscilloscope **Mode control to DUAL**.
13. Observe the digital signal from the Sequence Generator and the FSK signal from the VCO module on the oscilloscope.
14. Compare the two signals.

### Figure 3 
<img width="490" height="373" alt="image" src="https://github.com/user-attachments/assets/de51c49b-3191-4e65-807b-378eee91e437" />

---

## Part B – Demodulating the FSK Signal

15. Locate the **Tuneable Low Pass Filter (LPF)** module.
16. Turn the **LPF Gain control fully clockwise**.
17. Adjust the **LPF Cut-off Frequency control** slowly until one of the frequencies in the FSK signal becomes dominant.
18. Observe the filtered signal and the digital signal on the oscilloscope.

### Figure 5 
<img width="447" height="339" alt="image" src="https://github.com/user-attachments/assets/b385fc69-5980-4ffc-88f3-479b3acf1b4f" />

### Figure 7 
<img width="490" height="390" alt="image" src="https://github.com/user-attachments/assets/80a90962-5215-4b63-9dbc-2587c71ddbcd" />

---

## Part C – Restoring the Recovered Digital Signal

19. Modify the setup to include the **Envelope Detector** and **Comparator circuit**.
20. Connect the filtered signal into the **Comparator input**.
21. Adjust the **reference voltage** of the comparator to about half of the recovered signal amplitude.
22. Observe the restored digital signal on the oscilloscope.
23. Compare the restored signal with the original digital signal.

### Figure 9
<img width="490" height="369" alt="image" src="https://github.com/user-attachments/assets/a9f01582-e56e-4efe-bd84-c66d5eeff46c" />

---

# SUMMARY OF FINDINGS AND RESULTS:

## 1. Generating an FSK Signal
In the first part of the experiment, the Sequence Generator module produces a digital signal that controls the Voltage Controlled Oscillator (VCO). The
VCO generates two frequencies depending on the logic level of the digital input.
### 1.1 Observation
It is observed that the FSK signal alternates between two different frequencies depending on the digital input signal. When the digital signal is **logic 1**,
the VCO outputs the **mark frequency**, which is the higher frequency. When the digital signal is **logic 0**, the VCO outputs the **space frequency**, which is lower.

---

## 2. Demodulating the FSK Signal
The FSK signal is passed through a **Tuneable Low Pass Filter** that selects one of the two frequencies present in the signal.

### 2.1 Observation
The filter selects one frequency component while attenuating the other. When the filter is tuned near the mark frequency, that component becomes dominant. 
The output waveform begins to resemble the digital signal envelope.

---

## 3. Restoring the Recovered Digital Signal
The filtered signal is passed through an envelope detector and comparator circuit.

### 3.1 Observation
The envelope detector converts the filtered waveform into a slowly varying voltage corresponding to the digital signal. 
The comparator then converts this signal into a clean digital waveform with sharp transitions.

---

# LAB QUESTIONS AND ANSWERS:

### Question 1: What is the name for the VCO output frequency that corresponds with logic 1 in the digital data?
The VCO output frequency corresponding to logic 1 is called the **Mark Frequency**.

---

### Question 2: Based on your observations of the FSK signal, which of the two frequencies is the higher frequency?
The **Mark frequency** is the higher frequency, while the **Space frequency** is the lower frequency.

---

### Question 3: Which of the FSK signal's two sinewaves is the filter picking out?
The filter selects the frequency closest to its cut-off frequency. By adjusting the filter, either the mark or space frequency can be selected.

---

### Question 4: What does the filtered FSK signal look like?
The filtered signal appears as a sinusoidal waveform whose amplitude varies depending on whether the selected frequency is present.

---

### Question 5: What can be used to clean up the recovered digital signal?
A **comparator** is used to clean up the recovered signal and restore it into a digital waveform.

---

### Question 6: How does the comparator convert slow rising voltages into sharp transitions?
The comparator switches its output when the input voltage crosses a reference voltage. This converts gradual voltage changes into sharp transitions between logic high and logic low.

---

# CONCLUSION:

This experiment demonstrated the principle of **Frequency Shift Keying (FSK)** modulation. The digital signal controls the frequency of the carrier generated by the VCO,
producing two distinct frequencies representing binary information.The experiment also showed how FSK signals can be demodulated using filtering and envelope detection. 
Although the recovered signal resembles the original digital data, distortions can occur due to filtering effects and noise. Finally, the comparator successfully restores 
the distorted signal into a clean digital waveform by converting slow voltage changes into sharp transitions. The results highlight how FSK modulation can effectively transmit 
digital information and how signal processing techniques are used to recover the original message.
