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


## Single Step




