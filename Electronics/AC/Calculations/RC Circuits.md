- $V_{pk}=\frac{V_{pp}}{2}$
- $V_{rms}=V_{pk}*0.707$
- $I_{pk}=\frac{I_{pp}}{2}$
- $I_{rms}=I_{pk}*0.707$

# Series
>[!Important]
>Total capacitance $C_T$ of a series circuit is always less than the smallest capacitor

- Placing capacitors in series has the same effect as moving the plates of a capacitor farther apart
	- The greater the distance between the plates, the lower the capacitance.
	- The junction between C1 and C2 is essentially neutral
		- ![[Pasted image 20231020152212.png]]
			- Capacitance is developed between the left plate of C1 and the right plate of C2
## Finding total capacitance
- $C_T= \frac {C_1*C_2}{C_1+C_2}$
	- ![[Pasted image 20231020152711.png]]
- $C_T=\frac {1}{\frac{1}{C_1}+\frac{1}{C_2}+\frac{1}{C_3}}$
	- ![[Pasted image 20231020152728.png]]

## Capacitive Reactance $X_C$

- $X_C$ expresses the amount of opposition to current flow in the circuit
- The greater the capacitance the greater the stored charge
- AC voltage causes electrons to move from one plate to the other. The more electron movement, the higher current.
	- as capacitance increases, current increases, decreasing capacitive reactance
	- ![[Pasted image 20231020173738.png]]
	- As frequency increases, current increases, capacitive reactance decreases
	- ![[Pasted image 20231020174602.png]]
- $X_C=\frac {1}{2 \pi f C}$

## RC Series Circuits
- Solve for $R_T$ and $C_T$. Then find $X_{C_T}$
	- $R_T=R_1+R_2$
	- $C_T= \frac {C_1*C_2}{C_1+C_2}$
	- $C_T=\frac {1}{\frac{1}{C_1}+\frac{1}{C_2}+\frac{1}{C_3}}$
	- $X_C=\frac {1}{2 \pi f C_T}$
	- $X_{C_T}=X_{C_1}+X_{C_2}$

		- ![[Pasted image 20231020184800.png]]



### Only Capacitors

- $I_T=\frac {V_{pp}}{X_{C_T}}$
- $V_C=I_T*X_{C_T}$
	- ![[Pasted image 20231020185851.png]] ![[Pasted image 20231020185910.png]] 

### Resistors and Capacitors
- Remember **ICE**
	- Current (I) in a (C)apacitive circuit is before Voltag(E)
	- Capacitive ![[Pasted image 20231020192702.png]] 
	- Resistive ![[Pasted image 20231020192737.png]] 

#### Impedence
- $Z_T=\sqrt {R^2+{X_C}^2}$
	- ![[Pasted image 20231020193221.png]] ![[Pasted image 20231020193237.png]] 
- $I_T=\frac {V_{pp}}{Z_T}$
- 