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
  **CIRCUIT DIAGRAM**
  <img width="1600" height="1028" alt="WhatsApp Image 2026-09-15 at 7 14 25 PM" src="https://github.com/user-attachments/assets/1ea7a785-ae1a-4799-af6a-1aeb1194970b" />



  **MODEL GRAPH:**<img width="1600" height="1038" alt="WhatsApp Image 2026-09-15 at 7 14 53 PM" src="https://github.com/user-attachments/assets/442d0aaf-60ef-4088-9ebe-942ec2d952b1" />



  **TABULATION:**<img width="1600" height="541" alt="WhatsApp Image 2026-09-15 at 7 14 41 PM" src="https://github.com/user-attachments/assets/83ce7ea6-6fe7-4446-8a35-e4d7b0a80c78" />

 **GRAPH:**<img width="1080" height="1513" alt="WhatsApp Image 2026-09-15 at 7 15 19 PM" src="https://github.com/user-attachments/assets/3d36064b-c4af-41c0-aeed-3714a41c0c40" />


**DIFFERENTIATOR:**
  **CIRCUIT DIAGRAM**<img width="1600" height="814" alt="WhatsApp Image 2026-09-15 at 7 16 02 PM" src="https://github.com/user-attachments/assets/dfb07f3e-a008-42ff-81a4-b8efae83c34b" />



  **MODEL GRAPH:**<img width="909" height="1600" alt="WhatsApp Image 2026-09-15 at 7 17 19 PM" src="https://github.com/user-attachments/assets/5d4d54b2-9394-45b1-90d3-70326e995f07" />



  **TABULATION:**<img width="1600" height="665" alt="WhatsApp Image 2026-09-15 at 7 16 16 PM" src="https://github.com/user-attachments/assets/d660a87f-0c40-44b9-9d35-c7d22c025eb4" />

**GRAPH:**``<img width="1080" height="1405" alt="WhatsApp Image 2026-09-15 at 7 16 41 PM" src="https://github.com/user-attachments/assets/4b07acb8-6827-4454-a14e-ca4afb40ee3d" />


 

**LT-SPICE Tool:PROCEDURE:**
•	Double click on LT-Spice icon.
•	New schematic window open.
•	Pick and paste the required component from the library and draw the circuit diagram .
•	Complete the connection.
•	Save the file by giving file name.
•	Click on the run option ->click advanced open ->select Ac analysis->enter the amplitude time delay stop time value.
•	Click on the run option ->simulation window opens->place the probe ->output graph is obtained.
 
  **LT SPICE**
  **CIRCUIT and Waveform**
  <img width="1080" height="1451" alt="WhatsApp Image 2026-09-15 at 7 22 03 PM" src="https://github.com/user-attachments/assets/cacf673f-6927-4548-bc09-6069d47e88a7" />

  

**RESULT:**
Thus the Integrator and Differentiator are designed and simulated performance was successfully tested using op-amp IC 741 and LT SPICE.
