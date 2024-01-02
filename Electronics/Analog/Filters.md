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

# Low Pass

- Allow low frequencies to pass; attenuating high frequencies
- ![[Pasted image 20240102132519.png]] 
	- A simple low pass filter
- ![[Pasted image 20240102132540.png]] 
- Resistors do not perform any filtering action; they are used to help capacitors filter properly



# Band Pass

- Combo of High and Low pass filters
- Only allow a band of frequencies to be passed
- ![[Pasted image 20240102133057.png]] 
- ![[Pasted image 20240102133738.png]] 
  
  
  

# Band Reject, Band Stop, or Notch

- ![[Pasted image 20240102134002.png]] 
	- High pass and low pass are connected in parallel to each other
- ![[Pasted image 20240102134558.png]] 
