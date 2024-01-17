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
			- Comparators have a reference voltage applied from $+V_{cc}$ 
			- The reference voltages and inputs on pins 6 and 2 make the 555 operate
				- Components connected to these pins control 555 config
				- Even if threshold voltage drops below 2/3 $V_{cc}$ and causes a LOW output from comparator 1, the flip flop stays reset
				- When trigger input voltage drops below 1/3 $V_{cc}$ comparator 2 puts a HIGH on input S of the flip flop
					- When trigger input goes above, the 0 output of the comparator 2 will not change the flip flops state
			- Pin 3 (output) is LOW when the threshold input goes above 2/3 $V_{cc}$ and HIGH when trigger input goes below 1/3 $V_{cc}$ 
				- Goes low and stays low even if the voltage on the threshold input drops
				- Goes HIGH and stays high even if voltage on the trigger input goes above 1/3
			- Transistor is used as a switch to supply a ground to pin 7
				- When $\bar Q$ output is HIGH, transistor is forward biased connecting the ground on pin 1 to 7
					- When reverse biased it breaks the connection
![[Pasted image 20240114133920.png]]  

## Configuration

### Astable

- ![[Pasted image 20240114132440.png]] 
- Produces a continuous square wave output. No stable states
- Pin 4 at $V_{cc}$ disables the CLR input to the RS flip flop
- Pin 1 is grounded. 
	- Keeps reference voltages at 2/3 and 1/3 $V_{cc}$ 
- Pin 5 is grounded
	- Capacitor and ground filter noise and voltage variations from power supply
- Pin 7 has the connection of $R_1,R_2$ applied
	- Will be open or grounded depending on the state of the internal circuit
- Pin 2,6 has $R_2,C_1$ 
	- Circuit operation is based on the charging and discharging of $C_1$ 

#### Operation

- ![[Pasted image 20240114145457.png]] 

- When $V_{cc}$ is first applied, voltage across $C_1$ is 0V
	- 0V on pin 6 is not greater than 2/3 $V_{cc}$ 
		- Output on pin 3 will not change to LOW
	- 0V on pin 2 is less than 1/3 $V_{cc}$
		- Output on pin 3 will be HIGH and pin 7 is open
- Open on pin 7, $C_1$ starts to charge
	- When voltage across $C_1$ increases between 1/3 and 2/3 there is no circuit action
	- $C_1$ continues to charge until reaching 2/3
		- At 2/3, Threshold causes the output to change to a LOW and pin 7 is grounded
			- Ground on pin 7 causes $V_{cc}$ to be dropped across $R_1$ 
			- $C_1$ starts discharging, decreasing the voltage on pins 2,6
				- Discharging between 2/3 and 1/3 there is no circuit action
					- Stops around 1/3
						- Output becomes high again
							- ![[Pasted image 20240114150305.png]] 
				- Frequency of the output depends on the RC time constant of $R_1,R_2, and \, C_1$  
- $V_{cc}$ values have no effect on operation since the 555, resistors and capacitor use the same $V{cc}$ 



### Monostable

- ![[Pasted image 20240114160342.png]] 

- ![[Pasted image 20240114132452.png]] 
- Produces a High output only when an input is received, then the output goes back low. One stable state
- Normally High input on pin 2 does not cause the circuit to change
	- Neither 0V on pin 6
- LOW output indicate that pin 7 is grounded
- If output is HIGH at this time, the circuit automatically changes the output to a LOW
- Since Pin 7 is connected to pin 6, the voltage on pin 6 is grounded and the capacitor cannot charge 
	- Remains in a stable state since pin 2 voltage has not changed and pin 6 voltage cannot change
		- ![[Pasted image 20240114160712.png]] 
	- A LOW applied to pin 2 will change the output
		- With the ground removed from pin 6 and 7, $C_1$ begins to charge
		- Even if input goes back to HIGH, $C_1$ will charge
		- just above 2/3 threshold goes low and pin 7 is grounded
			- $C_1$ discharges
				- Output does not change
		- Once $C_1$ charges above 2/3 the output goes back to low and the ground is placed back on pins 6,7
		- The time the output remains high depends on the time constant of $R_1,C_1$ 
			- Not the time pin 2 is LOW
- Circuit remains in a stable state until another input is received on the trigger
- $V_{cc}$ value has no effect on the circuit operation
  
  
  # Intro to IC

## Classification

- First developed in 1959 by Texas Instruments
- ![[Pasted image 20240116173052.png]] 

### Monolithic

- ![[Pasted image 20240116173402.png]] 
	- Placing all integrated components into a single piece of doped semiconductor material
	- Used most often

### Thin Film

- ![[Pasted image 20240116173534.png]] 
	- Placed on a insulating material
	- Good insulation 
	- Less power

### Thick film

- ![[Pasted image 20240116173654.png]] 
	- More than one substrate
	- Resistors and capacitors are formed on the main substrate while transistors are contained on their own substrate

### Hybrid

- ![[Pasted image 20240116173809.png]] 
- Mix of both Monolithic and thin film, even thick
- 

## Linear

- ![[Pasted image 20240116174043.png]] 

## Digital

- ![[Pasted image 20240116174059.png]] 
- 

## Construction

- ![[Pasted image 20240116174249.png]]
	- Different layers of doped material are created using different techniques
- On the top wafer, wire is deposited to connect the different components
	- Normally aluminum or gold
- Factors in packaging an IC
	- Packaging material
		- Ceramic, plastic, or glass
		- ![[Pasted image 20240116174834.png]]
			- Ceramic can be sealed better than plastic
	- Packaging shape
	- Pin arrangement




## Identification

- ![[Pasted image 20240116175653.png]] 
- 
