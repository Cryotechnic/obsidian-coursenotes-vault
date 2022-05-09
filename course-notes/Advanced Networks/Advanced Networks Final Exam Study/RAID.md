# Raid
- Min # of HDD
- Security
- Capacity

### Basic - Static
### Dynamic - More than 1 HDD

## Raid 0
- Minimum amount: More than 1
- Data is split among all drives
- No parity


## Raid 1
- Minimum amount: Even number of HDD ()
- Access to half (50%) of installed capacity to user (maximum capacity)
	- The other half (remainder) is reserved for system (parity)

## Raid 5
- Minimum amount (maximum capacity): *n - 1*
- Data is split among all drives according to XOR:
	| Input | Output |     |     |
	| ----- | ------ | --- | --- |
	| A     | B      | P   | Q   |
	| 0     | 0      | 0   | 0   |
	| 0     | 1      | 0   | 1   |
	| 1     | 0      | 1   | 1   |
	| 1     | 1      | 1   | 0   |


XOR
- If # of 1s is even, XOR = 0
- If # of 1s is odd, XOR = 1
- Maximum amount of failed drives: 1

#advnetfinal 