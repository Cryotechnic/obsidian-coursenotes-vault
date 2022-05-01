# Routing Types
- Autonomous System (A.S): Collection or group of routers that work under the same administration policies and configuration
## Static Routes
- Router will look at all active interfaces to determine network numbers
	- Will populate routing table with that information
	- Typically called *connected / directly connected route*
	- 0.0.0.0 (special static route, *default route*, *gateway of last resort*)
		- If specified destination is not found
## Dynamic Routes
- Router learns dynamic routes by running [[Routing Protocol]]
| Routed Protocol | Routing Protocols                  |
| --------------- | ---------------------------------- |
| IP              | RIP, IGRP, OSPF, EIGRP, BGP, IS-IS |
| IPX             | RIP, NLSP, EIGRP                   |
| AppleTalk       | RMTP, AURP, EIGRP                  |
- Routing Protocol:
	- Routes for Routed Procol
- Routed Protocol
	- Layer 3 protocol (e.g. TCP/IP, Internetwork Packet Exchange (IPX))

## Administrative Distance (AD)
- Ranking for IP routing protocols developed by Cisco (proprietary)
	- The lower it is, the better (when most believable route is a directly connected one)
		- Connceted (0)
		- Static (0/1)
		- EIGRP (90) (Internal)
		- OSPF (110)
		- RIP (120)
		- EIGRP (170) (External, from another A.S)
		- 255 (Unknown route (considered invalid and will not be used  ))