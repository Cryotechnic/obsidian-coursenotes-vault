# Buttons & Signal Modulation
## Push Button
- Manually-operated switch devices
	- Simple electric mechanism to turn something on or off
- Depending on switch, either momentary or latching function


## Push Button - Momentary
- Button returns to its original position after it is relaesed
- While pressed down, keeps the ON state, when released, goes back to OFF
- Also known as *self-reset type*

## Push Button - Alternate
- Switch is set to ON after it is first pressed, then OFF after it is pressed again
	- Pretty much a toggle
- Also known as *self-holding type*

## Push Button - Push-Pull
- When it is pressed once, internal lock mechanism holds it in the same position (ON)
	- To release, pull back on the button, which releases the lock

## Push Button Types
- Normally open: Provide path for current (close circuit) when button is pressed
- Normally closed: Impede the flow of current (open circuit) when button is pressed

## Button I/O
- Pole: Number of input circuits of a switch
- Throw: Number of output circuits of a switch

![[Pasted image 20220509195617.png]]

## Signal Modulation
- Addition of information to an electronic / optical carrier signal
	- Process of varying 1+ properties of a waveform, usually containing information to be transmitted
- Periodic wave properties:
	- Amplitude
	- Frequency
	- Phase

### Modulation vs Demodulation
- Imposing input signal on carrier wave = modulation
	- Similar to hiding code in the carrier wave
- Demodulation: Extracting the original signal from modulated carrier wave

$Modulation + Demodulation = Modem$ 

## Pulse Width Modulation (PWM)
- Process to control average power supplied by electrical signal
- Method that digital outputs are used to control analog devices
	- Speed of motors
	- Smart lighting systems
	- Temperature of heating elements
	- Etc.

## Duty Cycle
- Total power applied to load ${\propto}$ (proportional to) time in which switch remains turned ON
- Percentage of digital signal in which it is turned ON = Duty Cycle

## Software vs Hardware PWM
#### Hardware PWM
- Registers are set to specific setting
- Hardware responsible for timing (max 19.2MHz)

#### Software PWM
- Code is setup which makes a pin the PWM pin
- 1Hz - ~1kHz