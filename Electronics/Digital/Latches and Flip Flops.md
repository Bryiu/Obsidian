# Intro to Latches and Flip Flops

## Sequential Circuits

- Digital circuits can be classified in two catagories
	- Combinational
		- produce outputs only when an input is applied
	- Sequential
		- will retain the output after the input is removed
		- feedback line allows the gate to remember its previous output
			- Latches an input to the output
			- ![[Pasted image 20240215193206.png]] 
- Latches and flip flops are both used as memory devices
	- Both are bistable

## Latch

- changes states when inputs are changed
	- ![[Pasted image 20240215193547.png]] 
- Active high RS Latch
	- **![[Pasted image 20240216192529.png]] 
- Active Low RS Latch
	- ![[Pasted image 20240216192736.png]] 
		- ![[Pasted image 20240219112754.png]] 
- Latches can have the same outputs, this can cause problems
- The biggest problem in RS latch is the RACE condition
	- Happens when putting a latch in an invalid combination
	- When both gates are trying to go high at the same time
		- Then changed instantly to the no change condition
- RS Latch was made to create a bounceless switch
	- Mechanical switches have a bounce in the signal


## Flip Flop

- Constructed of many gates and there are several gate configs used to create storage flip flops
- ![[Pasted image 20240216193235.png]] 
- Flip flops are almost never drawn out as a logic diagram.
	- They are represented by a logic symbol with the labeled inputs and outputs defining their type
	- Flip flops contain a clock circuit
- Latches an flip flops are used extensively in digital circuits in the form of registers, counters, and memory circuits



## RS Latch


# RS Flip Flops

![[Pasted image 20240219143234.png]] 

- Used to store the last input condition until the next input condition is applied
- Replacement for mechanical switches
	- Mechanical switches bounce
	- ![[Pasted image 20240219143142.png]] 





# Clocked RS Flip Flops

- ![[Pasted image 20240219160729.png]] 
- Designed to store the last input condition until the next input condition is gated through
- ![[Pasted image 20240219154329.png]] 
	- A high applied to S input sets a high Q and a low $\bar Q$ when the clock is high
	- A high on the clock allows a change in state
	- Clock input low disables change in the flip flop
- ![[Pasted image 20240219165230.png]] 
	- ![[Pasted image 20240219165259.png]] 
# D-Type Flip Flops

- Has one input that is used for both the S and R inputs
- ![[Pasted image 20240220092133.png]] 
	- D takes the high or low and passes them as S or R
	- C enables the flip flop
- ![[Pasted image 20240220092254.png]] 



# JK Flip Flops




# Master-Slave Flip Flops







