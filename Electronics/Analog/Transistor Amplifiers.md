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

- Verifying normal operation of a multistage amplifier requires comparing ==total== measured and calculated gains
	-  ![[Pasted image 20231127132022.png]] 
		- Both $Q_1$ and $Q_2$ invert the input signal
		- $A_v$'s must be within 20% of the calculated gain
	- $Q_1$'s voltage gain is affected by the input resistance of $Q_2$'s input resistance
		- ![[Pasted image 20231127134353.png]] 
		- *Individual amplifiers voltage gain* $A_v = \frac {R_c}{R_s + \frac {0.025}{I_E}}$ #formula 
		- *For Multi-stage amplifiers*
			- ==*Stage 1*==Calculate the new value for $R_L$ by placing $R_6,R_7,R_3$ in parallel. $R_C\,aka\,R_3=R_L$ 
				- $R_L= \frac {1}{\frac {1}{R_3}+\frac {1}{R_6}+\frac {1}{R_7}}$ #formula 
				- Calculate the individual amplifiers gain
					- $A_v = \frac {R_c}{R_s + \frac {0.025}{I_E}}$ 
			- ==*Stage 2*== *for this example* there is no third stage. Calculate gain with:
				- $A_v = \frac {R_c}{R_s + \frac {0.025}{I_E}}$ 
					- ==The second stages base voltage only comes from $+V_{cc}$== 
					- $R_c$ is only $R_8$ because there is no stage after
			- *Calculate $A_v$ 
				- $A_{v_T}=A_{v_1}*A_{v_2}$ 


>[!Note]
>When the output of an amplifier is loaded, the voltage gain decreases due to the parallel resistance of the load changing the collector load resistance

- As input frequency decreases, the reactance of $C_1,C_2,C_3$ increase
	- $X_C=\frac {1}{2 \pi f C}$ 
		- Low frequencies affect the circuit, while high frequencies do not
		- Large reactance ($X_C$) decreases total gain of the RC amplifier
			- Individual stage gains are not affected - they're between the coupling capacitors ($A_v$)
		- ![[Pasted image 20231127151700.png]] 
	- Comparing $A_v$ for stages  
		- $A_v=\frac {V_{out}}{V_{in}}$ 
		- Each stage can have good voltage gain, but the overall voltage gain can still be bad
	- If the input signal frequency is high, the gain of the amplifier is reduced
		- This is because transistors cannot amplify signals above a certain frequency
			- Each transistor has different characteristics - so they reduce voltage gain at different high frequencies
	- Amplitude affects circuit operation too
		- if $V_{pp}$ is too large, signal becomes distorted (clipping)
			- ![[Pasted image 20231127153058.png]] 
			- Input signal drives the transistor into cutoff and saturation
			- $Q_1$ can be good, but $Q_2$ can be bad

## Push Pull Amplifiers

- Used in the final power stage driving low resistive loads
	- High current gain
	- high efficiency
	- low output resistance
		- the output of the amplifier must match the input resistance of a load to transfer the power without losses
	- low distortion

### Common Emitter Push Pull Amp

![[Pasted image 20231128145344.png]] 
- Common emitter amps have medium gain; but since they're in parallel output current gain is high
- low output resistance is achieved by matching the resistance of $T_2's$ secondary
- Small amount of distortion
	- Crossover distortion
		- ![[Pasted image 20231128153258.png]] 
		- No current drain occurs during this time

#### Operation

>[!Caution]
>When understanding this; remember voltage and current are moving in opposite directions 



*This is an in phase transformer*
- ![[Pasted image 20231128153713.png]] 
	- During the positive alternation positive is applied to the base of$Q_1$ and negative to $Q_2$ 
		- $Q_1$ conducts; $Q_2$ is cut off
	- Current flows from ground to $+V_{cc}$ 
		- ![[Pasted image 20231128155304.png]] 
		- Causes a negative potential at the top of the primary windings of $T_2$ 
			- output is negative
				- ![[Pasted image 20231128160130.png]]
		- Negative alternation
			- $Q_1$ cut off; $Q_2$ conducts
			- output is positive
				- ![[Pasted image 20231128165853.png]] 
- Produces an inverted output
- Advantage to exactly match load resistance
- Disadvantage: Cost and more room



### Common Collector Push Pull Amp

- *aka complementary symmetry amplifiers* 
	- resistor values are mirrored across the input
- Base Voltage
	- $V_{B_1}= V_{cc}-V_{R_1}$ #formula 
	- $V_{B_2}= V_{cc}-V_{R_1}-V_{R_2}-V_{R_3}$ #formula 
- 

- ![[Pasted image 20231128171032.png]] 
	- Common collectors have high current gain
		- Low output resistance
	- $Q_1$ conducts on positive alternations
		- $Q_2$ cut off
	- $Q_2$ conducts on negative alternations
		- $Q_1$ cut off
	- $Q_1$ and $Q_2$ are not at ground potential
		- $V_{cc}$ is divided between emitters 
			- ![[Pasted image 20231128185053.png]] 
				- Voltage on the emitters has biasing at
					- ![[Pasted image 20231128185405.png]] 
			- $Q_1$ conducting pulls current from the left-hand plate of $C_2$ charging it in a positive direction
				- ![[Pasted image 20231128185816.png]] 
			- $R_L$ has a positive current flow
				- ![[Pasted image 20231129110804.png]] 
					- Because its a common collector class B transistor; half of the input signal is amplified with no phase change
			- In the negative phase; $Q_2$ pushes current to $C_2$ charging it in a negative direction
				- ![[Pasted image 20231129112716.png]] 
				- 
		- Must be matched transistors
			- Have the same gain characteristics
- Advantage: No transformers are used
- Disadvantage: Transistors can be damaged if load is disconnected
	- No load; no discharge path for $C_2$ 


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

# Troubleshooting

- Identify the faulted stage
	- ![[Pasted image 20231129122738.png]] 
- Repair
- Check for normal operation