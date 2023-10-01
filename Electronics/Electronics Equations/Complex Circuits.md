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

Once $I_N \,and\, R_N$ are determined, the equivalent Norton circuit can be drawn
Reinstall $R_L$ from step 1.
Since they're equal and $I_N$ is $12A$ each branch gets $6A$ total. 

![[Selection_028.png]]

Finding voltage is $V_{RL}=I_{RL}*RL$ 