# Multimeter Loading
> [!Note] 
> Multimeter loading is the effect the multimeter has on the circuit

## Internal Resistance
- Internal Resistance ($R_M$) is either in series or parallel to the circuit being measured
	- It adds a load
- Its automatically performed in a digital multimeter
- Manually performed with an analog meter

## Calculating Multimeter Loading Current
>[!Note]
> $R_M$ only affects current if the circuit values are really small

- Add a parallel resistance ($R_P$)
	- ![[Selection_005.png]] 
- With a calculated Current of $6mA$ the meter would reduce the current to $4mA$ 
	- ![[Selection_006.png]] 
- Adding a small resistor value to the meter decreases the loading effect from 33% error to a 0.1% error
	- ![[Selection_008.png]] 

## Calculating Multimeter Loading Voltage

>[!Note]
>$R_M$ only affects voltage if the circuit values are really large



- Reduced by adding a series resistance
	- ![[Selection_009.png]] 
		- Calculated:
			- ![[Selection_010.png]] 
		- With a 1k internal resistance
			- ![[Selection_011.png]] 
		- Adding a large value resistor to the meter decreases the loading effect
			- ![[Selection_012.png]] 

## Loading effects of the multimeter
- Multimeter loading effects are displayed on the selector for the MM
- ![[Selection_013.png]] 
