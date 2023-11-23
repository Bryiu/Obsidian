\# Intro

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
### Voltage Regulator Operation

- Typical variable series voltage regulator circuit
- ![[Pasted image 20231119111915.png]] ![[Pasted image 20231119120257.png]] 
- $Q_1$ is the component that maintains a constant $V_{out}$ 
- Since $R_L$ and $Q_1$ are in series, this circuit is a series voltage regulator
	- $R_1,Q_2,D_1$ form the voltage divider that applies to the base of $Q_1$ 
- $R_2$ is used to vary the conduction of $Q_2$ 


#### Troubleshoot
- Calculated = measured --> Ok
	- Otherwise --> Fault
	- ![[Pasted image 20231118112515.png]] ![[Pasted image 20231118112530.png]] 

##### Fixed

- The most common fault is semiconductor devices
- ![[Pasted image 20231119181316.png]] 
	- $D_1$ opens; base voltage increases
	- $R_1$ Shorts; base voltage increases
		- puts $Q_1$ into saturation
	- $D_1$ shorts; Base voltage decreases
	- $R_1$ opens; Base voltage decreases
		- $Q_1$ in cutoff
- ![[Pasted image 20231119183219.png]] ![[Pasted image 20231119183237.png]] 
	- Short on $Q_{ec}$ puts $V_e$ at max
	- Open at $V_c$
		- ![[Pasted image 20231119183610.png]] 
		- prevents collector current flow
		- load current severely reduced
	- Short at $V_e$ 
		- ![[Pasted image 20231119184154.png]] 
		- places $V_e$ at base voltage
		- places base voltage higher than normal
		- $D_1$ and $R_L$ now in parallel; dropping the voltage blow $V_Z$ 
	- Open at $V_e$ 
		- ![[Pasted image 20231119184802.png]] 

##### Variable

- ![[Pasted image 20231119185306.png]] ![[Pasted image 20231119185338.png]] 
- $D_1$ opens, $Q_1$ base voltage increases
	- $Q_1$ goes into saturation
	- ![[Pasted image 20231120112623.png]] 
- $D_1$ shorts; $Q_1$ base voltage decreases
	- Output decreases
	- ![[Pasted image 20231120113838.png]] 
- $Q_2$ Emitter opens; $D_1$ measures 0, E-C measures applied voltage, $R_1$ drops significantly
	- ![[Pasted image 20231120115318.png]] 
- $Q_2$ shorts
	- ![[Pasted image 20231120115352.png]] ![[Pasted image 20231120115415.png]] 
- $R_1$ opens;
	- ![[Pasted image 20231120115523.png]] ![[Pasted image 20231120115533.png]] 
- $Q_1$ shorts; output applied voltage
- $Q_1$ collector shorts; output drops; voltage applied across collector
- $Q_1$ short emitter; emitter reads base voltage
- $Q_1$ emitter open; output 0V

### IC Regulator

- ![[Pasted image 20231120141605.png]] 
	- Have overload protection 
	- Short circuit limiting protection
	- virtually no risk of overloading
- ![[Pasted image 20231120141814.png]] 


#### 7812 IC regulator

- Will maintain a constant 12VDC output when input is between 14.5 and 30V
- 1.5A is maximum current for this regulator
	- Load placed on the output should not fall below 8 $\ohm$ 

### Voltage Doubler

- ![[Pasted image 20231121141855.png]] 
- Two types of voltage doubler circuits
	- ![[Pasted image 20231121142139.png]] 
- Lack of isolation
	- Using an isolation transformer solves this
- Voltage multipliers can increase indefinitely 
	- the higher the multiplication factor; the worse the ripple; lower output capability; higher component ratings must be
- VM's are used where high voltage and low current are required
##### Half wave Voltage doubler

![[Pasted image 20231121142853.png]]  

- $RMS*1.414= Peak$ 
- On the negative alternation, $C_1$ is charged through $D_1$ to 170V
- On the positive, C2 is charged through D2
- Addem together and kablow
	- because the output is taken across $C_2$ 
	- ![[Pasted image 20231121143136.png]] 
		- The heavier the load; the more affect it has on the output

##### Full wave Voltage doubler

- $C_1$ and $C_2$ add in series
- Frequency doubles


## Protection

- Prevents damage to the power supply if the load faults
	- Samples output current then either limits or disables the power supply output
		- ![[Pasted image 20231116115202.png]] 
