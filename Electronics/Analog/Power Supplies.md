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
## Protection

- Prevents damage to the power supply if the load faults
	- Samples output current then either limits or disables the power supply output
		- ![[Pasted image 20231116115202.png]] 
