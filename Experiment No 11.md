# Sampling and Reconstruction of Analog Signals
### Experiment 11 – Emona Telecoms Trainer 101

---

# I. Introduction

In modern telecommunications, digital transmission has largely replaced analog communication systems because of its superior resistance to electrical noise and interference. However, most real-world signals such as speech, music, and other natural signals exist in analog form. To transmit these signals in digital communication systems, they must first be converted into discrete samples through a process known as sampling.

Sampling involves measuring the amplitude of a continuous-time signal at uniform time intervals. According to the Nyquist Sampling Theorem, the sampling frequency must be at least twice the highest frequency component of the signal in order to accurately reconstruct the original signal. If the sampling frequency is too low, aliasing may occur, resulting in distortion of the reconstructed signal.

The reconstruction of a sampled signal is typically achieved by passing the sampled waveform through a low-pass filter. This filter removes the higher frequency components introduced during the sampling process, allowing the original message signal to be recovered.

This experiment demonstrates the process of sampling a simple sinusoidal message signal and a speech signal using the Emona Telecoms-Trainer 101. It also investigates how the original signal can be reconstructed and how aliasing affects signal quality when the sampling frequency becomes insufficient.

---

# II. Objectives

The objectives of this experiment are:

- Demonstrate sampling of an analog message signal
- Observe sampled signals using an oscilloscope
- Reconstruct the signal using a tunable low-pass filter
- Examine aliasing when sampling frequency is reduced

---

# III. Materials and Equipment

1. Emona Telecoms-Trainer 101 (plus power pack)
2. Dual Channel 20 MHz Oscilloscope
3. Two Oscilloscope Leads
4. Assorted Patch Leads
5. Stereo Headphones

---

# IV. Methodology

## A. Sampling a Simple Message Signal

A 2 kHz sine wave from the master signals module was used as the message signal. The signal was connected to the dual analog switch module which was controlled by an 8 kHz digital sampling signal.

The oscilloscope displayed both the original message signal and the sampled signal for observation.


<img width="490" height="323" alt="image" src="https://github.com/user-attachments/assets/d4ee9ed7-3b27-4696-8a25-44f6f5ef8c4e" />

### OUTPUT
<img width="490" height="373" alt="image" src="https://github.com/user-attachments/assets/2f632d58-a505-4854-9409-c4481d36b281" />

---

## B. Sampling Speech

The sinusoidal signal was replaced with the speech module output to simulate a real voice signal. Students spoke into the microphone while observing waveform changes on the oscilloscope.

<img width="490" height="383" alt="image" src="https://github.com/user-attachments/assets/9e385938-4c09-4149-9f3e-ee762210811d" />

### Figure: Sample-&-Hold Scheme Sampling Block Diagram

### OUTPUT 
<img width="490" height="372" alt="image" src="https://github.com/user-attachments/assets/d29decb9-5843-435d-9ac0-548f1dcd8b2b" />

---

## C. Signal Reconstruction

The sampled signal was passed through a tunable low-pass filter to recover the original waveform.
The cutoff frequency and gain of the filter were adjusted until the reconstructed waveform resembled the original signal. 
### Figure: Reconstructing a Sampled Message Block Diagram

<img width="490" height="357" alt="image" src="https://github.com/user-attachments/assets/d588855b-49e4-4ff0-bd3e-5ee36572c546" />

### PART C STEP 15 OUTPUT

https://github.com/user-attachments/assets/8b8d8c9c-7f73-4250-a618-d9b561cef26
---

## D. Aliasing Investigation

The sampling frequency was gradually reduced using the VCO module. As the sampling frequency approached the Nyquist limit, distortion began to appear in the reconstructed waveform.

<img width="490" height="354" alt="image" src="https://github.com/user-attachments/assets/0c04fbf1-b3ef-4751-b7bd-4be0a2f5268f" />
#### Figure: Aliasing Block diagram

### OUTPUT
<img width="490" height="364" alt="image" src="https://github.com/user-attachments/assets/9f0c9f7c-d5d1-431b-b44e-fad6bd94add4" />

![PART D - Page 13](https://github.com/user-attachments/assets/254c4f1e-25ac-4b3e-933e-9232237c5bab)

---

# V. Results and Observations

### Sampling of a Simple Message

The sampled waveform consisted of pulses occurring at the sampling frequency of 8 kHz. The pulse amplitudes followed the shape of the original sinusoidal signal.

However, the sampled signal appeared more distorted compared to the original waveform.

---

### Sampling of Speech

When the speech module was used as the message signal, the sampled waveform changed depending on the voice amplitude and tone.

Stronger voice signals produced larger pulse amplitudes in the sampled waveform.

---

### Signal Reconstruction

When the sampled signal was passed through the tunable low-pass filter, the original waveform was gradually reconstructed.

Initially the signal appeared flat. Increasing the cutoff frequency allowed the original waveform to appear.

---

### Aliasing Effect

When the sampling frequency was reduced below the Nyquist rate, distortion appeared in the reconstructed signal. This distortion is known as **aliasing**.

---
# VI. QUESTIONS
Q1: What type of sampling is shown in the first part of the experiment? and What two features of the sampled signal confirm this?

The output shown was a Natural Sampling. This was a Natural Sampling because the sample voltages was affected during the sampling and the signal's voltage returns to zero volts between the samples.

Q2: What two features of the sampled signal confirm that the set-up models the sample-and-hold scheme?

The first feauture that shows that the sampled signal upholds a sample-and-hold scheme is there are no spaces found in between the samples. Then, the sample voltages doesn't change during the sampling process.

Q3: What’s the name of the distortion that appears when the VCO module’s Frequency Adjust control is turned far enough?

Aliasing

Q4: Given the message is a 2kHz sinewave, what’s the theoretical minimum frequency for the sampling signal?

4kHz (2 × 2kHz)

Q5: Why is the actual minimum sampling frequency higher than the theoretical minimum that you calculated for Question 4?

The actual minimum sampling frequency higher than the theoretical minimum calculated because the filters are not that accurate and their cut off are not instantenous.

---
# VII. Conclusion

The experiment demonstrated the process of sampling and reconstructing analog signals using the Emona Telecoms-Trainer 101.
A 2 kHz message signal was successfully sampled using an 8 kHz sampling signal and later reconstructed using a low-pass filter. The experiment verified the Nyquist Sampling Theorem and showed that aliasing occurs when the sampling frequency is too low.
Overall, the experiment provided practical understanding of how analog signals are converted into digital form and reconstructed in modern communication systems.

