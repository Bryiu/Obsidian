# Intro

- FET's are used in place of bipolar transistors when a circuit requires extremely high input impedance 
- ![[Pasted image 20231129132157.png]] 
	- Source: Current carriers enter the FET
	- Drain: Current carriers leave the FET
	- Gate: Current carriers controlled by this element
- ![[Pasted image 20231129133445.png]] ==MOSFET== 
- ![[Pasted image 20231129133512.png]] ==EMOSFET== 
- ![[Pasted image 20231129133334.png]] ==JFET== 
	- The two P type materials are connected to allow only one gate input
	- The width of the N channel controls the current flow and the size of the PN junction barriers

# Operation

- ![[Pasted image 20231129141516.png]] 
	- Positive voltage applied to drain $V_{dd}$
	- Negative voltage applied to gate $V_{gg}$
		- Reverse biases PN junction
		- Increasing $V_{gg}$ ($V_{gs}$) grows size of gate, decreases current
			- When current stops flowing; this is ==cut off== 
		- Decreasing $V_{gg}$ negative gate voltage decreases PN junction barrier
			- Increases current
		- FET's are made to operate with the gate reversed biased
			- Forward bias will damage component
	- $V_{gs}$ = reverse biased voltage between gate and source
	- $I_{d}$ = Source to drain current flow
		- ![[Pasted image 20231129144709.png]] 
		- ![[Pasted image 20231129144743.png]] ![![Electronics/Analog/#^Table]]
- ==*Transconductance*==: The amount of control that the input voltage has over the output current 
	- $g_m$ 
		- Comes from data book
		- Measured in mho or siemens
	- Opposite of resistance
	- similar to $\beta$ 
		- Values range between 1 and 10 $m$mhos 
			- ex: Means 2$m$mhos is a 1$V$ change produces a 3$m$A change in output
				- ![[Pasted image 20231129152141.png]] 
- ==*mho*==: Conductance; **Ohm backwards** 
- ==*siemens*==: Conductance
- FETS transfer **conductance**; Transistors transfer **resistance**
- Gate biasing does not produce a stable operating point and normally not used
	- ![[Pasted image 20231129152934.png]] 
- Self biasing
	- ![[Pasted image 20231129153210.png]] 
		- One Voltage source
		- $V_{dd}$ applies a positive voltage on the drain through $R_d$ 
		- $R_s$ sets up the reverse bias between gate and source
			- Gate is less positive than source
- Voltage Divider Bias
	- ![[Pasted image 20231129153449.png]] 
		- One voltage source
		- Applies a positive voltage on drain through $R_d$ 
		- $R_1,R_2$ form a fixed bias on the gate
		- $R_s$ applies self biasing
- Source Biasing
	- ![[Pasted image 20231129153640.png]] 
		- Two voltage sources

- FET's can be used instead of bipolar transistors
	- Difference is the input resistance
		- ![[Pasted image 20231130143306.png]] 
		- The high input resistance of a FET is obtained by applying the input to the reverse biased gate
			- Used in test equipment
				- Prevents the test equipment from loading the circuit

![[Pasted image 20231130144845.png]] 

## Common Source

- Self biasing; Temperatures do not affect the source to drain current flow
- input applied to the gate
- Most common
- ![[Pasted image 20231130150032.png]] 
	- $C_2$ grounds AC to the source
		- Allows only an AC signl on the gate to control current flow
	- With no bias voltage applied to the gate and source is at a positive voltage; Gate to source PN junction is reversed biased
		- $V_{gs}$ is a negative value
	- Inverts AC output signal
	- ![[Pasted image 20231130170529.png]] 
		- as input goes negative, gate voltage ($V_g$) increases
			- Decreases reverse bias ($V_{gs}$)
			- Source voltage $V_s$ remains positive because of $C_2$ 
			- Decrease in $V_{gs}$ increases source to drain current
				- $R_2$ drops more voltage
					- Decreases drain voltage ($V_d$)
				- $C_3$ blocks the dc voltage on the drain
	- A smaller AC input controls a larger output current, producing an amplified inverted AC signal

>[!Important]
>The difference between the common source and drain is the inverted output  

- Measured: $A_v=\frac {E_{output}}{E_{input}}$ #formula 

- Calculated: $A_v=g_m*R_d$ #formula 
	- $g_m=\frac {I_{output}}{E_{input}}$ 
	- if $g_m$ is not known use 2$m$mhos 

## Common Drain

- input applied to the gate


## Common Gate

- Not used as an amplifier because it doesnt have a high input resistance
- Used as electronic switches


## MOSFET

![[Pasted image 20231201172332.png]] 
- Base does not draw current like the base of a bipolar transistor
- MOSFETS are ESD
- ![[Pasted image 20231201175121.png]] 
	- The gate is not connected to any other part of the device
		- Operates similar to a capacitor
		- ![[Pasted image 20231201175638.png]] 
			- Blue region is the oxide layer
				- formed when the wafer is heated in normal air
				- Silicon dioxide ($Si0_2$) 

### Operation

- ![[Pasted image 20231201180525.png]] 
	- A voltage is applied to the gate to overcome the threshold
		- Around 1$V$ 
		- Positive with respect to the source
			- Attracts negative charges between source and drain
			- Threshold voltage is the point where the voltage applied to the gate causes the same number of positive and negative charges in the channel region.
				- No voltage - the channel is P-type
	- As the gate voltage goes above threshold; Inversion occurs
		- Inversion: The charge on the gate causes more negative ions in the channel than positive
		- 