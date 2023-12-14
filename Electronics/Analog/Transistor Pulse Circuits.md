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

## Monostable

- ![[Pasted image 20231213172219.png]] 
	- Pink is the trigger input
	- RC time constant of the feedback circuit determines how long $Q_1$ is on and how long $Q_2$ is off after input pulse is applies to $Q_1$ 

## Bistable 

- ![[Pasted image 20231213172811.png]]  
	- The feedback circuit keeps each transistor in one state until an input pulse changes them