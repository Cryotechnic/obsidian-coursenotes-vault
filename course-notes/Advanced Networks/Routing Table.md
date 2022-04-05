# Routing Table
{NEED TO ADD PREVIOUS CLASS INFO}

### Router 1 Routing Table
| Type              | Source IP Address | Destination Address | Interface |
| ----------------- | ----------------- | ------------------- | --------- |
| C                 | 192.168.1.0 /24   | 192.168.1.1         | F0/0      |
| C                 | 192.168.2.0 /24   | 192.168.2.1         | F0/1      |
| S                 | 192.168.3.0 /24   | 192.168.2.2         | F0/1      |
| S                 | 192.168.4.0 /24   | 192.168.2.2         | F0/1      |
| S                 | 192.168.5.0 /24   | 192.168.2.2         | F0/1      |
| * (default route) | 0.0.0.0 /0        | 192.168.2.2         | F0/1          |

### Router 2 Routing Table
| Type | Source IP Address | Destination Address               | Interface |
| ---- | ----------------- | --------------------------------- | --------- |
| C    | 192.168.2.0       | Routers only know network address | F0/0      |
| C    | 192.168.3.0       | Routers only know network address | F0/1      |
| C    | 192.168.4.0       | Routers only know network address | F0/2      |
| S    | 192.168.1.0       | 192.168.2.1                       | F0/0      |
| S    | 192.168.5.0       | 192.168.4.2                       | F0/2      | 

C = Connected (Connection has been established with the destination)
S = Static (Manually inserted)

- If modifications to the network are made, all routing tables must be updated as some routing tables contain static routing
- Autonomous System (A.S): Collection of groups of routers that work under the same admin policies and configurations
- Edge Router: Router connected to another Autonomous System (A.S)
- Interior Routing Protocol: Protocol(s) that can only route packets inside the given A.S
- Exterior Routing Protocol: Protocol(s) that can only route packets outside the given A.S
- Distance Vectoring: Routers share their routing tables with their neighbors (better in smaller networks)
- Link State: Each line has its own weight (better in large networks)
	- The algorithm works on the Link State Shortest Path and uses Dijkstra's algorithm to find the shortest path 
Interior Gateway Routing Protocol (IGRP - Cisco)
Enterprise Interior Gateway Routing Protocol (E-IGRP - Cisco)
#### Routing Types
- Static: Manually entered by the network administrator
- Dynamic: Automatically assigned by the system with the following:
	- Distance Vector 
	- Link State



