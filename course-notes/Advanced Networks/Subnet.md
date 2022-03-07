## Subnet Mask
- Indicates the range of the operating network
- Subnet Mask is 32-bits
	- Comprised of 2 sections:
		- Network:
		- Host:
			- Number of possible members in the network: *2^Host*
			- E.g. 192.168.0.X /24 = 32 - 24 = 8, therefore 2^8 = *256 hosts*
				- You *always* need to subtract 2 from the hosts, **to account** for the network & broadcast address
	- 192.168.1.2 /24 is **not the same as** 192.168.1.132 /24  
- Structure of subnet mask is similar to IP address
- Default subnet masks:
	- Class A: 255.0.0.0 /8 (11111111.00000000.00000000.00000000)
		- Network: 2^8 (256)
		- Host: 2^24 (16777216)
		- Private: 10.X.X.X
	- Class B: 255.255.0.0  /16 (11111111.11111111.00000000.00000000)
		- Network: 2^16 (65536)
		- Host: 2^16 (65536)
		- Private: 172.16.X.X OR 172.31.X.X
	- Class C: 255.255.255.0 /24 (11111111.11111111.11111111.00000000)
		- Network: 2^24 (16777216)
		- Host: 2^8 (256)
		- Private: 192.168.X.X
- Octets that are "1" are considered to be *Network* address
	- __Look at the above representation for examples!__
- Octets that are "0" are considered to be *Host* address
- /8, /16, /24 (subnet mask) delimits how many octets have to be identical to be considered as part of the same network
	- /8 means that the first octet needs to match
	- /16 means that the first 2 octets need to match
	- /24 means that the first 3 octets need to match
	- If this condition is not true, then they do belong on the same network


## Examples / Practice
- Assume the following:
	- LAN 1: 192.168.1.X /24:
		- Network Address: *192.168.1.0 /24*
			- 192.168.1.00000000 -> 192.168.1.0
			- 192.168.1.00000001 -> 192.168.1.1
			- 192.168.1.11111111 -> 192.168.1.254
		- Broadcast Address: *192.168.1.255 /24*
	- LAN 2: 192.168.2.X /24:
		- Network Address: *192.168.2.0 /24*
		- Broadcast Address: *192.168.2.255 /24*
## Subnetting
### Determining custom Subnet Mask
- To determine a "custom" subnet mask (/25, /28, etc.), divide the total amount of hosts by the amount of networks that we want to create, then find the scientific notation of 2 for it.
- Finally, subtract the power notation from the resulting number to obtain the subnet mask
- Then, define the IP range for the network
- E.g. Create 8 subnetworks
	- 256/8 = 32
	- 2^x = 32, x-> 5
		- 32 - 5 = 27
Therefore
- 192.168.0.0 -> 192.168.0.31 /27
- 192.168.0.32 -> 192.168.0.63 /27
- 192.168.0.64 -> 192.168.0.95 /27
- 192.168.0.96 -> 192.168.0.127 /27
- 192.168.0.128 -> 192.168.0.159 /27
- 192.168.0.160 -> 192.168.0.191 /27
- 192.168.0.192 -> 192.168.0.223 /27
- 192.168.0.224 -> 192.168.0.255 /27