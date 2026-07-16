these are y notes for day 3 
OSI Model 
“Open Systems Interconnection’ model
Created by the “International Organization for Standardization (ISO)
Functions divided into 7 layers
Application Layer- Closest to the end user 
Interactions with software application for example chrome
HTTP and HTTPS are layer 7 protocols.
(https;//www.cisco.com)
Indicates that https is being used to get the website and is used to show the user the browser. 
Functions
Identifying communication partners 
Synchronizing communication. 
Closest to the end user. 
Data is processed through the osi stack and goes down and it is called encapsulation when it reaches the physical layer it is sent to the neighboring system. Then the neighboring system does the opposite and goes from the physical layer to the application layer. This is called de-encapsulation. 
Both these processes are adjacent-layer interactions
Both application layers in the hosts are same layer interactions
Presentation layer 
Data in the application layer is in the “application format”
It needs to be ‘translated’ to a different format to be send over the network
The presentation layers job is to translate between application and network formats
For example, encryption of data as it is sent, and decryption of data as it is received.
Also translate between different Application-Layer formats. 
Basically translates data into the appropriate format
Session Layer
Controls dialogues(sessions) between communicating hosts
Establishes,manages, and terminates connections between the local application(for example the web browser) and remote applications( for example youtube) 
The purpose is to manage, establish, maintain, and terminate communication sessions between devices. 
Network engineers don't work with the 3 top layers. 
Data from the top 3 layers is sent to the bottom 4 layers it is sent to the neighboring device 
Transport layer 
Breaks large pieces of data into smaller segments which can be easily sent over the network and are less likely to cause transmission problems if errors occur.
If data is in small units it is less of a problem if one small piece gets lost.
Provides host-to-host communication
Provides end to end communication 
Provides a process to process communication. 
Layer 4 adds a header which is a layer 4 header
Network Layer
Adds another header to the information
Provides connectivity between end hosts on different networks (ie. outside of the lan) 
Provides logical addressing(ip addresses)
Provinces path selection between source and destination
Layer 3 selects the best path 
Routers operate at layer 3 
Data with a L4 header is called a segment
Data with a L4 and layer 3 header is called a packet
Data Link layer. 
Adds a layer 2 header and layer 2 trailer. 
Provinces node-to-node connectivity and data transfer(for example, pc to switch, switch to router, router to router. 
Defines how data is formatted for transmission over a physical medium(for example,copper UTP cables)
Detects and (possibly) corrects physical layer errors
Uses layer 2 addressing,separate from layer 3 addressong
Switches operate at layer 2
Looks for destination layer 2 addresses to determine where to send the data. 
Data with a L2 trailer, L2 header, L4 header and L3 header is called a frame
The frame is sent over the connection in the physical layer. It is not further encapsulated in layer 1. 
Physical layer. 
Defines physical characteristics of the medium used to transfer data between devices
For example,voltage levels, maximum transmission distances,physical connectors, cable specifications etc
Digital bits are converted into electrical(for wired connections) or radio(for wireless connections) signals. 
All of day 2s information is on the physical layer. 


Now with the complete frame it is sent over from the local device over the cable to the remote device. Now De-encapsulation takes place from the remote device. 

De-encapsulation

The data link layer translates the raw physical data into a complete frame again. Then the L2 header and trailer are removed. Leaving the L4 and L3 header on the data. Now the L3 header is removed leaving the L4 Segment . Now the L4 header is removed leaving the original data ready by the upper layers of the original device 





Segment- L4 pdu
Packet- L3 pdu
Bits- L1 pdu


"Please Do Not Throw Sausage Pizza Away"
Each letter stands for a layer in the OSI model from top to bottom:
P - Physical
D - Data Link
N - Network
T - Transport
S - Session
P - Presentation
A- Application 



TCP/IP Suite


Conceptual model and set of communications protocols used in the internet and other networks.
Known as TCP/Ip because those are two of the foundational protocols in the suite. 
Developed by the United States department of Defense through DARPA( Defense advanced research projects agency) 
Similar structure to the OSI, model but with fewer layers
This is the model actually in use in the modern networks. 
The OSI model still influences how network engineers think and talk about networks.
If people say there is a layer 2 problem in the network they are referring to the OSI models layer 2. 

OSI MODEL
- 7 APplication
- 6 Presentation
- 5 Session
- 4 Transport
- 3 Network
- 2 Data Link
- 1 Physial

TCP/IP Suite 
- 4 Application
- 3 Transport
- 2 Internet
- 1 Link




 
