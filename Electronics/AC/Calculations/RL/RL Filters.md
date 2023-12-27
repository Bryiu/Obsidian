# Types of filters

- RL filters block out unwanted frequencies and pass others
- Only differece between the two filters is where the output is taken
- They come in two different configurations
	- High pass
		- passes high frequencies and blocks low
		- Large inductive reactance
		- input signal is dropped across the inductor reaches the output
		- Resistor is before the inductor
		- small inductive reactance at low frequencies
		- 
	- Low pass
		- passes low frequencies and blocks high
		- Input is applied in series with the inductor
			- Resistor is after inductor
		- output is taken from across the resistor
		- the inductor has a low inductive reactance
			- because a small $X_L$ doesnt drop much voltage, most of the input signal reaches the resistor where the output is taken

# Frequency Cutoff

- Signal is blocked at ==HALF POWER==

 >[!Important]
 >Cutoff frequency or $f_{CO}$ is 0.707 of the maximum voltage
 >*aka RMS*
 
- The $f_{CO}$ will pass through anything before ==HALF POWER== or 0.707 times the maximum voltage 
	- everything below $f_{CO}$ is attenuated (blocked)

>[!Warning] NOT VERY ACCURATE
> $f_{CO}=\frac {R}{2 \pi L}$

# Troubleshooting
- No need to calculate $X_L,Z,I,V_R,and\, V_L$
- Compare $f_{CO}$ measured to the planned 