# Temperature Sensors & Motors
## DHT series
### DHT-11
- 0-50$^{\circ}$C $+/-$ 2$^{\circ}$C temperature
- 20-80% $+/-$ 5%
- Uses capacitive humidity sensor & thermistor to measure air
### DHT-22
- -40-80$^{\circ}$C $+/-$ 0.5$^{\circ}$C temperature
- 0-100% $+/-$ 2-5% humidity
- Normal & not real-time response time

### DS18B20
- -55-125$^{\circ}$C $+/-$ 0.5$^{\circ}$C temperature
- Has digital output (works well with Rpi)
- Good for when you need to measure something far away / wet conditions
- Response times < 750ms

### Bosch Sensor
- Air pressure, temperature & humidity
- Best low-cost sensing solution for measuring humidity with $+/-$ 3% accuracy

## Motors
- Must align with purpose and overall performance goals of the system
- 3 common motors
	- DC
	- Stepper
	- Servo

### Direct Current (DC) Motors
- 2-wire (power & group) continuous rotation motors
- Electromagnetic device using magnetic fields & conductors converting electrical -> mechanical energy for rotation
- Brushed & brushless DC motors are the most common

![[Pasted image 20220509193023.png]]

### Stepper Motors
- Motors that move in slow & precise, discrete steps
- Good for their precise position control
	- Desktop printers
	- Security Cameras
	- CNC Milling machines

### Servo Motors
- Motors that can provide very precise motion control
- Assembly of:
	- DC motor
	- Gearing set
	- Control Circuit
	- Position-sensor
- Typically can rotate within 180$^{\circ}$ angle range

## Motor Driver Integrated Circuit (IC)
- Control motors in autonomous robots (typically)
- Acts as interface between microprocessors & motors
- Microprocessor cannot supply direct current to motors -> IC is the solution to that