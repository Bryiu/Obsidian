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
 

## Programmable Unijunction Transistors

![[Pasted image 20231228174720.png]] 

- Part of the Thyristor family; Performing a similar function as the UJT
	- **Thyristor**: Four layer semiconducting device similar to a diode, with the exception of an external terminal. Conducts as long as a sufficient current is present. Used in high current applications. #definition 
- Can be used as a relaxation oscilator, where output is a sawtooth and pulse waveform. Frequency determined by $R_1$ and $C_1$ value
	- **Relaxation Oscillator**: Produces oscillations by slowly charging a capacitor and discharging it. Output is usually a sawtooth #definition 
	- ![[Pasted image 20231228175058.png]] 
- Also used as a bistable multivibrator, element switch, level detector, or frequency divider. 
	- Essentially triggering SCR's
- **Intrinsic Standoff Ratio**: Sets the firing voltage ($V_p$). Small ratio variations produce large oscillator frequency variations #definition 
	- Can be overcome with PUT
- ![[Pasted image 20231228182241.png]] 
	- In the PUT, the ratio is programmed with external resistors. 
		- Makes it possible to build a circuit that oscillates very near the design frequency
	  
	  


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
- Does not have a reset circuit
- Rectifies and controls the amount of power supplied to the load
- ![[Pasted image 20231221140324.png]] 
- ![[Pasted image 20231221141825.png]] 
	- power control circuit
- ![[Pasted image 20231221141906.png]] 
	- $R_1$ = Cathode bias
	- $C_1,C_2$ DC blocking capacitors
- ![[Pasted image 20231221144802.png]] 
	- Once the SCR is reverse biased, $I_a$ stops
		- This action turns off the SCR
- ![[Pasted image 20231221144928.png]] 
	- Forward bias turns on the SCR
- Operation of the circuit is based on controlling the amount of time that AC voltage is sent to the load
	- ![[Pasted image 20231221145217.png]] 
		- 50% maximum
			- Gate also controls when the SCR turns on during that time that the SCR is forward biased
				- ![[Pasted image 20231221145326.png]] 
					- If gate is on for only half of the cycle 25% efficiency
	- By controlling the gate voltage (gate current), the time that the load receives voltage is controlled
- ![[Pasted image 20231221150106.png]] 
	- At 0$\degree$ of the input, signal across Load and SCR
- ![[Pasted image 20231221150152.png]] 
	- SCR forward biased, no current through load
		- acts as an open component
- ![[Pasted image 20231221150249.png]] 
	- At 90$\degree$ $I_g$ large enough to turn on SCR
	- Between 0$\degree$ and 90$\degree$ called ==fire angle== 
- ![[Pasted image 20231221150451.png]] 
	- From 90$\degree$ to 180$\degree$ SCR is conducting
		- Called ==Conduction Angle== 
	- SCR is a short circuit
	- $180\degree = Fire \, angle + Conduction \, Angle$ #formula 
- ![[Pasted image 20231221150711.png]] 
	- SCR is reversed biased and current does not flow
	- SCR reset automatically
	- $P=\frac {E^2}{R_L}$ #formula  
- ![[Pasted image 20231221150918.png]] 
	- If $R_2$ is changed so the gate current will not turn on the SCR until after 90$\degree$, less power
		- ![[Pasted image 20231221151128.png]] 
	- If turned on between 0 and 90, more power
		- ![[Pasted image 20231221151218.png]] 
		- ![[Pasted image 20231221151254.png]] 
- Approximate average voltage
	- $E_{rms}$ is the value on the input sine wave
	- C is number of degrees of the sine wave that SCR controls
	- $E_{avg}=E_{rms}*\frac {C\degree}{360\degree }$ #formula 
		- Where $E_{rms}=0.707*E_{peak}$ 
	- $P=\frac {E^2}{R}$ 

## Troubleshooting

- A shorted SCR is on all the time
	- In DC you will not be able to turn the power off to the load
	- In AC there would not be any rectifying action or power control of the load
- Voltage measurements to determine if operating correctly
	- ![[Pasted image 20231225094410.png]] 
- To verify if SCR is good or bad, an analog ohmmeter is required to completely test the device.
	- Lowest range should be used
		- Digital meter lacks sufficient power to forward bias the SCR
			- Can only confirm shorted conditions
			- Diode test will not reliably test either
	- Check the Resistance forward and reversed without gate signal
		- Should be high in both directions
		- If resistance is low; shorted SCR
	- ![[Pasted image 20231227153650.png]] 
	- ![[Pasted image 20231227155233.png]] (Black is positive. idk why tf they did that)
		- Placing a jumper between the anode to the gate
			- A positive voltage applied to the anode will also be applied to the gate, forward biasing the SCR
		- When connected with a forward bias, there should be a low reading
			- High reading means its open or too high of a range setting
		- With the multimeter connected, remove the jumper.
			- Reading should stay low; SCR remains on
		- Remove leads and retest.
			- Reading should go high

#### Checking an SCR Circuit

- Determine type (trigger or power control)
- Determine correct applied voltage and gate input signals
- Check SCR operation
- Check other components


## Triacs, Diacs, Four Layer Diodes

### Triacs 

- ![[Pasted image 20231227162921.png]] 
	- Triacs
		- ![[Pasted image 20231227164724.png]] 
		- Used for power control instead of simple resistance devices
		- Produce much less heat
		- Solid state component
		- Basic structure of a triac is two SCR's connected in reverse (anodes to cathodes) with gates connected
	- ![[Pasted image 20231227165145.png]] 
		- Doesnt let current flow from cathode to anode unless gate is triggered
			- Current flows from cathode to anode until voltage across anode and cathode drop below a certain level
			- Doesnt allow current to flow no matter what voltage is applied to the trigger
			- Power SCR's do not use the negative portion of the AC signal
	- ![[Pasted image 20231227171201.png]] 
		- Half wave SCR Phase shifters
		- Power reduced to 50% 
		- ![[Pasted image 20231227171309.png]] 
			- A single SCR can reduce power to 50%
			- Input power can be adjusted from half to 0%
		- ![[Pasted image 20231227172148.png]] 
			- Since Triac is two SCR's, it operates during both alternations of the sine wave
			- Allows power to be reduced from 100% to 0%
		- ![[Pasted image 20231227172420.png]] 
			- Triacs also used as high current switches
				- Mechanical switches would have high current jump between the contacts; damaging them
				- Triacs use a small voltage level can be applied with a mechanical switch to the gate to open the path


### Diac and Four Layer Diodes

- ![[Pasted image 20231227163150.png]] 
- ![[Pasted image 20231227172845.png]] 
	- Diac and 4 layer diode
		- Used as trigger devices to SCR's and Triacs
		- Better trigger control
		- Provide protection to trigger circuit
		- Will continue to conduct until the input voltage falls below a certain level
		- Four layer diodes normally used with SCR's since conduction is only required during one alternation
		- Diacs used with triacs
			- Limits the input current to the gate until a certain level has been reached
		- ![[Pasted image 20231228151901.png]] 
			- Power reducing circuits are normally connected directly to a power system
		- Diacs provide protection to the circuit
		- ![[Pasted image 20231228153555.png]] 

