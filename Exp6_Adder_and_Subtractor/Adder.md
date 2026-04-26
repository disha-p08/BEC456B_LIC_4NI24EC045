# Inverting Summing Amplifier

An **inverting summing amplifier** is an op-amp configuration used to **add multiple input voltages** and produce a single output that is proportional to their **weighted sum with inversion**.

In this circuit, all input signals are applied to the **inverting (–) terminal** through individual resistors, while the non-inverting (+) terminal is connected to ground. The circuit operates using negative feedback, ensuring accurate and stable summation.

The output voltage is an inverted combination of all input voltages.

<img width="800" height="320" alt="image" src="https://github.com/user-attachments/assets/9e8d6c99-2eab-49ad-97fd-9a772a2b376d" />
<br><br>
The Gain of the amplifier is, 
<br>​
<img width="286" height="60" alt="image" src="https://github.com/user-attachments/assets/6a3fe96a-9a2d-47f6-af6f-7afe4e4cb725" />

<br>
where, Rf is the feedback resistor

and V1,V2....Vn are input voltages.

---

**Design the circuit using OPAMP to get the output as given:**

**y<sub>1</sub>(t) = -[5x<sub>1</sub>(t) + x<sub>2</sub>(t)]**

Given:  
x<sub>1</sub>(t) = 0.5 sin(3000&pi;t) V  
x<sub>2</sub>(t) = -1.5V  
Vcc = 12 V  
-Vcc = -12 V   

**Design:**

y<sub>1</sub>(t) = -[5x<sub>1</sub>(t) + x<sub>2</sub>(t)] is of the form   
<img width="216" height="51" alt="image" src="https://github.com/user-attachments/assets/169abd36-5f20-416a-aec5-7b6232492ca1" />

Here,  
<img width="147" height="56" alt="image" src="https://github.com/user-attachments/assets/4b72436c-f46f-420a-bca5-513589b95e62" />

According to the question,  
For V1,  
(-Rf/R1) = -5  
Rf = 5*R1

Assuming **R1 = 1K&ohm;,**    
**Rf = 5*1K&ohm; = 5K&ohm;**

Similarly,
For V2,  
(-Rf/R2) = -1  
Rf = R2

Since Rf = 5K&ohm;,  
**R2 = 5K&ohm;**  
<br><br>
**Circuit:**

![circuit](images/ckt1.png)
<br><br>
**Input and Output Waveforms:**

![waveform](images/wave1.png)
<br><br>
![waveform](images/wave11.png)

- The output waveform is observed to be the **algebraic sum of all input signals**, confirming correct summing operation of the circuit.
- The output is **inverted (180° phase shift)** with respect to the input signals, as expected for an inverting summing amplifier .
- The amplitude of the output corresponds to the weighted sum of individual inputs, depending on the resistor ratios (Rf/R1),(Rf/R2)...etc.
- When multiple sinusoidal inputs are applied, the output waveform represents a combined waveform, clearly showing superposition of signals.
- No distortion is observed, indicating that the op-amp is operating in the linear region with proper biasing.
- The waveform confirms the relation: **Vout = −(V1+V2+⋯)**  (for equal resistors)

**AC Analysis:**

![ac](images/ac1.png)

Simulated gain = 13.9786 dB = 4.999V/V  
Theoretical gain = 5*1 = 5V/V  
Bandwidth = 149.688KHz  
GBP = 748.44KHz  

- The AC analysis shows a midband gain of approximately **13.9786 dB**, which corresponds to about **4.999 V/V**, closely matching the theoretical gain of **5 V/V**.
- This confirms that the circuit accurately implements the expected summation gain based on resistor ratios.
- The gain remains constant (~14 dB) over the low-frequency region, indicating stable operation of the amplifier in the midband.
- The −3 dB cutoff frequency is observed at approximately **149.688 kHz**, which defines the effective bandwidth of the circuit.
- The AC analysis validates both the designed gain accuracy and the gain-bandwidth limitation, confirming proper operation of the inverting summing amplifier in practical conditions.


**Inference:**

- The experiment demonstrates that an op-amp can be effectively used to perform analog computation, specifically the addition of multiple input signals using the principle of superposition.
- The close agreement between theoretical and simulated gain indicates that the circuit behavior is primarily governed by **external resistor ratios**, making it predictable and design-friendly.
- The presence of phase inversion highlights the fundamental characteristic of the **inverting configuration**, which must be considered in practical applications.
- The finite bandwidth obtained from AC analysis reflects the **non-ideal nature of practical op-amps**, emphasizing that accurate summation is limited to a specific frequency range.
- The results reinforce the importance of the gain-bandwidth trade-off, showing that increasing gain reduces the usable frequency range of the circuit.
- Overall, the inverting summing amplifier is validated as a reliable building block for signal processing applications, where multiple inputs need to be combined with controlled weighting.
