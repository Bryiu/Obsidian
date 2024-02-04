# Logic Expressions

## Logic Expressions and Connections

- A statement cannot be true and false at the same time
- P represents the statement
- Q represents the remark
- ~ negates the statement or remark
	- ![[Pasted image 20240128132750.png]] 
- Connectives join statements
	- ![[Pasted image 20240128132832.png]] 
	- $\land$ 
		- ![[Pasted image 20240128133015.png]] 
	- $\lor$ 
		- ![[Pasted image 20240128140910.png]] 

## Conditional Statements
### Conditional

- "If.. Then.."
	- ![[Pasted image 20240128162120.png]] 
	- Once P is false any outcome Q can happen
	- Converse vs conditional
		- ![[Pasted image 20240128162330.png]] 


### Biconditional

- ![[Pasted image 20240128164244.png]] 


## Compound Statements and Arguments

- ![[Pasted image 20240128170133.png]] 
- An argument takes a logic statement, compares it with additional information, and then arrives at a conclusion
- ![[Pasted image 20240128174021.png]] 

###  Arguments

- ![[Pasted image 20240128175248.png]] 
- Logic statements compared in an argument are called premises. This argument has two premises
- The conclusion starts with the three-dot symbol for "therefore" and then identifies the resultant logic statements


# Boolean Algebra

## Boolean Algebra and Gates

- Boolean Operators
	- Product
	- Sum
	- Negate
		- $\bar x$  
- Logic Connectors
	- And
	- Or
	- Not
		- ~
- Negate
	- Not Connector
	- ![[Pasted image 20240131170230.png]] ![[Pasted image 20240131170238.png]] 
- Properties
	- Closure
		- The result of each operation is always 0 or 1
	- Identity
		- The product of a 1 and a variable results in the variable
			- $1*X=X$ 
			- ![[Pasted image 20240131171204.png]] 
		- The sum of a 0 and a variable results in the variable
			- $0+X=X$ 
			- ![[Pasted image 20240131173013.png]] 
	- Commutative
		- The result of a product/sum or two or more variables dos not depend on the order
	- Distributive
		- ![[Pasted image 20240131174016.png]] 



## Basic Boolean Algebra Equations

- Equation form allows a boolean truth table to be converted easily into the three basic gates; AND, OR, NOT

### Sum of Products Form

- (Product)+(Product)
- To find the equation:
	- Find the product of the terms for each 1 condition in the F(X,Y)
		- ![[Pasted image 20240131182650.png]] 
	- Once products are found, sum the products
		- ![[Pasted image 20240131182801.png]] 

### Product of Sums form

- ![[Pasted image 20240131183226.png]] 


### Compliments

- ![[Pasted image 20240131190140.png]] 
- ![[Pasted image 20240131190215.png]] 
- A compliment of a sum is changed by using the sum of products form
	- ![[Pasted image 20240131190407.png]] 
	- ![[Pasted image 20240131190514.png]] 
- ![[Pasted image 20240131191653.png]] 

# Gate Networks

## Developing Gate Networks

- Two ways to develop a gate network from a Boolean Equation

### Sum of Products

- ![[Pasted image 20240201164655.png]] 
	- There will be two and gates and an or gate in the network
		- because the boolean operations product and sum relate to logic gates and and or
- Change each Product to an AND gate
	- ![[Pasted image 20240201165142.png]] 
- Since there are NEGATE terms, add the NOT gates
	- ![[Pasted image 20240201165257.png]] 
		- It is common practice to indicate the inputs only once by using connecting lines to each gate
- Last SUM the PRODUCTS
	- ![[Pasted image 20240201171416.png]] 
	- ![[Pasted image 20240201171448.png]] 
	- ![[Pasted image 20240201171550.png]] 

### Product of Sums

- ![[Pasted image 20240201175518.png]] 
- ![[Pasted image 20240201175604.png]] 


## Determining Outputs of Gate Networks

- meh

# Simplifying Boolean Equations

## Boolean Principals and Rules

### Basic Principals

- Closure Property
	- The result of each operation is always a 1 or 0
- Identity Property (Product)
	- The product of a 1 and a variable results in the variable
- Identity Property (Sum)
	- The sum of a 0 and a variable results in the variable
- Communicative Property
	- The result of a product or a sum of two or more variables does not depend on the order
- Distributive Property
	- The product of a sum is the same as the sum of two products

![[Pasted image 20240202174849.png]] 

### Rules

- The sum of A and its compliment $\bar A$ is always 1
- A variabled double not is the variable
- A variable summed with a product of the same variable and another variable is the single variable
	- ![[Pasted image 20240201184030.png]] 
- The sum of a variable with a product of the same "not" variable and another varabl is the sum of the two variables
	- ![[Pasted image 20240201190108.png]] 
- The product of the sums, where one variable is the same in each sum, produces that variable aone plus the product of the other two variables
	- ![[Pasted image 20240201191622.png]] 

### DeMorgan's Theorems

- $\bar {AB} = \bar A  + \bar B$ 
	- The complement of a product equals the sum of complements
	- The theorems are used to break 'not' bars in the process of simlifying boolean equations
		- ![[Pasted image 20240201193723.png]] 
	- 


## Simplifying Equations

- ![[Pasted image 20240202180552.png]] 
- ![[Pasted image 20240202181224.png]] 

# Karnaugh Maps

- Boolean equation must be in the sum of products form
- Three Variable Map
	- ![[Pasted image 20240203102235.png]] 
- Four Variable Map
	- ![[Pasted image 20240203103231.png]] 
	- Formatting the table
		- ![[Pasted image 20240203103322.png]] 
- Five and 6
	- ![[Pasted image 20240203104309.png]] 
- Maps with 7 or more must be done with a computer

## Simplifying

- Identify Adjacent Cells
	- ![[Pasted image 20240203104452.png]] 
- Combine the 1's in adjacent cells into groups of 1,2,4,8,16, etc
- Maximize each group
	- Make the largest group
	- Dont overlook 1's that may have already been included in another group
		- They may overlap
- For each group, the sum the products represented in the cells of the group.
	- The opposite variables will be eliminated, resulting in one simplified product for each group instead of the group of products in individual cells
	- Sum the group products to obtain the simplified boolean equation

### Simplifying 

- ![[Pasted image 20240203134850.png]] 
- ![[Pasted image 20240203134935.png]] 
- ![[Pasted image 20240203141310.png]] 
	- For green the Y and $\bar Y$ terms cancel leaving $\bar XZ$ 
	- The Z and the X variables cancel, leaving $\bar Y$ 
- ![[Pasted image 20240203160811.png]] 
- ![[Pasted image 20240203161146.png]] 

# Introduction to Combinational Circuits

## Combinational Logic

- Combinational logic is the combining of two or more logic gates

## Universal Logic Gates

- NAND and NOR are commonly used as universal logic gates
- 3 NAND = OR
- 5 NAND = XOR

# Logic Families

- TTL
	- Transistor to Transistor logic
	- most widely used family of IC's
	- Divided into two groups
		- Military
			- Labeled 5400
		- Commercial
			- Labeled 7400
	- Voltage Requirements
		- 0-5V Input
		- 0-5V output
	- Current requirements
		- Fan-in
			- identifies how much current it will draw when driven by an IC similar to itself
			- Fan in is subtracted from the fan out of the driving IC
		- Fan-out
			- Identifies how many other IC's can be driven from its output
			- if the fan out is 5, then 5 IC's can be connected to the output
	- Speed
		- Also known as **propagation delay**
			- The amount of time an IC takes to switch from one condition to the other
			- ![[Pasted image 20240204114356.png]] 
			- ![[Pasted image 20240204114419.png]] 
				- L
					- Low power consumption of that chip
					- Longer propagation delays
				- H
					- High speed switching
					- Short propagation delay
					- High power consumption
				- S
					- Schottky Circuit
					- Super fast
					- Less power than most H-types
	- Noise
		- TTL produce noise each time they switch from high to low
		- Too much noise will cause input or output to change at the wrong time
- CMOS
	- Complimentary Mosfet
	- Slower than TTL
	- Much lower power requirement than TTL
	- High input impedance
		- Ensures that the CMOS IC operates at a lower input power
	- ![[Pasted image 20240204131545.png]] 
		- CMOS has the C in the name
	- Input/output voltage 0-15V 
	- Almost no switching noise is generated 
- ECL
	- Emitter Coupled Logic
		- Used when speed is more important than cost
	- ![[Pasted image 20240204131940.png]] 
		- Distinguished by the 10,000 series numbers
- IIL
	- Integrated Injection Logic
	- Used in circuits that require analog and digital interaction
	- Distinguished by the manufacturers name than by the IC number
		- ![[Pasted image 20240204132944.png]] 
- There are different families of IC's because some circuits require speed while some require less power
	- ![[Pasted image 20240204133045.png]] 

# Number Systems

## Decimal

- Base 10
- 0-9


## Binary

- Base 2
- 0,1

## Octal

- Base 8
- 0-7

## Hexadecimal

- Base 16
- 0-9, A-F

# Number Conversions

- Octal is in groups of 3 
	- ![[Pasted image 20240204141756.png]] 


## Hexadecimal and Binary

- ![[Pasted image 20240204143800.png]] 
	- Binary converted to hexadecimal
	- ![[Pasted image 20240204144014.png]] ![[Pasted image 20240204144300.png]] 

## Math Operations

### Binary Addition

- ![[Pasted image 20240204152139.png]] 

### Subtraction

- ![[Pasted image 20240204152245.png]] ![[Pasted image 20240204152253.png]] 
	- The complement allows a computer to subtract numbers by adding the negative binary value to the positive binary value
		- ![[Pasted image 20240204152456.png]] 
		- 
			- First is to invert the number being subtracted and add
			- Next if a carry is generated, bring it down and add it to the sum
				- ![[Pasted image 20240204153919.png]] 
				- Carries not generated when the subtraction results in a negative number
					- ![[Pasted image 20240204154907.png]] 
					- When a carry is not generated, the result of the addition must be 1s complimented, and a negative sign placed in front of it
						- ![[Pasted image 20240204155058.png]] 
>[!Note]
>After inverting the lower number, the result has to be inverted as well

>[!Important]
>Match the lower digits with the same number of digits on the bottom


### Multiplication

- Multiplication of binary numbers is performed just as multiplication of decimal numbers is performed
- ![[Pasted image 20240204162128.png]] ![[Pasted image 20240204162320.png]] 

### Division

- ![[Pasted image 20240204163404.png]] 
	- Subtract 11 from 11 and bring down a 1
	- 11 goes into 1 zero times
	- Bring down the last 1
	- 11 goes into 11 1 time
	- ![[Pasted image 20240204163525.png]] 

