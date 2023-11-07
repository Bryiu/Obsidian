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

# Diode Limiters

## Function
### Standard
![[Pasted image 20231107104554.png]] 

- Purpose is to limit the amplitude of the signal
- ==Forward Bias== acts like a short circuit
- ==Reverse Biased== acts like an open circuit



## Series

![[Pasted image 20231107113209.png]] 

- ==Forward Biased== output signal is developed across the resistor
	- Negative alternation is eliminated *Negative Limiter*
- ==Reversed Biased== positive alternation is eliminated *Positive Limiter*

## Parallel

![[Pasted image 20231107114214.png]] 

- Works opposite of the series limiter
- ==Forward Biased== output is shunted to the ground
	- Positive Limiter
- ==Reversed Biased== Signal is passed to the output
	- Becomes a negative limiter

## Added Bias
- Bias voltage changes the reverse bias point for the *Series Limiter* and the forward bias point for the *Parallel Limiter*
- When bias is added, partial alternations can be eliminated
	- ==Positive series or parallel *Positive Bias*== raises the limit point from $0V$ to the bias level
		- ![[Pasted image 20231107121135.png]] 
	- ==Positive Series or Positive Parallel *Negative Bias*== lowers the limit point from $0V$ to the bias level
		- ![[Pasted image 20231107122122.png]] 
	- ==Negative Series or Parallel *Positive Bias*== raises the limit point from $0V$ to the bias limit
		- ![[Pasted image 20231107124948.png]] 
	- ==Negative Series or Parallel *Negative Bias*== lowers the Limit point from $0V$ to the bias level
		- ![[Pasted image 20231107124534.png]] 

### Combining Alterations

- Combining a biased positive parallel limiter and a biased negative parallel limiter changes both alternations
	- ![[Pasted image 20231107125613.png]] 

# Diode Clampers
- ![[Pasted image 20231107133142.png]] 
- Clampers change the AC voltage level by adding DC Voltage
	- Used when AC needs to ride on a DC level

## Positive Clampers

>[!Note]
>==Forward based== diode - Low resistance allows current to flow through the diode. Result is a fast time constant
>==Reversed Biased== diode - High resistance allows current flow through the resistor. Result is a slow time constant

- $TC=C*R$


- ![[Pasted image 20231107140353.png]] 
- Positive Clampers Pass a positive DC signal

## Negative Clampers

- ![[Pasted image 20231107144245.png]] 

- Functions the same as Positive, but passes negative voltage
- Points towards the ground

## Adding Bias

- Adding a positive Bias raises the output voltage DC level
	- Positive Bias on a negative clamper raises the output voltage DC level
- Negative Bias lowers the output voltage DC level
	- Negative bias on a negative clamper lowers the output voltage DC level

- ![[Pasted image 20231107144732.png]] 
- 