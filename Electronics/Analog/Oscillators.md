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
		- When an AC voltage is applied across the plates of a crystal it vibrates. 
			- This is the *Piezoelectric effect*
	- Since the common emitter is an inverted output, the feedback is applied to the bottom of the crystal
- ![[Pasted image 20231206163446.png]] 

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

### Hartley Oscillators

- ![[Pasted image 20231206165157.png]] 
	- Adds regenerative feedback to the LC oscillator to compensate for losses due to the flywheel effect
		- **Flywheel effect**: Transfer of energy back and forth between capacitor and inductor
			- This transfer of energy causes losses that must be counteracted by applying enough energy to sustain oscillations
	- Regenerative feedback is usually half the initial waveform or less
	- Two inductors are used to reduce the amount of feedback to the amplifiers input
		- prevents overdriving the amplifier
	- $L_2$ and $C_1$ develops the feedback circuit
	- $L_1$ and $C_1$ 