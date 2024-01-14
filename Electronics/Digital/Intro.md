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

- When TTL was devised, Lows were 0.8V or less and highs were 2V or more
	- Some variance whether we're looking at input or output
		- ![[Pasted image 20240113080749.png]] 
		- Manufacturers have stiffer mandatory levels
		- The voltages between 0.8 and 2V are indeterminate and illegal as they are not valid logic levels
			- When voltage is in these parameters its called a float, and likely points to an open in the circuit
		- The actual point where a TTL device switches from a LOW to a HIGH or vice versa is normally about 1.4V. 
			- The 0.8V-2V levels were established for Margin of Error
			- Also for noise levels

# Digital Test Equipment

# Clock Generator

- Supplies inputs to digital circuits for the purpose of determining normal operation
	- High, Low, and Pulse square waves are produced by the clock generator
- ![[Pasted image 20240113115941.png]] 
	- ![[Pasted image 20240113120006.png]] 
		- Placing an oscilloscope at the clocks outputs allows you to monitor the square wave produced
- ![[Pasted image 20240113120937.png]] 
	- The square wave is sent to the frequency divider to generate three square waves of different frequency
		- Measured at $F_1,F_2,F_3$ 
		- If the potentiometer is adjusted, three output signals changed

# Logic Probe

- Used to detect the presence or absence of signals in digital circuits
- Indicate when High, Low, or Pulsating logic levels are present
- ![[Pasted image 20240113124909.png]] 
	- Red clip to the +5V test point; Black to ground

# 555 Timer

- Provides timing signals to other digital circuits

## Description

- Operates as either an astable or monostable vibrator
- Output is a square wave that can range from a few hertz to several megahertz
- Can operate as a TTL-compatible astable, monostable, pulse width modulator, or linear ramp generator
- Modern 555 are 8 pin DIPS
	- Older styles are housed in cans
	- ![[Pasted image 20240113152028.png]] 
		- $V_{cc}$ can vary from 5VDC to 15VDC without affecting circuit operation 
		- To produce different circuit configs; different components and voltages are connected to pins 2,4,5,6,7
- ![[Pasted image 20240113153648.png]] 
	- Internal design of the 555
	- Major components are an inverter, transistor, 2 comparators, and an RS flip flop
		- Comparator
			- Compares two voltage levels
			- If the + is more positive than the -, the output is high
				- If less positive, the output is LOW
				- The - input is subtracted from the + input.
			- Input is analog and output is digital
		- RS 
			- Means Reset, set
			- Three inputs, two outputs
				- Two outputs are always opposite of each other
					- If both match its an invalid input condition
				- Outputs will not change if inputs become 0
				- Clear input overrides inputs R and S.
					- If low, the flip flop resets
					- Bubble indicates low activates this function
		- 555 Timer
			- Wont operate by itself. Requires external components on pins
			- In most configs, CLR input is tied to $V_{cc}$ which disables CLR