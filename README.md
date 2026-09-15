# 2.-Design-implement-and-simulatioin-of-Integrator-and-Differentiator
**AIM:**
To design , implement and simulate  an integrator and differentiator circuits

**APPARATUS  and SOFTWARE REQUIRED:**
S.No	Name of the Apparatus	Range	Quantity
1.	Signal Generator	3 MHz	1
2.	DSO	30 MHz	1
3.	Dual RPS	(0 – 30) V	1
4.	Op-Amp	µA741	1
5.	Bread Board		1
6.	Resistors	1K,10K,100K,	2
7.	Capacitors	0.1µF,0.01µF	1
8.	Connecting wires and probes	As required	
9.  LT SPICE software

**THEORY:**

**INTEGRATOR**
A circuit in which the output voltage waveform is the integral of the input voltage waveform is the integrator. Such a circuit is obtained by using a basic inverting amplifier configuration if the feedback resistor Rf is replaced by a capacitor Cf . The expression for the output voltage is given as,
Vo = - (1/Rf C1 ) ∫ Vi dt

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. Normally between fa and fb the circuit acts as an integrator. Generally, the value of fa < fb . The input signal will be integrated properly if the Time period T of the signal is larger than or equal to Rf Cf . That is,
T ≥ Rf Cf

The integrator is most commonly used in analog computers and ADC and signal-wave shaping circuits.

**DESIGN:**
 
To obtain the output of an Integrator circuit with component values R1Cf = 0.1ms , Rf = 10 R1 and Cf = 0.01 µF and also if 1 V peak square wave at 1000Hz is applied as input.
We know the frequency at which the gain is 0 dB, fb = 1 / (2π R1 Cf) Therefore fb = 	 Since fb = 10 fa , and also the gain limiting frequency fa = 1 / (2π Rf Cf)
We get , R1 =	and hence Rf = 	

**DIFFEERENTIATOR:**

The differentiator circuit performs the mathematical operation of differentiation; that is, the output waveform is the derivative of the input waveform. The differentiator may be constructed from a basic inverting amplifier if an input resistor R1 is replaced by a capacitor C1 . The expression for the output voltage is given as,
Vo = - Rf C1 ( dVi /dt )

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. A resistor Rcomp = Rf is normally connected to the non-inverting input terminal of the op-amp to compensate for the input bias current. A workable differentiator can be designed by implementing the following steps:
1.	Select fa equal to the highest frequency of the input signal to be differentiated. Then, assuming a value of C1 < 1 µF, calculate the value of Rf.
2.	Choose fb = 20 fa and calculate the values of R1 and Cf so that R1C1 = Rf Cf.

The differentiator is most commonly used in wave shaping circuits to detect high frequency components in an input signal and also as a rate–of–change detector in FM modulators.
 
**DESIGN (DIFFERENTIATOR):**

Design an op-amp differentiator that will differentiate an input signal with fmax = 100HZ Select fa = fmax = 100 HZ = 1 / 2πRFC1
Let C1 = 0.1μF
Then RF = 1 / 2π(102)(10-7)
= 15.9KΩ
Now choose fb = 10fa = 1 / 2πR1C1 Therefore, R1 = 1 / 2π(103)(10-7)
= 1.59KΩ Since RFCF = R1C1
We get, CF = (1.59*103*10-7) / 15.9*103
= 0.01μF


**PROCEDURE:**
1.	Connections are given as per the circuit diagram
2. + Vcc and - Vcc supply is given to the power supply terminal of the Op-Amp IC.
3.	By adjusting the amplitude and frequency knobs of the function generator, appropriate input voltage is applied to the inverting input terminal of the Op- Amp.
4.	The output voltage is obtained in the CRO and the input and output voltage waveforms are plotted in a graph sheet.

 
**INTEGRATOR:**
  **CIRCUIT DIAGRAM**<img width="1600" height="1090" alt="WhatsApp Image 2026-09-15 at 8 48 00 PM" src="https://github.com/user-attachments/assets/f64f9982-d2de-4f69-a69b-ee98a992fe50" />



  **MODEL GRAPH:**<img width="1600" height="808" alt="WhatsApp Image 2026-09-15 at 8 48 54 PM" src="https://github.com/user-attachments/assets/d6b4bed3-4302-461c-a724-e088694ae198" />



  **TABULATION:**<img width="1600" height="536" alt="WhatsApp Image 2026-09-15 at 8 48 28 PM" src="https://github.com/user-attachments/assets/52b64d28-937a-406e-9ead-1e9a689161fe" />

 

**GRAPH:**
<img width="1045" height="1511" alt="WhatsApp Image 2026-09-15 at 8 51 35 PM" src="https://github.com/user-attachments/assets/a01be261-04b4-4f2a-b39d-5f9b1a3acba9" />


**DIFFERENTIATOR:**
  **CIRCUIT DIAGRAM**<img width="1600" height="1391" alt="WhatsApp Image 2026-09-15 at 8 50 22 PM" src="https://github.com/user-attachments/assets/1164054c-e783-4e26-a583-510acd2b6234" />



  **MODEL GRAPH:**<img width="1600" height="826" alt="WhatsApp Image 2026-09-15 at 8 49 21 PM" src="https://github.com/user-attachments/assets/e073f9bf-510b-4368-9b8c-64abbff8167f" />
<img width="1512" height="1600" alt="WhatsApp Image 2026-09-15 at 8 50 38 PM" src="https://github.com/user-attachments/assets/473d190a-807a-4648-a992-caffb1e6ef09" />



  **TABULATION:**<img width="1600" height="613" alt="WhatsApp Image 2026-09-15 at 8 50 04 PM" src="https://github.com/user-attachments/assets/64d8e3bc-1dec-44f1-9892-250dea96b37b" />
  **GRAPH:**
<img width="996" height="1476" alt="WhatsApp Image 2026-09-15 at 8 52 08 PM" src="https://github.com/user-attachments/assets/4b355dce-d026-4e0f-9ebf-afe3fe27e64a" />
<img width="1080" height="1567" alt="WhatsApp Image 2026-09-15 at 8 51 18 PM" src="https://github.com/user-attachments/assets/4d1af12e-993a-4148-a47f-a084ffe191dd" />



 

**LT-SPICE Tool:PROCEDURE:**
•	Double click on LT-Spice icon.
•	New schematic window open.
•	Pick and paste the required component from the library and draw the circuit diagram .
•	Complete the connection.
•	Save the file by giving file name.
•	Click on the run option ->click advanced open ->select Ac analysis->enter the amplitude time delay stop time value.
•	Click on the run option ->simulation window opens->place the probe ->output graph is obtained.
 
  **LT SPICE**
  **CIRCUIT and Waveform**<img width="806" height="478" alt="WhatsApp Image 2026-09-15 at 9 10 29 PM" src="https://github.com/user-attachments/assets/3d2689ee-3f35-487b-a164-e0e837a67b46" />

  <img width="827" height="391" alt="WhatsApp Image 2026-09-15 at 9 10 45 PM" src="https://github.com/user-attachments/assets/228fe9d5-2bbe-4c55-b189-f311ce258404" />


**RESULT:**
Thus the Integrator and Differentiator are designed and simulated performance was successfully tested using op-amp IC 741 and LT SPICE.
