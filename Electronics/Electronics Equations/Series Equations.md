## Ohms Law
![[Pasted image 20230922114921.png]]

# Calculations
## Series Circuit 

>[!Info]
>Current is the same across a series circuit. 


### Power in a Load
	1.  Is to find the power being used by a load
		1. This was used in class for determining the power across a resistor

$$P_2=I_t^2R_x$$

---
### Voltage Divider Formula
	1. Consists of two or more resistors connected in series with a voltage source. They're used to obtain a smaller voltage from a larger voltage source

$$ V_2 = V_s(\frac {R_x}{R_t})$$
		2. When applying this formula, $R_x$ is applied to the divider and the following resistors between the output terminals.


==For Figure 8-5==

 ![[Obsnote1.jpg]]

```chart
type: line
labels: [R4, R3, R2, R1]
series:
  - title: Volts
    data: [.01, .1,1,10]
tension: 1
width: 55%
labelColors: true
fill: false
beginAtZero: true
bestFit: true
bestFitTitle: undefined
bestFitNumber: 1
```
```chart
type: line
labels: [R4,R3,R2,R1]
series:
  - title: Volts
    data: [.01,.1,1,10]
tension: 0.2
width: 80%
labelColors: false
fill: true
beginAtZero: true
bestFit: false
bestFitTitle: undefined
bestFitNumber: 0
```

---

==For Figure 8-3(b)==

![[obsnote2.jpg | 600]]

>This is the calculated voltage between the two points. Though, when returning to ground the voltage is going to be 0 volts.

```chart
type: bar
labels: [Min Voltage, Max Voltage]
series:
  - title: Volts Produced at Vx
    data: [2.61, 8.17]
tension: 0.2
width: 27%
labelColors: true
fill: true
beginAtZero: true
bestFit: false
bestFitTitle: undefined
bestFitNumber: 0
```

