## IP Address
- Address type is the IP Address
- 2 versions
	- IPv4:
		- Cannot have the same address in the same network
		- 32-bit address
		- Maximum is **4,294,967,296** addresses
		- Each section is an octet (group of 8 bits), who's numbers range from 0-255 inclusively
		- 4 octets comprise the IPv4 address range
		- Valid IP Addresses:
			- 121.2.100.254
			- 2.4.4.2
			- 192.168.0.1
		- Invalid IP Addresses:
			- 301.1.2.3
			- 257.2.1.100
		- IP Address classes:
			- The first octet determines the class
				- A: 1-126 (7.100.2.1)
				- B: 128-191 (190.2.100.7)
				- C: 192-223 (193.2.1.1)
				- D: 224-239 (221.1.4.9)
					- Used to [[Multicast]]
				- E: 240-255 (243.123.56.12)
					- Reserved but not really used nowadays
			- Where is 127?
				- It's the *loopback* address, commonly known as *localhost* (127.0.0.1)
	- IPv6: Not covered
## Public & Private IP
- Public: Anything that is not private, by default everything is assumed as public unless stated otherwise
- Private:
	- Class A: *10.0.0.0* to *10.255.255.255*
	- Class B: *172.16.0.0* to *172.31.255.255*
	- Class C: *192.168.0.0* to *192.168.255.255*
	- Used inside a local network and are invalid for outside use
Anything that is outside of this range is considred as **public**

