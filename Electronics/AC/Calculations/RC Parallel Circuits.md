- Only need to consider the phase relationships of the resistor and capacitor
- Total capacitance of a parallel circuit is always greater than the largest capacitor.
	- Placing capacitors in parallel has the same effect as increasing the size of the plates
- ![[Pasted image 20231022153432.png]] 
	- The junctions of $C_1$ and $C_2$ are essentially the same point

# Calculating Total Capacitance

- $C_T$ is equal to the sum of each capacitors value
- $C_T=C_1+C_2$

# Calculating Reactance

## Process 1
- $X_C=\frac {1}{2 \pi f C}$
- $X_{C_T}=\frac {X_{C_1}*X_{C_2}}{X_{C_1}+X_{C_2}}$

## Process 2

- $C_T=C_1+C_2$
- $X_C=\frac {1}{2 \pi f C_T}$

# Capacitors only

- $X_{C_1}= Ohm$ 
- $X_{C_2}= Ohm$
- $X_{C_T}= Ohm$
- $I_{C_1}=\frac {V_A}{X_{C_1}}$
- $I_{C_2}=\frac {V_A}{X_{C_2}}$
- $I_{C_T}=\frac {V_A}{X_{C_T}}$

# RC Circuit

- $Z_T=\frac {R_T*X_{C_T}}{\sqrt {{R_T}^2+{X_{C_T}}^2}}$
- $I_T=\frac {V_A}{Z_T}$
- $I_R=\frac {V_A}{R}$
- $I_C=\frac {V_A}{X_C}$
# Finding Branch Current
- $I_T=\sqrt {{I_R}^2+{I_C}^2}$

# Power

### Real

- Power consumed by the resistor
- $P_R=V_R*I_R$

### Reactive

- Power in the inductor
- $P_C=V_C*I_C$

### Apparent

- The combination of Real and Reactive power
- $P_A=V_A*I_T$
