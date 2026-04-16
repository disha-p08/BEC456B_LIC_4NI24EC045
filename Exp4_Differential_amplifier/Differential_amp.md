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
Voutcm = 0V; 
Vp = -0.7V;
L = 360nm

__CIRCUIT - 1:__

![CIRCUIT](images/ckt1.png)

- __DC ANALYSIS:__

Power, P = 1.5mW  
P = VDD * ID  
1.5m = 1.8 * ID  
__ID = ISS = 0.833mA__

Since the 2 branches are identical, current through M1, __ID1__ = current through M2, __ID2__ = __ISS/2 = 0.4165mA__

Applying KVL,   
Vout = VDD - IDRD  
RD = (VDD - Vo)/ID  
__RD = 2.16Kohm__

For NMOS M1 and M2,  
VG1 = VG2 = Vincm = 0V  
VGS1 = VG1 - VS1 = 0 - (-0.7) = 0.7V  
VOV1 = VGS1 - VT = 0.7 - 0.36 = 0.34V  
VDS1 = VD - VS = 0 - (-0.7) = 0.7V  

Since, VGS1 >= VT  --> 0.7V > 0.36V  
and, VDS1 >= VGS1 - VT --> 0.7V >= 0.34V  
Both __M1 and M2 are in SATURATION__

Width of M1 and M2 is given by current equation ,  
![Current_eqn](images/id.png)  
Substituting the values of ID1, L, VOV and k' we get, __W = 11.259&mu;m__  

![dcopnt](images/dc1.png)  

The DC operating point is set.

- __TRANSIENT ANALYSIS:__

Input swing,  
Vincm<sub>min</sub> = VGS1 + VS = 0.7 + (-0.7) = 0V  
Vincm<sub>max</sub> = Vout + VT = 0 + 0.36 = 0.36V  

Output swing,  
Voutcm<sub>min</sub> = VDD - IDRD = -0.9V  
Voutcm<sub>max</sub> = VDD = 0.9V  

![wave](images/waveform1.png)

The simulated output waveforms Vout1 and Vout2 remain within the calculated output swing range, confirming that the differential amplifier operates within permissible limits without clipping or distortion. This indicates proper biasing and linear amplification of the differential input signals.  
The two outputs are equal in amplitude and opposite in phase, verifying correct differential amplifier behavior.

The differential input voltage of the amplifier varies within the range:  
__-&radic;2 < vid <  &radic;2__

__CASE 1: vid <  &radic;2__  
let vid<sub>p-p</sub> = 100mV

![diffwave](images/diffwave1.png)

__CASE 2: vid >  &radic;2__  
let vid<sub>p-p</sub> = 1.6V

![diffwave](images/diffwave11.png)

For __-&radic;2 < vid <  &radic;2__, the differential amplifier operates linearly with undistorted output. Beyond this range, nonlinear behavior occurs (CASE 2), causing waveform distortion.

- __AC ANALYSIS:__

Transconductance, gm = (2*ID1)/VOV = 2.45 mS

The gain can be found by using __Half circuit analysis__,  
                    Gain = gm * RD  
                         = 2.45m * 2.16k  
                         = 5.292 V/V  
                         = 14.47dB  
Therefore the theoretical gain is 14.47dB

![ac](images/ac1.png)

The simulated gain is 16.15dB  
Frequency at -3dB gain = 5.57GHz  
Gain Bandwidth product = 35.759GHz
