# Switches & Bridges
- Switches operate on the Data Link layer, as with bridges
	- Switches also manage a MAC table:
```markdown
| Port | MAC   |   |   |   |
|------|-------|---|---|---|
| 6    | CC:CC |   |   |   |
|      |       |   |   |   |
|      |       |   |   |   |
```
- Bridge: 
	- Bridges are hard to find as an individual device and are instea bundled with router/modem combo
	- Layer 2 switch: MAC Address
	- Layer 3 switch: IP Address
	- Layer 4: Ports & Protocols (rare)
		- i.e. Layer 4 switches have access to Layer 1-4 information
	- Connects two (or more) different networks together 
	- Bridge vs Switches: Bridge links 2 networks together, while switch works *within* the network
- Message is usually called **Payload**
	- If the message is added at the start of the *payload*, it's a **Header**
	- If the message is added at the end of the *payload*, it's a **Trailer**
- Headers can include:
	- *Source MAC Address:* The source address of the device that wants to send data
	- *Destination MAC Address:* The destination address of the device that receives the data 
If the Destination MAC Address is not known, then the sender will put FF:FF:FF:FF as the destination address. That's called the *Broadcast Address*.

Some switches operate in Unicast, and some in multicast:
	- Unicast: One-to-One (one source to one destination)
	- Multicast: One-to-Many (one source to multiple destinations)
	There is no designation for Many-to-Many applications 
