# Intro

- Trigger devices are solid state components which turn on when an input exceeds a specified value
	- Switches
		- UJT and SCRs are designed only for switching
			- Requires less circuitry, saves space and cost

# UJT

- ![[Pasted image 20231220103401.png]] ![[Pasted image 20231220103618.png]] 
	- Arrowhead always pointing to $B_1$ base
		- No P-type bases
- Purpose is to switch voltage
	- Turns on when input voltage exceeds a specified level
- ![[Pasted image 20231220103535.png]] 
	- less circuitry
- ![[Pasted image 20231220104118.png]] 
	- N-Type is lightly doped
	- P-Type is heavily doped
	- Only when the junction is forward biased will current flow from the N-Type to P-type

## Operation

- Only requires biasing bases
- ![[Pasted image 20231220112133.png]] 
	- $B_2$ is positive
	- Emitter receives input
- When input voltage is sufficiently positive, $B_1$ to emitter is forward biased and current will flow
	- When on, emitter current flows
- When not positive, current does not flow
- Takes approx +0.6V
- ![[Pasted image 20231220113304.png]] 
	- Low current because there is high resistance between the two bases
		- $R_{bb}$ = Interbase resistance
- ![[Pasted image 20231220114551.png]] 
	- This places a positive voltage on the cathode of the diode
	- The input voltage must be larger than $+E_{R_{bb_1}}$ to forward bias the diode and turn it on 
	- Placement of the emitter determines the voltage required to overcome $+E_{R_{bb_1}}$ 
		- ![[Pasted image 20231220120806.png]] 
			- If $V_{cc}=12$ and $R_{bb_1}=R_{bb_2}$ then it takes a little more than 6v to turn on   
				- Once on, $R_{bb_1}$ drops to near 0
			- Heavily doped Emitter forces holes into the base when forward biased
			- To find turn-on voltage for a particular UJT
				- Find eta ($\eta$) in a transistor reference book 
					- $Turn\, on= \eta * V_{cc}$ #formula 
					- $\eta = \frac {R_{bb_1}}{R_{bb_1}+R_{bb_2}}$  #formula 
--- 

### UJT Oscillators

- Can produce 3 ouput signals
- ![[Pasted image 20231220141952.png]] 
- Typical UJT Oscillator circuit
	- ![[Pasted image 20231220142116.png]] 
		- Produces Sawtooth wave
		- Changes DC power to AC
		- $V_{cc}$ applies bias voltage
		- RC circuit that applies emitter voltage to $Q_1$ 
		- Operation based on the RC time transient
	- ![[Pasted image 20231220143058.png]] 
		- $C_1$ charges until Turn on voltage is reached
		- ![[Pasted image 20231220143151.png]] 
		- As $C_1$ discharges voltage drops and $Q_1$ turns off
		- Cycle repeats
		- When $Q_1$ turns on emitter voltage drops to 0v
			- ![[Pasted image 20231220143542.png]] 
		- $Q_1$ turns on, allowing $C_1$ to charge again
			- ![[Pasted image 20231220143630.png]] 
		- Frequency depends on the RC time constant
			- $f=\frac {1}{T}$ #formula 
				- $T=R*C$ 
- When a small resistor is added to each base circuit, three output signals are produced
	- ![[Pasted image 20231220145214.png]] 
		- TP1, output voltage is a little less than $+V_{cc}$ as long as $Q_1$ is off
			- Since $R_2$ is a small value, most of $V_{cc}$ is dropped across $Q_1$ 
	- ![[Pasted image 20231220145849.png]] 
		- $Q_1$ turns on $R_2$ drops more voltage
			- Decreases voltage on $B_2$ 
			- Doesnt stay on long. Only for the time it takes $C_1$ to discharge through $R_3$ 
				- ![[Pasted image 20231220150616.png]] 
				- Same frequency as the sawtooth since they both rely on charging and discharging of $C_1$ 
					- ![[Pasted image 20231220150756.png]] 
	- ![[Pasted image 20231220151127.png]] 
		- $Q_1$ off, Voltage at TP2 is about 0
			- Most voltage is dropped across $Q_1$ 
		- $Q_1$ on, Voltage across $R_3$ becomes larger
			- Conducts heavily between E and $B_1$ 
		- ![[Pasted image 20231220152007.png]] 
			- $Q_1$ doesnt stay on long; only the RC Time constant through $R_3$ 
				- ![[Pasted image 20231220152128.png]] 

### Checking for Normal Operation

- Compare measured frequencies with calculated frequencies
	- Calculated frequency uses one TC of $R_1$ and $C_1$ 
 

# SCR 

- ![[Pasted image 20231220122522.png]] 
- Purpose is to switch current on and off
	- Turn on when current is applied to one of the elements
	- Can replace mechanical switches that control large amounts of load current
		- No moving parts
- ![[Pasted image 20231220123445.png]] 
	- Only when the Anode to cathode are forward biased will current flow
		- If the gate allows it
			- Gate is connected to a thin piece of P-Type material
				- Can be as thin as one atom

## Operation

- ![[Pasted image 20231220124327.png]] 
	- When Anode is negative with respect to cathode, no current flows
	- When Anode is Positive to the cathode; No current flows
- ![[Pasted image 20231220124752.png]] 
	- Applying a positive current flow to the gate causes the P-Type material to vanish
		- Voltage is necessary to cause current flow
			- Must be +0.7V
	- Gate to cathode current flow eliminates the P-Type material gate
		- SCR acts like a diode
			- Current flows
	- Removing gate current when SCR is on has no effect
		- SCR latches on
	- Only way to restore the P-Type material in the gate is to interrupt cathode to anode current flow
		- Either placing a switch in series with SCR or shorting cathode to anode
			- ![[Pasted image 20231220125709.png]] 
				- When SCR is off, it remains off
	- Transistor reference books list the value as Trigger current
		- Same as ouput current

--- 

- Based on $I_g$ and $I_a$ 
	- Applying a positivevoltage to the input circuit establishes gate current flow
		- ![[Pasted image 20231220173017.png]] 
		- causes gate material to vanish
	- +DC supplying forward bias, SCR turns on producing $I_a$ 
		- ![[Pasted image 20231220173221.png]] 
	- When $I_g$ is removed SCR remains on
		- If $I_a$ is small, SCR will immediately turn off
	- The minimum $I_a$ to sustain current flow is called a ==Holding current== ($I_h$) and found in transistor reference books
	- Reset circuit is used to stop $I_a$ or reduce $I_a$ to less than $I_h$ 
	- ![[Pasted image 20231220174119.png]] 
		- $S_1$ open, $C_1$ charges towards the voltage equal to the voltage drop of $R_L$ 
	- ![[Pasted image 20231220174900.png]] 
		- $S_1$ closed, $C_1$ is placed in parallel with $SCR_1$ 
		- Briefly applying reverse bias voltage across $SCR_1$ 
			- Long enough to turn the circuit off
	- ![[Pasted image 20231220175258.png]] 
		- After $C_1$ discharges; it charges in the opposite direction
	- ![[Pasted image 20231220175406.png]] 
		- Open again, $C_1$ discharges through $R_1$ and $R_L$ and remains uncharged until input is applied again

## SCR in DC Operation

- Called trigger circuits
- Controls the application of power to the load
- ![[Pasted image 20231220161501.png]] 
- Purpose to apply power to $R_L$ using SCR as a switch
- ![[Pasted image 20231220161730.png]] 
	- Input applies gate current to turn on
- ![[Pasted image 20231220161757.png]] 
	- Reset circuit turns SCR off
- +DC forward biases the SCR
	- When on; anode current ($I_a$) flows through the load

## SCR in AC Operation 

- Called power control circuits
- Rectifies and controls the amount of power supplied to the load
- ![[Pasted image 20231221140324.png]] 
- 
