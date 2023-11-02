---
banner: Source/10/Selection_026.png
---
- The circuit effect on the conductor and capacitor cancel each other
	- ![[Pasted image 20231026114907.png]]
- $X_L = X_C$
	- They cancel in both series and parrallel
	- No reactance, so theyre purely resistive

# Series

- $X_L>X_C$ 
	- $X_L$ eliminates $X_C$ and the circuit becomes inductive
- $X_C>X_L$
	- $X_C$ eliminates $X_L$ and the circuit becomes capacitive

## Solve for Reactance

- [[RC Circuits]]
- [[RC Parallel Circuits]]
- [[RL Series Circuits]]
- [[RL Parallel Circuits]]


## Solve for Impedence

- $Z_T=\sqrt{R^2+({X_L}-{X_C})^2}$

## Solve for Current

- $I_T=\frac {V_A}{Z_T}$ 

## Solve for Voltage Drops

- $Voltage ,\ Drop=I_T*R$
- $Voltage ,\ Drop=I_T*X_C$
- $Voltage ,\ Drop=I_T*X_L$

## Solve Voltage Applied

- $V_A=\sqrt{{V_R}^2+({V_L}-{V_C})^2}$


# Parallel
- $X_L>X_C$
	- Current in $X_C$ is larger and cancels the current developed in $X_L$
		- The circuit is capacitive
- $X_L<X_C$
	- Current in $X_L$ is larger and cancels the current developed in $X_C$.
		- The circuit is inductive
- The branch with the highest current determines the type of circuit 

## Solve for reactance

- [[RC Circuits]]
- [[RC Parallel Circuits]]
- [[RL Series Circuits]]
- [[RL Parallel Circuits]]

## Solve for Impedence

- $X_T=\frac {X_L*X_C}{X_L-X_C}$  

- $Z_T=\frac {R*X_{T}}{\sqrt {R^2+{X_{T}}^2}}$ 

### Using the reciprocal formula

- $Z_T=\frac {1}{\sqrt {(\frac {1}{R})^2+(\frac{1}{X_L}-\frac{1}{X_C})^2}}$

## Solve for Current

- $I_T=\frac {V_A}{Z_T}$ 

### Solve for Current in Each Branch

- $I_{Branch}=\frac {V_A}{R \, or \, X}$

### Calculate total Current

- $I_T=\sqrt{{I_R}^2+(I_L-I_C)^2}$

# Troubleshooting
- Good resistor reads measured value
- Good inductor reads a low ohm
- Good capacitor reads infinity

- Open Inductor reads infinity
- Open resistor reads infinity

# Bandwidth

