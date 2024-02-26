# Data

- **Bit**: **B**inary Dig**it**. Each individual number
- **Byte**: Used to express size of large binary numbers

## Serial

- Serial data transfer uses one wire for the input and output
	- ![[Pasted image 20240224115529.png]] 
- Advantage: one wire used
- Disadvantage: each bit of data needs a clock pulse. Large amounts of data require more time to transfer

## Parallel

- Uses a separate wire for each bit
	- Multiple bits per clock pulse
	- ![[Pasted image 20240224122315.png]] 
- Advantage: Less time is required to transfer large amounts of data
- Disadvantage: More hardware is required

# Registers and Memory

- Registers Allow data transfer from one circuit to another
- ![[Pasted image 20240224140907.png]] 
- The number of flip-flops determines the registers storage capacity
- ![[Pasted image 20240224142554.png]] 

## Storage

- ![[Pasted image 20240224145019.png]] 
- ![[Pasted image 20240224152154.png]] 
- Purpose is to temporarily store data


## Shift 

- ![[Pasted image 20240224145036.png]] 
- Transfer data from one circuit to another
- As new data enters the register, the existing data is shifted to the next circuit in line
	- ![[Pasted image 20240224152956.png]] 
- Does Serial and parallel data transfer

# 4 Bit Storage Register

## Serial Storage register

- ![[Pasted image 20240224183550.png]] 
- ![[Pasted image 20240224183802.png]] 
	- The circulate path allows the register to store data
		- Contents of the register are not lost when shifted to the output
	- Four clock pulses will shift the registers data to the next circuit in line and feed the data back to the register
		- Happens for each output switch
	- When $S_1$ moves back to data input, new data is transferred to the output


## Parallel Storage

- ![[Pasted image 20240224185045.png]] 
	- A separate output is taken from each flip-flops Q output

# 4 Bit Shift Register

- Transfer four bits of binary data from one circuit to another
- ![[Pasted image 20240225130951.png]] 
	- Mode control sets the register for serial or parallel transfer
	- ![[Pasted image 20240225131723.png]] 
- Always serial or parallel data present at the registers output
- In serial mode, data is shifted right in re-circulation mode
- Shift left can be done in parallel
	- Used to perform math operations
- In parallel mode, data is entered serially into F/F D and shifts left
- Circulate and input
	- Parallel = shift left
	- Serial = shift right
- Shift registers can also be used as storage registers since the data is stored after its transferred in

# 8 Bit Shift Register

- Used to transfer 8 bits from one circuit to another
- ![[Pasted image 20240225150421.png]] 
	- Serial synchronous data is available at the output QH
	- Each clock output shifts data one flip flop to the right
	- Parallel inputs are asynchronous and controlled by a high applied to the PRESET enable
	- Enabling CLEAR resets the register
	- When PRE is high, the clock is not used


# 64 Bit Memory

- *Think of a 64 bit memory circuit as being 16 4-bit registers contained in one IC
	- Each register stores 4 bits of data
		- called a WORD
			- Words can be 4, 8, or 16 bit
			- Word is a group of bits representing a complete piece of digital information
			- Stored in memory and assigned an address. Each word has a different address
- ![[Pasted image 20240225171036.png]] 
	- A memory circuit needs several register circuits to operate properly
	- Transferring of the address can be serial or parallel
	- When new data enters memory, the address register assigns an address
	- When data leaves the register knows where to find the data
- **ROM**: Read Only Memory
	- Used in applications that require identical data every time a process occurs
- **RAM**: Random Access Memory 
	- Used in applications that require information to go into and out of memory
- **Random Access**: The writing to and reading from memory
- **Non-Volitile Memory**: Retain data when power is removed
- **Volitile Memory**: Stores data when power is applied
- ![[Pasted image 20240225171941.png]] 
	- In this two bit register, can address four memory locations
	- 00 in the address causes gate 1 to go high, enabling word 0