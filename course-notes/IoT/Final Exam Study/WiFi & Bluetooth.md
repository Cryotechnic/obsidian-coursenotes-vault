# WiFi & Bluetooth
- Wireless Fidelity (Wi-Fi) term is a marketing hoax
- Wi-Fi is wireless technology used to connect devices to the internet, or together

## Wi-Fi Network
- Internet connection that is shares with multiple devices via a wireless router
	- Router is connected to a modem which acts as a hub to broadcast internet signal to all devices
- Flexibility to stay connected to the internet while in network coverage area

## Wi-Fi Frequency Bands
- 2.4GHz: Better range
- 5GHz: Better speed / performance

## Wi-Fi Standards
- IEEE WLAN group develops new wireless standards 
	- 802.11b, 802.11a, 802.11g, 802.11n, 802.11ac and 802.11ax
		- Also known as WiFi1 -> WiFi6

## 802.11 Association Process
- 802.11 probing
- 802.11 authentication
- 802.11 association

## Probe Request
- Wi-Fi enabled device sends proboe request to discover 802.11 networks in proximity
- Advertises supported data rates and 802.11 capabilities in L2 (MAC)
- Once Probe sent, ProbeTimer countdown starts and waits for answer. No response => next channel & repeat

## Wireless Card Modes
- Managed Mode: Wireless card relies on local AP in Managed Mode to provide connectivity to wireless network
- Monitor Mode: Wireless card stops transmitting data and sniffs currently configured channel & reports contents of any observed packets to host OS

## MAC Randomization
- New OS use randomized MAC address when probing
	- Prevents listeners from building a device history -> protects user privacy

## Bluetooth
- Wireless technology using Radio Frequency (RF) to share data over short distance
- Replaces the need for cables connecting electronic devices
- Designed for communicating in distances <10m or <30ft.

## Piconet & Scatternet
- When Bluetooth devices automatically detect & connect to one another, max 8 can communicate at 1 time
- 2+ Bluetooth devices -> ad-hoc -> piconet
	- 2+ separate piconets join -> scatternet
![[Pasted image 20220509211426.png]]

## Master/Slave Concept
- 1 master device can connect to 7 slave devices
- Master can send & request data from any slave devices
- Slave can only transmit to master & receive from master

## Bluetooth Connection Process
1. Inquiry: If 2 Bluetooth devices know nothing about each other, they run inquiry to discover the other
2. Paging (connecting): Forming connection between 2 devices
3. Connection: After completing Paging state
	- Active
	- Sniff
	- Hold
	- Park

## Bonding & Pairing
- If 2 Bluetooth devices share special affinity for each other
- Automatically establish connection when in range
- Bonds created through 1-time process: **Pairing**
	- Devices share addresses
		- Names
		- Profiles
	- Stored in memory


## Bluetooth Versions
- Iteration over previous versions typically has the following benefits:
	- Data transfer speed increase
	- Connection range increase
	- Connection stability enhanced
	- Energy consumption reduced
	- Security features improved

### Bluetooth 1.X
- Suffered from many problems, which were completely fixed in Bluetooth 1.2
- 1.0 => 1.2:
	- Adaptive Frequency-Hoppinh spread spectrum (AFH)
		- Reduces interference
		- Faster transmission speeds (721kbits/s)
		- Faster connection
		- Faster discovery

### Bluetooth 2.X
- 1.2 => 2.0:
	- Support for Enhanced Data Rate (EDR)
- 2.0 => 2.1:
	- Added support for Secure Simple Pairing (SSP)
		- Improves security
		- Improves pairing experience
	- Extended range (10m -> 33m)
	- Enhanced data transfer speeds (0.7Mbps -> 3Mbps)

### Bluetooth 3.X
- 2.1 => 3.0:
	- High Speed (HS) mode
		- Theoretical data transfer speeds up to 24Mbps over 802.11 link
		- ***Drawback***: High power consumption
			- Shorter battery life in Bluetooth-enabled devices

### Bluetooth 4.X
- 3.0 => 4.0:
	- Introduced Bluetooth Low Energy (BLE)
	- Added backwards compatibility for features in previous BT versions
		- Reduced power consumption 
- 4.0 => 4.2:
	- Enabled the creation of Internet of Things (IoT) due to:
		- Low Energy Secure Connection w/ Data Packet Length Extension

#### Bluetooth Low Energy (BLE)
- Known as Smart Bluetooth in ^BT4.X
- Consumes much less energy
	- Only consumes when active
- Suitable for devices that require periodic data transfer (Fitbit)
- 3ms latency vs 100ms for typical BT devices

### Bluetooth 5.X
- 4.2 => 5.0:
	- Improved IoT connectivity & experience
		- Seamless data flow
	- BLE:
		- Increased speed to 2Mbps
		- Extended range (LE Long Range)
	- Added Angle of Arrival (AoA) & Angle of Departure (AoD)
		- Used for location & tracking of devices


#### Angle of Arrival (AoA)
- Principle of measuring angular directions (Azimuth & Elevation) from devices placed in a known location
- System features antenna array on receiver
	- Measures phase-shift of incoming signal to find direction

#### Angle of Departure (AoD)
- Uses antenna array to direct transmitted signal in given angle
- Principle:
	- Device with multiple antennas (array) sends signal to device with single antenna
	- Device with single antenna receives all signals from separate antenna thru single antenna
	- Receiver analyzes difference between angles formed to estimate relative signal direction from where signals departed


## Bluetooth Addresses
- Each BT device has unique 48-bit address (BD_ADDR)
	- 24 bits OUI
	- Last 24 bits:
		- NAP: Non-significant Address Part. Used in Frequency Hopping Synchronization frames
		- UAP: Upper Address Part. Used for seeding in various BT spec algorithms

![[Pasted image 20220509213837.png]]


## Bluetooth Address Types
- Public: Global fixed address which needs to be registered with IEEE
- Random: More popular since there is no need for IEEE registration

![[Pasted image 20220509213811.png]]

### Random Static Address
- Popular alternative to Public addresses -> no fees
- Can be assigned and fixed for the lifetime of device OR
- Can be changed at bootup
- ***Cannot be changed during runtime***

### Resolvable Random Private Address
- To prevent 3rd parties from tracking BT device
- Resolvable using key shared with trusted device (IRK -> Identity Resolving Key)
- This address will change periodically

## Ultra-Wide-Band (UWB)
- Short-range wireless communication protocol
- Fast, secure, low-power radio protocol 
- Used to determine location 
- Best accuracy compared to any other wireless technology