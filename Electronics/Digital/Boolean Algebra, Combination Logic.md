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


