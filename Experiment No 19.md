<img width="490" height="367" alt="image" src="https://github.com/user-attachments/assets/7320f580-8627-4ea5-b55f-40305e4a2d23" /># Experiment No 19 DSSS Modulation and Demodulation

---

# INTRODUCTION

Direct Sequence Spread Spectrum (DSSS) is a digital communication technique that spreads a signal across a wider frequency band than the original message signal. 
This is achieved by multiplying the message signal with a high-frequency pseudo-noise (PN) sequence. The resulting signal appears noise-like and occupies a much
larger bandwidth compared to the original signal.DSSS is widely used in wireless communication systems because it improves resistance to interference, jamming,
and signal interception. Since the signal is spread over a wide frequency range, it becomes difficult for unwanted signals or noise to completely disrupt the transmission.
In this experiment, DSSS modulation and demodulation are implemented using the Emona Telecoms Trainer to observe how spread spectrum techniques work in practical communication systems.

---

# OBJECTIVES

The objectives of this experiment are:

* To understand the concept of **Direct Sequence Spread Spectrum (DSSS)** modulation.
* To generate a DSSS signal using a **pseudo-noise (PN) sequence**.
* To observe the characteristics of the DSSS signal using an oscilloscope.
* To recover the original message signal using a **product detector**.
* To analyze the effect of **interference and jamming** on DSSS communication systems.

---

# EQUIPMENT

1. Emona Telecoms Trainer 101 (plus power-pack)
2. Dual Channel 20 MHz Oscilloscope
3. Two Emona Telecoms-Trainer Oscilloscope leads
4. Assorted Emona Telecoms-Trainer 101 patch leads
5. Sequence Generator Module
6. Multiplier Module
7. Tuneable Low-Pass Filter Module
8. Adder Module
9. Voltage Controlled Oscillator (VCO) Module
10. Speech Module

---

# PROCEDURE

## Part A – Generating a DSSS Signal

1. Gather the required equipment and set up the oscilloscope according to the instructions.
2. Configure the oscilloscope trigger source and mode settings.
3. Locate the **Sequence Generator module** and configure it to generate the PN sequence.
4. Connect the circuit according to the block diagram provided in the experiment manual.
5. Adjust the oscilloscope timebase control to observe the signals clearly.
6. Observe both the **message signal** and the **DSSS signal** at the multiplier output.
7. Record or sketch the waveforms displayed on the oscilloscope.

### Figure 2 
<img width="345" height="361" alt="image" src="https://github.com/user-attachments/assets/f57b9a66-dd5a-4ab5-94e5-d516d6fbade2" />

### OUTPUT  
<img width="490" height="372" alt="image" src="https://github.com/user-attachments/assets/901a141f-351d-450c-9cb8-5fee48e9cd20" />

---

## Part B – Generating DSSS Signal Using Speech

8. Disconnect the original message source from the master signal generator.
9. Connect the **Speech module output** as the message input signal.
10. Observe the DSSS waveform while speaking or producing sound into the speech module.

<img width="490" height="373" alt="image" src="https://github.com/user-attachments/assets/e4632177-acc6-4447-b6f3-09f5c2230db6" />

---

## Part C – Recovering the Message

11. Connect the **product detector circuit** using the multiplier module.
12. Use the same **PN sequence** that was used in the transmitter.
13. Pass the output through the **Tuneable Low-Pass Filter**.
14. Adjust the filter cutoff frequency until the original message signal is recovered.

### Figure 5 
<img width="490" height="295" alt="image" src="https://github.com/user-attachments/assets/11e5a5f5-2f1c-4268-a2bd-43ef0b610b1e" />

### OUTPUT 
<img width="446" height="339" alt="image" src="https://github.com/user-attachments/assets/e6db5b91-2d56-45a0-b050-1385f7a0ebee" />

### Figure 6 
<img width="439" height="260" alt="image" src="https://github.com/user-attachments/assets/80f908be-1c2b-41bf-9849-34d8f14a15b5" />

### OUTPUT
<img width="490" height="367" alt="image" src="https://github.com/user-attachments/assets/aa54b400-7320-4557-87cc-b66a58ebf780" />
---

## Part D – DSSS with Interference

15. Introduce interference into the system using the **Adder module**.
16. Observe how the interference affects the DSSS signal.
17. Compare the recovered message signal before and after interference is introduced.

### Figure 9 
<img width="490" height="251" alt="image" src="https://github.com/user-attachments/assets/7731725a-5a8a-44d9-9a20-0eafe825c55c" />

### OUTPUT 
<img width="426" height="318" alt="image" src="https://github.com/user-attachments/assets/281c1185-2f81-4538-aaab-c272787f7936" />

---

# SUMMARY OF FINDINGS AND RESULTS

The experiment demonstrated the generation and recovery of a Direct Sequence Spread Spectrum (DSSS) signal.
By multiplying the message signal with a pseudo-noise sequence, the signal bandwidth increased significantly, making the signal appear random and noise-like.
The DSSS signal was successfully demodulated using a product detector and a low-pass filter. When the correct PN sequence was used in the receiver, the
original message signal was recovered. However, when interference or an incorrect PN sequence was introduced, the recovered signal became distorted. This 
highlights the importance of synchronization between the transmitter and receiver in DSSS communication systems.

---

# OBSERVATION

## 1.1 Observation – DSSS Signal Generation
The oscilloscope displayed both the original message signal and the DSSS signal. The DSSS signal appeared more complex and noise-like compared to
the original signal because the message was multiplied with a pseudo-noise sequence. This caused the signal to spread over a wider bandwidth.

---

## 2.1 Observation – Message Recovery
After passing the DSSS signal through the product detector and low-pass filter, the recovered signal resembled the original message. Minor distortions
were observed due to filtering effects and possible noise in the system.

---

## 3.1 Observation – Effect of Interference
When interference was introduced into the system, the DSSS signal became distorted. However, the receiver was still able to recover the original message
when the correct PN sequence was used. This demonstrates the strong resistance of DSSS systems to interference and jamming.

---

# LAB QUESTIONS AND ANSWERS

### Q1: What feature of the multiplier module's output suggests that it is basically a DSBSC signal?
The multiplier output shows the absence of the carrier component while only the sideband frequencies remain. This indicates that the signal behaves similarly 
to a Double Sideband Suppressed Carrier (DSBSC) signal.

---

### Q2: Why is the DSSS signal large when it is supposed to be small and indistinguishable from noise?
The signal appears large on the oscilloscope because the display amplifies the waveform for observation. In reality, the signal energy is spread across a
wide frequency band and appears noise-like.

---

### Q3: Why isn't there any signal out of the DSSS modulator when you're not talking?
When no speech or input signal is present, the message signal is essentially zero. Since DSSS modulation multiplies the message signal with the PN sequence, 
no significant output is generated without an input signal.

---

### Q4: What does the signal out of the low-pass filter look like?
The output of the low-pass filter resembles the original message signal because the filter removes the high-frequency PN components and restores the baseband message.

---

### Q5: Why does using the wrong PN sequence for the local carrier cause the product detector’s output to look distorted?
Using the wrong PN sequence prevents proper correlation between the transmitted signal and the receiver's local sequence. As a result, the signal cannot be properly despread,
causing distortion or noise in the recovered output.

---

### Q6: Why doesn’t the jamming signal interfere with the recovery of the message?
The DSSS technique spreads the signal across a wide frequency band. When the receiver multiplies the signal with the correct PN sequence, the desired signal is reconstructed 
while most interference and jamming signals are suppressed.

---

# CONCLUSION
This experiment demonstrated the operation of Direct Sequence Spread Spectrum (DSSS) modulation and demodulation using the Emona Telecoms Trainer. The message signal was 
successfully spread using a pseudo-noise sequence, producing a signal with a much widerbandwidth. This spreading process allowed the signal to appear noise-like and improved its resistance to interference.
The original message was successfully recovered at the receiver using a product detector and a low-pass filter when the correct PN sequence was used. The experiment also showed that interference and jamming 
signals had minimal effect on the recovered message when the proper PN sequence was applied. Overall, the experiment highlighted the advantages of DSSS systems in terms of improved security, resistance to
interference, and reliable communication. This experiment demonstrated the operation of Direct Sequence Spread Spectrum (DSSS) modulation and demodulation using the Emona Telecoms Trainer. The message signal 
was successfully spread using a pseudo-noise sequence, producing a signal with a much wider bandwidth. This spreading process allowed the signal to appear noise-like and improved its resistance to interference.
The original message was successfully recovered at the receiver using a product detector and a low-pass filter when the correct PN sequence was used. The experiment also showed that interference and jamming
signals had minimal effect on the recovered message when the proper PN sequence was applied. Overall, the experiment highlighted the advantages of DSSS systems in terms of improved security, resistance to 
interference, and reliable communication.
