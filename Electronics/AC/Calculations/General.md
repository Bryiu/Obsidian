![[Pasted image 20230922114921.png]]


# Frequency
- When finding the frequency on the oscilliscope, multiply the SEC/DIV setting by the number of divisions


	- *==Period*== is determined by the time taken to complete once cycle of the sine wave
		-  $T(period)=\frac {1}{f (frequency)}$
			-  ex in WISC $.2ms*9(divisions)=0.0018 \,seconds$
	- ==*Frequency*== is calculated by the cycles per second
		- $f=\frac{1}{T}$
			- $f = \frac {1}{0.0018}=555 Hz$

# Wavelength
- This is the distance between the beginning and end of one cycle
	- represented by $\lambda = distance$ 
	- expressed in meters or centimeters
- $\lambda = \frac {300*10^6}{f}$ 

# Induction
## Average sine wave
- The constant $0.637$ is used
- $Average = 0.637 * the Peak Value$
	- ![[Selection_018.png]]
		- $V_{AVG}=0.637 * V_P$
			- $V_{AVG}= 0.637*10=6.37$
	- ![[Selection_020.png]]
		- $V_{AVG}=0.637*170=108.29V$
		- 

## RMS
- RMS has the constant .707
	- This number stems from AC being 70.7% effective as DC
	- $RMS = 0.707 * the Peak Value$
	- ![[Selection_019.png]]
		- $RMS = 0.707 * 10$
		- $V_{RMS}=0.707*10$
- ![[Selection_021.png]]
	- 120 VAC = 120 VDC
- 
# Ramp Wave forms
- Below is a sawtooth 
- ![[Selection_028.png]]
	- Measured in Volts/Second or Amps/second
		- $\frac{\Delta V}{\Delta t}=\frac{V}{s}$
			- ![[Selection_029.png]]
- ![[Selection_030.png]]
- $f=\frac{1}{T}$
- $T(period)=\frac {1}{f (frequency)}$ 

# Ohms Law in AC
## Determining VRMS
- ![[Selection_031.png]]
	- find peak voltage
		- $P_V=\frac {Vpp}{2}=10Vp$
	- Calculate $V_{rms}$
		- $V_{rms}=0.707*Vp=7.07V_{rms}$
	- Calculate current
		- $I=\frac {V_rms}{R_t}=0.28mA$
>[!Note]
>To find peak from $V{rms}$. $Peak=V_{rms}*\frac{1}{0.707}$

# Calculating IRMS

- ![[Selection_033.png]]
	- Find peak voltage
		- $P_V=\frac{V_{pp}}{2}=\frac {20}{2}=10V_p$
	- Calculate $V_{rms}$
		- $V_{rms}=0.707*V_p=0.707*10=7.07V_{rms}$
	- Calculate Current
		- $I_T=\frac{V_{rms}}{R_T}=\frac{7.07}{3k}=2.4mA$

# Phase Angle

-  The time axis represents 360$\degree$. The 50 subdivisions each represent 7.2$\degree$. 
	- To find the phase angle, multiply the subdivision 