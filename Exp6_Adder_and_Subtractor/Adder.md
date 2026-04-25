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

