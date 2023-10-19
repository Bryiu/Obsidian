- All calculations are based *in this lesson* are $V_{pp}$
- Inductance describes the induced voltage produced by a changing magnetic field
	- Greater inductance = Greater induced voltage
- AC voltage causes the magnetic field to expand and contract 
	- produces a voltage that opposes current flow
- As Inductance increases, current decreases, inductive resistance increases
- At higher frequencies the magnetic field expands and contracts faster - providing more opposition to circuit current
	- As frequency increases, current decreases, inductive reactance increases
- As frequency increases, Inductive Reactance increases ($X_L$)
- In an inductive circuit, (V)oltage (L)eads (C)urrent
	- by 90$\degree$ 
- The combined opposition to current flow from the resistor and inductor is called Impedence
	- Represented by (Z)
	- Measured in ohms

# Changing $V_{pp}$ to RMS
- $V_{pk}=\frac{V_{pp}}{2}$
- $V_{rms}=V_{pk}*0.707$
- $I_{pk}=\frac{I_{pp}}{2}$
- $I_{rms}=I_{pk}*0.707$

==Total Inductance = ($L_T$)==

# Calculating Total Inductance
- $L_T=L_1+L_2+L_3+L_4...$

# Calculating Ohms Law
## Inductive Reactance
- Represented by $X_L$
	- Measured in ohms
		- Represents the amount of opposition to current flow in the circuit
- Caused by the inductance and frequency of the circuit
- $X_L=2\pi f L$
	- $f = frequency$
	- $L = inductance (aka \, Henry's)$

## Calculating $V_L$ and $I_T$

- $V_L=I_T*X_L$
	- $V_L$ represents the voltage applied to the circuit
- $I_T=\frac{V_{pp}}{X_{LT}}$
	- $X_{LT}$ Represents the total resistance in the circuit to the amount of inductance

 >[!Warning]
 > - In a Resistive and inductive circuit the resistor and inductor cannot be directly added
 > 	- The oppose current differently
 
# Calculating Impedence
- Impedence total
	- $Z_T=\sqrt {{R_T}^2+{X_L}^2}$
- Inductive Reactance Total
	- $X_{LT}=2\pi f L_T$
- Current Total
	- $I_T=\frac{V_{pp}}{Z_T}$
- Voltage drops can then be determined
	- $V_{R1}=I_T*R_1$
	- $V_{L1}=I_T*X_{L1}$

>[!Important]
>Because of the 90$\degree$ phase difference adding the impedence and resistance voltages will not add up to the applied voltage

- $V_A=\sqrt{{V_R}^2+{V_L}^2}$

# Reactance Power Calculations
## Real

- Power consumed by the resistor
- $P_R=V_R*I_R$

## Reactive

- Power in the inductor
- $P_L=V_L*I_L$

## Apparent

- The combination of Real and Reactive power
- $P_A=V_A*I_T$

# LAB RL Circuit Operation

- When finding the Voltage across a resistor in series with two inductors
	- Add the two signals together with the channel B signal inverted

# RL Series Circuit Faults

- Use voltage measurements to determine if the circuit is working correctly
- Use resistance measurements to determine which component is faulty or unserviceable