__DIFFERENTIAL AMPLIFIER__
---
A Differential Amplifier is an electronic circuit that __amplifies the difference between two input signals while rejecting any signal common to both inputs__. It is widely used in analog circuits such as operational amplifiers because of its high noise immunity and precision. The basic circuit typically consists of two matched transistors sharing a common emitter/source connection, with one input applied to each transistor. When the input voltages differ, the amplifier produces an output proportional to their voltage difference. Its key characteristics include high common-mode rejection ratio (CMRR), good stability, and linear amplification, making it essential in signal conditioning and instrumentation applications.

__Differential Input Voltage: vid = vin1 - vin2__

<img width="495" height="427" alt="image" src="https://github.com/user-attachments/assets/b6433ecb-fc1d-4c46-a05c-27379a1fe2cb" />

---


__Design and analyze the MOS Differential Amplifier circuit for the following specifications__

VDD = 0.9V; 
VSS = -0.9V; 
P <= 1.5W; 
Vincm = 0V; 
Vocm = 0V; 
Vp = -0.7V

__CIRCUIT - 1:__

![CIRCUIT](images/ckt1.png)

Power, P = 1.5mW 

P = VDD * ID

1.5m = 1.8 * ID

__ID = ISS = 0.833mA__

Since the 2 branches are identical, current through M1, __ID1__ = current through M2, __ID2__ = __ISS/2 = 0.4165mA__

Applying KVL, Vo = VDD - IDRD

RD = (VDD - Vo)/ID

__RD = 2.16Kohm__

For NMOS M1 and M2, VG1 = VG2 = Vincm = 0V

VGS1 = VG1 - VS1 = 0 - (-0.7) = 0.7V

VOV1 = VGS1 - VT = 0.7 - 0.36 = 0.34V 

Width of M1 and M2 is given by current equation , 
