LAN (Local Area Network) 
A network contained in a relatively small area, e.g., an office floor. 

Switches do not separate lans but adding more switches expands lans. 

OSI Model PDUS 
DATA -> Data 
DATA- L4 header -> Segment
Data - L4 header - L3 Header -> packet 
L2 trailer - Data - L4 header - L3 Header - L2 Header -> Frame 

= Protocol Data Units (PDUs) 

Ethernet Trailer --- PACKET --- Ethernet Header

The Ethernet Header contains 5 Fields:

Preamble -- SFD -- Destination -- Source -- Type Either 7 bytes -- 1 byte -- 6 bytes -- 6 bytes -- 2 bytes

Preamble-> 
7 bytes (56 bits)
Series of alternating 1’s and 0’s (for example 10101010-7 times because 7 bytes)
Allows devices to synchronize their receiver clocks.

SFD
‘Start Frame Delimiter’
Length is 1 byte (8 bits)
10101011 (Bit pattern) 
Marks the end of the preamble and the beginning of the next frame

Destination and Source
Indicates the devices sending and receiving the frame
Consists of the destination and source ‘MAC address’
Mac= Media Access Control
6 byte(48-bit) addresses of the physical device. 

Type / Length 
2 bytes(16-bit) field
A value of 1500 or less in this field indicates the LENGTH of the encapsulated packet (in bytes).
A value of 1536 or greater in this field indicates the TYPE of the encapsulated packet(usually iPv4 or IPv6), and the length is determined via other methods. 
IPv4= 0x0800 (hexadecimal) 				Ipv6= 0x86DD (hexadecimal) 
(2048 in decimal) 						(34525 in decimal) 


Ethernet Frame (Length) 

( it is in bytes) 
7 bytes 
1 byte 
6 bytes
6 bytes
2 bytes
Frame Check Sequence(FCS) 
4 bytes (32 bits) in length 
The purpose is to detect corrupt data by running a “CRC” algorithm over the received data
CYC ‘’Cyclic Redundancy Check’ 


The total length of an Ethernet trailer is 26 bytes(header + trailer) 


Mac Address
6- byte (48-bit) physical address assigned to the device when it is made
Also known as the ‘Burned-in Address’(BIA)
Is globally unique
The first 3 bytes are the OUI( Organizationally Unique Identifier), which is assisted to the company making the device. It is 24 bits long It is the first half of a MAC address
The last 3 bytes are unique to the device itself
Written as 12 hexadecimal characters

Example: E8:BA:70 // 11:28:74 OUI // Unique Device ID



Hexadecimal
Uses 16 possible digits
0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F
A-10, B-11, C-12,D-13,E-14,F-15 
To convert, you divide the decimal number by 16, then subtract the decimal number by 16, the first digit will be the quotient and the second will be the remainder which is gotten after subtracting so for example 23 in hexadecimal is 23/6 which is 1 then 23-16 is 7 so it is 17.


The first collum is equal to 16 thats why 18 is 12 because 1 is 16 and then 2 is 2 so 16+2 is 18 
MAC Addresses 
Unicast frame: a frame designed for a single target

^^^ when the switch learns an address itself and it is not manually configured

Every switch will fill its address table by looking at the source mac address by the frame it receives. 
Switches know where each device on the network is dynamically by looking at the source mac address of the frame. 
An Unknown Unicast frame is a frame that a switch does not have a corresponding entry for in its MAC address table. When the switch receives such a frame, it doesn't know which port to forward it to because it has no record of the destination MAC address. In this case, the switch will flood the frame to all ports except the one it was received on.
PCs that do not match the destination MAC address will disregard and drop the frame.
The PC with the matching MAC address will receive the frame, process it, and continue with the communication, typically handling it through the OSI model (e.g., it will process the frame at Layer 2, pass it up to Layer 3 if needed, etc.).
The switch floods the frame when it doesn't know the destination, and only the device with the correct MAC address will process the frame.


MAC ADDRESS TABLE

Each Switch stores a DYNAMICALLY LEARNED MAC ADDRESS TABLE, using the SOURCE MAC ADDRESS of frames it receives.


When a Switch doesn't know the DESTINATION MAC ADDRESS of a frame (UNKNOWN UNICAST FRAME), it is forced to FLOOD the frame - Forward the frame out of ALL it's interfaces, except the one it received the packet from.

When a KNOWN Unicast Frame is known (MAC Address is recognized by the entry in the MAC ADDRESS TABLE), the frame is FORWARDED like normal.

Dynamic MAC addresses are removed from the MAC address table after 5 minutes of inactivity. 


Dynamically learned MAC address/ Dynamic MAC address.
A type of MAC address that a switch learns automatically when a device sends a frame on a network. The switch records the source MAC address in its MAC address table and associates it with the corresponding port. This allows the switch to forward future frames to the correct destination efficiently.

Unknown unicast frame=flood 
 

 Dynamic MAC Addresses are removed from the MAC ADDRESS TABLE every 5 minutes of inactivity.

all of the images are in my drive 
