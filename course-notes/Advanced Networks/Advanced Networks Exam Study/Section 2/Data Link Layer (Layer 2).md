# Data Link Layer (Layer 2)
- Contains Media Access Control (*MAC*) addresses
- Defines how network components access connected media
- Frame includes fields & components [[Data Link Layer (Layer 2)]] uses to communicate with devices that are on the same layer
- Most WAN protocols function at [[Data Link Layer (Layer 2)]] & [[Physical Layer (Layer 1)]]
- Responsible for taking bits from [[Physical Layer (Layer 1)]] & reassembling them into [[Data Link Layer (Layer 2)]] frames
- Can do error detection but will not correct errors (error correction is done in [[Transport Layer (Layer 4)]]) but some protocols support error correction
- Bridges, switches, network interface controllers (*NICs*) work at [[Data Link Layer (Layer 2)]]
- Responsibility:
	- Define MAC / hardware addresses
	- Define physical / hardware topology for connections
	- Define encapsulation process for the Data Link Layer frame
	- Provind connectionless & connection-oriented services
		- Connection-oriented only if System Network Architecture (*SNA*) is used as [[Data Link Layer (Layer 2)]] protocol => provides sequencing & flow control
	- Verify checksum of received frame to ensure its validity (discarded if invalid)

***[[Data Link Layer (Layer 2)]] defines MAC addresses & communication process. Switches, bridges & NICs function in this layer. Its primary function is to regulate the communication of devices on the same layer 2 protocol & ensures integrity of transmitted frames on the layer.*** 

## Examples of protocols
- LAN:
	- 802.2
	- 802.3
	- 802.5
- WAN:
	- Asynchronous Transfer Mode (*ATM*)
	- Frame-Relay
	- High-Level Data Link Control (*HLDC*)
	- Point-to-Point Protocol (*PPP*)
	- Synchronous Data Link Control (*SDLC*)
	- Serial Line Internet Protocol (*SLIP*)
	- X.25

## Data Link Layer Addressing
- MAC
	- 48 bits represented in hexadecimal
	- Uniquely identifies devices on [[Data Link Layer (Layer 2)]]
	- MAC needs to be only unique within the broadcast domain (includes all layer 2 collision domains)
	- Allows communication between different devices on the same physical network
	- Distribution
		- First 6 bits:
			- Organizationally Unique Identifier (*OUI*)

## Address Types
| Address Type | Description                            |
| ------------ | -------------------------------------- |
| Unicast      | Represents single device on segment    |
| Broadcast    | Represents every device on segment     |
| Multicast    | Represents group of devices on segment | 

### Unicast
- Frame with a destination of only **1** network component

### Multicast
- Represents a group of devices on a segment
- Can contain no device or all devices on a segment
- Membership of group is dynamic (members can leave & join whenever)

### Broadcast
- Intended for every component on a segment to receive
- MAC broadcasts:
	- All bit positions are enabled (FF:FF:FF:FF:FF:FF)
- Used in 2 situations:
	- More effective than unicast
	- Discover unicast address of device
- TCP / IP => ARP is used to discover another device's MAC address

#advnetmidterm 