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
					- *aka* gain

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

# Amplifiers

## Intro

- DC bias is added to the base so when an AC frequency is input the small change controls Alpha
- Where a transistor is DC biased determines the class of operation. 

### Class A

- ![[Pasted image 20231114124042.png]] 

- Biased so the input signal occurs within the limits of cut-off and saturation
	- Good Fidelity (faithful reproduction of the signal) with low distortion (Output does not match input)
	- Current flows when no input signal is applied, lower efficiency

### Class B

- ![[Pasted image 20231114132134.png]] 
- Biased to collect half of the input signal
	- Increased efficiency 
	- Poor fidelity
- ==Push-Pull Amplifiers==: Two amplifiers connected together to overcome the poor fidelity; maintaining good efficiency.
	- One collects the negative alternation and the other collects the positive
	- Issue with crossover distortion

### Class AB

- ![[Pasted image 20231114132742.png]] 
- Current is zero for a portion
- More efficient than class A; Higher fidelity than class B
- Less efficiency than class B; Less fidelity than class A
- Used to overcome crossover distortion
	- ![[Pasted image 20231114134137.png]] 
	- Found in B push pull amplifiers
### Class C
- ![[Pasted image 20231114134335.png]] 
- Collector current is zero for most of the input cycle
- High efficiency
- Poor fidelity

### Overdriving an amplifier

![[Pasted image 20231114135547.png]]
- This is where the amplitude goes into Cut off and saturation
- Can be done to any of the 4 class's
- distorts the output signal

## Configurations

![[Pasted image 20231114140827.png]] 

![[Pasted image 20231114143136.png]] 


### Common Emitter (CE)

![[Pasted image 20231114140940.png]] 

- Class and Voltage gain ($A_v$) are needed to identify normal operation
- Most frequently used
- Good voltage, current, and power amplification
- Input applied to the base
- Output is taken from the collector
- Only configuration which provides a phase reversal
	- Out of phase 180$\degree$ 
- Input (base) resistance is minimum (500-1500$\ohm$)
- Output (collector) resistance is medium (30k-50k$\ohm$) - because Collector is reversed bias
- ![[Pasted image 20231114141905.png]] 

#### Characteristics

![[Pasted image 20231114152034.png]] 

- Input - Base to emitter
- Output - Emitter to collector
- Increasing input signal produces a decreasing output signal
	- Vice versa
- Bias voltage determined by $R_1$ and $R_2$ 
	- This is combined with the input signal
- $R_4$ and bypass capacitor $C_1$ add stability to the circuit
	- $R_4$ provides temperature stability by decreasing emitter current due to heat
	- $C_1$ provides a path for unwanted AC that is produced
		- ensures output signal is not affected
- $R_3$ determines output signal
	- When collector current increases; $R_3$ has a larger voltage drop 
		- Output decreases
	- Collector current decreases; $R_3$ has a smaller voltage drop
		- Output increases
- Normal operation produces heat
	- Heat causes unpredictable changes at the output
- ![[Pasted image 20231114154651.png]] 
	- $C_2$ and $C_3$ block DC signals from entering the bias and output
		- They dont affect bias voltages
- Class of operation is determined by the bias placed on the base of $Q_1$ by $R_1$ and $R_2$ 
- Gain ($A_v$) is determined by $R_3$ and $R_4$ 

##### Example 
- ![[Pasted image 20231114163748.png]] 
- ![[Pasted image 20231114161448.png]]
	- This is a class A with a gain of 100
		- $A_v=\frac{E_{out}}{E_{in}}=\frac {1}{.01}=100$
	- If bias dropped to .6V; the class becomes B
		- ![[Pasted image 20231114162051.png]] 
###### Calculating Base Bias
- ![[Pasted image 20231114163319.png]] 
	- Solve the Voltage divider
		- ![[Pasted image 20231114163421.png]] 
		- The voltage between $R_1$ and $R_2$ is applied as $Q_1$ bias voltage
	- Bias is above cutoff; Class A
- Once Operation found; compare I/O signals to find gain
	- ![[Pasted image 20231114164158.png]] 
		- $A_v=\frac{E_{out}}{E_{in}}$
			- $A_v=\frac {3}{.01}=300$
		- Used to verify expected
		- If unknown:
			- $A_v=\frac {R_c}{0.025 \div I_e}$ 
				- Load resistor $R_c$ and emitter current are needed
				- Not exact value; checks normal operation
				- Solve for $I_e$
					- Calculate base voltage
					- Calculate $E_e$
						- $E_e = E_b - (Base \, bias \, cutoff)$ ==.6==
					- Calculate $I_e$ 
						- $I_e = \frac {E_e}{Emitter \, Resistor}$ 
			- $A_v = \frac {30k}{0.025 \div 0.00024} = 288$  
		- Multiply input by $A_v$ 
			- $0.01*288=2.88V$ 




### Common Collector

- ![[Pasted image 20231114142215.png]] 

- Used for impedance matching
	- High impedance matched to a low impedance load
- High current gain
	- sometimes used as a current driver
- Input resistance is high (2k-500k$\ohm$)
	- Input is applied to the reverse biased junction
- Output resistance is low (50-1500$\ohm$)
	- Output is taken from the forward biased junction
- ![[Pasted image 20231114142446.png]] 

### Common Base

![[Pasted image 20231114142539.png]] 

- Used for impedance matching
	- Low impedance matched to a high impedance
- Large voltage gain
- Input resistance low (30-160$\ohm$)
	- input applied to the forward biased junction
- Output resistance is high (250k-550k$\ohm$)
	- output taken from reversed biased
- ![[Pasted image 20231114143058.png]] 