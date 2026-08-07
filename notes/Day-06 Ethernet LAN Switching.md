

The preamble +SFD is usually not considered part of the Ethernet header
Therefore the size of the Ethernet header +trailer is only 18 bytes. (6+6+2+4)
The minimum size for an Ethernet frame is 64 bytes this includes the (Header+Payload {packet+Trailer}) 
64 bytes- 18 bytes (header + trailer size)= 46 bytes 
Therefore the minimum payload(packet) size is 46 bytes. 
If the payload is less than 46 bytes, padding bytes are added
Example 34-byte packet+12 byte padding=46 bytes 


Ethernet LAN switching 


When a PC sends a packet to a device with an unknown IP address, it uses an ARP Request.
ARP
ARP stands for ‘Address Resolution Protocol’
Arp  i used to discover the Layer 2 address (MAC address) of a known Layer 3 address (IP address)
THe arp process consists of two messages
ARP REQUEST- Sent by the device that wants to know the address of the other device (source message ) 
ARP REPLY- Sent to inform the requesting device of the mac address(Destination message) 
ARP Request is broadcast= sent to all hosts on the network besides the one it received the request from.
ARP Reply is unicast =sent only to one host (the host that sent the request) 
An ARP REQUEST frame has:

Source IP Address
Destination IP Address
Source MAC address
BROADCAST MAC Address - FFFF.FFFF.FFFF

An ARP REPLY frame has:

Source IP Address
Destination IP Address
Source MAC address
Destination MAC Address


Known unicast frame=forward(not flood)

PING

A network utility that is used to test reachability 
Measures round trip time 
Uses two messages 
ICMP Echo Request 
ICMP Echo Reply 
Is UNICAST
Command to use ping:
Ping (ip-address) 
By Default, a CISCO IOS sends 5 ICMP requests/replies (Default size is 100-bytes)

Default size of each ping is 100 bytes
A period (.) is a failed ping
An exclamation mark (!) is a successful ping
 


192.168.1.3 is being looked for by 192.168.1.1 its told over the broadcast 
192.168.1.3 is at 0c:2f:b0:6a:39:00
Now it sends the ICMP(ping) Source of pc 1 and destination of pc 3 for the request 
The replies have a source of pc 3 and a destination of pc 1 






USEFUL CISCO IOS COMMANDS (from Privileged EXEC mode)
PC1# show arp // shows hosts ARP table
SW1#show mac address-table // show the switches MAC table





MAC Address Table



Will show:

Vlan --- MAC Address --- Type --- Ports(interfaces) 
(Vlan = Virtual Local Area Network)

Dynamic addresses are removed from the mac address table after 5 minutes, This is called aging. If the Switch does not get any traffic from that MAC address for 5 minutes it will remove the entry from the mac address table


That clears the dynamic mac addresses


Put the address if you want to clear certain addresses.

This command clears it for specific interfaces whichever mac address is linked to it. 


SW1# clear mac address-table dynamic

// clears the entire switch's MAC table. // IF the optional MAC address is used, it will clear the SPECIFIC MAC address.

SW1 #clear mac address-table dynamic interface

// clears the MAC table entry of the Switch by its INTERFACE name.


Alot of my notes are screenshots from the videos once again they are in my personal drive






