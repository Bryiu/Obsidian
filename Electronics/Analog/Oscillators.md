# Intro

- Oscillators produce sinusoidal and non-sinusoidal waveforms
- Sine wave Oscillators contain two circuits
	- Feedback circuits
	- Amplifier circuits

## Sine Wave Oscillators

![[Pasted image 20231206130339.png]] 

- Convert DC to sinusoidal AC energy
- Frequencies range from a few hertz to tens of gigahertz
- Sine Wave Oscillators are transistor amplifiers with a few extra components that sample their output signal, returning it as their input
- Feedback circuit is the output return
	- Only used to determine the frequency of the output signal
	- maintains the feedback circuit output at a given frequency
	- ensures the applied input signal is the correct phase to produce output
	- **Negative Feedback**: *Two signals that would cancel each other if the output connects directly to the input*
		- ![[Pasted image 20231206132152.png]] 
		- Common emitter amplifiers
	- **Positive Feedback**: *Ensures input phase to the amplifier is correct*
		- ![[Pasted image 20231206133519.png]] 
		- Common collector and common base amplifiers
- Oscillators are classified according to the type of amplifier circuit used
	- Common emitter, collector, or base
	- Class A, B, C operation
- The feedback determines the type of oscillator
	- LC
	- RC
	- Crystal

### Class A Common emitter Amplifier (LC Oscillator)

[[LCR Circuits]]

- ![[Pasted image 20231206143701.png]] 
- ![[Pasted image 20231206144338.png]] 
	- $L_1$ and $C_1$ form a tank/resonant circuit. The frequency is dependent on the component values
- ![[Pasted image 20231206144620.png]] 
	- Since the common emitter has an inverted output, the feedback is applied to the bottom of the tank
		- If the output is in phase; its applied to the top
			- ![[Pasted image 20231206144809.png]] 
- The circuit changes $+V_{cc}$ into a sine wave output
	- ![[Pasted image 20231206150230.png]] 

### Class A Common Emitter Amplifier (RC)

- ![[Pasted image 20231206151445.png]]
	- The feedback circuit forms a phase shift circuit
		- A capacitor shifts the phase of signals 90$\degree$ with no resistance
			- Resistance in the circuit causes shifts less than 90$\degree$ 
			- More capacitors increases phase shifts
		- With the resistors, the phase shift per capacitor is 60$\degree$ 
			- The value of the components are such that only one frequency is shifted 180$\degree$ 
			- All other shifts of less than 180$\degree$ are cancelled out by *degenerative feedback*
- The circuit changes $+V_{cc}$ into a sine wave
	- ![[Pasted image 20231206153247.png]] 

### Class A Common Emitter Amplifier (Crystal)

- ![[Pasted image 20231206155540.png]]
	- The crystal operates similar to a tank circuit. Frequency depends on how the crystal is made
		- When an AC voltage is applied across the plates of a crystal it vibrates and produce AC voltage at the output
			- This is the *Piezoelectric effect*
				- The vibrations are equal to the frequency of the AC voltage
	- Since the common emitter is an inverted output, the feedback is applied to the bottom of the crystal
- ![[Pasted image 20231206163446.png]] 
- ![[Pasted image 20231209140922.png]] 
	- The resonant frequency is determined by the cut of crystal and the thickness of the slab
		- $f=\frac {K}{t}$ #formula 
		- ![[Pasted image 20231209141457.png]] 
			- No need to calculate
	- Has a small amount of capacitance ($C_m$) 
	- ![[Pasted image 20231209142558.png]] 
		- $R_1$ is the gate return resistor. 
			- It supplies the ground reference for the gate (0 volt)
		- An AC signal at the gate will increase and decrease the drain current
		- $R_2$ provides the self bias
		- $L_1$ is an RF choke that appears as an open to AC
			- Isolates the supply from the circuit while functioning as a drain load resistor for VDD
		- $C_2$ is a coupling capacitor
		- $R_3$ is the output load resistor, varies the amplitude
		- When $V_{DD}$ is applied the crystal begins to vibrate
		- The crystal inverts the signal
			- ![[Pasted image 20231209163154.png]] 
		- The mounting capacitance of the crystal ($C_m$) and $C_1$ form a voltage divider to limit the amount of feedback 
- Correct operation is determined by comparing the value of the crystal with the measured frequency
	- Frequency of crystal operators does not drift
		- The smaller the drift, the more stable
												

### Operation

- With the circuit turned off, the input and output signals to the amplifier are 0
	- ![[Pasted image 20231206135210.png]] 
- When DC is applied, the amplifier circuit sets up normal bias voltages to the transistor
	- ![[Pasted image 20231206135303.png]] 
- Since there is no input, the amplifier amplifies the multi-frequency noise that is produced by the resistors
	- ![[Pasted image 20231206140551.png]] 
- The noise is fed back into the feedback circuit
- The circuit only allows one frequency to pass into the amplifiers input
- The amplifier no longer amplifies noise; it amplifies the output of the feedback circuit
- The sine wave output is applied to the feedback circuit; shifted 180$\degree$ if necessary
- The output signal is limited in two ways
	- Transistors have saturation and cutoff points. This is equivalent to reducing the voltage gain
	- Losses in the feedback circuit reduce the input signal to the amp


## LC 
### Hartley Oscillators

- ![[Pasted image 20231206165157.png]] 
	- Adds regenerative feedback to the LC oscillator to compensate for losses due to the flywheel effect
		- **Flywheel effect**: Transfer of energy back and forth between capacitor and inductor
			- This transfer of energy causes losses that must be counteracted by applying enough energy to sustain oscillations
	- Regenerative feedback is usually half the initial waveform or less
	- Two inductors are used to reduce the amount of feedback to the amplifiers input
		- prevents overdriving the amplifier
	- $L_2$ and $C_1$ develops the feedback circuit
	- $L_1$ and $C_1$ develop the output to $Q_1$ 
- ![[Pasted image 20231207140601.png]] 
	- to check for normal operation calculate the frequency of the resonant circuit
		- $f=\frac {1}{2 \pi \sqrt {LC}}$ #formula 
	- Then measure the output frequency with an oscilloscope or frequency counter
- ![[Pasted image 20231207141331.png]] 
	- This is also a Hartley Oscillator
	- Uses collector feedback biasing
	- fewer components are used
	- no temperature stabilization
	- taking the output from the collector of an amp biased class B or C produces a distorted output waveform
- ![[Pasted image 20231207142738.png]] 
	- This is also a Hartley 
	- input to the feedback from the emitter
	- the in phase condition because $L_1$ is in series to the input and output of the amp
		- ![[Pasted image 20231207142959.png]] 
	- ![[Pasted image 20231207143101.png]]
		- Collector signal is inverted and only negative portion present
			- operating at class B
- To check if operating correctly
	- $f=\frac {1}{2 \pi \sqrt {L_t C}}$ #formula 

### Colpitts Oscillator

- ![[Pasted image 20231207145559.png]]  
	- $f=\frac {1}{2 \pi \sqrt {L C_t}}$ #formula 
		- Product over sum for capacitors
- ![[Pasted image 20231207150916.png]] 
	- C1 and C2 reduce the amount of amplitude at the input
- ![[Pasted image 20231207150952.png]] 
- ![[Pasted image 20231207151136.png]] 

## RC Phase Shift Oscillators

- ![[Pasted image 20231208164746.png]]
	- ![[Pasted image 20231208164840.png]] 
		- $Q_1$ is the oscillator amp and $Q_2$ is a buffer amp
			- Buffer amp: Placed between stages to isolate the first stage from the 2nd
				- The buffer amp increases current, not voltage, output from $Q_1$ collector
		- $Q_1$ output is routed through the feedback circuit to the base of $Q_1$ 
			- ![[Pasted image 20231208171715.png]] 
			- This produces oscillations at one frequency
			- $f=\frac {1}{2 \pi ((R_1*C_1)+(R_2*C_2)+(R_3*C_3))}$ #formula 
				- if $R_1$-$R_3$ and $C_1$-$C_3$ have the same values:
					- $f=\frac {1}{3(2 \pi R C)}$ 
						- 2.45 (sqrt of 6) is more accurate; 3 is "good enough"
						- R is the value of 1 resistor
						- C is the value of 1 capacitor
			- Changing the value of any component in the feedback circuit changes the oscillation frequency
			- Each RC network is called a lead network and produces a phase shift
			- Ideally if the circuit values are the same, each network shifts the frequency 60$\degree$ 
			- Since $Q_1$ produces a 180$\degree$ phase shift; feedback and $Q_1$ produce a full 360$\degree$ phase shift
	- Positive Regenerative feedback circuit
	- To check for normal operation calculate feedback
		- ![[Pasted image 20231208173848.png]] 
		- $f=\frac {0.053}{RC}$ #formula 

## Sine Wave Oscillator Troubleshooting

![[Pasted image 20231210163225.png]] 

- Usually, an interruption anywhere in the oscillator results in no output
- Once measured output is incorrect; measure supply voltage
- Inspect amp 
	- To check the transistor in the amp, disconnect $V_{cc}$ and perform continuity checks via diode check
- Check Feedback circuit
	- If you measure 0 ohms or infinite ohms across the resonant circuit, its faulted
	- measuring across each component determines open or short
		- Open capacitors can only be detected by testing with an RCL bridge or replacing the capacitor and rechecking
>[!Important]
>Capacitors measure infinite DC resistance
- Turn on $V_{cc}$ and check output circuit
	- Measuring signal on the output side of the capacitor will determine if its faulted
	- measure signal on the potentiometer to determine if its faulted
		- Resistance to confirm open or short
![[Pasted image 20231210172216.png]] 
#### Part II

- Measure output signal to determine if working correctly
- In crystal ocillators, all the components in the feedback can be checked as an RC phase shift oscillator, except the crystal
	- To check crystal, replace it and check for normal operation
- If a transistor is in the output circuit, it has already been checked
	- Resistance measurements will isolate the fault to a component

## Sawtooth Generators

- Changes a square wave input to a sawtooth
- Does not use feedback
- The square wave is clamped, or held, at a dc level by $C_1$ and the base to collector junction of $Q_1$ 
	- ![[Pasted image 20231211135745.png]] 
- The AC square wave input becomes a DC square wave
	- ![[Pasted image 20231211135915.png]] 
		- When the DC square wave goes positive, $Q_1$ is reversed biased and does not conduct
		- With $Q_1$ off, $C_2$ begins to charge through $R_2$ 
			- ![[Pasted image 20231211142325.png]] 
		- When the DC square wave drops to 0, $Q_1$ is forward biased and conducts
			- When $Q_1$ conducts, it creates a low resistance path for $C_2$ to discharge through. 
				- ![[Pasted image 20231211143322.png]]
	- Frequency of output is determined by frequency of input
	- How straight the output is is also determined by input frequency
	- Low input frequency allows the capacitor to charge for a longer period of time
		- ![[Pasted image 20231211143515.png]] 
		- Because the capacitor charges longer, the output amplitude is greater
	- High input frequency; short charge time. Less amplitude
		- $V_{cc}$ only affects the output amplitude
		- ![[Pasted image 20231211144912.png]] 
	- Output linearity and frequency are unaffected by the amount of $V_{cc}$ 
	- The RC time constant of $R_2$ and $C_2$ will affect the output
		- long time constant = linear
			- linear output and low amplitude
			- affects it the same way as high frequency
		- short TC non linear and high amplitude
			- affects the same way low frequency input does
![[Pasted image 20231211150100.png]] 

## Blocking Oscillators

- Change DC into short rectangular pulses that can be used as timing pulses to trigger other circuits
- An Oscillator that cuts off its own oscillations at a predetermined time

### Free Running Blocking Oscillators

![[Pasted image 20231212142614.png]] 
- $C_1$ is not used in free-running operation
- When $V_{cc}$ is applied, the NPN starts to conduct
- Collector current flows trough the primary winding of $T_1$; inducing voltage to the secondary
	- ![[Pasted image 20231212143030.png]] 
- The voltage in the secondary is limited by $R_3$ and coupled through $C_2$ to the base of $Q_1$ 
	- Drives $Q_1$ into saturation
	- ![[Pasted image 20231212143233.png]] 
- $Q_1$ reaches saturation, collector current stops increasing. No change in current, no voltage is coupled through $T_1$ 
- $C_2$ discharges through $R_1,R_2$ 
	- ![[Pasted image 20231212143454.png]] 
- Makes $Q_1$ base negative into cutoff for a long time. 
	- $D_1$ prevents inductive kickback
		- **Inductive Kickback**: *A spike of very high voltage resulting from the almost instantaneous collapse of the magnetic field around an inductor when voltage is removed*
- When $C_2$ is almost discharged, reverse bias is removed from the base of $Q_1$ and begins to conduct again
- When $Q_1$ is at cutoff, collector voltage is at $V_{cc}$ 
	- ![[Pasted image 20231212144954.png]] 
- When $Q_1$ is saturated for a short time, collector voltage drops to near 0
- $V_{cc}$ determines the amplitude of the pulses
- These components determine width of the output pulse
	- ![[Pasted image 20231212145439.png]] 
	  

### Triggered Blocking Oscillators

- Cannot free run
	- No forward bias on the base of $Q_1$ 
- $Q_1$ cannot conduct until an input pulse of sufficient amplitude is coupled through $C_1$ for forward bias 
	- ![[Pasted image 20231212145826.png]] 
- When $Q_1$ conducts
	- ![[Pasted image 20231212145911.png]] 
- $Q_1$ becomes saturated and voltage on the secondary stops
- $C_2$ discharges and reverse biases $Q_1$; stopping collector current
	- ![[Pasted image 20231212150222.png]] 
- $Q_1$ must receive another trigger pulse to begin conducting again
	- Pulse must not arrive before $C_2$ is done discharging or no output occurs
		- Called recovery time
- Purpose to improve the shape of input pulses
	- can also clean up signals when precise timing pulses are required
- 1 input 1 output

### Troubleshooting

#### Blocking Oscillator

- Measure the output with an oscilloscope and vary and frequency determining components
- Check inputs
- Check transistor
- Check resistances