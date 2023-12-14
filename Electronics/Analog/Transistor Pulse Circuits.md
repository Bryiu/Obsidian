# Intro

>[!Important]
>Think of the capacitor as the break in the circuit preventing electrical flow.
>Current then goes from $V_{cc}$ to the ground of the emitter


- Multi-vibrators are circuits that produce square waves
	- All operate on the principle that the transistor can be cut off or in saturation
- Use two transistor amps
	- biased so they're either in cutoff or saturation and never operate in between
		- On in saturation
			- Max current flows from emitter to collector. Output is 0
				- Acts like a short circuit
					- $V_{cc}$ is dropped across the collector load resistor
		- Off in cutoff
			- Transistor acts like an open circuit
				- Output is approximately $V_{cc}$ 
		- ![[Pasted image 20231213115541.png]] 
			- 
- Feedback circuit is added that controls which transistor is on and which is off 
- Output is taken from the collector of one of the transistors
- When the feedback circuit forces $Q_2$ off, output voltage is $V_{cc}$ or high
	- ![[Pasted image 20231213121501.png]] 
- When feedback forces $Q_2$ on, output voltage is 0 or low
	- This is the negative peak
- The frequency of the output square wave depends on how fast the feedback forces the transistors to switch from ON to OFF
	- Depending on components in feedback
- Output can be $Q_1$ or 2. Normally has both connections
	- Two outputs are 180$\degree$ out of phase
## Free Running Multivibrators 

- Produce square wave outputs as soon as power is applied
- As long as DC operating voltage is present; circuit works


## Triggered Multivibrators

- Produce a square wave output wen an external input is applied
	- Turns on and off on an input pulse

# Classification

![[Pasted image 20231213134557.png]] 

- Classified to the number of stable states that are produced by the feedback circuit
- **Multivibrators** that have no stable state are free running.
	- Astable 
		- Means its always switching from on to off
	- Monostable
		- Has one steady condition
		- Triggered multivibrators 
			- Input pulses causes $Q_2$ to turn off and $Q_1$ to turn on
			- Input gone; returns to steady state $Q_2$ on
	- Bistable
		- Has two steady conditions
		- When power is applied, assume $Q_2$ is on and remains on
		- Another type of triggered multivibrator  
		- Input pulses causes $Q_2$ to turn off and $Q_1$ to turn on
			- After the inpulse is gone $Q_1$ remains on
			- Stays in its second stable state condition
			- Second input pulse causes $Q_1$ to turn off and $Q_2$ to turn on
				- After the second input pulse is gone, $Q_2$ remains on
					- Stays in its first stable state condition

## Astable

- ![[Pasted image 20231213135103.png]]
	- Has two capacitors in the feedback circuit
- Output of $Q_1$ is bed back through one capacitor to the input of $Q_2$ 
	- ![[Pasted image 20231213135220.png]] 

### Operation

- ![[Pasted image 20231213175634.png]] 
	- Consists of two common emitter amps
	- $Q_1$ uses $R_1,R_3$ for biasing
		- $R_3,C_2$ control the charge time for the voltage present at the base of $Q_1$ 
	- $Q_2$ uses $R_2,R_4,C_1$ 
	- ![[Pasted image 20231213182655.png]] 
- When the circuit is first energized
	- ![[Pasted image 20231213183631.png]] 
	- Positive voltage is applied to the base of each transistor
		- Capacitors have no effect initially. Both have positive potential applied
		- Since they're not perfectly the same value one will charge the base to .6V first
- $Q_1$ turns on
	- 12V on the collector goes to 0
	- $C_1$ discharges
		- Dumps negative potential to the base of $Q_2$
		- Latches $Q_2$ off
- $Q_2$ collector is 12V since $Q_2$ is off
- The side of $C_1$ is common to the collector ($Q_1$) is 0v.
	- Causes $C_1$ to begin charging through $R_2$ 
		- Voltage at the base of $Q_2$ begins to increase
			- (Both sides are common)
- FIRST STATE
	- ![[Pasted image 20231213185005.png]] 
- SECOND STATE
	- ![[Pasted image 20231214135508.png]] 
- RETURN TO FIRST
	- ![[Pasted image 20231214135706.png]] 
### Checking for Normal Operation

- Checking the frequency
- $f=\frac{1}{0.7*((C_1*R_2)+(C_2*R_3))}$ #formula 
	- Two time constants are added since each controls only half of the period
	- $f=\frac{1}{T}$ 
		- $T=0.7*((C_1*R_2)+(C_2*R_3))$ 
		- 0.7 is used because the transistor will begin conduction prior to the completion of one time constant

### Vars

- ![[Pasted image 20231214142621.png]] 
	- $R_5$ is used to adjust the symmetry of the output waveform
		- Compensate for any differences
		- Added resistance must be used in frequency calculations
- ![[Pasted image 20231214144236.png]] 
	- $R_5$ allows for frequency to be changed
		- Adds the same amount of resistance to both resistors
		- Must be used in frequency calculations 
- ![[Pasted image 20231214144719.png]] 
	- Ensures sharp rise times
		- Diodes isolate capacitor from the output to prevent slow rise times

## Monostable

- ![[Pasted image 20231213172219.png]] 
	- Pink is the trigger input
	- RC time constant of the feedback circuit determines how long $Q_1$ is on and how long $Q_2$ is off after input pulse is applies to $Q_1$ 

### Operation

- ![[Pasted image 20231214150244.png]] 
	- Requires an input to commence oscillations 
		- One stable state
	- $Q_1$ uses these resistors for biasing
		- ![[Pasted image 20231214150600.png]] 
			- $R_3-R_5$ are used for base biasing voltage
				- 3&5 are a voltage divider for base bias voltage $Q_1$ 
				- 2&4 are used for $Q_2$ 
					- 2 is for base bias
					- 4 is collector load resistor
	- $C_1,R_3$ couple the output of one amp to the input of another
	- $D_1,C_2$ are used to input the trigger pulse
- First energized a positive voltage is applied to the base of each transistor amp
	- ![[Pasted image 20231214151449.png]] 
		- As $Q_2$ conducts, collector voltage is used to supply $Q_1$ base
		- When $Q_2$ is on, the voltage on its collector drops to 0V
			- ![[Pasted image 20231214151721.png]] 
		- Base of $Q_1$ drops to 0V, cut off by the conduction of $Q_2$ collector
			- ![[Pasted image 20231214151818.png]] 
		- $Q_1$ turns off, causing the voltage on the collector to rise to 12V
			- ![[Pasted image 20231214152047.png]] 
		- Circuit remains stable until an input trigger is received
- STABLE STATE
	- $Q_1$ is off with 12v on the collector. 
	- $Q_2$ stays on as the base biase voltage is supplied through $R_2$ 
	- $C_1$ charges due to the voltage on the collector of $Q_1$ 
		- ![[Pasted image 20231214152738.png]] 
	- When positive input pulse is received, $D_1$ becomes forward biased
		- ![[Pasted image 20231214152853.png]] 
	- Turns $Q_1$ on
	- $Q_2$ turns off
		- Collector voltage drops to 0v
			- Causes $C_1$ to discharge
				- ![[Pasted image 20231214153033.png]] 
				- Discharging current sets a negative voltage on the base of $Q_2$ 
					- Turns it off
- UNSTABLE STATE
	- $Q_1$ on with 0v at the collector
	- $Q_2$ turns off by the discharging of $C_1$ 
		- ![[Pasted image 20231214153738.png]] 
			- The 12V on the collector is divided and applied to the base of $Q_1$.
				- $Q_1$ remains on until $C_1$ charges enough to turn $Q_2$ on
					- $C_1$ charges towards +12v, an overall change of 24v 
				- $Q_2$ turns on, collector voltage drops to 0, $Q_1$ off
- RETURNed TO STABLE STATE
	- ![[Pasted image 20231214154256.png]] 
	- Stays until the next trigger pulse

### Normal Operation

- Measuring the output frequency off $Q_1, Q_2$ 
	- ![[Pasted image 20231214154814.png]] 
- Compare with frequency of trigger pulses
- $T=0.7*(C_1*R_2)$ #formula 
	- ![[Pasted image 20231214155041.png]] 
		- Time constant of the capacitor

### Vars

- ![[Pasted image 20231214160131.png]] 
	- $R_2$ is variable
		- pulse width of $Q_2$ being off can be adjusted
- ![[Pasted image 20231214160232.png]] 
	- Input is fed through a differentiator
		- changes square wave input to a pulse
			- ![[Pasted image 20231214160323.png]] 
			- A negative trigger input is coupled across $C_1$ to the base of $Q_2$ turning it off
				- $Q_2$ off turns $Q_1$ on
				- $Q_1$ on; $C_1$ discharges to turn $Q_2$ back on


## Bistable 

- ![[Pasted image 20231213172811.png]]  
	- The feedback circuit keeps each transistor in one state until an input pulse changes them