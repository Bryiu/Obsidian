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


