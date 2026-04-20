# Voltage Follower

A **voltage follower**, also known as a **unity gain buffer**, is a special configuration of an operational amplifier where the output is directly fed back to the inverting (–) terminal, and the input signal is applied to the non-inverting (+) terminal.

In this configuration, the amplifier provides **no voltage gain**, and the output voltage follows the input voltage exactly. Hence, it is called a voltage follower.

The circuit employs **100% negative feedback**, which forces the op-amp to operate in a stable linear region.

<img width="500" height="250" alt="image" src="https://github.com/user-attachments/assets/84acc863-193f-4365-8ebd-d5b9e80df86b" />

<br><br>

 Output Voltage Equation: **Vout = Vin**
 
---

 **Design OPAMP based circuit and analyze the frequency response**

Vcc = 15 V  
-Vcc = -15 V   
RL = 2.2K&ohm;  

**Circuit:**

![ckt](images/ckt2.png)  
<br>

**Input and Output Waveforms:**

![waveform](images/wave2.png)  
<br>

Here, Vin<sub>p-p</sub> = 5V
and Vout<sub>p-p</sub> = 5V  

- The output waveform is observed to be exactly **in phase** with the input waveform, confirming correct buffer operation.
- The amplitude of the output signal is equal to the input amplitude, indicating a gain of 1 (unity gain).
- This verifies the theoretical relation: **Vout = Vin**
- The output perfectly tracks the input signal with **no attenuation or amplification**, as expected from a voltage follower.
- The waveform shape is preserved without distortion, indicating that the op-amp is operating in its **linear region**.

**Frequency Response:**

![ac](images/ac2.png)  

Simulated gain = 0dB = 1 V/V  
Bandwidth = 1.371 MHz
GBP = 1.371 MHz  

- The frequency response shows a **flat gain of 0 dB** (unity gain) over a wide range of low frequencies, confirming ideal buffer behavior.
- Unlike amplifiers, there is **no gain increase**, and the magnitude remains constant at **1 V/V**.
- Since the gain is unity, the voltage follower achieves the **maximum possible bandwidth** compared to other closed-loop configurations.
- The observed bandwidth of the voltage follower is approximately equal to the op-amp’s gain-bandwidth product (~1 MHz).

**Inference:**

- The voltage follower produces an output **equal in amplitude and phase** to the input, confirming **unity gain operation**.
- It acts as an effective **buffer**, providing high input impedance, low output impedance, and stable frequency response.
- The voltage follower maintains **signal integrity at low frequencies** while providing high bandwidth and impedance isolation, making it ideal as a buffer stage.
- At higher frequencies, deviation from unity gain highlights the **practical limitations of real op-amps**.
