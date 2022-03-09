# Routing Protocol
## Distance Vector (DV)
- The most used distance vector-based algorithm is RIPv2 (Routing Information Protocol)
- The router chooses the minimum distance (minimum hops)
	- Hops: # of routers
## Link State (LS)
- The most used link state-based algorithm is OSPF (Open Shortest Path First)
- Router considers the *speed* & *traffic* of a route before sending packets through a given route
- Typically better for long-range since it is more time-consumming to send data
## Border Gateway Protocol (BGP)
- Protocol for the global routing system of the internet

## Ping vs Traceroute (tracert)
- Ping finds if the server is reachable by sending a packet to the destination server and waits for a reply
- Traceroute finds the exact route that the packet travels to reach the destination server
	- It is considerably slower but much more useful for troubleshooting
		- Slower because it returns a reply each time it goes through a router
## What to do if you want to create networks with variable size?
E.g. 
- Given IP is 192.168.1.0 /24
	- H.R.: 64
		- 64 = 2^6 => Host = 6
			- 32 - 6 = 26
				- Network: 192.168.1.127 /26
				- Broadcast: 192.168.1.191 /26
	- Accounting: 32
		- 32 = 2^6 => Host = 5
			- 32 - 5 = 27
				- Network: 192.168.1.192 /27
				- Broadcast: 192.168.1.223 /27
	- Cont. Ed.: 8
		- 8 = 2^3 => Host = 3
			- 32 - 3 = 29
				- Network: 192.168.1.224 /29
				- Broadcast: 192.168.1.231 /29
	- Management: 4
		- 4 = 2^2 =>Host = 2
			- 32 - 2 = 30
				- Network: 192.168.1.232 /30
					- Broadcast: 192.168.1.235 /30
	- Teachers: 128
		- 128 = 2^7 => Host = 7
			- 32 - 7 = 25
				- Network: 192.168.1.0 /25
				- Broadcast: 192.168.1.127 /25
## Variable Length Subnet Mask (VLSM)
