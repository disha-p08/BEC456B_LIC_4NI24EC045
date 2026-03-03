Q1) Design CS amplifier configurations using NMOSFET in tsmc180nmtech.lib in LTSPICE.

Given: Vdd = 1.8V, Power <= 1mW, CL = 1pF, L = 180nm, Vin = 10mV, f = 1kHz

**CIRCUIT DIAGRAM:**

Without Capacitor:

![CIRCUIT](images/circuit3.png)


**DESIGN CALCULATIONS:**

**1. DC ANALYSIS:**

Power = Voltage * Current

P = VDD*ID

Let ID = 200uA

Thus, Power = 1.8*200u = 0.36mW which is <= 1mW 

Given, The drop across RS is 0.2V --> VS = 0.2V

Vout = VDS + IDRS = (VDD/2) + 0.2 = (1.8/2) + 0.2 = 1.1V

We know that, by Ohm's law,

VS = IDRS

RS = VD/ID = 0.2/200u = 1kohm
<br><br><br>
For M1 (NMOS) transistor:

Given, the overdrive voltage VOV = 0.25V

From the datasheet, VTH = 0.36V

We know that,

VOV = VGS - VTH  

VGS = VOV + VTH = 0.25 + 0.36 = 0.61V

Biasing voltage VB1 is obtained by,

VB1 = VG1 = VGS + IDRS = 0.61 + 0.2 = 0.81V
<br><br>
For M1 to be SATURATION,

VGS >= VTH

0.61 >= 0.36

and VDS >= VOV

(VDD/2) >= VOV

0.9 >= 0.25

Hence both the conditions are satisfied. Therefore M1 is operating in **SATURATION** region.
<br><br>                                                                        
From the drain current formula in saturation region, we get the value of W.

![id](images/id.png)

![k](images/k.png) = 230.4uA/V^2

Hence, W1 = 5um 

---

For M2 (PMOS) transistor:

Given, the overdrive voltage VOV = 0.25V

From the datasheet, VTH = 0.39V


We know that,

VOV = VSG - |VTH|  

VSG = VOV + |VTH| = 0.25 + 0.39 = 0.64V


Biasing voltage VB1 is obtained by,

VB2 = VG2 = VS + VSG = VDD - VSG = 1.8 - 0.64 = 1.16V
<br><br>
For M2 to be SATURATION,

VSG >= VTH

0.64 >= 0.39

and VDS >= VOV

(VDD/2) >= VOV

0.9 >= 0.25

Hence both the conditions are satisfied. Therefore M2 is operating in **SATURATION** region.
<br><br>
From the drain current formula in saturation region, we get the value of W.

![id](images/id.png)

![k](images/k.png) = 230.4uA/V^2

Hence, W2 = 11.823um 
<br><br><br>
To fix the DC operating point, 

![DC_opnt1](images/DC_opnt3.png)

Initially, we get 

**ID = 75.029uA for W1 = 5um and W2 = 11.823um**

After altering W values, we get 

**ID = 201.37uA for W1 = 27um and W2 = 36.5um**


The DC biasing ensures that the drain current is set according to the power budget while keeping the MOSFET operating in the saturation region, which is essential for achieving proper and stable amplification.

---

**2. Transient Analysis:**

![wave](images/waveform3.png)

Here the blue waveform represents the input voltage and the green waveform represents the output voltage. We can observe the 180 degree phase shift and the amplification of the output signal.

Peak to peak values of Vin = 20mV ; Vout = 224mV

Therefore, the Practical Gain |Av| = Vout/Vin = 2.678 = 8.55dB

From the theoretical calculations, Transconductance gm = 2Id/Vov = 0.749mmho

|Av| = gm*RD = 3.37 = 10.55dB

Hence,

**Theoretical |Av| = 10.55dB**

**Practical or simulated |Av| = 8.55dB**

In theory, the MOSFET has infinite output resistance, no parasitic capacitances, and perfect biasing, which leads to higher calculated gain. In simulation, effects such as channel‑length modulation, finite output resistance, parasitic capacitances, and small bias shifts reduce the effective gain. Thus, the simulated gain is lower and more realistic, while the theoretical gain represents the ideal upper limit.

**4. Frequency Analysis :**

- Without Capacitor

![freq](images/freq.png)

Bandwidth Bw = 51.892GHz

Gain Bandwidth Product GBwP = Av*Bw = 140.004GHz

- With Capacitor

![CIRCUIT1](images/circuit31.png)

![freq1](images/freq1.png)

Bandwidth Bw = 40.52MHz

GBwP = Av*Bw = 108.59MHz

Therefore, GBwP:

**Without Capacitor = 140.004GHz**

**With Capacitor = 108.59MHz**

The presence of the coupling capacitor shifts the frequency response upward, limiting low‑frequency operation and reducing the effective bandwidth. Without the capacitor, the amplifier shows a much wider bandwidth (in the GHz range), but with the capacitor, the usable bandwidth is restricted to the mid‑frequency range (in the MHz range).

**RESULTS:**

CS Amplifier of Vgs = 0.9V, W = 1530.65nm , L = 180nm , Vdd = 1.8V and Rd = 4.5k is designed and verified for power budget of P = 1uW.
- The MOSFET operates in the saturation region.
- The output waveform is amplified and shows 180° phase inversion.
- The Gain Bandwidth Product obtained:

   Without Capacitor = 188.084 MHz

   With Capacitor = 188.594 MHz
- Proper mid-band amplification is observed.

**VALIDATION:**

The phase inversion observed in the output matches the theoretical behavior of a CS amplifier.
The gain obtained is consistent with theoretical expectation:
The frequency response partially matches theory, showing proper mid-band behavior and high-frequency attenuation.
Thus, the simulated results validate the expected operation of the Common Source amplifier.

**INFERENCE:**
- The circuit successfully amplified the weak input signal. The output signal is significantly larger than the input, demonstrating the transconductance property of the MOSFET.
- A 180 degree phase shift was observed between the input and output waveforms, which is a characteristic feature of the Common Source configuration.
- The output waveform remained undistorted for the given input, indicating
