# Intro

- Diodes belong to a group of components called Solid-State devices
- The purpose of a diode is to allow current in one direction and stop current in another
	- Like a check valve

![[Pasted image 20231105183545.png]] 

- The arrow represents the positive side
	- aka Anode (A)
- The bar represents the negative side
	- aka the Cathode (K)
- The ==Zener Diode== are designed to regulate voltage

![[Pasted image 20231105184041.png]] 
- ==Rectifiers== are used to convert AC voltage to pulsating DC
- ==Limiters== are useful in signal shaping
	- Remove signal voltages above or below a specific level
- ==Clampers== add a DC voltage to the input signal


## Identification

- ![[Pasted image 20231105183742.png]] 

# Materials

# N-Type

- Doped with atoms that have 5 electrons in the valence shell
	- The free electron can can conduct current and move in any direction
- Also called a cathode (K)
- Still electrically neutral because the protons and nutrons are equal

# P-Type

- Doped with atoms that have 3 electrons in the valence shell
	- The missing electrons form a hole that can accept an electron
- Called the Anode

# Function

- The center of the semiconductor is the PN Junction
	- Free electrons and holes combine in the center
		- This is called ==Recombination== 
	- Free electrons move to the holes in the P-Type material, creating ==negative ions== near the PN junction of the P-type material
	- The loss of electrons from the N-type material creates ==positive ions== near the PN Junction in the N-Type material
	- ![[Pasted image 20231106120734.png]] 
		- This action forms a barrier to the PN Junction called the Depletion region
		- ![[Pasted image 20231106121033.png]] 
			- Prevents current flow
	- An external voltage applied to the diode affects the barrier
		- Called ==Bias== 
			- Forward Bias is Negative to N; Positive to P
			- Reverse Bias is Negative to P; Positive to N
			- ![[Pasted image 20231106122509.png]] 
				- This widens the barrier
			- ==Knee voltage or Offset voltage== is the minimum voltage for the diode to conduct
				- ![[Pasted image 20231106125523.png]] 

# Calculations

- $V_T = (Knee \, Voltage)-(Applied \, Voltage)$
- $I_T=\frac {V_T}{R}$ 

