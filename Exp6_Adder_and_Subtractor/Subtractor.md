# Subtractor

A **subtractor**, also known as a **difference amplifier**, is an operational amplifier configuration used to obtain the **difference between two input voltages**. It produces an output proportional to the difference of the applied signals.

In this circuit, one input is applied to the **inverting (–) terminal** and the other to the **non-inverting (+) terminal** through appropriate resistor networks. The circuit uses **negative feedback**, ensuring stable and linear operation.

The subtractor is widely used in applications where it is required to **eliminate common signals (noise)** and extract the difference between two signals.

<img width="381" height="273" alt="image" src="https://github.com/user-attachments/assets/1b8fed34-9c64-4db8-9d58-9d233fc1dbd1" />
<br><br>
The Gain of the amplifier is, 
<br>​
<img width="648" height="65" alt="image" src="https://github.com/user-attachments/assets/caa05862-eb02-42bb-b0b0-e54a29343cfe" />

where,

<img width="525" height="215" alt="image" src="https://github.com/user-attachments/assets/110d8e12-7e5e-414e-b3f0-d525f23221be" />

<br>

---

**Design the circuit using OPAMP to get the output as given:**

**y<sub>3</sub>(t) = 2x<sub>1</sub>(t) - 6x<sub>2</sub>(t)**

Given:  
x<sub>1</sub>(t) = 0.5 sin(3000&pi;t) V  
x<sub>2</sub>(t) = -1.5V  
Vcc = 12 V  
-Vcc = -12 V   

**Design:**

y<sub>3</sub>(t) = 2x<sub>1</sub>(t) - 6x<sub>2</sub>(t)] is of the form   
<img width="648" height="65" alt="image" src="https://github.com/user-attachments/assets/caa05862-eb02-42bb-b0b0-e54a29343cfe" />


According to the question,  
For V2,  
(-Rf/R2) = -6  
Rf = 6R2

Assuming **R1 = 1K&ohm;,**    
**Rf = 6*1K&ohm; = 6K&ohm;**  

For V1,  
(1+(Rf/R1))(Rb/(Ra+Rb)) = 2  
(1+(6K/1K))(Rb/(Ra+Rb)) = 2  
7(Rb/(Ra+Rb)) = 2  
Rb/(Ra+Rb) = 2/7  
7Rb = 2Ra + 2Rb  
Rb/Ra = 2/5 = 0.4  

Hence, let **Ra = 5K&ohm;  
then Rb = 2K&ohm;**    
<br><br>
**Circuit:**

![circuit](images/ckt2.png)
<br><br>
**Input and Output Waveforms:**

![waveform](images/wave2.png)
<br><br>
![waveform](images/wave22.png)

- 

**AC Analysis:**

![ac](images/ac2.png)

Simulated gain =   
Theoretical gain =   
Bandwidth =   
GBP = 

- 


**Inference:**

- 
