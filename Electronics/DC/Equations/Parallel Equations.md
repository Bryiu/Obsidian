## Ohms Law
![[Pasted image 20230922114921.png]]
### Ohms Law in Parallel
### Calculating Current
![[Selection_002.png]]

$$ I_t=I_{R1}+I_{R2}+I_{R3}$$
### Calculating Resistance

>[!Important]
>The total resistance is *always* less than the value of any single branch resistance

$$R_t=\frac{V}{I_t}$$
*for only two resistors*
$$R_t=\frac{R_1R_2}{R_1+R_2}$$

>[!info]
>If you have three resistors, chain them together. Meaning, perform the equation for the first two resistors *THEN* replace that value for $R_1$ in the equation.



**or**
$$R_t=\frac{1}{\frac{1}{R_1}+\frac{1}{R_2}}$$
## Comparing two Voltage Dividers

$V_2-V_1=x$

When you have two voltage dividers use these formula's

![[Selection_006.png]]


| Ohms Law Method                       |                                        |
| ------------------------------------- | -------------------------------------- |
| How to calculate $V_1$ using Ohms Law Method  | How to calculate $V_2$ Using Ohms Law Method                        |
| $I_1= (\frac {V_A}{R_1+R_2})$         | $I_2=\frac{V_A}{R_x+R_s}$              |
| $V_1=I_1* R_o$                        | $V_2=I_2*R_o$                          |
| Ratio Method                          |                                        
| Calculate $V_1$                       | Calculate $V_2$                        |
| $\frac{V_A}{V_1}=\frac{R_1+R_2}{R_2}$ | $\frac{V_A}{V_2}=\frac {R_x+R_s}{R_s}$ |


### Finding the unknown value in a balanced bridge circuit
$\frac {R_1}{R_2} = \frac  {R_x}{R_s}$ Then cross multiply

