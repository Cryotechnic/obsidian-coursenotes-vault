# Routing Protocols
# Distance Vector (D.V Protocols)
| Metric                      | Routing Protocol | Description                                                             |
| --------------------------- | ---------------- | ----------------------------------------------------------------------- |
| Bandwidth                   | EIGRP            | Capacity of links in Kbps (T1 = 1554)                                   |
| Cost                        | OSPF             | Arbitrary values on each node allowing admins to alter network paths    |
| Delay                       | EIGRP            | Time it takes to reach destination                                      |
| Hop Count                   | RIP              | How many [[Network Layer (Layer 3)]] hops it takes to reach destination |
| Load                        | EIGRP            | Path with least utilization                                             |
| MTU (Max Transmission Unit) | EIGRP            | Path that supports largest frame size                                   |
| Reliability                 | EIGRP            | Path with least errors & downtime                                       | 

## Advertising Updates
- Mechanism by which routing protocols share routing & reachability information with neighbors 
	- Advertising updates are run on a specific timer, regardless of any changes
- Routers running DV protocols learn who neighbors are by listening for routing broadcasts on their interfaces
	- Assume that through the broadcast process, neighbors will be learned
		- If fails, missing broadcasts will eventually be detected
		- If router misses an update, they'll get it next update

## Processing Updates
1. Increment metrics of the incoming routes in the advertisement  (Add 1 to hop count for RIP)
2. Compare network numbers in routing update from neighbor to what current router has in routing table
3. If neighbor information is better, update routing table
4. If neighbor information is worse, ignore it
5. If neighbor information is the same, reset timer entry in routing table
6. If neighbor information is different path, router adds it to routing table alongside the old entry

# Link State Protocols (LS)
- LS use multicasts for routing information (compared to local broadcasts for D.V)
- Link State Advertisement (LSA)
	- Only ran once there is a change detected in the network (much more resource-)
		- LSA update:
			- Destination router sends an ACK to source router
- More CPU & memory-intensive than D.V protocols but are more network-friendly in return
- Very scalable due to route summarization & hierarchical routing

# Problems
## Distance Vector
### Convergence
- When all routers understand the topology of the network
	- Slow on DV if large network because it takes more time to discover all nodes
	- Solution: Triggered updates
		- Forcing DV to run at specific intervals, or modify the periodic timer interval

### Routing Loops
- Disagreement on how a destination network should be reached
	- Solution: Split Horizon
		- If a neighboring router sends a route to a router, the receiving router will *not* propagate the route back to hte advertising router on the same interface
	- Solution #2: Poisoned route & hold-down timers
		- Hold-down timers are used to make sure that the poisoned route propagates in the network
			- Slows down convergence
		- Poisoned route: if route has failed, router will set infinite metric to it (RIP -> hop count = 16, thus unreachable since 15 is max)