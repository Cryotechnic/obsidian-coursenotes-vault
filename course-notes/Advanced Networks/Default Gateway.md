# Default Gateway
- It is essentially one side of the router that is connected to a given network
- Requires an [[IP Addresses]]
- Very common that the IP Address assigned to the default gateway is the first available one, but **it is not required**
- You do not need MAC address when sending data outside of LAN
	- Only the MAC address of the default gateway is required
- Gateway (as the name implies), connects the Internet to the LAN

### Why do we need a default gateway?
## Address Resolution Protocol (ARP)
- ARP should be used when you know the sender & receiver IP Address, but you don't know the destination MAC Address of the device

### ARP Request Example
> IP # 192.168.2.101
> (Requesting MAC Address for) 192.168.2.101, send to 192.168.2.100
> Destination MAC Address is set to Broadcast (FF:FF:FF:FF)
> Device that has corresponding IP address replies with their MAC address

After the ARP request/reply has been fulfilled, the information is cached inside the device's internal ARP Cache

## Network Address Translation (NAT)
- Maps IP address from one space into another (can be public -> private or private -> public)
