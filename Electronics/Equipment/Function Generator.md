# Purpose

- The function generator is used to produce accurate AC Signals
	- With a known input, circuit values can be calculated, measured, and checked
	- Signals produced
		- Sine
		- Ramp
		- Square
		- Triangle
		- Pulse
	- The symmetry of the output signal is adjustable by changing the duty cycle of a signal
		- ![[Selection_035.png]]
	- Output signal can me ==modulated== 
		- AM or FM modulation using sine, square, or triangle

# Operation

![[Selection_036.png]]

## Frequency Section

- Selects the type of signal, frequency, amplitude, DC offset, CMOS level, and duty cycle of the output
- Two output and three input connectors for internal and external signals
	- ![[Selection_037.png]]
		- The VCG/MOD input is part of the Modulation section
- The function switches select the type of signal output
	- ![[Selection_038.png]]
- The Duty cycle (Symmetry) controls change the waveform
	- ![[Pasted image 20231017105550.png]]
		- For example, a triangle wave can be changed to a ramp
		- Square can be changed to a pulse, etc
- The Range buttons select the maximum frequency at the output.
	- Coarse and fine controls adjust the frequency to a value between the selected range button and the button of the next lowest value.
		- Output frequency is shown on the display
- On the display, the frequency is shown in kHz when the range buttons 20k and above are used
	- Mutliply the value shown on the display by 1000 Hz
- When the EXT CNTR INPUT is connected to an external circuit and the CNTR switch is set to EXT, the function generator's display show the measured frequency
	- 
## Modulation Section
## Sweep Section