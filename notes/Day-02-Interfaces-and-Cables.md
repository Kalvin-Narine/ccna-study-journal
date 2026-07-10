2. INTERFACES AND CABLES

RJ-45 (RJ = Registered Jack )



Ethernet is a collection of network protocols/standards 
Why do we need network protocols and standards?

Provide common communication standards over networks.
Provide common hardware standards to allow connectivity between devices.


Connections between devices operate at a set speed.

Bits and Bytes
0
1
1
0
0
1
1
1
8 bits = 1 byte

Speed is measured in bits per second, not bytes per second
Data on a hard drive is measured in bytes, not bits 

Size	# of Bits
1 kilobit (Kb)	= 1,000
1 megabit (Mb)   =	1,000,000
1 gigabit (Gb)  =	1,000,000,000
1 terabit (Tb)	 = 1,000,000,000,000


## Ethernet Standards (Copper)

### 10 Mbps Ethernet
- **Speed:** 10 Mbps
- **Common Name:** Ethernet
- **Standard:** IEEE 802.3i
- **Cable Type:** 10BASE-T
- **Maximum Transmission Distance:** 100 meters

### 100 Mbps Ethernet
- **Speed:** 100 Mbps
- **Common Name:** Fast Ethernet
- **Standard:** IEEE 802.3u
- **Cable Type:** 100BASE-T
- **Maximum Transmission Distance:** 100 meters

### 1 Gbps Ethernet
- **Speed:** 1 Gbps
- **Common Name:** Gigabit Ethernet
- **Standard:** IEEE 802.3ab
- **Cable Type:** 1000BASE-T
- **Maximum Transmission Distance:** 100 meters

### 10 Gbps Ethernet
- **Speed:** 10 Gbps
- **Common Name:** 10 Gigabit Ethernet
- **Standard:** IEEE 802.3an
- **Cable Type:** 10GBASE-T
- **Maximum Transmission Distance:** 100 meters



BASE = refers to Baseband Signaling

T = Twisted Pair

Most Ethernet uses copper cables.

UTP Cables → Unsheidled Twisted Pair  meaning no metallic shield
Twist protects against EMI (Electromagnetic Interference)

10/100BASE-T = 2 pairs (4 wires)

1000BASE-T
10GBase-t= 4 pairs (8 wires) 

The network interface card on a PC or server transmits data on pins 1 and 2, and the interfaces and the interface on a switch receive data on pins 1 and 2 

Each ethernet cable has a RJ-45 plug with 8 pins on the ends.

PCs Transmit(TX) data on Pins #1-2
Switches Receive(RX) data on Pins #1-2
PCs Receive(RC) data on Pins #3,6
Switches Transmit(TX) data on Pins #3,6

This is a full-duplex transmission of data 

This means that both devices can send and receive data at the same time, and no problems like collisions will occur because they use separate wires to transmit and receive data.
Now, if you change one device, so now it's a router and a switch 


Routers Transmit(TX) data on Pins #1-2
Routers Receive(RX) data on Pins #3,6
Switches Transmit(TX) data on Pins #3,6
Switches Receive(RX) data on Pins #1-2

Routers and PCs connect the same way with Switches.
Routers and switches are opposites when it comes to where they receive and transmit data. 
The cable used to connect is called a Straight-Through cable

A copper Ethernet cable has two RJ-45 connectors, one on each end. That's why it's a straight-through cable: pin 1 on one end connects straight to pin 1 on the other end. 

What if we want to connect a router to a router or a switch to a switch 

.We CANNOT use a "Straight-Through" cable. We MUST use a "Crossover" cable.

This cable swaps the pins on one end to allow connection to work.



PIN #1 -----> PIN #3 PIN #2 -----> PIN #6

PIN #3 -----> PIN #1 PIN #6 -----> PIN #2

The transmit pins on one side are connected to the receive pins on the other side. Now they can send data to each other.



Most modern-day devices now have AUTO MDI-X, which automatically detects which pins their neighbor is transmitting on and adjusts the pins they receive data on. 

This is only for old network setups. 

1000BASE-T/10GBASE-T = 4 pairs (8 wires)

Each wire pair is bidirectional so that it can transmit/receive much faster than 10/100BASE-T.



SFP Transceiver (Small form-factor pluggable) 
You connect those with fiber optic cables. 

Fiber optic cables send light over glass fibers rather than electricity over copper. 
They have to connect one to transit and one to receive data on each end. 

4 parts to a fiber-optic cable.



There are TWO types of fiber-optic cable.

Single-Mode:


Narrower than the multimode
Light enters at a single angle (mode) from a laser-based transmitter
Allows longer cables than both utp and  multimode fiber
More expensive than multimode fiber (due to more expensive laser- based SFP transmitters)

Multimode:

The core diameter is wider than single-mode fiber 
Allows multiple angles (modes) of light waves to enter the fiberglass core.
Allows longer cables than UTP, but shorter cables than single-mode fiber. 
## Fiber-Optic Ethernet Standards

### 1000BASE-LX
- **Standard:** IEEE 802.3z
- **Connection Speed:** 1 Gbps
- **Mode Support:** Multimode and Single-mode
- **Maximum Transmission Distance:**
  - 550 meters using Multimode fiber
  - 5 kilometers using Single-mode fiber

### 10GBASE-SR
- **Standard:** IEEE 802.3ae
- **Connection Speed:** 10 Gbps
- **Mode Support:** Multimode
- **Maximum Transmission Distance:** 400 meters

### 10GBASE-LR
- **Standard:** IEEE 802.3ae
- **Connection Speed:** 10 Gbps
- **Mode Support:** Single-mode
- **Maximum Transmission Distance:** 10 kilometers

### 10GBASE-ER
- **Standard:** IEEE 802.3ae
- **Connection Speed:** 10 Gbps
- **Mode Support:** Single-mode
- **Maximum Transmission Distance:** 40 kilometers


UTP vs Fiber-Optic Cabling:


UTP are:

Lower cost than fiber-optic.
Shorter maximum distance than fiber-optic (~100m).
Can be vulnerable to EMI (Electromagnetic Interference).
RJ45 ports used with UTP are cheaper than SFP ports.
Emit (leak) a faint signal outside of cable, which can be copied (security risk).
Fiber-Optic:

Higher cost than UTP.
Longer maximum distance than UTP.
No vulnerability to EMI.
SFP ports are more expensive than RJ45 ports (single-mode is more expensive than multimode).
Does not emit any signal outside of the cable (no security risk).


i have screenshots and diagrams from the video just in my personal google drive because github isnt leting me paste images. 

