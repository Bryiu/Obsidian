- Divide into two area's
	- Analog
	- Digital

# History

- Electronics of counting
- Abacus was the first digital counting device
- 17th century, Pascal invented a mechanical counting machine
- 19th century, Babbage made a counting machine with a programmed controller
- 1940, ENIAC was invented, the first electronic general-purpose digital computer
	- Used large vacuum tubes that were big, expensive, unreliable
	- Second generation replaced the vacuum tube with the transistor
	- Third generation combined the transistor with the Integrated Circuit

# Intro

- Digital circuit schematics have square box's instead of components
- Only react to two input signals or voltage levels, high and low
	- Square or pulse
	- Form logic functions
		- And; Or; Not

## Logic functions

### And

- ![[Pasted image 20240112134532.png]] 
	- Produces a high output only if all inputs are high
	- ![[Pasted image 20240112134624.png]] 

### Or

- ![[Pasted image 20240112134854.png]] 
	- Produces a high output if any input is high
	- Used in security functions
	- ![[Pasted image 20240112135441.png]] 

### Not

- ![[Pasted image 20240112135621.png]] 
- Inverts the input signal, producing the opposite as the input
- Used with the AND and OR functions to change the output
- ![[Pasted image 20240112135706.png]] 

# Boolean Algebra

- $AND=A*B$ 
- $OR=A+B$
- $NOT=A-B$ 
	- Represented by $\overline A$  

# Hardware

- Pins provide for input and output signals of the IC
	- Connecting an IC in different ways can produce different logic functions

## Part Number

- ![[Pasted image 20240112153548.png]] 

## CAN

- ![[Pasted image 20240112144600.png]] 
- The IC can is primarily an analog device
- Has the tab as a reference point


## Flatpack

- ![[Pasted image 20240112144648.png]] 
- Rectangular ceramic or plastic
- ![[Pasted image 20240112150112.png]] 


## DIP

- ![[Pasted image 20240112144827.png]] 

## Classification

### Level of Integration

- ![[Pasted image 20240112154208.png]] 
- ![[Pasted image 20240112154236.png]] 
- ![[Pasted image 20240112155303.png]] 
	- SN is a Texas Instruments standard prefix
	- Circuit description describes the function and logic family technology
		- Different from part number
		- Could contain whether it meets military specs or commercial standards
		- First two numbers indicate operating temperature
			- 54 and 74 are used for TTL (Transistor-Transistor logic) chips
				- 54 has an operating range is -55$\degree$ to 125$\degree$C 
					- Used for military purposes
				- 74 has an operating range of 0$\degree$ to 70$\degree$C 
					- Used for commercial use
					- 54's can be put in place of 74s but 74s may not be substituted for 54's
		- Middle letters describes the tech in the IC
			- ![[Pasted image 20240112163023.png]] 
		- Numbers at the end of the chip description identify the chips specific function such as NOR, dual JK flip flop, 4-bit up/down counter etc
			- Range from 0 to 999
		- Package letter describes how the IC is packaged
		- Instructions specify any special instructions about the chip
- IC data book lists specifications
	- Use part number on the IC to locate in the book
		- Contains all the info you need to know
			- Part #, ID, Block diagram, Pin connection

# Buffers and Inverters

- Digital circuits that have one input and one output

## Buffer

- ![[Pasted image 20240112173040.png]] 
	- Low input always produces a low output
- ![[Pasted image 20240112173118.png]] 
- Three basic functions
	- Protection
		- Used to protect digital components from a voltage or current that is too high
	- Driver
		- Used as a driver circuit when several digital circuits operate from the same voltage source
			- Each circuit adds a load to the 5 volts until the effective voltage is too small to operate any of the circuits
		- Able to maintain current at a high enough level so that voltage is not loaded down
	- Switching
		- Functions much like an amp, but is capable of producing only two different output states

## Inverter

- The bubble is the NOT function
- ![[Pasted image 20240112190856.png]] 
	- Is a combination of the buffer and the NOT function.
		- High input is LOW at the output and vice versa
	- When buffers are wanted but not available, two inverters can be used

# Input/Output Voltages

- 