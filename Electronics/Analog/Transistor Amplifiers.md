# Cascade Amplifiers

![[Pasted image 20231126155749.png]] 

*Cascade*: How the output of one amplifier is applied to the input of another
*Stage*: Each individual amplifier in the ==cascade== 

- Purpose is to increase gain
	- High gain; Stability and predictability are lost
	- Low gain; Stable and predictable
- Cascade amplifiers achieve high gain without loss of stability or predictability
	- Normally stages are designed to have a voltage gain of 10
		- Ex. Amplifier needs to amplify a 5$\micro V$ output to a 5V speaker; Six stages are needed
			- ![[Pasted image 20231126162637.png]]
- $A_{v_t}=A_{v1}*A_{v2}*A_{v3}$ #formula 

## RC Coupling

[[RC]]

- ![[Pasted image 20231126163139.png]]
	- Output signal developed across collector load resistor ($R_{c1}$)
	- Coupled across coupling capacitor ($C_{c2}$)
		- Passes AC and blocks DC
- Most common
- Inexpensive components

>[!Important] Disadvantage: low frequency response
 At low frequencies; coupling capacitor reduces input and output signals
		
  - $X_c=\frac {1}{2 \pi f C}$ #formula 

## LC Coupling

[[LCR]]

- ![[Pasted image 20231126170746.png]] 
	- $L_1$ and $L_2$ have very low resistances to DC
		- $V_{cc}$ is applied almost directly to $Q_1$ and $Q_2$ collectors
		- Resistance depends on the frequency
			- $X_L=2 \pi f L$ #formula 
			- At higher frequencies, reactance is very high
				- Very little AC is wasted on the inductor
					- AC power is coupled to the next stage

>[!Important]
>Disadvantage: Inductors are more expensive and reactance drops off at lower frequencies

- Used in Radio Frequencies
	- RF Chokes

## Transformer Coupling

[[Transformer]]

- ![[Pasted image 20231126173937.png]] 
	- In high frequency amplifiers, a capacitor is added in parallel to enhance the amount of signal that is coupled from stage to stage
	- The capacitor across the primary of each transformer makes a resonant circuit
		- Pass only one frequency
- Used in Radios and TV's
	- Principal behind radio stations and TV channels

>[!Important]
>Disadvantage: Size of the transformer at low frequencies

## Direct Coupling

- ![[Pasted image 20231126175526.png]] 
	- Base biasing resistors are not used
	- Amplify any signal applied; AC or DC

>[!Important]
>Disadvantage: Changes in temperature and No compensating components
>Any variations in AC or DC is passed on to the next stage

- Used for low frequency or input extends over a large range of frequencies
- 

