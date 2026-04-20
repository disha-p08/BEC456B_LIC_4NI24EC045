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

**Frequency Response:**

![ac](images/ac2.png)  

Simulated gain = 0dB  
Hence, GBP = 0Hz
