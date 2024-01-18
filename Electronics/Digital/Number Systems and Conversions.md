# Number System Concepts

- Base 10
	- ![[Pasted image 20240117123012.png]] 
		- Each section in the dark blue is like a box. So once a number reaches 9, the next box starts
		- ![[Pasted image 20240117123538.png]] 
- Base 5
	- ![[Pasted image 20240117123704.png]] 
	- ![[Pasted image 20240117124853.png]] 
		- Doesnt mean 10 as in base 10; it means one group of 5
	- ![[Pasted image 20240117125417.png]] 
		- Does not mean 13; it means one group of 5 plus three
	- ![[Pasted image 20240117125624.png]] 
- The base number is the quantity you carry to or borrow from the next column
## Addition


- ![[Pasted image 20240117130046.png]] 
	- In base 5 when you reach a 5 in one column you place a 0 and add a 1 into the next column

## Subtraction

### Table method

- ![[Pasted image 20240117131738.png]] 
	- Cannot subtract 4 from 0
		- Borrow 1 from the second column
		- Combine with 0 to equal $10_5$ = 5 in decimal
	- To use the table find the column label 4 (top row)
		- Go down in the table and find 10
		- Then go left to find the row label difference 1
	- Cannot subtract 4 from 1
		- Borrow 1 from the third column
		- Combine it with the 1 to equal 11 (6 in decimal)
		- Use the table to find the difference of 11 and 4 (ans: 2)

### Compliment method

- ![[Pasted image 20240117134406.png]] 
- ![[Pasted image 20240117134220.png]] 
	- Take each digit in the subtrahend and subtracting it from the highest digit allowed in the working base
		- The highest digit in base 5 is 4
			- So we subtract each digit in the subtrahend from 4 
 -  Add the compliment (00) to the minuend (120) to determine the subresult (120)
	- ![[Pasted image 20240117134620.png]] 
- ![[Pasted image 20240117135038.png]] 
	- 
Regular subtraction, just carry 4's instead of 10's

# Number System Conversions

- ![[Pasted image 20240117140912.png]] 
- ![[Pasted image 20240117141055.png]] 
- Adding the products gives the final answer in base 10
- Examples
	- ![[Pasted image 20240117141354.png]] 

- Base 10 to N (10 to 5)
	- List the powers of the target base and their decimal equivalents
		- ![[Pasted image 20240117143411.png]] 
	- Divide the powers of the target base into the base number we are converting until we reach a remainder of 0 
		- ![[Pasted image 20240117145520.png]] 
		- Start with 5 since 5 is the largest power that will go into 17
			- Remainder 2
		- Divide the remainder by the next lower power of the target base
		- Final answer $32_5$ 
	- Examples
		- ![[Pasted image 20240117151433.png]] 
- Remember where you start is where you go back 1 by 1. So if one doesnt work, you skip it - place a 0 - and go to the next

# Multiplication and Division

## Multiplication

- Multiply the numbers using base 10 and convert the answer to base 5.
	- ![[Pasted image 20240117161812.png]] 
	- $4*4=16$ in base 10 which equals 3 groups of five plus 1 or 31 in base 5
- ![[Pasted image 20240117171327.png]] 
- ![[Pasted image 20240117171828.png]] 
- ![[Pasted image 20240117172120.png]] 
![[Pasted image 20240117181559.png]] 
## Division

- ![[Pasted image 20240117181007.png]] 
	- 4 goes into 23 a maximum of 3 times
	- 4 goes into 13 a maximum of 2 times
	- 4 goes into 31 a maximum of 4 times

# The Binary System

- 