# Transport Layer (Layer 4)
- Ensures the setup, maintenance and teardown of:
	- Reliable connections:
		- Error detection & correction
			- [[Transport Layer (Layer 4)]] will resend the data, providing a correction in the process
		- TCP/IP
	- Unreliable connections:
		- Error detection *only*
			- Error correction is left typically to [[Application Layer (Layer 7)]]
		- UDP
- Manages timeout issues, notifications, hello packets (used to determine connection issues), etc.
The [[Transport Layer (Layer 4)]] therefore can be described as the *delivery mechanism* for moving information (at the transport layer), between different network components

TLDR; The [[Transport Layer (Layer 4)]] provides guaranteed & unguaranteed data delivery. Efficient delivery is provided through *sequencing*, *acknowledgment* & *flow control*. UDP & TCP/IP are included in the [[Transport Layer (Layer 4)]]

## Layer Functions
- Setup, maintenance & teardown of connection between two (or more) components
- Provides reliable / unreliable delivery of information through connection
- Provides data segmentation (divides data into chunks that can be delivered over the network)
- Multiplexing of connections (allows for multiple applications to send / receive data at the same time on the same network device)
- Implements flow control (ready / not-ready signals or windowing to prevent data overflow. ). These methods typically use buffering and are implemented to avoid congestion on a network

### Reliable Connections
- TCP / IP is a *reliable connection* implementation
- Reliable Connections typically use *sequence numbers* & *acknowledgments* (*ACKs*)
	- Destination examines sequence numbers in transmitted segments to determine if something is missing
		- Also used to re-assemble transmitted data in the correct order
	- If data is corrupted / chunks are missing **destination** can request that source re-sends the information that is missing, or the entire information, depending on protocol
- Some Reliable Connections use *handshakes*
	- When initially establishing connection
	- Used to obtain information regarding if both networking devices can build the connection & negotiate parameters used to provide a reliable connection
		- ***Three-way handshake*** is the name of the TCP / IP handshake

### Unreliable Connections
- Used when *handshake* process is not required because it adds more delay (e.g. DNS query)
	- DNS Example:
		- Need to find FQDN (fully qualified domain name)
			- Client query <=> server response
				- If there is no response, the client can just query again, so there is no loss of information and therefore a handshake is not required 

### Segmentation
- Information transferred between networking devices & transport layer is called *segment*
- Segmentation required to break up large data into a size that is manageable for the network
- **Segments are used to transport information at the transport layer**

### Connection Multiplexing
- Required when there are multiple network application or devices running on the same network
- Transport layer assigns unique set of *ports* or *socket numbers* for each connection
	- Source port & destination port are assigned for each connection
		- Destination port assigned by source device can be *reserved* (0-1023) or *well-known* (1024-65536)
	- Each connection has a *different* port number
- ***Transport layer uses source & destination port numbers and layer 3 logical addresses to perform multiplexing of connections***


### Flow Control
- Used to ensure that components do not send too much information (which can cause a buffer overflow & lose information)
- **Ready / not ready signals**:
	- When destination receives more traffic than possible, can send a *not-ready* signal to source => source will stop transmitting data
	- When source receives *ready* signal => starts sending data to destination again
	- 2 problems:
		- Source can still send information while *not-ready* signal is being broadcast, which can still cause information to be lost
		- Destination must wait to receive more information from source after *ready* signal is broadcast due to delay from the source needing to read the signal and start sending data again
	- Because of these problems, **ready / not ready signals** are not commonly used for *flow control*
	- **Ready / not ready signals** can also be calle **start / stop signals** 
- **Windowing**:
	- *Window size* is defined, specifying how much data (segments) can be sent before source needs to wait for another *ACK* from destination
		- Once *ACK* received, next batch of data is sent
	- 2 features:
		- *Window size* dynamically negotiated & re-negotiated during connecting lifetime
			- Ensures optimal window size and reduces bandwidth consumption
		- Through windowing, destination informs source of data received, which can indicate if any data was lost & allows source to re-send information in that way
			- Better reliability & efficiency than **ready / not ready signals**
- *Window Size* affects efficiency & throughput (bandwidth)
- Destination can send *ACK* in different ways:
	- Send back list of sequence numbers received
	- Send back next expected sequence number  
- ***The purpose of flow control is to ensure that the destination does not get overrun by too much information sent by the source***

***Ready / not ready signals & windowing are used to implement flow control at the transport layer. R / NR signals are less efficient, causing drops of traffic & delays in transmission, which windowing does not have. Windowing establishes window size, defining the number of segments that can be transferred before waiting for an ACK from destination.***

#advnetmidterm 