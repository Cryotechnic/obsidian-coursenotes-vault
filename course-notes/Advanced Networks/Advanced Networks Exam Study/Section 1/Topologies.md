# Topologies
- Below are the topologies that are currently implemented in networking:
	- [[Point-to-Point Topology]]
	- [[Star Topology]]
	- [[Extended Star Topology]]
	- [[Bus Topology]]
	- [[Single Ring Topology]]
	- [[Dual Ring Topology]]

| Media Type | Physical Topology                                                | Logical Topology |
| ---------- | ---------------------------------------------------------------- | ---------------- |
| Ethernet   | [[Bus Topology]], [[Star Topology]], [[Point-to-Point Topology]] | Bus              |
| FDDI       | [[Single Ring Topology]],[[Dual Ring Topology]]                  | Ring             |
| Token Ring | [[Star Topology]]                                                | Ring                 |

## Full Mesh vs Partial Mesh
- Full Mesh means that all devices are physically connected to the same piece of wire
- Partial Mesh is a cabling method to reduce cost by connecting certain devices together
	- Can introduce increased latency because of missing links

***The formula to determine the number of links needed to fully mesh a network is*** *(N x (N - 1)) / 2*

#advnetmidterm