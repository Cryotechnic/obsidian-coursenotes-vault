# VLANs & Trunking
| Protocol        | Number of Devices |
| --------------- | ----------------- |
| IP              | 500               |
| IPX             | 300               |
| NetBIOS         | 200               |
| AppleTalk       | 200               |
| Mixed Protocols | 200               | 

### Trunking Methods for Cisco 
- ISL Protocol (Proprietary)
	- Only between specific supported Cisco devices
- 802.1Q (dot1q)
	- Allows between different vendors' devices
	- Tagged frames:
		- 
	- Untagged frames:
		- Does not carry any VLAN identification within it
			- Same thing as a standard Ethernet frame
		- VLAN membership controlled based on the port by which it is connected to
			- If switch's port is connected to VLAN 1, frame will belong to VLAN 1, etc.
				- Called *native* VLAN
	- You can have **both** tagged & untagged on the given trunk connection

### Frame Process for 802.1Q
![[Pasted image 20220430213145.png]]

- Advantage of using tagging:
	- Frame size will not exceed 1518 bytes
		- Means that you can forward the frame through access link connection of switches
## VLAN Trunk Protocol (VTP)
- Cisco-proprietary protocol that traverses trunks
- Used to create consistent VLAN configuration across all switches of the same Domain
- Switches will ignore VTP messages from other VTP domains that is not their domain

| Property                       | Server | Client | Transparent |
| ------------------------------ | ------ | ------ | ----------- |
| CRUD VLANs                     | Yes    | No     | Yes         |
| Generate VTP Messages          | Yes    | No     | No          |
| Propagate VTP Messages         | Yes    | Yes    | Yes         |
| Accept changes in VTP messages | Yes    | Yes    | No          |
| Default VTP Mode               | Yes    | No     | No          |
| Save VLANs to NVRAM            | Yes    | No     | Yes         |

## VTP Messages
- Generated by client to acquire information
	- Server response contains *subset advertisement*
		- Detaile VLAN configuration information
			- VLAN numbers
			- Names
			- Types
			- Etc.
	- *Summary Advertisement*
		- Generated when switch is in Server mode
			- Every 300 seconds by default
			- Also when configuration change on server switch
		- Contains only summarized VLAN information
			- VLAN numbers
			- Names
			- Maximum Transmission Unit (MTU) Size
			- Securit Association ID (SAID) 
				- Required if VLAN is 802.10, implemented using FDDI
			- Configuration revision number
			- Name of VTP domain

## VTP Pruning
- Delete or add VLANs to trunk
- Dynamic Pruning automatically removes inactive VLANs 
- VTP Pruning must be enabled on VTP server switch & other switches must be servers/clients
#advnetfinal 