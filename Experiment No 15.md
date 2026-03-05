# Experiment 15 – Amplitude Shift Keying (ASK)

## Objectives

- To understand the concept of Amplitude Shift Keying (ASK) in digital communications.
- To generate an ASK signal using the Emona Telecoms Trainer.
- To observe the relationship between a digital signal and the ASK modulated signal.
- To demodulate an ASK signal using envelope detection.
- To restore a distorted digital signal using a comparator.

---

# Materials and Equipment

Emona Telecoms Trainer 101 
Dual Channel Oscilloscope 
Oscilloscope Leads 
Patch Leads 
Sequence Generator, Dual Analog Switch, VCO, Utilities Module, Tuneable Low-Pass Filter 

---

# Procedure

## Part A – Generating an ASK Signal

1. Gather the equipment listed above.
2. Set up the oscilloscope according to the instructions.
3. Set the oscilloscope **Mode control to the DUAL position**.
4. Set the oscilloscope **Trigger Source control to EXT**.
5. Set the **Trigger Source Coupling control to HF REJ**.
6. Set **Channel 1 and Channel 2 Input Coupling controls to DC**.
7. Set the **Timebase control to the 1 ms/div position**.
8. Connect the circuit as shown in the experiment diagram.
9. Observe the **Sequence Generator output and the ASK signal** from the Dual Analog Switch module.
10. Compare the digital signal with the ASK signal on the oscilloscope.

### Figure 2 
<img width="490" height="368" alt="image" src="https://github.com/user-attachments/assets/c57e8b60-ccf0-48d1-af4c-23c5ddfa2614" />

### Figure 4
<img width="490" height="373" alt="image" src="https://github.com/user-attachments/assets/26c1c4cc-6e20-4fce-9d31-25d4c5215422" />

---

## Part B – Demodulating the ASK Signal

11. Locate the **Tuneable Low-Pass Filter module**.
12. Turn its **Gain control fully clockwise**.
13. Turn the **Cut-off Frequency Adjust control fully clockwise**.
14. Modify the setup according to the demodulation diagram.
15. Observe the demodulated ASK signal on the oscilloscope.

### Figure 6 
<img width="436" height="330" alt="image" src="https://github.com/user-attachments/assets/0c3f63ae-d25a-491d-a69d-f1a1a2b578e4" />


---

## Part C – Restoring the Digital Signal

16. Modify the setup to include the **Comparator in the Utilities Module**.
17. Use the comparator to restore the digital signal.
18. Observe the restored digital signal and compare it with the original signal.

### Figure 8
<img width="490" height="368" alt="image" src="https://github.com/user-attachments/assets/434ec0da-5057-4bd2-8310-2cb44dfcae01" />

---

# Results and Observations

### Generating an ASK Signal with VCO
In this part of the experiment, the fixed carrier is replaced with a **Voltage Controlled Oscillator (VCO)** to generate the ASK signal.

### 2.1 Observation
By replacing the fixed carrier with the VCO, the ASK signal is produced through switching of a high-frequency carrier controlled by the digital input 
signal. When the digital signal is at logic high, the analog switch allows bursts of the carrier signal to pass through. The oscilloscope shows a carrier 
frequency of approximately **1.806 kHz** and a peak-to-peak voltage of **4.080 V**. When the digital signal is low, the carrier is completely suppressed, resulting in gaps in the waveform.

---

## 3. Demodulating an ASK Signal using an Envelope Detector
In this stage, the ASK signal is demodulated using an **AM envelope detection method** consisting of a rectifier and a tunable low-pass filter.

### 3.1 Observation
The demodulated ASK signal is recovered from the modulated carrier by passing it through the envelope detector. The oscilloscope displays a recovered waveform with a peak-to-peak voltage of approximately **6.160 V**. The recovered signal resembles the original binary sequence but exhibits slight ripple and slanted edges due to the charging and discharging characteristics of the filter capacitor.

---

## 4. Restoring the Recovered Digital Signal using a Comparator
In the final part of the experiment, a comparator circuit is used to restore the recovered signal to a clean digital waveform.

### 4.1 Observation
The comparator processes the output of the envelope detector and converts the distorted waveform into a clean square wave that matches the original 
digital signal. The restored signal has a peak-to-peak voltage of approximately **5.20 V**, and the transitions between logic levels become sharp and well
defined. This confirms that the digital information has been successfully recovered.

---

# Questions and Answers

## Question 1
**What is the relationship between the digital signal and the presence of the carrier in the ASK signal?**
In ASK modulation, the digital signal controls whether the carrier is transmitted or not. When the digital signal is HIGH (logic 1), 
the carrier signal is present. When the digital signal is LOW (logic 0), the carrier is removed. This switching of the carrier amplitude represents the digital data.

## Question 2
**What is the ASK signal's voltage when the digital signal is logic 0?**
When the digital signal is logic 0, the ASK signal has approximately **0 volts** because the carrier signal is turned off. This means there is no carrier transmission during the logic 0 state.

## Question 3
**Why does the shape of the ASK signal suggest that it is an AM signal?**
The ASK signal resembles an AM signal because its amplitude changes according to the digital data. The carrier wave remains the same frequency but its amplitude is switched on and off by the
digital signal, similar to amplitude modulation.

## Question 4
**Why is the recovered digital signal not a perfect copy of the original?**
The recovered signal is not perfect because noise, filtering effects, and imperfections in the envelope detection process can distort the signal. The low-pass filter also smooths the signal 
which may slightly alter the waveform.

## Question 5
**What can be used to clean up the recovered digital signal?**
A **comparator** can be used to clean up the recovered digital signal. The comparator converts the distorted analog waveform into a clean digital signal by switching the output between HIGH
and LOW depending on the input voltage threshold.

---

# Conclusion

This experiment demonstrated the principle of Amplitude Shift Keying (ASK) used in digital communication systems. The digital signal controls the presence or absence of a carrier wave to
represent binary data. The ASK signal can be demodulated using envelope detection and then restored using a comparator to obtain a digital signal similar to the original message. The experiment 
also highlighted how noise and filtering can distort signals in communication systems.
