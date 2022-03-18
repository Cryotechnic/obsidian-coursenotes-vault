# Encapsulation & De-encapsulation
- Process Data Unit (*PDU*) is the general term used for data & headers / trailers it has
- Encapsulation:
	- Process that occurs when information passes from higher => lower layers
- De-encapsulation:
	- Process that occurs when information passes from lower layers => higher

| PDU Term | OSI Reference Model Layer                                                                      |
| -------- | ---------------------------------------------------------------------------------------------- |
| Data     | [[Application Layer (Layer 7)]], [[Presentation Layer (Layer 6)]], [[Session Layer (Layer 5)]] |
| Segment  | [[Transport Layer (Layer 4)]]                                                                  |
| Packet   | [[Network Layer (Layer 3)]] (TCP / IP calls it *datagram*)                                     |
| Frame    | [[Data Link Layer (Layer 2)]]                                                                  |
| Bits     | [[Physical Layer (Layer 1)]]                                                                                               |

***When sending traffic between 2 devices on different segments, the source device has [[Data Link Layer (Layer 2)]] frame with its own MAC address and the default gateway's (router) MAC address as the destination address. This changes to router's source address (IP) and destination IP as destination address***