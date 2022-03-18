# Session Layer (Layer 5)
- Initiating setup and tearing down connections
	- Tries to determines if the process stays local or requires a network connection
		- Tries to initiate connection if required
- Responsible for differentiating multiple network connections to ensure that data is sent to the correct connection and then forwarding that data to the correct application
- ***The mechanics of the process is contained inside the [[Transport Layer (Layer 4)]]***
- Reponsible for error reporting for [[Application Layer (Layer 7)]], [[Presentation Layer (Layer 6)]], [[Session Layer (Layer 5)]] 
- Responsible for implementing any class of service (*CoS*) for application 
- Responsible for traffic / connection prioritization

TLDR; Setting up, maintaining & tearing down network connections (E.g. RFC & NFC)
#advnetmidterm 