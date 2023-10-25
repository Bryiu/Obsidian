![[Selection_056.png]]

- Similar to Parallel resistor circuits
	- Need to consider phase relationship of the resistor and inductor
- Inductive resistance is the opposition to current flow

# Converting from $V_{pp}$ To $V_{rms}$
- $V_{pk}=\frac{V_{pp}}{2}$
- $V_{rms}=V_{pk}*0.707$
- $I_{pk}=\frac{I_{pp}}{2}$
- $I_{rms}=I_{pk}*0.707$

# Intro
- Total inductance of a parallel circuit is always less than the smallest inductor
- Placing inductors in parallel has the same effect as increasing the area that contains the winding
	- The more area, the less flux density

# Finding total inductance

- $L_T=\frac {L_1*L_2}{L_1+L_2}$
- $X_L=2 \pi f L$
	- Measured in ohms
	- As frequency increases $X_L$ increases
	- As inductance increases $X_L$ increases

# Finding Current
## Inductors Only
- $I_T=\frac {V_{pp}}{X_{L_T}}$
	- $I_{L_1}=\frac {V_{pp}}{X_{L_1}}$
	- $I_{L_2}=\frac {V_{pp}}{X_{L_2}}$
- 

>[!Warning]
>$X_L$ and R cannot be added directly

## Impedance (Inductors and resistors)

- $Z_T=\frac {R*X_{LT}}{\sqrt {R^2+{X_{LT}}^2}}$
	- Accounts for the 90$\degree$ difference

- $I_T=\frac {V_{pp}}{Z_T}$
	- $I_R=\frac {V_{pp}}{R}$
	- $I_L=\frac {V_{pp}}{X_L}$
### Total current using branch circuits
- $I_T=\sqrt{{I_R}^2+{I_L}^2}$

# Process
## Calculate total inductance
![[Selection_057.png]]

## Find total inductance reactance
![[Selection_058.png]]

## Determine total resistance
![[Selection_059.png]]

## Solve for total impedance
![[Selection_060.png]]

## Solve for total current
![[Selection_061.png]]

## Calculate branch circuits
![[Selection_062.png]]

## Check results; calculate total current
![[Selection_063.png]]

# Power
## Real
- $P_R=V_R*I_R$
## Reactive
- $P_L=V_L*I_L$
## Apparent
- $P_A=V_A*I_T$

# Faults
