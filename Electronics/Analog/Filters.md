[[RC Filters]]
[[RL Filters]]

# Intro

- Filters are to pass or reject frequencies that are passed through them
- ![[Pasted image 20240101170604.png]] 
- ![[Pasted image 20240101172038.png]] 
	- Passive filters are circuits that do not require any power for them to operate
		- Contain simple components like resistors, inductors, and capacitors
		- Disadvantage that it reduces the input signals amplitude
		- Disadvantage is components are very large in size
	- Active filters are circuits that require power to operate
		- Contain active components like op amps and transistors
		- Smaller in size
		- No loss of input signal amplitude
		- Same functions as passive filters
			- Pass and reject frequencies
			- Attenuate frequencies
		- Disadvantage is they require an input power to work
		- Disadvantage more difficult to design and analyze

## Inductive and Capacitive

- ![[Pasted image 20240102120743.png]] 
	- These components oppose or try to block current flow to some degree
		- Resistors offer resistance
			- Resistors value of resistance is not affected by frequency
		- Capacitors and Inductors are affected by the frequency of current and voltage
			- Amount of opposition is determined by the frequency of the current
			- ![[Pasted image 20240102121024.png]] 
				- An inductor has the least opposition to direct current and the most opposition to a current flow that has a very high frequency
					- Opposition that an inductor offers:
						- $X_L=2 \pi f L$ #formula 
							- $X_L$ represents ohms
					- As frequency of the input signal increases, the inductive resistance increases
						- ![[Pasted image 20240102122402.png]] 
					- Inductors cause current to lag applied voltage by 90 $\degree$ 
					- If an inductor is in series with the load, it passes low frequencies and blocks high frequencies
						- ![[Pasted image 20240102125400.png]] 
					- If an indcutor is in parallel with the load, it passes high frequencies and attenuates low frequencies
						- ![[Pasted image 20240102125450.png]] 
- ![[Pasted image 20240102123055.png]] 
	- An active filter simulates inductive reactance by using a feedback circuit and a capacitor
	- By sending feedback current through the capacitor a phase shift is accomplished
		- ![[Pasted image 20240102123330.png]] 
		- As input frequency increases; capacitive reactance decreases
			- ![[Pasted image 20240102123436.png]] 
			- $X_C=\frac{1}{2\pi f C}$ #formula 
				- $X_C$ is reactance in ohms
		- If a capacitor is in series with the load, it attenuates low frequencies and passes high frequencies
			- ![[Pasted image 20240102125527.png]] 
		- If a capacitor is in parallel with the load, it attenuates high frequencies and passes low frequencies
			- ![[Pasted image 20240102130050.png]] 


# High Pass

- Allow high frequencies to pass while attenuating low frequencies 
- ![[Pasted image 20240102130747.png]] 
- Capacitors are usually used over inductors in filters because they absorb less power
- ![[Pasted image 20240102131705.png]] 
- ![[Pasted image 20240103105415.png]] 
- ![[Pasted image 20240103110216.png]] 
	- L-Filter
		- At low frequencies, the low impedance of the coil provides a ground path for signal current. Attenuating the signal
		- At high frequencies, the coil has a high impedance allowing the signal currents to pass to the output
	- T-Filter
		- Works the same way as an L-Filter
		- ![[Pasted image 20240103123619.png]] 
	- $\pi$-Filter
		- I guess no in depth lolz
- ![[Pasted image 20240103123754.png]] 
	- Most common and simplest high pass is the RC filter
	- Has capacitor in series with the load 
		- Parallel resistor
	- Low frequencies capacitor acts like an open circuit
	- High frequencies capacitor has very low reactance
		- Allows all the current to flow through to the output
- $f_c=\frac{1}{2 \pi RC}$ #formula 

# Low Pass

- Allow low frequencies to pass; attenuating high frequencies
- ![[Pasted image 20240102132519.png]] 
	- A simple low pass filter
- ![[Pasted image 20240102132540.png]] 
- Resistors do not perform any filtering action; they are used to help capacitors filter properly
- ![[Pasted image 20240103134840.png]] 
	- Inverted L-Filter
		- The coil has a low impedance at low frequencies and a high impedance at high frequencies
			- The low impedance of the coil and high impedance of the capacitor provide a path for signal current, producing an output voltage
		- At high frequencies the coil has a high impedance and the capacitor has a low impedance, passing the small amount of current from the inductor to ground
		- Disadvantage is the amount of power that is absorbed by the inductor
- ![[Pasted image 20240103140339.png]] 
	- T-Filter 
		- Inductors have a low impedance at low frequencies and a high impedance at high frequencies
		- Capacitors have a high impedance at low frequencies and a high impedance at high frequencies
		- This filter type prevents power loss
- ![[Pasted image 20240103141103.png]] 
	- $\pi$-Type Filter
		- Improved filtering and less inductor loss than the T-Type filter
- ![[Pasted image 20240103141208.png]] 
	- RC-Filter
		- Simplest and most common type of low pass filter
		- $X_c=\frac {1}{2 \pi f C}$ #formula 
			- Cutoff occurs when $X_c=R$ 
		- $\frac {1}{2 \pi R C}=f$ #formula 



# Band Pass

- Combo of High and Low pass filters
- Only allow a band of frequencies to be passed
- ![[Pasted image 20240102133057.png]] 
- ![[Pasted image 20240102133738.png]] 
  
  
  

# Band Reject, Band Stop, or Notch

- ![[Pasted image 20240102134002.png]] 
	- High pass and low pass are connected in parallel to each other
- ![[Pasted image 20240102134558.png]] 
