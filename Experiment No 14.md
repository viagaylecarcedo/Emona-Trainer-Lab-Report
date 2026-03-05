# Experiment 14 – Bandwidth Limiting and Restoring Digital Signals
---
# Objectives
The objectives of this experiment are:

- To observe the effect of bandwidth limiting on a PCM communication system.
- To model a communication channel using a low-pass filter.
- To examine the effect of bandwidth limiting on digital signal shape.
- To investigate the effect of increasing bit-rate.
- To restore a bandwidth-limited digital signal using a comparator and observe its limitations.
---

# Materials and Components Used

Emona Telecoms-Trainer 101 (plus power-pack) 
Oscilloscope Dual-channel 20 MHz oscilloscope 
Variable DCV, PCM Encoder, PCM Decoder, Tuneable Low-pass Filter, Sequence Generator, VCO, Utilities (Comparator) 
Three oscilloscope leads, assorted patch leads, stereo headphones 

---

# Preliminary Discussion

In the classical communications model, intelligence (the message) moves from a transmitter to a receiver over a channel. A number of transmission media can be used for the channel including metal conductors such as twisted-pair or coaxial cable, optical fibre, and free space (commonly referred to as the airwaves).

Regardless of the medium used, all communication channels have a bandwidth. This means that the medium allows a certain range of signal frequencies to pass with little or no attenuation, while frequencies outside this range are reduced in amplitude. Because of this behavior, the communication channel effectively acts as a filter.

This characteristic has important implications for communication systems. In analog modulation schemes such as amplitude modulation (AM), the transmitted signal is composed of many sinusoidal components. If the channel bandwidth is not wide enough, some of these frequency components will be attenuated or lost. As a result, the demodulated signal, which represents the recovered message, becomes distorted.

Similarly, digital signals are also composed of multiple sinusoidal components, including a fundamental frequency and several harmonics. When the channel bandwidth is insufficient, some of these components are attenuated or removed, which alters the overall shape of the signal.

To illustrate this concept, if all but the first two sinewave components of a square wave are removed, the resulting waveform becomes distorted. This demonstrates how limiting the bandwidth of the channel affects the signal shape.

Additionally, communication channels can introduce phase shifts to different frequency components. Because each frequency component may be shifted by a different amount, the combined waveform can become further distorted.

This creates a significant challenge for digital receivers such as PCM decoders. If the signal becomes too distorted, the receiver may misinterpret the logic levels, causing some digital codes to be incorrectly detected. These errors result in incorrect voltages at the decoder output, making the recovered message noisy and unreliable.
---

# PROCEDURE

## Part A – The Effects of Bandwidth Limiting on PCM Decoding

1. Gather all the equipment listed in the experiment manual.
2. Set up the oscilloscope according to the instructions from the previous experiment.
3. Set the oscilloscope **Mode control** to the **DUAL** position.
4. Set the oscilloscope **Channel 1 and Channel 2 Input Coupling controls** to the **DC position**.
5. Set the oscilloscope **Channel 1 and Channel 2 Vertical Attenuation controls** to the **1V/div position**.
6. Locate the **Variable DCV module** and set its **VDC control** to about the middle of its range.
7. Locate the **PCM Encoder module** and set its **Mode switch to the PCM position**.
8. Connect the circuit according to the diagram provided in the manual.
9. Vary the **Variable DCV module’s VDC control** left and right and observe the output signals.

### Figure 3 
<img width="1293" height="935" alt="image" src="https://github.com/user-attachments/assets/cc283759-2361-4b45-8c3e-4597a06e1913" />

### Figure 4
<img width="490" height="270" alt="image" src="https://github.com/user-attachments/assets/f10aeef1-b941-411a-9ba6-a4ab6fb95777" />

### OUTPUT
<img width="490" height="364" alt="image" src="https://github.com/user-attachments/assets/7ee3e055-13da-4fde-a39b-635b4168a869" />

---

## Part B – The Effects of Bandwidth Limiting on a Digital Signal’s Shape

10. Locate the **Tunable Low-Pass Filter module** and set its **Gain control** to the middle position.
11. Turn the **Cut-off Frequency Adjust control fully clockwise**.
12. Modify the circuit setup according to the diagram in the experiment manual.
13. Adjust the **VCO module’s frequency** and observe the digital signal on the oscilloscope.
14. Slowly turn the **Low-Pass Filter Cut-off Frequency control** and observe the waveform distortion.

<img width="396" height="306" alt="image" src="https://github.com/user-attachments/assets/b5857820-4e22-45fc-9680-2078826ef8ae" />

---

## Part C – Restoring Digital Signals

15. Disconnect the patch lead from the **VCO module’s Digital Output**.
16. Set the oscilloscope **Timebase control to 0.5 ms/div**.
17. Set the **Variable DCV control** to the middle position.
18. Modify the circuit setup according to the restoration diagram.
19. Slowly adjust the **Low-Pass Filter Cut-off Frequency control** until the signal resembles the original digital waveform.
20. Compare the restored digital signal with the bandwidth-limited signal.

<img width="471" height="357" alt="image" src="https://github.com/user-attachments/assets/9349ea88-ee61-42aa-92bf-a2ab5f41ac29" />

---

# RESULTS / OBSERVATIONS

## Bandwidth Limiting

When the digital signal passes through the **tunable low-pass filter**, the higher frequency components are reduced. Because digital signals require sharp transitions between logic levels, removing these components causes the waveform edges to become rounded.

## Signal Distortion

As the filter bandwidth becomes narrower, the digital waveform becomes more distorted. The pulses lose their sharp edges and begin to overlap with adjacent bits. This distortion can cause errors in digital communication systems.

## Signal Restoration

Using a **comparator circuit**, the distorted signal can be converted back into a clean digital waveform. The comparator compares the incoming signal with a reference voltage and regenerates the correct HIGH and LOW logic levels.

---

# QUESTIONS TO BE ANSWERED

## Question 1
How can bandwidth limiting of the channel cause the PCM Decoder module to output incorrect voltages as well as the correct ones?
Bandwidth limiting removes high-frequency components of the digital signal. These components are required for sharp transitions between logic levels. When they are removed, the waveform becomes distorted and the PCM decoder may misinterpret the signal, producing incorrect voltages.

---
## Question 2
If this were a communications system transmitting speech, what would these errors sound like when the message is reconstructed?
The reconstructed speech would contain noise, distortion, or clicking sounds. Errors in the digital signal result in incorrect audio samples, which degrade the recovered speech signal.

---

## Question 3
What two things are happening to cause the digital signal to change shape?
1. Attenuation of high-frequency components caused by bandwidth limitation.
2. Phase distortion where different frequency components are delayed differently.
Both effects distort the digital waveform.

---
## Question 4
What change to your communications system distorts the digital signal in the same way as increasing its bit rate?
Reducing the **channel bandwidth** produces the same effect as increasing the bit rate. Both conditions require higher frequency components for proper signal transmission.

---
## Question 5
Are the restored digital signals almost identical to the original digital signal?
Yes. The comparator regenerates the digital waveform, producing clear HIGH and LOW levels that closely resemble the original signal.
---
## Question 6
Can this difference be ignored? Why?
Yes. Digital communication systems only depend on logic levels. Small differences in waveform shape do not affect the interpretation of digital data as long as the signal crosses the correct threshold.
---

## Question 7
Why do some DC voltages cause the comparator to output the wrong information?
If the DC reference voltage is not set correctly, the comparator threshold may fall within the distorted signal range. This can cause incorrect logic interpretation and result in wrong output data.

---
# Conclusion

The experiment demonstrated the effects of bandwidth limitation on digital signals. When a digital signal passes through a bandwidth-limited channel, high-frequency components are attenuated, causing distortion in the waveform.
The distorted signal can lead to errors in digital communication systems. However, by using comparator circuits, the signal can be regenerated and restored to a clean digital waveform.
This experiment highlights the importance of sufficient bandwidth in communication systems and shows how signal restoration techniques are used to recover distorted digital signals.
