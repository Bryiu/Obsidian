
# Intro

- Classified by the amount of electrodes they contain
- ![[Pasted image 20231107193506.png]]
	- The heater is not counted
- Anode receives the electrons and the cathode emits the electrons
	- The plate (anode) has a larger value which allows the electron transmission
- At room temperature, electrons are not able to move
- Do not last long as far as a component
	- They have numbered sockets
	- ![[Pasted image 20231107201439.png]] 

## Thermal Emission

- ==Thermal Emission==: Heating the cathode for electron emission
	- As temperature increases so does emission
		- Until it breaks
	- Cathode normally made of tungsten covered with thorium oxide
		- Tungsten needs to be heated too much to emit electrons
	- Heaters can be applied either directly or indirectly
		- ![[Pasted image 20231107195833.png]] 
			- Directly Heated cathodes have two disadvantages:
				- The potential wire is inconsistent
				- Emission of electrons may occur as a result (hum)
			- Indirectly heated cathodes have insulated tungsten wire inserted into a cylinder 
	- For Emission to occur, the anode and cathode must be within the envelope
		- ![[Pasted image 20231107200602.png]] 
		- Made of glass or ceramic
		- Has the air removed or replaced
			- Air causes collisions with the electrons
			- Prevents the heating elements from burning up

## Triodes, Tetrodes, Penode

- A tiode is a diode with a control grid
	- The control grid regulates the amount of electron flow
		- controls the resistance of the tube
	- ![[Pasted image 20231107200821.png]] 
- A tetrode has a screen grid
	- ![[Pasted image 20231107201040.png]] 
	- placed between the plate and the control grid
- Pentrodes have a suppressor grid between the screen and plate
	- ![[Pasted image 20231107201245.png]] 

## Gas Filled Tubes

- Filled with an inert gas
- Has a dot in the schematic
	- ![[Pasted image 20231107201617.png]] 
- Doesnt need to be heated
- Electrons are transferred from the inert gas and not the heating of the cathode
	- As current increases, resistance decreases
	- Constant voltage drop

# Operation

## Diode

- Current flows in one direction

## Triode

- When the control grid becomes more positive or negative, resistance increases
	- Due to interelectrode capacitance
		- ![[Pasted image 20231107202713.png]] 
		- 
- Similar to a JFET
- Can shut off from varying voltage or too much voltage
- Replaced by the transistor

## Tetrode

- Screen grid is to reduce interelectrode capacitance
	- Capacitors in series are calculated in parallel
	- Screen grid is positive
	- Causes the electrons to move slowly
		- interferes with the electron beam
- Has secondary emmission as a disadvantage
	- Electrons hitting the plate were knocking off other electrons

## Pentode

- ![[Pasted image 20231107203650.png]] 

- Supressor grid is negative
	- Reduces interelectrode capacitance
	- Secondary emission electrons get forced back to the plate
	- Removes undesired effects

# Configuration

- ![[Pasted image 20231107204010.png]]
- 
## Common Cathode

- ![[Pasted image 20231107205348.png]] 

- $C_1$ blocks DC signal from input
- $C_2$ filters AC signals
	- reduces negative feedback
- $R_1$ develops output voltage
- $R_2$ provides DC path to ground, Develops input signal
- $R_3$ is cathode self bias
- $I_k$ is current that flows in the cathode lead
- $I_p$ is current that flows in the plate
- Control grid current is nevative and does not draw current

- When no input signal, current through tube is ==Static Current== 
	- As input signal goes positive, bias decreases
		- Bias decreases, resistance decreases in $V_1$
		- Plate current increases
			- $V_{R_1}$ increases
			- $V_{V_1}$ decreases
	- Input signal negative, bias increases

### Configurations
 High Input Impedence
 High interelectrode capacitance
 High Gain
 180 out of Phase 

## Common Anode

- aka cathode follower amplifier
- Used for Impedence matching
- Plate is used as common
- input applied to the grid

	-  As input signal alternates positive, bias decreases
		- Bias decreases, resistance decreases in $V_1$
		- current increases
			- $V_{R_2}$ increases
	- Input signal alternates negative opposite
		- input is in phase with output


## Common Grid



# CRT

- Converts electrical signals to a visible image

## Electrostatic

- Deflects electrodes within the envelope
- ![[Pasted image 20231108134412.png]] 
- Schematic Symbols
	- ![[Pasted image 20231108144231.png]] 

## Electromagnetic

![[Pasted image 20231108134758.png]] 

- has two sets of deflection coils, vertical and horizontal
	- Called a yoke


## Electron Gun (Electrostatic)

![[Pasted image 20231108135103.png]] 

- focusing and accelerating anodes are positive with respect to the grid
	- accelerating is the most positive
- Aquadag coating is a thin, conductive coating on the inside wall of the tube
	- prevents secondary emmision
	- Highly positive to collect the loose electrons and return them to the power supply
- Deflection plates send electrons to different parts of the screen
	- varying the voltages will pass the beam to different parts of the screen
	- 

![[Pasted image 20231108135510.png]] 
- Grid is negative to limit the amount of electrons
- by changing the size of the electrostatic field, you can control where the beams will cross, changing the intensity

