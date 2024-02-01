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
