# Counters

- All counters are basically the same
	- They use JK Flip-Flops in Toggle mode
		- Toggle mode has a high on both the J and the K
	- ![[Pasted image 20240304145429.png]] 
		- When an input is received, the flip flop changes states
		- Since flip flop A receives the clock signal input and toggles B, QA represents the Least Significant Digit of the counters output
			- ![[Pasted image 20240304145714.png]] 
				- Uses two flip flops
				- Called a MOD 4 counter
					- **Modulus**: Describes the number of counts that a counter can produce
						- *ex*. MOD 8 counters can count from 0-7
						- $MOD=2^N$ 
- ![[Pasted image 20240304150203.png]] 
	- Asynchronous counter.
	- Input applied to the clock
- ![[Pasted image 20240304151842.png]] 
	- Synchronous counter
	- Input is only applied when the clock is high
- ![[Pasted image 20240304152001.png]] 
	- Counter circuit used for division
- ![[Pasted image 20240304153239.png]] 
	- Counter circuits are also used to produce a timing pulse
	- Happens every 8 clock pulses in this counter

# Adders 

- ![[Pasted image 20240304154409.png]] 
	- Used to determine the sum of two binary numbers
	- Perform four operations
		- Addition
		- Multiplication
		- Subtraction
		- Division

## Adders

- ![[Pasted image 20240304154526.png]] 


### Half Adders 

- ![[Pasted image 20240304155306.png]] 
	- Adds two numbers
	- Produces a carry out, but does not use carry in
	- Will produce an accurate sum if no carry is produced by a previous circuit


### Full Adders

- ![[Pasted image 20240304155353.png]] 
	- Adds two numbers and the carry in from a previous circuit
	- Produces a sum and a carry out
	- Picture above is a full one bit adder
		- Gate 1 and 3 make a half adder for inputs A and B
		- Gate 2 and 4 make a half adder for inputs A, B, and carry in
		- The carry out is generated when at least two of the three inputs are 1
			- ![[Pasted image 20240304163324.png]] 
				- 


### One Bit Adder

- ![[Pasted image 20240304164946.png]] 
	- Used to serially add two binary numbers
- ![[Pasted image 20240304165704.png]] 
	- Used to parallel add two bit binary numbers


## Multiplication

- ![[Pasted image 20240304154738.png]] 
	- The result of the first addition is fed back into B where it is again added to 6

## Subtraction

- ![[Pasted image 20240304154912.png]] 

## Division

- ![[Pasted image 20240304154954.png]] 
	- The number of times the counter has to subtract to reach 0 is the quotient

# Ripple Counter

- ![[Pasted image 20240304172828.png]] 
- Is a basic asynchronous binary counter
- Used to count pulses in binary
- Can also produce a *modified modulus* of 3, 5, 10, etc
- ![[Pasted image 20240304174324.png]] 
	- CLR MOD CONTROL allows the counter to count to any binary number and reset

>[!Note]
>When writing and reading binary numbers, start with the right with the MSD (Most significant digit)

- Advantage: Operates in various MODs by using the clear input
	- When clear is high, the counter counts from 0000 to 1111
	- When clear is low, the counter is reset
	- ![[Pasted image 20240304174905.png]] 
		- Connecting Q or $\bar Q$ outputs to logic gates control when the register resets
		- Since Clear goes low on the 8 count, the counter is a MOD 8

# Up Counter

- Synchronous binary counter
- Set up to run in two modes
	- **Free Run**: Counter counts continuously. Hits 1111 and starts all over again
	- **Single Step**: Counts to the maximum count and then stops
- First pulse is a set pulse, following pulses are counts

## Free Run

- ![[Pasted image 20240304184858.png]] 
	- Counts up to the maximum count by the counter and starts over
		- Set by SA-SD
		- V+ is used to apply a 1111 to change the output of the gate since no switch is set to the V+ position
	- Each input pulse is counted and stored


## Single Step

- ![[Pasted image 20240305115146.png]] 
	- Counts to the maximum count and stops. 
	- Each input pulse is counted and stored
	- At max count, the input pulses are disabled inside the counter 

## General

- ![[Pasted image 20240305115431.png]] 
	- Seven inputs and four outputs to perform free run and single step
	- Input pulses applied to the clock input
		- They are counted as they are entered
	- The enable input allows the counter to function
	- Load input allows the counter to start counting over at various mods.
	- QA-QD are used to drive a display and as inputs to a logic gate that SETs the LOAD
- ![[Pasted image 20240305121608.png]] 
	- Needs an extra clock pulse to reset for the D-type flip flop
	- Inputs A-D override the pulse input on the CLOCK and SET the counter to 0000. With 0000 in the counter, the output of the AND gate is again LOW. This places a LOW at the ENABLE input and the DATA input to the flip flop. A HIGH is placed at the LOAD input with the next clock pulse, and loading is disabled. the counter can now count 
	- The inputs A-D are what the counter is reset to
- ![[Pasted image 20240305131612.png]] 
	- The flip flop has a ground applied to D so the output at $\bar Q$ will always be high
	- The counter will not start counting until S1 is pressed
		- This loads 0000 into the counter
		- must be manually restarted


# Down Counters

- Designed to count down
- ![[Pasted image 20240305141534.png]] 
- ![[Pasted image 20240305141746.png]] 


# 4-Bit Adder
- ![[Pasted image 20240305143705.png]] 
	- **Arithmatic Logic Unit (ALU)**: an integrated circuit that contains adders, counters, registers, and logic circuits. The ALU performs math operations and logic functions
- Adders are designed to add two one bit binary numbers
	- ![[Pasted image 20240305144732.png]] 
	- ![[Pasted image 20240305144753.png]] 
	- Half adders are used when the carry in is not important.
		- A carry from a previous circuit will not be accepted
	- Full adders are used when the carry in is important
		- ![[Pasted image 20240305144934.png]] 
- ![[Pasted image 20240305145122.png]] 
	- Serial
- ![[Pasted image 20240305151634.png]] 
	- Parallel

# 4 Bit Subtractors

- ![[Pasted image 20240305152735.png]] 
	- Input A applies the minuend
		- **Minuend**: The number from which another number is subtracted
	- Input B applies the subtrahend
	- Two's Compliment circuit inverts the B input and adds a 1 to the result.
		- ![[Pasted image 20240305153131.png]] 
	- ![[Pasted image 20240305153357.png]] 
		- When a carry is generated the answer is positive
			- The carry is dropped
	- ![[Pasted image 20240305153429.png]] 
		- When no carry is generated, the answer is negative
- ![[Pasted image 20240305154012.png]] 
	- ![[Pasted image 20240305154125.png]] 
		- CI is taken from the flip flop because it starts with a HIGH Q due to the momentary HIGH that is applied to the PRE input
- ![[Pasted image 20240305154348.png]] 
	- +5V applied to CI for Two's Compliment
- if MSD=1 the number is positive
	- It will be dropped from the final answer, but will be shown in register C

