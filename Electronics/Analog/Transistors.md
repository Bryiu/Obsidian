# Intro

- Transistors are used as:
	- Amplifiers
	- Oscillators
	- Electronic switches
	
 - NPN
	- ![[Pasted image 20231111124609.png]] 
- ==Emitter== is heavily doped; to have a large number of current carriers
	- N-Type Electrons
	- P-Type Protons
- ==Base== is lightly doped; allows current carriers to pass from ==Emitter== to ==Collector== 
- ==Collector== is moderately doped. Collects current from base
	- The collector is the largest because it needs to dissipate the most heat
- ![[Pasted image 20231111164755.png]] 
	- ![[Pasted image 20231111170715.png]] 
		- Schematic letter "Q"
- ![[Pasted image 20231111172034.png]] 
- Power Transistors
	- ![[Pasted image 20231111172257.png]] 
- Two types of signal applied to a transistor
	- Input
	- Bias
- Transistors transfer energy from low resistance to high resistance
- Too much positive bias on the base of an NPN transistor causes it to lose its amplifying ability
- Too little bias on the base will stop it conducting current
- ![[Pasted image 20231112172646.png]] 
- Saturation is when the base current is above the necessary current to turn the transmitter on 
	- Collector current remains constant
	- transmitter acts as a short
	- ![[Pasted image 20231112183651.png]] 
- Increasing $V_C$ has very little effect on $I_C$ 
	- ![[Pasted image 20231112184343.png]] 
	- $I_e=I_b+I_c$ 
		- The ratio's of the currents are constant for each type of transistor
			- This is called alpha ( $\alpha$ ) and beta ($\beta$ ), to describe transistor operation under any condition and bias level
				- $\alpha = \frac{I_c}{I_e}$
					- $\alpha$ never exceeds 1. Normal value ranges .97 and .99
				- $\beta = \frac {I_c}{I_b}$
					- $\beta$ values are larger than 1. Normal value between 20 and 400

# Basic Bias Circuits
## Fixed
### NPN

![[Pasted image 20231113173332.png]] 

- $R_b$ is the bias resistor
- $R_L$ is the load resistor
- The voltage on the resistor is higher on the collector, so that the collector is a higher positive voltage than the bias voltage
- *Disadvantage* is that small changes to the base current due to temperature affect the collector voltage

### PNP
 


## Self

![[Pasted image 20231113174601.png]] 

- $R_b$ is connected directly to the collector
- As $I_c$ increases $I_b$ decreases
	- Reduces base bias, returns $I_c$ to normal

## Combination

### NPN 
- ![[Pasted image 20231113175554.png]] 
- $R_3$ self biases the emitter
	- Which is controlled by the base voltage
- $C_1$ keeps AC input off the emitter

### PNP

- $V_{cc}$ is changed to (-)