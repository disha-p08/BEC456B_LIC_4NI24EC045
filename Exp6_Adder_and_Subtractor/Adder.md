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

**AC Analysis:**

![ac](images/ac1.png)
