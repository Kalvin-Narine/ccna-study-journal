OSI Model- Network Layer
Provides connectivity between end hosts on different networks(ie.outside of the LAN)
Provides logical addressing(IP addresses)
Provides path selection between source and destination
Routers operate at Layer 3 

ROUTING

SWITCHES (Layer 2 Devices) do not separate different networks. They connect and EXPAND networks within the same LAN.

By adding a ROUTER, however, between two SWITCHES, you create a SPLIT in the network; each with its own network IP address.

Example: 192.168.1.0/24 (255.255.255.0) 192.168.2.0/24 (255.255.255.0)


Routers have unique IP Addresses for EACH of their interface connections, depending on their location.

The IP Address for the ROUTER's G0/0 Interface is: 192.168.1.254/24

The IP Address for the ROUTER's G0/1 Interface is: 192.168.2.254/24

The first 3 octets represent the network itself in this example it is 192.168.1 and 192.168.2

The last 0 changes to represent the end host on the network that is the fourth octet 

The /24 are used to tell which part of the addresses represents the network and which represents the end hosts.

/24 means the first 3 groups of numbers represents the network 
The IP Address depends on the network address of the LAN it is connected to.

The NETWORK portion of given IP Address will be the same for all HOSTS on a given LAN.

Example:

192.168.1.100 192.168.1.105 192.168.1.205

All of these addresses are on the SAME Network because the NETWORK PORTION of their IP Address is the same (192.168.1) while the HOST part (100,105,205) is UNIQUE!

When a BROADCAST message hits a ROUTER, it does NOT continue onward. It stays within the LOCAL LAN (Switch/Hosts).


IP (or Internet Protocol) is the primary Layer 3 protocol in use today. Version 4 is the version in use in most networks

IPv4 header has more fields than then ethernet header

The IPv4 Headers contain a SOURCE IP Address and DESTINATION IP Address field.

The source ip address and destination ip address field are both 32-bits in length 


They stretch from 0-31 in the chart. 
Ip addresses are 32 bits(4 bytes) in length 

IPV4 Addresses 

192.168.1.254 (each decimal number represents 8 bits)
Ip addresses are 32 bits(4 bytes) in length 
Each octet of numbers represents 8 bits 

Translated to Binary:
192.168.1.254
11000000 . 10101000 . 00000001 . 11111110

Binary is base 2 meaning that every digit doubles
For example: 

 


8 bit groups are referred to as octets 




128-64-32-16-8-4-2-1
The values of each binary digit 


1 0 0 0 1 1 1 1
1 * 128 = 128
0 *  64 = 0
0 * 32 = 0 
0 * 16 = 0
1 * 8 = 8
1 * 4 = 4
1 * 2 = 2
1 * 1 = 1
128 + 8 + 4 + 2 + 1 = 143

The answer is 143.



0 1 1 1 0 1 1 0

0 * 128 = 0
1 * 64 = 64
1 * 32 = 32
1 * 16 = 16
0 * 8 = 0
1 * 4 = 4
1 * 2 = 2
0 * 1 = 0
64+32+16+4+2= 118

The answer is 118.

1 1 1 0 1 1 0 0

1 * 128 = 128
1 * 64 = 64
1 * 32 = 32
0 * 16 = 0
1 * 8 = 8
1 * 4 = 4
0 * 2 = 0
0 * 1 = 0
128+64+32+8+4= 236
The answer is 236. 

How do we convert a decimal number to binary 

We can take that number and start subtracting it from LEFT to RIGHT of our Binary slots.


Example: 

221 

221 - 128 = 93 so we place a 1 in the "128" slot

93 - 64 = 29 so we place another 1 in the "64" slot

29 - 32 isn't possible so we place a 0 in the "32" slot

29 - 16 = 13 so we place a 1 in the "16" slot

13 - 8 = 5 so we place a 1 in the "8" slot

5 - 4 = 1 so we place a 1 in the "4" slot

1 - 2 isn't possible so we put a 0 in the "2" slot

1 - 1 is possible so we put a 1 in the "1" slot
This, then, allows us to write out the BINARY number for 221.

It is : 11011101






Convert decimal 127 to binary 

127-128 is not possible so we place a 0 in the “128” slot
127-64=63 is possible so we place a 1 in the “64” slot 
63 - 32 is possible so we place 1 in "32"
31 - 16 is possible so we place 1 in "16"
15 - 8 is possible so we place 1 in "8"
7 - 4 is possible so we place 1 in "4"
3 - 2 is possible so we place 1 in "2"
1 is possible so we place1 in "1"

So 127, in BINARY, is 0111 1111


Decimal → binary

207 

207-128= 79 we place a 1 in this spot
79-64=15 we place a 1 on this spot
15-32 doesn't work so we put a 0 in this spot 
15-16 does not work so we put a 0 in this spot
15-8= works so we put a 1 in this spot
7-4= 3 works so we put a 1 in this spot
3-2=1 works so we put a 1 in this spot
1-1=0 works so we put a 1 in this spot
11001111


Binary ranges from 0-255 which is 256 values

IPV4 Addresses

IPv4 addresses are a series of 32 bits( split up into 4 octets) written in dotted decimal format to make it simpler for humans to read and understand. 

192.168.1.254/24

The /24 means that the first 24 bits of this ip address represent the network portion of the address and the remaining 8 represent the end host. 


It means the FIRST 24 BITS of this address represent the NETWORK portion of the address.

192.168.1 is the NETWORK PORTION (the first 3 OCTETS)

.254 is the HOST PORTION (the last OCTET)


The first 3 octets of the addresses are the same because they are apart of the same local network. 

Convert this binary number into an IPv4 Address
10011010010011100110111100100000

10011010 . 01001110 . 01101111 . 00100000
 
Converted into dotted decimal → 154.78.111.32/16 

The first 16 bits is the network portion meaning first two octets 
The last 2 octets are the host portion 

154.78 is the NETWORK PORTION 111.32 is the HOST PORTION

Another example:

00001100100000001111101100010111

00001100 . 10000000 . 11111011 . 00010111

4+8=12
128 
1+2+8+16+32+64+128=251 
1+2+4+16= 23

12.128.251.23/8 

12 is the NETWORK PORTION 128.251.23 is the HOST PORTION


IPV4 address classes

IPv4 addresses are split up into 5 different 'classes'. The class of an IPv4 is determined by the FIRST OCTET of the address.


We focus on using classes A, B and C 

Class D are reserved for multicast addresses
Class E addresses are used for experimental purposes and are not needed in the course 

The end of the class A range is 126 not 127 

LoopBack Addresses 

The 127 range is reserved for ‘’loopback addresses’ 
The address range 172.0.0.0-127.255.255.255
It is used to test the ‘network stack’ (think OSI,TCP/IP model) on the local device. 


IPV4 Addresses Classes 

The PREFIX LENGTH is the LENGTH of the NETWORK PORTION of the Address.









NETMASK:
A NETMASK is written like a Dotted Decimal IP Address



Class A: /8 → 255.0.0.0 which is 11111111.00000000.00000000.00000000
Class B: /16 → 255.255.0.0 which is 11111111.11111111.00000000.00000000
Class C:/24 →255.255.255.0 which is 11111111.11111111.11111111.00000000


Network Address


If the HOST PORTION of an IP ADDRESS is ALL 0's, it means it is the NETWORK ADDRESS = the identifier of the network itself.

A NETWORK ADDRESS cannot be assigned to a HOST. A NETWORK ADDRESS is the FIRST ADDRESS.



If the Host Portion of an Ip address is all 1's, it means it is the broadcast address for the network.
Broadcast addresses cannot be assigned to a HOST.

DESTINATION IP : 192.168.1.255 (Broadcast IP address) DESTINATION MAC : FFFF.FFFF.FFFF (Broadcast MAC address)

Because of the two 'reserved' addresses, the range of USABLE HOST ADDRESSES is 1 to 254.


 
How do you get the / number 
/x (where x is a number) represents the subnet mask, and it changes depending on the class of the IP address. Here's how it works for each class:

Class A:
Default subnet mask: /8

IP range: 1.0.0.0 to 127.255.255.255

Subnet mask in decimal: 255.0.0.0

The first 8 bits represent the network, and the remaining 24 bits are for host addresses.

Class B:
Default subnet mask: /16

IP range: 128.0.0.0 to 191.255.255.255

Subnet mask in decimal: 255.255.0.0

The first 16 bits represent the network, and the remaining 16 bits are for host addresses.

Class C:
Default subnet mask: /24

IP range: 192.0.0.0 to 223.255.255.255

Subnet mask in decimal: 255.255.255.0

The first 24 bits represent the network, and the remaining 8 bits are for host addresses.


images in personal drive. 
