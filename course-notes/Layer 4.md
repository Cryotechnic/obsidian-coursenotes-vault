# Layer 4
## Transport Layer
- Port range is defined as a 16-bit unsigned integer
- Port Number: Indicates the type of data transmitted
- There are 2 port types:
	- < 1024: Well-known, fixed, ports:
		- E.g.:
			- SSH: 22
			- FTP: 21
			- HTTP: 80
			- HTTPS: 443
	- > 1024:
		- Registered Ports: 1024-49151
		- Dynamic Ports: 49152-65535
## Protocols:
### TCP:
- Connection-oriented
- Sender must provide packet reception verification
- More reliable
- Handshake:
	- Sender sends message (SYN (synchronization packet))
	- Receiver sends SYN ACK when ready 
	- Sender sends ACK when SYN ACK is received
	- Data stream and transfer begins when SYN ACK is received
This handshake model is general, some of them have more verification for reliability.
This process is time-consuming and requires more resources than UDP

Handshakes can be exploited to create a Denial-of-Service (DOS) attack by sending TCP request packets (SYN) without replying anything to them when the server responds with SYN ACK 
### UDP:
- Connection-less
- Sender does not need to provide packet reception verification
- Faster & lighter

