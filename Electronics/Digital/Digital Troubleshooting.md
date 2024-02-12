# Intro

- Most common internal failures of a digital IC
	- Malfunction of internal circuitry
		- IC outputs do not respond to the IC inputs.
		- No way to predict what the outputs will do; depends on what failed
	- Inputs or outputs shorted to ground or $V_{cc}$ 
	- Inputs or outputs with an open circuit
	- Shorts between two pins (other than ground or $V_{cc})$ 
- Most common External failures of a digital IC
	- Open signal lines
	- Shorted signal lines
	- Faulty power supply
- Voltmeters are often not as effective as devices like logic probes and current tracers

# Common IC Faults and Symptoms

- Three basic steps
	- Fault Detection
		- Observe the circuit or system operation and compare it with the expected operation
	- Fault Isolation
		- Perform tests and make measurements to isolate the fault
	- Fault Correction
		- Replace the faulty component
		- Repair faulty connections
		- Remove shorts 
- If one or more of the IC's inputs are internally shorted to ground or $V_{cc}$ the device will be stuck in either a LOW or HIGH state
	- The gate will remain high or low depending on its path and open or short
	- Characterized by excessive heat dissipation from the IC package
- ![[Pasted image 20240123123108.png]] 
	- TTL will respond as if this floating input is a logic 1
	- CMOS devices will respond erratically and may become damaged from overheating
- ![[Pasted image 20240123130122.png]] 
	- Initially both inverters have a high input; so the short makes no difference
	- It makes a difference in t2, t3, t4 where the inputs are trying to make opposing outputs
- External Faults
	- Open signal lines
		- Broken wire
		- Poor solder connections
		- Cracked or cut trace on a PCB
		- Bent or broken pin on an IC
		- Faulty IC socket where the pin does not make good contact with the socket
		- Easily verified by disconnecting power from the circuit and checking continuity with an ohmmeter between the two points in question
	- Shorted signal lines
		- Same effect as internal shorts between IC pins; Causes signals of the shorted pins always to be identical
		- Sloppy wiring
		- Solder bridges
		- Flawed etching
		- Most common: Stripping too much insulation from wire ends that are in close proximity 
	- Faulty power supply
		- Either IC will not operate at all
			- Operate irratically
		- PSU may go out of regulation because of an internal fault or circuit drawing more current than the PSU can handle
			- Can happen if a chip or component has a fault that causes it to draw much more current than normal
			- Good practice to check the voltage levels at the PSU in the system to see if they're within their ranges
				- Also to check with oscilloscope to verify no significant AC ripple
		- Most common sign is when one or more chips act erratically or not at all
			- Always check power and ground levels of each IC that appear to be operating incorrectly



# Troubleshooting Techniques

- Checking PSU
	- Multimeter
		- Used to verify the power supply voltage levels are within tolerance and that current draw has not exceeded the PSU's specs
	- Oscilloscope
		- Good idea to check for AC ripple on DC levels and that voltage levels are regulated
- Logic Levels
	- Multimeter
		- Used to verify that device logic levels are within specification
			- TTL Low should be between 0 and .8V
			- TTL High should be between 2.7 and 5V
			- ![[Pasted image 20240124200226.png]] 
- Resistance
	- Multimeter
		- Used to check for opens or shorts
- Multimeter
	- Digital (pulsed to clock measurements) has frequencies too high to display accurate readings
		- Measurements are inaccurate and erratic
- Logic Probe
	- Developed to overcome the shortcomings of the multimeter
	- Used to detect the presence or absence of signals in digital circuits
- Oscilloscope
	- .
- Signal Tracing
	- If voltage measurements with Oscill and current measurements made with a multimeter do not isolate a fault, use logic probe
	- Works well with a circuit with few components
	- A defective component could be any gate connected to the fault
		- ![[Pasted image 20240124212729.png]] 
		- Only able to disconnect all connections at X and rechecking
			- The gate which is disconnected at signal goes back to normal is the defect
	- **Half Split Signal Tracing Rule**: divides the circuit in half, and the faulty half is divided in half. The division continues until the defective component has been determined