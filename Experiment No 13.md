# Experiment 13 – PCM Decoding

---

# INTRODUCTION

Pulse Code Modulation (PCM) is a digital technique used to convert analog signals into a stream of binary data for transmission. In digital communication systems, analog signals such as speech must first be encoded into digital form before they can be transmitted. The process of converting digital PCM data back into its original analog signal is known as **PCM decoding**.

PCM decoding involves interpreting the binary PCM data, converting it back into corresponding voltage levels, and reconstructing the original signal using filtering techniques. The PCM Decoder module uses the clock and frame synchronization signals from the encoder to correctly interpret the incoming digital data.

In this experiment, the Emona Telecoms-Trainer 101 PCM Encoder and PCM Decoder modules are used to demonstrate the complete process of PCM encoding and decoding. The experiment also shows how a low-pass filter is used to reconstruct the original analog signal from the decoded data.

---

# OBJECTIVES

In this experiment, we aim to:

- Understand the operation of the PCM Decoder module.
- Observe the PCM DATA and Frame Synchronization signals.
- Convert PCM digital data back into an analog signal.
- Compare the decoded signal with the original message signal.
- Understand the role of low-pass filtering in signal reconstruction.

---

# EQUIPMENT TO BE USED

- Emona Telecoms-Trainer 101 (plus power-pack)
- Dual Channel 20 MHz Oscilloscope
- Two Emona Telecoms-Trainer Oscilloscope leads
- Assorted Emona Telecoms-Trainer 101 patch leads
- One set of headphones (stereo)

---

# PROCEDURE

## Part A – Setting Up the PCM Encoder

1. Gather all the required equipment for the experiment.
2. Set up the oscilloscope according to the instructions.
3. Locate the PCM Encoder module and set the **Mode switch to PCM**.
4. Connect the circuit according to the diagram shown in the manual.
5. Set the oscilloscope’s **Scope control to the “+” position**.
6. Adjust the oscilloscope’s **Timebase control** to observe one pulse of the FS signal.
7. Set the Variable DC module control to approximately the middle of its range.
8. Set the oscilloscope mode to **DUAL** to observe both PCM DATA and FS signals.
9. Vary the Variable DC module and observe the changes in the PCM DATA output.

### Figure 1 
<img width="490" height="368" alt="image" src="https://github.com/user-attachments/assets/255603f4-dd7b-462b-a0e9-49950f94d046" />

### Figure 3 
<img width="459" height="344" alt="image" src="https://github.com/user-attachments/assets/fc4651d1-e55c-4222-a4ce-4ff05868b13e" />
---

## Part B – Decoding the PCM Data

1. Return the oscilloscope’s **Slope control to the positive position**.
2. Set the oscilloscope’s **Mode control to ALT**.
3. Modify the setup according to the PCM Decoder connection diagram.
4. Connect the PCM DATA output from the encoder to the PCM Decoder input.
5. Observe the PCM Decoder output waveform on the oscilloscope.

### Figure 5 
<img width="869" height="643" alt="image" src="https://github.com/user-attachments/assets/df0a64b4-ecbc-42b6-a895-bfccbea11c63" />

### Figure 6 
<img width="433" height="338" alt="image" src="https://github.com/user-attachments/assets/7974162d-0a23-4eed-879c-9c59c483feed" />
---

## Part C – Listening to the Decoded Signal

1. Turn the Buffer module’s **Gain control fully anti-clockwise**.
2. Connect the headphones to the Buffer module.
3. Gradually increase the gain until the decoded signal can be heard.
4. Compare the sound of the decoded signal with the original signal.

### Figure 9 
<img width="904" height="633" alt="image" src="https://github.com/user-attachments/assets/41d8b087-929f-4219-8b47-39ab4d62df33" />

---

## Part D – Reconstructing the Message Signal

1. Connect the Tunable Low-Pass Filter module to the PCM Decoder output.
2. Adjust the **cut-off frequency** of the filter.
3. Observe how the stepped waveform becomes smoother as the filter removes high-frequency components.
4. Listen to the reconstructed signal using headphones.

### Figure 10   
<img width="443" height="338" alt="image" src="https://github.com/user-attachments/assets/420dc5b0-e27c-41ac-ab17-7dc657afbbe6" />

---

# SUMMARY OF FINDINGS AND RESULTS

## 1. PCM Encoding of the Message Signal
In the first stage of the experiment, the PCM Encoder module samples the analog signal and converts it into a digital PCM data stream. The oscilloscope is used to observe the **Frame Synchronization (FS)** signal and the **PCM DATA** output.

### Observation
The PCM DATA output appears as a series of high-speed digital pulses. These pulses represent the binary codes assigned to the quantized voltage levels of the input signal.
The FS signal appears as a regular pulse indicating the start of each frame of digital data.

---

## 2. PCM Decoding of the Digital Signal
In the second part of the experiment, the PCM DATA output is connected to the PCM Decoder module. The decoder reconstructs the analog signal by converting each binary code back into a corresponding voltage level.

### Observation
The output of the PCM Decoder appears as a **stepped waveform**. Each step represents a quantized level corresponding to the encoded digital data.
Although the waveform resembles the original signal, it contains visible discontinuities due to quantization.

---

## 3. Listening to the PCM Decoder Output
The PCM Decoder output is connected to the Buffer module and headphones.

### Observation
The reconstructed sound is very similar to the original signal. However, slight distortion can be heard due to quantization error and the limited number of quantization levels.

---

## 4. Reconstruction Using a Low-Pass Filter
The decoded signal is passed through a Tunable Low-Pass Filter module.

### Observation
After filtering, the stepped waveform becomes smoother and more closely resembles the original analog signal. The filter removes high-frequency components introduced during the sampling process.

---
# QUESTIONS
Q: What does the PCM Decoder's "stepped" output tell you about the type of signal that it is? 
It indicates the signal is a Pulse Amplitude Modulation (PAM) signal. The "steps" show that the decoder is holding a specific voltage level for the duration of one frame before jumping to the next sampled value.

Q: What must be done to the PCM Decoder module's output to reconstruct the message properly? 
It must be passed through a Low-pass Filter. This filter removes the high-frequency transitions (the steps) and recovers the original smooth analog waveform.

Q: Even though the two signals look and sound the same, why isn't the reconstructed message a perfect copy of the original message? 
This is due to Quantization Error. Because an 8-bit system only has 256 discrete levels to represent an infinite range of analog voltages, there is a small rounding difference (quantization noise) between the original signal and its digital representation.
---

# CONCLUSION

After analyzing the gathered data and observations from the PCM decoding experiment, the following conclusions were made:

Pulse Code Modulation (PCM) decoding successfully reconstructs an analog signal from a digital PCM data stream by converting binary codes back into corresponding voltage levels. The PCM Decoder module relies on clock and frame synchronization signals to correctly interpret the incoming digital data.

The decoded signal initially appears as a stepped waveform due to quantization. This waveform approximates the original analog signal but contains small distortions caused by quantization error.

When the decoded signal is passed through a tunable low-pass filter, the waveform becomes smoother and more closely resembles the original message signal. The filtering process removes unwanted high-frequency components introduced during sampling.

Overall, the experiment demonstrates how PCM systems convert analog signals into digital form and how decoding and filtering processes allow the original signal to be reconstructed in modern digital communication systems.

