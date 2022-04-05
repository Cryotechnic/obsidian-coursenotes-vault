# Network Layer (Layer 3)
- Provides logical topology for network using logical / layer 3 addresses
	- Used to group networking components together
- Network has 2 components:
	- Network
	- Host
- **Network**:
	- Used to group 2 components together
	- 4 functions:
		- Define logical addresses used at level 3
		- Find paths based on network numbers of logical addresses to reach destination components
		- Connect different [[Data Link Layer (Layer 2)]] types together (e.g. Ethernet, Fiber Distributed Data Interface (*FDDI*), serial, Token Ring)
		- Define segmentation via packets to transport information at [[Network Layer (Layer 3)]]
- *Router* is required to move information from devices that have different network numbers
	- Uses information to make intelligent decisions on how to reach given destination 
***[[Network Layer (Layer 3)]] provides logical topology to define layer 3 addresses and finds best paths from source to logical address destination. Routers are responsible for packet switching & selecting paths. (e.g. TCP / IP, IPX, AppleTalk***

## Layer 3 Addressing
- 2 components:
	- Network
	- Host (node)
		- Requires unique host number from within assigned network number
- IP addresses are *32 bits* in length 
- IPX addresses are *48 bits* in length

## Routing Tables
- Tables which contain path information
	- Network number
	- Interface router should use to reach network number
	- Metric of path (cost) => bandwidth, delay, hop count
		- Used to rank each link to determine best path
	- How that information was learned
	- Information age
	- Best rank gets appended to [[Routing Table]]
- TCP / IP Routing Information Protocol (*RIP*) uses hop count
- When router receives inbound packet -> examines destination layer 3 address in packet header
	- Router determines logical address and compares it to the one in its routing table
		- If match, forwards packet to destination interface
		- If no match, router drops the packet
***Routers make routing decisions based on network numbers in layer 3 addresses such as TCP / IP addresses. Location of addresses are stored in routing tables.***

### Advantage of Routers
- Build hierarchical networks that scale 
- Prevent propagation of *broadcast* & *multicast*
- Better at connecting different layer 2 technologies together (Ethernet, Token Ring, FDDI, serial, etc.) without conversion issues
- Switch packets on the same interface using virtual LANs (*VLANs*)
- Advanced features allowing the implementation of quality of service (*QoS*) using queueing, traffic shaping, traffic filtering using access control lists (*ACLs*) or encrypting traffic
***Each interface of the router is a separate broadcast & collision domain***
***Bridges & switches do not support hierarchical addressing***

Common tools to troubleshoot layer 3 problems are *ping*, *traceroute* & Address Resolution Protocol (*ARP*)
#advnetmidterm 