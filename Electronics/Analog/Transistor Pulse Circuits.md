# Intro

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