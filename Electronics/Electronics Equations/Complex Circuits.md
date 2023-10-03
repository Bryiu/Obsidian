## Ohms Law
![[Pasted image 20230922114921.png]]
# Process

## Kirchhoff's Law of Voltage

Step 1 Identify the loops and assign current directions
![[Selection_010.png]]

Step 2 Make equations
![[Selection_011.png]]

Step 3 Solve equations
![[Selection_012.png]]
![[Selection_013.png]]
>[!Important]
>When you transpose, include both $I_2$ and $I_3$ for $I_1$ *or* $I_1$ and $I_2$ for $I_3$


![[Selection_014.png]]
![[Selection_015.png]]

Equations 1 and 2 were used to solve for $I_3$. Substitute $I_3$ (.77) into equation 1 to solve for $I_2$
![[Selection_016.png]]
$I_2=-0.85$. The negative current indicates that current flows in the opposite direction.
![[Selection_017.png]]
![[Selection_018.png]]
![[Pasted image 20230930184750.png]]


## Voltage Drops

Sometimes its possible to find a single voltage drop and solve for 1 loop

$-V_A-V_{R_1}-V_{R_2}+V_B=0$

![[Selection_020.png]]

$V_{R_1} = I_1*R_1$
$=80mA*12ohm$
$=0.96V$

Substitute known values
$-6V-0.96V-V_{R_2}+12V=0$
$V_{R_2}=5.04V$


>[!Warning]
>This practice question 2710 in Kirchhoff's Voltage and Current Laws is incorrect. 
>1. Its not possible to have a higher voltage output than the voltage provided. The voltage drops are higher than the applied voltage
>2. If you mathematically reduce the formula's provided in the question mark in the toolbar, the equations are not equal.
>	1. Loop#2 $I_3=2-2I_2$ does not equal Loop #3 $I_3=4+2I_2$


![[Pasted image 20230930210206.png]]

>[!Warning]
>Question 2720 is also wrong. Its even wrong compared to the example in NIDA itself. its the same equation.

![[Selection_022.png]]![[Selection_023.png]]
> The correct answer was 6.9V for the voltage drop

## Nortons Theorem

>[!Info]
>1. A current source supplies a total current to be divided among parallel branches
>2. A circuit is reduced to a single current source ($I_N$) in parallel with a single resistance ($R_N$)
>3. The current produced when a short is applied across A and B is $I_N$

![[Selection_025.png]]
The only resistance left in the circuit is $R_1$, which is in series with the $36V$ source ($I_N=\frac {V_A}{R}$). The current through the short circuit is $12A$. 

The value for $R_N$ is calculated
![[Selection_024.png]]

Remove the short circuit.
![[Selection_026.png]]

$R_N$ is the resistance of the circuit looking back from the open terminals $A\,and\,B$  
$R_N=\frac {R_1*R_2}{R_1+R_2}$ 

![[Selection_027.png]]

In this circuit, because there is a short between A&B the parallel resistors are mute, therefore 3 ohms is left for the resistance

Once $I_N \,and\, R_N$ are determined, the equivalent Norton circuit can be drawn
Reinstall $R_L$ from step 1.
Since they're equal and $I_N$ is $12A$ each branch gets $6A$ total. 

![[Selection_028.png]]

Finding voltage is $V_{RL}=I_{RL}*RL$ 

>From other formula
$I_{RL}=\frac {R_T}{R_L}*I_N$
for $R_T=\frac {R_N*R_L}{R_N+R_L}$ ==ans is 3.7ohm==
		for $I_RL = \frac {3.7}{5}*2=1.48A$
				
>$V_{RL}=I_{RL}*R_L$
        ans. = 7.4
![[Selection_034.png]]




## Nortons Theorem Part II

### Calculating for amperage

Short across A&B connects $R_2 \, and \, R_3$ in parallel
![[Selection_029.png]]

Find the parallel resistance of $R_2 \, and \, R_3$ with $R_e=\frac {R_2*R_3}{R_2+R_3}$
Since $R_{eq}=4$ and in series with $R_1$ add them together for $R_T=8$ and $I_T=6A$ 
![[Selection_030.png]]
Remove the short.

Calculating amps across $R_2$ is $I_{R2}=\frac {R_{eq}}{R_2}*I_T$  or in this example $4A$
$I_R3=\frac {R_{eq}}{R_3}*I_T$ or $2A$ since $2A$ is whats flowing to the A/B branch aka $I_N$ 

### Calculating for norton values

When calculating for $R_N=\frac {R_1*R_2}{R_1+R_2} +R_3$

Circuit redrawn with the norton values
![[Selection_031.png]]

### Calculating for Load resistor

![[Selection_032.png]]

>[!Note]
>This formula will only work for a parallel circuit such as this. Also instructions on how to find the values are under the equation

![[Selection_033.png]]

$I_{RL}=\frac {R_T}{R_L}*I_N$
for $R_T=\frac {R_N*R_L}{R_N+R_L}$ ==ans is 3.7ohm==
		for $I_RL = \frac {3.7}{5}*2=1.48A$


$V_{RL}=I_{RL}*R_L$
        ans. = 7.4
![[Selection_034.png]]

# Thevenins Theorem
## Thevenins Theorem Simple

>[!Note]
Thevenin's theorem is used to reduce a large complex circuit to a simple circuit when repeated calculations of the load resistor are required.

- The entire network connected to ==A== and ==B== can be replaced by a single voltage source ($V_{TH}$) and a single series resistance ($R_{TH}$) 
- ![[Selection_035.png]]



- $V_{TH}$ is the open-circuit voltage across ==A== and ==B==. 
	- $V_{TH}$ is measured across $R_2$ and ==B==. 
		- There is no current flow through $R_3$
		- ![[Selection_036.png]]

- $R_{TH}$ is the open-circuit resistance across terminals ==A== and ==B==, but with all voltage sources bypassed
	- ![[Selection_037.png]]

### Mentally disconnect the load resistor
![[Selection_038.png]]


### Find $V_{TH}$ across terminals ==A== and ==B==
![[Selection_039.png]]
- The voltage across terminals ==A== and ==B== is the voltage drop across $R_2$ 

- Determine the voltage dropped across $R_2$
- ![[Selection_040.png]]![[Selection_041.png]]
	- $V_{R_2}=\frac {R_2}{R_1+R_2} * V_A$
		- $48V=\frac{12ohms}{18ohms}*72V$

### Determine $R_{TH}$
- Mentally short the voltage supply
	- ![[Selection_042.png]] ![[Selection_043.png]]
		- $R_1$ and $R_2$ are now in parallel
		- $R_{R_2(TH)}= \frac {R_1*R_2}{R_1+R_2}$
			- 4 ohms
- This is a Thevenized circuit
	- ![[Selection_044.png]]
		- These Thevenin equivalents apply for any value of $R_L$ because $R_L$ was disconnected at the time of calculations

### Reconnect $R_L$ to terminals ==A== and ==B== 
- ![[Selection_045.png]] ![[Selection_046.png]]

### Determine voltage across the load $V_{RL}$
- ![[Selection_047.png]] 
	- $V_{RL}= \frac {R_L}{R_{TH}+R_L} *V_{TH}$
		- $24V=\frac {4}{8}*48$

### Finding load current
- ![[Selection_048.png]] 
	- $I_{RL}=\frac {V_{RL}}{R_L}$
		- $6A=\frac {24V}{4ohm}$

## Thevenins Theories - Simple, Dual, Bridge
### Simple Circuit
#### Remove Load Resistor
- ![[Selection_050.png]] ![[Pasted image 20231002161827.png]] 

#### Calculate Thevenin Voltage
- ![[Selection_051.png]]
	- After removing $R_L$ to calculate $V_{TH}$, there is no current going through $R_3$ due to an ==open circuit==. So there is no voltage going across it.
	- $V_{R_2}=\frac {R_2}{R_1+R_2} * V_A$
		- $24=\frac {6}{9}*36$

#### Calculate Thevenin Resistance
- Short the power supply
- ![[Selection_052.png]] 
	- $R_{R_2(TH)}= \frac {R_1*R_2}{R_1+R_2}+R_3$ 
		- $6.25k=\frac {3*9}{12}+4$
			- ans in Nida is 6k

- Circuit can be redrawn with the new Thevenin values inserted and $R_L$ replaced
	- ![[Selection_053.png]] 

#### Calculate Voltage across the Load
- ![[Pasted image 20231002164234.png]] 
	- $V_{RL}= \frac {R_L}{R_{TH}+R_L} *V_{TH}$
		- $12=\frac {6}{12}*24$

#### Calculate Load Current
- ![[Pasted image 20231002164234.png]] 
	- $I_{RL}=\frac {V_{RL}}{R_L}$
		- $0.002=\frac {12}{6000}$

![[Selection_055.png]] 

### Dual Circuit

- ![[Selection_056.png]] 

#### Remove Load resistor
- ![[Selection_057.png]] 
#### Short one power supply at a time
##### Short $V_2$ 
- ![[Selection_058.png]] 
	- $V_{R_2}=\frac {R_2}{R_1+R_2} * V_A$
		- $-16.8=\frac {3k}{15k}*84$
			- Notice its location and the negative reading

##### Short $V_1$
- ![[Selection_059.png]] 
	- $V_{R1}= \frac {R_1}{R_1+R_2}*V_A$
		- $-16.8=\frac {12k}{15k}*21$
			- Notice its location and the negative reading

- Since they both have the same polarity, they are added. Therefore $V_{TH}=-33.6V$

#### Find $R_{TH}$ 
- Short both voltage sources
- ![[Selection_060.png]] 
	- Both are in parallel across terminal ==A== and ==B== 
	- $R_{TH}= \frac {R_1*R_2}{R_1+R_2}$ 
		- $2.4k=\frac {12k*3k}{12k+3k}$

- Circuit is redrawn with the Thevenin values
	- ![[Selection_061.png]] 

#### Calculate load voltage
- ![[Selection_061 1.png]] 
	- $V_{RL}= \frac {R_L}{R_{TH}+R_L} *V_{TH}$
		- $-24=\frac {6k}{8.4k}*-33.6V_{TH}$

Calculate Load Current
- ![[Selection_062.png]] 
	- $I_{RL}=\frac {V_{RL}}{R_L}$
		- $-0.004=\frac {-24}{6000}$

![[Selection_063.png]] 

### Bridge Circuit
- ![[Selection_064.png]] 
- Remove $R_L$ 
	- ![[Selection_065.png]] aka ![[Selection_066.png]]

- $R_1\,and\,R_2$; $R_3\,and\,R_4$ have been made into two voltage dividers

#### Determine the Voltage Drop
##### Solve for $R_3$ and $R_4$
- $V_{R_4}=\frac {R_4}{R_3+R_4}*V_A$
	- $20V=\frac {6k}{9k}*30V$
- $V_{R_3}=V_A-V_{R_4}$
	- $10V=30V-20V$

##### Solve for $R_1$ and $R_2$
- $V_{R_2}=\frac {R_2}{R_1+R_2}*V_A$
	- $\frac{4k}{10k}*30V=12V$
- $V_{R_1}=V_A-V_{R_2}$
	- $30V-12V=18V$

#### Determine Potential Differences $V_{TH}$
- The potential from terminals ==A== and ==B== to *Chassis ground* need to be determined

- ![[Selection_067.png]] 
	- $B(R_2)-A(R_4)=V_{TH}$ *Potential difference*
	- $-20V-(-12V)=-8V_{TH}$
		- ![[Selection_068.png]] 
		- For the purpose of Thevenin's Theorem, use an absolute value instead of *Potential Difference*

#### Determine $R_{TH}$
- Short out source and redraw the circuit
	- ![[Selection_069.png]] 
		- How to redraw
			- ![[Selection_001.png]] 
			- ![[Selection_002.png]] 
		- Find parallel resistance
			- $R_{R_A}=\frac {R_3*R_4}{R_3+R_4}$
				- $2k=\frac {3k*6k}{9k}$
			- $R_{R_B}=\frac {R_1*R_2}{R_1+R_2}$
				- $2.4k=\frac {6k*4k}{10k}$
			- Now the circuit looks like this
				- ![[Selection_003.png]] 
			- Add ==A== and ==B== together
				- 4.4k ohm
			- Redrawn to:
				- ![[Selection_004.png]] 
					- From the *original* drawing the RL was 2k

#### Determine $V_{RL}$ and $I_{RL}$
- ![[Selection_004.png]] 
	- $V_{RL}= \frac {R_L}{R_{TH}+R_L} *V_{TH}$
		- $=2.5V$
	- $I_{RL}=\frac {V_{RL}}{R_L}$
		- $=1.25mA$

