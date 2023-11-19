# Intro

- Power supply and diode rectifiers change AC power to DC power
- ![[Pasted image 20231116110330.png]] 

## Input 

- When voltage is not directly connected to the rectifier, the input section is used to step up or down AC input required for output.
	- A power transformer

## Rectifier
- Average measurements are more accurate than RMS for a rectifier because the output is unfiltered
- Converts AC to pulsating DC
	- ![[Pasted image 20231116111432.png]] 

### Half-Wave

- One diode
- Diode series limiter
	- ![[Pasted image 20231116120616.png]] 
	- ![[Pasted image 20231116131551.png]] 
		- $R_L$ develops the signal output
	- $V_{DC}=V_{peak}*0.318$ 
		- ex:
			- ![[Pasted image 20231116131939.png]] 
		- Converting RMS to peak
			- $V_p=\frac{V_{rms}}{0.707}$  
- Not efficient
	- only use half of the input signal
- Simple; inexpensive

### Full-Wave

- Two diodes
	- ![[Pasted image 20231116121322.png]]
	- ![[Pasted image 20231116132807.png]] 
		- $R_L$ develops the output signal
		- $V_{DC}=V_{peak}*0.636$ 
	- Continuous input doubles the frequency
	- Each diode receives a voltage half of the amplitude of the secondary voltage
- More efficient than half wave
	- Use the entire input signal

### Bridge 

- Four diodes		
	- Eliminate the need for a center tapped transformer
	- Output voltage is twice the full wave rectifier
	- ![[Pasted image 20231116123943.png]]  
	- ![[Pasted image 20231116152515.png]] 
		- Diodes only conduct when forward biased
		- During positive half cycle, point A is positive to B
			- Current at B cycles to ground
	- Reversing the diodes creates a pulsating negative DC
		- ![[Pasted image 20231116124125.png]] 
	- $V_{avg}=V_{pk}*0.636$ 
- More efficient and less expensive 

## Filter

- Changes pulsating DC to smooth DC
	- Consists of reactive components
		- ![[Pasted image 20231116112806.png]] 
			- Transients of the capacitor eliminate variations
			- ![[Pasted image 20231116111734.png]]
## Regulator

- maintains the output voltage at a constant level; despite changes in load current
	- ![[Pasted image 20231116112942.png]] 
		- Contain Zener diodes to maintain output
			- ![[Pasted image 20231116113148.png]] 
### Series Voltage Regulators

![[Pasted image 20231117105535.png]] 
![[Pasted image 20231117105925.png]] 
- $R_1$ is the series voltage regulator.
	- One end is not connected 
	- Manually adjusted potentiometer to maintain voltage drop
		- subtracts voltage from the source
- Any changes to current drawn by the load also affect output voltage
- 


### Parallel Voltage Regulator

![[Pasted image 20231117120452.png]] 

- Decreasing resistance in $R_1$ causes current in $R_1$ branch to increase
	- Increases current through $R_2$ 
		- $R_2$ voltage drop increases; dropping $V_{out}$ 
- If source decreases; voltage drops decrease
	- decreasing $R_1$ will decrease current; Decreasing $R_2$ 

### Zener Diodes

![[Pasted image 20231117183248.png]] 
- Acts like a closed switch when forward biased
- Acts like an open switch when reversed biased
	- ![[Pasted image 20231118104135.png]] 
	- ![[Pasted image 20231118104441.png]] 
- Designed to operate in the break down condition. 
	- With too much reverse bias
- When the reversed biased voltage is higher than $V_z$ or *breakdown*, the diode acts like a resistor always having a voltage drop equal to $V_z$ 
- Can be used as shunt regulators or fixed voltage references
- ![[Pasted image 20231117184832.png]] 
	- Shunt regulators are placed in parallel with the load ($R_L$)
	- When forward biased
		- Requires 0.7V
		- $V_{out}$ is 0.7V
		- Acts as an open
	- When reversed biased
		- Acts like an open switch
		- Reverse current begins to flow through
		- ![[Pasted image 20231117185753.png]] 
- Output voltage of a rectifier filter is applied to the collector
	- ![[Pasted image 20231118175216.png]] 
		- $R_L$ and $Q_1$ are in series
		- Collector bias is obtained from the filter
		- Emitter voltage is developed by the action of the transistor
#### Operation of Zener Diodes
- Maintains a constant voltage drop as long as it operating in the breakdown region
	- ![[Pasted image 20231118181353.png]] 
		- ![[Pasted image 20231118181756.png]] 
			- $V_{ce}$ is the remainder from the source; with $V_e$ 
			- If input voltage increases, collector to emitter resistance increased; and vice versa
			- If $R_L$ decreases, $V_{out}$ decrease. Load current increases
			- When $V_e$ decreases, base to emitter PN junction forward bias increases, decreasing emitter to collector resistance. 
				- Causes $Q_1$; $I_{ce}$ to increase
			- If $V_e$ & $R_L$ increases, $V_{out}$ will also increase
				- This will cause load current to decrease
>[!Important]
>This is based off of potential difference. So biasing is based off of dominant charge



#### Troubleshoot
- Calculated = measured --> Ok
	- Otherwise --> Fault
	- ![[Pasted image 20231118112515.png]] ![[Pasted image 20231118112530.png]] tr

## Protection

- Prevents damage to the power supply if the load faults
	- Samples output current then either limits or disables the power supply output
		- ![[Pasted image 20231116115202.png]] 
