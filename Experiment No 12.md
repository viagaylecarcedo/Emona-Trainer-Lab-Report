# Experiment 12 – PCM Encoding
---
# I. Introduction

Modern communication systems rely heavily on digital transmission methods due to their improved noise immunity, signal integrity, and efficient processing capabilities. However, most real-world signals such as speech and music exist in analog form. To transmit these signals digitally, they must first be converted into digital data.
Pulse Code Modulation (PCM) is one of the most widely used techniques for analog-to-digital conversion. PCM converts an analog signal into a digital bitstream through three primary steps: sampling, quantization, and encoding. In the sampling stage, the analog signal is measured at regular intervals. In the quantization stage, the sampled values are approximated to the nearest discrete voltage level. Finally, the quantized values are encoded into binary numbers.
In this experiment, the PCM Encoder module of the Emona Telecoms-Trainer 101 is used to demonstrate PCM encoding using both static and variable DC voltages. Observations are made using an oscilloscope to understand how analog input signals are converted into digital PCM codes.

---

# II. Objectives

The objectives of this experiment are:

- To understand the working principle of Pulse Code Modulation.
- To observe the PCM encoding process using a laboratory setup.
- To investigate how changes in input voltage affect the PCM encoder output.
- To analyze quantization levels and quantization error in PCM systems.

---

# III. Materials and Equipment

The following equipment were used in the experiment:

1. Emona Telecoms-Trainer 101 (plus power-pack)
2. Dual channel 20 MHz oscilloscope
3. Oscilloscope leads
4. Patch leads
5. Variable DC voltage module
6. PCM Encoder module
7. Master signals module

---

# IV. Theory

Pulse Code Modulation (PCM) is a digital representation of analog signals. It involves three main processes:

### 1. Sampling
Sampling measures the amplitude of an analog signal at regular intervals. The sampling frequency must satisfy the Nyquist criterion to prevent aliasing.

### 2. Quantization
Quantization approximates the sampled signal values to the nearest discrete voltage levels. The number of quantization levels determines the resolution of the digital representation.

### 3. Encoding
Each quantized level is assigned a binary code, which is transmitted as a digital signal.

The PCM encoder in the Emona trainer converts the input voltage into an 8-bit digital code.

---

# V. Methodology

## A. PCM Encoding Using Static DC Voltage

The initial setup involves connecting the PCM encoder module with the master signals module and oscilloscope. The input voltage of the encoder is set to 0 V using the master signals module.
The oscilloscope is used to observe the PCM data output and frame synchronization signal.
1. Gather a set of the equipment listed above.
2. Set up the scope per the instructions in Experiment 1. Ensure that the Trigger Source is set to CH1 and Mode is set to CH1.
3. Locate the PCM Encoder module and set its Mode switch to the PCM position.
4. Connect the set-up where the PCM Encoder module is clocked by the Master Signals module’s 8kHz DIGITAL output and its analog input is connected to 0V DC.
5. Adjust the scope's Timebase control to view three pulses of the PCM Encoder module's FS output.
6. Set the scope's Slope control to the "-" position to start the sweep when the FS signal goes from high to low.
7. Adjust the scope’s Horizontal Position control so that the start of the trace aligns with the left-most vertical line on the screen.
8. Set the scope's Timebase control to the 0.1ms/div position.
9. Adjust the scope's Variable Sweep control until the FS signal matches the required reference.
10. Set the scope's Mode control to the DUAL position to view the PCM Encoder module’s CLK input as well as its FS output.
11. Draw the two waveforms to scale, leaving enough room for a third digital signal.
12. Connect the scope's Channel 2 input to the PCM Encoder module's output.
13. Draw the resulting waveform (10 bits of data) to scale on the graph paper.

### PART A: An introduction to PCM encoding using a static DC Voltage

<img width="412" height="374" alt="image" src="https://github.com/user-attachments/assets/264faa7a-c8cc-40c0-894d-d33f857f9e16" />

### OUTPUT
<img width="490" height="368" alt="image" src="https://github.com/user-attachments/assets/769e822e-4555-4b61-97c6-a1e99b7d8a1c" />
---

## B. Observing PCM Output Waveform

The oscilloscope timebase and triggering controls are adjusted to properly display the PCM data bits. The binary output waveform of the encoder is drawn and analyzed.
1. Set the scope's Mode control to the CH1 position.
2. Set the scope's Trigger Source control to the EXT position.
3. Set the scope's Trigger Source Coupling control to the HF REJ position.
4. Modify the set-up to include the Variable DCV module to change the DC voltage on the PCM Encoder module's input.
5. Set the scope's Channel 1 Vertical Attenuation control to the 1V/div position.
6. Set the scope's Channel 1 Input Coupling control to the GND position.
7. Use the scope's Channel 1 Vertical Position control to align the trace with a horizontal line (zero volt reference).
8. Set the scope's Channel 1 and Channel 2 Input Coupling controls to the DC position.
9. Set the scope's Mode control to the DUAL position.
10. Adjust the Variable DCV module's Variable DC control until the PCM Encoder module outputs the 0V code.
11. Measure the Variable DCV module's output voltage (should be close to 0V).
12. Turn the Variable DCV module's Variable DC control clockwise.
13. Continue turning clockwise until the PCM Encoder module's output is 11111111.
14. Record the input voltage in Table 1.
15. Devise a method (using a Buffer or Adder) to reach the upper and lower limits of the input range if necessary.
16. Adjust the setup for a small negative input voltage.
17. Increase the negative voltage and observe the binary number output.
18. Continue until the output is 00000000.
19. Measure and record this value in Table 1.

<img width="490" height="367" alt="image" src="https://github.com/user-attachments/assets/38fac9b9-0c9d-4bd7-9429-784338747074" />
---

## C. Quantisation

The variable DC voltage module is connected to the PCM encoder input. The voltage is gradually increased while observing changes in the PCM output code.
The output binary code changes depending on the amplitude of the input voltage.

1. Return to the basic variable DC setup and set the control to the middle of its travel.
2. Vary the control left and right slightly to observe that the output code remains unchanged until a quantisation threshold is crossed.

### D. PCM encoding of continuously changing voltages

1. Return the scope's Trigger Source control to CH1 and Trigger Source Coupling to AC.
2. Set the scope's Vertical Attenuation for both channels to 2V/div.
3. Locate the VCO module and set its Range control to the HI position.
4. Turn the VCO module's Frequency Adjust control fully anti-clockwise (for approx. 50kHz clock).
5. Disassemble the current set-up.
6. Connect the setup where the VCO clocks the PCM Encoder and a sinewave is applied to the input.
7. Set the scope's Timebase control to the 50µs/div position.
---

# VI. Results and Observations

### Static Input Voltage

When the input voltage was set to 0 V, the PCM encoder produced a fixed binary output corresponding to the quantization level closest to zero.

### Binary Output Behavior

The PCM encoder output is transmitted as an 8-bit digital code in serial form. The frame synchronization signal indicates the beginning of each frame.

### Effect of Changing Input Voltage

When the input voltage was increased gradually, the binary output code also increased. This behavior demonstrates the quantization process of the PCM encoder.

---
# VI. Results and Observations
**Question 1:** Indicate on your drawing the start and end of the frame. 
The frame starts at the beginning of Bit-7 (MSB) and ends after Bit-0 (LSB).

**Question 2:** Indicate on your drawing the start and end of each bit. 
Each bit period is defined by one period of the 8kHz clock signal.

**Question 3:** Indicate on your drawing which bit is bit-0 and which is bit-7. 
Bit-7 is transmitted first; Bit-0 is transmitted last and coincides with the FS signal.

**Question 4:** What is the binary number that the PCM Encoder module is outputting at 0V? 
Typically 10000000, representing the midpoint of the bipolar range.

**Question 5:** Why does the code change even though the input voltage is steady? 
This is caused by analog noise; if the voltage is at a quantisation threshold, noise makes the bit toggle.

**Question 6:** Why does the PCM Encoder module output this code for 0V DC and not 00000000? 
Because the system is bipolar; 00000000 is for the most negative voltage, and 0V is the center.

**Question 7:** What happens to the Variable DCV module's output? 
The DC voltage level increases.

**Question 8:** In what way does the binary number change? 
The binary value increases as the input voltage becomes more positive.

**Question 9:** Explain why you were unable to obtain 11111111. 
The Variable DCV's max output may be lower than the encoder's required reference for that code.

**Question 10:** Devise a method of obtaining a variable DC voltage that can reach the limits. 

Use an Adder module to add a DC offset or a Buffer with gain to boost the signal.

**Question 11:** What happens to the binary number as the size of the negative input voltage increases? 
The binary number decreases toward 00000000.

**Question 12:** What is the maximum allowable amplitude (peak-to-peak) for an AC signal? 
Approximately 4Vpp (the difference between the max and min recorded voltages).

**Question 13:** What's the name for the difference between a sampled voltage and its closest quantisation level? 
Quantisation Error.

**Question 14:** Calculate the difference between the quantisation levels. 
Step Size (Δ) = (Vmax − Vmin)/256.

**Question 15:** To reduce quantisation error it's better to have: 
more quantisation levels between ±2.5V.

Question 16: Why does the PCM DATA change continuously? 
Because the analog input (sinewave) is constantly changing, each sample taken results in a different binary code.
---

# VII. Discussion

The PCM encoder converts analog voltages into digital codes using discrete quantization levels. The number of levels determines the accuracy of the representation.
In this experiment, the PCM encoder uses an 8-bit resolution, which allows for 256 possible quantization levels.
Quantization error occurs when the sampled voltage falls between two quantization levels. This error is the difference between the actual signal value and the nearest quantized value.
Increasing the number of quantization levels reduces the quantization error and improves signal quality.

---

# VIII. Conclusion

The experiment successfully demonstrated the process of Pulse Code Modulation using the Emona Telecoms-Trainer 101. The PCM encoder was able to convert analog input voltages into binary digital codes that were observed on the oscilloscope.
The results showed that changes in input voltage correspond directly to changes in the binary output code. Additionally, the experiment highlighted the role of quantization levels and quantization error in digital signal representation.
Overall, the experiment provided practical insight into the analog-to-digital conversion process used in modern digital communication systems.
