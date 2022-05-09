# Radio Frequency Identification (RFID)
- Wireless communication incorporating the use of electromagnetic radio frequency to collect data + automatically identify objects thru low-power radio waves
## Application
- Traceability in supply chain
- Logistics and inventory management in retail
- Security and control of various assets

## RFID Bands
- Low Frequency (LF) - 125kHz-134kHz -> 10cm range
- High Frequency (HF) - 13.56MHz -> 10cm to 1m range
- Ultra High Frequency (UHF) - 860-960MHz (EPC global standard) -> 12m range
- Near Field Communication (NFC) - 13.56MHz + lower than 15mA -> 10-20cm range

## RFID System Components
- Tags: Containing identity + other info and communicates it to readers
- Reader: Device that contains 1+ antennas that emit radio waves and receives signal from tags
- Backend system: Defines business logic for interpreting raw RFID data + actions 

## RFID Tags
### Passive RFID
- Reader sends signal to tag
	- Tag uses signal energy to power on and send back data to reader
- Operate in LF, HF or UHF bands

### Passive UHF RFID
- Limited by tag characteristics, propagation environment & reader parameters

### Passive NFC RFID
- Branch of HF, operating at 13.56MHz
- Designed for secure form of data exchange
	- Payment method
	- Access control

### Passive LF RFID Tags
- Can operate in environment with high water content
- Based on inductive coupling technology
- Ideal for access control, laundry, animal identification, etc.

### Active RFID Tags
- Has own power source & transmitter
- Typically on UHF but range is 150m
- 2 Types:
	- Transponder
	- Beacon

## RFID Readers
- Required for any RFID system
### Fixed RFID Reader
- Stays mounted in a location (walls, desks, portals, etc.)
### Mobile RFID Reader
- Handheld devices, allows for flexibility + allows communication with host

## 2D & 3D RFID Readers
### 2D RFID Reader
- Tracks item location on 2 axis (X & Y)
### 3D RFID Reader
- Tracks item location on 3 axis (X, Y, Z)