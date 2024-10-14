- ![02_Principles_Layers.pdf](../assets/02_Principles_Layers_1695732186774_0.pdf)
- DONE Incorrect slides uploaded to learn
- ![03_Link_Network.pdf](../assets/03_Link_Network_1695849907038_0.pdf)
- ![04_Application.pdf](../assets/04_Application_1695732194155_0.pdf)
-
- # Network Principles
	- Reading: 222-228, 230-231,240-241
	- ## NetSec Concepts
		- ### Internet Protocol Layers
			- Physical 
			  logseq.order-list-type:: number
				- Wiring 
				  logseq.order-list-type:: number
				- Radio Transmission
				  logseq.order-list-type:: number
			- Link 
			  logseq.order-list-type:: number
				- Routing Paths in Local Area Network
				  logseq.order-list-type:: number
				- Uses MAC
				  logseq.order-list-type:: number
			- Network/Internet 
			  logseq.order-list-type:: number
				- Individually addresses every host with an IP
				  logseq.order-list-type:: number
				- Not all packets Make it through
				  logseq.order-list-type:: number
			- Transport
			  logseq.order-list-type:: number
				- Support Communication between IP and ports
				  logseq.order-list-type:: number
				- TCP
				  logseq.order-list-type:: number
				- UDP
				  logseq.order-list-type:: number
			- Application
			  logseq.order-list-type:: number
				- HTTP
				  logseq.order-list-type:: number
			- This was created by a time when the internet was used with no mal-intent
		- ### NetSec Issues
			- Confidentiality
			- Integrity
			- Availability
			- Assurance
			- Authenticity
			- Anonymity
	- ## Ethernet
		- ### Hubs (Ethernet Hubs)
			- Logically connects multiple devices
			- They become a single network segment
			- They (typically) forward all frames to all the devices
			- Inefficient, large amounts of unnecessary traffic
			- Easy to eavesdrop
		- ### Switches
			- Better Hubs
			- Originally work the same
			- Over time learn the addresses of the connected machines, become more efficient
			- More secure, less likely for eavesdropping to occur
	- ## Encapsulation
		-
	-
- # ARP/TCP/IP and Vulnerabilities
	- Reading: 232-237, 242-243, 246, 248-250, 253, 256-258, 261
	- ## Media Access Control (MAC)  Addresses
		- ((6512d65f-f6fb-4d39-82bd-279481966c11))
		- First 24 bits are issued by IEEE are for Organisation that issued address
		- ((6512d6d0-f24c-4252-a3cb-681bb34c9e53)) for remaining bits
		- Network Specific MAC address can be assigned by changing ((6512d738-f415-49ea-9931-7e013b1b28a2))
		- As they are so easy to change, they cannot be used of identifying an untrusted source
	- ## ARP (Address Resolution Protocol)
		- The resolution of IP addresses into MAC
		- "Who has IP 192.168.1.105?"
			- "192.168.1.105 is at 00:16:B7:29:E4:7D!"
		- ### ARP Cache Poisoning Attack (Spoofing)
			- ARP lacks authentication
			- Any machine that receives an ARP reply will automatically update its cache
			- This establishes a man-in-the middle scenario
			  ((6512f368-e405-43ea-bce6-0b29b30af0af))
		- ### Preventing ARP Spoofing:
			- Restrict LAN access to trusted users
			- Check for multiple occurances of the same mac address
			- Static ARP tables
				- Have to manually add each user
				- Does not prevent MAC spoofing
			- For flexible (and complex) defence, specialized software is used
	- ## IP
		- If the packet is addressed to a machine on the same LAN, then it is transmitted directly through LAN
		- If not it is transmitted through the gateway, (MAC saved in ARP)
		- It is sent along a series of routers
		- Routers use routing tables to determine next router it should go to
		- To avoid infinite loops a is given so that it only passes through a certain number of routers
-
- # Application-Layer and DNS
	- ## DNS
		- ### URL
			- Uniform Resource Locators
			- Standardized format for describing location and access method
			- They are a bit confusing:
			  ((6513f21e-3eb1-45d9-8b8f-1a1caf82fac7))
		- ### Domain Name Registration
			- Generic top-level domains   .com .edu
			- Country code top-level domains .au .uk
			- Registration is simple
				- Small fee charged by registrar
				- Give contact details
			- These details are public, can be used in a social engineering attack
			- ((65149b72-e1d5-4211-91d9-9b72a3b4c0ba)), anticipating that a corporation will want to purchase domain and holding them "ransom" to seek profit
		- ### DNS Mapping
			- Maps domain names to IP addresses
			- Top-level domain is stored on servers operated by ICANN
			- ww.ed.ac.uk maps to 1 IP, google.com maps to Many IPs
			- Other Mappings:
			- Address (A)
			  logseq.order-list-type:: number
			- Mail Exchange (MX)
			  logseq.order-list-type:: number
			- Name Server (NS)
			  logseq.order-list-type:: number
		- ### DNS Tree
			- Root Domain = .
			- Top-Level = com, edu, uk
		- ### Servers
			- Keeps Local rcords of dns
			- Answers Queries
			- Asks other servers if record is not in local database
			- Authoritative Name Server stores reference version of DNS for a zone
			- ### Resolution
		- ### DNS Packet
			- Queries and replies use UDP
			- TCP is used for large requests (over 512 bytes)
			- Query consists of wanted domain name and type of recor
			- Answer consist of:
				- Domain name
				- Type of record
				- Class (Broad category)
				- TTL How long record is valid
				- RDLENGTH Length of data segment
				- Record data e.g. IP address of requested domain
	- ## DNS Cache
		- ### Servers
			- Essentially Dynamic programming
			- Low-level servers keep records for a certain period of time so that high-level servers are not overloaded
		- ### OS
			- Cache shared among all running apps in OS
			- can be seen using 
			  ```apl
			  ipconfig /displaydns
			  ```
			- Linux does not have cache
			- Cache still saved even if using incognito
		- ### DNS Attacks
			- Pharming 
			  Sending DNS response so that user connects with malicious IP
			- Cache Poisoning
			  Eve sends requests to dns server, and simultaneously a spoofed "response" from server. 
			  Server now maps website to malicious IP
			- Subdomain Cache Poisoning
			  In essence is advanced Cache Poisoning
			  Spam request of for non-existent subdomain
			  Send many responses, one will be correct
	- ## DNSSEC
		- Didn't take off, too much overhead
-
- # Firewalls
	- Reading: 287-291, 299-303, 305-311
	- ## Firewalls
		- #### Policies
			- Accepted:
			  Permitted through Firewall
			- Dropped: 
			  Not allowed
			- Rejected:
			  Not allowed through, source is informed
		- ### Blacklist
			- Default-allow
			- Flexible
			- Network admin wont be able to stop all malicious traffic
		- ### Whitelist
			- Default-deny
			- Very secure
			- Require greater familiarity with protocols
		- ### Stateless firewalls
			- No memory of context
			- No memory dedicated to determining if a packet is part of an existing connection or not
			- Require very little overhead
		- ### Stateful Firewalls
			- Only allows packages that are in an already established connection or a handshake
			- Once connection is terminated, rejects any more packages
			- This works well for TCP
			- UDP needs to have a "session" created.
				- Sessions begin after first UDP packet comes through
				- Until a specified time is reached (how is it specified)
			- Allows admins to apply more restrictive rules
	- ## Intrusion Detection
		- ### Intrusions
			- Masquerader - flase identity/credentials
			- Misfeasor - legit user who performs actions he is not authorized to do
			- Clandestine - user who tries to cover his tracks by deleting logs
		- ### IDS (Intrusion Detection System)
			- Can detect the following:
				- Port scans - attack reconnaissance to see which port allow TCP
				- DoS
				- Malware
				- ARP spoofing
				- DNS cache poisoning
			- IDS attacks- overwhelm IDS with attacks, making it hard to log all attacks
		- ### Intrusion Detection Events
		-
		- ### Honeypots
		-
	- ## Tunneling (not in reading lol)
		- *End to End Encryption*
		- ### SSH (Secure Schell)
			- Is used by SCP (Secure Copy Protocol) and SFTP (Secure file Transfer Protocol)
			- Main used is for secure tunneling
			- How it works:
			- Client connects to server via TCP session
			  logseq.order-list-type:: number
			- Exchange admin details: Encryption method, protocol version, etc.
			  logseq.order-list-type:: number
			- Initiate secret-key exchange
			  logseq.order-list-type:: number
			- Server sends list of valid authentication method
			  logseq.order-list-type:: number
			- Once authentication is successful server lets client access appropriate resources
			  logseq.order-list-type:: number
			- 4. can also work in the following way through the public key authentication
			- Client sends server a public key
			  logseq.order-list-type:: number
			- Server checks key is authorized
			  logseq.order-list-type:: number
			- Server encrypts challenge and sends to client
			  logseq.order-list-type:: number
			- Client decrypts challenge with private key and responds to server
			  logseq.order-list-type:: number
		-
		-