# Intro

- Used as Non-Inverting Amp
	- Inverting Amp
	- Differential Amp
	- Summing Amp
- Replaced Transistor Amplifiers except for high frequency and power amps
- ![[Pasted image 20231230140627.png]] 
	- Contain three circuits
	- Use two inputs to determine the output
	- Labeled with a positive and a negative sign
- Packaged into an IC or integrated circuit
	- Made from P-type and N-type material

# Non inverting Amp

	
- The positive input is called the **Non inverting** input
	- Grounding the non inverting input produces an inverting amp
		- Input and output are out of phase
			- ![[Pasted image 20231230155202.png]] 
				- The output is equal to negative input minus zero (ground)
				- The output signal will be inverted





# Inverting Amp

-  The negative input is called the **Inverting** input
	- Grounding the inverting input produces a non inverting amp
		- Input and output are in phase
			- ![[Pasted image 20231230155050.png]] 
				- Output is equal to positive input minus zero



# Differential Amp

- Using both inputs produces a differential amplifier
	- Output is the difference between inputs
	- ![[Pasted image 20231230142613.png]] 
		- ![[Pasted image 20231230154407.png]] 
			- The output of the differential amplifier is applied to the common collector amp
				- The output is the difference between the (+) and (-) inputs
		- ![[Pasted image 20231230161532.png]] 
			- The common collector amp is used to isolate the differential amp from the push-pull amp
				- Common collector amps have high impedance. 
					- Ensures that the differential amp is not loaded down by the push-pull amp
			- ![[Pasted image 20231230164326.png]] 
				- Output of the common collector amp
		- ![[Pasted image 20231230164403.png]] 
			- Most of the amplification is in the push-pull amp.
				- Power gain is high
--- 

- ![[Pasted image 20231230171358.png]] 
	- Simple op amp circuit
	- Non-inverting input to the base of $Q_1$
	- Inverting input to the base of $Q_2$ 
	- Both emitters connected to negative voltage
	- Output taken from the collector of $Q_2$ 
	- Depending on inputs, $Q_1$ is either a common collector or a common base amp
	- $Q_2$ is either a common base or a common emitter amp
	- ![[Pasted image 20231230174236.png]] 
		- Inverting input is grounded when differential amp is used as a non inverting amp
		- $Q_1$ drives $Q_2$ 
		- $Q_1$ has the non inverting applied to its base. 
			- Emitter provides the output, $Q_1$ is a common collector amp
				- Doesnt invert the signal
				- gain of 1
			- Output applied to the emitter of $Q_2$ 
		- $Q_2$ output from the collector
			- Common base amp
				- Doesnt invert the signal
				- High voltage gain
	- ![[Pasted image 20231230181240.png]] 
		- Non inverting input is grounded when the diff amp is used as an inverting amp
		- $Q_2$ drives $Q_1$ 
		- Inverting input applied to the base of $Q_2$ 
			- Collector is the output
				- Signal is out of phase with input 
				- ![[Pasted image 20231230181438.png]] 
		- $Q_1$ is a common base
			- Adds to the voltage gain of output $Q_2$ 
			- With non inverting input grounded, inverted input is amplified
	- ![[Pasted image 20231230183848.png]] 
		- When both inputs are used, output is the difference between the inputs
		- Can operate in two modes; Difference Mode or Common Mode
			- **Difference Mode** 
				- Operates in this mode when the inputs are 180$\degree$ out of phase
					- In the positive phase on the positive input; produces a positive output
					- In the positive phase on the negative input; produces a positive output
					- The two output signals combine
						- Since they are in phase the output is larger
					- The output is the difference between the input signals. If they're equal, the output is twice the gain of a single input
			- **Common Mode** 
				- Operates when inputs are in phase
				- Positive signal on the + input produces a positive output
				- Positive signal on the - input produces a negative output
				- When they combine the output is smaller or flat looking
					- If both outputs are equal, the output is zero
	- 


# Summing Amp

- ![[Pasted image 20231230145409.png]] 
	- Connecting several signals to the inverting input produces a summing amp
	- The output is the algebraic inverted sum of the inputs
- ![[Pasted image 20231230193151.png]] 


