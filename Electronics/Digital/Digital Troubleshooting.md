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



# Troubleshooting Techniques


